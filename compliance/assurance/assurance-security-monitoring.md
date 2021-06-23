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
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MET150
- MOE150
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 2019289542a49f6f586d22da8907eb5c7143e329
ms.sourcegitcommit: fb379d1110a9a86c7f9bab8c484dc3f4b3dfd6f0
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/23/2021
ms.locfileid: "53088875"
---
# <a name="security-monitoring-overview"></a>Panoramica sul monitoraggio della sicurezza

## <a name="what-is-microsofts-strategy-for-monitoring-security"></a>Qual è la strategia di Microsoft per il monitoraggio della sicurezza?

Microsoft 365 si impegna a monitorare la sicurezza continua dei propri sistemi per rilevare e rispondere alle minacce Microsoft 365 Services. I principi chiave per il monitoraggio e l'avviso di sicurezza sono:

- Robustezza: segnali e logica per rilevare una varietà di comportamenti di attacco
- Accuratezza: avvisi significativi per evitare distrazioni dal rumore
- Velocità: capacità di intercettare gli utenti malintenzionati abbastanza velocemente da arrestarli

L'automazione, la scalabilità e le soluzioni basate sul cloud sono i pilastri chiave della nostra strategia di monitoraggio e risposta. Per intercettare e arrestare in modo efficace gli attacchi sulla scala di alcuni dei servizi di base di Microsoft 365, i sistemi di monitoraggio devono generare automaticamente avvisi estremamente accurati quasi in tempo reale. Allo stesso modo, quando viene rilevato un problema, è necessaria la possibilità di ridurre il rischio su larga scala, non è possibile affidarsi al team per risolvere manualmente i problemi computer per computer. Per ridurre i rischi su larga scala, usiamo strumenti basati sul cloud per applicare automaticamente contromisure e fornire ai tecnici strumenti per applicare rapidamente le mitigazioni approvate in tutto l'ambiente.

## <a name="how-does-microsoft-365-perform-security-monitoring"></a>In che modo Microsoft 365 il monitoraggio della sicurezza?

Microsoft 365 utilizza la registrazione centralizzata per raccogliere e analizzare gli eventi del registro per le attività che potrebbero indicare un incidente di sicurezza. Gli strumenti di registrazione centralizzata aggregano i registri di tutti i componenti di sistema, inclusi i registri eventi, i registri applicazioni, i registri di controllo di accesso e i sistemi di rilevamento delle intrusioni basati sulla rete. Oltre alla registrazione del server e ai dati a livello di applicazione, l'infrastruttura di base del servizio è dotata di agenti di sicurezza personalizzati che generano telemetria dettagliata e forniscono il rilevamento delle intrusioni basato sull'host. Usiamo questa telemetria per il monitoraggio e la ricerca forense.

I dati di registrazione e telemetria raccolti consentono l'avviso di sicurezza 24 ore su 24, 7 giorni su 7. Il sistema di avvisi analizza i dati del registro durante il caricamento, generando avvisi quasi in tempo reale. Sono inclusi avvisi basati su regole e avvisi più sofisticati basati su modelli di machine learning. La logica di monitoraggio va oltre gli scenari di attacco generici e incorpora una conoscenza approfondita dell'architettura e delle operazioni del servizio. Usiamo i dati di monitoraggio della sicurezza per migliorare continuamente i nostri modelli per rilevare nuovi tipi di attacchi e migliorare l'accuratezza del monitoraggio della sicurezza.

## <a name="how-does-microsoft-365-respond-to-security-monitoring-alerts"></a>In che modo Microsoft 365 gli avvisi di monitoraggio della sicurezza?

Quando è necessario intraprendere un'azione in risposta a un avviso o per analizzare ulteriormente le prove forensi in tutto il servizio, i nostri strumenti basati sul cloud ci consentono di rispondere rapidamente in tutto l'ambiente. Questi strumenti includono agenti intelligenti completamente automatizzati che rispondono alle minacce rilevate con contromisure di sicurezza. In molti casi, questi agenti distribuiscono contromisure automatiche per ridurre i rilevamenti di sicurezza su larga scala senza intervento umano. Quando ciò non è possibile, il sistema di monitoraggio della sicurezza avvisa automaticamente i tecnici di chiamata appropriati, dotati di un set di strumenti che consentono loro di agire in tempo reale per ridurre le minacce rilevate su larga scala. I potenziali eventi imprevisti inoltrati al team Microsoft 365 security response vengono risolti utilizzando il processo di risposta agli incidenti di sicurezza.

## <a name="how-does-microsoft-365-monitor-system-availability"></a>In che modo Microsoft 365 la disponibilità del sistema?

Microsoft 365 monitora attivamente i propri sistemi per gli indicatori di sovra-utilizzo delle risorse e uso anomalo. Il monitoraggio delle risorse è completato da licenzianze dei servizi per evitare tempi di inattività imprevisti e fornire ai clienti un accesso affidabile a prodotti e servizi. I problemi di integrità del servizio vengono comunicati tempestivamente ai clienti tramite il dashboard di integrità del servizio (SHD).

## <a name="related-external-regulations--certifications"></a>Normative esterne correlate & certificazioni

I servizi online di Microsoft vengono regolarmente controllati per la conformità alle normative e alle certificazioni esterne. Fare riferimento alla tabella seguente per la convalida dei controlli correlati al monitoraggio della sicurezza.

| **Controlli esterni** | **Sezione** | **Data ultimo report** |
|:--------|:--------|:------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | AC-2: Gestione account <br> AC-17: Accesso remoto <br> AU-7: Riduzione del controllo e generazione di report <br> SI-4: Monitoraggio del sistema di informazioni <br> SI-7: software, firmware e integrità delle informazioni <br> | 24 settembre 2020 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> <br> [Dichiarazione di applicabilità](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Certificazione](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.1.3: Monitoraggio della disponibilità e pianificazione della capacità | 20 aprile 2021 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Dichiarazione di applicabilità](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Certificazione](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.1.3: Monitoraggio della disponibilità e pianificazione della capacità <br> A.16.1: Gestione di incidenti e miglioramenti relativi alla sicurezza delle informazioni | 20 aprile 2021 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-19: Monitoraggio delle modifiche <br> CA-26: Segnalazione degli incidenti di sicurezza <br> CA-29: Tecnici a chiamata <br> CA-48: Registrazione datacenter | 24 dicembre 2020 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-19: Monitoraggio delle modifiche <br> CA-26: Segnalazione degli incidenti di sicurezza <br> CA-29: Tecnici a chiamata <br> CA-30: Monitoraggio della disponibilità <br> CA-48: Registrazione datacenter | 24 dicembre 2020 |
| [SOC 3 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=274054e5-4968-48d2-bf94-9a8eda5d7a93&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CUEC-08: segnalazione di eventi imprevisti <br> CUEC-10: contratti di servizio | 24 dicembre 2020 |

## <a name="resources"></a>Risorse

- [Behind the Scenes: Securing the Infrastructure Powering the Microsoft 365 Service](https://download.microsoft.com/download/c/4/5/c45b197e-f0d9-4f40-bd5f-ed8fc7d0cd8c/M365DCSecurityIntro_Whitepaper.pdf)
