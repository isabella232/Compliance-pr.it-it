---
title: 'Gestione degli incidenti di sicurezza Microsoft: contenimento, eliminazione e ripristino'
description: In questo articolo viene fornita una panoramica del processo di contenimento, eliminazione e ripristino della gestione degli incidenti di sicurezza nei servizi online Microsoft.
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
ms.openlocfilehash: 95e52107df2f3e745d393c62929f7c169bcf9a33
ms.sourcegitcommit: 8bf2602d56eedee4447ddb374ef95b0587f254e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/12/2021
ms.locfileid: "53377553"
---
# <a name="microsoft-security-incident-management-containment-eradication-and-recovery"></a>Gestione degli incidenti di sicurezza Microsoft: contenimento, eliminazione e ripristino

In base all'analisi eseguita dal team di risposta alla sicurezza, dal team del servizio e da altri, viene sviluppato un piano di contenimento e ripristino appropriato per ridurre al minimo l'effetto dell'incidente di sicurezza. I team di servizio appropriati applicano quindi il piano in produzione con il supporto del team di risposta alla sicurezza.

## <a name="containment"></a>Contenimento

Dopo aver rilevato un incidente di sicurezza, è importante contenere l'intrusione prima che l'avversario possa accedere a più risorse o causare più danni. L'obiettivo principale delle procedure di risposta agli incidenti di sicurezza è limitare l'impatto sui clienti o sui dati o sui sistemi, servizi e applicazioni Microsoft.

## <a name="eradication"></a>Eradicazione

L'eliminazione è il processo di eliminazione della causa principale dell'incidente di sicurezza con un elevato grado di sicurezza. L'obiettivo è duplice:

- per eliminare completamente l'avversario dall'ambiente
- per mitigare la vulnerabilità (se nota) che ha abilitato o potrebbe consentire all'avversario di reimmersi nell'ambiente.

A seconda della natura dell'incidente, dell'ambito dell'incidente di sicurezza, della profondità della penetrazione e delle possibili ripercussioni, il team di risposta alla sicurezza consiglia ai team di servizio di adottare tecniche di eradicazione. Considerando il potenziale impatto aziendale che può essere causato da questi passaggi di eradicazione, queste decisioni verranno prese dai team di servizio e dal team di risposta alla sicurezza dopo un'analisi dettagliata e l'approvazione da parte del Executive Incident Manager (se necessario).

## <a name="recovery"></a>Ripristino

Quando il team di risposta ottiene un ragionevole livello di sicurezza che l'avversario è stato rimosso dall'ambiente e tutti i percorsi vulnerabili noti sono stati eliminati, i singoli team di servizio avvieranno i passaggi di ripristino per portare il servizio a una configurazione nota e corretta. Questi passaggi di ripristino saranno in consultazione con il team di risposta alla sicurezza. Questa attività include l'identificazione dell'ultimo stato valido noto del servizio, il ripristino dai backup a questo stato, l'ispezione dei percorsi di attacco vulnerabili nello stato ripristinato e così via. Il team di risposta alla sicurezza, in consultazione con i team di servizio, determinerà il miglior piano di ripristino possibile per l'ambiente.

Un aspetto chiave per il ripristino è avere una maggiore vigilanza e controlli per verificare che il piano di ripristino sia stato eseguito correttamente e che non vi siano segni di violazione nell'ambiente.

## <a name="customer-notification-of-security-incident"></a>Notifica al cliente di un evento imprevisto di sicurezza

Se Microsoft determina che si è verificato un incidente di sicurezza, microsoft informerà l'utente con un ritardo indebito e entro i requisiti contrattuali e di conformità concordati. Dopo aver identificato tutti i tenant interessati, il team di comunicazione corrispondente lavora per identificare eventuali normative rilevanti che potrebbero essere applicate ai tenant interessati. Il team delle comunicazioni utilizza il canale di comunicazione appropriato definito nelle normative applicabili per inviare una notifica al contatto tenant appropriato.

La notifica includerà informazioni dettagliate sull'evento imprevisto, ad esempio una descrizione dell'evento imprevisto, l'effetto sui dati dei clienti, se presenti, le azioni intraprese da Microsoft e/o le azioni suggerite ai clienti per risolvere il problema e impedire la ricorrenza. La notifica verrà recapitata agli amministratori designati del tenant dei servizi online Microsoft. Per assicurarsi che le notifiche siano ricevute, è necessario assicurarsi che gli amministratori forniranno e mantengano informazioni di contatto accurate nei profili tenant. Inoltre, a seconda della natura dell'incidente, i clienti Microsoft 365 possono ricevere una notifica anche tramite il dashboard Microsoft 365 [Service Health Dashboard](http://status.yammer.com/).

## <a name="related-articles"></a>Articoli correlati

- [Gestione degli incidenti di sicurezza Microsoft](assurance-security-incident-management.md)
- [Gestione degli incidenti di sicurezza Microsoft: preparazione](assurance-sim-preparation.md)
- [Gestione degli incidenti di sicurezza Microsoft: rilevamento e analisi](assurance-sim-detection-analysis.md)
- [Gestione degli incidenti di sicurezza Microsoft: attività post-incidente](assurance-sim-post-incident-activity.md)
- [Come registrare un ticket di supporto per gli eventi di sicurezza](/azure/security/fundamentals/event-support-ticket)
- [Notifica di violazione nell'ambito del GDPR in Azure e Dynamics 365](/compliance/regulatory/gdpr-breach-azure-dynamics)
