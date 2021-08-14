---
title: Payment Card Industry (PCI) Data Security Standard (DSS)
description: Azure, SharePoint Online e OneDrive for Business sono conformi a Payment Card Industry Data Security Standards Level 1 versione 3.2.
keywords: Microsoft 365, conformità, offerte
localization_priority: Priority
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
ms.openlocfilehash: 78078698bbe5b69c02cb7a53d4affc4e58e8a0d3
ms.sourcegitcommit: 01938022a292c07e98041dc6ae1312a1b8c617db
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/13/2021
ms.locfileid: "58260301"
---
# <a name="payment-card-industry-pci-data-security-standard-dss"></a>Payment Card Industry (PCI) Data Security Standard (DSS)

## <a name="pci-dss-overview"></a>Panoramica PCI DSS

Il Payment Card Industry (PCI) Data Security Standards (DSS) è uno standard di sicurezza delle informazioni globale progettato per prevenire le frodi attraverso un maggiore controllo dei dati delle carte di credito. Tutte le organizzazioni, indipendentemente dalle loro dimensioni, devono aderire agli standard PCI DSS se accettano le carte di credito dei cinque principali marchi ovvero Visa, MasterCard, American Express, Discover e Japan Credit Bureau (JCB). L'adozione dello standard PCI DSS è obbligatoria per tutte le organizzazioni che archiviano, elaborano o trasmettono dati di pagamento e dei titolari di carte di credito.

## <a name="microsoft-and-pci-dss"></a>Microsoft e PCI DSS

Microsoft ha incaricato un Qualified Security Assessor (QSA) approvato di condurre una valutazione PCI DSS annuale. I revisori hanno valutato gli ambienti Microsoft Azure, Microsoft OneDrive for Business e Microsoft SharePoint Online comprese le infrastrutture, l’ambiente di sviluppo e operativo, la gestione, il supporto e i servizi applicabili. Lo standard PCI DSS definisce quattro livelli di conformità secondo il volume di transazioni. Azure, OneDrive for Business e SharePoint Online hanno ottenuto la certificazione di conformità a PCI DSS versione 3.2 al livello 1 dei provider di servizi (il volume più alto di transazioni, ovvero oltre 6 milioni all'anno).

I risultati della valutazione sono riportati in un Attestato di conformità (AoC, Attestation on Compliance), consultabile dai clienti, e in un Report di conformità (RoC, Report on Compliance) rilasciati dal QSA. Il periodo di validità della conformità inizia dopo il superamento del controllo e dopo aver ricevuto l'AoC dal QSA e termina dopo un anno a partire dalla data della firma dell'Attestato di conformità. 

I clienti che intendono sviluppare un ambiente per i titolari di carte di credito o un servizio di elaborazione carte possono sfruttare questi attestati anche per molte delle porzioni sottostanti e ridurre così le attività e i costi necessari per ottenere la loro certificazione PCI DSS.

È importante capire che lo stato di conformità allo standard PCI DSS di Azure, OneDrive for Business e SharePoint Online non si traduce automaticamente in una certificazione PCI DSS per i servizi che i clienti creano o ospitano su queste piattaforme. Il rispetto dei requisiti PCI DSS è responsabilità dei clienti.

## <a name="microsoft-in-scope-cloud-platforms--services"></a>Piattaforme e servizi cloud Microsoft inclusi nell'ambito

- Azure e Azure per enti pubblici
- Intune
- Microsoft Cloud App Security
- [Microsoft Defender per endpoint](/windows/security/threat-protection/microsoft-defender-atp/microsoft-defender-advanced-threat-protection)
- Microsoft Graph
- Office 365
- OneDrive for Business e SharePoint Online (solo Stati Uniti)
- Servizio cloud PowerApps come servizio autonomo o incluso in un piano o in una famiglia di prodotti con marchio Office 365 o Dynamics 365
- Power Automate: servizio autonomo o incluso in un piano o in una famiglia di prodotti Office 365 o Dynamics 365
- Servizio cloud Power BI, servizio autonomo o incluso in un piano o in una famiglia di prodotti Office 365

## <a name="azure-dynamics-365-and-pci-dss"></a>Azure, Dynamics 365 e PCI DSS

Per altre informazioni su Azure, Dynamics 365 e la conformità dei servizi online, vedere l'[offerta Azure PCI DSS](/azure/compliance/offerings/offering-pci-dss).

## <a name="office-365-and-pci-dss"></a>Office 365 e PCI DSS

### <a name="office-365-cloud-environments"></a>Ambienti cloud di Office 365

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a>Applicabilità di Office 365 e servizi inclusi nell'ambito

Usare la tabella seguente per determinare l'applicabilità per i servizi e l'abbonamento a Office 365:

| **Applicabilità** | **Servizi inclusi nell'ambito** |
|:------------------|:----------------------|
| **Commerciale** | OneDrive for Business (Stati Uniti), SharePoint Online |

### <a name="office-365-audit-reports-and-certificates"></a>Controlli, report e certificati di Office 365

- [Attestato di conformità PCI DSS di OneDrive for Business e SharePoint Online](https://aka.ms/spo-pci)

### <a name="frequently-asked-questions"></a>Domande frequenti

**Perché la data riportata sulla prima pagina dell'Attestato di conformità adeguamento (AoC) è ‘giugno 2018’?**

La data giugno 2018 riportata sulla prima pagina dell’attestato si riferisce a quando il modello AoC è stato pubblicato. Fare riferimento alla Sezione 2 per la data della valutazione. 

**Qual è la relazione tra PA DSS e PCI DSS?**

Il Payment Application Data Security Standard (PA DSS) è un insieme di requisiti conformi a PCI DSS che sostituisce le Payment Application Best Practices di Visa e riunisce tutti i requisiti di conformità degli altri principali istituti emittenti delle carte. Il PA DSS aiuta i fornitori di software a sviluppare applicazioni di terze parti per archiviare, elaborare o trasmettere i dati di pagamento dei titolari delle carte per l’autorizzazione o il saldo di una transazione. I venditori al dettaglio devono usare applicazioni certificate PA DSS per la conformità allo standard PCI DSS. PA DSS non si applica ad Azure.

**Cosa si intende per acquirente? Azure usa un acquirente?**

Un acquirente è una banca o un altro istituto finanziario che elabora le transazioni con carta di pagamento. Azure non offre l'elaborazione delle carte di pagamento come servizio, pertanto non si serve di un acquirente.

**A quali organizzazioni ed esercenti si applica PCI DSS?**

PCI DSS si applica a qualsiasi azienda, a prescindere dalle dimensioni o dal numero di transazioni elaborate, che accetta, trasmette o archivia i dati dei titolari di carte. Ciò significa che se un cliente effettua un pagamento all'azienda usando una carta di credito o debito, si applicano i requisiti PCI DSS. Le aziende vengono valutate rispetto ai quattro livelli disponibili in base al volume di transazioni totale elaborate in un periodo di 12 mesi. Il livello 1 è per le aziende che elaborano oltre 6 milioni di transazioni all'anno, il livello 2 da 1 milione a 6 milioni, il livello 3 da 20.000 a 1 milione e il livello 4 fino a 20.000 transazioni.

**OneDrive for Business e SharePoint Online saranno conformi a PCI DSS al fuori degli Stati Uniti?**

Al momento, OneDrive for Business e SharePoint Online sono conformi a PCI DSS solo negli Stati Uniti. Microsoft valuterà i requisiti e le tempistiche per le altre aree geografiche e informerà i clienti se il processo di adozione di PCI DSS interesserà altre aree geografiche.

**Cosa includono OneDrive for Business e SharePoint Online?**

Al momento, solo i file e i documenti caricati su OneDrive for Business e SharePoint Online saranno conformi a PCI DSS.

### <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a>Usare Microsoft Compliance Manager per valutare i rischi

[Microsoft Compliance Manager](/microsoft-365/compliance/compliance-manager) è una funzionalità nel [Centro conformità Microsoft 365](/microsoft-365/compliance/microsoft-365-compliance-center) utile per comprendere lo stato di conformità dell'organizzazione e intraprendere azioni per ridurre i rischi. Compliance Manager offre un modello premium per creare una valutazione per questa normativa. Individuare il modello nella pagina **modelli di valutazioni** in Compliance Manager. Informazioni su come [creare valutazioni in Compliance Manager](/microsoft-365/compliance/compliance-manager-assessments).

### <a name="resources"></a>Risorse

- [PCI Security Standards Council](https://www.pcisecuritystandards.org/)
- [PCI Data Security Standard](https://www.pcisecuritystandards.org/documents/PCI_DSS_v3-1.pdf)
- [PCI DSS Quick Reference Guide](https://www.pcisecuritystandards.org/documents/PCISSC%20QRG%20August%202014%20-print.pdf)
- [Conformità nel Centro protezione Microsoft](https://www.microsoft.com/trust-center/compliance/compliance-overview)
