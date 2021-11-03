---
title: Guida alla valutazione dei rischi per Microsoft Cloud
description: Informazioni sulla Guida alla valutazione dei rischi per Microsoft Cloud
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: Admin
ms.topic: article
f1.keywords:
- NOCSH
ms.service: O365-seccomp
ms.localizationpriority: medium
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
search.appverid:
- MET150
- MOE150
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: df4b98f90c70bab3bd7f09e6312833d8a7ea768b
ms.sourcegitcommit: 85b36ce8c79fb111980cc6462f2addb44a924065
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/02/2021
ms.locfileid: "60678433"
---
# <a name="risk-assessment-guide-for-microsoft-cloud"></a>Guida alla valutazione dei rischi per Microsoft Cloud

L'obiettivo di una valutazione dei rischi cloud è garantire che il sistema e i dati considerati per la migrazione nel cloud non introduca alcun rischio nuovo o non identificato nell'organizzazione. L'obiettivo è garantire la riservatezza, l'integrità, la disponibilità e la privacy dell'elaborazione delle informazioni e mantenere i rischi identificati al di sotto della soglia di rischio interno accettata.

In un modello di responsabilità condivisa, cloud service provider (CSP) è responsabile della gestione della sicurezza e della conformità del *cloud* come provider. Il cliente rimane responsabile della gestione e della configurazione della sicurezza e della conformità nel *cloud* in base alle proprie esigenze e alla tolleranza ai rischi.

![Modello di responsabilità condivisa.](../media/assurance-shared-responsibility-model.png)

In questa guida vengono condivise le procedure consigliate su come valutare in modo efficiente i rischi dei fornitori e su come utilizzare le risorse e gli strumenti disponibili da Microsoft.

## <a name="understand-shared-responsibility-in-the-cloud"></a>Comprendere la responsabilità condivisa nel cloud

Le distribuzioni cloud possono essere classificate come Infrastruttura come servizio (IaaS), Piattaforma come servizio (PaaS) o Software as a Service (SaaS). A seconda del modello di servizio cloud applicabile, il livello di responsabilità per i controlli di sicurezza delle soluzioni cambia tra il CSP e il cliente. In un modello locale tradizionale, il cliente è responsabile dell'intero stack. Quando si esegue il passaggio al cloud, tutte le responsabilità fisiche di sicurezza vengono trasferite al CSP. A seconda del modello di servizio cloud per l'organizzazione, ulteriori responsabilità passano al CSP. Tuttavia, nella maggior parte dei modelli di servizio, l'organizzazione rimane responsabile dei dispositivi utilizzati per accedere al cloud, alla connettività di rete, agli account e alle identità e ai dati. Microsoft investe molto nella creazione di servizi che consentano ai clienti di mantenere il controllo dei dati durante l'intero ciclo di vita.

Microsoft Cloud opera su un'iperscala, basandosi su una combinazione di DevSecOps e automazione per standardizzare i modelli operativi. Il modello operativo Microsoft cambia il modo in cui viene approcciato il rischio rispetto ai modelli operativi locali tradizionali, determinando l'implementazione di controlli diversi e talvolta sconosciuti per gestire i rischi. Quando si esegue la valutazione dei rischi nel cloud, tenere presente che l'obiettivo di Microsoft è garantire che tutti i rischi siano indirizzati, ma non necessariamente implementare gli stessi controlli dell'organizzazione. Microsoft può affrontare gli stessi rischi con un set diverso di controlli e questo dovrebbe essere riflesso nella valutazione dei rischi cloud. La progettazione e l'implementazione di controlli preventivi forti possono ridurre gran parte del lavoro richiesto dal detective e dai controlli correttivi. Un esempio è l'implementazione microsoft di [Zero Standing Access (ZSA)](assurance-microsoft-365-service-engineer-access-control.md).

## <a name="adopt-a-framework"></a>Adottare un framework

Microsoft consiglia ai clienti di mappare il framework dei rischi e dei controlli interni a un framework indipendente che indirizzi i rischi cloud in modo standardizzato. Se i modelli di valutazione dei rischi interni esistenti non affrontano le sfide specifiche del cloud computing, trarrete vantaggio da questi framework ampiamente adottati e standardizzati. Un vantaggio secondario è che Microsoft fornisce mapping con questi framework nella documentazione e negli strumenti che velocizzano le valutazioni dei rischi. Esempi di questi framework includono lo standard di sicurezza delle informazioni [ISO 27001,](/compliance/regulatory/offering-iso-27001) [CIS Benchmark](/compliance/regulatory/offering-cis-benchmark)e [NIST SP 800-53.](https://csrc.nist.gov/Projects/risk-management/sp800-53-controls/release-search#!/800-53) Microsoft offre il set più completo di offerte di conformità di qualsiasi provider di servizi di configurazione. Per ulteriori informazioni, vedere [Offerte di conformità Microsoft.](/compliance/regulatory/offering-home)

Utilizzare [Microsoft Compliance Manager](/microsoft-365/compliance/compliance-manager) per creare valutazioni che valutino la conformità con le normative del settore e regionali applicabili all'organizzazione. Le valutazioni si basano sul framework dei modelli di valutazione, che contengono i controlli necessari, le azioni di miglioramento e, se applicabile, le azioni Microsoft per completare la valutazione. Per le azioni Microsoft, vengono forniti piani di implementazione dettagliati e risultati di controllo recenti. In questo modo, è possibile salvare il tempo necessario per trovare, mappare e ricercare in che modo i controlli specifici vengono implementati da Microsoft. Per ulteriori informazioni, vedere l'articolo di Microsoft Compliance Manager.

## <a name="understand-how-microsoft-operates-to-safeguard-your-data"></a>Comprendere il modo in cui Microsoft opera per proteggere i dati

Mentre il cliente è responsabile della gestione e della configurazione della sicurezza e della conformità nel *cloud,* il CSP è responsabile della gestione della sicurezza e della *conformità del cloud.* Un modo per verificare che il provider di servizi di configurazione sia effettivamente in grado di gestire le proprie responsabilità e mantenere le promesse è esaminare i report di controllo esterni, ad esempio ISO e SOC. Microsoft rende disponibili report di controllo esterni per i gruppi di destinatari autenticati nel [Service Trust Portal.](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3)

Oltre ai report di controllo esterni, Microsoft incoraggia vivamente i clienti a sfruttare le risorse seguenti per comprendere in modo approfondito il funzionamento di Microsoft:

- [On-demand Learning Path](/learn/roles/auditor): la piattaforma Learn di Microsoft offre centinaia di percorsi di apprendimento e moduli su diversi argomenti. Tra questi, prendere [Informazioni su come Microsoft protegge i](/learn/paths/audit-safeguard-customer-data/) dati dei clienti per comprendere le procedure fondamentali di sicurezza e privacy di Microsoft.

- [Service Assurance on Microsoft Compliance](/compliance/#service-assurance): gli articoli sulle procedure di Microsoft sono classificati in 16 domini per una revisione più semplice. Ogni dominio include una panoramica che consente di acquisire il modo in cui Microsoft gestisce i rischi associati a ogni area. Vengono fornite tabelle di controllo contenenti collegamenti ai report più recenti archiviati nel Service Trust Portal, alle sezioni correlate e alla data in cui è stato condotto il report di controllo per i servizi online Microsoft. Se disponibili, vengono forniti collegamenti a artefatti che illustrano l'implementazione del controllo, ad esempio valutazioni di vulnerabilità di terze parti e report di verifica del piano di continuità aziendale. Come i report di controllo, questi elementi sono ospitati su STP e richiedono l'autenticazione per l'accesso.

| **Dominio** |**Descrizione** |
|:---------- |:-------------- |
| [**Architettura**](assurance-architecture.md) | La progettazione dei servizi online Microsoft e i principi di sicurezza che fungono da base. |
| [**Registrazione di controllo**](assurance-audit-logging.md) | In che modo Microsoft acquisisce, elabora, archivia e protegge i log che rendono possibile il monitoraggio della sicurezza e delle prestazioni. |
| [**Sicurezza del datacenter**](assurance-datacenter-security.md) | Come Microsoft gestisce in modo sicuro i datacenter che forniscono i mezzi per utilizzare i servizi online Microsoft in tutto il mondo. |
| [**Crittografia e gestione delle chiavi**](assurance-encryption.md) | Protezione crittografica delle comunicazioni dei clienti e dei dati archiviati ed elaborati nel cloud. |
| [**Governance**](assurance-governance.md) | Come Microsoft crea, distribuisce, aggiorna e applica i criteri di sicurezza in tutta l'azienda per soddisfare le promesse dei clienti e i requisiti di conformità. |
| [**Risorse umane**](assurance-human-resources.md) | I processi di screening e la gestione sicura del personale durante tutto il loro tempo presso Microsoft. |
| [**Gestione delle identità e degli accessi**](assurance-identity-and-access-management.md) | Protezione dei servizi online Microsoft e dei dati dei clienti da accessi non autorizzati o dannosi. |
| [**Gestione degli incidenti**](assurance-incident-management.md) | I processi utilizzati da Microsoft per preparare, rilevare, rispondere e comunicare tutti gli incidenti di sicurezza e privacy. |
| [**Sicurezza di rete**](assurance-network-security.md) | In che modo Microsoft protegge i propri confini di rete da attacchi esterni e gestisce la rete interna per limitarne la propagazione. |
| [**Privacy**](assurance-privacy.md) | In che modo Microsoft gestisce e protegge i dati dei clienti per preservare i diritti dei dati. |
| [**Resilienza e continuità**](assurance-resiliency-and-continuity.md) | Processo e tecnologie utilizzati per mantenere la disponibilità del servizio e garantire continuità e ripristino aziendali. |
| [**Gestione dei rischi**](assurance-risk-management.md) | L'identificazione, la valutazione e le azioni intraprese per ridurre al minimo i rischi nell'organizzazione. |
| [**Operazioni e sviluppo della sicurezza**](assurance-security-development-and-operation.md) | In che modo Microsoft garantisce che i servizi siano progettati, eseguiti e gestiti in modo sicuro durante tutto il ciclo di vita. |
| [**Monitoraggio della sicurezza**](assurance-security-monitoring.md) | Analisi centrale dei registri per rilevare e avvisare il personale di qualsiasi attività non autorizzata o dannosa. |
| [**Gestione dei fornitori**](assurance-supplier-management.md) | Come Microsoft monitora e gestisce le società di terze parti che assistono i servizi online Microsoft. |
| [**Gestione delle vulnerabilità**](assurance-vulnerability-management.md) | I processi utilizzati da Microsoft per cercare, rilevare e risolvere vulnerabilità e malware. |

## <a name="resources"></a>Risorse

- [Guida alla valutazione dei rischi e alla conformità per gli istituti finanziari in Microsoft Cloud](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=edee9b14-3661-4a16-ba83-c35caf672bd7&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_FAQ_and_White_Papers)
- [Rischio di concentrazione: prospettive di Microsoft](https://azure.microsoft.com/mediahandler/files/resourcefiles/concentration-risk-perspectives-from-microsoft-/Concentration_Risk_Perspectives_092020.pdf)
- [Service Trust Portal](https://servicetrust.microsoft.com/)
