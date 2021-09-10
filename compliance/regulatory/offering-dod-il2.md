---
title: Department of Defense (DoD) Impact Level 2 (IL2)
description: Scopri come Microsoft soddisfa gli standard DoD (Department of Defense Impact Level 2) (IL2).
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
ms.openlocfilehash: c57183a53c563fffa2bb3eb1cedb2fca23db26f4
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2021
ms.locfileid: "58947891"
---
# <a name="department-of-defense-dod-impact-level-2-il2"></a>Department of Defense (DoD) Impact Level 2 (IL2)

## <a name="dod-il2-overview"></a>Panoramica di DoD IL2

La Defense Information Systems Agency (DISA) è un'agenzia del Dipartimento della Difesa (DoD) statunitense responsabile dello sviluppo e della manutenzione della Guida ai requisiti di sicurezza del cloud computing DoD [(SRG).](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html) L'SRG definisce i requisiti di sicurezza di base utilizzati da DoD per valutare la posizione di sicurezza di un provider di servizi cloud (CSP), supportando la decisione di concedere un'autorizzazione provvisoria DoD che consente a un CSP di ospitare missioni DoD. Incorpora, sostituisce e rescinde il modello di sicurezza cloud DoD (CSM) pubblicato in precedenza e mappa al DoD Risk Management Framework (RMF).

DISA guida le agenzie e i reparti DoD nella pianificazione e autorizzazione dell'uso di un CSP. Valuta inoltre le offerte CSP per la conformità con sRG, un processo di autorizzazione in base al quale i provider di servizi di configurazione possono fornire documentazione che ne delinea la conformità agli standard DoD. Se appropriato, elaga autorizzazioni provvisorie DoD, in modo che le agenzie DoD e le organizzazioni di supporto possano utilizzare i servizi cloud senza dover eseguire un processo di approvazione completo, risparmiando tempo e fatica.

La nota del CIO DoD del 15 dicembre [2014](https://www.esi.mil/contentview.aspx?id=585) relativa alle linee guida aggiornate sull'acquisizione e l'utilizzo di servizi cloud *commerciali* afferma che "FedRAMP servirà come base di sicurezza minima per tutti i servizi cloud DoD". L'SRG usa la linea di base FedRAMP Moderate a tutti i livelli di impatto sulle informazioni (IL) e considera l'High Baseline in alcuni casi.

La sezione [SRG 5.1.1](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html#5SECURITYREQUIREMENTS) DoD use *of FedRAMP Security Controls* afferma che le informazioni IL2 possono essere ospitate in un CSP che contiene al minimo una PA moderata FedRAMP e una PA doD di livello 2, soggette alla conformità ai requisiti di sicurezza del personale descritti nella sezione 5.6.2. Tuttavia, questo approccio non consente al CSP di soddisfare altri requisiti di sicurezza e integrazione come richiesto dal proprietario della missione. Secondo la sezione [SRG 5.2.2.1](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html#5.2LegalConsiderations) *Il2 Requisiti* di posizione e separazione, DoD IL2 PA è adeguatamente coperto da una PA moderata FedRAMP in modo che i requisiti non siano valutati in modo aggiuntivo per una PA IL2.

## <a name="microsoft-in-scope-cloud-platforms--services"></a>Piattaforme e servizi cloud Microsoft inclusi nell'ambito

- Azure
- Dynamics 365
- Microsoft Cloud App Security
- Microsoft Defender per endpoint
- Microsoft Graph
- Microsoft Intune
- Microsoft Stream
- Office 365 U.S. Government, Office 365 U.S. Government - High
- Power Apps
- Power Automate
- Power BI

## <a name="azure-dynamics-365-and-dod-il2"></a>Azure, Dynamics 365 e DoD IL2

Per altre informazioni sulla conformità di Azure, Dynamics 365 e altri servizi online, vedi l'offerta [Azure DoD IL2.](/azure/compliance/offerings/offering-dod-il2)

## <a name="office-365-and-dod-il2"></a>Office 365 e DoD IL2

### <a name="office-365-cloud-environments"></a>Ambienti cloud di Office 365

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a>Applicabilità di Office 365 e servizi inclusi nell'ambito

Usare la tabella seguente per determinare l'applicabilità per i servizi e l'abbonamento a Office 365:

| **Applicabilità** | **Servizi inclusi nell'ambito** |
|:------------------|:----------------------|
| **GCC** | Activity Feed Service, Bing Services, Delve, Exchange Online Protection, Exchange Online, Intelligent Services, Microsoft Teams, Office 365 Customer Portal, Office Online, Office Service Infrastructure, Office Usage Reports, OneDrive for Business, People Card, SharePoint Online, Skype for Business, Windows Ink |
| **GCC High** | Activity Feed Service, Bing Services, Delve, Exchange Online Protection, Exchange Online, Intelligent Services, Microsoft Teams, Office 365 Customer Portal, Office Online, Office Service Infrastructure, Office Usage Reports, OneDrive for Business, People Card, SharePoint Online, Skype for Business, Windows Ink |

### <a name="resources"></a>Risorse

- [Soluzioni microsoft per enti pubblici](https://www.microsoft.com/enterprise/government)
- [Guida ai requisiti di sicurezza del cloud computing DoD](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html)
- [Documenti FedRAMP](https://www.fedramp.gov/documents/)
- [NIST SP 800-37](https://csrc.nist.gov/publications/detail/sp/800-37/rev-2/final) *Risk Management Framework for Information Systems and Organizations: A System Life-Cycle Approach for Security and Privacy*
- [NIST SP 800-53](https://csrc.nist.gov/Projects/risk-management/sp800-53-controls/release-search#!/800-53) *Controlli di sicurezza e privacy per sistemi e organizzazioni informative*
- [Istruzione DoD 8510.01](https://www.esd.whs.mil/Portals/54/Documents/DD/issuances/dodi/851001p.pdf) *DoD Risk Management Framework (RMF) per DoD Information Technology (IT)*
