---
title: Securities and Exchange Commission (SEC) Rule 17a-4(f) United States
description: Una società di valutazione indipendente ha convalidato che Azure e Office 365 possono aiutare le società finanziarie a soddisfare i requisiti di conservazione dei record della regola SEC 17a-4(f) e i requisiti di archiviazione non modificabili.
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
ms.openlocfilehash: f877bbec76cc0d760f2f908975b3818b88551829
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/05/2021
ms.locfileid: "50121205"
---
# <a name="securities-and-exchange-commission-sec-rule-17a-4f-united-states"></a>Securities and Exchange Commission (SEC) Rule 17a-4(f) United States

## <a name="about-sec-rule-17a-4f"></a>Informazioni sulla regola SEC 17a-4(f)

La [SEC (Us Securities and Exchange Commission)](https://www.sec.gov/) è un'agenzia indipendente del governo federale degli Stati Uniti e il principale sovrinsecatore e regolatore dei mercati dei titoli statunitensi. Essa gestisce l'autorità di imposizione sulle leggi federali in materia di titoli, propone nuove regole in materia di titoli e supervisiona la normativa di mercato del settore dei titoli.

La SEC definisce requisiti rigorosi ed espliciti per le entità regolamentate che decidno di conservare libri e record su supporti di archiviazione elettronici. Ha stabilito [17 CFR 240.17a-3](https://www.govinfo.gov/app/details/CFR-2012-title17-vol3/CFR-2012-title17-vol3-sec240-17a-3) e [17 CFR 240.17a-4](https://www.ecfr.gov/cgi-bin/text-idx?mc=true&node=pt17.4.240&rgn=div5#se17.4.240_117a_64) per regolare la gestione dei record, inclusi i periodi di conservazione, per i broker-rivenditori di titoli. In seguito, la [SEC](https://www.sec.gov/rules/interp/34-47806.htm) ha modificato il paragrafo 17 CFR 240.17a-4 (f), emettendo due rilasci interpretativi espressamente per consentire la conservazione di libri e record su supporti di archiviazione elettronici, purché siano soddisfatte determinate condizioni.

Un sistema di archiviazione elettronica soddisfa tali condizioni se impedisce l'alterazione o la cancellazione dei record per il periodo di conservazione richiesto. I periodi di conservazione variano da tre a sei anni in base ai tipi di record, con l'immediata accessibilità dei primi due anni. Inoltre, uno dei rilasci interpretativi richiede che il sistema di archiviazione sia in grado di conservare i record oltre il periodo di conservazione stabilito dalla SEC per conformarsi a richieste di comparizione, archiviazione a livello legale o altri requisiti di questo tipo.

## <a name="microsoft-and-sec-rule-17a-4f"></a>Regola Microsoft e SEC 17a-4(f)

I clienti di servizi finanziari, che rappresentano uno dei settori più regolamentati al mondo, sono soggetti a disposizioni complesse come la conservazione delle transazioni finanziarie e le comunicazioni correlate in uno stato non cancellabile e non modificabile. Tra le più prescrittive c'è la regola 17a-4(f) della SEC (Security and Exchange Commission) degli Stati Uniti che prevede requisiti rigosi per le entità regolamentate che decidino di conservare libri e record su supporti di archiviazione elettronici. I record archiviati devono essere a prova di manomissione senza possibilità di modificarli o eliminarli fino al termine del periodo di conservazione designato.

L'archiviazione BLOB non modificabile di Microsoft Azure con blocco dei criteri e Microsoft Office 365 con protezione dell'archiviazione può aiutare gli istituti finanziari a soddisfare i requisiti di archiviazione non modificabili della regola SEC 17a-4(f).

Per valutare la conformità di Azure e Office 365 alla regola SEC 17a-4(f), Microsoft ha mantenuto una società di valutazione indipendente specializzata nella gestione dei record e nella governance delle informazioni, Cohasset Associates. Nel report risultante per:

- **Azure**: valutazione della conformità [SEC 17a-4(f): Archiviazione](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=19b08fd4-d276-43e8-9461-715981d0ea20&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_GRC_Assessment_Reports)di Microsoft Azure , Cohasset ha convalidato che l'archiviazione BLOB non modificabile di [Azure](/azure/storage/blobs/storage-blob-immutable-storage) con l'opzione di blocco dei criteri, se usata per conservare BLOB basati sul tempo in un formato WORM (Non-Erasable and Non-Rewritable), soddisfa i requisiti di archiviazione non modificabili della regola SEC. Ogni BLOB (record) non può essere modificato, sovrascritto o eliminato fino alla scadenza del periodo di conservazione richiesto e al rilascio di eventuali blocchi legali associati. I provider di software e i partner con carichi di lavoro sensibili possono ora fare affidamento sull'archiviazione BLOB non modificabile di Azure come soluzione cloud per la conservazione dei record e l'archiviazione non modificabile. Gli istituti finanziari possono ora creare le proprie applicazioni sfruttando queste funzionalità pur rimanendo conformi.
- **Microsoft 365:** per i requisiti [sec 17a-4(f),](/microsoft-365/compliance/retention-regulatory-requirements#sec-17a-4f-finra-4511c-and-cftc-131c-d) Cohasset ha convalidato che Microsoft 365 include funzionalità di archiviazione che consentono ai clienti regolamentati, inclusi broker-rivenditori, di archiviare i dati in modo che rispettino i requisiti sec per la conservazione dei record. Le funzionalità di conservazione in Microsoft 365 consentono di mantenere una vasta gamma di dati, tra cui posta elettronica, segreteria telefonica, documenti condivisi, messaggi istantanei e dati di terze parti. In particolare, l'archiviazione in Microsoft 365 consente ai clienti di impostare criteri di conservazione della messaggistica globali o granulari per archiviare i dati per un periodo definito e oltre in un formato non riscrivibile e non cancellabile.

## <a name="microsoft-in-scope-cloud-services"></a>Servizi cloud Microsoft in ambito

- [Azure](https://gallery.technet.microsoft.com/Overview-of-Azure-c1be3942)
- [Office 365](https://aka.ms/Office365ComplianceOfferings)

## <a name="audits-reports-and-certificates"></a>Controlli, report e certificati

### <a name="azure--sec-rule-17"></a>Azure & sec Rule 17

[Valutazione di conformità SEC 17a-4(f) & CFTC 1.31 (c-d) di Archiviazione di Azure](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=19b08fd4-d276-43e8-9461-715981d0ea20&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_GRC_Assessment_Reports)

### <a name="office-365--sec-rule-17"></a>Regola SEC 17 & Office 365

[Valutazione della conformità SEC 17a-4(f): Centro sicurezza & e conformità Microsoft con SharePoint, OneDrive, Teams, Exchange e Skype for Business](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=9fa8349d-a0c9-47d9-93ad-472aa0fa44ec&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_FAQ_and_White_Papers)

## <a name="how-to-implement"></a>Come eseguire l'implementazione

### <a name="financial-services-regulation"></a>Regolamento sui servizi finanziari

Mappa di conformità dei principi normativi chiave degli Stati Uniti per il cloud computing e i servizi online Microsoft. [Altre informazioni](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=5b483567-00b0-4d86-96ae-ee887dadb61c&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_Compliance_Guides)

### <a name="risk-assessment--compliance-guide"></a>Guida alla conformità & valutazione dei rischi

Creare un modello di governance per la valutazione dei rischi dei servizi cloud Microsoft e la notifica dell'autorità di regolamentazione. [Altre informazioni](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=edee9b14-3661-4a16-ba83-c35caf672bd7&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_FAQ_and_White_Papers)

### <a name="financial-use-cases"></a>Casi d'uso finanziari

Usare panoramiche dei casi, esercitazioni e altre risorse per creare soluzioni di Azure per i servizi finanziari. [Altre informazioni](/azure/industry/financial/)

## <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a>Usare Microsoft Compliance Manager per valutare i rischi

[Microsoft Compliance Manager](/microsoft-365/compliance/compliance-manager) è una funzionalità nel [Centro conformità Microsoft 365](/microsoft-365/compliance/microsoft-365-compliance-center) utile per comprendere lo stato di conformità dell'organizzazione e intraprendere azioni per ridurre i rischi. Compliance Manager offre un modello premium per creare una valutazione per questa normativa. Individuare il modello nella pagina **modelli di valutazioni** in Compliance Manager. Informazioni su come [creare valutazioni in Compliance Manager](/microsoft-365/compliance/compliance-manager-assessments).

## <a name="resources"></a>Risorse

- [Archiviazione in Microsoft Office 365, conservazione dei dati e regola 17a-4](https://www.microsoft.com/microsoft-365/blog/2015/11/10/office-365-exchange-online-archiving-now-meets-sec-rule-17a-4-requirements/)
- [Conformità ai Servizi finanziari Microsoft](https://download.microsoft.com/download/6/4/7/64707E3E-6D3E-45D0-8207-A0EA3201B4A6/Microsoft%20Cloud%20-%20Financial%20Services%20Compliance%20Program%20\(Print\).pdf)
- [Programma di conformità Servizi cloud aziendali Microsoft e servizi finanziari](https://servicetrust.microsoft.com/viewpage/financialservicesoverview)
- [Azure Financial Services Compliance Program](https://azure.microsoft.com/resources/videos/azurecon-2015-financial-services-compliance-in-azure/)
- [Strumento di valutazione del rischio cloud di Azure per i servizi finanziari](https://servicetrust.microsoft.com/ViewPage/FFIECBlueprint?command=Download&downloadType=Document&downloadId=079a1973-711a-428f-9312-9ddd290cff7b&docTab=c726d5c0-2d1e-11e8-a485-57140ec19669_PaaS)
- [Microsoft Office di conservazione di 365](/office365/securitycompliance/retention-policies)
- [Community dei servizi finanziari Microsoft](https://techcommunity.microsoft.com/t5/financial-services/ct-p/FinancialServices)
- [Conformità nel Centro protezione Microsoft](https://www.microsoft.com/trust-center/compliance/compliance-overview)
