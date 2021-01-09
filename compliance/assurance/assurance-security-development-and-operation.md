---
title: Panoramica delle operazioni e dello sviluppo della sicurezza
description: Informazioni sullo sviluppo e le operazioni di sicurezza in Microsoft 365
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
search.appverid:
- MET150
- MOE150
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: 916303ff2a65777785c89c6ccae70bea9a0bfda9
ms.sourcegitcommit: 7a5b6bc58fc4613b38f3fda20aebee5cec6a5730
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "49787305"
---
# <a name="security-development-and-operations-overview"></a>Panoramica delle operazioni e dello sviluppo della sicurezza

## <a name="how-does-microsoft-implement-secure-development-practices"></a>In che modo Microsoft implementa le procedure di sviluppo sicure?

Il Security Development Lifecycle (SDL) di Microsoft è un processo di verifica della sicurezza incentrato sullo sviluppo e sul funzionamento del software sicuro. SDL fornisce requisiti di sicurezza dettagliati e misurabili per sviluppatori e ingegneri di Microsoft per ridurre il numero e la gravità delle vulnerabilità nei prodotti e servizi. Tutti i team di sviluppo software Microsoft devono seguire i requisiti di SDL e aggiornare continuamente il processo SDL per riflettere il paesaggio mutevole delle minacce, le procedure consigliate per l'industria e gli standard normativi per la conformità.

## <a name="how-does-microsofts-sdl-improve-application-security"></a>Come funziona SDL di Microsoft per migliorare la sicurezza delle applicazioni?

Il processo SDL di Microsoft può essere considerato in termini di cinque fasi di sviluppo: requisiti, progettazione, implementazione, verifica e rilascio. Inizia definendo i requisiti software con la sicurezza in mente. A tale scopo, vengono richieste questioni rilevanti per la sicurezza relative all'applicazione che deve eseguire. L'applicazione deve raccogliere dati sensibili? L'applicazione eseguirà attività importanti o sensibili? L'applicazione deve accettare l'input da origini non attendibili?

Una volta identificati i requisiti di sicurezza rilevanti, il software viene progettato per incorporare le funzionalità di sicurezza che soddisfano tali requisiti. Gli sviluppatori implementano i requisiti di progettazione e SDL nel codice, che vengono verificati tramite la revisione manuale del codice, gli strumenti di sicurezza automatizzati e i test di penetrazione. Infine, prima che il codice possa essere rilasciato, le nuove caratteristiche e le modifiche materiali subiscono la sicurezza finale e la revisione della privacy per garantire che siano soddisfatti tutti i requisiti.

## <a name="how-does-microsoft-test-source-code-for-common-vulnerabilities"></a>Come funziona il codice sorgente di Microsoft Test per le vulnerabilità comuni?

Per supportare gli sviluppatori nell'implementazione dei requisiti di sicurezza durante lo sviluppo del codice e dopo la versione, Microsoft offre una serie di strumenti di sviluppo sicuri per il controllo automatico del codice sorgente per i difetti di sicurezza e le vulnerabilità. Microsoft definisce e pubblica un elenco di strumenti approvati per gli sviluppatori da utilizzare, quali compilatori e ambienti di sviluppo, insieme ai controlli di sicurezza incorporati eseguiti automaticamente all'interno delle pipeline di Microsoft Build. Gli sviluppatori utilizzano le versioni più recenti degli strumenti approvati per trarre vantaggio dalle nuove funzionalità di sicurezza.

Prima che il codice possa essere archiviato in una filiale di rilascio, SDL richiede la revisione manuale del codice da parte di un revisore separato. I revisori del codice verificano la presenza di errori di codifica e verificano che le modifiche al codice soddisfino i requisiti di SDL e progettazione, superino i test di sicurezza e funzionali Vengono inoltre esaminate la documentazione, le configurazioni e le dipendenze associate per garantire che le modifiche al codice siano documentate in modo appropriato e che non provochino effetti collaterali indesiderati. Se un revisore trova problemi durante la revisione del codice, può chiedere al mittente di inviare di nuovo il codice con le modifiche consigliate e i test aggiuntivi. I revisori del codice possono anche decidere di bloccare completamente l'archiviazione per il codice che non soddisfa i requisiti. Una volta che il codice è stato considerato soddisfacente dal revisore, il revisore fornisce l'approvazione, che è necessario prima che il codice possa procedere alla fase di distribuzione successiva.

Oltre a proteggere gli strumenti di sviluppo e la revisione manuale del codice, Microsoft applica i requisiti di SDL tramite lo strumento di sicurezza automatizzato. Molti di questi strumenti sono incorporati nella pipeline di commit e analizzano automaticamente il codice per i difetti di sicurezza così come vengono archiviati e vengono compilate le nuove compilazioni. Tra gli esempi sono inclusi l'analisi del codice statico per difetti di sicurezza comuni e scanner di credenziali che analizzano il codice per i segreti incorporati. I problemi individuati dagli strumenti di sicurezza automatici devono essere corretti prima che le nuove compilazioni possano superare la revisione della sicurezza ed essere approvate per il rilascio.

## <a name="how-does-microsoft-manage-open-source-software"></a>In che modo Microsoft gestisce il software open source?

Microsoft ha adottato una strategia di alto livello per la gestione della sicurezza open source, che sfrutta gli strumenti e i flussi di lavoro creati per:

- Informazioni sui componenti open-source utilizzati nei prodotti e nei servizi.
- Individuare la posizione e la modalità di utilizzo dei componenti.
- Determinare se i componenti presentano vulnerabilità.
- Rispondere correttamente quando vengono individuate vulnerabilità che interessano tali componenti.

I team di Microsoft Engineering mantengono la responsabilità per la sicurezza di tutto il software open-source incluso in un prodotto o servizio. Per ottenere questo risultato in scala, Microsoft ha creato funzionalità essenziali nei sistemi ingegneristici tramite CG, che automatizza il rilevamento open source, i flussi di lavoro dei requisiti legali e gli avvisi per i componenti vulnerabili. L'analisi automatizzata degli strumenti CG esegue la generazione in Microsoft per i componenti open-source e le vulnerabilità di sicurezza associate o gli obblighi legali. I componenti individuati vengono registrati e inoltrati ai team di sicurezza per le aziende e le revisioni appropriate. Tali recensioni sono progettate per valutare eventuali obblighi legali o vulnerabilità di sicurezza associati ai componenti open-source e risolverli prima di approvare i componenti per la distribuzione.

## <a name="related-external-regulations--certifications"></a>Normative esterne correlate & certificazioni

I servizi online di Microsoft vengono controllati regolarmente per la conformità con le certificazioni e le normative esterne. Fare riferimento alla tabella seguente per la convalida dei controlli relativi allo sviluppo e all'operazione di sicurezza.

| **Verifiche esterne** | **Sezione** | **Data ultimo rapporto** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | SA-3: ciclo di vita dello sviluppo del sistema | 24 settembre 2020 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Dichiarazione di applicabilità](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certificazione](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A. 12.1.2: Change Management Controls <br> A. 14.2: sicurezza nei processi di sviluppo e supporto | 22 febbraio 2020 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Dichiarazione di applicabilità](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certificazione](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A. 12.1.2: Change Management Controls <br> A. 14.2: sicurezza nei processi di sviluppo e supporto | 22 febbraio 2020 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-03: gestione dei rischi <br> CA-18: Change Management <br> CA-19: modifica del monitoraggio <br> CA-21: modificare i test <br> CA-38: configurazioni di base <br> CA-46: Revisione della sicurezza | 24 dicembre 2020 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-03: gestione dei rischi <br> CA-18: Change Management <br> CA-19: modifica del monitoraggio <br> CA-21: modificare i test <br> CA-38: configurazioni di base <br> CA-46: Revisione della sicurezza | 24 dicembre 2020 |

## <a name="resources"></a>Risorse

- [Ciclo di vita dello sviluppo della sicurezza di Microsoft](https://www.microsoft.com/securityengineering/sdl)
