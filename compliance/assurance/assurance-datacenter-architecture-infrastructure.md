---
title: Architettura e infrastruttura del datacenter
description: Panoramica dell'architettura e dell'infrastruttura del datacenter Microsoft.
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.localizationpriority: medium
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
f1.keywords:
- NOCSH
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 44876abef95f269d454139fd721194ef3d48dcd4
ms.sourcegitcommit: cf424cb1e7c12048120977f294f780b776119a96
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/11/2021
ms.locfileid: "60265118"
---
# <a name="datacenter-architecture-and-infrastructure"></a>Architettura e infrastruttura del datacenter

I datacenter Microsoft sono progettati per implementare una strategia di difesa approfondita, utilizzando più livelli di misure di sicurezza per proteggere in modo affidabile l'architettura cloud e l'infrastruttura di supporto. La ridondanza è integrata in tutti i sistemi a più livelli per supportare la disponibilità del datacenter.

Microsoft ha strutture di datacenter altamente protette distribuite in tutto il mondo creando un'infrastruttura datacenter distribuita, che supporta migliaia di servizi online. Questa infrastruttura distribuita a livello globale è progettata per avvicinare le applicazioni agli utenti, mantenere la residenza dei dati e offrire ai clienti opzioni complete di conformità e resilienza.

Le aree geografiche sono insiemi di datacenter interconnessi tramite una rete di grandi dimensioni e resiliente. Le aree geografiche sono organizzate in aree geografiche, per consentire ai clienti con residenza e conformità di dati specifici di mantenere i propri dati e applicazioni vicini. La tolleranza di errore incorporata consente alle aree geografiche di sopportare un errore di area completa tramite la connessione all'infrastruttura di rete dedicata ad alta capacità.

Le posizioni fisicamente separate all'interno di un'area sono denominate aree di disponibilità, ognuna delle quali è costituito da uno o più datacenter dotati di alimentazione, raffreddamento e rete indipendenti. Le aree di disponibilità consentono l'esecuzione di applicazioni mission-critical con la replica a disponibilità elevata e a bassa latenza.

I data center distribuiti geograficamente consentono a Microsoft di avvicinare i servizi ai clienti, ridurre la latenza di rete e consentire backup e failover con ridondanza geografica.

## <a name="availability"></a>Disponibilità

I datacenter Microsoft sono progettati per fornire una disponibilità del 99,999% per soddisfare i contratti di servizio dei clienti e le esigenze di servizio. Microsoft investe in modo significativo nelle operazioni globali, nella gestione, nelle reti e nella sustainability delle strutture che offrono servizi 24x7x365.

## <a name="compliance-standards-and-requirements"></a>Standard e requisiti di conformità

Microsoft ha investito oltre $15 miliardi per la creazione dell'infrastruttura globale e oltre 9 miliardi di dollari in ricerca e sviluppo per aumentare l'efficienza e guidare l'innovazione. Di conseguenza, i data center di Microsoft si stanno evolvendo a un ritmo più rapido rispetto a molte strutture del settore e pertanto non seguono requisiti prescrittivi delineati dagli standard tradizionali del datacenter. Oltre alla vasta gamma di informazioni operative che derivano dall'esecuzione di uno dei più grandi portfolio di datacenter al mondo, Microsoft utilizza i dati del Manuale D'oro IEEE e software di simulazione dell'affidabilità di terze parti per migliorare continuamente i nostri standard di progettazione dei datacenter. I datacenter Microsoft vengono controllati in modo approfondito nell'ambito di diversi controlli normativi, come descritto nel portfolio di conformità. Il livello di maturità nei data center Microsoft può essere valutato tramite il portfolio di conformità e, in particolare, per la resilienza, la certificazione ISO 22301.

Mentre Microsoft gestisce programmi allineati allo spirito dell'infrastruttura di telecomunicazioni ANSI/TIA-942 di Datacenters Standard, parti di questo standard non sono applicabili a Microsoft o sono in conflitto con altri requisiti normativi e/o specifici del paese. Inoltre, Microsoft ha scelto di utilizzare un approccio più basato sulle prestazioni per soddisfare le esigenze dei clienti.

## <a name="data-and-network-redundancy"></a>Ridondanza dei dati e della rete

Le strutture dei data center critiche usano sistemi ridondanti a più livelli per fornire supporto in caso di errori e ridurre al minimo le interruzioni del servizio. L'archiviazione con ridondanza locale a livello di disco protegge i dati all'interno di un'area, e l’archiviazione con ridondanza geografica fornisce ridondanza all'interno dell'area. Al fine di garantire comunicazioni di rete affidabili, Microsoft è proprietaria e utilizza diversi collegamenti in fibra ottica e hardware ridondante per proteggere i componenti critici da errori o interruzioni del servizio.

La replica geografica viene utilizzata per fornire ridondanza a posizioni geografiche alternative. La durata dei dati viene ottenuta replicando in modo sincrono i dati tra più database in datacenter diversi. I test di ripristino vengono eseguiti per tutti i dati di backup di proprietà del cloud. Il ripristino di emergenza viene ottenuto tramite la replica asincrona in un datacenter in un'area geografica diversa.

## <a name="capacity"></a>Capacità

Cloud Operations è un team dedicato alla capacità che prevede requisiti futuri per garantire che la capacità necessaria sia strutturata e disponibile per l'uso interno e del cliente. I sistemi vengono monitorati per garantire prestazioni del servizio accettabili, disponibilità, utilizzo del servizio, utilizzo dello spazio di archiviazione, latenza di rete e capacità del registro di controllo. Microsoft protegge inoltre i datacenter dagli effetti degli attacchi Denial of Service sulla larghezza di banda, sulla capacità transazionale e sulla capacità di archiviazione.

Tutti i team di servizio includono la pianificazione della capacità come funzionalità chiave dei modelli di datacenter e dei piani di replica dei dati per garantire la capacità necessaria per l'elaborazione delle informazioni, le telecomunicazioni e il supporto ambientale.

## <a name="power"></a>Alimentazione

I data center di Microsoft hanno alimentatori ininterrotti (UPS) dedicati 24x7 e supporto per l'alimentazione di emergenza, che include generatori in loco che forniscono alimentazione di backup. Le normali attività di manutenzione e verifica vengono eseguite sia per gli UPS che per i generatori, e i team delle operazioni hanno accordi contrattuali con i fornitori locali per l'erogazione di combustibile di emergenza. I data center dispongono anche di un centro operativo dedicato per monitorare i sistemi di alimentazione, compresi i componenti elettrici critici.

I datacenter Microsoft sono dotati di spazi di protezione e di etichettatura appropriata per i cavi. Le apparecchiature dell'infrastruttura di alimentazione sono collocate in ambienti progettati per proteggere dai rischi ambientali. Tutte le risorse di tutti i servizi online portatili devono essere bloccate o bloccate per garantire la protezione da furti o danni al movimento. I cavi di alimentazione vengono eseguiti sotto i piani, in testa nei vassoi dei cavi e all'interno degli archivi per la protezione da parti in movimento e danni accidentali. Tutti gli spazi elettrici sono dietro lettori di carte o blocchi di tasti aggiuntivi in base alle esigenze. I corridoi di accesso, gli accessi esterni e le attrezzature sono tutti monitorati tramite videosorveglianza. I sistemi di alimentazione utilizzano anche la ridondanza come forma di protezione, con più alimentatori/utility che alimentano la struttura e i generatori e i sistemi UPS.

Per il sistema di informazioni viene implementato un alimentatore alternativo a lungo termine in grado di mantenere l'alimentazione in una capacità operativa minimamente necessaria. Quando l'alimentazione non riesce o scende a un livello di voltaggio inaccettabile, i sistemi UPS vengono immediatamente online. In questo modo si garantisce una potenza sufficiente per l'esecuzione dei server fino a quando i generatori non possono assumere il controllo. I generatori di emergenza forniscono alimentazione di backup per interruzioni estese, manutenzione pianificata e possono utilizzare il centro dati con riserve di carburante in loco in caso di emergenza naturale.

I datacenter Microsoft (sia in leasing che completamente gestiti) implementano l'illuminazione di emergenza sotto forma di illuminazione di emergenza in sovraccarico su circuiti dedicati di cui è stato eseguito il backup da up up e sistemi generatori. L'illuminazione automatica di emergenza viene implementata in conformità al Codice di sicurezza della vita (NFPA) dell'Associazione nazionale antincendio (NFPA) o al codice/legge locale applicabile. Se l'alimentazione dell'utilità viene persa, l'illuminazione di emergenza passa automaticamente all'alimentazione fornita dai sistemi UPS e generatori. I sistemi di illuminazione di emergenza all'interno dei datacenter vengono sottoposti a manutenzione ordinaria per garantire che rimangano nell'ordine di lavoro corretto.

## <a name="maintenance"></a>Manutenzione

I criteri e le procedure di manutenzione del sistema sono in atto in conformità con lo Standard di sicurezza fisica e ambientale dei Servizi *online di Microsoft.* Tutte le attrezzature e i sistemi Microsoft vengono regolarmente gestiti per garantire l'efficienza operativa. La manutenzione di qualsiasi attrezzatura o sistema deve essere eseguita in conformità alle raccomandazioni del produttore, eseguita da personale autorizzato e registrata in un ticket di manutenzione.

Esistono due team di asset che gestiscono diversi tipi di sistemi:

- **Team dell'ambiente critico (CE):**

    - CE è il team che fornisce la gestione delle strutture per i sistemi elettrici, meccanici e fisici che costituiscono l'infrastruttura operativa della struttura. Il team CE pianifica, esegue, documenta e rivede tutte le attività di manutenzione eseguite sui componenti CE. I datacenter Microsoft si basano su un sistema computerizzato per gestire le pianificazioni di manutenzione e gli ordini di lavoro.
    - La gestione del datacenter (DCM) è responsabile di tutta la manutenzione CE eseguita in locale o in remoto. La manutenzione CE è prescritta in documenti dettagliati necessari denominati Metodi di procedura (MOP). I mop vengono esaminati/approvati dalla gestione del datacenter prima di qualsiasi inizio di lavoro.

- **Team servizi sito:**

    - Site Services è il team che fornisce la manutenzione degli asset dei servizi online Microsoft che si trovano nel datacenter Microsoft. Il team dc site services fornisce un servizio di correzione smart hands/break per gli asset appartenenti ai servizi di provisioning delle proprietà dal datacenter. Ad esempio, gli asset che richiedono la manutenzione fisica potrebbero richiedere il servizio smart hands al team dc Site Services. Tutti i lavori di Site Services sulle risorse Microsoft vengono pianificati, eseguiti, documentati e esaminati nei ticket di lavoro all'interno dello strumento di ticket del flusso di lavoro e nessun lavoro può verificarsi senza un ticket di lavoro approvato.
    - Il responsabile del programma tecnico (TPM) e il team DCM sono responsabili di tutte le attività di Site Services che si verificano nel datacenter e che richiedono il trasferimento dell'asset fuori sede. La manutenzione di Site Services viene eseguita in aree del datacenter controllate e protette da meccanismi di sicurezza fisici.

Se i componenti CE devono essere rimossi dalla struttura, la gestione dell'attrezzatura è approvata da DCM. Nella maggior parte dei casi, i componenti CE ricevono la manutenzione sul posto e non vengono rimossi dalla struttura. Gli asset di proprietà (ad esempio, dispositivi di rete o server) che richiedono il trasferimento fuori sede devono avere l'approvazione esplicita del proprietario dell'asset.

I supporti digitali all'interno del cloud potrebbero non essere trasportati dallo spazio di colocation a meno che non vengano spostati per essere distrutti. Quando questi asset devono essere distrutti, vengono archiviati in contenitori di archiviazione bloccati che sono sotto la copertura della fotocamera CCTV. Quando gli asset sono pronti per essere distrutti, un responsabile della sicurezza fisica e un dipendente a tempo pieno Di Microsoft da Gestione asset devono scortare il cestino bloccato dallo spazio di colocation a dove deve verificarsi la triturazione in sede. Quando la triturazione avviene nel datacenter e sotto la supervisione di Microsoft, gli asset Microsoft non lasciano le aree controllate del datacenter.

Tutte le attività di manutenzione devono essere approvate prima dell'inizio del lavoro, incluso l'accesso agli strumenti di manutenzione del sistema. Microsoft Infrastructure ha implementato il controllo degli strumenti di manutenzione creando un livello di accesso all'interno dello strumento DCAT (Datacenter Access Tool). Ogni struttura contiene una casella di blocco fisica o una sala controllata dall'accesso per l'archiviazione di strumenti di manutenzione specializzati. L'accesso alla casella di blocco o alla sala di archiviazione è controllato nello strumento DCAT per impedire l'accesso non autorizzato agli strumenti di manutenzione. Questo programma garantisce che solo il personale con accesso approvato possa accedere agli strumenti. Il team di Servizi sito esegue controlli di inventario di routine per verificare lo stato di tutti gli strumenti. Su base trimestrale, il team di gestione del datacenter e i team di sicurezza fisici eseguono controlli dell'elenco di accesso DCAT per mantenere l'elenco di accesso del personale addetto alla manutenzione. Le terminazioni o i trasferimenti del personale si riflettono immediatamente tramite un aggiornamento manuale dell'elenco di accesso. L'accesso alla casella di blocco o alla sala di archiviazione di manutenzione viene monitorato nei registri del lettore di badge di accesso, che sono disponibili per eventuali indagini.

Il team di Site Services gestisce un inventario degli strumenti di manutenzione approvati da utilizzare all'interno del datacenter. Il personale addetto alla manutenzione viene indirizzato all'uso degli strumenti di manutenzione forniti. L'approvazione di Gestione datacenter (DCM) è necessaria per utilizzare gli strumenti non forniti dal datacenter. Gli strumenti fisici sono esenti da questo tipo di controllo.

I data center Microsoft mantengono il personale di manutenzione residente per supportare i sistemi critici dell'infrastruttura del datacenter (il team dell'ambiente critico) e le operazioni del datacenter (il team di Site Services). I team dell'ambiente critico e dei servizi del sito hanno identificato i componenti critici del sistema di sicurezza e tecnologia che mantengono i pezzi di ricambio per il sito. Viene eseguito il provisioning dei servizi del sistema di informazioni critiche da più datacenter per evitare un'interruzione del servizio a causa di un incidente in uno dei datacenter.
