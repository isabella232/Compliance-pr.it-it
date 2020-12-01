---
title: Panoramica del monitoraggio della sicurezza
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
ms.openlocfilehash: f3eae0aa5ba79372a7ce0d9a34d4dd35fe83a36b
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/30/2020
ms.locfileid: "49508847"
---
# <a name="security-monitoring-overview"></a>Panoramica del monitoraggio della sicurezza

## <a name="what-is-microsofts-strategy-for-monitoring-security"></a>Che cos'è la strategia di Microsoft per il monitoraggio della sicurezza?

Microsoft 365 si avvale del monitoraggio della sicurezza continua dei sistemi per rilevare e rispondere alle minacce ai servizi di Microsoft 365. I principi fondamentali per il monitoraggio della sicurezza e gli avvisi sono i seguenti:

- Robustezza: segnali e logica per rilevare una serie di comportamenti di attacco
- Accuratezza: avvisi significativi per evitare distrazioni dal rumore
- Velocità: possibilità di intercettare gli aggressori in modo che siano in grado di fermarli

Le soluzioni di automazione, scala e cloud sono pilastri fondamentali della strategia di monitoraggio e di risposta. Per poter rilevare e arrestare efficacemente gli attacchi alla scalabilità di alcuni dei servizi di base di Microsoft 365, i sistemi di monitoraggio devono generare automaticamente avvisi estremamente accurati in tempo quasi reale. Analogamente, quando viene rilevato un problema, è necessaria la possibilità di attenuare il rischio in scala, non è possibile fare affidamento sul nostro team per risolvere manualmente i problemi di computer per computer. Per attenuare i rischi in scala, è possibile utilizzare gli strumenti basati sul cloud per applicare automaticamente le contromisure e fornire agli ingegneri gli strumenti per applicare rapidamente le attenuazioni approvate nell'ambiente.

## <a name="how-does-microsoft-365-perform-security-monitoring"></a>In che modo Microsoft 365 esegue il monitoraggio della sicurezza?

Microsoft 365 utilizza la registrazione centralizzata per raccogliere e analizzare gli eventi dei registri per attività che potrebbero indicare un problema di sicurezza. Gli strumenti di registrazione centralizzati vengono aggregati da tutti i componenti di sistema, inclusi i registri eventi, i registri applicazioni, i registri di controllo di accesso e i sistemi di rilevamento delle intrusioni basati sulla rete. Oltre alla registrazione dei server e ai dati a livello di applicazione, l'infrastruttura di base del servizio è equipaggiata con agenti di sicurezza personalizzati che generano una telemetria dettagliata e forniscono il rilevamento delle intrusioni basato sull'host. Usiamo questa telemetria per il monitoraggio e la scientifica.

I dati di registrazione e di telemetria raccolti consentono di 24/7 avvisi di sicurezza. Il sistema di avviso analizza i dati del log Man mano che vengono caricati, producendo avvisi in tempo quasi reale. Sono inclusi gli avvisi basati sulle regole e l'avviso più sofisticato basato sui modelli di apprendimento automatico. La logica di monitoraggio supera gli scenari di attacco generici e incorpora una profonda consapevolezza dell'architettura e delle operazioni del servizio. Vengono utilizzati i dati di monitoraggio della sicurezza per migliorare continuamente i modelli per individuare nuovi tipi di attacchi e migliorare l'accuratezza del monitoraggio della sicurezza.

## <a name="how-does-microsoft-365-respond-to-security-monitoring-alerts"></a>In che modo Microsoft 365 risponde agli avvisi per il monitoraggio della sicurezza?

Quando è necessario intraprendere un'azione in risposta a un avviso o per esaminare ulteriormente le evidenze forensi in tutto il servizio, gli strumenti basati sul cloud consentono di rispondere rapidamente in tutto l'ambiente. Questi strumenti includono agenti intelligenti completamente automatizzati che rispondono a minacce rilevate con contromisure di sicurezza. In molti casi, questi agenti distribuiscono contromisure automatiche per attenuare i rilevamenti di sicurezza in scala senza l'intervento dell'uomo. Quando ciò non è possibile, il sistema di monitoraggio della sicurezza avvisa automaticamente gli ingegneri di chiamata corretti, che dispongono di un insieme di strumenti che consentono loro di agire in tempo reale per attenuare le minacce rilevate in scala. I potenziali incidenti escalati nel team di risposta alla sicurezza di Microsoft 365 vengono risolti utilizzando il processo di risposta agli incidenti di sicurezza.

## <a name="how-does-microsoft-365-monitor-system-availability"></a>In che modo Microsoft 365 monitora la disponibilità del sistema?

Microsoft 365 monitora attivamente i propri sistemi per gli indicatori relativi all'utilizzo eccessivo delle risorse e all'uso anormale. Il monitoraggio delle risorse è completato da ridondanze del servizio per evitare tempi di inattività imprevisti e fornire ai clienti un accesso affidabile a prodotti e servizi. I problemi di integrità dei servizi vengono comunicati tempestivamente ai clienti tramite il dashboard Health Service (SHD).

## <a name="related-external-regulations--certifications"></a>Normative esterne correlate & certificazioni

I servizi online di Microsoft vengono controllati regolarmente per la conformità con le certificazioni e le normative esterne. Per la convalida dei controlli relativi al monitoraggio della sicurezza, vedere la tabella seguente.

| **Verifiche esterne** | **Sezione** | **Data ultimo rapporto** |
|:--------|:--------|:------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | AC-2: gestione account <br> AC-17: accesso remoto <br> AU-7: riduzione dei controlli e generazione dei report <br> SI-4: monitoraggio del sistema informativo <br> SI-7: software, firmware e integrità delle informazioni <br> | 24 settembre 2020 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> <br> [Dichiarazione di applicabilità](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certificazione](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A. 12.1.3: monitoraggio della disponibilità e pianificazione della capacità | 22 febbraio 2020 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Dichiarazione di applicabilità](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certificazione](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A. 12.1.3: monitoraggio della disponibilità e pianificazione della capacità <br> A. 16.1: gestione degli incidenti e dei miglioramenti della sicurezza delle informazioni | 22 febbraio 2020 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b07c0f7b-6bd5-4544-8255-7a5f14bf914a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-19: modifica del monitoraggio <br> CA-26: segnalazione degli incidenti di sicurezza <br> CA-29: ingegneri di chiamata <br> CA-48: registrazione del datacenter | 30 settembre 2019 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=fa062990-e758-4ddc-ace3-7fb21a301d09&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Rep-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-19: modifica del monitoraggio <br> CA-26: segnalazione degli incidenti di sicurezza <br> CA-29: ingegneri di chiamata <br> CA-30: monitoraggio della disponibilità <br> CA-48: registrazione del datacenter | 30 settembre 2019 |
| [SOC 3 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=9df8b99b-96ce-49a9-bff4-268031dcc9a6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CUEC-08: segnalare gli eventi non consentiti <br> CUEC-10: contratti di servizio | 30 settembre 2019 |

## <a name="resources"></a>Risorse

- [Dietro le quinte: protezione dell'infrastruttura che alimenta il servizio Microsoft 365](https://download.microsoft.com/download/c/4/5/c45b197e-f0d9-4f40-bd5f-ed8fc7d0cd8c/M365DCSecurityIntro_Whitepaper.pdf)
