---
title: Resilienza dei dati in Microsoft 365
description: In questo articolo, informazioni sulla progettazione e sui principi di resilienza e ripristino dei dati in Microsoft 365.
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
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 48fe50347e7e81c7e5f8552299c04a268b8b449c
ms.sourcegitcommit: 4c00fd65d418065d7f53216c91f455ccb3891c77
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/23/2021
ms.locfileid: "58482109"
---
# <a name="data-resiliency-in-microsoft-365"></a>Resilienza dei dati in Microsoft 365

Data la natura complessa del cloud computing, Microsoft è consaci del fatto che non è un caso se le cose andranno storte, ma piuttosto quando. Progettiamo i nostri servizi cloud per ottimizzare l'affidabilità e ridurre al minimo gli effetti negativi sui clienti in caso di problemi. È stata superata la strategia tradizionale di basarsi su un'infrastruttura fisica complessa e la ridondanza è stata creata direttamente nei servizi cloud. Usiamo una combinazione di un'infrastruttura fisica meno complessa e di un software più intelligente che crea resilienza dei dati nei nostri servizi e offre disponibilità elevata ai nostri clienti.

## <a name="resiliency-and-recoverability-are-built-in"></a>Resilienza e recuperabilità sono integrate

La creazione di resilienza e ripristino inizia dal presupposto che l'infrastruttura e i processi sottostanti avranno esito negativo a un certo punto: l'hardware (infrastruttura) avrà esito negativo, gli umani commetteranno errori e il software avrà bug. Anche se non sarebbe corretto dire che gli sviluppatori di software non stavano pensando a queste cose prima del cloud, il modo in cui questi problemi sono stati gestiti in un'implementazione IT tipica era diverso prima del cloud:

- In primo luogo, le protezioni hardware e dell'infrastruttura sono state significative. Questa struttura significava che i datacenter con affidabilità del 99,99% richiedevano una notevole ridondanza di alimentazione e rete e i server venivano implementati con clustering basato su hardware, alimentatori doppi, interfacce di rete doppie e simili.
- In secondo momento, il processo era fondamentale. I team delle operazioni hanno mantenuto procedure rigorose, sono state impiegate finestre di modifica e spesso si è presente un notevole sovraccarico per la gestione dei progetti.
- In terzo luogo, la distribuzione ha avuto luogo a un ritmo glaciale. La distribuzione del codice senza possedere l'origine significava attendere i rilasci delle patch e le versioni principali comportavano la sostituzione dell'hardware e un notevole aumento di capitale. Inoltre, l'unico modo per correggere un problema era il rollback. Di conseguenza, la maggior parte delle organizzazioni IT distribuisce solo le versioni principali per evitare il lavoro da eseguire per mantenersi aggiornati.
- Infine, la scala dei sistemi distribuiti e il livello di interconnessione erano storicamente molto più piccoli di quanto non lo sia ora.

Oggi, i clienti si aspettano un'innovazione continua da Microsoft senza compromettere la qualità e questo è uno dei motivi per cui i servizi e il software microsoft sono creati con resilienza e recuperabilità in mente.

## <a name="microsoft-365-data-resiliency-principles"></a>Microsoft 365 di resilienza dei dati

La resilienza si riferisce alla capacità di un servizio basato su cloud di sopportare determinati tipi di errori e di rimanere completamente funzionante dal punto di vista dei clienti. La resilienza dei dati significa che, indipendentemente da quali errori si verificano all'interno Microsoft 365, i dati critici dei clienti rimangono intatti e inalterati. A tale scopo, i Microsoft 365 sono stati progettati in base a cinque principi di resilienza specifici:

- Sono presenti dati critici e non critici. I dati non critici (ad esempio, se un messaggio è stato letto) possono essere eliminati in rari scenari di errore. I dati critici (ad esempio, i dati dei clienti come i messaggi di posta elettronica) devono essere protetti a costi estremi. Come obiettivo di progettazione, i messaggi di posta elettronica recapitati sono sempre critici e aspetti come la lettura di un messaggio non sono critici.
- Le copie dei dati dei clienti devono essere separate in diverse aree di errore o nel maggior numero possibile di domini di errore (ad esempio datacenter, accessibili con credenziali singole (processo, server o operatore)) per garantire l'isolamento degli errori. 
- I dati critici dei clienti devono essere monitorati per eventuali errori di atomicità, coerenza, isolamento, durabilità (ACID).
- I dati dei clienti devono essere protetti da danneggiamenti. Deve essere analizzato o monitorato attivamente, ripristinabile e ripristinabile.
- La maggior parte dei risultati della perdita di dati deriva dalle azioni dei clienti, quindi consenti ai clienti di recuperare da soli usando un'interfaccia utente grafica che consente loro di ripristinare gli elementi eliminati accidentalmente.

Grazie alla creazione dei servizi cloud a questi principi, insieme a test e convalida affidabili, Microsoft 365 è in grado di soddisfare e superare i requisiti dei clienti garantendo al contempo una piattaforma per l'innovazione e il miglioramento continui.

## <a name="related-articles"></a>Articoli correlati

- [Gestione della corruzione dei dati](assurance-dealing-with-data-corruption.md)
- [Protezione malware e ransomware](assurance-malware-and-ransomware-protection.md)
- [Il monitoraggio e la riparazione automatica](assurance-monitoring-and-self-healing.md)
- [Exchange Resilienza dei dati](assurance-exchange-data-resiliency.md)
