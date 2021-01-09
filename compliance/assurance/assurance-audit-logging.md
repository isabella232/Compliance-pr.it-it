---
title: Panoramica sulla registrazione di controllo
description: Informazioni sulla registrazione dei controlli in Microsoft 365
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
ms.openlocfilehash: 6e32e089a5b42f846a332e32218959fef5103615
ms.sourcegitcommit: 7a5b6bc58fc4613b38f3fda20aebee5cec6a5730
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "49787505"
---
# <a name="audit-logging-overview"></a>Panoramica sulla registrazione di controllo

## <a name="how-does-microsoft-365-employ-audit-logging"></a>In che modo Microsoft 365 impiega la registrazione di controllo?

Microsoft 365 impiega la registrazione di controllo per rilevare attività non autorizzate nei propri prodotti e servizi e fornire la responsabilità per il personale Microsoft. I registri di controllo acquisiscono informazioni dettagliate sulle modifiche alla configurazione del sistema e sugli eventi di Access, con informazioni dettagliate per identificare gli utenti responsabili dell'attività, quando e dove hanno avuto luogo e quali sono i risultati dell'attività. L'analisi automatizzata dei log supporta il rilevamento quasi in tempo reale di comportamenti sospetti. I possibili incidenti sono stati inoltrati al team di risposta alla sicurezza di Microsoft 365 per ulteriori indagini.

La registrazione di controllo interno Microsoft 365 acquisisce i dati di log da una vasta gamma di origini, ad esempio:

- Registri eventi
- Registri di AppLocker
- Dati sulle prestazioni
- Dati di System Center
- Record dettagli chiamata
- Dati sulla qualità delle esperienze
- Registri del server Web IIS
- Registri di SQL Server
- Dati syslog
- Registri di controllo della sicurezza

## <a name="how-does-microsoft-365-centralize-and-report-on-audit-logs"></a>In che modo Microsoft 365 centralizza e segnala i registri di controllo?

Molti tipi diversi di dati di log vengono caricati da server Microsoft 365 a un servizio di elaborazione dati di grandi dimensioni interno denominato Cosmos. Ogni team di servizio carica i registri di controllo dai rispettivi server nel database Cosmos per l'aggregazione e l'analisi. Questo trasferimento dei dati si verifica su una connessione TLS convalidata FIPS 140-2 su porte e protocolli approvati tramite uno strumento di automazione proprietaria denominato Office Data Loader (FAD).

I team di servizio eseguono query con ambito sui dati in Cosmos per la correlazione dei log, gli avvisi e i report. Ad esempio, il team di sicurezza di Microsoft 365 utilizza i dati di Cosmos con un parser del registro eventi proprietario per correlare i dati di log, inviare avvisi e generare report azionabili su possibili attività sospette nell'ambiente di produzione di Microsoft 365. I report di questi dati vengono utilizzati per correggere le vulnerabilità e per migliorare le prestazioni complessive del servizio.

## <a name="how-does-microsoft-365-protect-audit-logs"></a>In che modo Microsoft 365 protegge i log di controllo?

Gli strumenti utilizzati in Microsoft 365 per la raccolta e l'elaborazione dei record di controllo non consentono modifiche permanenti o irreversibili al contenuto del record di controllo originale o all'ordine di tempo. L'accesso ai dati di Microsoft 365 archiviati in Cosmos è limitato al personale autorizzato. Microsoft 365 limita la gestione della funzionalità di controllo al sottoinsieme limitato di membri del team di servizio responsabili della funzionalità di controllo. Questi membri del team non hanno la possibilità di modificare o eliminare i dati dal cosmo e tutte le modifiche apportate ai meccanismi di registrazione per Cosmos vengono registrate e controllate. I registri di controllo vengono mantenuti abbastanza a lungo per supportare le indagini sugli incidenti e soddisfare i requisiti normativi. Il periodo esatto di conservazione dei dati del log di controllo in Cosmos è determinato dai team di servizio. la maggior parte dei dati del registro di controllo viene conservata per 90 giorni o più.

## <a name="how-does-microsoft-365-protect-end-user-identifiable-information-that-may-be-captured-in-audit-logs"></a>In che modo Microsoft 365 protegge le informazioni identificabili dell'utente finale che possono essere acquisite nei registri di controllo?

Prima di caricare i dati in Cosmos, l'applicazione per l'utilizzo dell'assistenza viene utilizzata per nascondere i campi che contengono i dati dei clienti, ad esempio le informazioni sui tenant e le informazioni di identificazione degli utenti finali, e sostituire tali campi con un valore hash. I registri con hash e anonimi vengono riscritti e quindi caricati nel cosmo.

## <a name="related-external-regulations--certifications"></a>Normative esterne correlate & certificazioni

I servizi online di Microsoft vengono controllati regolarmente per la conformità con le certificazioni e le normative esterne. Per la convalida dei controlli relativi alla registrazione di controllo, vedere la tabella seguente.

| **Verifiche esterne** | **Sezione** | **Data ultimo rapporto** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | AU-2: eventi di controllo <br> AU-3: contenuto dei record di controllo <br> AU-4: capacità di archiviazione di controllo <br> AU-5: risposta agli errori di elaborazione del controllo <br> AU-6: revisione, analisi e Reporting di controllo <br> AU-7: riduzione dei controlli e generazione dei report <br> AU-8: indicatori di data e ora <br> AU-9: protezione delle informazioni di controllo  <br> AU-10: non ripudio <br> AU-11: conservazione dei record di controllo <br> AU-12: generazione di controllo  | 24 settembre 2020 | 
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Dichiarazione di applicabilità](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certificazione](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A. 12.4: registrazione e monitoraggio | 22 febbraio 2020 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Dichiarazione di applicabilità](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certificazione](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A. 12.4: registrazione e monitoraggio | 22 febbraio 2020 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-48: registrazione del datacenter <br> CA-60: registrazione di controllo | 24 dicembre 2020 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-48: registrazione del datacenter <br> CA-60: registrazione di controllo | 24 dicembre 2020|