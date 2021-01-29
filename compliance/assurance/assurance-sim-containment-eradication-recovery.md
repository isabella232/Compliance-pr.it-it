---
title: 'Gestione degli incidenti di sicurezza di Microsoft 365: contenimento, eliminazione e ripristino'
description: In questo articolo viene fornita una panoramica del processo di contenimento, eliminazione e ripristino degli incidenti di sicurezza in Microsoft 365.
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
ms.openlocfilehash: 702735ed2ba35a4f3b0a02123f0c58b5fb4d397e
ms.sourcegitcommit: d67e4d4fdc664f1da450c8ef2f6732e19bdd403a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/28/2021
ms.locfileid: "50037606"
---
# <a name="microsoft-365-security-incident-management-containment-eradication-and-recovery"></a>Gestione degli incidenti di sicurezza di Microsoft 365: contenimento, eliminazione e ripristino

In base all'analisi eseguita dal team di Microsoft 365 Security Response, dal team del servizio e da altri, viene sviluppato un piano di contenimento e ripristino appropriato per ridurre al minimo l'effetto dell'incidente di sicurezza. I team di servizio appropriati applicano quindi il piano in produzione con il supporto del team di Microsoft 365 Security Response.

## <a name="containment"></a>Contenimento

Dopo aver rilevato un incidente di sicurezza, è importante contenere l'intrusione prima che l'antagonante possa accedere a più risorse o causare più danni. L'obiettivo principale delle procedure di risposta agli incidenti di sicurezza è limitare l'impatto sui clienti o sui loro dati o su sistemi, servizi e applicazioni Microsoft.

## <a name="eradication"></a>Eradicazione

L'eliminazione è il processo di eliminazione della causa principale dell'incidente di sicurezza con un elevato grado di sicurezza. L'obiettivo è duplice:

- per eliminare completamente l'antagonale dall'ambiente
- per attenuare la vulnerabilità (se nota) che ha abilitato o potrebbe consentire all'antagonista di reimmersi nell'ambiente.

A seconda della natura dell'incidente, dell'ambito dell'incidente di sicurezza, della profondità della penetrazione e delle possibili ripercussioni, il team di Microsoft 365 Security Response consiglia ai team di servizio di adottare tecniche di eliminazione. Considerando il potenziale impatto aziendale che può essere causato da questi passaggi di eliminazione, queste decisioni verranno prese dai team di servizio e dal team di Microsoft 365 Security Response dopo un'analisi dettagliata e l'approvazione da parte del Executive Incident Manager (se necessario).

## <a name="recovery"></a>Ripristino

Quando il team di risposta ottiene un livello ragionevole di sicurezza che l'antagono è stato eliminato dall'ambiente e che tutti i percorsi vulnerabili noti sono stati eliminati, i singoli team di servizio avvieranno i passaggi di ripristino per portare il servizio a una configurazione nota e valida. Questi passaggi di ripristino saranno in consultazione con il team di Microsoft 365 Security Response. Questa attività include l'identificazione dell'ultimo stato valido noto del servizio, il ripristino dai backup a questo stato, l'analisi dei percorsi di attacco vulnerabili nello stato ripristinato e così via. Il team di Microsoft 365 Security Response, in consultazione con i team di servizio, determinerà il piano di ripristino migliore possibile per l'ambiente.

Un aspetto chiave del ripristino è disporre di controlli e vigilanza ottimizzati per verificare che il piano di ripristino sia stato eseguito correttamente e che non vi siano segni di violazione nell'ambiente.

## <a name="customer-notification-of-security-incident"></a>Notifica dell'incidente di sicurezza da parte del cliente

Se Microsoft determina che si è verificato un incidente di sicurezza, microsoft informerà l'utente con un ritardo indebito e entro i requisiti contrattuali e di conformità concordati. Dopo aver identificato tutti i tenant interessati, il team delle comunicazioni di Microsoft 365 Customer Experience (CxP) lavora per identificare eventuali normative rilevanti applicabili ai tenant interessati. Il team delle comunicazioni CxP di Microsoft 365 utilizza il canale di comunicazione appropriato definito nelle normative applicabili per inviare una notifica al contatto tenant appropriato.

La notifica includerà informazioni dettagliate sull'incidente, ad esempio una descrizione dell'incidente, l'effetto sui dati dei clienti, se presenti, le azioni intraprese da Microsoft e/o le azioni suggerite dai clienti per risolvere il problema e impedire la ricorrenza. La notifica verrà recapitata agli amministratori designati del tenant di Microsoft 365. Per assicurarsi che le notifiche siano ricevute, è necessario assicurarsi che gli amministratori forniranno e mantengano accurate informazioni di contatto nei propri profili tenant. Inoltre, a seconda della natura dell'incidente, i clienti possono ricevere una notifica[](http://status.yammer.com/) anche tramite il dashboard sull'integrità dei servizi di Microsoft 365.

## <a name="related-articles"></a>Articoli correlati

- [Gestione degli incidenti di sicurezza di Microsoft 365](assurance-security-incident-management.md)
- [Preparazione della gestione degli incidenti di sicurezza di Microsoft 365](assurance-sim-preparation.md)
- [Rilevamento e analisi degli incidenti di sicurezza di Microsoft 365](assurance-sim-detection-analysis.md)
- [Attività post-incidente di gestione degli incidenti di sicurezza di Microsoft 365](assurance-sim-post-incident-activity.md)
