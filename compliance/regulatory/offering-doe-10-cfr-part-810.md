---
title: US DoE 10 CFR Parte 810
description: I clienti soggetti ai requisiti di controllo dell'esportazione di US DoE 10 CFR Part 810 possono usare Azure Government.
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
ms.openlocfilehash: 1a16495f5cfe3e293910ebe84e6af566aea17621
ms.sourcegitcommit: fb379d1110a9a86c7f9bab8c484dc3f4b3dfd6f0
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/23/2021
ms.locfileid: "53087545"
---
# <a name="us-doe-10-cfr-part-810"></a>US DoE 10 CFR Parte 810

## <a name="microsoft-and-doe-10-cfr-part-810"></a>Microsoft e DoE 10 CFR Parte 810

Microsoft Azure Il governo può aiutare i clienti soggetti ai requisiti di controllo delle esportazioni del Dipartimento dell'energia degli Stati Uniti (DoE) 10 CFR Parte 810 attraverso due autorizzazioni:

- L'autorizzazione provvisoria elevata fedraMP (P-ATO) emessa dal Joint Authorization Board (JAB)
- Le autorizzazioni provvisorie di livello 4 e 5 del Department of Defense (DoD) Defense Information Systems Agency

FedRAMP offre una linea di base appropriata per garantire che Azure Government fornirà tecnologie e servizi di infrastruttura e virtualizzazione di base, come il calcolo, l'archiviazione e la rete, progettati con controlli NIST stringenti. Queste informazioni consentono di soddisfare i requisiti di separazione dei dati dei clienti e di abilitare connessioni sicure agli ambienti locali dei clienti.

Inoltre, Azure Government è un cloud di community per enti pubblici statunitensi fisicamente separato dal cloud di Azure. Fornisce ulteriori garanzie in merito ai requisiti specifici di screening in background da parte del governo degli Stati Uniti, inclusi controlli specifici che limitano l'accesso alle informazioni e ai sistemi ai cittadini statunitensi schermati tra il personale operativo di Azure.

## <a name="microsoft-in-scope-cloud-services"></a>Servizi cloud Microsoft inclusi nell'ambito

- [Azure Per enti pubblici](https://aka.ms/AzureCompliance)
- Intune

## <a name="how-to-implement"></a>Come eseguire l'implementazione

- [Standard CIP NERC & Cloud Computing](https://aka.ms/AzureNERC): Linee guida per le utilità elettriche e le entità registrate che distribuiscono carichi di lavoro in Azure o Azure Per enti pubblici.

## <a name="about-doe-10-cfr-part-810"></a>Informazioni su DoE 10 CFR Parte 810

Il regolamento di controllo delle esportazioni del Dipartimento dell'energia degli Stati Uniti (DoE) [10 CFR Parte 810](https://www.govinfo.gov/content/pkg/FR-2015-02-23/pdf/2015-03479.pdf) regola l'esportazione di tecnologia e assistenza non classificate per il settore dell'energia atomica. Contribuisce a garantire che le tecnologie atomiche esportate dagli Stati Uniti siano utilizzate solo per scopi pacifici. La parte 810 rivista (regola finale) è entrata in vigore a marzo 2015 ed è amministrata dalla [National Nuclear Security Administration.](https://www.energy.gov/nnsa/national-nuclear-security-administration) La sezione 810.6 indica che è necessaria un'autorizzazione Specifica doE sia per le disposizioni di assistenza che per i trasferimenti di tecnologie nucleari sensibili che sono "generalmente autorizzate", nonché per quelle che richiedono autorizzazioni specifiche (ad esempio per l'assistenza relativa a tecnologie nucleari sensibili come l'arricchimento e la produzione di acqua pesante).

## <a name="frequently-asked-questions"></a>Domande frequenti

**Le 10 normative CFR parte 110 della Commissione di regolamentazione statunitense sulle normative sul nucleare si applicano al governo di Azure?**

No. La [Us Nuclear Regulatory Commission](https://www.nrc.gov/) (NRC) regola l'esportazione e l'importazione di strutture e attrezzature e materiali correlati sotto [10 CFR Parte 110.](https://www.nrc.gov/reading-rm/doc-collections/cfr/part110/) [](https://www.nrc.gov/about-nrc/ip/export-import.html) L'NRC non regola la tecnologia e l'assistenza atomica relative a questi elementi che rientrano nella giurisdizione DoE. Pertanto, le normative NRC 10 CFR parte 110 non si applicano ad Azure Government.

**Come posso fornire la prova che sono conforme a DoE 10 CFR Part 810?**

Se l'organizzazione distribuisce dati ad Azure Per enti pubblici, puoi fare affidamento su Azure Government FedRAMP High P-ATO come prova che stai gestendo i dati in modo appropriato. Tuttavia, sei responsabile di ottenere l'autorizzazione DoE dei tuoi sistemi, incluso l'uso dei servizi cloud.

**Quali sono le responsabilità per classificare i dati distribuiti ad Azure Per enti pubblici?**

I clienti che distribuiscono dati ad Azure Per enti pubblici sono responsabili del proprio processo di classificazione della sicurezza. Per i dati dei clienti soggetti ai controlli di esportazione DoE, il sistema di classificazione è arricchito dai controlli UCNI (Unclassified Controlled Nuclear Information) stabiliti dalla sezione 148 [dell'US Atomic Energy Act.](https://www.epa.gov/laws-regulations/summary-atomic-energy-act)

## <a name="resources"></a>Risorse

- [Servizi cloud di Azure e controlli per l'esportazione negli Stati Uniti](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=c24c11f2-2cd4-444a-9160-19762855ad3a&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_FAQ_and_White_Papers)
- [Microsoft e FedRAMP](offering-fedramp.md)
- [Microsoft e DoD](offering-dod-disa-l2-l4-l5.md)
- [Cloud Microsoft per enti pubblici](https://www.microsoft.com/enterprise/government)
- [Conformità nel Centro protezione di Microsoft](https://www.microsoft.com/trust-center/compliance/compliance-overview)
