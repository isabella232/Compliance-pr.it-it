---
title: Controlli tecnologici in Microsoft 365
description: In questo articolo viene fornita una panoramica degli strumenti e delle tecnologie utilizzati da Microsoft per il controllo della tecnologia in Microsoft 365.
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
ms.custom:
- seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 06d8f500a96c84bf961dc47f6b8d259e0fffe02d
ms.sourcegitcommit: 4c00fd65d418065d7f53216c91f455ccb3891c77
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/23/2021
ms.locfileid: "58481648"
---
# <a name="technology-controls-in-microsoft-365"></a>Controlli tecnologici in Microsoft 365 

Microsoft usa diversi strumenti e tecnologie per controllare, gestire e controllare l'accesso ai dati dei clienti nei propri servizi online. Si applicano a Exchange Online, SharePoint Online, Lockbox e Customer Lockbox, autenticazione a più fattori e altro ancora. Yammer vengono utilizzati controlli simili descritti in [Yammer Enterprise Access Controls](assurance-yammer-enterprise-access-controls.md).

Microsoft 365 tecnici non hanno accesso permanente ai Microsoft 365 dei clienti. I tecnici devono eseguire un processo di approvazione Microsoft prima che si verifichi l'accesso ai dati dei clienti per le operazioni di servizio. Se il cliente licenze la funzionalità Customer Lockbox per Exchange Online e SharePoint Online, l'accesso ai dati del cliente richiede l'approvazione del cliente. Dopo l'approvazione, agli account amministrativi specifici del servizio viene effettuato il provisioning dell'accesso just-in-time per le attività richieste dalla richiesta di servizio.

## <a name="lockbox-and-customer-lockbox"></a>Lockbox e Customer Lockbox

Sebbene raro, un cliente potrebbe richiedere assistenza a Microsoft che espone il contenuto del cliente a un tecnico Microsoft. Per controllare l'accesso Exchange Online, Microsoft usa un sistema di controllo di accesso denominato Lockbox. Prima che un tecnico Microsoft accedono a Exchange Online o SharePoint online o ai dati, deve inviare una richiesta di accesso tramite Lockbox. Tutte le richieste di Exchange Online e SharePoint Online vengono gestite dal sistema Lockbox. Con Lockbox e Customer Lockbox, tutti gli accessi approvati sono tracciabili per un utente univoco, rendendo i tecnici in grado di gestire i dati dei clienti.

> [!NOTE]
> Exchange Online include tutti i Skype for Business archiviati nelle cassette postali degli utenti. Skype for Business non include le registrazioni Riunione Skype broadcast o il contenuto caricato nelle riunioni dagli utenti. SharePoint Online include OneDrive for Business.

Lockbox elabora le richieste di autorizzazioni che concedono ai tecnici la possibilità di eseguire funzioni operative e amministrative all'interno del servizio. I tecnici inviano le richieste tramite Lockbox e un responsabile Microsoft deve approvare la richiesta prima che il tecnico possa accedere ai dati dei clienti. Dopo l'approvazione del manager, il tecnico ha accesso limitato a tempo e ambito ai dati del cliente per lavorare sul problema del cliente.

Customer Lockbox per Microsoft 365 consente di soddisfare gli obblighi di conformità se sono necessarie procedure per l'autorizzazione esplicita di accesso ai dati. Si tratta di un requisito per alcuni standard di conformità, ad esempio FedRAMP e HIPAA. Customer Lockbox inserisce l'utente nel processo di approvazione di Lockbox e consente di controllare l'autorizzazione dell'accesso Microsoft al contenuto di Exchange Online o SharePoint Online per le operazioni di servizio.

Nel raro caso in cui un tecnico del servizio Microsoft deve accedere ai dati, si concede l'accesso solo ai dati necessari per risolvere il problema e per un periodo di tempo limitato. Se si rifiuta una richiesta di accesso, i tecnici Microsoft non hanno accesso al contenuto e non saranno in grado di completare le operazioni di servizio. Se si approva la richiesta, i tecnici Microsoft riceveranno un accesso limitato just-in-time ai contenuti tramite interfacce di gestione monitorate e vincolate.

Le azioni intraprese dal tecnico del supporto vengono registrate per scopi di controllo e sono accessibili tramite [l'API](/office/office-365-management-api/get-started-with-office-365-management-apis) di Office 365 Management Activity e il Centro sicurezza [e conformità.](https://protection.office.com/)

>[!NOTE]
> Customer Lockbox è disponibile in [Microsoft 365 E5](https://products.office.com/business/office-365-enterprise-e5-business-software) come acquisto di componenti aggiuntivi. Per ulteriori informazioni, vedere [Microsoft 365 Customer Lockbox Requests](https://support.office.com/article/Office-365-Customer-Lockbox-Requests-36f9cdd1-e64c-421b-a7e4-4a54d16440a2).

## <a name="just-in-time-access"></a>Accesso just-in-time

Microsoft usa il principio di accesso just-in-time (JIT) per Microsoft 365 per ridurre i rischi di manomissione delle credenziali e gli attacchi laterali. JIT rimuove l'accesso amministrativo permanente ai servizi e sostituisce i diritti con la possibilità di elevare tali ruoli su richiesta. La rimozione dei diritti di accesso persistente da parte degli amministratori garantisce che le credenziali siano disponibili solo quando sono necessarie e riduce i rischi di furto delle credenziali.

Il modello di accesso JIT richiede ai tecnici di richiedere privilegi elevati per un periodo limitato per eseguire attività amministrative. Inoltre, i tecnici utilizzano account temporanei creati con password complesse generate dal computer e hanno concesso solo i ruoli che consentono loro di eseguire le attività necessarie. Ad esempio, l'accesso amministrativo concesso da Lockbox è associato a tempo e la quantità di tempo concessa dipende dal ruolo richiesto. Un tecnico specifica la durata dell'accesso necessario nella richiesta al sistema Lockbox. Il sistema Lockbox rifiuta le richieste quando il tempo richiesto supera il tempo massimo consentito per l'elevazione. Dopo la scadenza, l'accesso amministrativo viene rimosso e l'account temporaneo scade.

Quando sono autorizzati e approvati per l'accesso, i tecnici ricevono una password amministrativa per uso unico generata dal sistema di autorizzazione. Le nuove password vengono generate ogni volta che viene approvata una richiesta di accesso con privilegi elevati. La password viene copiata in una password sicura, è separata dalle credenziali del tecnico per l'ambiente aziendale Microsoft ed è valida solo per la sessione di accesso con privilegi elevati approvata.

## <a name="constrained-management-interfaces"></a>Interfacce di gestione vincolata

I tecnici utilizzano due interfacce di gestione per eseguire attività amministrative: Desktop remoto tramite gateway del servizio terminal (TSG) protetti e Remote PowerShell. All'interno di queste interfacce di gestione, i criteri software e i controlli di accesso determinano restrizioni significative sulle applicazioni eseguite e sui comandi e i cmdlet disponibili.

Microsoft 365 server limitano le sessioni simultanee a una sessione per ogni amministratore del team di servizio, per server. I gruppi di protezione dei servizi terminal consentono una sola sessione simultanea per gli utenti e non consentono più sessioni. Utilizzando una singola sessione per server, i gruppi di sicurezza dei servizi di Microsoft 365 consentono agli amministratori del team del servizio di connettersi contemporaneamente a più server in modo che gli amministratori possano svolgere efficacemente le proprie attività. Gli amministratori del team del servizio non dispongono di autorizzazioni per i gruppi di sicurezza dei servizi di dominio. Il gruppo TSG viene utilizzato solo per applicare l'autenticazione a più fattori (MFA) e i requisiti di crittografia. Una volta che l'amministratore del team del servizio si connette a un server specifico tramite un gruppo di protezione dei servizi, il server specifico applica un limite di sessione di uno per ogni amministratore.

Le restrizioni di utilizzo e i requisiti di connessione e configurazione per Microsoft 365 personale vengono stabiliti dai criteri di gruppo di Active Directory. Questi criteri includono le caratteristiche seguenti:

- I TSG utilizzano solo la crittografia [convalidata FIPS](https://www.microsoft.com/TrustCenter/Compliance/FIPS) 140-2.
- Le sessioni TSG si disconnettino dopo 30 minuti di inattività.
- Le sessioni TSG si discostono automaticamente dopo 24 ore.

Per le connessioni ai TSG è inoltre necessaria l'autenticazione a più fattori utilizzando una smart card fisica separata e un account separato dalle credenziali aziendali Microsoft del tecnico. I tecnici vengono emessi smart card diverse per diverse piattaforme e piattaforme di gestione dei segreti garantiscono l'archiviazione sicura delle credenziali. I gruppi di servizi terminal utilizzano i criteri di gruppo di Active Directory per controllare chi può accedere ai server remoti, il numero di sessioni consentite e le impostazioni di timeout di inattività. Criteri aggiuntivi limitano l'accesso alle applicazioni consentite e limitano l'accesso a Internet.

Oltre all'accesso remoto tramite TSG configurati appositamente, Exchange Online consente agli utenti con il ruolo Service Engineer Operations di accedere a determinate funzionalità amministrative nei server di produzione tramite Remote PowerShell. A tale scopo, l'utente deve essere autorizzato per l'accesso di sola lettura (debug) all'Microsoft 365 di produzione. L'escalation dei privilegi è abilitata nello stesso modo in cui viene abilitata per i TSG tramite il processo Lockbox.

Per l'accesso remoto, ogni datacenter dispone di un IP virtuale con bilanciamento del carico che funge da singolo punto di accesso. I cmdlet di Remote PowerShell disponibili si basano sul livello di privilegio identificato nell'attestazione di accesso ottenuta durante l'autenticazione. Questi cmdlet forniscono l'unica funzionalità amministrativa accessibile dagli utenti che si connettono utilizzando questo metodo. Remote PowerShell limita l'ambito dei comandi disponibili per il tecnico e si basa sul livello di accesso concesso tramite il processo Lockbox. Ad esempio, in Exchange Online, Get-Mailbox potrebbe essere disponibile, ma Set-Mailbox potrebbe non.
