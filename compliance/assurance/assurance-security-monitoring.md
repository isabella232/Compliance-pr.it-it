---
title: Panoramica sul monitoraggio della sicurezza
description: Informazioni sul monitoraggio della sicurezza in Microsoft 365
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
ms.openlocfilehash: 37213f9c9ccab59bbd956cb64c1b2f16a8d72821
ms.sourcegitcommit: 1f30616328d7deb04e41dcbd44a330ea937fe94f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/26/2021
ms.locfileid: "60582479"
---
# <a name="security-monitoring-overview"></a>Panoramica sul monitoraggio della sicurezza

## <a name="what-is-microsofts-strategy-for-monitoring-security"></a>Qual è la strategia di Microsoft per il monitoraggio della sicurezza?

Microsoft si impegna a monitorare la sicurezza continua dei propri sistemi per rilevare e rispondere alle minacce ai servizi online Microsoft. I principi chiave per il monitoraggio e l'avviso di sicurezza sono:

- Robustezza: segnali e logica per rilevare vari comportamenti di attacco
- Accuratezza: avvisi significativi per evitare distrazioni dal rumore
- Velocità: capacità di intercettare gli utenti malintenzionati abbastanza velocemente da arrestarli

Le soluzioni basate su automazione, scalabilità e cloud sono fondamentali per la nostra strategia di monitoraggio e risposta. Per evitare in modo efficace attacchi su larga scala di alcuni dei servizi online Microsoft, i sistemi di monitoraggio devono generare automaticamente avvisi estremamente accurati quasi in tempo reale. Allo stesso modo, quando viene rilevato un problema, è necessaria la possibilità di ridurre il rischio su larga scala, non è possibile affidarsi al team per risolvere manualmente i problemi computer per computer. Per ridurre i rischi su larga scala, usiamo strumenti basati sul cloud per applicare automaticamente contromisure e fornire ai tecnici strumenti per applicare rapidamente azioni di mitigazione approvate in tutto l'ambiente.

## <a name="how-do-microsoft-online-services-perform-security-monitoring"></a>In che modo i servizi online Microsoft eseguono il monitoraggio della sicurezza?

I servizi online Microsoft utilizzano la registrazione centralizzata per raccogliere e analizzare gli eventi di registro per le attività che potrebbero indicare un incidente di sicurezza. Gli strumenti di registrazione centralizzata aggregano i log di tutti i componenti di sistema, inclusi i log eventi, i log applicazioni, i log di controllo di accesso e i sistemi di rilevamento delle intrusioni basati sulla rete. Oltre alla registrazione del server e ai dati a livello di applicazione, l'infrastruttura di base è dotata di agenti di sicurezza personalizzati che generano telemetria dettagliata e forniscono il rilevamento delle intrusioni basato sull'host. Questi dati di telemetria vengono usati per il monitoraggio e l'analisi forense.

I dati di registrazione e telemetria raccolti consentono l'avviso di sicurezza 24 ore su 24, 7 giorni su 7. Il sistema di avviso analizza i dati di log durante il caricamento, generando avvisi quasi in tempo reale. Questo include avvisi basati su regole e avvisi più sofisticati basati su modelli di apprendimento automatico. La nostra logica di monitoraggio va oltre gli scenari di attacco generici e integra una conoscenza approfondita dell'architettura e delle operazioni del servizio. Analizziamo i dati di monitoraggio della sicurezza per migliorare continuamente i nostri modelli per rilevare nuovi tipi di attacchi e migliorare l'accuratezza del monitoraggio della sicurezza.

## <a name="how-do-microsoft-online-services-respond-to-security-monitoring-alerts"></a>In che modo i servizi online Microsoft rispondono agli avvisi di monitoraggio della sicurezza?

Quando gli eventi di sicurezza che attivano avvisi richiedono un'azione reattiva o un'ulteriore indagine delle prove forensi in tutto il servizio, i nostri strumenti basati sul cloud consentono una risposta rapida in tutto l'ambiente. Questi strumenti includono agenti intelligenti completamente automatizzati che rispondono alle minacce rilevate con contromisure di sicurezza. In molti casi, questi agenti distribuiscono contromisure automatiche per attenuare i rilevamenti di sicurezza su larga scala senza intervento umano. Quando questa risposta non è possibile, il sistema di monitoraggio della sicurezza avvisa automaticamente i tecnici di chiamata appropriati, dotati di un set di strumenti che consentono loro di agire in tempo reale per ridurre le minacce rilevate su larga scala. I potenziali incidenti vengono inoltrati al team di risposta alla sicurezza Microsoft appropriato e vengono risolti utilizzando il processo di risposta agli incidenti di sicurezza.

## <a name="how-do-microsoft-online-services-monitor-system-availability"></a>In che modo i Servizi online Microsoft monitorano la disponibilità del sistema?

Microsoft monitora attivamente i propri sistemi per gli indicatori di sovra-utilizzo delle risorse e uso anomalo. Il monitoraggio delle risorse è completato da licenzianze dei servizi per evitare tempi di inattività imprevisti e fornire ai clienti un accesso affidabile a prodotti e servizi. I problemi di integrità dei servizi online Microsoft vengono comunicati tempestivamente ai clienti tramite il dashboard di integrità dei servizi (SHD).

I servizi online di Azure e Dynamics 365 utilizzano più servizi di infrastruttura per monitorare la disponibilità di sicurezza e integrità. L'implementazione dei test delle transazioni sintetiche (STX) consente ai servizi di Azure e Dynamics di verificare la disponibilità dei propri servizi. Il framework STX è progettato per supportare il test automatizzato dei componenti nei servizi in esecuzione ed è testato in avvisi di errore del sito in tempo reale. Inoltre, il servizio Azure Security Monitoring (ASM) ha implementato procedure di test sintetici centralizzati per verificare che gli avvisi di sicurezza funzionino come previsto sia nei servizi nuovi che in esecuzione.

## <a name="related-external-regulations--certifications"></a>Normative esterne correlate & certificazioni

I servizi online di Microsoft vengono regolarmente controllati per la conformità alle normative e alle certificazioni esterne. Fare riferimento alla tabella seguente per la convalida dei controlli correlati al monitoraggio della sicurezza.

### <a name="azure-and-dynamics-365"></a>Azure e Dynamics 365

| **Controlli esterni** | **Sezione** | **Data ultimo report** |
|:--------|:--------|:------|
| [ISO 27001/27002](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> <br> [Dichiarazione di applicabilità](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=00af6c3e-7f3e-4e0d-8b0e-79f45ef2cef1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Certificazione](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7af5304-3a31-40e6-9abb-e26352305d41&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.1.3: Monitoraggio della disponibilità e pianificazione della capacità | 2 dicembre 2020 |
| [ISO 27017](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Dichiarazione di applicabilità](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a3bca0ac-867d-4204-b66b-13665f5f1e8d&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Certificazione](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=25718a8a-f34d-41e1-a95a-c49246508787&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.1.3: Monitoraggio della disponibilità e pianificazione della capacità <br> A.16.1: Gestione di incidenti e miglioramenti relativi alla sicurezza delle informazioni | 2 dicembre 2020 |
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b8721ebd-af20-42fe-b22f-8332b0a19517&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | IM-1: Framework di gestione degli eventi imprevisti <br> IM-2: configurazione di rilevamento degli eventi imprevisti <br> IM-3: Procedure di gestione degli eventi imprevisti <br> IM-4: incidente post-mortem <br> VM-1: raccolta e registrazione degli eventi di sicurezza <br> VM-12: monitoraggio della disponibilità dei servizi di Azure <br> VM-4: indagine sugli eventi dannosi <br> VM-6: Monitoraggio delle vulnerabilità della sicurezza | 31 marzo 2021 |
| [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=234a0f57-83c1-4afc-a586-a0e7a59592f7&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 3](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=75c8cbf6-e456-473c-a05e-34fea888ec2a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | IM-1: Framework di gestione degli eventi imprevisti <br> IM-2: configurazione di rilevamento degli eventi imprevisti <br> IM-3: Procedure di gestione degli eventi imprevisti <br> IM-4: incidente post-mortem <br> PI-2: Analisi delle prestazioni del contratto di servizio del portale di Azure <br> VM-1: raccolta e registrazione degli eventi di sicurezza <br> VM-12: monitoraggio della disponibilità dei servizi di Azure <br> VM-4: indagine sugli eventi dannosi <br> VM-6: Monitoraggio delle vulnerabilità della sicurezza | 31 marzo 2021 |

### <a name="office-365"></a>Office 365

| **Controlli esterni** | **Sezione** | **Data ultimo report** |
|:--------|:--------|:------|
| [FedRAMP](https://compliance.microsoft.com/compliancemanager) | AC-2: Gestione account <br> AC-17: Accesso remoto <br> AU-7: Riduzione del controllo e generazione di report <br> SI-4: Monitoraggio del sistema di informazioni <br> SI-7: software, firmware e integrità delle informazioni <br> | 24 settembre 2020 |
| [ISO 27001/27002/27017](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> <br> [Dichiarazione di applicabilità](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Certificazione](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.1.3: Monitoraggio della disponibilità e pianificazione della capacità | 20 aprile 2021 |
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-19: Monitoraggio delle modifiche <br> CA-26: Segnalazione degli incidenti di sicurezza <br> CA-29: Tecnici a chiamata <br> CA-48: Registrazione datacenter | 24 dicembre 2020 |
| [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-19: Monitoraggio delle modifiche <br> CA-26: Segnalazione degli incidenti di sicurezza <br> CA-29: Tecnici a chiamata <br> CA-30: Monitoraggio della disponibilità <br> CA-48: Registrazione datacenter | 24 dicembre 2020 |
| [SOC 3](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=274054e5-4968-48d2-bf94-9a8eda5d7a93&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CUEC-08: segnalazione di eventi imprevisti <br> CUEC-10: contratti di servizio | 24 dicembre 2020 |

## <a name="resources"></a>Risorse

- [Dietro le quinte: proteggere l'infrastruttura potenziando il servizio Microsoft 365](https://download.microsoft.com/download/c/4/5/c45b197e-f0d9-4f40-bd5f-ed8fc7d0cd8c/M365DCSecurityIntro_Whitepaper.pdf)
