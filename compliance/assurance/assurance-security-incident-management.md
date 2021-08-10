---
title: Gestione degli incidenti di sicurezza Microsoft
description: In questo articolo viene fornita una panoramica del processo di gestione degli incidenti di sicurezza nei servizi online Microsoft.
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
- MS-Compliance
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 38bb8c8492c3bbff6ed96380ac3a4d284f220a0ec5b2fb7b7c00814033a5c02c
ms.sourcegitcommit: af1925730de60c3b698edc4e1355c38972bdd759
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/05/2021
ms.locfileid: "54292189"
---
# <a name="microsoft-security-incident-management"></a>Gestione degli incidenti di sicurezza Microsoft

Microsoft lavora costantemente per fornire servizi altamente sicuri e di livello aziendale per i clienti Microsoft, ma gli incidenti di sicurezza sono una realtà inevitabile che deve essere gestita in modo accurato e rapido. In questo documento viene fornita una panoramica sul modo in cui Microsoft gestisce gli incidenti di sicurezza utilizzando metodi e tecnologie già provati e veri per ridurre al minimo il loro potenziale impatto. Un incidente di sicurezza si riferisce a qualsiasi accesso illecito ai dati dei clienti archiviati nelle attrezzature di Microsoft o nelle strutture di Microsoft, o all'accesso non autorizzato a tali attrezzature o strutture che potrebbero causare la perdita, la divulgazione o l'alterazione dei dati dei clienti. Gli obiettivi di Microsoft per rispondere agli incidenti di sicurezza sono proteggere i dati dei clienti e i servizi online di Microsoft.

I team di sicurezza dei servizi online Microsoft e i vari team di servizio lavorano insieme e prendono lo stesso approccio agli incidenti di sicurezza:

- Preparazione
- Rilevamento e analisi
- Contenimento, eliminazione e ripristino
- Attività post-evento imprevisto

## <a name="microsoft-approach-to-security-incident-management"></a>Approccio Microsoft alla gestione degli incidenti di sicurezza

L'approccio di Microsoft alla gestione di un incidente di sicurezza è conforme al [National Institute of Standards and Technology (NIST)](https://www.nist.gov/) Special Publication (SP) 800-61. Microsoft ha diversi team dedicati che lavorano insieme per prevenire, monitorare, rilevare e rispondere a incidenti di sicurezza.

|**Team/area**|**Descrizione**|
|:------------|:--------------|
| Microsoft Security Response Center | Identifica, monitora, risolve e risponde a incidenti di sicurezza e vulnerabilità di sicurezza software Microsoft. |
| Cyber Defense Operations Center | Il Cyber Defense Operations Center è la posizione fisica che riunisce team di risposta alla sicurezza ed esperti di tutta l'azienda per proteggere, rilevare e rispondere alle minacce in tempo reale. |
| Affari aziendali, esterni e legali | Fornisce consigli legali e normativi per un sospetto incidente di sicurezza. |
| Microsoft Datacenter Security Team | Team che si concentra sui vari servizi su investimenti comuni di progettazione della sicurezza per proteggere, rilevare e rispondere ai rischi e alle minacce dell'architettura dei servizi. |
| Team di risposta alla sicurezza Microsoft | Team di sicurezza indipendenti di Azure, Dynamics 365 e Microsoft 365 che collaborano con i team di servizio per creare il processo di gestione degli incidenti di sicurezza appropriato e per guidare qualsiasi risposta agli incidenti di sicurezza. |
| Team di governance, rischio e conformità (GRC) Microsoft | Fornire indicazioni su requisiti normativi, conformità e privacy. |
| Team di assistenza | Team di progettazione per Azure, Dynamics 365, Microsoft 365 responsabili dei criteri e delle decisioni relative alla sicurezza per ogni servizio. |
| Responsabili delle operazioni di Azure | Supervisiona l'indagine e la risoluzione degli incidenti di sicurezza e privacy correlati ad Azure. |
| Microsoft Threat Intelligence Center (MSTIC) | Fornisce lo stato attuale delle minacce alla sicurezza digitale contro le infrastrutture e gli asset Microsoft, aiuta i team dei partner all'interno di Microsoft a definire le priorità dei piani di azione di prevenzione e prevenzione e aumenta la protezione adottando il monitoraggio/rilevamento di incidenti quasi in tempo reale. |
| Team di comunicazione per l'esperienza del cliente | Team di progettazione responsabili di tutte le comunicazioni dei clienti su incidenti di sicurezza e servizi. I team separati sono dedicati ad Azure, Dynamics 365 e Microsoft 365. |

## <a name="response-management-process"></a>Processo di gestione delle risposte

I team di sicurezza e i team dei servizi online Microsoft lavorano insieme e prendono lo stesso approccio agli incidenti di sicurezza, che si basa sulle fasi di gestione delle risposte NIST 800-61:

- **Preparazione:** si riferisce alla preparazione dell'organizzazione necessaria per rispondere, inclusi strumenti, processi, competenze e preparazione.
- **Detection & analysis**: fa riferimento all'attività per rilevare un incidente di sicurezza in un ambiente di produzione e per analizzare tutti gli eventi per verificare l'autenticità dell'incidente di sicurezza.
- **Containment, eradication, recovery**: Fa riferimento alle azioni necessarie e appropriate intraprese per contenere l'incidente di sicurezza in base all'analisi eseguita nella fase precedente. Potrebbe essere necessaria un'analisi più approfondita anche in questa fase per il ripristino completo dall'incidente di sicurezza.
- **Attività post-incidente**: fa riferimento all'analisi post-mortem eseguita dopo il ripristino di un incidente di sicurezza. Le azioni operative eseguite durante il processo vengono esaminate per determinare se è necessario apportare modifiche nelle fasi di preparazione o rilevamento e analisi.

![Fasi di gestione degli incidenti di sicurezza](../media/assurance-sim-phases.png)

## <a name="federated-security-response-model"></a>Modello di risposta di sicurezza federata

I servizi online Microsoft sono costituiti da prodotti Microsoft di base, tra cui Azure, Dynamics 365 e Microsoft 365. Ognuno di questi servizi è gestito da team separati con i propri processi operativi di sicurezza. Altri team di Microsoft, ad esempio MSTIC, sono coinvolti in vari aspetti della sicurezza dei servizi online Microsoft. A causa della vasta gamma di team che lavorano alla gestione delle operazioni di sicurezza in tutti i vari servizi che costituiscono i servizi online Microsoft, Microsoft ha implementato un modello di risposta di sicurezza federata.

In questa tabella vengono presentati i limiti operativi tra i vari team microsoft per le operazioni di sicurezza dei servizi online e i team dei servizi Microsoft:

|**Attività**|**Operazioni del team di sicurezza Microsoft**|**Microsoft Service Team Operations**|
|:-----------|:-----------------------------------------|:----------------------------------------|
| Rilevamento e analisi | - Requisiti di rilevamento <br> - Monitoraggio e analisi della sicurezza <br> - Indicatori di compromissione (IOC) <br> - Risposta alle violazioni <br> - Lead di sicurezza 24x7 in caso di chiamata e risposta a eventi imprevisti | - Requisiti di rilevamento <br> - Monitoraggio della distribuzione dell'infrastruttura <br> - Analisi dei servizi e approfondimenti <br> - Triage di eventi e avvisi <br> - 24x7 service engineering on-call  |
| Contenimento, eradicazione, ripristino | - Lead di risposta a eventi imprevisti <br> - Indagine forense <br> - Consulenza e competenza in materia di sicurezza <br> - Indicazioni per il ripristino | - Proprietario dell'incidente di sicurezza <br> - Informazioni dettagliate e competenze sui servizi <br> - Eseguire il contenimento, l'eliminazione e il ripristino |
| Attività post-evento imprevisto | - Lead di analisi post-incidente <br> - Raccolta e archiviazione dei dati <br> - Lezioni apprese e richieste di bug <br> - Segnalazione degli eventi imprevisti | - Analisi degli eventi imprevisti sul lato servizio <br> - Assegnare priorità alle attività di follow-up <br> - Investimenti per la sicurezza dell'implementazione <br> - Conformità alla sicurezza del servizio |

## <a name="related-articles"></a>Articoli correlati

- [Gestione degli incidenti di sicurezza Microsoft: preparazione](assurance-sim-preparation.md)
- [Gestione degli incidenti di sicurezza Microsoft: rilevamento e analisi](assurance-sim-detection-analysis.md)
- [Gestione degli incidenti di sicurezza Microsoft: contenimento, eliminazione e ripristino](assurance-sim-containment-eradication-recovery.md)
- [Gestione degli incidenti di sicurezza Microsoft: attività post-incidente](assurance-sim-post-incident-activity.md)
