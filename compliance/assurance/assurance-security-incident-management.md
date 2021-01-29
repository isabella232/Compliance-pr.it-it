---
title: Gestione degli incidenti di sicurezza di Microsoft 365
description: Questo articolo offre una panoramica del processo di gestione degli incidenti di sicurezza in Microsoft 365.
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
f1.keywords:
- NOCSH
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance0
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: 9a76a258edf77708786cf19b160c4c5ee7af7ee6
ms.sourcegitcommit: 2973d25e9e0185b84d281f963553a332eac1c1a3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/28/2021
ms.locfileid: "50040359"
---
# <a name="microsoft-365-security-incident-management"></a>Gestione degli incidenti di sicurezza di Microsoft 365

Microsoft lavora costantemente per fornire servizi altamente sicuri di livello aziendale per i clienti di Microsoft 365. Questo documento descrive in che modo Microsoft gestisce gli incidenti di sicurezza in Microsoft 365. Un incidente di sicurezza si riferisce a qualsiasi accesso illecito ai dati dei clienti archiviati nelle apparecchiature di Microsoft o nelle strutture di Microsoft, o all'accesso non autorizzato a tali attrezzature o strutture che potrebbero comportare la perdita, la divulgazione o l'alterazione dei dati dei clienti. Gli obiettivi di Microsoft per rispondere agli incidenti di sicurezza sono proteggere i dati dei clienti e i servizi di Microsoft 365.

Il team di sicurezza di Microsoft 365 e i vari team di servizio lavorano insieme e prendono lo stesso approccio per gli incidenti di sicurezza:

- Preparazione
- Rilevamento e analisi
- Contenimento
- Eradication
- Ripristino
- Attività post-evento imprevisto

## <a name="microsoft-approach-to-security-incident-management"></a>Approccio Microsoft alla gestione degli incidenti di sicurezza

L'approccio di Microsoft alla gestione di un incidente di sicurezza è conforme al [National Institute of Standards and Technology (NIST)](https://www.nist.gov/) Special Publication (SP) 800-61. Microsoft ha diversi team dedicati che lavorano insieme per prevenire, monitorare, rilevare e rispondere agli incidenti di sicurezza.

|**Team/area**|**Descrizione**|
|:------------|:--------------|
| Microsoft Security Response Center | Identifica, monitora, risolve e risponde agli incidenti di sicurezza e alle vulnerabilità di sicurezza del software Microsoft. |
| Cyber Defense Operations Center | Il Cyber Defense Operations Center è la posizione fisica che riunisce team di risposta alla sicurezza ed esperti di tutta l'azienda per proteggere, rilevare e rispondere alle minacce in tempo reale. |
| Affari aziendali, esterni e legali | Fornisce consigli legali e normativi per un sospetto incidente di sicurezza. |
| Team di risposta alla sicurezza di Microsoft 365 | Collabora con i team del servizio Microsoft 365 per creare il processo di gestione degli incidenti di sicurezza appropriato e per guidare qualsiasi intervento in caso di incidenti di sicurezza. |
| Attendibilità di Office 365 | Fornisce indicazioni su requisiti normativi, conformità e privacy. |
| Team di sicurezza del datacenter di Microsoft 365 | Team che si concentra sui vari servizi su investimenti comuni di progettazione della sicurezza per proteggere, rilevare e rispondere ai rischi e alle minacce dell'architettura dei servizi di Microsoft 365. |
| Team di servizio | Team di progettazione per i servizi di Microsoft 365, ad esempio Exchange, SharePoint e Microsoft Teams, responsabili dei criteri e delle decisioni relative alla sicurezza per ogni servizio. |
| Microsoft Threat Intelligence Center (MSTIC) | Fornisce lo stato attuale delle minacce alla sicurezza digitale contro le infrastrutture e le risorse Microsoft, aiuta i team dei partner all'interno di Microsoft a dare priorità ai piani di azione di prevenzione e mitigazione e alle azioni di prevenzione e aumenta la protezione adottando il monitoraggio/rilevamento di incidenti quasi in tempo reale. |
| Team per la sicurezza dei partner | Altri team di sicurezza dei partner all'interno di Microsoft che forniscono servizi chiave o sono responsabili delle dipendenze chiave in Microsoft 365, ad esempio il team di Azure Security Response, Identity Security Response e i team di Microsoft Corporate Security Response. |
| Comunicazioni con l'esperienza utente di Microsoft 365 | Team di progettazione responsabile di tutte le comunicazioni dei clienti in caso di incidenti di sicurezza e di servizio. |

## <a name="response-management-process"></a>Processo di gestione delle risposte

Il team di sicurezza di Microsoft 365 e i team del servizio lavorano insieme e prendono lo stesso approccio per gli incidenti di sicurezza, che si basa sulle fasi di gestione delle risposte NIST 800-61:

- **Preparazione:** si riferisce alla preparazione organizzativa necessaria per rispondere, inclusi strumenti, processi, competenze e preparazione.
- **Analisi &** rilevamento : fa riferimento all'attività per rilevare un evento imprevisto di sicurezza in un ambiente di produzione e per analizzare tutti gli eventi per verificare l'autenticità dell'incidente di sicurezza.
- **Contenimento, eliminazione,** ripristino: fa riferimento alle azioni necessarie e appropriate intraprese per contenere l'incidente di sicurezza in base all'analisi eseguita nella fase precedente. In questa fase potrebbe essere necessaria un'analisi più approfondita per il ripristino completo dall'incidente di sicurezza.
- **Attività post-incidente:** fa riferimento all'analisi post-mortem eseguita dopo il ripristino di un incidente di sicurezza. Le azioni operative eseguite durante il processo vengono esaminate per determinare se è necessario apportare modifiche nelle fasi di preparazione o rilevamento e analisi.

## <a name="federated-security-response-model"></a>Modello di risposta per la sicurezza federata

I servizi microsoft 365 includono i principali servizi online Microsoft (Exchange, SharePoint e Microsoft Teams e così via) e altri servizi cloud Microsoft, come Azure Active Directory, Microsoft Commerce Platform e MSTIC. Questi servizi sono gestiti da team separati con i propri processi operativi di sicurezza. Altri team di Microsoft sono inoltre impegnati in vari aspetti della sicurezza di Microsoft 365. A causa della quantità di team che lavorano alla gestione delle operazioni di sicurezza in tutti i vari servizi che costituiscono Microsoft 365, Microsoft ha implementato un modello di risposta alla sicurezza federata.

Questa tabella presenta i limiti operativi tra i vari team delle operazioni di sicurezza di Microsoft 365 e i team dei servizi di Microsoft 365:

|**Attività**|**Operazioni del team di sicurezza di Microsoft 365**|**Microsoft 365 Service Team Operations**|
|:-----------|:-----------------------------------------|:----------------------------------------|
| Rilevamento e analisi | - Requisiti di rilevamento <br> - Monitoraggio e analisi della sicurezza <br> - Indicatori di compromissione (IOC) <br> - Risposta alle violazioni <br> - 24 ore su 24, 7 giorni su 7, lead di risposta a eventi imprevisti e di sicurezza | - Requisiti di rilevamento <br> - Monitoraggio della distribuzione dell'infrastruttura <br> - Analisi dei servizi e approfondimenti <br> - Triage di eventi e avvisi <br> - Progettazione dei servizi 24 ore su 24, 7 giorni su 7 a chiamata  |
| Contenimento, eliminazione, ripristino | - Lead di risposta a un evento imprevisto <br> - Indagine forense <br> - Consulenza e competenza in materia di sicurezza <br> - Indicazioni per il ripristino | - Proprietario dell'incidente di sicurezza <br> - Informazioni dettagliate e competenze sui servizi <br> - Eseguire il contenimento, l'eliminazione e il ripristino |
| Attività post-evento imprevisto | - Lead dell'analisi post-incidente <br> - Raccolta e archiviazione dei dati <br> - Lezioni apprese e richieste di bug <br> - Report operazioni non consentite | - Analisi degli eventi imprevisti sul lato servizio <br> - Assegnare priorità alle attività di follow-up <br> - Investimenti per la sicurezza dell'implementazione <br> - Conformità alla sicurezza dei servizi |

## <a name="related-articles"></a>Articoli correlati

- [Preparazione della gestione degli incidenti di sicurezza di Microsoft 365](assurance-sim-preparation.md)
- [Rilevamento e analisi degli incidenti di sicurezza di Microsoft 365](assurance-sim-detection-analysis.md)
- [Contenimento, eliminazione e ripristino della gestione degli incidenti di sicurezza di Microsoft 365](assurance-sim-containment-eradication-recovery.md)
- [Attività post-incidente di gestione degli incidenti di sicurezza di Microsoft 365](assurance-sim-post-incident-activity.md)
