---
title: Regola 4511(c) Dell'autorità di regolamentazione del settore finanziario (FINRA) Stati Uniti
description: Una società di valutazione indipendente ha convalidato che Azure e Office 365 possono aiutare le società finanziarie a soddisfare i requisiti di conservazione dei record e di archiviazione non modificabili della regola FINRA 4511.
keywords: Microsoft 365, conformità, offerte
localization_priority: None
ms.prod: microsoft-365-enterprise
ms.topic: article
f1.keywords:
- NOCSH
ms.author: robmazz
author: robmazz
manager: laurawi
audience: itpro
ms.collection:
- M365-security-compliance
- MS-Compliance
hideEdit: true
titleSuffix: Microsoft Compliance
ms.openlocfilehash: 0b45e9e526ad95030eed1a6b7b1814ad4aee66e8b33651ee466d71795ba97f74
ms.sourcegitcommit: af1925730de60c3b698edc4e1355c38972bdd759
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/05/2021
ms.locfileid: "54287435"
---
# <a name="financial-industry-regulatory-authority-finra-rule-4511c-united-states"></a>Regola 4511(c) Dell'autorità di regolamentazione del settore finanziario (FINRA) Stati Uniti

## <a name="about-finra-rule-4511"></a>Informazioni sulla regola FINRA 4511

La [Financial Industry Regulatory Authority (FINRA)](https://www.finra.org/#/) è il più grande organismo indipendente che regolamenta le società di titoli con la supervisione di più di 4.500 società di intermediazione negli Stati Uniti. È stato autorizzato dal Congresso degli Stati Uniti "a proteggere gli investitori statunitensi assicurando che il settore broker-rivenditori opeli equamente e onestamente".

Nel 2011, la Commissione per la sicurezza e la Exchange (SEC) statunitense ha approvato l'adozione finRA delle regole SEC che regolano la conservazione di libri e record su supporti di archiviazione elettronici. La regola [FINRA 4511(c)](https://www.finra.org/sites/default/files/NoticeDocument/p123548.pdf) specifica che "tutti i libri e i record necessari per essere effettuati ai sensi delle regole FINRA devono essere conservati in un formato e supporti conformi alla regola SEA (Securities Exchange Act) 17a-4".

Inoltre, la regola FINRA 4511(c) richiede alle aziende di conservare per un periodo di almeno sei anni tali libri e record per i quali non esiste un periodo di conservazione specificato in base alle regole FINRA o SEA applicabili. In effetti, se i libri e i record riguardano un account, il periodo di conservazione deve essere di sei anni dopo la chiusura dell'account. In caso contrario, il periodo di conservazione è di sei anni dopo la creazione di tali libri e record.

## <a name="microsoft-and-finra-rule-4511c"></a>Regola Microsoft e FINRA 4511(c)

I clienti dei servizi finanziari, che rappresentano uno dei settori più regolamentati al mondo, sono soggetti a disposizioni complesse come la conservazione delle transazioni finanziarie e le comunicazioni correlate in uno stato non cancellabile e non modificabile. Tra questi c'è la regola 4511 della Financial Industry Regulatory Authority (FINRA) che stabilisce requisiti rigosi per le entità regolamentate che decidno di conservare libri e record su supporti di archiviazione elettronici. I record archiviati devono essere a prova di manomissione senza possibilità di modificarli o eliminarli fino a dopo il periodo di conservazione designato.

Microsoft Azure L'Archiviazione BLOB non modificabile con blocco dei criteri e Microsoft Office 365 con blocco di conservazione può aiutare gli istituti finanziari a soddisfare i requisiti di archiviazione non modificabili della regola FINRA 4511(c).

## <a name="microsoft-azure"></a>Microsoft Azure

Per valutare la conformità di Azure alla regola FINRA 4511(c), Microsoft ha mantenuto una società di valutazione indipendente specializzata nella gestione dei record e nella governance delle informazioni, Cohasset Associates. Il report risultante, [SEC 17a-4(f) & CFTC 1.31 (c-d) Compliance Assessment: Archiviazione di Microsoft Azure](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=19b08fd4-d276-43e8-9461-715981d0ea20&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_GRC_Assessment_Reports), comprende la conformità di Azure alla regola FINRA 4511(c), che rinvia ai requisiti di formato e supporto della regola SEC 17a-4(f).

Cohasset ha convalidato che il [Archiviazione BLOB](/azure/storage/blobs/storage-blob-immutable-storage) non modificabile di Azure con l'opzione Blocco criteri, se usato per conservare i BLOB basati sul tempo in un formato WORM (Non-Erasable and Non-Rewritable), soddisfa i requisiti di archiviazione FINRA pertinenti. Ogni BLOB (record) è protetto dalla modifica, dalla sovrascrittura o dall'eliminazione fino alla scadenza del periodo di conservazione richiesto e al rilascio di eventuali blocchi legali associati.

I provider di software e i partner con carichi di lavoro sensibili possono ora fare affidamento su Azure Immutable Blob Archiviazione come soluzione cloud di negozio unica per la conservazione dei record e l'archiviazione non modificabile. Gli istituti finanziari possono ora creare le proprie applicazioni sfruttando queste funzionalità pur rimanendo conformi.

## <a name="microsoft-365"></a>Microsoft 365

Per i requisiti della regola [FINRA 4511(c),](/microsoft-365/compliance/retention-regulatory-requirements#sec-17a-4f-finra-4511c-and-cftc-131c-d) Cohasset ha convalidato che Microsoft 365 include funzionalità di archiviazione che consentono ai clienti regolamentati, inclusi i broker-rivenditori, di archiviare i dati in modo che siano conformi ai requisiti SEC per la conservazione dei record. Le funzionalità di conservazione in Microsoft 365 consentono di conservare un'ampia gamma di dati, tra cui posta elettronica, segreteria telefonica, documenti condivisi, messaggi istantanei e dati di terze parti. In particolare, l'archiviazione in Microsoft 365 consente ai clienti di impostare criteri di conservazione della messaggistica globali o granulari per archiviare i dati per un periodo definito e oltre in un formato non riscrivibile e non cancellabile.

## <a name="microsoft-in-scope-cloud-platforms--services"></a>Piattaforme e servizi cloud Microsoft inclusi nell'ambito

- [Azure](https://gallery.technet.microsoft.com/Overview-of-Azure-c1be3942)
- [Office 365](https://aka.ms/Office365ComplianceOfferings)

## <a name="audits-reports-and-certificates"></a>Controlli, report e certificati

### <a name="azure--finra-rule-4511c"></a>Azure & FINRA Rule 4511(c)

[Sec 17a-4(f) & CFTC 1.31 (c-d) Compliance Assessment of Archiviazione di Azure](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=19b08fd4-d276-43e8-9461-715981d0ea20&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_GRC_Assessment_Reports)

### <a name="office-365--finra-rule-4511c"></a>Office 365 & FINRA Rule 4511(c)

[Archiviazione in Office 365, conservazione dei dati e conformità della regola SEC 17a-4](https://www.microsoft.com/microsoft-365/blog/2015/11/10/office-365-exchange-online-archiving-now-meets-sec-rule-17a-4-requirements/)

## <a name="how-to-implement"></a>Come eseguire l'implementazione

- **Regolamentazione dei servizi finanziari**: Mappa di conformità dei principali principi normativi statunitensi per il cloud computing e i servizi online Microsoft. [Altre informazioni](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=5b483567-00b0-4d86-96ae-ee887dadb61c&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_Compliance_Guides)
- **Valutazione dei rischi e guida alla conformità**: creare un modello di governance per la valutazione dei rischi dei servizi cloud Microsoft e la notifica all'organismo di regolamentazione. [Altre informazioni](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=edee9b14-3661-4a16-ba83-c35caf672bd7&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_FAQ_and_White_Papers)
- **Casi di utilizzo finanziari**: usare panoramiche di casi, esercitazioni e altre risorse per creare soluzioni di Azure per i servizi finanziari. [Altre informazioni](/azure/industry/financial/)

## <a name="resources"></a>Risorse

- [Microsoft Financial Services Compliance Program](https://download.microsoft.com/download/6/4/7/64707E3E-6D3E-45D0-8207-A0EA3201B4A6/Microsoft%20Cloud%20-%20Financial%20Services%20Compliance%20Program%20\(Print\).pdf)
- [Servizi cloud e servizi finanziari di Microsoft per le aziende](https://servicetrust.microsoft.com/viewpage/financialservicesoverview)
- [Azure Financial Services Compliance Program](https://azure.microsoft.com/resources/videos/azurecon-2015-financial-services-compliance-in-azure/)
- [Strumento di valutazione del rischio cloud di Azure per i servizi finanziari](https://servicetrust.microsoft.com/ViewPage/FFIECBlueprint?command=Download&downloadType=Document&downloadId=079a1973-711a-428f-9312-9ddd290cff7b&docTab=c726d5c0-2d1e-11e8-a485-57140ec19669_PaaS)
- [Microsoft Office 365 Criteri di conservazione](/office365/securitycompliance/retention-policies)
- [Blog sui servizi finanziari di Microsoft](https://techcommunity.microsoft.com/t5/Financial-Services-Blog/bg-p/FinancialServicesBlog)
- [Conformità nel Centro protezione Microsoft](https://www.microsoft.com/trust-center/compliance/compliance-overview)
