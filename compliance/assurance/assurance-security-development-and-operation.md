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
ms.openlocfilehash: 7a706cda887c0c2675841648ef8541ffbb872884
ms.sourcegitcommit: 07578a8e03b931f47c49f4e34b78cf8ba0605e8f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/23/2021
ms.locfileid: "53573694"
---
# <a name="security-development-and-operations-overview"></a>Panoramica delle operazioni e dello sviluppo della sicurezza

## <a name="how-does-microsoft-implement-secure-development-practices"></a>In che modo Microsoft implementa procedure di sviluppo sicure?

Il security development lifecycle (SDL) di Microsoft è un processo di garanzia della sicurezza incentrato sullo sviluppo e l'utilizzo di software sicuro. SDL fornisce requisiti di sicurezza dettagliati e misurabili per sviluppatori e tecnici di Microsoft per ridurre il numero e la gravità delle vulnerabilità nei nostri prodotti e servizi. Tutti i team di sviluppo software Microsoft devono rispettare i requisiti SDL e il processo SDL viene costantemente aggiornato per riflettere il panorama delle minacce in evoluzione, le procedure consigliate del settore e gli standard normativi per la conformità.

## <a name="how-does-microsofts-sdl-improve-application-security"></a>In che modo il processo SDL di Microsoft migliora la sicurezza delle applicazioni?

Il processo SDL di Microsoft può essere pensato in termini di cinque fasi di sviluppo: requisiti, progettazione, implementazione, verifica e rilascio. Si inizia definendo i requisiti software con la sicurezza in mente. A tale scopo, vengono poste domande rilevanti per la sicurezza sulle attività che l'applicazione deve eseguire. L'applicazione deve raccogliere dati sensibili? L'applicazione eseguirà attività sensibili o importanti? L'applicazione deve accettare l'input da origini non attendibili?

Dopo aver identificato i requisiti di sicurezza pertinenti, progettiamo il software in modo da incorporare funzionalità di sicurezza che soddisfino questi requisiti. I nostri sviluppatori implementano SDL e i requisiti di progettazione nel codice, che verifichiamo tramite revisione manuale del codice, strumenti di sicurezza automatizzati e test di penetrazione. Infine, prima che il codice possa essere rilasciato, le nuove funzionalità e le modifiche materiali vengono sottoposte alla revisione finale della sicurezza e della privacy per garantire che tutti i requisiti siano soddisfatti.

## <a name="how-does-microsoft-test-source-code-for-common-vulnerabilities"></a>In che modo Microsoft testa il codice sorgente per le vulnerabilità comuni?

Per supportare gli sviluppatori nell'implementazione dei requisiti di sicurezza durante lo sviluppo del codice e dopo il rilascio, Microsoft fornisce una famiglia di strumenti di sviluppo sicuri per verificare automaticamente la presenza di difetti e vulnerabilità della sicurezza nel codice sorgente. Microsoft definisce e pubblica un elenco di strumenti approvati che gli sviluppatori possono usare, ad esempio compilatori e ambienti di sviluppo, insieme ai controlli di sicurezza incorporati eseguiti automaticamente nelle pipeline di compilazione Microsoft. I nostri sviluppatori usano le versioni più recenti degli strumenti approvati per sfruttare le nuove funzionalità di sicurezza.

Prima che il codice possa essere archiviato in un ramo di rilascio, il file SDL richiede la revisione manuale del codice da parte di un revisore separato. I revisori del codice verificano la presenza di errori di codifica e verificano che le modifiche al codice soddisfino i requisiti di progettazione e SDL, superino test funzionali e di sicurezza ed esercitino operazioni affidabili. Esaminano anche la documentazione, le config e le dipendenze associate per verificare che le modifiche al codice siano documentate in modo appropriato e non causeranno effetti collaterali indesiderati. Se un revisore rileva problemi durante la revisione del codice, può chiedere al mittente di inviare di nuovo il codice con modifiche suggerite e test aggiuntivi. I revisori del codice possono anche decidere di bloccare completamente l'archiviazione per il codice che non soddisfa i requisiti. Dopo che il codice è stato ritenuto soddisfacente dal revisore, il revisore fornisce l'approvazione, necessaria prima che il codice possa passare alla fase di distribuzione successiva.

Oltre a proteggere gli strumenti di sviluppo e la revisione manuale del codice, Microsoft applica i requisiti SDL utilizzando strumenti di sicurezza automatizzati. Molti di questi strumenti sono incorporati nella pipeline di commit e analizzano automaticamente il codice per i difetti di sicurezza quando viene archiviato e quando vengono compilate nuove build. Alcuni esempi includono l'analisi del codice statico per difetti di sicurezza comuni e scanner di credenziali che analizzano il codice per i segreti incorporati. I problemi scoperti dagli strumenti di sicurezza automatizzati devono essere risolti prima che le nuove build possano superare la revisione della sicurezza e essere approvate per il rilascio.

## <a name="how-does-microsoft-manage-open-source-software"></a>In che modo Microsoft gestisce il software open source?

Microsoft ha adottato una strategia di alto livello per la gestione della sicurezza open source, che sfrutta strumenti e flussi di lavoro progettati per:

- Comprendere quali componenti open source vengono utilizzati nei prodotti e nei servizi.
- Tenere traccia della posizione e della modalità di utilizzo di tali componenti.
- Determinare se tali componenti hanno vulnerabilità.
- Rispondere correttamente quando vengono rilevate vulnerabilità che interessano tali componenti.

I team di progettazione Microsoft mantengono la responsabilità della sicurezza di tutto il software open source incluso in un prodotto o in un servizio. Per ottenere questo risultato su larga scala, Microsoft ha integrato funzionalità essenziali nei sistemi di progettazione tramite CG, che automatizza il rilevamento open source, i flussi di lavoro dei requisiti legali e l'avviso per i componenti vulnerabili. Gli strumenti CG automatizzati analizzano le build di Microsoft per la ricerca di componenti open source e vulnerabilità della sicurezza o obblighi legali associati. I componenti individuati vengono registrati e inviati ai team appropriati per le revisioni aziendali e di sicurezza. Queste revisioni sono progettate per valutare eventuali obblighi legali o vulnerabilità della sicurezza associate ai componenti open source e risolverli prima di approvare i componenti per la distribuzione.

## <a name="related-external-regulations--certifications"></a>Normative esterne correlate & certificazioni

I servizi online di Microsoft vengono regolarmente controllati per la conformità alle normative e alle certificazioni esterne. Fare riferimento alla tabella seguente per la convalida dei controlli correlati allo sviluppo e al funzionamento della sicurezza.

| **Controlli esterni** | **Sezione** | **Data ultimo report** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | SA-3: Ciclo di vita dello sviluppo del sistema | 24 settembre 2020 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Dichiarazione di applicabilità](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Certificazione](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.1.2: Modificare i controlli di gestione <br> A.14.2: Sicurezza nei processi di sviluppo e supporto | 20 aprile 2021 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Dichiarazione di applicabilità](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Certificazione](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.1.2: Modificare i controlli di gestione <br> A.14.2: Sicurezza nei processi di sviluppo e supporto | 20 aprile 2021 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-03: Gestione dei rischi <br> CA-18: Gestione delle modifiche <br> CA-19: Monitoraggio delle modifiche <br> CA-21: Test delle modifiche <br> CA-38: Configurazioni di base <br> CA-46: Revisione della sicurezza | 24 dicembre 2020 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-03: Gestione dei rischi <br> CA-18: Gestione delle modifiche <br> CA-19: Monitoraggio delle modifiche <br> CA-21: Test delle modifiche <br> CA-38: Configurazioni di base <br> CA-46: Revisione della sicurezza | 24 dicembre 2020 |

## <a name="resources"></a>Risorse

- [Ciclo di vita dello sviluppo della sicurezza di Microsoft](https://www.microsoft.com/securityengineering/sdl)
