---
title: Securities and Exchange Commission - Regulation Systems Compliance and Integrity (SCI)
description: Le regole SCI si applicano alle entità SCI, che includono organizzazioni di auto-regolamentazione (SRO) come scambi di azioni e opzioni, agenzie di cancellazione registrate e sistemi di negoziazione alternativi (ATS).
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
ms.openlocfilehash: 049f0516598209411b0c5ca47eea39140762fd3d
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/05/2021
ms.locfileid: "50119875"
---
# <a name="securities-and-exchange-commission-regulation-systems-compliance-and-integrity-sci"></a>Securities and Exchange Commission: Regulation Systems Compliance and Integrity (SCI)

## <a name="about-regulation-sci"></a>Informazioni sul regolamento SCI

La SEC (Us Securities and Exchange Commission) è un'agenzia indipendente del governo federale degli Stati Uniti e il principale sovrinsecatore e regolatore dei mercati dei titoli statunitensi. Essa gestisce l'autorità di imposizione sulle leggi federali in materia di titoli, propone nuove regole in materia di titoli e supervisiona la normativa di mercato del settore dei titoli.

Nel novembre 2014, la SEC ha adottato [la REGULATION Systems Compliance and Integrity (SCI) (e](https://www.sec.gov/rules/final/2014/34-73639.pdf) Form SCI per la segnalazione degli eventi SCI) per rafforzare l'infrastruttura tecnologica nei mercati dei titoli statunitensi. La normativa è progettata per ridurre la frequenza di interruzioni del sistema, migliorare la resilienza in caso di incidenti di questo tipo e aumentare la supervisione sec della tecnologia del mercato dei titoli e l'applicazione delle normative.

Le regole SCI si applicano alle entità SCI, che includono organizzazioni di auto-regolamentazione (SRO) come scambi di azioni e opzioni, agenzie di cancellazione registrate e sistemi di negoziazione alternativi (ATS). Le regole regolano principalmente i sistemi che supportano direttamente le principali funzioni del mercato dei titoli: negoziazione, autorizzazione e liquidazione, routing degli ordini, dati di mercato, regolamentazione del mercato e sorveglianza del mercato.

## <a name="microsoft-and-sec-regulation-sci"></a>Microsoft e SEC Regulation SCI

La SEC (Us Securities and Exchange Commission) ha adottato il regolamento SCI per rafforzare l'infrastruttura tecnologica delle organizzazioni finanziarie che operano e supportano i mercati dei titoli statunitensi. Sotto la supervisione di SEC, i suoi requisiti sono progettati per garantire che questi sistemi siano a disponibilità elevata, resilienza forte e bassa latenza (volume elevato di messaggi con poco ritardo).

Per aiutare i clienti dei servizi finanziari statunitensi che devono rispettare questa normativa, Microsoft ha pubblicato la Guida all'implementazione del cloud di conformità e integrità dei sistemi della SEC [di Microsoft Azure.](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=a69ce0c1-7b7e-44e9-9143-867241e6b2f9&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_FAQ_and_White_Papers) Le indicazioni contenute in questo documento:

- Fornisce una panoramica delle funzionalità generali di Azure che supportano resilienza, disponibilità elevata e bassa latenza.
- Chiari le aree di controllo e gli aspetti normativi degli indirizzi di Azure. Questo mapping punto per punto delle funzionalità e dei servizi di Azure ai requisiti SCI misura la conformità di Azure rispetto al framework normativo. Consente inoltre ai clienti di capire dove possono spostare le responsabilità di sicurezza in Azure che avevano completamente di proprietà quando gestivano in locale. Queste funzionalità sono supportate dalle promesse che Microsoft fa nei contratti di servizio di Azure.
- Specifica ogni requisito SCI del regolamento che è responsabilità del cliente affrontare e offre documentazione e servizi di Azure per aiutarli a risolvere queste responsabilità.

In questo documento viene fornito un elenco di controllo completo delle aree critiche della normativa SCI. Questo elenco di controllo consente alle organizzazioni finanziarie di comprendere in che modo possono adottare Azure per garantire agli enti normativi, ai clienti e ai dirigenti la conformità ai requisiti normativi applicabili.

## <a name="microsoft-in-scope-cloud-services"></a>Servizi cloud Microsoft in ambito

- [Azure](https://aka.ms/AzureCompliance)

## <a name="how-to-implement"></a>Come eseguire l'implementazione

- [Guida all'implementazione della normativa SCI:](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=a69ce0c1-7b7e-44e9-9143-867241e6b2f9&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_FAQ_and_White_Papers)mappa le funzionalità di Azure rispetto alla normativa e illustra in dettaglio la responsabilità condivisa per la conformità.
- [Progettazione di applicazioni Azure affidabili:](/azure/architecture/resiliency/)breve panoramica su come creare affidabilità in ogni passaggio della progettazione delle applicazioni di Azure.
- [Progettazione di applicazioni a disponibilità elevata:](/azure/storage/common/storage-designing-ha-apps-with-ragrs)in che modo gli sviluppatori possono garantire la disponibilità elevata delle applicazioni di archiviazione di Azure.
- [Guida alla valutazione dei rischi e alla conformità](https://aka.ms/RiskGovernanceGuide): creare un modello di governance per la valutazione dei rischi dei servizi cloud Microsoft e la notifica all'organismo di regolamentazione.

## <a name="frequently-asked-questions"></a>Domande frequenti

**Cosa significa responsabilità condivisa quando si usa la tecnologia cloud?**

Quando gli ambienti di elaborazione passano dai datacenter locali a quelli nel cloud, anche la responsabilità della sicurezza cambia: il provider di servizi cloud (CSP) e il cliente ora condividono tale responsabilità. Per ogni applicazione e soluzione, la quantità di tale responsabilità ricade sul cliente e su quanto dipende dal modello azure distribuito da un cliente, ovvero IaaS, SaaS o PaaS. È compito del cliente comprendere in che misura è responsabilità dell'implementazione dei controlli di sicurezza necessari. Tuttavia, Microsoft fornisce indicazioni per aiutare i clienti a esplorare questa dinamica complessa. Per ulteriori informazioni, vedere [Shared Responsibilities for Cloud Computing.](https://gallery.technet.microsoft.com/Shared-Responsibilities-81d0ff91)

**Quali istituti finanziari possono sfruttare Azure per soddisfare i requisiti della normativa SCI?**

Le organizzazioni finanziarie, o entità SCI, soggette a questa normativa possono distribuire Azure. La SEC afferma che il suo regolamento si applica alle "organizzazioni di auto-regolamentazione (SRO), inclusi scambi di azioni e opzioni, agenzie di cancellazione registrate, FINRA e MSRB, sistemi di negoziazione alternativi (ATS), che commercializzano titoli NMS e non NMS che superano soglie di volume specificate, divulgatori di dati di mercato consolidati (responsabili del processore del piano) e determinate agenzie esenti da cancellazione".

## <a name="resources"></a>Risorse

- [Risposte sec alle domande frequenti relative al regolamento SCI](https://www.sec.gov/divisions/marketreg/regulation-sci-faq.shtml)
- [Continuità aziendale e ripristino di emergenza (BCDR): aree geografiche accoppiate di Azure](/azure/best-practices-availability-paired-regions)
- [Mappa di conformità dei principi normativi e dei criteri di cloud computing Microsoft Online Services](https://aka.ms/FinServ-Guide-US)
- [Cloud Financial Services Compliance Program di Microsoft](https://aka.ms/FSCP-Print)
- [Conformità dei servizi finanziari in Azure](https://aka.ms/FinServ-Compliance-Azure)
- [Servizi finanziari Microsoft](https://aka.ms/FinServ-Compliance)
- [Regola Microsoft e SEC 17a-4](offering-SEC-17a-4.md)
- [Conformità nel Centro protezione Microsoft](https://www.microsoft.com/trust-center/compliance/compliance-overview)
