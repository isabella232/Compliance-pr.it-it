---
title: Exchange Online Resilienza dei dati in Microsoft 365
description: In questo articolo viene fornita una spiegazione dei vari aspetti della resilienza dei dati in Exchange Online e Microsoft 365.
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 8952d492c4427d5f4af64a853adaaf15303e8caf
ms.sourcegitcommit: fb379d1110a9a86c7f9bab8c484dc3f4b3dfd6f0
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/23/2021
ms.locfileid: "53088635"
---
# <a name="exchange-online-data-resiliency-in-microsoft-365"></a>Exchange Online resilienza dei dati in Microsoft 365

>[!IMPORTANT]
>Mentre continuiamo a investire in modi diversi per conservare il contenuto delle cassette postali, annunciamo il ritiro delle esenzioni di In-Place nell'interfaccia di amministrazione di Exchange (EAC) in Exchange Online. A partire dal 1° luglio 2020, non sarà possibile creare nuove In-Place esenzioni. Tuttavia, sarà comunque possibile gestire In-Place blocchi nell'interfaccia di amministrazione di Exchange o utilizzando il cmdlet **Set-MailboxSearch** in Exchange Online PowerShell. Tuttavia, a partire dal 1° ottobre 2020, non sarà possibile gestire le In-Place esenzioni. Sarà possibile rimuoverli solo nell'interfaccia di amministrazione di Exchange o utilizzando il cmdlet **Remove-MailboxSearch.** L'In-Place delle Exchange Server e Exchange le distribuzioni ibride saranno ancora supportate. Per ulteriori informazioni sul ritiro delle In-Place in Exchange Online, vedere [Ritiro degli strumenti di eDiscovery legacy.](/microsoft-365/compliance/legacy-ediscovery-retirement)

Un In-Place conserva tutto il contenuto delle cassette postali, inclusi gli elementi eliminati e le versioni originali degli elementi modificati. Tutti questi elementi delle cassette postali vengono restituiti in una ricerca di [eDiscovery in locale](/exchange/security-and-compliance/in-place-ediscovery/in-place-ediscovery). Quando si posiziona un blocco In-Place sulla cassetta postale di un utente, anche il contenuto nella cassetta postale di archiviazione corrispondente (se abilitata) viene messo in attesa e restituito in una ricerca eDiscovery.

Esistono due tipi di danneggiamento che possono influire su un database di Exchange: il danneggiamento fisico, che in genere è causato da problemi hardware (in particolare hardware di archiviazione) e il danneggiamento logico, che si verifica a causa di altri fattori. In genere, esistono due tipi di danneggiamento logico che possono verificarsi all'interno di un database Exchange database:

- **Danneggiamento logico del** database - Il checksum della pagina del database corrisponde, ma i dati nella pagina sono er logico. Ciò può verificarsi quando il motore di database (Extensible Archiviazione Engine (ESE)) tenta di scrivere una pagina di database e anche se il sistema operativo restituisce un messaggio di esito positivo, i dati non vengono mai scritti sul disco o vengono scritti nella posizione errata. Questo viene definito *rilevamento flush*. ESE include numerose funzionalità e misure di sicurezza progettate per impedire il danneggiamento fisico di un database e altri scenari di perdita di dati. Per evitare che gli scaricamenti persi perdano i dati, ESE include un meccanismo di rilevamento dello scaricamento perso nel database insieme a una funzionalità (ripristino a pagina singola) per correggerlo.
- **Danneggiamento logico** dell'archivio: i dati vengono aggiunti, eliminati o manipolati in modo che l'utente non si aspetti. Questi casi sono causati da applicazioni di terze parti. In genere si tratta di un danneggiamento nel senso che l'utente la visualizza come danneggiata. L'archivio di Exchange considera la transazione che ha causato il danneggiamento della partizione logica come una serie di operazioni MAPI valide. Le [funzionalità di archiviazione](/exchange/security-and-compliance/create-or-remove-in-place-holds) sul posto in Exchange Online protezione dal danneggiamento logico dell'archivio (perché impedisce l'eliminazione definitiva del contenuto da parte di un utente o di un'applicazione). 

Exchange Online esegue diverse verifiche di coerenza sui file di registro replicati durante l'ispezione e la riesecuzione dei registri. Questi controlli di coerenza impediscono che il danneggiamento fisico venga replicato dal sistema. Ad esempio, durante l'ispezione del registro, è disponibile un controllo di integrità fisica che verifica il file di registro e verifica che il checksum registrato nel file di registro corrisponda al checksum generato in memoria. Inoltre, l'intestazione del file di registro viene esaminata per verificare che la firma del file di registro registrata nell'intestazione del registro corrisponda a quella del file di registro. Durante la riesecuzione del registro, il file di registro viene sottoposto a un ulteriore controllo. Ad esempio, l'intestazione del database contiene anche la firma del registro che viene confrontata con la firma del file di registro per assicurarsi che corrispondano. 

La protezione contro il danneggiamento dei dati delle cassette postali in Exchange Online viene ottenuta utilizzando Exchange Native Data Protection, una strategia di resilienza che sfrutta la replica a livello di applicazione tra più server e più datacenter insieme ad altre funzionalità che consentono di proteggere i dati dalla perdita a causa di danneggiamenti o altri motivi. Queste funzionalità includono funzionalità native gestite da Microsoft o dall'Exchange Online stessa applicazione, ad esempio:

- [Gruppi di disponibilità dei dati](/exchange/back-up-email)
- Correzione bit singolo 
- Analisi database online 
- Rilevamento scaricamento perso 
- Ripristino a pagina singola 
- Servizio di replica delle cassette postali 
- Controlli dei file di registro 
- Distribuzione nel file system resiliente 

Per ulteriori informazioni sulle caratteristiche native elencate in precedenza, selezionare i collegamenti ipertestuali e vedere quanto segue per ulteriori informazioni e per informazioni dettagliate sugli elementi senza collegamenti ipertestuali. Oltre a queste funzionalità native, Exchange Online include anche funzionalità di resilienza dei dati che i clienti possono gestire, ad esempio: 
- [Ripristino di un singolo elemento (abilitato per impostazione predefinita)](/exchange/recipients-in-exchange-online/manage-user-mailboxes/recover-deleted-messages) 
- [Conservazione in locale e per controversia legale](/exchange/security-and-compliance/in-place-and-litigation-holds) 
- [Conservazione elementi eliminati e Soft-Deleted cassette postali (entrambe abilitate per impostazione predefinita)](/exchange/recipients-in-exchange-online/delete-or-restore-mailboxes) 

## <a name="database-availability-groups"></a>Gruppi di disponibilità del database 
Ogni database delle cassette postali in Microsoft 365 è ospitato in un gruppo di disponibilità del [database (DAG)](/exchange/back-up-email) e replicato in datacenter geograficamente separati all'interno della stessa area geografica. La configurazione più comune è quattro copie del database in quattro datacenter. Tuttavia, alcune aree geografiche hanno meno datacenter (i database vengono replicati in tre datacenter in India e due datacenter in Australia e Giappone). Tuttavia, in tutti i casi, ogni database delle cassette postali dispone di quattro copie distribuite tra più datacenter, garantendo in tal modo che i dati delle cassette postali siano protetti da errori software, hardware e persino datacenter. 

Di queste quattro copie, tre di esse sono configurate come altamente disponibili. La quarta copia è configurata come [copia ritardata del database.](/Exchange/high-availability/manage-ha/activate-lagged-db-copies) La copia ritardata del database non è destinata al ripristino di singole cassette postali o agli elementi delle cassette postali. Il suo scopo è fornire un meccanismo di ripristino per il raro evento di danneggiamento logico a livello di sistema e catastrofico. 

Le copie del database ritardate in Exchange Online sono configurate con un intervallo di riesecuzione del file di registro di sette giorni. Inoltre, gestione riesecuzione riesecuzione di Exchange è abilitata per fornire la riproduzione dinamica del file di registro per le copie ritardate per consentire alle copie ritardate del database di auto-ripristinare e gestire l'aumento dei file di registro. Anche se le copie ritardate del database vengono utilizzate in Exchange Online, è importante comprendere che non si tratta di un backup point-in-time garantito. Le copie ritardate del database in Exchange Online hanno una soglia di disponibilità, in genere circa il 90%, a causa dei periodi in cui il disco contenente una copia ritardata viene perso a causa di un errore del disco, la copia ritardata diventa una copia altamente disponibile (a causa della riproduzione automatica), nonché i periodi in cui la copia del database ritardata sta ricostruendo la coda di riesecuzione del registro. 

## <a name="transport-resilience"></a>Resilienza del trasporto 
Exchange Online include due funzionalità principali di resilienza del trasporto: Ridondanza shadow e Rete sicura. La ridondanza shadow mantiene una copia ridondante di un messaggio mentre è in transito. Rete sicura mantiene una copia ridondante di un messaggio dopo che il messaggio è stato recapitato correttamente. 

Con la ridondanza shadow, ogni Exchange Online di trasporto crea una copia di ogni messaggio ricevuto prima che riconosca la corretta ricezione del messaggio al server di invio. In questo modo tutti i messaggi nella pipeline di trasporto vengono ridondanti durante il transito. Se Exchange Online il messaggio originale è stato perso durante il transito, viene rieliverata una copia ridondante del messaggio. 

Rete sicura è una coda di trasporto associata al servizio di trasporto su un server Cassette postali. In questa coda vengono archiviate le copie dei messaggi elaborati correttamente dal server. Quando un errore del server o del database delle cassette postali richiede l'attivazione di una copia non aggiornata del database delle cassette postali, i messaggi nella coda Rete sicura vengono reinvii automaticamente alla nuova copia attiva del database delle cassette postali. Anche Rete sicura è ridondante, eliminando così il trasporto come singolo punto di errore. Utilizza il concetto di rete sicura principale e rete sicura shadow in cui se la rete sicura principale non è disponibile per più di 12 ore, le richieste di reinvio diventano richieste di reinvio shadow e i messaggi vengono reinviati dalla Rete sicura shadow.

I reinvii dei messaggi dalla rete sicura vengono avviati automaticamente dal componente Active Manager del servizio replica di Microsoft Exchange che gestisce i gruppi di disponibilità del database e le copie del database delle cassette postali. Non sono necessarie azioni manuali per inviare di nuovo i messaggi da Rete sicura. 

## <a name="single-bit-correction"></a>Correzione bit singolo 
ESE include un meccanismo per rilevare e risolvere gli errori CRC a bit singolo (noti anche come capovolgimenti a bit singolo) che sono il risultato di errori hardware (e di conseguenza rappresentano danneggiamenti fisici). Quando si verificano questi errori, ESE li corregge automaticamente e registra un evento nel registro eventi. 

## <a name="online-database-scanning"></a>Analisi database online 
L'analisi dei database online (nota anche come somma del controllo del *database)* è il processo in cui ESE utilizza una verifica della coerenza del database per leggere ogni pagina e verificare il danneggiamento delle pagine. Lo scopo principale è rilevare il danneggiamento fisico e gli scaricamenti persi che potrebbero non essere rilevati dalle operazioni transazionali. L'analisi del database esegue anche operazioni di arresto anomalo post-archivio. Lo spazio può essere perso a causa di arresti anomali e l'analisi dei database online rileva e recupera lo spazio perso. Il sistema è progettato con l'aspettativa che ogni database sia analizzato completamente una volta ogni sette giorni. 

## <a name="lost-flush-detection"></a>Rilevamento scaricamento perso 
Uno scaricamento perso si verifica quando un'operazione di scrittura del database restituita dal sottosistema del disco o dal sistema operativo come completato non è stata effettivamente scritta su disco o è stata scritta in una posizione errata. Gli eventi imprevisti di scaricamento persi possono causare un danneggiamento logico del database, pertanto per evitare che gli scaricamenti persi possano causare la perdita di dati, ESE include un meccanismo di rilevamento dello scaricamento perso. Quando le pagine del database vengono scritte in copie passive, viene eseguita una verifica per gli scaricamenti persi nella copia attiva. Se viene rilevato uno scaricamento perso, ESE può ripristinare il processo utilizzando un processo di applicazione di patch alle pagine. 

## <a name="single-page-restore"></a>Ripristino a pagina singola 
Il ripristino a pagina singola, noto anche come applicazione di *patch* alle pagine, è un processo automatico in cui le pagine di database danneggiate vengono sostituite da copie integre di una replica integra. Il processo di ripristino di una pagina danneggiata dipende dal fatto che la copia del database sia attiva o passiva. Quando una copia del database attiva rileva una pagina danneggiata, può copiare una pagina da una delle relative repliche, a condizione che la pagina copiata sia aggiornata. Questo processo viene ottenuto inserendo una richiesta per la pagina nel flusso di registro, che è alla base della replica del database delle cassette postali. Non appena una replica incontra la richiesta di pagina, risponde inviando una copia della pagina alla copia del database richiedente. Il ripristino a pagina singola fornisce inoltre un meccanismo di comunicazione asincrono per l'attivo per richiedere una pagina alle repliche, anche se le repliche sono attualmente offline. 

In caso di danneggiamento in una copia passiva del database, inclusa una copia ritardata del database, poiché tali copie si trova sempre dietro la copia attiva, è sempre possibile copiare qualsiasi pagina dalla copia attiva a una copia passiva. Una copia passiva del database è per sua natura estremamente disponibile, quindi durante il processo di applicazione di patch alle pagine, la riproduzione dei registri viene sospesa, ma la copia del registro continua. La copia passiva del database recupera una copia della pagina danneggiata dalla copia attiva, attende che il file di registro che soddisfi il requisito di generazione del registro massimo richiesto sia copiato e esaminato e quindi la pagina danneggiata sia stata patchata. Una volta che la pagina è stata patchata, la riesecuzione del log riprende. Il processo è lo stesso per la copia ritardata del database, con la differenza che il database ritardato riproduce innanzitutto tutti i file di registro necessari per ottenere uno stato patchable. 

## <a name="mailbox-replication-service"></a>Servizio di replica delle cassette postali 
Lo spostamento delle cassette postali è una parte fondamentale della gestione di un servizio di posta elettronica su larga scala. Esistono sempre tecnologie aggiornate, hardware e aggiornamenti delle versioni da gestire, quindi avere un sistema affidabile e limitato che consenta ai nostri tecnici di eseguire questo lavoro mantenendo gli spostamenti delle cassette postali trasparenti per gli utenti (assicurando che rimangano online durante tutto il processo) è fondamentale e garantire che il processo si eserciti in modo semplificato mancheranno le dimensioni delle cassette postali. 

Il Exchange servizio di replica delle cassette postali (MRS) è responsabile dello spostamento delle cassette postali tra database. Durante lo spostamento, MRS esegue una verifica di coerenza su tutti gli elementi all'interno della cassetta postale. Se viene rilevato un problema di coerenza, MRS correggerà il problema o salterà gli elementi danneggiati, rimuovendo così il danneggiamento dalla cassetta postale. 

Poiché MRS è un componente di Exchange Online, è possibile apportare modifiche al codice per risolvere nuove forme di danneggiamento rilevate in futuro. Ad esempio, se viene rilevato un problema di coerenza che mrs non è in grado di risolvere, è possibile analizzare il danneggiamento, modificare il codice MRS e correggere l'incoerenza (se si comprende come fare). 

## <a name="log-file-checks"></a>Controlli dei file di registro 
Tutti i file di registro delle transazioni generati da Exchange database vengono sottoposti a diverse forme di verifica della coerenza. Quando viene creato un file di registro, viene scritto un modello di bit e quindi viene eseguita una serie di scritture di log. Questa struttura consente Exchange Online di eseguire una serie di controlli (svuotamento perso, CRC e altri controlli) per convalidare ogni file di registro durante la scrittura e di nuovo durante la replica. 

## <a name="deployment-on-resilient-file-system"></a>Distribuzione nel file system resiliente 
Per evitare che si verifichino danneggiamenti a livello di file system, Exchange Online viene distribuito su partizioni ReFS (Resilient File System) per fornire funzionalità di ripristino migliorate. ReFS è un file system in Windows Server 2012 e versioni successive progettato per essere più resiliente contro il danneggiamento dei dati, massimizzando così la disponibilità e l'integrità dei dati. In particolare, ReFS apporta miglioramenti al modo in cui i metadati vengono aggiornati, che offrono una protezione migliore per i dati e riducono i casi di danneggiamento dei dati. Vengono inoltre utilizzati checksum per verificare l'integrità dei dati e dei metadati dei file, garantendo che il danneggiamento dei dati sia facilmente individuato e riparato. 

Exchange Online sfrutta diversi vantaggi di ReFS: 
- Maggiore resilienza nell'integrità dei dati significa meno incidenti di danneggiamento dei dati. Riducendo il numero di eventi imprevisti di danneggiamento, si riduce il numero di reseeded dei database non necessari. 
- Checksum in esecuzione sui metadati che consentono di rilevare i casi di danneggiamento in modo sempre più deterministico, consentendoci di correggere il danneggiamento dei dati dei clienti prima che si verifichino errori di grigio nei volumi di dati.
- Progettato per funzionare correttamente con set di dati di grandi dimensioni, ovvero petabyte e dimensioni maggiori, senza un impatto sulle prestazioni
- Supporto per altre funzionalità usate da Exchange Online, ad esempio la crittografia BitLocker. 

Exchange Online vantaggi anche da altre funzionalità di ReFS: 
- **Integrità (integrità Flussi)** - ReFS archivia i dati in modo da proteggerli da molti degli errori comuni che in genere possono causare la perdita di dati. Microsoft 365 La ricerca usa l'Flussi integrità per facilitare il rilevamento precoce del danneggiamento del disco e i checksum del contenuto dei file. La funzionalità consente inoltre di ridurre gli incidenti di danneggiamento causati da "Scritture diserte" (quando un'operazione di scrittura non viene completata a causa di interruzioni dell'alimentazione e così via). 
- **Disponibilità (recupero):** ReFS assegna la priorità alla disponibilità dei dati. Storicamente, i file system erano spesso soggetti a danneggiamenti dei dati che richiedevano che il sistema fosse portato offline per la riparazione. Sebbene raro, se si verifica un danneggiamento, ReFS implementa il recupero, una funzionalità che rimuove i dati danneggiati dallo spazio dei nomi in un volume reale e garantisce che i dati validi non siano influenzati da dati danneggiati non ripristinabili. L'applicazione della funzionalità di recupero e l'isolamento del danneggiamento dei dati Exchange Online volumi di database significa che è possibile mantenere integri i database non interessati in un volume danneggiato tra il momento del danneggiamento e l'azione di ripristino. Questa struttura aumenta la disponibilità dei database che normalmente sarebbero interessati da tali problemi di danneggiamento del disco. 
