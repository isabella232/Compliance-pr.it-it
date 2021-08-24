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
ms.openlocfilehash: ff1719ce931a50904fb6b7e6069cd29a1883aa90
ms.sourcegitcommit: 4c00fd65d418065d7f53216c91f455ccb3891c77
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/23/2021
ms.locfileid: "58481798"
---
# <a name="resiliency-and-continuity-overview"></a>Panoramica sulla resilienza e sulla continuità

## <a name="how-does-microsoft-ensure-business-continuity-if-a-disaster-or-other-threat-to-service-availability-occurs"></a>In che modo Microsoft garantisce la continuità aziendale se si verifica un'emergenza o un'altra minaccia alla disponibilità del servizio?

Il team di Microsoft Enterprise Business Continuity Management (EBCM) supervisiona le attività di gestione della continuità aziendale e ripristino di emergenza servizi Microsoft e cloud. I rappresentanti delle unità aziendali Microsoft si coordinano con il team EBCM per sviluppare piani di continuità aziendale e convalidare la conformità ai requisiti di continuità aziendale.

Il ciclo di vita di Business Continuity Management (BCM) è alla base della metodologia BCM. Questo processo in tre fasi è progettato per essere adattabile in modo che possa essere implementato da un'ampia gamma di modelli aziendali in Microsoft. Inizia con una fase **di** valutazione per identificare i processi e gli obiettivi critici che devono essere inclusi nel programma di continuità aziendale. La fase di valutazione richiede anche un'analisi dell'impatto aziendale (BIA). La **fase di** pianificazione è incentrata sullo sviluppo e l'implementazione di strategie di resilienza e ripristino e sulla loro documentazione nei piani ufficiali di continuità aziendale. Infine, **Capability Validation** testa i piani di continuità aziendale e le relative implementazioni per verificare l'efficacia e identificare i potenziali miglioramenti.

Le strategie di continuità aziendale dei Servizi online Microsoft utilizzano la ridondanza hardware, di rete e del datacenter. La replica dei dati tra datacenter offre disponibilità elevata e affidabilità durante un incidente catastrofico. Aumenta inoltre la resilienza a eventi imprevisti banali, ad esempio errori hardware isolati o danneggiamento dei dati.

## <a name="how-does-microsoft-test-business-continuity-and-disaster-recovery-plans"></a>In che modo Microsoft testa la continuità aziendale e i piani di ripristino di emergenza?

Il criterio Enterprise EBCM (Business Continuity Management) di Microsoft stabilisce che tutti i piani di continuità aziendale e ripristino di emergenza di Microsoft devono essere testati, aggiornati e esaminati su base annuale. I servizi online Microsoft testano i propri piani di continuità aziendale almeno ogni anno in base ai criteri EBCM. Dopo aver creato e esaminato i report azione per convalidare, testare i risultati e informare gli aggiornamenti del piano in risposta a eventuali problemi rilevati durante il test.

Per convalidare la flessibilità e le strategie di ripristino rispetto a un'ampia gamma di potenziali incidenti, il programma EBCM definisce più categorie di scenari di test che interessano persone, località e tecnologia. Il livello di convalida necessario per ogni servizio è basato sulla relativa criticità, per cui i servizi con la maggiore criticità ricevono una convalida più rigorosa. Ogni team del servizio online Microsoft testa il piano di continuità aziendale in base alle linee guida EBCM per misurare l'efficacia del piano e la disponibilità del team del servizio ad eseguire il piano.

In base alle linee guida EBCM, le revisioni annuali dei piani di continuità aziendale e della convalida delle funzionalità devono avere luogo entro 12 mesi dall'ultima revisione. La convalida delle funzionalità deve includere la revisione della documentazione di supporto, ad esempio il BIA, per garantire che rimanga accurata. Microsoft rende disponibili ai clienti i risultati della convalida delle funzionalità per i servizi online Microsoft selezionati tramite report trimestrali.

## <a name="how-do-microsoft-online-services-ensure-system-capacity-meets-demand"></a>In che modo i servizi online Microsoft garantiscono che la capacità del sistema soddisfi la domanda?

La pianificazione della capacità consente ai team di servizio di allocare le risorse necessarie per supportare la disponibilità dei servizi online Microsoft. È necessaria una pianificazione regolare della capacità come parte del programma EBCM di Microsoft. I team di servizio esaminano i dati sulla capacità durante le revisioni trimestrali e durante le situazioni di emergenza che giustificano una maggiore revisione della capacità.

I dati non elaborati per la pianificazione della capacità vengono gestiti da ogni team del servizio e includono metriche come l'elaborazione del sistema, la memoria e la capacità hardware. Le revisioni pianificate usano un modello della capacità corrente del sistema e lo testano in base alle esigenze previste in situazioni di emergenza. Se il modello indica lacune nella capacità, le modifiche proposte alla capacità del sistema vengono sottoposte alla leadership del team di assistenza per la revisione. Le modifiche approvate vengono incorporate in un nuovo modello prima dell'implementazione da parte dei tecnici del team di assistenza.

## <a name="how-do-microsoft-online-services-maintain-service-availability-during-routine-system-failures"></a>In che modo i servizi online Microsoft mantengono la disponibilità del servizio durante gli errori di sistema di routine?

I servizi online Microsoft consentono di ottenere la resilienza del servizio tramite l'architettura ridondante, la replica dei dati e il controllo automatico dell'integrità. L'architettura ridondante prevede la distribuzione di più istanze di un servizio in hardware geograficamente e fisicamente separati, offrendo una maggiore tolleranza di errore per i servizi online Microsoft. La replica dei dati garantisce che siano sempre presenti più copie dei dati dei clienti in diverse aree di errore, consentendo il ripristino dei dati critici dei clienti in caso di danneggiamento, perdita o persino eliminazione accidentale da parte del cliente. Il controllo automatico dell'integrità aumenta la disponibilità dei dati ripristinando automaticamente i dati influenzati da molti tipi di danneggiamento fisico o logico.

## <a name="related-external-regulations--certifications"></a>Normative esterne correlate & certificazioni

I servizi online di Microsoft vengono regolarmente controllati per la conformità alle normative e alle certificazioni esterne. Fare riferimento alla tabella seguente per la convalida dei controlli correlati alla resilienza e alla continuità.

### <a name="azure-and-dynamics-365"></a>Azure e Dynamics 365

| **Controlli esterni** | **Sezione** | **Data ultimo report** |
|:--------------------|:------------|:-----------------------|
| [ISO 27001/27002](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Dichiarazione di applicabilità](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=00af6c3e-7f3e-4e0d-8b0e-79f45ef2cef1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Certificazione](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7af5304-3a31-40e6-9abb-e26352305d41&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.17.1: Continuità della sicurezza delle informazioni <br> A.17.2: Licenzianze | 2 dicembre 2020 |
| [ISO 22301](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=6d388547-fc88-46e3-8de2-6bc2edc08b06&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Certificazione](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=ee4b611b-bb4d-4056-b189-00da36e88949&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | Tutti i controlli | 13 maggio 2020 |
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b8721ebd-af20-42fe-b22f-8332b0a19517&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=234a0f57-83c1-4afc-a586-a0e7a59592f7&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 3](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=75c8cbf6-e456-473c-a05e-34fea888ec2a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | BC-1: Piani di continuità aziendale <br> BC-3: Procedure di continuità aziendale e ripristino di emergenza <br> BC-4: test BCDR <br> BC-7: Piani di continuità aziendale del datacenter <br> BC-8: Test di continuità aziendale del datacenter <br> BC-9: valutazione della resilienza del datacenter <br> DS-5: componenti del servizio chiave di backup <br> DS-6: ridondanza di componenti critici <br> DS-7: replica automatica dei dati dei clienti <br> DS-8: pianificazione del backup <br> DS-9: procedure di ripristino del backup <br> DS-11: backup fuori sede <br> DS-14: ripristino automatico del servizio clienti | 31 marzo 2021 |

### <a name="office-365"></a>Office 365

| **Controlli esterni** | **Sezione** | **Data ultimo report** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP](https://compliance.microsoft.com/compliancemanager) | CP-2: Piano di emergenza <br> CP-3: Formazione sulla emergenza <br> CP-4: Test del piano di emergenza <br> CP-6: sito di archiviazione alternativo <br> CP-7: sito di elaborazione alternativo <br> CP-9: backup del sistema di informazioni <br> CP-10: ripristino e ricostituzione del sistema di informazioni | 24 settembre 2020 |
| [ISO 27001/27002](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Dichiarazione di applicabilità](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.17.1: Continuità della sicurezza delle informazioni <br> A.17.2: Licenzianze | 20 aprile 2021 |
| [ISO 22301](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=13951eb3-6339-4629-b80d-dd0d43812fe7&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | Tutti i controlli | 18 marzo 2019 |
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-49: Criteri di backup <br> CA-50: Continuità aziendale <br> CA-51: Replica dei dati | 24 dicembre 2020 |
| [SOC 3](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=274054e5-4968-48d2-bf94-9a8eda5d7a93&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CUEC-09: ripristino della posta elettronica EXO | 24 dicembre 2020 |

## <a name="resources"></a>Risorse

- [White paper microsoft Enterprise Business Continuity Management Program](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=64f922a6-d624-40dd-a8ae-6f996b5186f3&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f)
- [Report di convalida di Microsoft Cloud EBCM e del piano di ripristino di emergenza: FY21 Q4](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=83dc940a-2078-4e14-8b7d-07128e5b453d&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_FAQ_and_White_Papers)

## <a name="legal-disclaimer"></a>Dichiarazione di non responsabilità legale

- [Dichiarazione di non responsabilità della gestione della continuità aziendale della società](assurance-ebcm-legal-disclaimer.md)