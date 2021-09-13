---
title: Considerazioni sul piano per la gestione della continuità aziendale
description: Aspetti da considerare durante lo sviluppo di un piano di continuità aziendale compatibile con il cloud.
author: robmazz
ms.author: robmazz
manager: laurawi
ms.reviewer: sosstah
f1.keywords:
- NOCSH
audience: ITPro
ms.topic: article
ms.service: o365-solutions
ms.localizationpriority: medium
ms.collection:
- M365-subscription-management
- Strat_O365_Enterprise
- MS-Compliance
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 6a44866d5c82ffa93e6c3c0d9c0ece3946651bd2
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/12/2021
ms.locfileid: "59159223"
---
# <a name="developing-your-business-continuity-plan"></a>Sviluppo del piano di continuità aziendale

In questo argomento vengono fornite indicazioni sullo sviluppo di un piano di continuità aziendale che tiene conto Microsoft 365 dipendenze aziendali. Vengono consigliati metodi per analizzare le funzioni aziendali e identificare quelle che dipendono dai servizi Microsoft 365. Si eseguirà questa analisi con la consapevolezza che si verificheranno errori dei servizi e che è necessario prepararsi per questa eventualità.

In generale, la pianificazione della continuità aziendale implica quattro aspetti, ovvero la valutazione, la pianificazione, la convalida delle funzionalità, nonché le comunicazioni e il coordinamento.

## <a name="assessment"></a>Valutazione
È necessario prima di tutto identificare le funzioni aziendali presenti nell'organizzazione e i servizi e i processi che le supportano. Questo include il completamento di un'analisi dell'impatto aziendale, nota come Business Impact Assessment (BIA), in cui ogni funzione aziendale è classificata in base alla criticità e si identificano i processi e i servizi da cui ognuna di esse dipende. Ecco una tabella di esempio che può essere utile per iniziare a creare la propria valutazione.

**Esempio di Business Impact Assessment (BIA)**

Questo è un documento BIA per `name of the service, system, process, or function`

|Campi BIA|Descrizione|
|---------|---------|
|Tipo BIA|`is it a business process or technology, service or system?`|
|Nome BIA|`name of the service/system/function/process`|
|Descrizione servizio|`give a full description of the service, process, or function`|
|Funzione aziendale|`some examples: customer services; legal; marketing; risk management, security, sales, information technology, production, manufacturing`|
|Anno fiscale|`the current fiscal year, re-evaluate these on a regular basis`|
|Criticità|`develop your own classifications, but here are some examples: mission critical, important, deferrable`|
|Business unit|`name of the business unit that owns this business function`|
|Processo (servizio, funzionalità)|`the name of the process, service, or feature`|
|responsabile senior gruppo aziendale|`the name and contact information of the senior leader of the business group that owns this business process`|
|La tecnologia ha uno SLA o un OLA interno stabilito?|`please explain in as much detail as possible`|
|La tecnologia ha uno SLA o un OLA **esterno** stabilito?|`please explain in as much detail as possible`|
|La tecnologia ha un mandato esecutivo noto per la gestione dello SLA di uno specifico processo? In caso affermativo, spiegare in dettaglio.|`details here`|
|La perdita o la compromissione dei dati associati a questo servizio attiverà un evento principale? In caso affermativo, spiegare in dettaglio.|`details here`|
|Il servizio dispone di un'alternativa per alcune o tutte le relative funzioni e funzionalità principali? In caso affermativo, spiegare in dettaglio.|`details here`|
|Il servizio elabora, archivia o trasmette dati dei clienti, ad esempio informazioni personali? In caso affermativo, spiegare in dettaglio.|`details here`|
|Stato BIA|`develop your own status classification, here are some examples: planned, started, in-progress, complete, on-hold, expired`|
|Data di completamento|`the date this BIA was completed`|
|Facilitatore BIA|`name of the person or group who is responsible for developing and maintaining this BIA`|
|Approvazione BIA|`name of the person or group who is the executive sponsor of this BIA and who has responsibility for approving it.`|
|Collaboratori|`optional list of the people who helped develop this BIA and their contact information`|
|Posizione approvazione BIA|`indicate where the executive approval is located, or attach proof to this document`|

## <a name="planning"></a>Pianificazione

Successivamente, si esamineranno i processi aziendali per identificare le eventuali relazioni di dipendenza a catena. In base al risultato, è possibile definire le priorità e creare strategie di resilienza, oltre a procedure operative standard a supporto delle strategie.

Per semplificare questa operazione, si può usare Mapping dei servizi Microsoft. Mapping dei servizi Microsoft individua automaticamente i componenti dell'applicazione nei sistemi Windows e Linux ed esegue il mapping di tutte le dipendenze TCP, identificando le connessioni e i sistemi di terze parti remoti da cui l'app dipende. Inoltre, esegue il mapping delle dipendenze ad aree della rete tradizionalmente oscure, come Active Directory.

Ecco un'analisi delle dipendenze di esempio da cui iniziare. Nell'analisi delle dipendenze verranno identificate ed esaminate le dipendenze dei processi. Assicurati di includere persone, fornitori, clienti, partnership e strutture. I dati provenienti da questa analisi verranno usati per identificare le discrepanze tra i requisiti di ripristino di un processo e le funzionalità di ripristino delle dipendenze di supporto.


|Campo|Descrizione|
|---------|---------|
|Tipo di processo|         |
|Facilitatore|         |
|Completato da|         |
|Data completamento|         |
|Collaboratori|         |
  
## <a name="capability-validation"></a>Convalida delle funzionalità

Dopo aver inventariato i processi aziendali e aver mappato tutte le relazioni con altri processi e tecnologie, è necessario creare scenari di convalida per tutti i processi. Fondamentalmente, riflettere su come convalidare i piani di continuità dei processi aziendali. Probabilmente si scoprirà che alcuni sono più importanti di altri e si vorrà dare loro la priorità.
È importante tenere presente che, una volta stabilito il piano, formare regolarmente i dipendenti in merito alle misure di continuità e risposta agli incidenti è molto importante. È opportuno usare revisioni post evento per migliorare le strategie di resilienza, incorporando quanto appreso da ogni convalida o test.

![visio di convalida delle funzionalità.](../media/capability-validation-visio.png)

## <a name="incident-coordination-and-communication"></a>Comunicazioni e coordinamento in caso di incidenti

Durante un incidente relativo a un servizio, i normali canali di comunicazione potrebbero risultare compromessi o degradati, quindi è consigliabile predisporre alternative per aiutare l'organizzazione a mantenere le comunicazioni durante un evento imprevisto. È essenziale che, prima di una interruzione, i canali di comunicazione siano stati stabiliti e verificati in termini di sicurezza e conformità e che gli utenti siano stati formati su come usarli. Passare da uno stato noto a un altro stato noto è di gran lunga preferibile a utenti che, nel bel mezzo di una crisi, propongono soluzioni ad hoc e sconosciute.

In Microsoft, ogni team del servizio ha stabilito canali di comunicazione alternativi interni per aiutarci a coordinarci quando i normali canali di comunicazione non sono disponibili. Questi includono soluzioni di telefonia e di audioconferenza di backup, gruppi di Yammer, gruppi di Teams, dashboard di integrità dei servizi interni e software di Incident Management interni.

Durante l'analisi dell'impatto aziendale e l'analisi delle dipendenze, si assoceranno i processi critici alle tecnologie o ai servizi a cui dipendono. Prestare particolare attenzione alle comunicazioni in questa fase della pianificazione e pensare a soluzioni alternative. Ecco alcuni esempi.

- Se il metodo principale usato per informare gli utenti e gli stakeholder è l'e-mail e il servizio di posta elettronica è degradato o non è disponibile, si può usare come backup un altro servizio, come Microsoft Teams, Yammer o un servizio di terze parti. La chiave consiste nello stabilire tutto questo in anticipo e nell'insegnare agli utenti dove andare. Un Yammer thread non sarà utile se nessuno sa che esiste o se nessuno lo ha aggiunto ai segnalibri.  
- Se i processi interni di gestione degli incidenti si basano sulle comunicazioni vocali per coordinare le risposte, stabilire una soluzione di telefonia alternativa da usare durante una crisi. Questa soluzione non deve avere la parità completa con il servizio principale, ma deve fornire il livello minimo di collaborazione per coordinare i team di continuità aziendale e gestione degli incidenti. Inoltre, chiedere agli utenti di pubblicare i numeri di telefono cellulare nell'elenco indirizzi globale può fornire un ulteriore livello di comunicazione di backup nei casi più estremi.
- Può essere utile creare un dashboard di integrità dei servizi personalizzato o un altro sito di questo genere, che possa fornire aggiornamenti sullo stato durante un evento imprevisto. Informare gli utenti in anticipo su dove rivolgersi per ottenere informazioni contribuirà a ridurre le chiamate superflue all'help desk e a infondere fiducia nella base degli utenti sul fatto che la situazione viene gestita in modo rapido ed efficiente. Usa l'API O365 Service Communications per collegare queste informazioni Microsoft 365 un livello di visibilità ancora maggiore.  
- È essenziale che l'ubicazione dei piani di continuità aziendale e delle procedure operative standard sia ben nota. È consigliabile mantenere copie online e offline dei documenti critici, ad esempio configurando OneDrive for Business o SharePoint Online per la sincronizzazione automatica con i dispositivi locali. Per i Centri operazioni di servizio/rete e altri team simili che saranno critici per il ripristino, è anche possibile mantenere disponibili copie rigide da utilizzare in caso di emergenza.

## <a name="know-your-external-points-of-integration"></a>Conoscere i punti di integrazione esterni

Indipendentemente dal modello aziendale, ogni azienda ha punti di integrazione con clienti, partner e fornitori. La supply chain del valore aziendale è basata sull'integrazione con entità esterne. Per migliorare la continuità aziendale in caso di interruzione del servizio, è necessario considerare e proteggere ogni punto di integrazione.  
Quando si analizza la supply chain, è necessario considerare le comunicazioni esterne nello stesso modo in cui si analizzano le comunicazioni interne. I clienti fanno affidamento sui server di Exchange Online come unico metodo per contattare l'organizzazione? Sono stati stabiliti e comunicati ai fornitori metodi di comunicazione alternativi, per i casi in cui l'operatività sia stata compromessa? Ecco una tabella di esempio che suggerisce come organizzare il proprio ragionamento.

|Nome entità esterna|Scenario dell'incidente|Servizi Microsoft 365 integrati|Alternative|
|---------|---------|---------|---------|
|`vendor name`|Flusso di posta|Exchange Online è l'unico mezzo di comunicazione con Contoso|Configurare canali esterni di Microsoft Teams o software di collaborazione di terze parti          |
|`service supplier name`|Chat|Microsoft Teams|messaggistica istantanea di terze parti|
|`partner name`|Voce|Microsoft Teams|Rete mobile o PSTN pubblica      |
|`supplier name`|Condivisione file|OneDrive e siti di SharePoint condivisi esternamente|condivisione di file di terze parti         |
