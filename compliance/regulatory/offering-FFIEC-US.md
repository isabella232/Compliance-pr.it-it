---
title: Federal Financial Institutions Examination Council (FFIEC)
description: Microsoft aiuta i clienti dei servizi finanziari a rispettare i requisiti di controllo del Federal Financial Institutions Examination Council (FFIEC).
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
ms.openlocfilehash: 1830d0d61fe0787d7f8e8034af2e4ca64bdb0bc8
ms.sourcegitcommit: 01938022a292c07e98041dc6ae1312a1b8c617db
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/13/2021
ms.locfileid: "58261024"
---
# <a name="federal-financial-institutions-examination-council-ffiec"></a>Federal Financial Institutions Examination Council (FFIEC)

## <a name="ffiec-overview"></a>Panoramica di FFIEC

Il Federal Financial Institutions Examination Council (FFIEC) è un organismo di intermediazione formale costituito da cinque autorità di regolamentazione bancarie responsabili degli esami del governo federale statunitense degli istituti finanziari negli Stati Uniti. Il manuale FFIEC Examiner Education Office pubblica manuali di esame IT destinati agli esaminatori sul campo delle agenzie membro FFIEC.

Il [manuale FFIEC Audit IT Examination Contiene](https://ithandbook.ffiec.gov/it-booklets/audit.aspx) indicazioni per questi esaminatori per valutare la qualità e l'efficacia dei programmi di controllo IT di istituti finanziari e TSP. In particolare, include la menzione dei rapporti di attestazione SOC 1, SOC 2 e SOC 3 dell'American Institute of Certified Public Accountants (AICPA) come esempi di report di controllo indipendenti. Tuttavia, la FFIEC consiglia agli istituti finanziari di non basarsi esclusivamente sulle informazioni contenute in questi report, ma anche di utilizzare le procedure di verifica e monitoraggio descritte in dettaglio nel manuale [FFIEC Outsourcing Technology Services IT Examination Handbook](https://ithandbook.ffiec.gov/it-booklets/outsourcing-technology-services.aspx).

## <a name="microsoft-and-ffiec"></a>Microsoft e FFIEC

Microsoft Azure, Microsoft Power BI e Microsoft Office 365 sono stati creati per soddisfare i requisiti stringenti della fornitura di servizi cloud per gli istituti di servizi finanziari. Come parte del supporto, offriamo indicazioni per la conformità ai requisiti di controllo FFIEC per le tecnologie dell'informazione e la possibilità di usare le attestazioni SOC di Azure quando si rispettano gli obblighi di conformità FFIEC.

Per aiutare i clienti delle istituzioni finanziarie a soddisfare i requisiti di conformità FFIEC con Azure, Microsoft ha sviluppato il blueprint di sicurezza e conformità di Azure per i carichi di lavoro dei servizi regolamentati [FFIEC.](https://servicetrust.microsoft.com/ViewPage/FFIECBlueprint) Offre indicazioni sull'uso dei servizi cloud di Azure e considerazioni per la conformità dei clienti ai requisiti FFIEC e alle linee guida per la valutazione dei rischi.

Per soddisfare ulteriormente i requisiti FFIEC, i servizi cloud Microsoft forniscono report di [attestazione SOC](offering-SOC.md) prodotti da una società CPA indipendente. Ad esempio, l'attestazione SOC 1 Tipo 2 si basa sullo standard AICPA SSAE 18 (vedere at-C Sezione 105) che ha sostituito SAS 70 ed è appropriato per la segnalazione di determinati controlli per la creazione di report finanziari. I rapporti SOC includono il parere del revisore sull'efficacia dei controlli Microsoft nel raggiungimento degli obiettivi di controllo correlati durante il periodo di monitoraggio specificato. Gli istituti finanziari possono usare questo controllo formale per adempimento degli obblighi di conformità specifici FFIEC per le risorse distribuite in Azure, Power BI e Office 365.

## <a name="microsoft-in-scope-cloud-platforms--services"></a>Piattaforme e servizi cloud Microsoft inclusi nell'ambito

- Azure
- Intune
- Office 365, Office 365 U.S. Government
- Servizio cloud Power BI, servizio autonomo o incluso in un piano o in una famiglia di prodotti Office 365

## <a name="azure-dynamics-365-and-ffiec"></a>Azure, Dynamics 365 e FFIEC

Per altre informazioni sulla conformità di Azure, Dynamics 365 e altri servizi online, vedi l'offerta [FFIEC di Azure.](/azure/compliance/offerings/offering-ffiec-us)

## <a name="office-365-and-ffiec"></a>Office 365 e FFIEC

### <a name="office-365-cloud-environments"></a>Ambienti cloud di Office 365

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a>Applicabilità di Office 365 e servizi inclusi nell'ambito

Usare la tabella seguente per determinare l'applicabilità per i servizi e l'abbonamento a Office 365:

| **Applicabilità** | **Servizi inclusi nell'ambito** |
|:------------------|:----------------------|
| **Commerciale** | Azure Active Directory, Azure Information Protection, Bookings, Compliance Manager, Delve, Exchange Online, Exchange Online Protection, Forms, Kaizala, Microsoft Analytics, Microsoft Booking, Microsoft Defender per Office 365, Microsoft Graph, Microsoft Teams, Microsoft To-Do per il Web, MyAnalytics, componente aggiuntivo Conformità avanzata di Office 365, Office 365 Cloud App Security, Gruppi di Office 365, Centro sicurezza e conformità di Office 365, Video di Office 365, Office Online, Office Pro Plus, OneDrive for Business, Planner, PowerApps, Power Automate, Power BI, Microsoft SharePoint Online, Skype for Business, StaffHub, Microsoft Stream, Sway, Yammer Enterprise |
| **GCC** | Azure Active Directory, Compliance Manager, Delve, Exchange Online, Forms, Microsoft Defender per Office 365, Microsoft Teams, MyAnalytics, componente aggiuntivo Office 365 Advanced Compliance, Centro sicurezza e conformità di Office 365, Office Online, Office Pro Plus, OneDrive for Business, Planner, PowerApps, Power Automate, Power BI, SharePoint Online, Skype for Business, Stream |

### <a name="office-365-audits-reports-and-certificates"></a>Controlli, report e certificati di Office 365

Vedi i Office 365 di attestazione SOC.

### <a name="frequently-asked-questions"></a>Domande frequenti

**Posso usare la conformità Microsoft agli standard SOC per soddisfare gli obblighi di conformità FFIEC per il mio istituto?**

Per soddisfare questi obblighi, Microsoft fornisce le specifiche sulla conformità agli standard SOC come descritto in precedenza. Tuttavia, in ultima analisi, sta a te determinare se i nostri servizi sono conformi alle leggi e alle normative specifiche applicabili al tuo istituto. L'FFIEC consiglia inoltre che "gli utenti dei rapporti di controllo o delle revisioni non devono basarsi esclusivamente sulle informazioni contenute nel report per verificare l'ambiente di controllo interno del provider di servizi condivisi. Devono utilizzare altre procedure di verifica e [](https://ithandbook.ffiec.gov/it-booklets/outsourcing-technology-services.aspx) monitoraggio, come descritto più in modo più approfondito nel Manuale sulla tecnologia di esternalizzazione del manuale di esame IT FFIEC."

### <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a>Usare Microsoft Compliance Manager per valutare i rischi

[Microsoft Compliance Manager](/microsoft-365/compliance/compliance-manager) è una funzionalità nel [Centro conformità Microsoft 365](/microsoft-365/compliance/microsoft-365-compliance-center) utile per comprendere lo stato di conformità dell'organizzazione e intraprendere azioni per ridurre i rischi. Compliance Manager offre un modello premium per creare una valutazione per questa normativa. Individuare il modello nella pagina **modelli di valutazioni** in Compliance Manager. Informazioni su come [creare valutazioni in Compliance Manager](/microsoft-365/compliance/compliance-manager-assessments).

### <a name="resources"></a>Risorse

- [Federal Financial Institutions Examination Council (FFIEC)](https://www.ffiec.gov/)
- [Mappa di conformità del cloud computing e dei principi normativi negli Stati Uniti](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=5b483567-00b0-4d86-96ae-ee887dadb61c&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_Compliance_Guides)
- [Manuale di esame IT di controllo FFIEC](https://ithandbook.ffiec.gov/it-booklets/audit.aspx)
- [Manuale di esame IT FFIEC Outsourcing Technology Services](https://ithandbook.ffiec.gov/it-booklets/outsourcing-technology-services.aspx)

### <a name="other-microsoft-resources-for-financial-services"></a>Altre risorse Microsoft per i servizi finanziari

- [Programma di conformità dei servizi finanziari Microsoft](https://www.microsoft.com/download/details.aspx?id=55332)
- [Conformità dei servizi finanziari in Azure](https://azure.microsoft.com/resources/videos/azurecon-2015-financial-services-compliance-in-azure/)
- [Servizi finanziari e servizi cloud aziendali di Microsoft](https://servicetrust.microsoft.com/viewpage/financialservicesoverview)
- [Responsabilità condivise per il cloud computing](https://aka.ms/sharedresponsibility)
- [Conformità nel Centro protezione Microsoft](https://www.microsoft.com/trust-center/compliance/compliance-overview)
