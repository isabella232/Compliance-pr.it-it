---
title: Distruzione dei dati in Microsoft 365
description: Panoramica dei criteri Microsoft relativi al riciclo, all'eliminazione o alla distruzione delle unità disco e dei server dei data center di Microsoft 365.
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
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
f1.keywords:
- NOCSH
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 1b9d410422e22fe67cb27617ba16e2ddbbaec0fd
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497643"
---
# <a name="data-destruction-in-microsoft-365"></a>Distruzione dei dati in Microsoft 365

## <a name="physical-data-destruction"></a>Distruzione fisica dei dati

Microsoft dispone di criteri standard per la gestione dei dati che si occupa del riciclo e dell'eliminazione delle unità disco e dei server non riusciti o ritirati. Prima di riutilizzare le unità disco di Microsoft 365, Microsoft esegue un processo di sanitizzazione fisica coerente con la pubblicazione speciale 800-88 del National Institute of Standards and Technology[(NIST SP 800-88 Guidelines for Media Sanitization).](https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-88r1.pdf) Poiché tutte le unità disco in Microsoft 365 sono crittografate utilizzando la crittografia a livello di volume BitLocker, la cancellazione conforme a NIST SP 800-88 non è tecnicamente necessaria. Tuttavia, Microsoft esegue questo processo.

I dischi con problemi utilizzati nei datacenter di Microsoft 365 vengono fisicamente distrutti e controllati tramite il processo ISO. Il tipo di risorsa determina il mezzo di eliminazione appropriato. Per i dischi rigidi che non possono essere cancellati, Microsoft usa un processo di distruzione per distruggere i supporti e rendere impossibile il ripristino delle informazioni. Ad esempio, i dischi vengono distrutti fisicamente, pulverizzati o inceneriti. Microsoft conserva tutti i record della distruzione ed esegue un processo di sanizzazione simile sui server riutilizzati all'interno di Microsoft 365. Queste linee guida includono la sanità di sanità fisica e elettronica.

Ogni datacenter usa un processo di distruzione fisica sul posto per eliminare i propri dischi. I cestini sicuri per i supporti di archiviazione designati per l'eliminazione dei dischi sono presenti in ogni area del datacenter. Ogni stazione bin sicura dispone di videosorveglianza di monitoraggio video. Una volta che un cestino di eliminazione raggiunge circa il 50% di capacità, il team di Servizi sito contatta il team di sicurezza fisica per coordinare la rimozione. Il personale dei servizi del sito e un Ufficio sicurezza rimuovono il cestino di eliminazione sicuro e lo collocano in un'area di archiviazione protetta designata. I criteri e le procedure che regolano la gestione dei dispositivi di rilevamento dei dati durante lo smaltimento vengono regolarmente testati, incluse le procedure per garantire la condizione di macchine approvate per la distruzione.

Nel processo di distruzione dei dati, i dischi vengono cancellati in modo conforme al NIST 800-88 (se possibile) e quindi inseriti in uno shredder industriale e demoliti fisicamente. Microsoft mantiene la responsabilità per gli asset che lasciano il datacenter usando NIST SP 800-88 pulizia/eliminazione coerenti, distruzione degli asset, crittografia, inventario accurato, monitoraggio e protezione della catena di custodia durante il trasporto. Questo processo viene monitorato tramite la tv a circuito chiuso e al termine viene rilasciato un certificato di distruzione.

Microsoft usa unità di cancellazione dei dati [da Extreme Protocol Solutions](https://www.enterprisedataerasure.com/) (EPS). Il software EPS supporta i requisiti NIST SP 800-88 per la pulizia e l'eliminazione/cancellazione sicura. Prima della pulizia o della distruzione, viene creato un inventario da Microsoft Asset Manager. Se un fornitore viene utilizzato per la distruzione, il fornitore fornisce un certificato di distruzione per ogni risorsa distrutta, convalidata dal gestore delle risorse.

## <a name="virtual-data-destruction"></a>Distruzione dei dati virtuali

Microsoft dispone di criteri e procedure di gestione dei dati che affrontano la distruzione virtuale effettiva dei dati per proteggersi dalla possibilità che i dati vengano condivisi in modo inappropriato tra i tenant del servizio o siano accessibili dopo l'eliminazione definitiva nel servizio. I dati eliminati dal servizio in un tenant non sono accessibili a un altro tenant del servizio, anche se viene riassegnato uno qualsiasi dell'archiviazione fisica sottostante. Questo è il risultato degli effetti composti di più tecnologie di virtualizzazione e frammentazione utilizzate per ridimensionare gli ambienti virtuali, i comportamenti di eliminazione attivi delle applicazioni all'interno di ogni tenant del servizio (ad esempio l'azzeramento delle [pagine)](/office365/securitycompliance/office-365-exchange-online-data-deletion#page-zeroing)e i processi di crittografia dei contenuti multimediali e delle applicazioni necessari.