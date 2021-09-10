---
title: Federal Financial Institutions Examination Council (FFIEC)
description: Microsoft aiuta i clienti dei servizi finanziari a rispettare i requisiti di controllo del Federal Financial Institutions Examination Council (FFIEC).
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
ms.openlocfilehash: 7cdc024d19ce0753d3d0c0e5cf45b6276939d6f2
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2021
ms.locfileid: "58947963"
---
# <a name="federal-financial-institutions-examination-council-ffiec"></a>Federal Financial Institutions Examination Council (FFIEC)

## <a name="ffiec-overview"></a>Panoramica di FFIEC

Il Federal Financial Institutions Examination Council (FFIEC) è un organismo di intermediazione formale costituito da cinque autorità di regolamentazione bancarie responsabili degli esami del governo federale statunitense degli istituti finanziari negli Stati Uniti. Il FFIEC Examiner Education Office pubblica manuali di esame IT destinati agli esaminatori sul campo delle agenzie membro FFIEC.

Il [manuale FFIEC Audit IT Examination Contiene](https://ithandbook.ffiec.gov/it-booklets/audit.aspx) indicazioni per questi esaminatori per valutare la qualità e l'efficacia dei programmi di controllo IT di istituti finanziari e TSP. In particolare, include la menzione dei rapporti di attestazione SOC 1, SOC 2 e SOC 3 dell'American Institute of Certified Public Accountants (AICPA) come esempi di report di controllo indipendenti. Tuttavia, la FFIEC consiglia agli istituti finanziari di non basarsi esclusivamente sulle informazioni contenute in questi report, ma anche di utilizzare le procedure di verifica e monitoraggio descritte in dettaglio nel manuale [FFIEC Outsourcing Technology Services IT Examination Handbook](https://ithandbook.ffiec.gov/it-booklets/outsourcing-technology-services.aspx).

## <a name="microsoft-and-ffiec"></a>Microsoft e FFIEC

Microsoft Azure, Microsoft Power BI e Microsoft Office 365 sono stati creati per soddisfare i requisiti stringenti della fornitura di servizi cloud per gli istituti di servizi finanziari. Azure fornisce agli istituti finanziari report di attestazione SOC 1 Tipo 2, SOC 2 Tipo 2 e SOC 3 prodotti da una società di controllo indipendente per aiutare i clienti a rispettare i propri obblighi di conformità FFIEC. Ad esempio, [l'attestazione SOC 1 Di tipo 2](./offering-soc-1.md) viene eseguita in:

- SSAE n. 18, standard di attestazione: chiarimento e codifica, che include la sezione AT-C 320, *Report sull'esame dei controlli in un'organizzazione di servizi rilevante per il controllo interno delle entità utente sui report finanziari* (AICPA, standard professionali).
- Report SOC 1 sull'esame dei controlli in un'organizzazione di servizi rilevante per il controllo interno delle entità utente sui report finanziari (Guida AICPA).

Lo standard AICPA SSAE 18 ha sostituito SAS 70 ed è appropriato per la creazione di report sui controlli in un'organizzazione di servizi rilevante per i controlli interni delle entità utente sui report finanziari. Questo è il controllo formale che gli istituti finanziari possono sfruttare per le revisioni di terze parti dei provider di servizi tecnologici nel perseguire i propri obblighi di conformità specifici FFIEC per le risorse distribuite in Azure. Include il parere del revisore sull'efficacia del controllo per raggiungere gli obiettivi di controllo correlati durante il periodo di monitoraggio specificato.

Azure ha inoltre sviluppato uno strumento di diagnostica della sicurezza cloud basato su Excel per accelerare una valutazione dei rischi che un istituto finanziario potrebbe voler eseguire in relazione ai servizi di Azure. Lo strumento si basa su un foglio di calcolo con 19 domini distinti che identificano i requisiti definiti nelle normative pertinenti e relative ai servizi finanziari, tra cui i manuali di esame IT FFIEC.  Lo strumento di valutazione dei rischi è precompilato con spiegazioni su come Azure è conforme ai requisiti applicabili ai provider di servizi cloud e può aiutare i clienti a soddisfare i propri requisiti di conformità FFIEC.

Disponibile anche per i clienti è il complementare della cartella di lavoro per la diagnostica della sicurezza cloud di Azure FFIEC, che offre indicazioni sull'uso dei servizi di Azure e considerazioni per la conformità dei clienti ai requisiti FFIEC

## <a name="microsoft-in-scope-cloud-platforms--services"></a>Piattaforme e servizi cloud Microsoft inclusi nell'ambito

- Azure
- Intune
- Office 365, Office 365 U.S. Government
- Servizio cloud Power BI, servizio autonomo o incluso in un piano o in una famiglia di prodotti Office 365

## <a name="azure-guidance-documents"></a>Documenti di guida di Azure

Per assistere gli istituti finanziari soggetti alla supervisione FFIEC con l'adozione del cloud, Microsoft ha pubblicato i seguenti documenti di guida che possono essere scaricati dalla sezione Service Trust Portal [Data Protection Resources - Compliance Guides:](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3)

- Azure - Strumento di diagnostica della sicurezza cloud
- Azure - Complementare cartella di lavoro per la diagnostica della sicurezza cloud FFIEC

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

## <a name="resources"></a>Risorse

- [Federal Financial Institutions Examination Council (FFIEC)](https://www.ffiec.gov/)
- [Mappa di conformità del cloud computing e dei principi normativi negli Stati Uniti](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=5b483567-00b0-4d86-96ae-ee887dadb61c&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_Compliance_Guides)
- [Manuale di esame IT di controllo FFIEC](https://ithandbook.ffiec.gov/it-booklets/audit.aspx)
- [Manuale di esame IT FFIEC Outsourcing Technology Services](https://ithandbook.ffiec.gov/it-booklets/outsourcing-technology-services.aspx)

## <a name="other-microsoft-resources-for-financial-services"></a>Ulteriori risorse Microsoft per i servizi finanziari

- [Documentazione sulla conformità di Azure](/azure/compliance/)
- [Azure offre un mondo di conformità](https://azure.microsoft.com/resources/azure-enables-a-world-of-compliance/)
- [Risorse per i servizi finanziari Microsoft Cloud](https://servicetrust.microsoft.com/viewpage/financialservicesoverview)
- [Programma di conformità dei servizi finanziari Microsoft Cloud](https://aka.ms/FSCP-Print)
- [Guida alla valutazione dei rischi e alla conformità per gli istituti finanziari in Microsoft Cloud](https://azure.microsoft.com/resources/risk-assessment-and-compliance-guide-for-financial-institutions-in-the-microsoft-cloud-/)
- [Casi d'uso del settore dei servizi finanziari](/azure/industry/financial/)
