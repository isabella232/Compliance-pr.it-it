---
title: Resilienza e continuità
description: Informazioni su resilienza e continuità in Microsoft 365
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
ms.openlocfilehash: 0201ad28f25af78ec69f99725e12118dc205b338
ms.sourcegitcommit: 07578a8e03b931f47c49f4e34b78cf8ba0605e8f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/23/2021
ms.locfileid: "53573804"
---
# <a name="resiliency-and-continuity-overview"></a>Panoramica sulla resilienza e sulla continuità

## <a name="how-does-microsoft-ensure-business-continuity-in-the-case-of-a-disaster-or-other-threat-to-service-availability"></a>In che modo Microsoft garantisce la continuità aziendale in caso di emergenza o di altre minacce alla disponibilità del servizio?

Il team di Microsoft Enterprise Business Continuity Management (EBCM) supervisiona le attività di gestione della continuità aziendale e ripristino di emergenza servizi Microsoft e cloud. I rappresentanti delle unità aziendali Microsoft, ad esempio Microsoft 365, si coordinano con il team EBCM per sviluppare piani di continuità aziendale e convalidare la conformità ai requisiti di continuità aziendale.

Il fulcro della metodologia BCM (Business Continuity Management) è il ciclo di vita di BCM. Questo processo in tre fasi è progettato per essere adattabile in modo che possa essere implementato da un'ampia gamma di modelli aziendali in Microsoft. Inizia con una fase **di** valutazione per identificare i processi e gli obiettivi critici che devono essere inclusi nel programma di continuità aziendale. La fase di valutazione richiede anche un'analisi dell'impatto aziendale (BIA). La **fase di** pianificazione è incentrata sullo sviluppo e sull'implementazione di strategie di resilienza e ripristino, oltre a documentarle nei piani ufficiali di continuità aziendale. Infine, **Capability Validation** testa i piani di continuità aziendale e le relative implementazioni per verificare l'efficacia e identificare i potenziali miglioramenti.

Microsoft 365 strategia di continuità aziendale di Microsoft 365 sfrutta la ridondanza hardware, di rete e del datacenter. La replica dei dati tra datacenter offre disponibilità e affidabilità elevate in caso di incidente catastrofico. Aumenta inoltre la resilienza a eventi imprevisti banali, ad esempio errori hardware isolati o danneggiamento dei dati.

## <a name="how-does-microsoft-test-business-continuity-and-disaster-recovery-plans"></a>In che modo Microsoft testa la continuità aziendale e i piani di ripristino di emergenza?

Il criterio Enterprise EBCM (Business Continuity Management) di Microsoft prevede che tutti i piani di continuità aziendale e ripristino di emergenza Di Microsoft devono essere testati, aggiornati e esaminati su base annuale. Microsoft 365 i propri piani di continuità aziendale vengono testati almeno ogni anno in base ai criteri EBCM. Dopo aver creato e esaminato i report azione per convalidare, testare i risultati e informare gli aggiornamenti del piano in risposta a eventuali problemi rilevati durante il test.

Per convalidare le strategie di resilienza e ripristino in base a un'ampia gamma di potenziali incidenti, il programma EBCM definisce più categorie di scenari di test che interessano persone, posizioni e tecnologia. Il livello di convalida richiesto per ogni servizio si basa sulla criticità del servizio, con servizi più critici che ricevono una convalida più rigorosa. Ogni Microsoft 365 del servizio verifica il piano di continuità aziendale in base alle linee guida EBCM per misurare l'efficacia del piano e la disponibilità del team del servizio ad eseguire il piano.

In base alle linee guida EBCM, le revisioni annuali dei piani di continuità aziendale e della convalida delle funzionalità devono avere luogo entro 12 mesi dall'ultima revisione. La convalida delle funzionalità deve includere la revisione della documentazione di supporto, ad esempio il BIA, per garantire che rimanga accurata. Microsoft rende disponibili ai clienti i risultati della convalida delle funzionalità per Microsoft 365 servizi selezionati tramite report trimestrali.

## <a name="how-does-microsoft-365-ensure-system-capacity-meets-demand"></a>In che modo Microsoft 365 garantire che la capacità del sistema soddisfi la domanda?

La pianificazione della capacità consente ai team di servizio di allocare le risorse necessarie per supportare la disponibilità Microsoft 365 servizio. La pianificazione regolare della capacità è necessaria nell'ambito del programma EBCM di Microsoft. I team di servizio esaminano i dati sulla capacità durante le revisioni trimestrali, nonché durante le situazioni di emergenza che giustificano un'ulteriore revisione della capacità.

I dati non elaborati per la pianificazione della capacità vengono gestiti da ogni team del servizio e includono metriche come l'elaborazione del sistema, la memoria e la capacità hardware. Le revisioni pianificate utilizzano un modello della capacità corrente del sistema e lo testano in base alle esigenze previste in situazioni di emergenza. Se il modello indica lacune di capacità, le modifiche proposte alla capacità del sistema vengono inviate alla direzione del team di servizio per la revisione. Le modifiche approvate vengono incorporate in un nuovo modello prima dell'implementazione da parte dei tecnici del team di servizio.

## <a name="how-does-microsoft-365-maintain-service-availability-during-routine-system-failures"></a>In che modo Microsoft 365 la disponibilità del servizio durante gli errori di sistema di routine?

Microsoft 365 la resilienza del servizio attraverso l'architettura ridondante, la replica dei dati e il controllo automatico dell'integrità. L'architettura ridondante prevede la distribuzione di più istanze di un servizio in hardware geograficamente e fisicamente separati, offrendo una maggiore tolleranza di errore per Microsoft 365 servizi. La replica dei dati garantisce che siano sempre presenti più copie dei dati dei clienti in diverse aree di errore, consentendo il ripristino dei dati critici dei clienti in caso di danneggiamento, perdita o persino eliminazione accidentale da parte del cliente. Il controllo automatico dell'integrità aumenta la disponibilità dei dati ripristinando automaticamente i dati influenzati da molti tipi di danneggiamento fisico o logico.

## <a name="related-external-regulations--certifications"></a>Normative esterne correlate & certificazioni

I servizi online di Microsoft vengono regolarmente controllati per la conformità alle normative e alle certificazioni esterne. Fare riferimento alla tabella seguente per la convalida dei controlli correlati alla resilienza e alla continuità.

| **Controlli esterni** | **Sezione** | **Data ultimo report** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | CP-2: Piano di emergenza <br> CP-3: Formazione sulla emergenza <br> CP-4: Test del piano di emergenza <br> CP-6: sito di archiviazione alternativo <br> CP-7: sito di elaborazione alternativo <br> CP-9: backup del sistema di informazioni <br> CP-10: ripristino e ricostituzione del sistema di informazioni | 24 settembre 2020 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Dichiarazione di applicabilità](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Certificazione](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.17.1: Continuità della sicurezza delle informazioni <br> A.17.2: Licenzianze | 20 aprile 2021 |
| [ISO 22301 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=13951eb3-6339-4629-b80d-dd0d43812fe7&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Certificazione](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=2bb29cc0-53e7-4a53-a9de-871316e1b80c&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | Tutti i controlli | 18 marzo 2019 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-49: Criteri di backup <br> CA-50: Continuità aziendale <br> CA-51: Replica dei dati | 24 dicembre 2020 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-49: Criteri di backup <br> CA-50: Continuità aziendale <br> CA-51: Replica dei dati | 24 dicembre 2020 |
| [SOC 3 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=274054e5-4968-48d2-bf94-9a8eda5d7a93&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CUEC-09: ripristino della posta elettronica EXO | 24 dicembre 2020 |

## <a name="resources"></a>Risorse

- [White paper microsoft Enterprise Business Continuity Management Program](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=64f922a6-d624-40dd-a8ae-6f996b5186f3&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f) 
- [Report di convalida di Microsoft Cloud EBCM e del piano di ripristino di emergenza: FY21 Q4](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=83dc940a-2078-4e14-8b7d-07128e5b453d&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_FAQ_and_White_Papers)

## <a name="legal-disclaimer"></a>Dichiarazione di non responsabilità legale

- [Dichiarazione di non responsabilità della gestione della continuità aziendale della società](assurance-ebcm-legal-disclaimer.md)