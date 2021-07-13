---
title: 'Gestione degli incidenti di sicurezza Microsoft: rilevamento e analisi'
description: In questo articolo viene fornita una panoramica del processo di rilevamento e analisi della gestione degli incidenti di sicurezza nei servizi online Microsoft.
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
ms.openlocfilehash: 445d812b33214a3d2287268b587607004ef96ab7
ms.sourcegitcommit: 8bf2602d56eedee4447ddb374ef95b0587f254e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/12/2021
ms.locfileid: "53377353"
---
# <a name="microsoft-security-incident-management-detection-and-analysis"></a>Gestione degli incidenti di sicurezza Microsoft: rilevamento e analisi

Per rilevare attività dannose, ognuno dei servizi online di Microsoft registra centralmente eventi di sicurezza e altri dati ed esegue varie tecniche analitiche per individuare attività anomale o sospette. I file di registro vengono raccolti dai server e dai dispositivi dell'infrastruttura dei Servizi online Microsoft e archiviati in database centrali e consolidati.

Microsoft adotta un approccio basato sui rischi per rilevare attività dannose. Usiamo i dati degli incidenti e l'intelligence per le minacce per definire e definire la priorità dei rilevamenti.

L'utilizzo di un team di persone altamente esperte, competenti e qualificate è uno dei pilastri più importanti per il successo nella fase di rilevamento e analisi. Microsoft impiega più team di servizio che includono dipendenti con competenze su tutti i componenti all'interno dello stack, tra cui la rete, i router, i firewall, i servizi di bilanciamento del carico, i sistemi operativi e le applicazioni.

I meccanismi di rilevamento della sicurezza nei servizi online Microsoft includono anche notifiche e avvisi avviati da origini diverse. I team di risposta alla sicurezza dei servizi online Microsoft sono gli orchestratori chiave del processo di escalation degli incidenti di sicurezza. Questi team ricevono tutte le escalation e sono responsabili dell'analisi e della conferma della validità dell'incidente di sicurezza.

![Flusso di lavoro per la gestione degli incidenti di sicurezza](../media/assurance-sim-workflow.png)

Uno dei pilastri principali del rilevamento è la notifica:

- Ogni team del servizio è responsabile di registrare qualsiasi azione o evento all'interno del servizio in base ai requisiti del team di sicurezza del servizio online. Tutti i log creati dai diversi team di servizio vengono elaborati da una soluzione SiEM (Security Information and Event Management) con regole di sicurezza e rilevamento predefinite. Queste regole si evolvono in base alle raccomandazioni del team di sicurezza, sulle informazioni apprese dagli incidenti di sicurezza precedenti, per determinare se sono presenti attività sospette o dannose.
- Se un cliente determina che è in corso un incidente di sicurezza, può aprire un caso di supporto con Microsoft, che viene assegnato al team di comunicazione Microsoft e trasformato in un'escalation a tutti i team appropriati.

I team del servizio Azure, Dynamics 365 e Microsoft 365 usano anche l'intelligence acquisita nell'analisi delle tendenze tramite il monitoraggio e la registrazione della sicurezza per rilevare anomalie nei sistemi in informazioni dei servizi online Microsoft che potrebbero indicare un attacco o un incidente di sicurezza. I sistemi microsoft online services aggregano l'output di questi registri nell'ambiente di produzione in server di registrazione centralizzati. Da questi server di registrazione centralizzati, i registri vengono esaminati per individuare le tendenze in tutto l'ambiente di produzione. I dati aggregati nei server centralizzati vengono trasmessi in modo sicuro in un servizio di registrazione per l'esecuzione di query avanzate, la creazione di dashboard e il rilevamento di attività anomale e dannose. Il servizio usa anche l'apprendimento automatico per rilevare anomalie con l'output del log.

Durante la fase di escalation e a seconda della natura dell'incidente di sicurezza, i team di risposta alla sicurezza possono coinvolgere uno o più esperti in materia di vari team di Microsoft:

- Team di sicurezza e conformità dei servizi online
- Microsoft Threat Intelligence Center (MSTIC)
- Microsoft Security Response Center (MSRC)
- Affari aziendali, esterni e legali (CELA)
- Sicurezza di Azure
- Microsoft 365 progettazione e altri.

Prima che si verifichi un'escalation a un team di risposta alla sicurezza, il team del servizio è responsabile della determinazione e dell'impostazione del livello di gravità dell'incidente di sicurezza in base a criteri definiti, ad esempio:

- Privacy
- Impatto
- Ambito
- Numero di tenant interessati
- Area geografica
- Servizio
- Dettagli dell'evento imprevisto
- Specifiche normative del settore o del mercato dei clienti.

La definizione della priorità degli incidenti viene determinata utilizzando fattori distinti, tra cui l'impatto funzionale dell'incidente, l'impatto informativo dell'incidente e la recuperabilità dall'incidente.

Dopo aver ricevuto un'escalation su un incidente di sicurezza, il team di sicurezza organizza un team virtuale (v-team) composto da membri del team di risposta alla sicurezza dei servizi online Microsoft, dei team di servizio e del team di comunicazione degli incidenti. Il team virtuale deve quindi confermare la legittimità dell'incidente di sicurezza ed eliminare eventuali falsi positivi. L'accuratezza delle informazioni fornite dagli indicatori determinati durante la fase di preparazione è fondamentale. Analizzando queste informazioni per categoria di attacchi vettoriali, il team virtuale può determinare se l'incidente di sicurezza è un problema legittimo.

All'inizio dell'indagine, il team di risposta agli incidenti di sicurezza registra tutte le informazioni sull'incidente in base ai criteri di gestione dei casi. Manterremo traccia delle azioni in corso e seguiremo gli standard di gestione delle prove per raccogliere, conservare e proteggere questi dati durante tutto il ciclo di vita degli eventi imprevisti.

Alcuni esempi di queste azioni includono:

- Riepilogo, che è una breve descrizione dell'incidente e del suo potenziale impatto
- Gravità e priorità dell'incidente, che derivano dalla valutazione del potenziale impatto
- Un elenco di tutti gli indicatori identificati che hanno portato al rilevamento dell'incidente
- Elenco di eventuali eventi imprevisti correlati
- Elenco di tutte le azioni intraprese dal v-team
- Eventuali prove raccolte, che verranno conservate anche per l'analisi post-mortem e le future indagini forensi
- Azioni e passaggi successivi consigliati

Dopo la conferma degli incidenti di sicurezza, gli obiettivi principali del team di risposta alla sicurezza e del team di servizio appropriato sono contenere l'attacco, proteggere i servizi sotto attacco ed evitare un maggiore impatto globale. Allo stesso tempo, i team di progettazione appropriati lavorano per determinare la causa principale e preparare il primo piano di ripristino.

Nella fase successiva, il team di risposta alla sicurezza identifica i clienti interessati dall'evento imprevisto di sicurezza, se presente. L'ambito di applicazione può richiedere del tempo per determinare, in base all'area geografica, al datacenter, al servizio, alla server farm, al server e così via. L'elenco dei clienti interessati viene compilato dal team del servizio e dal team di comunicazione Microsoft corrispondente, che quindi gestisce il processo di notifica dei clienti nell'ambito degli obblighi contrattuali e di conformità.

## <a name="related-articles"></a>Articoli correlati

- [Gestione degli incidenti di sicurezza Microsoft](assurance-security-incident-management.md)
- [Gestione degli incidenti di sicurezza Microsoft: preparazione](assurance-sim-preparation.md)
- [Gestione degli incidenti di sicurezza Microsoft: contenimento, eliminazione e ripristino](assurance-sim-containment-eradication-recovery.md)
- [Gestione degli incidenti di sicurezza Microsoft: attività post-incidente](assurance-sim-post-incident-activity.md)
- [Come registrare un ticket di supporto per gli eventi di sicurezza](/azure/security/fundamentals/event-support-ticket)
- [Notifica di violazione nell'ambito del GDPR in Azure e Dynamics 365](/compliance/regulatory/gdpr-breach-azure-dynamics)
