---
title: Securities and Exchange Commission (SEC) Rule 17a-4(f) United States
description: Una società di valutazione indipendente ha convalidato che Azure e Office 365 possono aiutare le società finanziarie a soddisfare i requisiti di conservazione dei record e di archiviazione non modificabili della regola SEC 17a-4(f).
keywords: Microsoft 365, conformità, offerte
ms.localizationpriority: medium
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
ms.openlocfilehash: 50c44b6801e15af02bf4bfa4f4d46758b7a6c7a8
ms.sourcegitcommit: 70efe7749db2c6dd4ae0faa8ac22da6e87109c79
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/30/2021
ms.locfileid: "58707125"
---
# <a name="securities-and-exchange-commission-sec-rule-17a-4f-united-states"></a>Securities and Exchange Commission (SEC) Rule 17a-4(f) United States

## <a name="about-sec-rule-17a-4f"></a>Informazioni sulla regola SEC 17a-4(f)

[La US Securities and Exchange Commission (SEC)](https://www.sec.gov/) è un'agenzia indipendente del governo federale statunitense e il principale supervisore e regolatore dei mercati dei titoli statunitensi. Essa gestisce l'autorità di imposizione sulle leggi federali in materia di titoli, propone nuove regole in materia di titoli e supervisiona la regolamentazione di mercato del settore dei titoli.

La SEC definisce requisiti rigorosi ed espliciti per le entità regolamentate che decidno di conservare libri e record su supporti di archiviazione elettronici. Ha stabilito [17 CFR 240.17a-3](https://www.govinfo.gov/app/details/CFR-2012-title17-vol3/CFR-2012-title17-vol3-sec240-17a-3) e [17 CFR 240.17a-4](https://www.ecfr.gov/cgi-bin/text-idx?mc=true&node=pt17.4.240&rgn=div5#se17.4.240_117a_64) per regolare la gestione dei record, compresi i periodi di conservazione, per i broker-rivenditori di titoli. In seguito, la [SEC](https://www.sec.gov/rules/interp/34-47806.htm) ha modificato il paragrafo 17 CFR 240.17a-4 (f), emettendo due rilasci interpretativi espressamente per consentire la conservazione di libri e record su supporti di archiviazione elettronici purché siano soddisfatte determinate condizioni.

Un sistema di archiviazione elettronico soddisfa tali condizioni se impedisce l'alterazione o la cancellazione dei record per il periodo di conservazione richiesto. I periodi di conservazione variano da tre a sei anni in base ai tipi di record, con l'accessibilità immediata per i primi due anni. Inoltre, uno dei rilasci interpretativi richiede che il sistema di archiviazione sia in grado di conservare i record oltre il periodo di conservazione stabilito dalla SEC per conformarsi a citazioni in giudizio, archiviazione legale o altri requisiti di questo tipo.

## <a name="microsoft-and-sec-rule-17a-4f"></a>Regola Microsoft e SEC 17a-4(f)

I clienti dei servizi finanziari, che rappresentano uno dei settori più regolamentati al mondo, sono soggetti a disposizioni complesse come la conservazione delle transazioni finanziarie e le comunicazioni correlate in uno stato non cancellabile e non modificabile. Tra i più prescrittivi è la regola 17a-4(f) della Commissione per la sicurezza e la Exchange (SEC) statunitense che stabilisce requisiti rigosi per le entità regolamentate che decidno di conservare libri e record su supporti di archiviazione elettronici. I record archiviati devono essere a prova di manomissione senza possibilità di modificarli o eliminarli fino a dopo il periodo di conservazione designato.

Microsoft Azure L'Archiviazione BLOB non modificabile con Policy Lock e Microsoft Office 365 con Preservation Lock può aiutare gli istituti finanziari a soddisfare i requisiti di archiviazione non modificabili della regola SEC 17a-4(f).

## <a name="microsoft-in-scope-cloud-platforms--services"></a>Piattaforme e servizi cloud Microsoft inclusi nell'ambito

- [Azure](https://gallery.technet.microsoft.com/Overview-of-Azure-c1be3942)
- [Office 365](https://aka.ms/Office365ComplianceOfferings)

## <a name="independent-assessments"></a>Valutazioni indipendenti

Per valutare la conformità di Azure e Office 365 alla regola SEC 17a-4(f), Microsoft ha mantenuto una società di valutazione indipendente specializzata nella gestione dei record e nella governance delle informazioni, Cohasset Associates.

### <a name="azure"></a>Azure

[L'archiviazione non modificabile per l'archiviazione BLOB](/azure/storage/blobs/storage-blob-immutable-storage) di Azure consente agli utenti di archiviare i record critici per l'azienda in uno stato DIS (Write Once Read Many). Questo stato rende i dati non cancellabili e non modificabili per un intervallo specificato dall'utente. Per la durata dell'intervallo di conservazione, i BLOB possono essere creati e letti, ma non possono essere modificati o eliminati. Queste funzionalità dell'archiviazione non modificabile di Azure possono aiutare i clienti a soddisfare i requisiti di conservazione dei record.

Microsoft ha conservato una società indipendente di valutazione di terze parti specializzata nella gestione dei record e nella governance delle informazioni per valutare l'archiviazione non modificabile per la conformità dell'archiviazione BLOB di Azure ai requisiti della regola SEC 17a-4(f). Il report risultante *[Cohasset Assessment: Microsoft Azure WORM Archiviazione](https://azure.microsoft.com/resources/azure-immutable-storage-assessment-for-sec-17a-4f-by-cohasset/)* disponibile per i clienti.

È opinione del valutatore che Archiviazione di Azure con la funzionalità di archiviazione non  modificabile per i BLOB di *Azure* e l'opzione dei criteri basati sul tempo bloccata mantiene i BLOB basati sul tempo (record) in un formato non cancellabile e non risibile e soddisfa i requisiti di archiviazione pertinenti della regola SEC 17a-4(f), della regola [FINRA 4511(c)](offering-FINRA-4511.md)e dei requisiti basati sui principi della regola [CFTC 1.31(c)-(d)](offering-cftc-1-31-us.md).

Su richiesta, Microsoft fornirà anche una lettera di *90* giorni necessaria per soddisfare i requisiti sec 17a-4(f)(2) per consentire ai clienti di comunicare all'autorità di controllo designata almeno 90 giorni prima di utilizzare supporti di archiviazione elettronici. Come indicato nelle normative, "il membro, il broker o il rivenditore deve fornire la propria rappresentazione o una dal fornitore del supporto di archiviazione o da altre terze parti con competenze appropriate che il supporto di archiviazione selezionato soddisfi le condizioni specificate in questo paragrafo (f)(2)." Per ottenere l'attestazione *Microsoft* del Archiviazione Servizi multimediali elettronico per la regola SEC 17a-4, i clienti con un piano di supporto di [Azure](https://azure.microsoft.com/support/plans/) possono creare un [ticket](https://azure.microsoft.com/support/create-ticket/) di supporto nel portale di Azure e richiedere la lettera di attestazione per la regola SEC 17a-4. In questo documento, Microsoft fornisce garanzie rilevanti per i requisiti SEC 17a-4(f)(2).

### <a name="office-365"></a>Office 365

Per i requisiti [sec 17a-4(f),](/microsoft-365/compliance/retention-regulatory-requirements#sec-17a-4f-finra-4511c-and-cftc-131c-d) Cohasset ha convalidato che Microsoft 365 include funzionalità di archiviazione che consentono ai clienti regolamentati, inclusi i broker-rivenditori, di archiviare i dati in modo che rispettino i requisiti SEC per la conservazione dei record. Le funzionalità di conservazione in Microsoft 365 consentono di conservare un'ampia gamma di dati, tra cui posta elettronica, segreteria telefonica, documenti condivisi, messaggi istantanei e dati di terze parti. In particolare, l'archiviazione in Microsoft 365 consente ai clienti di impostare criteri di conservazione della messaggistica globali o granulari per archiviare i dati per un periodo definito e oltre in un formato non riscrivibile e non cancellabile.

## <a name="audits-reports-and-certificates"></a>Controlli, report e certificati

### <a name="azure--sec-rule-17"></a>Azure & SEC Rule 17

- [Sec 17a-4(f) & CFTC 1.31 (c-d) Compliance Assessment of Archiviazione di Azure](https://azure.microsoft.com/resources/azure-immutable-storage-assessment-for-sec-17a-4f-by-cohasset/)

Microsoft *Attestation of Electronic Archiviazione Servizi multimediali* for SEC Rule 17a-4 può essere richiesto creando un ticket di [supporto](https://azure.microsoft.com/support/create-ticket/) con il supporto [di Azure](https://azure.microsoft.com/support/plans/). In questa lettera di attestazione, Microsoft fornisce garanzie per aiutare i clienti a rispettare i requisiti SEC 17a-4(f)(2).

### <a name="office-365--sec-rule-17"></a>Office 365 & SEC 17

- [Valutazione della conformità SEC 17a-4(f): & Centro sicurezza e conformità Microsoft con SharePoint, OneDrive, Teams, Exchange e Skype for Business](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=2dc92867-5f83-49d8-ad04-9e7295c9e40e&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_FAQ_and_White_Papers)

## <a name="how-to-implement"></a>Come eseguire l'implementazione

### <a name="financial-services-regulation"></a>Regolamento sui servizi finanziari

Mappa di conformità dei principali principi normativi statunitensi per il cloud computing e i servizi online Microsoft. [Altre informazioni](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=5b483567-00b0-4d86-96ae-ee887dadb61c&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_Compliance_Guides)

### <a name="risk-assessment--compliance-guide"></a>Guida alla & di valutazione dei rischi

Creare un modello di governance per la valutazione dei rischi dei servizi cloud Microsoft e la notifica dell'autorità di regolamentazione. [Altre informazioni](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=edee9b14-3661-4a16-ba83-c35caf672bd7&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_FAQ_and_White_Papers)

### <a name="financial-use-cases"></a>Casi d'uso finanziari

Usare panoramiche dei casi, esercitazioni e altre risorse per creare soluzioni di Azure per i servizi finanziari. [Altre informazioni](/azure/industry/financial/)

## <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a>Usare Microsoft Compliance Manager per valutare i rischi

[Microsoft Compliance Manager](/microsoft-365/compliance/compliance-manager) è una funzionalità nel [Centro conformità Microsoft 365](/microsoft-365/compliance/microsoft-365-compliance-center) utile per comprendere lo stato di conformità dell'organizzazione e intraprendere azioni per ridurre i rischi. Compliance Manager offre un modello premium per creare una valutazione per questa normativa. Individuare il modello nella pagina **modelli di valutazioni** in Compliance Manager. Informazioni su come [creare valutazioni in Compliance Manager](/microsoft-365/compliance/compliance-manager-assessments).

## <a name="resources"></a>Risorse

- [Documentazione sulla conformità di Azure](/azure/compliance/)
- [Azure offre un mondo di conformità](https://azure.microsoft.com/resources/azure-enables-a-world-of-compliance/)
- [Securities and Exchange Commission](https://www.sec.gov/) (SEC) [Rule 17a-4](https://www.sec.gov/rules/final/34-38245.txt)
- [Risorse per i servizi finanziari Microsoft Cloud](https://servicetrust.microsoft.com/viewpage/financialservicesoverview)
- [Programma di conformità dei servizi finanziari Microsoft Cloud](https://aka.ms/FSCP-Print)
- [Mappa di conformità dei principi normativi del cloud computing e dei servizi online Microsoft](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=5b483567-00b0-4d86-96ae-ee887dadb61c&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_Compliance_Guides)
- [Guida alla valutazione dei rischi e alla conformità per gli istituti finanziari in Microsoft Cloud](https://azure.microsoft.com/resources/risk-assessment-and-compliance-guide-for-financial-institutions-in-the-microsoft-cloud-/)
- [Casi d'uso del settore dei servizi finanziari](/azure/industry/financial/)
- [Archiviazione in Microsoft Office 365, conservazione dei dati e regola 17a-4](https://www.microsoft.com/microsoft-365/blog/2015/11/10/office-365-exchange-online-archiving-now-meets-sec-rule-17a-4-requirements/)
