---
title: Resilienza e continuità
description: Informazioni sulla resilienza e la continuità in Microsoft 365
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
ms.openlocfilehash: 2cc3f35a9d109a1a84159de8d0518f58270e3fe9
ms.sourcegitcommit: 1dc97ae3f0511cb1a41565da56e725bbe0cb013c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "49671181"
---
# <a name="resiliency-and-continuity-overview"></a>Panoramica sulla resilienza e sulla continuità

## <a name="how-does-microsoft-ensure-business-continuity-in-the-case-of-a-disaster-or-other-threat-to-service-availability"></a>In che modo Microsoft garantisce la continuità aziendale nel caso di un'emergenza o di altre minacce per la disponibilità del servizio?

Il team di Microsoft Enterprise Business Continuity Management (EBCM) supervisiona la gestione della continuità aziendale e le attività di ripristino di emergenza tra i servizi Microsoft e le offerte cloud. I rappresentanti di Microsoft Business Unit, ad esempio Microsoft 365, coordinano con il team di EBCM per sviluppare piani di continuità aziendale e convalidare la conformità con i requisiti di continuità aziendale.

Al centro della nostra metodologia di Business Continuity Management (BCM) è il ciclo di vita di BCM. Questo processo in tre fasi è stato creato per essere adattabile, in modo che possa essere implementato da una vasta gamma di modelli aziendali in Microsoft. Inizia con una fase di **valutazione** per identificare i processi critici e gli obiettivi che devono essere inclusi nel programma di continuità aziendale. La fase di valutazione richiede anche un'analisi di impatto aziendale (BIA). La fase di **pianificazione** è incentrata sullo sviluppo e l'implementazione delle strategie di resilienza e ripristino, oltre a documentarli nei piani ufficiali di continuità aziendale. Infine, test di **convalida delle funzionalità** piani di continuità aziendale e relative implementazioni per verificare l'efficacia e identificare i potenziali miglioramenti.

La strategia di continuità aziendale di Microsoft 365 utilizza la ridondanza di hardware, reti e Datacenter. La replica dei dati tra i datacenter garantisce un'elevata disponibilità e affidabilità nel caso di un incidente catastrofico. Aumenta inoltre la resilienza degli incidenti banali, come un errore hardware isolato o un danneggiamento dei dati.

## <a name="how-does-microsoft-test-business-continuity-and-disaster-recovery-plans"></a>In che modo Microsoft testing Business Continuity and Disaster Recovery piani?

Il criterio Microsoft Enterprise Business Continuity Management (EBCM) stabilisce che tutti i piani di continuità aziendale e di ripristino di emergenza di Microsoft devono essere testati, aggiornati e recensiti su base annua. I servizi Microsoft 365 testano i piani di continuità aziendale almeno ogni anno per i criteri di EBCM. Dopo la creazione e la revisione dei rapporti di azione per convalidare, testare i risultati e informare gli aggiornamenti dei piani in risposta a eventuali problemi riscontrati durante il testing.

Per convalidare la resilienza e le strategie di ripristino rispetto a una vasta gamma di potenziali incidenti, il programma EBCM definisce più categorie di scenari di test che interessano persone, percorsi e tecnologia. Il livello di convalida necessario per ogni servizio si basa sulla criticità del servizio, con servizi più critici che ricevono una convalida più rigorosa. Ogni team del servizio Microsoft 365 verifica il piano di continuità aziendale in base alle linee guida di EBCM per misurare l'efficacia del piano e la disponibilità del team di servizio per l'esecuzione del piano.

Per le linee guida di EBCM, le revisioni annuali dei piani di continuità aziendale e la convalida delle funzionalità devono essere effettuate entro 12 mesi dall'ultima revisione. La convalida delle funzionalità deve includere la revisione della documentazione di supporto, ad esempio BIA, per garantire che rimanga accurata. Microsoft apporta risultati di convalida delle funzionalità per selezionare i servizi Microsoft 365 disponibili per i clienti tramite report trimestrali.

## <a name="how-does-microsoft-365-ensure-system-capacity-meets-demand"></a>In che modo Microsoft 365 garantisce che la capacità del sistema soddisfi la richiesta?

La pianificazione della capacità consente ai team di servizi di allocare le risorse necessarie per supportare la disponibilità del servizio Microsoft 365. La pianificazione della capacità regolare è necessaria nell'ambito del programma EBCM di Microsoft. I team di servizio esaminano i dati sulla capacità durante le revisioni trimestrali, nonché durante le situazioni di emergenza che garantiscono un ulteriore revisione della capacità.

I dati non elaborati per la pianificazione della capacità vengono gestiti da ogni team di servizio e includono metriche come l'elaborazione del sistema, la memoria e la capacità hardware. Le recensioni pianificate utilizzano un modello della capacità corrente del sistema e le verificano in base alle esigenze previste in situazioni di emergenza. Se il modello indica gli spazi vuoti di capacità, le modifiche proposte alla capacità del sistema vengono inviate alla leadership del team di servizio per la revisione. Le modifiche approvate sono incorporate in un nuovo modello prima dell'implementazione da parte di ingegneri del team di servizio

## <a name="how-does-microsoft-365-maintain-service-availability-during-routine-system-failures"></a>In che modo Microsoft 365 gestisce la disponibilità del servizio durante gli errori del sistema di routine?

Microsoft 365 raggiunge la resilienza del servizio tramite l'architettura ridondante, la replica dei dati e il controllo dell'integrità automatizzata. L'architettura ridondante implica la distribuzione di più istanze di un servizio su hardware geograficamente e fisicamente separato, garantendo una maggiore tolleranza di errore per i servizi Microsoft 365. La replica dei dati garantisce che vi siano sempre più copie di dati dei clienti in diverse aree di errore, consentendo di recuperare i dati critici dei clienti se danneggiati, persi o addirittura accidentalmente eliminati dal cliente. Il controllo dell'integrità automatizzata aumenta la disponibilità dei dati ripristinando automaticamente i dati interessati da molti tipi di danneggiamenti fisici o logici.

## <a name="related-external-regulations--certifications"></a>Normative esterne correlate & certificazioni

I servizi online di Microsoft vengono controllati regolarmente per la conformità con le certificazioni e le normative esterne. Fare riferimento alla tabella seguente per la convalida dei controlli relativi alla resilienza e alla continuità.

| **Verifiche esterne** | **Sezione** | **Data ultimo rapporto** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | CP-2: piano di emergenza <br> CP-3: training di contingenza <br> CP-4: test del piano di emergenza <br> CP-6: sito di archiviazione alternativo <br> CP-7: sito di elaborazione alternativo <br> CP-9: backup del sistema di informazioni <br> CP-10: ripristino e ricostituzione del sistema informativo | 24 settembre 2020 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Dichiarazione di applicabilità](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certificazione](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A. 17,1: continuità della sicurezza delle informazioni <br> A. 17,2: ridondanze | 22 febbraio 2020 |
| [ISO 22301 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=13951eb3-6339-4629-b80d-dd0d43812fe7&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Certificazione](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=2bb29cc0-53e7-4a53-a9de-871316e1b80c&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | Tutti i controlli | 18 marzo 2019 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b07c0f7b-6bd5-4544-8255-7a5f14bf914a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-49: criteri di backup <br> CA-50: continuità aziendale <br> CA-51: replica dei dati | 30 settembre 2019 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=fa062990-e758-4ddc-ace3-7fb21a301d09&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Rep-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-49: criteri di backup <br> CA-50: continuità aziendale <br> CA-51: replica dei dati | 30 settembre 2019 |
| [SOC 3 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=9df8b99b-96ce-49a9-bff4-268031dcc9a6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CUEC-09: ripristino di posta elettronica EXO | 30 settembre 2019 |

## <a name="resources"></a>Risorse

- [White paper del programma di gestione della continuità aziendale di Microsoft Enterprise](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=64f922a6-d624-40dd-a8ae-6f996b5186f3&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f) 
- [Report di convalida di Microsoft Cloud EBCM e Disaster Recovery Plan: FY21 Q1 e Q2](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=b4181ab3-b03d-4a62-b396-4bfd1c98ddb0&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_FAQ_and_White_Papers)

## <a name="legal-disclaimer"></a>Dichiarazione di non responsabilità legale

- [Dichiarazione di non responsabilità della gestione della continuità aziendale della società](assurance-ebcm-legal-disclaimer.md)