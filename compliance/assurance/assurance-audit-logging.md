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
ms.localizationpriority: medium
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
search.appverid:
- MET150
- MOE150
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 9d539899aecb68c4629ad27bea0d455353716c4e
ms.sourcegitcommit: 444a58b28f8611323e16d28b4c63a0f68eaaafa6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2021
ms.locfileid: "60780122"
---
# <a name="audit-logging-overview"></a>Panoramica sulla registrazione di controllo

## <a name="how-do-microsoft-online-services-employ-audit-logging"></a>In che modo i servizi online Microsoft utilizzano la registrazione di controllo?

I servizi online Microsoft utilizzano la registrazione di controllo per rilevare attività non autorizzate e fornire responsabilità al personale Microsoft. I log di controllo acquisiscono i dettagli sulle modifiche alla configurazione del sistema e sugli eventi di accesso, con i dettagli per identificare chi è stato responsabile dell'attività, quando e dove si è verificata l'attività e qual è il risultato dell'attività. L'analisi automatizzata dei log supporta il rilevamento quasi in tempo reale di comportamenti sospetti. I potenziali incidenti vengono inoltrati al team di risposta alla sicurezza Microsoft appropriato per ulteriori indagini.

La registrazione di controllo interna dei servizi online Microsoft acquisisce i dati di registro da varie origini, ad esempio:

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

## <a name="how-do-microsoft-online-services-centralize-and-report-on-audit-logs"></a>In che modo i servizi online Microsoft centralizzano e segnalano i log di controllo?

Molti tipi diversi di dati di log vengono caricati dai server Microsoft in una soluzione di monitoraggio della sicurezza proprietaria per l'analisi in tempo quasi reale (NRT) e un servizio di big data computing interno (Cosmos) o Azure Data Explorer (Kusto) per l'archiviazione a lungo termine. Questo trasferimento dei dati avviene tramite una connessione TLS convalidata da FIPS 140-2 su porte e protocolli approvati tramite strumenti di gestione dei log automatizzati.

I log vengono elaborati in NRT utilizzando metodi di apprendimento automatico, statistici e basati su regole per rilevare gli indicatori delle prestazioni del sistema e i potenziali eventi di sicurezza. I modelli di machine learning utilizzano i dati dei registri in ingresso e i dati cronologici archiviati in Cosmos o Kusto per migliorare continuamente le funzionalità di rilevamento. I rilevamenti correlati alla sicurezza generano avvisi, notificando ai tecnici di chiamata di un potenziale incidente e attivando azioni di correzione automatizzate, se applicabile. Oltre al monitoraggio automatico della sicurezza, i team di servizio utilizzano strumenti di analisi e dashboard per la correlazione dei dati, le query interattive e l'analisi dei dati. Questi report vengono utilizzati per monitorare e migliorare le prestazioni complessive del servizio.

Per ulteriori informazioni sul monitoraggio della sicurezza e sugli avvisi, vedere Panoramica [del monitoraggio della sicurezza.](assurance-security-monitoring.md)

![Controllare il flusso di dati.](../media/assurance-audit-data-flow.png)

## <a name="how-do-microsoft-online-services-protect-audit-logs"></a>In che modo i servizi online Microsoft proteggono i log di controllo?

Gli strumenti utilizzati nei servizi online Microsoft per raccogliere ed elaborare i record di controllo non consentono modifiche permanenti o irreversibili al contenuto del record di controllo originale o all'ordinamento temporale. L'accesso ai dati dei servizi online Microsoft archiviati in Cosmos o Kusto è limitato al personale autorizzato. Inoltre, Microsoft limita la gestione dei log di controllo a un sottoinsieme limitato di membri del team di sicurezza responsabili della funzionalità di controllo. Il personale del team di sicurezza non dispone dell'accesso amministrativo permanente Cosmos o Kusto. L'accesso amministrativo richiede l'approvazione dell'accesso JIT (Just-In-Time) e tutte le modifiche ai meccanismi di registrazione per Cosmos vengono registrate e verificate. I log di controllo vengono conservati abbastanza a lungo da supportare le indagini degli incidenti e soddisfare i requisiti normativi. Il periodo esatto di conservazione dei dati del log di controllo determinato dai team del servizio; la maggior parte dei dati del registro di controllo viene conservata per 90 giorni Cosmos e 180 giorni a Kusto.

## <a name="how-do-microsoft-online-services-protect-user-personal-data-that-may-be-captured-in-audit-logs"></a>In che modo i servizi online Microsoft proteggono i dati personali degli utenti che possono essere acquisiti nei log di controllo?

Prima di caricare i dati di registro, un'applicazione di gestione dei log automatizzata utilizza un servizio di pulitura per rimuovere tutti i campi che contengono i dati dei clienti, ad esempio le informazioni del tenant e i dati personali dell'utente, e sostituire tali campi con un valore hash. I log anonimi e con hash vengono riscritti e quindi caricati in Cosmos. Tutti i trasferimenti di log vengono eseguiti tramite una connessione crittografata TLS (FIPS 140-2).

## <a name="related-external-regulations--certifications"></a>Normative esterne correlate & certificazioni

I servizi online di Microsoft vengono regolarmente controllati per la conformità alle normative e alle certificazioni esterne. Fare riferimento alla tabella seguente per la convalida dei controlli correlati alla registrazione di controllo.

### <a name="azure-and-dynamics-365"></a>Azure e Dynamics 365

| **Controlli esterni** | **Sezione** | **Data ultimo report** |
|:--------------------|:------------|:-----------------------|
| [ISO 27001/27002](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Dichiarazione di applicabilità](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=00af6c3e-7f3e-4e0d-8b0e-79f45ef2cef1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Certificazione](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7af5304-3a31-40e6-9abb-e26352305d41&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.4: Registrazione e monitoraggio | 2 dicembre 2020 |
| [ISO 27017](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Dichiarazione di applicabilità](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a3bca0ac-867d-4204-b66b-13665f5f1e8d&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Certificazione](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=25718a8a-f34d-41e1-a95a-c49246508787&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.4: Registrazione e monitoraggio | 2 dicembre 2020 |
| [ISO 27018](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Dichiarazione di applicabilità](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=00af6c3e-7f3e-4e0d-8b0e-79f45ef2cef1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Certificazione](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=56904fc3-0942-4ff5-9eef-7cabc751a25c&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.4: Registrazione e monitoraggio | 2 dicembre 2020 |
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b8721ebd-af20-42fe-b22f-8332b0a19517&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | VM-1: raccolta e registrazione degli eventi di sicurezza | 31 marzo 2021 |
| [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=234a0f57-83c1-4afc-a586-a0e7a59592f7&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | C5-6: accesso limitato ai log <br> VM-1: raccolta e registrazione degli eventi di sicurezza | 31 marzo 2021 |

### <a name="office-365"></a>Office 365

| **Controlli esterni** | **Sezione** | **Data ultimo report** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP](https://compliance.microsoft.com/compliancemanager) | AU-2: Eventi di controllo <br> AU-3: Contenuto dei record di controllo <br> AU-4: Controllare la capacità di archiviazione <br> AU-5: Risposta agli errori di elaborazione del controllo <br> AU-6: Revisione, analisi e creazione di report di controllo <br> AU-7: Riduzione del controllo e generazione di report <br> AU-8: Indicatori di data e ora <br> AU-9: Protezione delle informazioni di controllo  <br> AU-10: Non ripudio <br> AU-11: Conservazione dei record di controllo <br> AU-12: Generazione di controllo  | 24 settembre 2020 |
| [ISO 27001/27002/27017](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=08ce227f-d1d9-4c4c-b255-4f2e4ec8f941&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Dichiarazione di applicabilità](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Certificazione](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.4: Registrazione e monitoraggio | 20 aprile 2021 |
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-48: Registrazione datacenter <br> CA-60: registrazione di controllo | 24 dicembre 2020 |