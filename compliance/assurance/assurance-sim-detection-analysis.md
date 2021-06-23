---
title: 'Microsoft 365 gestione degli incidenti di sicurezza: rilevamento e analisi'
description: In questo articolo viene fornita una panoramica del processo di rilevamento e analisi degli incidenti di sicurezza in Microsoft 365.
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
ms.openlocfilehash: 3eb42b340ed6a137d0bec7b58d015009a1b20621
ms.sourcegitcommit: fb379d1110a9a86c7f9bab8c484dc3f4b3dfd6f0
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/23/2021
ms.locfileid: "53087578"
---
# <a name="microsoft-365-security-incident-management-detection-and-analysis"></a>Microsoft 365 gestione degli incidenti di sicurezza: rilevamento e analisi

Per rilevare attività dannose, Microsoft 365 registra centralmente eventi di sicurezza e altri dati ed esegue varie tecniche analitiche per individuare attività anomale o sospette. I file di registro vengono raccolti Microsoft 365 server e dispositivi di infrastruttura e archiviati in un database centrale e consolidato.

Microsoft adotta un approccio basato sui rischi per rilevare attività dannose. Usiamo i dati degli incidenti e l'intelligence per le minacce per definire e definire la priorità dei rilevamenti.

L'utilizzo di un team di persone altamente esperte, competenti e qualificate è uno dei pilastri più importanti per il successo nella fase di rilevamento e analisi. Microsoft 365 impiega più team di servizio e tali team includono dipendenti con competenze su tutti i componenti all'interno dello stack, tra cui la rete, i router, i firewall, i servizi di bilanciamento del carico, i sistemi operativi e le applicazioni.

I meccanismi di rilevamento della sicurezza in Microsoft 365 includono anche notifiche e avvisi avviati da origini diverse. Il Microsoft 365 Security Response è l'orchestratore chiave del processo di escalation degli incidenti di sicurezza. Questo team riceve tutte le escalation ed è responsabile dell'analisi e della conferma della validità dell'incidente di sicurezza.

![Flusso di lavoro per la gestione degli incidenti di sicurezza](../media/assurance-sim-workflow.png)

Uno dei pilastri principali del rilevamento è la notifica:

- Ogni team del servizio è responsabile di registrare qualsiasi azione o evento all'interno del servizio in base ai requisiti del team Microsoft 365 Sicurezza. Tutti i log creati dai diversi team di servizio vengono elaborati da una soluzione SiEM (Security Information and Event Management) con regole di sicurezza e rilevamento predefinite. Queste regole si evolvono in base alle raccomandazioni del team Microsoft 365 sicurezza, sulle informazioni apprese da incidenti di sicurezza precedenti, per determinare se vi sono attività sospette o dannose.
- Se un cliente determina che è in corso un incidente di sicurezza, può aprire un caso di supporto con Microsoft, che viene assegnato al team di comunicazioni di Microsoft 365 Customer Experience (CxP) e trasformato in un'escalation a tutti i team appropriati.

Microsoft 365 team di servizio usano anche l'intelligence acquisita nell'analisi delle tendenze tramite il monitoraggio e la registrazione della sicurezza per rilevare anomalie nei sistemi in Microsoft 365 in cui potrebbe essere indicato un attacco o un incidente di sicurezza. Microsoft 365 server aggregano l'output di questi registri nell'ambiente di produzione in un server di registrazione centralizzato. Da questo server di registrazione centralizzato, i registri vengono esaminati per individuare le tendenze in tutto l'ambiente di produzione. I dati aggregati nel server centralizzato vengono trasmessi in modo sicuro in un servizio di registrazione per l'esecuzione di query avanzate, la creazione di dashboard e il rilevamento di attività anomale e dannose. Il servizio usa anche l'apprendimento automatico per rilevare anomalie con l'output del log.

Durante la fase di escalation e a seconda della natura dell'incidente di sicurezza, il team di Microsoft 365 Security Response può coinvolgere uno o più esperti in materia di vari team di Microsoft:

- Team di sicurezza e conformità dei servizi online
- Microsoft Threat Intelligence Center (MSTIC)
- Microsoft Security Response Center (MSRC)
- Affari aziendali, esterni e legali (CELA)
- Sicurezza di Azure
- Microsoft 365 progettazione e altri.

Prima che si verifichi un'escalation al team di Microsoft 365 Security Response, il team del servizio è responsabile della determinazione e dell'impostazione del livello di gravità dell'incidente di sicurezza in base a criteri definiti, ad esempio:

- Privacy
- Impatto
- Ambito
- Numero di tenant interessati
- Area geografica
- Servizio
- Dettagli dell'evento imprevisto
- Specifiche normative del settore o del mercato dei clienti.

La definizione della priorità degli incidenti viene determinata utilizzando fattori distinti, tra cui l'impatto funzionale dell'incidente, l'impatto informativo dell'incidente e la recuperabilità dall'incidente.

Dopo aver ricevuto un'escalation di un incidente di sicurezza, il team di sicurezza di Microsoft 365 organizza un team virtuale (v-team) composto da membri del team di Microsoft 365 Security Response, dei team di servizio e del team di comunicazione degli incidenti di Microsoft 365. La parte più complessa delle attività di questo v-team è la conferma dell'incidente di sicurezza e l'eliminazione di eventuali falsi positivi. L'accuratezza delle informazioni fornite dagli indicatori determinati nella fase di preparazione è fondamentale. Analizzando queste informazioni per categoria di attacchi vettoriali, il team virtuale può determinare se l'incidente di sicurezza è un problema legittimo.

All'inizio dell'indagine, il team Office Security Incident Response registra tutte le informazioni sull'incidente in base ai criteri di gestione dei casi. Manterremo traccia delle azioni in corso e seguiremo gli standard di gestione delle prove per raccogliere, conservare e proteggere questi dati durante tutto il ciclo di vita degli eventi imprevisti.

Alcuni esempi di queste azioni includono:

- Riepilogo, che è una breve descrizione dell'incidente e del suo potenziale impatto
- Gravità e priorità dell'incidente, che derivano dalla valutazione del potenziale impatto
- Un elenco di tutti gli indicatori identificati che hanno portato al rilevamento dell'incidente
- Elenco di eventuali eventi imprevisti correlati
- Elenco di tutte le azioni intraprese dal v-team
- Eventuali prove raccolte, che verranno conservate anche per l'analisi post-mortem e le future indagini forensi
- Azioni e passaggi successivi consigliati

Dopo la conferma degli incidenti di sicurezza, gli obiettivi principali del team di Microsoft 365 Security Response e del team del servizio appropriato sono contenere l'attacco, proteggere i servizi sotto attacco ed evitare un maggiore impatto globale. Allo stesso tempo, i team di progettazione appropriati lavorano per determinare la causa principale e preparare il primo piano di ripristino.

Nella fase successiva, il team Microsoft 365 Security Response identifica i clienti interessati dall'evento imprevisto di sicurezza, se presente. L'ambito di applicazione può richiedere del tempo per determinare, in base all'area geografica, al datacenter, al servizio, alla server farm, al server e così via. L'elenco dei clienti interessati viene compilato dal team del servizio e dal team di Microsoft 365 CxP Communications, che gestiscono quindi il processo di notifica dei clienti nell'ambito degli obblighi contrattuali e di conformità.

## <a name="related-articles"></a>Articoli correlati

- [Gestione degli incidenti di sicurezza di Microsoft 365](assurance-security-incident-management.md)
- [Microsoft 365 di gestione degli incidenti di sicurezza](assurance-sim-preparation.md)
- [Microsoft 365 di gestione degli incidenti di sicurezza, eliminazione e ripristino](assurance-sim-containment-eradication-recovery.md)
- [Microsoft 365 di gestione degli incidenti di sicurezza post-incidente](assurance-sim-post-incident-activity.md)
