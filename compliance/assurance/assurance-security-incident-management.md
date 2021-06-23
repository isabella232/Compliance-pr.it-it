---
title: Gestione degli incidenti di sicurezza di Microsoft 365
description: In questo articolo viene fornita una panoramica del processo di gestione degli incidenti di sicurezza in Microsoft 365.
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
hideEdit: true
ms.openlocfilehash: 5f3123d4b4ef853357c0b98f1b6973cc8ba4d1e8
ms.sourcegitcommit: fb379d1110a9a86c7f9bab8c484dc3f4b3dfd6f0
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/23/2021
ms.locfileid: "53088888"
---
# <a name="microsoft-365-security-incident-management"></a>Gestione degli incidenti di sicurezza di Microsoft 365

Microsoft lavora costantemente per fornire servizi altamente sicuri e di livello aziendale per Microsoft 365 clienti. In questo documento viene descritto come Microsoft gestisce gli eventi imprevisti di sicurezza Microsoft 365. Un incidente di sicurezza si riferisce a qualsiasi accesso illecito ai dati dei clienti archiviati nelle attrezzature di Microsoft o nelle strutture di Microsoft, o all'accesso non autorizzato a tali attrezzature o strutture che potrebbero causare la perdita, la divulgazione o l'alterazione dei dati dei clienti. Gli obiettivi di Microsoft per rispondere agli incidenti di sicurezza sono proteggere i dati dei clienti e i servizi Microsoft 365 sicurezza.

Il team Microsoft 365 sicurezza e i vari team di servizio lavorano insieme e prendono lo stesso approccio agli incidenti di sicurezza:

- Preparazione
- Rilevamento e analisi
- Contenimento
- Eradicazione
- Ripristino
- Attività post-evento imprevisto

## <a name="microsoft-approach-to-security-incident-management"></a>Approccio Microsoft alla gestione degli incidenti di sicurezza

L'approccio di Microsoft alla gestione di un incidente di sicurezza è conforme al [National Institute of Standards and Technology (NIST)](https://www.nist.gov/) Special Publication (SP) 800-61. Microsoft ha diversi team dedicati che lavorano insieme per prevenire, monitorare, rilevare e rispondere a incidenti di sicurezza.

|**Team/area**|**Descrizione**|
|:------------|:--------------|
| Microsoft Security Response Center | Identifica, monitora, risolve e risponde a incidenti di sicurezza e vulnerabilità di sicurezza software Microsoft. |
| Cyber Defense Operations Center | Il Cyber Defense Operations Center è la posizione fisica che riunisce team di risposta alla sicurezza ed esperti di tutta l'azienda per proteggere, rilevare e rispondere alle minacce in tempo reale. |
| Affari aziendali, esterni e legali | Fornisce consigli legali e normativi per un sospetto incidente di sicurezza. |
| Microsoft 365 Team di risposta alla sicurezza | Collabora con i team Microsoft 365 Service per creare il processo di gestione degli incidenti di sicurezza appropriato e per guidare qualsiasi risposta agli incidenti di sicurezza. |
| Office 365 Attendibilità | Fornisce indicazioni sui requisiti normativi, sulla conformità e sulla privacy. |
| Microsoft 365 Datacenter Security Team | Team che si concentra sui vari servizi su investimenti comuni di progettazione della sicurezza per proteggere, rilevare e rispondere ai rischi e alle minacce dell'architettura Microsoft 365 servizio. |
| Team di servizio | Team di progettazione per Microsoft 365, ad esempio Exchange, SharePoint e Microsoft Teams, responsabili dei criteri e delle decisioni relative alla sicurezza per ogni servizio. |
| Microsoft Threat Intelligence Center (MSTIC) | Fornisce lo stato attuale delle minacce alla sicurezza digitale contro le infrastrutture e gli asset Microsoft, aiuta i team dei partner all'interno di Microsoft a definire le priorità dei piani di azione di prevenzione e prevenzione e aumenta la protezione adottando il monitoraggio/rilevamento di incidenti quasi in tempo reale. |
| Team di sicurezza dei partner | Altri team di sicurezza dei partner all'interno di Microsoft che forniscono servizi chiave o sono responsabili delle dipendenze chiave in Microsoft 365, ad esempio il team di Azure Security Response, Identity Security Response e i team di Microsoft Corporate Security Response. |
| Microsoft 365 Comunicazioni con l'esperienza del cliente | Team di progettazione responsabile di tutte le comunicazioni dei clienti in caso di incidenti di sicurezza e di servizio. |

## <a name="response-management-process"></a>Processo di gestione delle risposte

Il team Microsoft 365 sicurezza e i team di servizio lavorano insieme e prendono lo stesso approccio agli incidenti di sicurezza, che si basa sulle fasi di gestione delle risposte NIST 800-61:

- **Preparazione:** si riferisce alla preparazione dell'organizzazione necessaria per rispondere, inclusi strumenti, processi, competenze e preparazione.
- **Detection & analysis**: fa riferimento all'attività per rilevare un incidente di sicurezza in un ambiente di produzione e per analizzare tutti gli eventi per verificare l'autenticità dell'incidente di sicurezza.
- **Containment, eradication, recovery**: Fa riferimento alle azioni necessarie e appropriate intraprese per contenere l'incidente di sicurezza in base all'analisi eseguita nella fase precedente. Potrebbe essere necessaria un'analisi più approfondita anche in questa fase per il ripristino completo dall'incidente di sicurezza.
- **Attività post-incidente**: fa riferimento all'analisi post-mortem eseguita dopo il ripristino di un incidente di sicurezza. Le azioni operative eseguite durante il processo vengono esaminate per determinare se è necessario apportare modifiche nelle fasi di preparazione o rilevamento e analisi.

![Fasi di gestione degli incidenti di sicurezza](../media/assurance-sim-phases.png)

## <a name="federated-security-response-model"></a>Modello di risposta di sicurezza federata

i Microsoft 365 includono i servizi online Microsoft di base (Exchange, SharePoint e Microsoft Teams e così via) e altri servizi cloud Microsoft, ad esempio Azure Active Directory, Microsoft Commerce Platform e MSTIC. Questi servizi sono gestiti da team separati con i propri processi operativi di sicurezza. Altri team di Microsoft sono inoltre impegnati in vari aspetti della sicurezza Microsoft 365. A causa della vasta gamma di team che lavorano alla gestione delle operazioni di sicurezza in tutti i vari servizi che costituiscono Microsoft 365, Microsoft ha implementato un modello di risposta di sicurezza federata.

In questa tabella vengono presentati i limiti operativi tra i vari team di Microsoft 365 sicurezza e i team Microsoft 365 di servizio:

|**Attività**|**Microsoft 365 Operazioni del team di sicurezza**|**Microsoft 365 Operazioni del team di servizio**|
|:-----------|:-----------------------------------------|:----------------------------------------|
| Rilevamento e analisi | - Requisiti di rilevamento <br> - Monitoraggio e analisi della sicurezza <br> - Indicatori di compromissione (IOC) <br> - Risposta alle violazioni <br> - Lead di sicurezza 24x7 in caso di chiamata e risposta a eventi imprevisti | - Requisiti di rilevamento <br> - Monitoraggio della distribuzione dell'infrastruttura <br> - Analisi dei servizi e approfondimenti <br> - Triage di eventi e avvisi <br> - 24x7 service engineering on-call  |
| Contenimento, eradicazione, ripristino | - Lead di risposta a eventi imprevisti <br> - Indagine forense <br> - Consulenza e competenza in materia di sicurezza <br> - Indicazioni per il ripristino | - Proprietario dell'incidente di sicurezza <br> - Informazioni dettagliate e competenze sui servizi <br> - Eseguire il contenimento, l'eliminazione e il ripristino |
| Attività post-evento imprevisto | - Lead di analisi post-incidente <br> - Raccolta e archiviazione dei dati <br> - Lezioni apprese e richieste di bug <br> - Segnalazione degli eventi imprevisti | - Analisi degli eventi imprevisti sul lato servizio <br> - Assegnare priorità alle attività di follow-up <br> - Investimenti per la sicurezza dell'implementazione <br> - Conformità alla sicurezza del servizio |

## <a name="related-articles"></a>Articoli correlati

- [Microsoft 365 di gestione degli incidenti di sicurezza](assurance-sim-preparation.md)
- [Microsoft 365 rilevamento e analisi della gestione degli incidenti di sicurezza](assurance-sim-detection-analysis.md)
- [Microsoft 365 di gestione degli incidenti di sicurezza, eliminazione e ripristino](assurance-sim-containment-eradication-recovery.md)
- [Microsoft 365 di gestione degli incidenti di sicurezza post-incidente](assurance-sim-post-incident-activity.md)
