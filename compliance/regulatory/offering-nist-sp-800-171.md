---
title: NIST SP 800-171
description: I servizi cloud Microsoft sono conformi alle linee guida NIST SP 800-171 per proteggere le informazioni non classificate controllate (CUI) nei sistemi in informazioni non aziendali.
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
ms.openlocfilehash: da5e2621969ff9cd4ce2778fa7f075522454aef7
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/05/2021
ms.locfileid: "50121115"
---
# <a name="nist-sp-800-171"></a>NIST SP 800-171

## <a name="about-nist-sp-800-171"></a>Informazioni su NIST SP 800-171

Il National Institute of Standards and Technology (NIST) degli Stati Uniti promuove e mantiene gli standard e le linee guida di misurazione per proteggere le informazioni e i sistemi informatici delle agenzie federali. In risposta all'ordine esecutivo 13556 sulla gestione delle informazioni non classificate controllate (CUI), ha pubblicato [NIST SP 800-171](https://csrc.nist.gov/publications/detail/sp/800-171/rev-1/final), *Protecting Controlled Unclassified Information In Nonfederal Information Systems and Organizations*. Le cui sono definite come informazioni, sia digitali che fisiche, create da un governo (o da un'entità per suo conto) che, anche se non classificate, sono ancora sensibili e richiedono protezione.

NIST SP 800-171 è stato originariamente pubblicato a giugno 2015 ed è stato aggiornato più volte da allora in risposta alle minacce informatiche in evoluzione. Fornisce linee guida su come accedere, trasmettere e archiviare in modo sicuro le CUI in sistemi e organizzazioni non aziendali; i requisiti rientrano in quattro categorie principali:

- Controlli e processi per la gestione e la protezione
- Monitoraggio e gestione dei sistemi IT
- Procedure e procedure chiare per gli utenti finali
- Implementazione di misure di sicurezza tecnologiche e fisiche

## <a name="microsoft-and-nist-sp-800-171"></a>Microsoft e NIST SP 800-171

Organizzazioni di valutazione di terze parti accreditate, Kratos Secureinfo e Coalfire, hanno collaborato con Microsoft per attestare che i suoi servizi cloud nell'ambito soddisfano i criteri in NIST SP 800-171, *Protecting Controlled Unclassified Information (CUI) in Nonfederal Information Systems and Organizations*, quando elaborano CUI. L'implementazione Microsoft dei requisiti [FedRAMP](offering-fedramp.md) garantisce che i servizi cloud microsoft nell'ambito soddisfino o superino i requisiti di NIST SP 800-171 utilizzando i sistemi e le procedure già in atto.

I requisiti NIST SP 800-171 sono un sottoinsieme di NIST SP 800-53, lo standard utilizzato da FedRAMP. L'Appendice D di NIST SP 800-171 fornisce un mapping diretto dei requisiti di sicurezza cui ai controlli di sicurezza pertinenti in NIST SP 800-53, per i quali i servizi cloud nell'ambito sono già stati valutati e autorizzati nell'ambito del programma FedRAMP.

Qualsiasi entità che elabora o archivia le CUI del governo statunitense, ovvero istituti di ricerca, società di consulenza, appaltatori di produzione, deve rispettare i requisiti stringenti del NIST SP 800-171. Questa attestazione significa che i servizi cloud microsoft nell'ambito possono supportare i clienti che desiderano distribuire carichi di lavoro cui con la garanzia che Microsoft è in piena conformità. Ad esempio, tutti gli appaltatori DoD che elaborano, archiviano o trasmettono "informazioni di difesa coperte" utilizzando i servizi cloud Microsoft nell'ambito dei propri sistemi in informazioni soddisfano le clausole DFARS del Dipartimento della Difesa degli Stati Uniti che richiedono la conformità ai requisiti di sicurezza di NIST SP 800-171.

## <a name="microsoft-in-scope-cloud-services"></a>Servizi cloud Microsoft in ambito

- [Azure per enti pubblici](https://aka.ms/AzureCompliance)
- [Azure Commercial](https://azure.microsoft.com/resources/microsoft-azure-compliance-offerings/)
- [Dynamics 365 U.S. Government](https://aka.ms/d365-compliance-list)
- Intune
- [Office 365 U.S. Government Community Cloud (GCC), Office 365 GCC High e DoD](https://aka.ms/o365-compliance-framework)

## <a name="audits-reports-and-certificates"></a>Controlli, report e certificati

- [Attestazione di conformità di Azure per enti pubblici con NIST SP 800-171](https://aka.ms/Azure-NIST-800-171)

## <a name="how-to-implement"></a>Come eseguire l'implementazione

- [Esempi di Blueprint di Azure](/azure/governance/blueprints/samples/): supporto per l'implementazione di carichi di lavoro conformi ai controlli basati su NIST.

## <a name="frequently-asked-questions"></a>Domande frequenti

**Posso usare la conformità Microsoft con NIST SP 800-171 per la mia organizzazione?**

Sì. I clienti Microsoft possono utilizzare i controlli descritti nei report di organizzazioni di valutazione di terze parti indipendenti (3PAO) sugli standard FedRAMP nell'ambito delle proprie attività di analisi e qualificazione dei rischi FedRAMP e NIST. Questi report attestano l'efficacia dei controlli implementati da Microsoft nei servizi cloud nell'ambito. I clienti sono responsabili di garantire che i carichi di lavoro cui siano conformi alle linee guida NIST SP 800-171.

## <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a>Usare Microsoft Compliance Manager per valutare i rischi

[Microsoft Compliance Manager](/microsoft-365/compliance/compliance-manager) è una funzionalità nel [Centro conformità Microsoft 365](/microsoft-365/compliance/microsoft-365-compliance-center) utile per comprendere lo stato di conformità dell'organizzazione e intraprendere azioni per ridurre i rischi. Compliance Manager offre un modello premium per creare una valutazione per questa normativa. Individuare il modello nella pagina **modelli di valutazioni** in Compliance Manager. Informazioni su come [creare valutazioni in Compliance Manager](/microsoft-365/compliance/compliance-manager-assessments).

## <a name="resources"></a>Risorse

- [La certificazione Microsoft DoD soddisfa i requisiti NIST 800-171](offering-DoD-DISA-L2-L4-L5.md)
- [La conformità NIST 800-171 inizia con la documentazione sulla sicurezza informatica](https://www.nist800171.com/)
- [Microsoft Cloud Services FedRAMP Authorizations](https://marketplace.fedramp.gov/index.html?status=Compliant&sort=productName#/products)
- [Controllo e responsabilità di NIST 800-171 3.3 con Office 365 GCC High](https://info.summit7systems.com/blog/nist-3.3-audit-and-accountability-with-office-365)
- [Microsoft e NIST Cybersecurity Framework](offering-nist-csf.md)
- [Cloud Microsoft per enti pubblici](https://www.microsoft.com/enterprise/government)
- [Conformità in Microsoft Trust Center](https://www.microsoft.com/trust-center/compliance/compliance-overview)
