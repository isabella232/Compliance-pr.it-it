---
title: Panoramica sulla gestione degli incidenti
description: Informazioni sulla gestione delle operazioni non consentite in Microsoft 365
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
ms.openlocfilehash: 24ecad99115705f293f765edb84345dad8ff8c93
ms.sourcegitcommit: 7a5b6bc58fc4613b38f3fda20aebee5cec6a5730
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "49787315"
---
# <a name="incident-management-overview"></a>Panoramica sulla gestione degli incidenti

## <a name="what-is-a-security-incident"></a>Che cos'è un evento di sicurezza?

Microsoft definisce un incidente di sicurezza nei suoi servizi online come una confermata violazione della sicurezza che porta alla distruzione accidentale, alla perdita, all'alterazione, alla divulgazione non autorizzata o all'accesso ai dati dei clienti o ai dati personali mentre è in corso l'elaborazione da parte di Microsoft. Ad esempio, l'accesso non autorizzato all'infrastruttura di Microsoft 365 e exfiltration di dati dei clienti costituirebbe un problema di sicurezza, mentre gli eventi di conformità che non influiscono sulla riservatezza, l'integrità o la disponibilità dei servizi o i dati dei clienti non sono considerati incidenti di sicurezza.

## <a name="how-does-microsoft-respond-to-security-incidents"></a>In che modo Microsoft risponde agli incidenti di sicurezza?

Ogni volta che si verifica un problema di sicurezza, Microsoft si sforza di rispondere rapidamente ed efficacemente ai servizi Microsoft e ai dati dei clienti. Microsoft impiega una strategia di risposta agli incidenti progettata per esaminare, contenere e rimuovere le minacce alla sicurezza in modo rapido ed efficiente.

I servizi cloud Microsoft vengono continuamente monitorati per i segni di compromesso. Oltre al monitoraggio e all'avviso di sicurezza automatizzati, tutti i dipendenti ricevono una formazione annuale per riconoscere e segnalare i segni di potenziali incidenti di sicurezza. Qualsiasi attività sospetta rilevata da dipendenti, clienti o strumenti di monitoraggio della sicurezza viene inoltrata ai team di risposta di sicurezza specifici del servizio per l'analisi. Tutti i team delle operazioni di servizio, inclusi i team di risposta alla sicurezza specifici del servizio, gestiscono una rotazione profonda delle chiamate per garantire che le risorse siano disponibili per i 24x7x365 di risposta sugli incidenti. Le rotazioni di chiamata consentono a Microsoft di installare una risposta di emergenza efficace in qualsiasi momento o scala, compresi gli eventi diffusi o simultanei.

Quando l'attività sospetta viene rilevata e inoltrata, i team di risposta di sicurezza specifici del servizio avviano un processo di **analisi, contenimento, eliminazione e ripristino**. Queste squadre coordinano l'analisi del potenziale incidente per determinarne l'ambito, incluso qualsiasi impatto per i clienti o i dati dei clienti. In base a questa analisi, i team di risposta di sicurezza specifici del servizio interagiscono con i team di servizi interessati per sviluppare un piano per contenere la minaccia e ridurre al minimo l'impatto dell'evento, eliminare la minaccia dall'ambiente e recuperare completamente lo stato di sicurezza conosciuto. I team di servizio rilevanti implementano il piano con il supporto di team di risposta alla sicurezza specifici del servizio per garantire che la minaccia venga eliminata correttamente e che i servizi interessati vengano sottoposti a un ripristino completo.

Dopo che è stato risolto un problema, i team di servizio hanno implementato qualsiasi lezione appresa dall'incidente per prevenire, rilevare e rispondere a incidenti simili in futuro. Selezionare incidenti di sicurezza, in particolare quelli con impatto sul cliente o provocare una violazione dei dati, sottoporsi a un evento post-mortem completo. La post-mortem è progettata per identificare le interruzioni tecniche, i problemi procedurali, gli errori manuali e gli altri difetti del processo che potrebbero aver contribuito all'incidente o che sono stati identificati durante il processo di risposta agli incidenti. I miglioramenti identificati durante l'autopsia vengono implementati con il coordinamento dei team di risposta alla sicurezza specifici del servizio per evitare incidenti futuri e migliorare le funzionalità di rilevamento e risposta.

## <a name="how-and-when-are-customers-notified-of-security-or-privacy-incidents"></a>Come e quando i clienti sono informati degli incidenti di sicurezza o di privacy?

Ogni volta che Microsoft viene a conoscenza di una violazione della sicurezza relativa a perdita, divulgazione o modifica non autorizzata dei dati del cliente, Microsoft notifica ai clienti interessati entro 72 ore come indicato nell'addendum sulla protezione dei dati (DPA) delle condizioni per i servizi online (OST). L'impegno della sequenza temporale di notifica inizia quando si verifica la dichiarazione di incidenti di sicurezza ufficiale. Al momento della dichiarazione di un incidente di sicurezza, il processo di notifica viene eseguito il più rapidamente possibile, senza indebiti ritardi.

Le notifiche includono una descrizione della natura della violazione, l'impatto approssimativo dell'utente e i passaggi di attenuazione (se applicabile). Se l'indagine di Microsoft non è completa al momento della notifica iniziale, la notifica indicherà anche i passaggi successivi e le sequenze temporali per la comunicazione successiva.

Se un cliente viene a conoscenza di un incidente che potrebbe avere un impatto su Microsoft, incluso ma non limitato a una violazione dei dati, il cliente è responsabile della notifica tempestiva a Microsoft dell'incidente, come definito in DPA.

## <a name="related-external-regulations--certifications"></a>Normative esterne correlate & certificazioni

I servizi online di Microsoft vengono controllati regolarmente per la conformità con le certificazioni e le normative esterne. Fare riferimento alla tabella seguente per la convalida dei controlli relativi alla gestione degli eventi non consentiti.

| **Verifiche esterne** | **Sezione** | **Data ultimo rapporto** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | IR-4: gestione degli incidenti <br> IR-6: relazioni sugli incidenti <br> IR-8: piano di risposta degli incidenti | 24 settembre 2020 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Dichiarazione di applicabilità](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certificazione](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A. 16.1: gestione degli incidenti e dei miglioramenti della sicurezza delle informazioni | 22 febbraio 2020 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Dichiarazione di applicabilità](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certificazione](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A. 16.1: gestione degli incidenti e dei miglioramenti della sicurezza delle informazioni | 22 febbraio 2020 |
| [ISO 27018 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Dichiarazione di applicabilità](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certificazione](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=43e89534-f48d-42ea-a7a7-3523ff516036&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A. 10.1: notifica di una violazione dei dati che coinvolge le informazioni personali  | 22 febbraio 2020 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-26: segnalazione degli incidenti di sicurezza <br> CA-47: risposta agli incidenti | 24 dicembre 2020 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-12: contratti di servizio (SLA) <br> CA-13: Guide alle risposte sugli incidenti <br> CA-15: notifiche di integrità del servizio  <br>  <br> CA-26: segnalazione degli incidenti di sicurezza <br> CA-29: ingegneri di chiamata <br> CA-47: risposta agli incidenti | 24 dicembre 2020 |
| [SOC 3 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=274054e5-4968-48d2-bf94-9a8eda5d7a93&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CUEC-08: segnalare gli eventi non consentiti  | 24 dicembre 2020  |

## <a name="resources"></a>Risorse

- [Condizioni dei servizi online (OST)](https://www.microsoft.com/licensing/product-licensing/products)
- [Addendum sulla protezione dei dati (DPA)](https://www.microsoft.com/licensing/product-licensing/products)
- [Guida all'implementazione di Microsoft Cloud Incident Management per Azure e Office 365](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=a8a7cb87-9710-4d09-8748-0835b6754e95&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_FAQ_and_White_Papers)
- [Office 365-valutazione della vulnerabilità di terze parti di Office 365-2019](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=e85e478f-2491-435d-9c1b-2f0ad7ca8e56&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_Pen_Test_and_Security_Assessments)
