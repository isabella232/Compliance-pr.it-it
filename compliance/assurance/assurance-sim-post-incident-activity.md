---
title: 'Gestione degli incidenti di sicurezza Microsoft: attività post-incidente'
description: In questo articolo viene fornita una panoramica del processo di attività post-incidente di gestione degli incidenti di sicurezza nei servizi online Microsoft.
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.localizationpriority: medium
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
ms.openlocfilehash: 820c912dc55d5cc98cedc38676b5039591cf5baa
ms.sourcegitcommit: 4c00fd65d418065d7f53216c91f455ccb3891c77
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/23/2021
ms.locfileid: "58481678"
---
# <a name="microsoft-security-incident-management-post-incident-activity"></a>Gestione degli incidenti di sicurezza Microsoft: attività post-incidente

## <a name="postmortem"></a>Postmortem

Alcuni incidenti di sicurezza, in particolare quelli che hanno un impatto sul cliente o che causano una violazione dei dati, sono soggetti a un evento imprevisto completo post-mortem. Il team di risposta alla sicurezza conduce un postmortem dettagliato con tutte le parti coinvolte nella risposta a eventi imprevisti di sicurezza a:

- Documentare la sequenza di eventi che hanno causato l'evento imprevisto.
- Creare un riepilogo tecnico dell'incidente come supportato dalle prove che includono gli attori coinvolti nella violazione (se noto). Questo riepilogo includerà la modalità di esecuzione della risposta e altre operazioni da asporto chiave.
- Identificare le interruzioni tecniche, gli errori procedurali, gli errori manuali, i difetti del processo e glitch di comunicazione e/o eventuali vettori di attacco precedentemente sconosciuti identificati durante la risposta agli incidenti di sicurezza.

Il postmortem influirà direttamente sul miglioramento dei servizi online Microsoft, sui processi operativi e sulla documentazione impostando nuove priorità nel ciclo di sviluppo di progettazione dei servizi online Microsoft.

## <a name="documentation"></a>Documentazione

Tutti i principali risultati tecnici del processo post-mortem vengono acquisiti in un report e gli investimenti nel servizio o le correzioni sotto forma di bug o richieste di modifica dello sviluppo. Questi risultati vengono seguiti dai team di progettazione appropriati. Per gli errori di processo e i problemi inter-organizzativi, i problemi sono documentati nel database del team di risposta alla sicurezza e seguiti con i gruppi appropriati per affrontarli.

## <a name="process-improvement"></a>Miglioramento dei processi

La risposta a un incidente di sicurezza nei servizi online Microsoft implica il coordinamento con più gruppi distribuiti tra organizzazioni diverse all'interno di Microsoft e organizzazioni esterne potenzialmente appropriate come le forze dell'ordine. Sappiamo che è fondamentale valutare le nostre risposte dopo ogni incidente di sicurezza sia per la sufficienza che per la completezza. Per eventuali miglioramenti o modifiche identificati, il team di risposta alla sicurezza valuta i suggerimenti in consultazione con i team e gli stakeholder appropriati e, se appropriato, li incorpora nelle procedure operative standard. Tutte le modifiche, i bug o i miglioramenti del servizio necessari identificati durante l'attività post-postmortem o di risposta agli incidenti di sicurezza vengono registrati e registrati in un database di progettazione Microsoft interno. Tutti i potenziali bug o funzionalità vengono assegnati al proprietario appropriato. Il team di risposta alla sicurezza Microsoft esamina tutte le voci finché il problema non viene risolto.

## <a name="related-articles"></a>Articoli correlati

- [Gestione degli incidenti di sicurezza Microsoft](assurance-security-incident-management.md)
- [Gestione degli incidenti di sicurezza Microsoft: preparazione](assurance-sim-preparation.md)
- [Gestione degli incidenti di sicurezza Microsoft: rilevamento e analisi](assurance-sim-detection-analysis.md)
- [Gestione degli incidenti di sicurezza Microsoft: contenimento, eliminazione e ripristino](assurance-sim-containment-eradication-recovery.md)
- [Come registrare un ticket di supporto per gli eventi di sicurezza](/azure/security/fundamentals/event-support-ticket)
- [Notifica di violazione nell'ambito del GDPR in Azure e Dynamics 365](/compliance/regulatory/gdpr-breach-azure-dynamics)
