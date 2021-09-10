---
title: Department of Defense (DoD) Impact Level 5 (IL5)
description: Scopri come Microsoft soddisfa gli standard DoD (Department of Defense Impact Level 5) (IL5).
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
ms.openlocfilehash: c0c987dc5fbe2bee60508f0fab7dbdb8dce97857
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2021
ms.locfileid: "58947894"
---
# <a name="department-of-defense-dod-impact-level-5-il5"></a>Department of Defense (DoD) Impact Level 5 (IL5)

## <a name="dod-il5-overview"></a>Panoramica di DoD IL5

La Defense Information Systems Agency (DISA) è un'agenzia del Dipartimento della Difesa (DoD) statunitense responsabile dello sviluppo e della manutenzione della Guida ai requisiti di sicurezza del cloud computing DoD [(SRG).](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html) L'SRG definisce i requisiti di sicurezza di base utilizzati da DoD per valutare la posizione di sicurezza di un provider di servizi cloud (CSP), supportando la decisione di concedere un'autorizzazione provvisoria DoD che consente a un CSP di ospitare missioni DoD. Incorpora, sostituisce e rescinde il modello di sicurezza cloud DoD (CSM) pubblicato in precedenza e mappa al DoD Risk Management Framework (RMF).

DISA guida le agenzie e i reparti DoD nella pianificazione e autorizzazione dell'uso di un CSP. Valuta inoltre le offerte CSP per la conformità con sRG, un processo di autorizzazione in base al quale i provider di servizi di configurazione possono fornire documentazione che ne delinea la conformità agli standard DoD. Se appropriato, elaga autorizzazioni provvisorie DoD, in modo che le agenzie DoD e le organizzazioni di supporto possano utilizzare i servizi cloud senza dover eseguire un processo di approvazione completo, risparmiando tempo e fatica.

In base ai livelli di impatto delle informazioni della sezione [3.2 di SRG,](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html#3.2InformationImpactLevels) le informazioni su IL5 riguardano:

- Informazioni non classificate controllate che richiedono un livello di protezione superiore a quello di IL4
    - Il [Registro di](https://www.archives.gov/cui) sistema CUI fornisce categorie specifiche di informazioni che sono sotto protezione dal ramo Executive, ad esempio, più di 20 raggruppamenti di categorie sono inclusi nell'elenco di categorie [CUI.](https://www.archives.gov/cui/registry/category-list)
    - [NIST SP 800-171](https://csrc.nist.gov/publications/detail/sp/800-171/rev-2/final) *Protecting Controlled Unclassified Information in Nonfederal Systems and Organizations* è progettato per l'uso da parte delle agenzie federali in contratti o altri accordi stipulati con organizzazioni non federali.

- National Security Systems (NSS)
    - [NIST SP 800-59](https://nvlpubs.nist.gov/nistpubs/Legacy/SP/nistspecialpublication800-59.pdf) *Guideline for Identifying an Information System as a National Security System* fornisce le definizioni di NSS.
    - [CNSSI 1253](https://www.dcsa.mil/portals/91/documents/ctp/nao/CNSSI_No1253.pdf) *Security Categorization and Control Selection for National Security Systems* fornisce indicazioni sugli standard di sicurezza che le agenzie federali devono applicare per classificare le informazioni sulla sicurezza nazionale.

La nota del CIO DoD del 15 dicembre [2014](https://www.esi.mil/contentview.aspx?id=585) relativa alle linee guida aggiornate sull'acquisizione e l'utilizzo di servizi cloud *commerciali* afferma che "FedRAMP servirà come base di sicurezza minima per tutti i servizi cloud DoD". L'SRG usa la linea di base FedRAMP Moderate a tutti i livelli di impatto sulle informazioni (IL) e considera l'High Baseline in alcuni casi.

La sezione [SRG 5.1.1](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html#5SECURITYREQUIREMENTS) DoD use *of FedRAMP Security Controls* afferma che un FedRAMP High PA, integrato con i controlli e i miglioramenti del controllo DoD FedRAMP+ (C/CE) e i requisiti in SRG, viene utilizzato per valutare i CSP per l'assegnazione di una pa DoD a IL5. Indipendentemente dalla linea di base C/CE utilizzata come base per una pa FedRAMP High, ulteriori considerazioni e/o requisiti dovranno essere valutati e approvati prima che una pa DoD possa essere assegnata a IL5. In particolare, la sezione [SRG 5.1.2](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html#5SECURITYREQUIREMENTS) *DoD FedRAMP+ Security Controls/Enhancements* indica nella tabella 2 che sono necessari 10 C/C Aggiuntivi oltre la linea di base FedRAMP High per un DoD IL5 PA.

Inoltre, secondo la sezione [SRG 5.2.2.3](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html#5.2LegalConsiderations) I requisiti di posizione e separazione *del livello 5* devono essere soddisfatti i requisiti seguenti (tra gli altri) per un piano di sicurezza di livello 5:

- È sufficiente la separazione virtuale/logica tra i tenant /missioni dod e federal government. È necessaria la separazione virtuale/logica tra i sistemi tenant/mission.
- È necessaria la separazione fisica da tenant non governativi o non federali (ovvero tenant pubblici, locali/statali).
- Il CSP limita il potenziale accesso alle informazioni di DoD e della community ai dipendenti CSP che sono cittadini statunitensi.

## <a name="microsoft-in-scope-cloud-platforms--services"></a>Piattaforme e servizi cloud Microsoft inclusi nell'ambito

- Azure
- Servizio clienti Dynamics 365
- Microsoft Defender per endpoint (in precedenza Microsoft Defender Advanced Threat Protection)
- Microsoft Graph
- Microsoft Stream
- Office 365 U.S. Government Defense
- Power Automate (in precedenza Microsoft Flow)
- Power BI

## <a name="azure-dynamics-365-and-dod-il5"></a>Azure, Dynamics 365 e DoD IL5

Per altre informazioni sulla conformità di Azure, Dynamics 365 e altri servizi online, vedi l'offerta [Azure DoD IL5.](/azure/compliance/offerings/offering-dod-il5)

## <a name="office-365-and-dod-il5"></a>Office 365 e DoD IL5

### <a name="office-365-cloud-environments"></a>Ambienti cloud di Office 365

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a>Applicabilità di Office 365 e servizi inclusi nell'ambito

Usare la tabella seguente per determinare l'applicabilità per i servizi e l'abbonamento a Office 365:

| **Applicabilità** | **Servizi inclusi nell'ambito** |
|:------------------|:----------------------|
| **DoD** | Activity Feed Service, Bing Services, Exchange Online, Exchange Online Protection, Intelligent Services, Microsoft Teams, Office 365 Customer Portal, Office Online, Office Service Infrastructure, Office Usage Reports, OneDrive for Business, People Card, SharePoint Online, Skype for Business, Windows Ink |

### <a name="attestation-documents"></a>Documenti di attestazione

I clienti del governo statunitense Office 365 la documentazione FedRAMP per la difesa del governo degli Stati Uniti direttamente dal [Marketplace FedRAMP](https://marketplace.fedramp.gov/#!/products?sort=productName&productNameSearch=azure) inviando un modulo di richiesta di accesso al pacchetto. Devi avere un indirizzo di posta elettronica .gov o .mil per accedere a un pacchetto di sicurezza FedRAMP direttamente da FedRAMP.

Selezionare la documentazione FedRAMP e DoD, tra cui System Security Plan (SSP), report di monitoraggio continuo, Plan of Action and Milestones (POA M) e così via, è disponibile per i clienti in NDA e l'autorizzazione di accesso in sospeso dalla sezione Report di controllo del Portale dei servizi attendibili \& [- Report FedRAMP.](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3) Per assistenza, contattare il rappresentante dell'account Microsoft.

### <a name="resources"></a>Risorse

- [Soluzioni microsoft per enti pubblici](https://www.microsoft.com/enterprise/government)
- [Guida ai requisiti di sicurezza del cloud computing DoD](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html)
- [Documenti FedRAMP](https://www.fedramp.gov/documents/)
- [Istruzione DoD 8510.01](https://www.esd.whs.mil/Portals/54/Documents/DD/issuances/dodi/851001p.pdf) *DoD Risk Management Framework (RMF) per DoD Information Technology (IT)*
- [NIST SP 800-37](https://csrc.nist.gov/publications/detail/sp/800-37/rev-2/final) *Risk Management Framework for Information Systems and Organizations: A System Life-Cycle Approach for Security and Privacy*
- [NIST SP 800-53](https://csrc.nist.gov/Projects/risk-management/sp800-53-controls/release-search#!/800-53) *Controlli di sicurezza e privacy per sistemi e organizzazioni informative*
- [Linee guida NIST SP 800-59](https://nvlpubs.nist.gov/nistpubs/Legacy/SP/nistspecialpublication800-59.pdf) per l'identificazione di un *sistema di informazioni come sistema di sicurezza nazionale*
- [CnSSI 1253](https://www.dcsa.mil/portals/91/documents/ctp/nao/CNSSI_No1253.pdf) *Security Categorization and Control Selection for National Security Systems*
- [NIST SP 800-171](https://csrc.nist.gov/publications/detail/sp/800-171/rev-2/final) Protezione delle informazioni non classificate controllate *in organizzazioni* e sistemi non aziendali
- Controlled Unclassified Information (CUI) [Registry](https://www.archives.gov/cui) and CUI [category list](https://www.archives.gov/cui/registry/category-list).
