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
ms.openlocfilehash: 9317b112d1fa759b1f90e072203e7b8093a432fd
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120545"
---
# <a name="encryption-for-skype-for-business-onedrive-for-business-sharepoint-online-microsoft-teams-and-exchange-online"></a>Crittografia per Skype for Business, OneDrive for Business, SharePoint Online, Microsoft Teams ed Exchange Online

Microsoft 365 è un ambiente altamente sicuro che offre una protezione estesa in più livelli: sicurezza dei data center fisici, sicurezza di rete, sicurezza degli accessi, sicurezza delle applicazioni e sicurezza dei dati.

## <a name="skype-for-business"></a>Skype for Business

I dati dei clienti di Skype for Business possono essere archiviati sotto forma di file o presentazioni caricati dai partecipanti alla riunione. Il server Web Conferencing crittografa i dati dei clienti utilizzando AES con una chiave a 256 bit. I dati crittografati del cliente vengono archiviati in una condivisione file. Ogni parte dei dati del cliente viene crittografata usando una chiave a 256 bit generata in modo casuale. Quando un dato del cliente viene condiviso in una conferenza, il server Web Conferencing indica ai client di conferenza di scaricare i dati crittografati del cliente tramite HTTPS. Invia la chiave corrispondente ai client in modo che i dati del cliente possano essere decrittografati. Il server Web Conferencing autentica inoltre i client di conferenza prima di consentire ai client di accedere ai dati dei clienti delle conferenze. Quando si partecipa a una conferenza Web, ogni client di conferenza stabilisce una finestra di dialogo SIP con il componente di stato attivo per le conferenze in esecuzione prima all'interno del server front-end tramite TLS. Lo stato attivo delle conferenze passa al client di conferenza un cookie di autenticazione generato dal server Web Conferencing. Il client per conferenze si connette quindi al server Web Conferencing che presenta il cookie di autenticazione da autenticare dal server.

## <a name="sharepoint-online-and-onedrive-for-business"></a>SharePoint Online e OneDrive for Business

Tutti i file dei clienti in SharePoint Online sono protetti da chiavi univoche per file che sono sempre esclusive di un singolo tenant. Le chiavi vengono create e gestite dal servizio SharePoint Online oppure quando viene usato customer key, create e gestite dai clienti. Quando un file viene caricato, la crittografia viene eseguita da SharePoint Online nel contesto della richiesta di caricamento, prima di essere inviata all'archiviazione di Azure. Quando un file viene scaricato, SharePoint Online recupera i dati del cliente crittografati dall'archiviazione di Azure in base all'identificatore univoco del documento e decrittografa i dati del cliente prima di inviarli all'utente. L'archiviazione di Azure non è in grado di decrittografare o persino identificare o comprendere i dati del cliente. Tutta la crittografia e la decrittografia si verificano negli stessi sistemi che applicano l'isolamento del tenant, che sono Azure Active Directory e SharePoint Online.

Diversi carichi di lavoro in Microsoft 365 archiviano i dati in SharePoint Online, tra cui Microsoft Teams, che archivia tutti i file in SharePoint Online, e OneDrive for Business, che usa SharePoint Online per l'archiviazione. Tutti i dati dei clienti archiviati in SharePoint Online sono crittografati (con una o più chiavi AES a 256 bit) e distribuiti nel centro dati come indicato di seguito. Ogni passaggio di questo processo di crittografia è convalidato da FIPS 140-2 Livello 2. Per ulteriori informazioni sulla conformità FIPS 140-2, vedere [Conformità FIPS 140-2.](/previous-versions/sql/sql-server-2008-r2/bb326611(v=sql.105))

- Ogni file è suddiviso in uno o più blocchi, a seconda delle dimensioni del file. Ogni blocco viene crittografato utilizzando la propria chiave AES a 256 bit univoca.
- Quando un file viene aggiornato, l'aggiornamento viene gestito nello stesso modo: la modifica viene suddivisa in uno o più blocchi e ogni blocco viene crittografato con una chiave univoca separata.
- Questi blocchi, ad esempio file, parti di file e delta di aggiornamento, vengono archiviati come BLOB nell'archiviazione di Azure distribuiti in modo casuale tra più account di archiviazione di Azure.
- Il set di chiavi di crittografia per questi blocchi di dati dei clienti è crittografato.

    - Le chiavi utilizzate per crittografare i BLOB vengono archiviate nel database del contenuto di SharePoint Online.
    - Il database del contenuto è protetto dai controlli di accesso al database e dalla crittografia in pausa. La crittografia viene eseguita [utilizzando Transparent Data Encryption](/sql/relational-databases/security/encryption/transparent-data-encryption-tde) (TDE) in Azure SQL [Database.](/azure/sql-database/sql-database-technical-overview) Il database di azure SQL è un servizio di database relazionale generico in Microsoft Azure che supporta strutture quali dati relazionali, JSON, spaziale e XML. Questi segreti sono a livello di servizio per SharePoint Online, non a livello di tenant. Questi segreti (a volte denominati chiavi master) vengono archiviati in un archivio protetto separato denominato archivio chiavi. TDE garantisce la sicurezza a riposo sia per il database attivo che per i backup dei database e per i registri delle transazioni.
    - Quando i clienti forniscono la chiave facoltativa, la chiave del cliente viene archiviata in Azure Key Vault e il servizio usa la chiave per crittografare una chiave tenant, che viene usata per crittografare una chiave del sito, che viene quindi usata per crittografare le chiavi a livello di file. In sostanza, viene introdotta una nuova gerarchia di chiavi quando il cliente fornisce una chiave.
- La mappa utilizzata per riassemblare il file viene archiviata nel database del contenuto insieme alle chiavi crittografate, separatamente dalla chiave master necessaria per decrittografarle.
- Ogni account di archiviazione di Azure dispone di credenziali univoche per ogni tipo di accesso (lettura, scrittura, enumerazione ed eliminazione). Ogni set di credenziali è conservato nell'archivio chiavi protetto e viene regolarmente aggiornato. Come descritto in precedenza, esistono tre diversi tipi di archivi, ognuno con una funzione distinta:
    - I dati dei clienti vengono archiviati come BLOB crittografati nell'archiviazione di Azure. La chiave per ogni blocco di dati dei clienti viene crittografata e archiviata separatamente nel database del contenuto. I dati del cliente non hanno alcuna indicazione su come possono essere decrittografati.
    - Il database del contenuto è un database SQL Server. Contiene la mappa necessaria per individuare e riassemblare i BLOB di dati dei clienti presenti nell'archiviazione di Azure, nonché le chiavi necessarie per crittografare tali BLOB. Tuttavia, il set di chiavi è crittografato (come spiegato in precedenza) e mantenuto in un archivio chiavi separato.
    - L'archivio chiavi è fisicamente separato dal database del contenuto e dall'archiviazione di Azure. Contiene le credenziali per ogni contenitore di archiviazione di Azure e la chiave master per il set di chiavi crittografate conservate nel database del contenuto.

Ognuno di questi tre componenti di archiviazione, l'archivio BLOB di Azure, il database del contenuto e l'archivio chiavi, sono fisicamente separati. Le informazioni contenute in uno dei componenti sono inutilizzabili da sole. Senza l'accesso a tutti e tre, non è possibile recuperare le chiavi dei blocchi, decrittografare le chiavi per renderle utilizzabili, associare le chiavi ai blocchi corrispondenti, decrittografare ogni blocco o ricostruire un documento dai blocchi costituenti.

I certificati BitLocker, che proteggono i volumi dei dischi fisici nei computer nel datacenter, vengono archiviati in un archivio sicuro (l'archivio segreto di SharePoint Online) protetto dalla chiave della farm.

Le chiavi TDE che proteggono le chiavi per BLOB sono archiviate in due posizioni:

- L'archivio sicuro, che ospita i certificati di BitLocker ed è protetto dalla chiave della farm; e
- In un archivio sicuro gestito da Azure SQL Database.

Le credenziali utilizzate per accedere ai contenitori di archiviazione di Azure vengono inoltre mantenute nell'archivio segreto di SharePoint Online e delegate a ogni farm di SharePoint Online in base alle esigenze. Queste credenziali sono firme SAS di archiviazione di Azure, con credenziali separate usate per leggere o scrivere dati e con criteri applicati in modo che scadono automaticamente ogni 60 giorni. Credenziali diverse vengono utilizzate per leggere o scrivere dati (non entrambi) e le farm di SharePoint Online non sono concesse autorizzazioni per enumerare.

> [!NOTE]
> Per i clienti di Office 365 U.S. Government, i BLOB di dati sono archiviati in Azure U.S. Government Storage. Inoltre, l'accesso alle chiavi di SharePoint Online in Office 365 U.S. Government è limitato al personale di Office 365 che è stato appositamente schermato. Il personale operativo di Azure U.S. Government non ha accesso all'archivio chiavi di SharePoint Online utilizzato per crittografare i BLOB di dati.

Per ulteriori informazioni sulla crittografia dei dati in SharePoint Online e OneDrive for Business, vedere Crittografia dei dati [in OneDrive for Business e SharePoint Online.](https://technet.microsoft.com/library/dn905447.aspx)

### <a name="list-items-in-sharepoint-online"></a>Voci di elenco in SharePoint Online

Gli elementi di elenco sono blocchi più piccoli di dati dei clienti creati ad hoc o che possono essere visualizzati in modo più dinamico all'interno di un sito, ad esempio righe in un elenco creato dall'utente, singoli post in un blog di SharePoint Online o voci all'interno di una pagina wiki di SharePoint Online. Gli elementi di elenco vengono archiviati nel database del contenuto (Azure SQL Database) e protetti con TDE.

## <a name="encryption-of-data-in-transit"></a>Crittografia dei dati in transito

In OneDrive for Business e SharePoint Online, esistono due scenari in cui i dati entrano ed escono dai data center.

- **Comunicazione client con il server:** la comunicazione con SharePoint Online e OneDrive for Business tramite Internet usa le connessioni TLS.
- **Spostamento dei dati tra datacenter:** il motivo principale per spostare i dati tra i datacenter è la replica geografica per abilitare il ripristino di emergenza. Ad esempio, i registri transazioni di SQL Server e le differenze dell'archiviazione BLOB viaggiano lungo questa pipe. Mentre questi dati vengono già trasmessi utilizzando una rete privata, sono ulteriormente protetti mediante la migliore crittografia.

## <a name="exchange-online"></a>Exchange Online

Exchange Online usa BitLocker per tutti i dati della cassetta postale e la configurazione di BitLocker è descritta in [BitLocker per la crittografia.](/microsoft-365/compliance/office-365-bitlocker-and-distributed-key-manager-for-encryption) La crittografia a livello di servizio crittografa tutti i dati della cassetta postale a livello di cassetta postale. 

Oltre alla crittografia dei servizi, Microsoft 365 supporta Customer Key, basato sulla crittografia del servizio. Customer Key è un'opzione con chiave gestita da Microsoft per la crittografia del servizio Exchange Online, anche nella roadmap di Microsoft. Questo metodo di crittografia garantisce una maggiore protezione non fornita da BitLocker perché offre la separazione tra gli amministratori del server e le chiavi crittografiche necessarie per la decrittografia dei dati e poiché la crittografia viene applicata direttamente ai dati (a differenza di BitLocker, che applica la crittografia nel volume del disco logico), tutti i dati dei clienti copiati da un server Exchange rimangono crittografati.

L'ambito per la crittografia del servizio Exchange Online sono i dati dei clienti archiviati in stato di inquieto all'interno di Exchange Online. Skype for Business archivia quasi tutti i contenuti generati dall'utente all'interno della cassetta postale di Exchange Online dell'utente e quindi eredita la funzionalità di crittografia del servizio di Exchange Online.


## <a name="microsoft-teams"></a>Microsoft Teams

Teams usa TLS e MTLS per crittografare i messaggi istantanei. Tutto il traffico da server a server richiede MTLS, indipendentemente dal fatto che il traffico sia limitato alla rete interna o attraversi il perimetro della rete interna.

Questa tabella riepiloga i protocolli utilizzati da Teams.

|**Tipo di traffico**|**Crittografato da**|
|:-----|:-----|
|Da server a server|MTLS|
|Da client a server (ad esempio messaggistica istantanea e presenza)|TLS|
|Flussi multimediali (ad esempio condivisione audio e video di elementi multimediali)|TLS|
|Condivisione audio e video di elementi multimediali|SRTP/TLS|
|Segnalazione|TLS|

#### <a name="media-encryption"></a>Crittografia multimediale

Il traffico multimediale viene crittografato tramite SRTP (Secure RTP), un profilo del protocollo RTP (Real-Time Transport Protocol) che garantisce riservatezza, autenticazione e protezione da attacchi di tipo replay per il traffico RTP. SRTP usa una chiave di sessione generata utilizzando un generatore di numeri casuali sicuro e viene scambiata tramite il canale TLS di segnalazione. Il traffico multimediale da client a client viene negoziato tramite una segnalazione di connessione da client a server, ma viene crittografato tramite SRTP quando si passa direttamente da client a client.

Teams usa un token basato sulle credenziali per l'accesso sicuro ai media relay su TURN. I media relay scambiano il token su un canale protetto da TLS.

#### <a name="fips"></a>FIPS

Teams usa algoritmi conformi a FIPS (Federal Information Processing Standard) per lo scambio di chiavi di crittografia. Per ulteriori informazioni sull'implementazione di FIPS, vedere [Federal Information Processing Standard (FIPS) Publication 140-2](/microsoft-365/compliance/offering-fips-140-2).
