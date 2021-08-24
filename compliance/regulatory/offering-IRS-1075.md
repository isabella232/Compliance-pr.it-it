---
title: Us Internal Revenue Service Publication 1075
description: Microsoft dispone di controlli che soddisfano i requisiti della pubblicazione 1075 del servizio dei ricavi interni degli Stati Uniti.
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
ms.openlocfilehash: 3212e28e055629b3f2894e7887ffac03e94b9e3a
ms.sourcegitcommit: 4c00fd65d418065d7f53216c91f455ccb3891c77
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/23/2021
ms.locfileid: "58481038"
---
# <a name="us-internal-revenue-service-publication-1075"></a>Us Internal Revenue Service Publication 1075

## <a name="us-internal-revenue-service-publication-1075-overview"></a>Panoramica della pubblicazione 1075 del servizio dei ricavi interni degli Stati Uniti

Internal Revenue Service Publication 1075 (IRS 1075) fornisce indicazioni per le agenzie governative statunitensi e i loro agenti che accedono alle informazioni fiscali federali (FTI) per garantire che utilizzino criteri, procedure e controlli per proteggere la riservatezza. IRS 1075 mira a ridurre al minimo il rischio di perdita, violazione o uso improprio di FTI tenuto da agenzie governative esterne. Ad esempio, un Dipartimento delle entrate dello Stato che elabora la FTI nelle dichiarazione dei redditi per i residenti o le agenzie di servizi sanitari che accedono a FTI, deve disporre di programmi per salvaguardare tali informazioni.  
  
Per proteggere FTI, IRS 1075 prescrive i controlli di sicurezza e privacy per i servizi di applicazioni, piattaforme e datacenter. Ad esempio, assegna la priorità alla sicurezza delle attività del datacenter, ad esempio la corretta gestione di FTI, e la supervisione degli appaltatori del datacenter per limitare l'immissione. Per garantire che le agenzie governative che ricevono FTI applichino tali controlli, l'IRS ha stabilito il Programma di sicurezza, che include revisioni periodiche di tali agenzie e dei loro appaltatori.

## <a name="microsoft-and-us-internal-revenue-service-publication-1075"></a>Microsoft e US Internal Revenue Service Publication 1075

Microsoft Azure I servizi cloud governativi e Microsoft Office 365 [U.S. Government](https://products.office.com/government/office-365-web-services-for-government) forniscono un impegno contrattuale per la creazione dei controlli appropriati e le funzionalità di sicurezza necessarie ai clienti delle agenzie Microsoft per soddisfare i requisiti sostanziali di IRS 1075.  
  
Questi servizi cloud Microsoft per enti pubblici forniscono una piattaforma su cui i clienti possono creare e gestire le proprie soluzioni, ma i clienti devono determinare da soli se tali soluzioni specifiche sono gestite in conformità con IRS 1075 e sono pertanto soggette a controlli IRS.  
  
Per aiutare le agenzie governative nei loro sforzi di conformità, Microsoft:

- Offre indicazioni dettagliate per aiutare le agenzie a comprendere le proprie responsabilità e il modo in cui i vari controlli IRS vengono mappati alle funzionalità in Azure Government e Office 365 U.S. Government. L'IRS 1075 Safeguard Security Report (SSR) documenta accuratamente come servizi Microsoft implementa i controlli IRS applicabili e si basa sui pacchetti FedRAMP di Azure Government e Office 365 U.S. Government. Poiché sia IRS 1075 che FedRAMP sono basati su NIST 800-53, il limite di conformità per IRS 1075 è lo stesso dell'autorizzazione FedRAMP.
- L'IRS deve approvare esplicitamente il rilascio di qualsiasi documento di sicurezza IRS, in modo che solo i clienti governativi sotto la NDA possano esaminare la richiesta.
- Rende disponibili report di controllo e informazioni di monitoraggio prodotti da valutatori indipendenti per i servizi cloud.
- Fornisce all'IRS Considerazioni sulla conformità di Azure per enti pubblici e Office 365 considerazioni sulla conformità del governo degli Stati Uniti, che illustrano come un'agenzia può usare i servizi Microsoft Cloud per enti pubblici in modo conforme a IRS 1075. I clienti governativi con NDA possono richiedere questi documenti.
- Offre ai clienti l'opportunità (a loro spese) di comunicare con esperti microsoft o revisori esterni, se necessario.

## <a name="microsoft-in-scope-cloud-platforms--services"></a>Servizi e piattaforme cloud Microsoft inclusi nell'ambito

Le autorizzazioni FedRAMP vengono concesse a tre livelli di impatto in base alle linee guida NIST: bassa, media e alta. Questi classificano l'impatto che la perdita di riservatezza, integrità o disponibilità potrebbe avere su un'organizzazione, ovvero basso (effetto limitato), medio (grave effetto negativo) e alto (effetto grave o catastrofico).

- Azure e Azure per enti pubblici
- Dynamics 365 U.S. Government
- Office 365, Office 365 U.S. Government
- Servizio cloud Power BI, autonomo o incluso in un piano o in una famiglia di prodotti con marchio Office 365

## <a name="azure-dynamics-365-and-irs-1075"></a>Azure, Dynamics 365 e IRS 1075

Per altre informazioni sulla conformità di Azure, Dynamics 365 e altri servizi online, vedi l'offerta [di Azure IRS 1075.](/azure/compliance/offerings/offering-irs-1075)

## <a name="office-365-and-irs-1075"></a>Office 365 e IRS 1075

### <a name="office-365-cloud-environments"></a>Ambienti cloud di Office 365

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a>Applicabilità di Office 365 e servizi inclusi nell'ambito

Usare la tabella seguente per determinare l'applicabilità per i servizi e l'abbonamento a Office 365:

| **Applicabilità** | **Servizi inclusi nell'ambito** |
|:------------------|:----------------------|
| **Commerciale** | Activity Feed Service, Bing Services, Delve, Exchange Online Protection, Exchange Online, Intelligent Services, Microsoft Teams, Office 365 Customer Portal, Office Online, Office Usage Reports, OneDrive for Business, People Card, Service Infrastructure, SharePoint Online, Skype for Business, Windows Ink |
| **GCC** | Activity Feed Service, Bing Services, Delve, Exchange Online Protection, Exchange Online, Intelligent Services, Microsoft Teams, Office 365 Customer Portal, Office Online, Office Service Infrastructure, Office Usage Reports, OneDrive for Business, People Card, SharePoint Online, Skype for Business, Windows Ink |

### <a name="office-365-audits-reports-and-certificates"></a>Controlli, report e certificati di Office 365

La conformità ai requisiti sostanziali dell'IRS 1075 è coperta dal controllo FedRAMP ogni anno.

- [Autorizzazioni FedRAMP](https://marketplace.fedramp.gov/#/product/azure-government?sort=productName&productNameSearch=azure)

### <a name="frequently-asked-questions"></a>Domande frequenti

**In che modo Microsoft affronta i requisiti di IRS 1075?**

Microsoft monitora regolarmente i controlli di sicurezza, privacy e operativi e NIST 800-53 rev. 4 controlli richiesti dalla linea di base FedRAMP per i sistemi in informazioni a impatto moderato. Fornisce l'accesso trimestrale a queste informazioni tramite report di monitoraggio continuo. I clienti di Azure Government e Office 365 U.S. Government possono accedere a queste informazioni di conformità riservate tramite [il Service Trust Portal.](https://aka.ms/stphelp)

Inoltre, Microsoft si è impegnata a includere i controlli IRS 1075 nel suo set di controlli principali per Azure Government e Office 365 U.S. Government e a controllare ogni anno.

**Posso esaminare i pacchetti FedRAMP o il Piano di sicurezza del sistema?**

Sì, se l'organizzazione soddisfa i requisiti di idoneità per Azure Government e Office 365 U.S. Government. Contattare direttamente il rappresentante dell'account Microsoft per esaminare questi documenti. Puoi anche fare riferimento all'elenco FedRAMP dei provider di servizi cloud conformi.

**È possibile usare Azure o Office 365 cloud pubblico ed essere comunque conforme a IRS 1075?**

No. Gli unici ambienti in cui È possibile archiviare ed elaborare FTI sono Azure Government Office 365 U.S. Government. I clienti governativi devono soddisfare i requisiti di idoneità per l'utilizzo di questi ambienti.

### <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a>Usare Microsoft Compliance Manager per valutare i rischi

[Microsoft Compliance Manager](/microsoft-365/compliance/compliance-manager) è una funzionalità nel [Centro conformità Microsoft 365](/microsoft-365/compliance/microsoft-365-compliance-center) utile per comprendere lo stato di conformità dell'organizzazione e intraprendere azioni per ridurre i rischi. Compliance Manager offre un modello premium per creare una valutazione per questa normativa. Individuare il modello nella pagina **modelli di valutazioni** in Compliance Manager. Informazioni su come [creare valutazioni in Compliance Manager](/microsoft-365/compliance/compliance-manager-assessments).

### <a name="resources"></a>Risorse

- [Pubblicazione IRS 1075](https://www.irs.gov/pub/irs-pdf/p1075.pdf)
- [Programma di sicurezza IRS](https://www.irs.gov/uac/Safeguards-Program)
- [Hub dei controlli comuni del framework di conformità Microsoft](https://www.microsoft.com/trust-center/compliance/compliance-overview)
- [Microsoft Cloud per enti pubblici](https://azure.microsoft.com/global-infrastructure/government/)
- [Conformità in Microsoft Trust Center](https://www.microsoft.com/trust-center/compliance/compliance-overview)
