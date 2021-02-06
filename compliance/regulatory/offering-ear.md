---
title: Regolamento PER l'amministrazione delle esportazioni (EAR) degli Stati Uniti
description: I servizi cloud Microsoft consentono ai clienti soggetti alle normative EAR (Export Administration Regulations) degli Stati Uniti di soddisfare i propri requisiti di conformità e gestire i rischi di controllo delle esportazioni.
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
ms.openlocfilehash: fbc8166770a3ad2539264bbf76319116a2c306a9
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120005"
---
# <a name="us-export-administration-regulations-ear"></a>Regolamento PER l'amministrazione delle esportazioni (EAR) degli Stati Uniti

## <a name="about-the-ear"></a>Informazioni sull'EAR

Il Dipartimento del Commercio degli Stati Uniti applica le normative EAR (Export Administration Regulations) attraverso il [Bureau of Industry and Security (BIS).](https://www.bis.doc.gov/) L'EAR governa e impone controlli sull'esportazione e la riesportare della maggior parte dei beni commerciali, del software e della tecnologia, inclusi gli elementi "dual use" che possono essere utilizzati sia per scopi commerciali che per scopi militari e per determinati elementi di difesa.

La guida BIS indica che, quando i dati o il software vengono caricati nel cloud o trasferiti tra nodi utente, il cliente, non il provider cloud, è l'"esportatore" che ha la responsabilità di garantire che i trasferimenti, l'archiviazione e l'accesso a questi dati o software siano conforme all'EAR.

In base al  [BIS,](https://www.bis.doc.gov/index.php/documents/regulation-docs/412-part-734-scope-of-the-export-administration-regulations/file)l'esportazione si riferisce al trasferimento di dati tecnici o tecnologici protetti a una destinazione esterna o al suo rilascio a una persona estranea negli Stati Uniti (detto anche esportazione *considerata*). L'EAR governa a livello generale:

- Esporta dagli Stati Uniti.
- Riesportare o ritrasferire gli elementi di origine negli Stati  Uniti e alcuni elementi di origine esterna con più di una parte ridotta al minimo del contenuto di origine statunitense.
- Trasferimenti o divulgazioni a persone di altri paesi.

Gli elementi soggetti all'EAR sono disponibili nell'elenco CCL (Commerce Control List) in cui a ogni elemento è assegnato un codice [ECCN (Export Control Classification Number) univoco.](https://www.bis.doc.gov/index.php/licensing/commerce-control-list-classification/export-control-classification-number-eccn) Gli elementi non elencati nel CCL sono designati come EAR99 e la maggior parte dei prodotti commerciali EAR99 non richiederà l'esportazione di una licenza. Tuttavia, a seconda della destinazione, dell'utente finale o dell'uso finale dell'elemento, anche un elemento EAR99 potrebbe richiedere una licenza di esportazione BIS.

La regola [finale,](https://www.federalregister.gov/documents/2016/06/03/2016-12734/revisions-to-definitions-in-the-export-administration-regulations)pubblicata a giugno 2016, ha chiarito che i requisiti di licenza EAR non si applicherebbero anche alla trasmissione e all'archiviazione di software e dati tecnici non classificati se fossero crittografati end-to-end utilizzando moduli crittografici convalidati da FIPS 140-2 e non fossero archiviati intenzionalmente in un paese esecutivo esecutivo o nella Federazione Russa.

## <a name="microsoft-and-the-ear"></a>Microsoft e ear

Le tecnologie, i prodotti e i servizi Microsoft sono soggetti alle normative EAR (Export Administration Regulations) degli Stati Uniti. Anche se non esiste alcuna certificazione di conformità per EAR, Microsoft Azure, Microsoft Azure per enti pubblici e ambienti Microsoft Office 365 Government (GCCHigh e DoD) offrono funzionalità e strumenti importanti per aiutare i clienti idonei soggetti all'EAR a gestire i rischi di controllo dell'esportazione e soddisfare i loro requisiti di conformità.

Il Dipartimento del commercio degli Stati Uniti, che applica l'EAR, ha assunto la posizione che i clienti, non i provider di servizi cloud come Microsoft, sono considerati esportatori dei propri dati dei clienti. Anche se la maggior parte dei dati dei clienti non è considerata "tecnologia" o "dati tecnici" soggetti ai controlli di esportazione EAR, i servizi cloud Microsoft nell'ambito sono strutturati per aiutare i clienti a gestire e ridurre in modo significativo i potenziali rischi per il controllo dell'esportazione che devono affrontare. Microsoft in genere, ma non esclusivamente, consiglia l'uso dei servizi cloud per enti pubblici per i clienti idonei. Con una pianificazione appropriata, i clienti possono utilizzare gli strumenti seguenti e le proprie procedure interne per garantire la completa conformità ai controlli per l'esportazione negli Stati Uniti.

- **Controlli sulla posizione dei dati.** I clienti hanno visibilità sulla posizione di archiviazione dei dati e l'accesso a strumenti affidabili per limitare lo spazio di archiviazione. Possono pertanto garantire che i loro dati siano archiviati negli Stati Uniti e ridurre al minimo il trasferimento di dati tecnici o tecnologici controllati al di fuori degli Stati Uniti. Inoltre, i dati dei clienti non vengono archiviati in una posizione non conforme, coerente con i divieti EAR in cui i dati sono "archiviati intenzionalmente": nessun datacenter di Azure si trova in uno dei 25 paesi del Gruppo D:5 o nella Federazione Russa.
- **Crittografia end-to-end.** Sfruttando l'isola sicura di crittografia end-to-end per le posizioni di archiviazione fisiche specificate nell'EAR, i servizi cloud microsoft nell'ambito offrono funzionalità di crittografia che consentono di proteggersi dai rischi di controllo dell'esportazione. Offrono inoltre ai clienti un'ampia [gamma](https://aka.ms/Azure-Encryption-Overview) di opzioni per crittografare i dati in transito e in pausa e la flessibilità di scegliere tra le opzioni di crittografia.
- **Strumenti e protocolli per impedire l'esportazione non autorizzata.** L'uso della crittografia aiuta anche a proteggersi da una potenziale esportazione (o riesportare) nell'EAR, perché anche se una persona non statunitense ha accesso ai dati crittografati, non viene rivelata alcuna cosa se non riesce a leggere o comprendere i dati mentre sono crittografati; pertanto non esiste alcun "rilascio" di dati controllati.

## <a name="microsoft-in-scope-cloud-services"></a>Servizi cloud Microsoft in ambito

- [Azure e Azure per enti pubblici](https://aka.ms/AzureCompliance)
- [Office 365 Government (GCC-High e DoD)](https://aka.ms/Office-365-Export-Controls)
- Intune

## <a name="how-to-implement"></a>Come eseguire l'implementazione

Panoramica dei controlli e delle indicazioni per l'esportazione negli Stati Uniti per i clienti che valutano i propri obblighi ai sensi dell'EAR.

- [Azure](https://aka.ms/Azure-Export-Controls)
- [Office 365](https://aka.ms/Office-365-Export-Controls)

## <a name="frequently-asked-questions"></a>Domande frequenti

**Cosa devo fare per rispettare i controlli di esportazione quando si usano i servizi cloud Microsoft?**

Sotto l'EAR, quando i dati vengono caricati in un server cloud come il cloud Microsoft, il cliente proprietario dei dati, non il provider di servizi cloud, viene considerato l'esportatore. Per questo motivo, il proprietario dei dati, ovvero il cliente Microsoft, deve valutare attentamente in che modo l'uso del cloud Microsoft può implicare controlli per l'esportazione negli Stati Uniti e determinare se i dati che desiderano usare o archiviare potrebbero essere soggetti ai controlli EAR e, in tal caso, quali controlli si applicano. Ulteriori informazioni su come i servizi cloud [di Azure](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=c24c11f2-2cd4-444a-9160-19762855ad3a&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_FAQ_and_White_Papers) e Office [365](https://query.prod.cms.rt.microsoft.com/cms/api/am/binary/RE1s5kI) possono aiutare i clienti a garantire la completa conformità ai controlli di esportazione negli Stati Uniti.

**Le tecnologie, i prodotti e i servizi Microsoft sono soggetti all'EAR?**

La maggior parte delle tecnologie, dei prodotti e dei servizi Microsoft è:

- Non sono soggetti all'EAR e pertanto non sono presenti nell'elenco di controllo commerce e non dispongono di ECCN;
- Oppure sono idonei per l'autoclassificazione da parte di Microsoft di EAR99 o 5D992 Mass Market e possono essere esportati in paesi senza licenza senza licenza richiesta (NLR).

Detto questo, ad alcuni prodotti Microsoft è stato assegnato un ECCN che potrebbe richiedere o meno una licenza. Consultare l'EAR o il consulente legale per determinare il tipo di licenza appropriato e i paesi idonei per l'esportazione.

**Qual è la differenza tra EAR e International Traffic in Arms Regulations (ITAR)?**

I principali controlli per l'esportazione negli Stati Uniti con l'applicazione più ampia sono l'EAR, amministrato dal Dipartimento del Commercio degli Stati Uniti. L'EAR è applicabile a elementi con doppio uso con applicazioni commerciali e militari e a elementi con applicazioni puramente commerciali.

Gli Stati Uniti hanno anche normative di controllo delle esportazioni separate e più specializzate, come l'ITAR, che regola gli elementi e la tecnologia più sensibili. Amministrati dal Dipartimento di Stato degli Stati Uniti, impongono controlli sull'esportazione, l'importazione temporanea, la riesportare e il trasferimento di molti elementi militari, di difesa e di intelligence (noti anche come "articoli di difesa"), inclusi i dati tecnici correlati.

## <a name="resources"></a>Risorse

- [Esportazione di prodotti Microsoft: panoramica](https://www.microsoft.com/exporting/overview.aspx)
- [Esportazione di prodotti Microsoft: domande frequenti](https://www.microsoft.com/exporting/faq.aspx)
- [Esportazione di prodotti Microsoft: ricerca di prodotti](https://www.microsoft.com/exporting/exporting-information.aspx)
- [Restrizioni per l'esportazione della crittografia](/windows/uwp/security/export-restrictions-on-cryptography)
- [Microsoft e FIPS 140-2](offering-fips-140-2.md)
- [Microsoft e ITAR](offering-itar.md)
- [Conformità nel Centro protezione Microsoft](https://www.microsoft.com/trust-center/compliance/compliance-overview)
