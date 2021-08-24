---
title: 'Codice di condotta in materia di controllo della sicurezza informatica ISO/IEC 27017:2015 '
description: I servizi cloud di Microsoft hanno implementato questo Codice di condotta in materia di controllo della sicurezza informatica.
keywords: Microsoft 365, conformità, offerte
ms.localizationpriority: high
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
ms.openlocfilehash: efd0e2c90018c8fb32e39f83bdafa7f02bf0f230
ms.sourcegitcommit: 4c00fd65d418065d7f53216c91f455ccb3891c77
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/23/2021
ms.locfileid: "58482931"
---
# <a name="isoiec-270172015-code-of-practice-for-information-security-controls"></a>Codice di condotta in materia di controllo della sicurezza informatica ISO/IEC 27017:2015 

## <a name="iso-iec-27017-overview"></a>Panoramica ISO-IEC 27017

Il Codice di condotta ISO/IEC 27017:2015 è stato progettato come un riferimento per la selezione dei controlli di sicurezza delle informazioni dei servizi cloud quando si implementa un sistema di gestione della sicurezza delle informazioni cloud computing basato su ISO/IEC 27002:2013. Può anche essere usato dai provider di servizi cloud come documento guida per l'implementazione dei controlli di protezione comunemente accettati.

Questo standard internazionale fornisce indicazioni aggiuntive sull'implementazione specifiche del cloud basate su ISO/IEC 27002 e controlli aggiuntivi per attenuare i rischi per la sicurezza delle informazioni facendo riferimento alle clausole 5-18 in ISO/IEC 27002: 2013 per controlli, indicazioni sull'implementazione e altre informazioni. In modo specifico, questo standard fornisce indicazioni su 37 controlli in ISO/IEC 27002 e include sette nuovi controlli che non sono duplicati in ISO/IEC 27002. Questi nuovi controlli riguardano le aeree importanti elencate di seguito:

- Responsabilità e ruoli condivisi nell'ambiente di cloud computing
- Rimozione e restituzione degli asset dei clienti dei servizi cloud alla rescissione del contratto
- Protezione e separazione dell'ambiente virtuale di un cliente da quello di altri clienti
- Requisiti di hardening delle macchine virtuali per soddisfare esigenze di business
- Procedure per operazioni amministrative di un ambiente di cloud computing
- Monitoraggio di attività rilevanti da parte dei clienti in un ambiente di cloud computing
- Allineamento della gestione della sicurezza per reti virtuali e fisiche

## <a name="microsoft-and-isoiec-27017"></a>Microsoft e ISO/IEC 27017

ISO/IEC 27017 è unico nel fornire indicazioni tanto ai provider di servizi cloud quanto ai clienti di servizi cloud. Fornisce inoltre ai clienti di servizi cloud informazioni pratiche su ciò che devono aspettarsi dai provider. I clienti possono trarre vantaggio direttamente da ISO/IEC 27017 assicurandosi che comprendano le responsabilità condivise nel cloud.

## <a name="microsoft-in-scope-cloud-platforms--services"></a>Piattaforme e servizi cloud Microsoft inclusi nell'ambito

- [Azure, Azure per enti pubblici e Azure Germania](https://aka.ms/AzureCompliance)
- Microsoft Cloud App Security
- [Dynamics 365, Dynamics 365 e Dynamics 365 Germany](https://aka.ms/d365-compliance-list)
- Intune
- Microsoft Defender per endpoint
- Microsoft Graph
- Microsoft Healthcare Bot
- [Microsoft Managed Desktop](/microsoft-365/managed-desktop/intro/compliance)
- Office 365, Office 365 U.S. Government, Office 365 U.S. Government Defense e Office 365 Germany
- Servizio cloud Power Automate (in precedenza Microsoft Flow), autonomo o incluso in un piano o in una famiglia di prodotti Office 365 o Dynamics 365
- Servizio cloud PowerApps, autonomo o incluso in un piano o in una famiglia di prodotti con marchio Office 365 o Dynamics 365
- Servizio cloud Power BI, autonomo o incluso in un piano o in una famiglia di prodotti con marchio Office 365
- Power BI Embedded

## <a name="azure-dynamics-365-and-iso-270172015"></a>Azure, Dynamics 365 e ISO 27017:2015

Per altre informazioni su Azure, Dynamics 365 e la conformità dei servizi online, vedere l'[offerta Azure ISO 27017](/azure/compliance/offerings/offering-iso-27017).

## <a name="office-365-and-iso-270172015"></a>Office 365 e ISO 27017:2015

### <a name="office-365-cloud-environments"></a>Ambienti cloud di Office 365

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a>Applicabilità di Office 365 e servizi inclusi nell'ambito

Usare la tabella seguente per determinare l'applicabilità per i servizi e l'abbonamento a Office 365:

| **Applicabilità** | **Servizi inclusi nell'ambito** |
|:------------------|:----------------------|
| **Commerciale** | Access online, Azure Active Directory, Servizi di comunicazioni Azure, Compliance Manager, Customer Lockbox, Delve, Exchange Online, Exchange Online Protection, Forms, Griffin, Identity Manager, Lockbox (Torus), Microsoft Defender per Office 365, Microsoft Teams, MyAnalytics, Office 365 Advanced Compliance Add-on, Portale per i clienti Office 365, microservizi Office 365 (inclusi, a titolo esemplificativo, Kaizala, ObjectStore, Sway, PowerPoint Online Document Service, Query Annotation Service, School Data Sync, Syphon, Voce, StaffHub, eXtensible Application Program), Centro sicurezza e conformità di Office 365, Office Online, Office Pro Plus, Office Services Infrastructure, OneDrive for Business, Planner, PowerApps, Power Automate, Power BI, Project Online, Servizio di crittografia con chiave cliente, SharePoint Online, Skype for Business, Stream |
| **GCC** | Azure Active Directory, Servizi di comunicazioni Azure, Compliance Manager, Delve, Exchange Online, Forms, Microsoft Defender per Office 365, Microsoft Teams, MyAnalytics, componente aggiuntivo Office 365 Advanced Compliance, Centro sicurezza e conformità di Office 365, Office Online, Office Pro Plus, OneDrive for Business, Planner, PowerApps, Power Automate, Power BI, SharePoint Online, Skype for Business, Stream |
| **GCC High** | Azure Active Directory, Servizi di comunicazioni Azure, Exchange Online, Forms, Microsoft Defender per Office 365, Microsoft Teams, componente aggiuntivo Office 365 Advanced Compliance, Centro sicurezza e conformità di Office 365, Office Online, Office Pro Plus, OneDrive for Business, Planner, PowerApps, Power Automate, Power BI, SharePoint Online, Skype for Business |
| **DoD** | Azure Active Directory, Servizi di comunicazioni Azure, Exchange Online, Forms, Microsoft Defender per Office 365, Microsoft Teams, componente aggiuntivo Office 365 Advanced Compliance, Centro sicurezza e conformità di Office 365, Office Online, Office Pro Plus, OneDrive for Business, Planner, Power BI, SharePoint Online, Skype for Business |

### <a name="office-365-audits-reports-and-certificates"></a>Controlli, report e certificati di Office 365

I servizi cloud Microsoft vengono controllati una volta all'anno per verificare l'adeguamento al Codice di comportamento ISO/IEC 27017:2015 come parte del processo di certificazione per ISO/IEC 27001:2013.

- [Office 365: report di valutazione di controllo ISO 27001, 27018 e 27017](https://aka.ms/o365isoreport)

### <a name="frequently-asked-questions"></a>Domande frequenti

**A chi si applica lo standard?**

Questo codice di comportamento fornisce controlli e indicazioni sull'implementazione tanto ai provider di servizi cloud quanto ai clienti di servizi cloud. È strutturato in un formato simile a ISO/IEC 27002:2013.

**Dove è possibile consultare le informazioni sull'adeguamento di Microsoft per ISO/IEC 27017:2015?**

Si può scaricare il [certificato ISO/IEC 27017:2015](https://aka.ms/azureiso27017) per Azure, Intune e Power BI.

**Posso usare la conformità ISO/IEC 27017 dei servizi Microsoft nella procedura di certificazione della mia organizzazione?**

Sì. Se l'azienda desidera una certificazione per le implementazioni distribuite su qualsiasi servizio cloud aziendale nell’ambito Microsoft, è possibile utilizzare le certificazioni rilevanti di Microsoft nella valutazione dell'adeguamento. Tuttavia, hai la responsabilità di affidare l'incarico a un valutatore affinché valuti la tua implementazione in termini di adeguamento e per i controlli e i processi all'interno dell'organizzazione.

**Come si possono ottenere copie dei report di controllo applicabili?**

Il [portale di attendibilità dei servizi](https://aka.ms/stphelp) fornisce report di controllo indipendenti e di terze parti e altra documentazione correlata. È possibile usare il portale per scaricare e rivedere questa documentazione come supporto per i requisiti normativi.

### <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a>Usare Microsoft Compliance Manager per valutare i rischi

[Microsoft Compliance Manager](/microsoft-365/compliance/compliance-manager) è una funzionalità nel [Centro conformità Microsoft 365](/microsoft-365/compliance/microsoft-365-compliance-center) utile per comprendere lo stato di conformità dell'organizzazione e intraprendere azioni per ridurre i rischi. Compliance Manager offre un modello premium per creare una valutazione per questa normativa. Individuare il modello nella pagina **modelli di valutazioni** in Compliance Manager. Informazioni su come [creare valutazioni in Compliance Manager](/microsoft-365/compliance/compliance-manager-assessments).

### <a name="resources"></a>Risorse

- [Codice di comportamento ISO/IEC 27017:2015](https://www.iso.org/iso/iso_catalogue/catalogue_tc/catalogue_detail.htm?csnumber=43757)
- [Condizioni di Microsoft Online Services](https://aka.ms/Online-Services-Terms)
- [Conformità nel Centro protezione Microsoft](https://www.microsoft.com/trust-center/compliance/compliance-overview)
