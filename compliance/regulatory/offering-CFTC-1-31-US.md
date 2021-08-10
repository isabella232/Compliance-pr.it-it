---
title: Commodity Futures Trading Commission (CFTC) Rule 1.31(c-d) Stati Uniti
description: Una società di valutazione indipendente ha convalidato che Azure e Office 365 possono aiutare le società finanziarie a soddisfare i requisiti di conservazione dei record e di archiviazione non modificabili della regola CFTC 1.31.
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
ms.openlocfilehash: 903f4d3db8965fdcd8c96a8d474e5180430b4966e4adc6945315f283ddbc0d3f
ms.sourcegitcommit: af1925730de60c3b698edc4e1355c38972bdd759
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/05/2021
ms.locfileid: "54292583"
---
# <a name="commodity-futures-trading-commission-cftc-rule-131c-d-united-states"></a>Commodity Futures Trading Commission (CFTC) Rule 1.31(c-d) Stati Uniti

## <a name="about-cftc-rule-13c-d"></a>Informazioni sulla regola CFTC 1.3(c-d)

La [Commodity Futures Trading Commission](https://www.cftc.gov/) (CFTC), un'agenzia federale statunitense indipendente, regola i mercati dei future e delle opzioni delle commodity e, più di recente, il mercato degli scambi.  
  
La regola CFTC di lunga data 1.31 definisce i requisiti di conservazione dei record stabiliti dalla regola SEC 17a-4(f). Inoltre, specifica che i record elettronici devono essere mantenuti per cinque anni e che gli originali devono essere mantenuti "facilmente accessibili" durante i primi due anni e resi disponibili per l'ispezione da parte della Commissione o del Dipartimento di giustizia degli Stati Uniti durante l'intero periodo di conservazione.  
  
Nel 2017, [il CFTC](https://www.cftc.gov/sites/default/files/idc/groups/public/@lrfederalregister/documents/file/2017-11014a.pdf)ha rivisto la sua regola, modificando e modernizzando la normativa di gestione dei record per adottare standard meno prescrittivi basati sui principi che offrono maggiore flessibilità nel modo in cui è possibile mantenere i record. Questa revisione rende la regola più neutra in termini di tecnologia, consentendo alle entità regolamentate di scegliere la tecnologia più appropriata per la propria azienda mantenendo al contempo le misure di sicurezza che "garantiscono l'affidabilità del processo di gestione dei record". La regola rivista rimuove il requisito che le organizzazioni mantengano i record originali per due anni, ma mantiene il periodo di manutenzione di cinque anni, che armonizza le pratiche per le aziende regolamentate sia dal CFTC che dalla SEC.

## <a name="microsoft-and-cftc-rule-131c-d"></a>Regola Microsoft e CFTC 1.31(c-d)

I clienti dei servizi finanziari, che rappresentano uno dei settori più regolamentati al mondo, sono soggetti a disposizioni complesse come la conservazione delle transazioni finanziarie e le comunicazioni correlate in uno stato non cancellabile e non modificabile. Uno dei più prescrittivi è la regola 1.31 della US Commodity Futures Trading Commission (CFTC) che stabilisce requisiti rigosi per le entità regolamentate che decidno di conservare libri e record su supporti di archiviazione elettronici. I record archiviati devono essere a prova di manomissione senza possibilità di modificarli o eliminarli fino a dopo il periodo di conservazione designato. Microsoft Azure L'Archiviazione BLOB non modificabile con Policy Lock e Microsoft Office 365 con Preservation Lock può aiutare gli istituti finanziari a soddisfare i requisiti di archiviazione della regola CFTC 1.31(c-d).

### <a name="microsoft-azure"></a>Microsoft Azure

Per valutare la conformità di Azure alla regola CFTC 1.31(c-d), Microsoft ha mantenuto una società di valutazione indipendente specializzata nella gestione dei record e nella governance delle informazioni, Cohasset Associates. Nel report risultante, [CFTC 1.31 (c)–(d) Compliance Assessment: Archiviazione di Microsoft Azure](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=19b08fd4-d276-43e8-9461-715981d0ea20&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_GRC_Assessment_Reports), Cohasset ha convalidato che [il Archiviazione BLOB](/azure/storage/blobs/storage-blob-immutable-storage) non modificabile di Azure con l'opzione Blocco criteri, se usato per conservare i BLOB basati sul tempo in un formato WORM non cancellabile e non risibile, soddisfa i requisiti basati sui principi della regola CFTC. Ogni BLOB (record) è protetto dalla modifica, dalla sovrascrittura o dall'eliminazione fino alla scadenza del periodo di conservazione richiesto e al rilascio di eventuali blocchi legali associati. I provider di software e i partner con carichi di lavoro sensibili possono ora fare affidamento su Azure Immutable Blob Archiviazione come soluzione cloud di negozio unica per la conservazione dei record. Gli istituti finanziari possono ora creare le proprie applicazioni sfruttando queste funzionalità pur rimanendo conformi.

### <a name="microsoft-365"></a>Microsoft 365

Per i requisiti [CFTC 1.31(c)-(d),](/microsoft-365/compliance/retention-regulatory-requirements#sec-17a-4f-finra-4511c-and-cftc-131c-d) Cohasset ha convalidato che Microsoft 365 include funzionalità di archiviazione che consentono ai clienti regolamentati, inclusi i broker-rivenditori, di archiviare i dati in modo che siano conformi ai requisiti SEC per la conservazione dei record. Le funzionalità di conservazione in Microsoft 365 consentono di conservare un'ampia gamma di dati, tra cui posta elettronica, segreteria telefonica, documenti condivisi, messaggi istantanei e dati di terze parti. In particolare, l'archiviazione in Microsoft 365 consente ai clienti di impostare criteri di conservazione della messaggistica globali o granulari per archiviare i dati per un periodo definito e oltre in un formato non riscrivibile e non cancellabile.

## <a name="microsoft-in-scope-cloud-platforms--services"></a>Piattaforme e servizi cloud Microsoft inclusi nell'ambito

- [Azure](https://aka.ms/AzureCompliance)
- [Office 365](https://aka.ms/o365-compliance-framework)

## <a name="audits-reports-and-certificates"></a>Controlli, report e certificati

[Azure & CFTC Rule 1.31: SEC 17a-4(f) & CFTC 1.31(c-d) Compliance Assessment of Archiviazione di Azure

[Office 365 & REGOLA CFTC 1.31: Archiviazione in Office 365, conservazione dei dati e conformità della regola SEC 17a-4

## <a name="how-to-implement"></a>Come eseguire l'implementazione

- [Regolamentazione dei servizi finanziari](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=5b483567-00b0-4d86-96ae-ee887dadb61c&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_Compliance_Guides): Mappa di conformità dei principali principi normativi statunitensi per il cloud computing e i servizi online Microsoft.
- [Valutazione dei rischi e guida alla conformità](https://aka.ms/RiskGovernanceGuide): creare un modello di governance per la valutazione dei rischi dei servizi cloud Microsoft e la notifica all'organismo di regolamentazione.
- [Casi di utilizzo finanziari](/azure/industry/financial/): usare panoramiche di casi, esercitazioni e altre risorse per creare soluzioni di Azure per i servizi finanziari.

## <a name="resources"></a>Risorse

- [Microsoft Financial Services Compliance Program](https://aka.ms/FSCP-Print)
- [Servizi cloud e servizi finanziari di Microsoft per le aziende](https://www.microsoft.com/trustcenter/cloudservices/financialservices)
- [Azure Financial Services Compliance Program](https://azure.microsoft.com/resources/videos/azurecon-2015-financial-services-compliance-in-azure/)
- [Microsoft Office 365 Criteri di conservazione](/office365/securitycompliance/retention-policies)
- [Blog sui servizi finanziari di Microsoft](https://techcommunity.microsoft.com/t5/Financial-Services-Blog/bg-p/FinancialServicesBlog)
- [Conformità nel Centro protezione Microsoft](https://www.microsoft.com/trust-center/compliance/compliance-overview)
