---
title: Panoramica delle operazioni e dello sviluppo della sicurezza
description: Informazioni sullo sviluppo e sulle operazioni di sicurezza in Microsoft 365
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
ms.openlocfilehash: b74c004e63838900f87c774a8acf84ab8aeb03d4
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2021
ms.locfileid: "58947427"
---
# <a name="security-development-and-operations-overview"></a>Panoramica delle operazioni e dello sviluppo della sicurezza

## <a name="how-does-microsoft-implement-secure-development-practices"></a>In che modo Microsoft implementa procedure di sviluppo sicure?

Microsoft Security Development Lifecycle (SDL) è un processo di garanzia di sicurezza incentrato sullo sviluppo e sul funzionamento di un software sicuro. SDL offre requisiti di sicurezza dettagliati e misurabili affinché sviluppatori e ingegneri di Microsoft possano ridurre il numero e la gravità delle vulnerabilità nei nostri prodotti e servizi. Tutti i team di sviluppo software Microsoft devono rispettare i requisiti SDL e il processo SDL viene costantemente aggiornato per riflettere il panorama delle minacce in evoluzione, le procedure consigliate del settore e gli standard normativi per la conformità.

## <a name="how-does-microsofts-sdl-improve-application-security"></a>In che modo il processo SDL di Microsoft migliora la sicurezza delle applicazioni?

Il processo SDL di Microsoft può essere pensato in termini di cinque fasi di sviluppo: requisiti, progettazione, implementazione, verifica e rilascio. Inizia dalla definizione dei requisiti software tenendo conto della sicurezza. Per raggiungere questo obiettivo, vengono poste domande rilevanti per la sicurezza sulle attività che l'applicazione deve eseguire. L'applicazione deve raccogliere dati sensibili? L'applicazione eseguirà attività importanti o sensibili? L'applicazione deve accettare l'input di origini non attendibili?

Una volta identificati i requisiti di sicurezza pertinenti, progettiamo il nostro software affinché incorpori le funzionalità di sicurezza adatte a soddisfare questi requisiti. I nostri sviluppatori implementano l'SDL e i requisiti di progettazione nel codice, che poi noi verifichiamo tramite analisi manuale del codice, strumenti di sicurezza automatici e test di penetrazione. Infine, prima che il codice possa essere rilasciato, le nuove funzionalità e le modifiche materiali vengono sottoposte alla revisione finale della sicurezza e della privacy per garantire che tutti i requisiti siano soddisfatti.

## <a name="how-does-microsoft-test-source-code-for-common-vulnerabilities"></a>In che modo Microsoft testa il codice sorgente per le vulnerabilità comuni?

Per supportare gli sviluppatori nell'implementazione dei requisiti di sicurezza durante lo sviluppo del codice e dopo il rilascio, Microsoft offre una suite di strumenti di sviluppo sicuri per controllare automaticamente il codice sorgente e rilevare eventuali difetti e vulnerabilità della sicurezza. Microsoft definisce e pubblica un elenco di strumenti approvati che gli sviluppatori possono usare, ad esempio compilatori e ambienti di sviluppo, insieme ai controlli di sicurezza incorporati eseguiti automaticamente nelle pipeline di compilazione Microsoft. I nostri sviluppatori usano le versioni più recenti degli strumenti approvati per sfruttare le nuove funzionalità di sicurezza.

Prima che il codice possa essere archiviato in un ramo di rilascio, il file SDL richiede la revisione manuale del codice da parte di un revisore separato. I revisori del codice verificano la presenza di errori di codifica e verificano che le modifiche al codice soddisfino i requisiti di progettazione e SDL, superino i test funzionali e di sicurezza e abbiano prestazioni affidabili. Esaminano anche la documentazione, le configurazioni e le dipendenze associate per garantire che le modifiche al codice siano documentate in modo appropriato e non provochino effetti collaterali imprevisti. Se un revisore rileva problemi durante la revisione del codice, può chiedere al mittente di inviare di nuovo il codice con modifiche suggerite e test aggiuntivi. I revisori del codice possono anche decidere di bloccare completamente l'archiviazione per il codice che non soddisfa i requisiti. Dopo che il codice è stato ritenuto soddisfacente dal revisore, il revisore fornisce l'approvazione, necessaria prima che il codice possa passare alla fase di distribuzione successiva.

Oltre a proteggere gli strumenti di sviluppo e la revisione manuale del codice, Microsoft applica i requisiti SDL utilizzando strumenti di sicurezza automatizzati. Molti di questi strumenti sono incorporati nella pipeline di commit e analizzano automaticamente il codice per i difetti di sicurezza quando viene archiviato e quando vengono compilate nuove build. Alcuni esempi includono l'analisi del codice statico per difetti di sicurezza comuni e scanner di credenziali che analizzano il codice per i segreti incorporati. I problemi scoperti dagli strumenti di sicurezza automatizzati devono essere risolti prima che le nuove build possano superare la revisione della sicurezza e essere approvate per il rilascio.

## <a name="how-does-microsoft-manage-open-source-software"></a>In che modo Microsoft gestisce il software open source?

Microsoft ha adottato una strategia di alto livello per la gestione della sicurezza open source, che utilizza strumenti e flussi di lavoro progettati per:

- Conoscere i componenti open source usati nei prodotti e nei servizi Microsoft.
- Tenere traccia della posizione e del modo in cui vengono usati tali componenti.
- Determinare se tali componenti presentano vulnerabilità.
- Rispondere correttamente quando vengono individuate vulnerabilità che interessano tali componenti.

I team di progettazione Microsoft sono responsabili della sicurezza di tutto il software open source incluso in un prodotto o servizio. Per ottenere questa sicurezza su larga scala, Microsoft ha integrato le funzionalità essenziali nei sistemi di progettazione tramite Component Governance (CG), che automatizza il rilevamento open source, i flussi di lavoro dei requisiti legali e l'avviso per i componenti vulnerabili. Gli strumenti CG automatizzati analizzano le build di Microsoft per la ricerca di componenti open source e vulnerabilità della sicurezza o obblighi legali associati. I componenti individuati vengono registrati e inviati ai team appropriati per le verifiche aziendali e di sicurezza. Queste verifiche sono progettate per valutare eventuali obblighi legali o vulnerabilità di sicurezza associati ai componenti open source e risolverli prima di approvare la distribuzione dei componenti.

## <a name="related-external-regulations--certifications"></a>Normative esterne correlate & certificazioni

I servizi online di Microsoft vengono regolarmente controllati per la conformità alle normative e alle certificazioni esterne. Fare riferimento alla tabella seguente per la convalida dei controlli correlati allo sviluppo e al funzionamento della sicurezza.

### <a name="azure-and-dynamics-365"></a>Azure e Dynamics 365

| **Controlli esterni** | **Sezione** | **Data ultimo report** |
|:--------------------|:------------|:-----------------------|
| [ISO 27001/27002](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Dichiarazione di applicabilità](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=00af6c3e-7f3e-4e0d-8b0e-79f45ef2cef1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Certificazione](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7af5304-3a31-40e6-9abb-e26352305d41&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.1.2: Modificare i controlli di gestione <br> A.14.2: Sicurezza nei processi di sviluppo e supporto | 2 dicembre 2020 |
| [ISO 27017](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Dichiarazione di applicabilità](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a3bca0ac-867d-4204-b66b-13665f5f1e8d&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Certificazione](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=25718a8a-f34d-41e1-a95a-c49246508787&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.1.2: Modificare i controlli di gestione <br> A.14.2: Sicurezza nei processi di sviluppo e supporto | 2 dicembre 2020 |
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b8721ebd-af20-42fe-b22f-8332b0a19517&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=234a0f57-83c1-4afc-a586-a0e7a59592f7&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 3](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=75c8cbf6-e456-473c-a05e-34fea888ec2a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | SDL-1: metodologia SDL (Security Development Lifecycle) <br> SDL-2: requisiti di controllo della sicurezza documentati nelle versioni <br> SDL-4: separazione degli ambienti di test e produzione <br> SDL-6: analisi malware nelle build del codice sorgente <br> SDL7: revisione semestral di SDL | 31 marzo 2021 |

### <a name="office-365"></a>Office 365

| **Controlli esterni** | **Sezione** | **Data ultimo report** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP](https://compliance.microsoft.com/compliancemanager) | SA-3: Ciclo di vita dello sviluppo del sistema | 24 settembre 2020 |
| [ISO 27001/27002/27017](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Dichiarazione di applicabilità](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.1.2: Modificare i controlli di gestione <br> A.14.2: Sicurezza nei processi di sviluppo e supporto | 20 aprile 2021 |
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-03: Gestione dei rischi <br> CA-18: Gestione delle modifiche <br> CA-19: Monitoraggio delle modifiche <br> CA-21: Test delle modifiche <br> CA-38: Configurazioni di base <br> CA-46: Revisione della sicurezza | 24 dicembre 2020 |

## <a name="resources"></a>Risorse

- [Ciclo di vita dello sviluppo della sicurezza di Microsoft](https://www.microsoft.com/securityengineering/sdl)
