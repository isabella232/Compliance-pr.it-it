---
title: Crittografia per Skype, OneDrive, SharePoint ed Exchange
description: 'Riepilogo: Descrizione della crittografia per Skype, OneDrive, SharePoint, Microsoft Teams ed Exchange Online.'
ms.author: krowley
author: kccross
manager: laurawi
ms.reviewer: sosstah
f1.keywords:
- NOCSH
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: None
search.appverid:
- MET150
ms.collection:
- Strat_O365_Enterprise
- M365-security-compliance
- Strat_O365_Enterprise
- SPO_Content
- MS-Compliance
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 3907a9a3f085af3d778daa2a385209f4dc9699a4
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497548"
---
# <a name="encryption-for-skype-for-business-onedrive-for-business-sharepoint-online-microsoft-teams-and-exchange-online"></a>Crittografia per Skype for Business, OneDrive for Business, SharePoint Online, Microsoft Teams ed Exchange Online

Microsoft 365 è un ambiente altamente sicuro che offre una protezione estesa su più livelli: sicurezza fisica del data center, sicurezza di rete, sicurezza degli accessi, sicurezza delle applicazioni e sicurezza dei dati.

## <a name="skype-for-business"></a>Skype for Business

I dati dei clienti di Skype for Business possono essere archiviati a riposo sotto forma di file o presentazioni caricati dai partecipanti alla riunione. Il server Web Conferencing crittografa i dati dei clienti utilizzando AES con una chiave a 256 bit. I dati dei clienti crittografati vengono archiviati in una condivisione file. Ogni parte dei dati dei clienti viene crittografata usando una chiave a 256 bit generata in modo casuale. Quando una parte dei dati dei clienti viene condivisa in una conferenza, il server Web Conferencing indica ai client di conferenza di scaricare i dati dei clienti crittografati tramite HTTPS. Invia la chiave corrispondente ai client in modo che i dati del cliente possano essere decrittografati. Il server Web Conferencing consente inoltre di autenticare i client di conferenza prima di consentire ai client di accedere ai dati dei clienti delle conferenze. Quando si partecipa a una conferenza Web, ogni client di conferenza stabilisce una finestra di dialogo SIP con il componente di stato attivo per le conferenze in esecuzione prima all'interno del server front-end su TLS. Lo stato attivo della conferenza passa al client per conferenze un cookie di autenticazione generato dal server Web Conferencing. Il client per conferenze si connette quindi al server Web Conferencing che presenta il cookie di autenticazione da autenticare dal server.

## <a name="sharepoint-online-and-onedrive-for-business"></a>SharePoint Online e OneDrive for Business

Tutti i file dei clienti in SharePoint Online sono protetti da chiavi univoche per file che sono sempre esclusive di un singolo tenant. Le chiavi vengono create e gestite dal servizio SharePoint Online oppure quando viene utilizzata la chiave cliente, creata e gestita dai clienti. Quando un file viene caricato, la crittografia viene eseguita da SharePoint Online nel contesto della richiesta di caricamento, prima di essere inviata all'archiviazione di Azure. Quando un file viene scaricato, SharePoint Online recupera i dati dei clienti crittografati dall'archiviazione di Azure in base all'identificatore univoco del documento e decrittografa i dati del cliente prima di inviarli all'utente. L'archiviazione di Azure non è in grado di decrittografare o persino identificare o comprendere i dati del cliente. Tutte le operazioni di crittografia e decrittografia si verificano negli stessi sistemi che applicano l'isolamento del tenant, ovvero Azure Active Directory e SharePoint Online.

Diversi carichi di lavoro in Microsoft 365 archiviano i dati in SharePoint Online, tra cui Microsoft Teams, che archivia tutti i file in SharePoint Online e OneDrive for Business, che usa SharePoint Online per l'archiviazione. Tutti i dati dei clienti archiviati in SharePoint Online vengono crittografati (con una o più chiavi AES a 256 bit) e distribuiti nel centro dati come indicato di seguito. Ogni passaggio di questo processo di crittografia è convalidato da FIPS 140-2 Livello 2. Per ulteriori informazioni sulla conformità FIPS 140-2, vedere [Conformità FIPS 140-2.](/previous-versions/sql/sql-server-2008-r2/bb326611(v=sql.105))

- Ogni file è suddiviso in uno o più blocchi, a seconda delle dimensioni del file. Ogni blocco viene crittografato utilizzando la propria chiave AES a 256 bit univoca.
- Quando un file viene aggiornato, l'aggiornamento viene gestito nello stesso modo: la modifica viene suddivisa in uno o più blocchi e ogni blocco viene crittografato con una chiave univoca separata.
- Questi blocchi, file, parti di file e delta di aggiornamento, vengono archiviati come BLOB nell'archiviazione di Azure distribuiti in modo casuale tra più account di archiviazione di Azure.
- Il set di chiavi di crittografia per questi blocchi di dati dei clienti è crittografato.

    - Le chiavi utilizzate per crittografare i BLOB vengono archiviate nel database del contenuto di SharePoint Online.
    - Il database del contenuto è protetto dai controlli di accesso al database e dalla crittografia in pausa. La crittografia viene eseguita [utilizzando Transparent Data Encryption](/sql/relational-databases/security/encryption/transparent-data-encryption-tde) (TDE) in Azure SQL [Database](/azure/sql-database/sql-database-technical-overview). (Azure SQL Database è un servizio di database relazionale generico in Microsoft Azure che supporta strutture quali dati relazionali, JSON, spaziali e XML. Questi segreti sono a livello di servizio per SharePoint Online, non a livello di tenant. Questi segreti (a volte denominati chiavi master) vengono archiviati in un archivio protetto separato denominato archivio chiavi. TDE garantisce la sicurezza in pausa sia per il database attivo che per i backup del database e i registri delle transazioni.
    - Quando i clienti forniscono la chiave facoltativa, la chiave del cliente viene archiviata in Azure Key Vault e il servizio usa la chiave per crittografare una chiave tenant, che viene usata per crittografare una chiave del sito, che viene quindi usata per crittografare le chiavi a livello di file. In sostanza, viene introdotta una nuova gerarchia di chiavi quando il cliente fornisce una chiave.
- La mappa utilizzata per assemblare di nuovo il file viene archiviata nel database del contenuto insieme alle chiavi crittografate, separatamente dalla chiave master necessaria per decrittografarle.
- Ogni account di archiviazione di Azure dispone di credenziali univoche per ogni tipo di accesso (lettura, scrittura, enumerazione ed eliminazione). Ogni set di credenziali è conservato nell'archivio chiavi protetto e viene regolarmente aggiornato. Come descritto in precedenza, esistono tre diversi tipi di archivi, ognuno con una funzione distinta:
    - I dati dei clienti vengono archiviati come BLOB crittografati nell'archiviazione di Azure. La chiave di ogni blocco di dati dei clienti viene crittografata e archiviata separatamente nel database del contenuto. I dati del cliente non hanno alcun indizio su come possono essere decrittografati.
    - Il database del contenuto è un database SQL Server. Contiene la mappa necessaria per individuare e riassemblare i BLOB di dati dei clienti presenti nell'archiviazione di Azure, nonché le chiavi necessarie per crittografare tali BLOB. Tuttavia, il set di chiavi viene crittografato (come spiegato in precedenza) e mantenuto in un archivio chiavi separato.
    - L'archivio chiavi è fisicamente separato dal database del contenuto e dall'archiviazione di Azure. Contiene le credenziali per ogni contenitore di archiviazione di Azure e la chiave master per il set di chiavi crittografate conservate nel database del contenuto.

Ognuno di questi tre componenti di archiviazione, l'archivio BLOB di Azure, il database del contenuto e l'archivio chiavi, è fisicamente separato. Le informazioni contenute in uno dei componenti sono inutilizzabili da sole. Senza l'accesso a tutti e tre, non è possibile recuperare le chiavi dei blocchi, decrittografare le chiavi per renderle utilizzabili, associare le chiavi ai blocchi corrispondenti, decrittografare ogni blocco o ricostruire un documento dai blocchi costitutivi.

I certificati di BitLocker, che proteggono i volumi del disco fisico nei computer nel datacenter, vengono archiviati in un archivio sicuro (l'archivio segreto di SharePoint Online) protetto dalla chiave farm.

Le chiavi TDE che proteggono le chiavi per BLOB vengono archiviate in due posizioni:

- L'archivio sicuro, che ospita i certificati BitLocker ed è protetto dalla chiave farm; e
- In un archivio sicuro gestito da Azure SQL Database.

Le credenziali utilizzate per accedere ai contenitori di archiviazione di Azure vengono inoltre mantenute nell'archivio segreto di SharePoint Online e delegate a ogni farm di SharePoint Online in base alle esigenze. Queste credenziali sono firme SAS di archiviazione di Azure, con credenziali separate usate per leggere o scrivere dati e con criteri applicati in modo che scadano automaticamente ogni 60 giorni. Credenziali diverse vengono utilizzate per leggere o scrivere dati (non entrambe) e alle farm di SharePoint Online non vengono concesse autorizzazioni per enumerare.

> [!NOTE]
> Per i clienti di Office 365 U.S. Government, i BLOB di dati vengono archiviati in Azure U.S. Government Storage. Inoltre, l'accesso alle chiavi di SharePoint Online in Office 365 U.S. Government è limitato al personale di Office 365 che sono stati appositamente schermati. Il personale operativo di Azure U.S. Government non ha accesso all'archivio chiavi di SharePoint Online utilizzato per crittografare i BLOB di dati.

Per ulteriori informazioni sulla crittografia dei dati in SharePoint Online e OneDrive for Business, vedere Crittografia dei dati [in OneDrive for Business e SharePoint Online.](https://technet.microsoft.com/library/dn905447.aspx)

### <a name="list-items-in-sharepoint-online"></a>Voci di elenco in SharePoint Online

Le voci di elenco sono blocchi più piccoli di dati dei clienti creati ad hoc o che possono essere presenti in modo più dinamico all'interno di un sito, ad esempio righe in un elenco creato dall'utente, singoli post in un blog di SharePoint Online o voci in una pagina wiki di SharePoint Online. Gli elementi di elenco vengono archiviati nel database del contenuto (Azure SQL Database) e protetti con TDE.

## <a name="encryption-of-data-in-transit"></a>Crittografia dei dati in transito

In OneDrive for Business e SharePoint Online, esistono due scenari in cui i dati entrano ed escono dai data center.

- **Comunicazione client con il server** - La comunicazione con SharePoint Online e OneDrive for Business tramite Internet utilizza le connessioni TLS.
- **Spostamento dei dati tra i datacenter-** Il motivo principale per spostare i dati tra i datacenter è la replica geografica per abilitare il ripristino di emergenza. Ad esempio, i registri transazioni di SQL Server e le differenze dell'archiviazione BLOB viaggiano lungo questa pipe. Mentre questi dati vengono già trasmessi utilizzando una rete privata, sono ulteriormente protetti mediante la migliore crittografia.

## <a name="exchange-online"></a>Exchange Online

Exchange Online usa BitLocker per tutti i dati delle cassette postali e la configurazione di BitLocker è descritta in [BitLocker per la crittografia](/microsoft-365/compliance/office-365-bitlocker-and-distributed-key-manager-for-encryption). La crittografia a livello di servizio crittografa tutti i dati delle cassette postali a livello di cassetta postale. 

Oltre alla crittografia del servizio, Microsoft 365 supporta la chiave del cliente, basata sulla crittografia del servizio. Customer Key è un'opzione con chiave gestita da Microsoft per la crittografia del servizio Exchange Online, anche nella roadmap di Microsoft. Questo metodo di crittografia garantisce una maggiore protezione non fornita da BitLocker perché fornisce la separazione tra gli amministratori del server e le chiavi di crittografia necessarie per la decrittografia dei dati e poiché la crittografia viene applicata direttamente ai dati (a differenza di BitLocker, che applica la crittografia al volume del disco logico), tutti i dati dei clienti copiati da un server Exchange rimangono crittografati.

L'ambito per la crittografia del servizio Exchange Online è dato da dati dei clienti archiviati in pausa all'interno di Exchange Online. Skype for Business archivia quasi tutti i contenuti generati dall'utente nella cassetta postale di Exchange Online dell'utente e quindi eredita la funzionalità di crittografia del servizio di Exchange Online.


## <a name="microsoft-teams"></a>Microsoft Teams

Teams usa TLS e MTLS per crittografare i messaggi istantanei. Tutto il traffico da server a server richiede MTLS, indipendentemente dal fatto che il traffico sia limitato alla rete interna o attraversi il perimetro della rete interna.

In questa tabella sono riepilogati i protocolli utilizzati da Teams.

|**Tipo di traffico**|**Crittografato da**|
|:-----|:-----|
|Da server a server|MTLS|
|Da client a server (ad esempio, messaggistica istantanea e presenza)|TLS|
|Flussi multimediali (ad esempio condivisione audio e video di elementi multimediali)|TLS|
|Condivisione audio e video di elementi multimediali|SRTP/TLS|
|Segnalazione|TLS|

#### <a name="media-encryption"></a>Crittografia multimediale

Il traffico multimediale viene crittografato tramite SRTP (Secure RTP), un profilo del protocollo RTP (Real-Time Transport Protocol) che garantisce riservatezza, autenticazione e protezione da attacchi di tipo replay per il traffico RTP. SRTP usa una chiave di sessione generata tramite un generatore di numeri casuali sicuro e viene scambiata utilizzando il canale TLS di segnalazione. Il traffico multimediale da client a client viene negoziato tramite una segnalazione di connessione da client a server, ma viene crittografato tramite SRTP quando si passa direttamente da client a client.

Teams usa un token basato sulle credenziali per l'accesso sicuro agli inoltri multimediali tramite TURN. Gli inoltri multimediali scambiano il token su un canale protetto da TLS.

#### <a name="fips"></a>FIPS

Teams utilizza algoritmi conformi a FIPS (Federal Information Processing Standard) per gli scambi di chiavi di crittografia. Per ulteriori informazioni sull'implementazione di FIPS, vedere [Federal Information Processing Standard (FIPS) Publication 140-2](/microsoft-365/compliance/offering-fips-140-2).
