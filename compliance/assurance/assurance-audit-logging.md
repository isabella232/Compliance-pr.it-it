---
title: Panoramica sulla registrazione di controllo
description: Informazioni sulla registrazione di controllo in Microsoft 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: Admin
ms.topic: article
f1.keywords:
- NOCSH
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
search.appverid:
- MET150
- MOE150
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: e6bf564f182f2dfabc6561602e5a4cb5c8c3445e
ms.sourcegitcommit: fb379d1110a9a86c7f9bab8c484dc3f4b3dfd6f0
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/23/2021
ms.locfileid: "53088688"
---
# <a name="audit-logging-overview"></a>Panoramica sulla registrazione di controllo

## <a name="how-does-microsoft-365-employ-audit-logging"></a>In che modo Microsoft 365 la registrazione di controllo?

Microsoft 365 utilizza la registrazione di controllo per rilevare attività non autorizzate nei propri prodotti e servizi e fornire responsabilità al personale Microsoft. I log di controllo acquisiscono dettagli sulle modifiche alla configurazione del sistema e sugli eventi di accesso, con i dettagli per identificare chi è stato responsabile dell'attività, quando e dove si è verificata l'attività e qual è il risultato dell'attività. L'analisi automatizzata dei log supporta il rilevamento quasi in tempo reale di comportamenti sospetti. I potenziali incidenti vengono inoltrati al team Microsoft 365 Security Response per ulteriori indagini.

Microsoft 365 registrazione di controllo interna acquisisce i dati di registro da varie origini, ad esempio:

- Registri eventi
- Log di AppLocker
- Dati sulle prestazioni
- System Center dati
- Record dettagli chiamata
- Dati sulla qualità dell'esperienza
- Registri del server Web IIS
- SQL Server log
- Dati Syslog
- Log di controllo della sicurezza

## <a name="how-does-microsoft-365-centralize-and-report-on-audit-logs"></a>In che modo Microsoft 365 centralizzare e creare report nei log di controllo?

Molti tipi diversi di dati di registro vengono caricati dai server Microsoft 365 in una soluzione di monitoraggio della sicurezza proprietaria per l'analisi NRT (Near Real-Time) e un servizio di big data computing (Cosmos) interno per l'archiviazione a lungo termine. Questo trasferimento dei dati avviene tramite una connessione TLS convalidata da FIPS 140-2 su porte e protocolli approvati utilizzando uno strumento di automazione proprietario denominato Office Data Loader (ODL).

I log vengono elaborati in NRT utilizzando metodi di apprendimento automatico, statistici e basati su regole per rilevare gli indicatori delle prestazioni del sistema e i potenziali eventi di sicurezza. I modelli di machine learning utilizzano i dati del registro in ingresso e i dati cronologici archiviati Cosmos per migliorare continuamente le funzionalità di rilevamento. I rilevamenti correlati alla sicurezza generano avvisi, notificando ai tecnici di chiamata di un potenziale incidente e attivando azioni di correzione automatizzate, se applicabile. Oltre al monitoraggio automatico della sicurezza, i team di servizio utilizzano strumenti di analisi e dashboard per la correlazione dei dati, le query interattive e l'analisi dei dati. Questi report vengono utilizzati per monitorare e migliorare le prestazioni complessive del servizio.

Per ulteriori informazioni sul monitoraggio della sicurezza e sugli avvisi, vedere Panoramica [del monitoraggio della sicurezza](assurance-security-monitoring.md).

![Flusso di dati di controllo](../media/assurance-audit-data-flow.png)

## <a name="how-does-microsoft-365-protect-audit-logs"></a>In che modo Microsoft 365 i log di controllo?

Gli strumenti utilizzati in Microsoft 365 per raccogliere ed elaborare i record di controllo non consentono modifiche permanenti o irreversibili al contenuto del record di controllo originale o all'ordinamento temporale. L'accesso Microsoft 365 dati archiviati in Cosmos è limitato al personale autorizzato. Inoltre, Microsoft 365 la gestione dei log di controllo a un sottoinsieme limitato di membri del team di sicurezza responsabili della funzionalità di controllo. Il team di sicurezza non dispone dell'accesso amministrativo permanente Cosmos. L'accesso amministrativo richiede l'approvazione dell'accesso JIT (Just-In-Time) e tutte le modifiche apportate ai meccanismi di registrazione per Cosmos vengono registrate e verificate. I log di controllo vengono conservati abbastanza a lungo da supportare le indagini degli incidenti e soddisfare i requisiti normativi. Il periodo esatto di conservazione dei dati del log di controllo Cosmos è determinato dai team del servizio; la maggior parte dei dati del registro di controllo viene conservata per 90 giorni o più.

## <a name="how-does-microsoft-365-protect-end-user-identifiable-information-that-may-be-captured-in-audit-logs"></a>In che modo Microsoft 365 proteggere le informazioni identificabili dell'utente finale che possono essere acquisite nei log di controllo?

Prima di caricare i dati di registro, l'applicazione ODL utilizza un servizio di pulitura per rimuovere tutti i campi che contengono i dati dei clienti, ad esempio le informazioni sul tenant e le informazioni identificabili dall'utente finale, e sostituire tali campi con un valore hash. I log anonimi e con hash vengono riscritti e quindi caricati in Cosmos. Tutti i trasferimenti di log vengono eseguiti tramite una connessione crittografata TLS (FIPS 140-2).

## <a name="related-external-regulations--certifications"></a>Normative esterne correlate & certificazioni

I servizi online di Microsoft vengono regolarmente controllati per la conformità alle normative e alle certificazioni esterne. Fare riferimento alla tabella seguente per la convalida dei controlli correlati alla registrazione di controllo.

| **Controlli esterni** | **Sezione** | **Data ultimo report** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | AU-2: Eventi di controllo <br> AU-3: Contenuto dei record di controllo <br> AU-4: Controllare la capacità di archiviazione <br> AU-5: Risposta agli errori di elaborazione del controllo <br> AU-6: Revisione, analisi e creazione di report di controllo <br> AU-7: Riduzione del controllo e generazione di report <br> AU-8: Indicatori di data e ora <br> AU-9: Protezione delle informazioni di controllo  <br> AU-10: Non ripudio <br> AU-11: Conservazione dei record di controllo <br> AU-12: Generazione di controllo  | 24 settembre 2020 | 
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Dichiarazione di applicabilità](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Certificazione](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.4: Registrazione e monitoraggio | 20 aprile 2021 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Dichiarazione di applicabilità](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Certificazione](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.4: Registrazione e monitoraggio | 20 aprile 2021 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-48: Registrazione datacenter <br> CA-60: registrazione di controllo | 24 dicembre 2020 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-48: Registrazione datacenter <br> CA-60: registrazione di controllo | 24 dicembre 2020|