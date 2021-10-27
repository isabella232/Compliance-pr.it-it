---
title: Panoramica sulla gestione degli incidenti
description: Informazioni sulla gestione degli incidenti in Microsoft 365
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
ms.openlocfilehash: 959d9c7b3a483ff71d43c325def048c8aaffff3a
ms.sourcegitcommit: 1f30616328d7deb04e41dcbd44a330ea937fe94f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/26/2021
ms.locfileid: "60582619"
---
# <a name="incident-management-overview"></a>Panoramica sulla gestione degli incidenti

## <a name="what-is-a-security-incident"></a>Cos'è un incidente della sicurezza?

Microsoft definisce un incidente della sicurezza all'interno dei suoi servizi online come una violazione confermata della sicurezza che causa la distruzione accidentale o illecita, la perdita, l'alterazione, la divulgazione non autorizzata o l'accesso ai dati personali o ai dati personali dei clienti durante l'elaborazione da parte di Microsoft. Ad esempio, l'accesso non autorizzato all'infrastruttura dei servizi online Microsoft e l'esfiltrazione dei dati dei clienti costituirebbero un incidente di sicurezza, mentre gli eventi di conformità che non influiscono sulla riservatezza, l'integrità o la disponibilità dei servizi o dei dati dei clienti non sono considerati incidenti di sicurezza.

## <a name="how-does-microsoft-respond-to-security-incidents"></a>In che modo Microsoft risponde agli incidenti di sicurezza?

Ogni volta che si verifica un incidente di sicurezza, Microsoft si impegna a rispondere in modo rapido ed efficace per proteggere servizi Microsoft e i dati dei clienti. Microsoft utilizza una strategia di risposta agli incidenti progettata per analizzare, contenere e rimuovere le minacce alla sicurezza in modo rapido ed efficiente.

I servizi cloud Microsoft vengono costantemente monitorati per i segni di compromissione. Oltre al monitoraggio e all'avviso di sicurezza automatizzati, tutti i dipendenti ricevono una formazione annuale per riconoscere e segnalare i segni di potenziali incidenti di sicurezza. Tutte le attività sospette rilevate da dipendenti, clienti o strumenti di monitoraggio della sicurezza vengono inoltrate ai team di Security Response specifici del servizio per l'indagine. Tutti i team delle operazioni di servizio, inclusi i team di Security Response specifici del servizio, mantengono una rotazione approfondita delle chiamate per garantire la disponibilità di risorse per la risposta agli incidenti 24x7x365. Le rotazioni di chiamata consentono a Microsoft di montare una risposta efficace agli incidenti in qualsiasi momento o scala, inclusi eventi diffusi o simultanei.

Quando vengono rilevate e riassegnate attività sospette, i team di Security Response specifici del servizio avviano un processo di **analisi, contenimento, eliminazione e ripristino.** Questi team coordinano l'analisi del potenziale incidente per determinarne l'ambito, incluso qualsiasi impatto sui clienti o sui dati dei clienti. In base a questa analisi, i team di Security Response specifici del servizio lavorano con i team del servizio che hanno un impatto per sviluppare un piano per contenere la minaccia e ridurre al minimo l'impatto dell'incidente, eliminare la minaccia dall'ambiente e ripristinare completamente uno stato sicuro noto. I team di servizi pertinenti implementano il piano con il supporto dei team di Security Response specifici del servizio per garantire che la minaccia sia eliminata e che i servizi influenzati siano sottoposti a un ripristino completo.

Dopo la risoluzione di un evento imprevisto, i team di servizio implementano tutte le lezioni apprese dall'incidente per prevenire, rilevare e rispondere a eventi imprevisti simili in futuro. Selezionare gli incidenti di sicurezza, in particolare quelli che influiscono sul cliente o che causano una violazione dei dati, subiscono un incidente completo post-mortem. La valutazione finale è progettata per identificare errori tecnici, errori procedurali, errori manuali e altri difetti di processo che potrebbero aver contribuito all'incidente o che sono stati identificati durante il processo di risposta all'incidente. I miglioramenti identificati durante la post-mortem vengono implementati con il coordinamento dei team di Security Response specifici del servizio per evitare incidenti futuri e migliorare le funzionalità di rilevamento e risposta.

## <a name="how-and-when-are-customers-notified-of-security-or-privacy-incidents"></a>In che modo e quando i clienti vengono informati di incidenti di sicurezza o privacy?

Ogni volta che Microsoft viene a conoscenza di una violazione della sicurezza che implica la perdita, la divulgazione o la modifica non autorizzata dei dati dei clienti, Microsoft informa i clienti interessati entro 72 ore, come descritto nel Data Protection Addendum (DPA) delle Condizioni per i servizi online (OST). L'impegno relativo alla sequenza temporale delle notifiche inizia quando si verifica la dichiarazione ufficiale dell'incidente di sicurezza. Quando si dichiara un incidente di sicurezza, il processo di notifica viene eseguito il più rapidamente possibile, senza indebiti ritardi.

Le notifiche includono una descrizione della natura della violazione, l'impatto approssimativo degli utenti e i passaggi di mitigazione (se applicabile). Se l'indagine di Microsoft non viene completata al momento della notifica iniziale, la notifica indicherà anche i passaggi e le tempistiche successivi per le comunicazioni successive.

Se un cliente viene a conoscenza di un evento imprevisto che potrebbe avere un impatto su Microsoft, anche se non limitato a una violazione dei dati, il cliente è responsabile di informare tempestivamente Microsoft dell'incidente come definito nel DPA.

## <a name="related-external-regulations--certifications"></a>Normative esterne correlate & certificazioni

I servizi online di Microsoft vengono regolarmente controllati per la conformità alle normative e alle certificazioni esterne. Fare riferimento alla tabella seguente per la convalida dei controlli correlati alla gestione degli eventi imprevisti.

### <a name="azure-and-dynamics-365"></a>Azure e Dynamics 365

| **Controlli esterni** | **Sezione** | **Data ultimo report** |
|:--------------------|:------------|:-----------------------|
| [ISO 27001/27002](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Dichiarazione di applicabilità](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=00af6c3e-7f3e-4e0d-8b0e-79f45ef2cef1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Certificazione](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7af5304-3a31-40e6-9abb-e26352305d41&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.16.1: Gestione di incidenti e miglioramenti relativi alla sicurezza delle informazioni | 2 dicembre 2021 |
| [ISO 27017](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Dichiarazione di applicabilità](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a3bca0ac-867d-4204-b66b-13665f5f1e8d&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Certificazione](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=25718a8a-f34d-41e1-a95a-c49246508787&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.16.1: Gestione di incidenti e miglioramenti relativi alla sicurezza delle informazioni | 2 dicembre 2021 |
| [ISO 27018](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Dichiarazione di applicabilità](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=00af6c3e-7f3e-4e0d-8b0e-79f45ef2cef1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Certificazione](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=56904fc3-0942-4ff5-9eef-7cabc751a25c&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.9.1: Notifica di una violazione dei dati relativa alle informazioni personali  | 2 dicembre 2021 |
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b8721ebd-af20-42fe-b22f-8332b0a19517&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | IM-1: Framework di gestione degli eventi imprevisti <br> IM-2: meccanismi di rilevamento e avvisi <br> IM-3: Esecuzione della risposta a eventi imprevisti <br> IM-4: post-mortem degli incidenti <br> IM-6: test di risposta a eventi imprevisti <br> OA-7: accesso tecnico a chiamata | 31 marzo 2021 |
| [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=234a0f57-83c1-4afc-a586-a0e7a59592f7&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 3](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=75c8cbf6-e456-473c-a05e-34fea888ec2a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CCM-9: procedure forensi <br> CUEC: segnalazione di eventi imprevisti <br> IM-1: Framework di gestione degli eventi imprevisti <br> IM-2: meccanismi di rilevamento e avvisi <br> IM-3: Esecuzione della risposta a eventi imprevisti <br> IM-4: post-mortem degli incidenti <br> IM-6: test di risposta a eventi imprevisti <br> OA-7: accesso tecnico a chiamata <br> SOC2-6: sito Web del Supporto tecnico clienti <br> SOC2-9: dashboard di servizio | 31 marzo 2021 |

### <a name="office-365"></a>Office 365

| **Controlli esterni** | **Sezione** | **Data ultimo report** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP](https://compliance.microsoft.com/compliancemanager) | IR-4: gestione degli eventi imprevisti <br> IR-6: segnalazione degli eventi imprevisti <br> IR-8: piano di risposta agli incidenti | 24 settembre 2020 |
| [ISO 27001/27002/27017](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Dichiarazione di applicabilità](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Certificazione](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.16.1: Gestione di incidenti e miglioramenti relativi alla sicurezza delle informazioni | 20 aprile 2021 |
| [ISO 27018](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Dichiarazione di applicabilità](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Certificazione](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=43e89534-f48d-42ea-a7a7-3523ff516036&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports)  | A.10.1: Notifica di una violazione dei dati relativa alle informazioni personali  | 20 aprile 2021 |
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-26: Segnalazione degli incidenti di sicurezza <br> CA-47: Risposta agli eventi imprevisti | 24 dicembre 2020 |
| [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-12: Contratti di servizio <br> CA-13: Guide per la risposta a eventi imprevisti <br> CA-15: Notifiche di integrità dei servizi  <br>  <br> CA-26: Segnalazione degli incidenti di sicurezza <br> CA-29: Tecnici a chiamata <br> CA-47: Risposta agli eventi imprevisti | 24 dicembre 2020 |
| [SOC 3](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=274054e5-4968-48d2-bf94-9a8eda5d7a93&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CUEC-08: segnalazione di eventi imprevisti  | 24 dicembre 2020  |

## <a name="resources"></a>Risorse

- [Condizioni per l'Utilizzo dei Servizi Online](https://www.microsoft.com/licensing/product-licensing/products)
- [Data Protection Addendum (DPA)](https://www.microsoft.com/licensing/product-licensing/products)
- [Guida all'implementazione di Microsoft Cloud Incident Management per Azure e Office 365](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=a8a7cb87-9710-4d09-8748-0835b6754e95&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_FAQ_and_White_Papers)
- [Office 365 - Valutazione della vulnerabilità di terze parti Office 365 - 2019](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=e85e478f-2491-435d-9c1b-2f0ad7ca8e56&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_Pen_Test_and_Security_Assessments)
