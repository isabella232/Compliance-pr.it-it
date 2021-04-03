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
ms.openlocfilehash: dc56d0413811d59309c974931e1fa50ee184e94a
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497685"
---
# <a name="audit-logging-overview"></a>Panoramica sulla registrazione di controllo

## <a name="how-does-microsoft-365-employ-audit-logging"></a>In che modo Microsoft 365 utilizza la registrazione di controllo?

Microsoft 365 utilizza la registrazione di controllo per rilevare attività non autorizzate nei propri prodotti e servizi e fornire responsabilità al personale Microsoft. I log di controllo acquisiscono dettagli sulle modifiche alla configurazione del sistema e sugli eventi di accesso, con i dettagli per identificare chi è stato responsabile dell'attività, quando e dove si è verificata l'attività e qual è il risultato dell'attività. L'analisi automatizzata dei log supporta il rilevamento quasi in tempo reale di comportamenti sospetti. I potenziali incidenti vengono inoltrati al team di Microsoft 365 Security Response per ulteriori indagini.

La registrazione di controllo interna di Microsoft 365 acquisisce i dati di registro da diverse origini, ad esempio:

- Registri eventi
- Log di AppLocker
- Dati sulle prestazioni
- Dati di System Center
- Record dettagli chiamata
- Dati sulla qualità dell'esperienza
- Registri del server Web IIS
- SQL Server log
- Dati Syslog
- Log di controllo della sicurezza

## <a name="how-does-microsoft-365-centralize-and-report-on-audit-logs"></a>In che modo Microsoft 365 centralizza e segnala i log di controllo?

Molti tipi diversi di dati di registro vengono caricati dai server Microsoft 365 in un servizio di elaborazione dei big data interno denominato Cosmos. Ogni team del servizio carica i log di controllo dai rispettivi server nel database Cosmos per l'aggregazione e l'analisi. Questo trasferimento dei dati avviene tramite una connessione TLS convalidata da FIPS 140-2 su porte e protocolli approvati utilizzando uno strumento di automazione proprietario denominato Office Data Loader (ODL).

I team di servizio eseguono query con ambito sui propri dati in Cosmos per la correlazione dei log, l'avviso e la creazione di report. Ad esempio, il team di sicurezza di Microsoft 365 usa i dati di Cosmos con un parser del registro eventi proprietario per correlare i dati del registro, inviare avvisi e generare report utilizzabili su possibili attività sospette nell'ambiente di produzione di Microsoft 365. I report di questi dati vengono utilizzati per correggere le vulnerabilità e migliorare le prestazioni complessive del servizio.

## <a name="how-does-microsoft-365-protect-audit-logs"></a>In che modo Microsoft 365 protegge i log di controllo?

Gli strumenti utilizzati in Microsoft 365 per raccogliere ed elaborare i record di controllo non consentono modifiche permanenti o irreversibili al contenuto del record di controllo originale o all'ordinamento temporale. L'accesso ai dati di Microsoft 365 archiviati in Cosmos è limitato al personale autorizzato. Microsoft 365 limita la gestione delle funzionalità di controllo al sottoinsieme limitato di membri del team di servizio responsabili della funzionalità di controllo. Questi membri del team non hanno la possibilità di modificare o eliminare dati da Cosmos e tutte le modifiche apportate ai meccanismi di registrazione per Cosmos vengono registrate e verificate. I log di controllo vengono conservati abbastanza a lungo da supportare le indagini degli incidenti e soddisfare i requisiti normativi. Il periodo esatto di conservazione dei dati del log di controllo in Cosmos è determinato dai team del servizio; la maggior parte dei dati del registro di controllo viene conservata per 90 giorni o più.

## <a name="how-does-microsoft-365-protect-end-user-identifiable-information-that-may-be-captured-in-audit-logs"></a>In che modo Microsoft 365 protegge le informazioni identificabili dell'utente finale che possono essere acquisite nei log di controllo?

Prima di caricare dati in Cosmos, l'applicazione ODL utilizza un servizio di scrubbing per offuscare tutti i campi che contengono i dati dei clienti, ad esempio informazioni sul tenant e informazioni identificabili dall'utente finale, e sostituire tali campi con un valore hash. I log anonimi e con hash vengono riscritti e quindi caricati in Cosmos.

## <a name="related-external-regulations--certifications"></a>Normative esterne correlate & certificazioni

I servizi online di Microsoft vengono regolarmente controllati per la conformità alle normative e alle certificazioni esterne. Fare riferimento alla tabella seguente per la convalida dei controlli correlati alla registrazione di controllo.

| **Controlli esterni** | **Sezione** | **Data ultimo report** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | AU-2: Eventi di controllo <br> AU-3: Contenuto dei record di controllo <br> AU-4: Controllare la capacità di archiviazione <br> AU-5: Risposta agli errori di elaborazione del controllo <br> AU-6: Revisione, analisi e creazione di report di controllo <br> AU-7: Riduzione del controllo e generazione di report <br> AU-8: Indicatori di data e ora <br> AU-9: Protezione delle informazioni di controllo  <br> AU-10: Non ripudio <br> AU-11: Conservazione dei record di controllo <br> AU-12: Generazione di controllo  | 24 settembre 2020 | 
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Dichiarazione di applicabilità](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certificazione](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.4: Registrazione e monitoraggio | 22 febbraio 2020 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Dichiarazione di applicabilità](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certificazione](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.4: Registrazione e monitoraggio | 22 febbraio 2020 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-48: Registrazione datacenter <br> CA-60: registrazione di controllo | 24 dicembre 2020 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-48: Registrazione datacenter <br> CA-60: registrazione di controllo | 24 dicembre 2020|