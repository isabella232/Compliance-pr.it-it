---
title: Registrazione interna di Microsoft 365 per la progettazione di Microsoft 365
description: In questo articolo viene fornita una spiegazione del funzionamento della registrazione interna per i team di Microsoft 365 Engineering.
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
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 110a61c27a00380eede4d4f2303acfb025a27a1f
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497068"
---
# <a name="internal-logging-for-microsoft-365-engineering"></a>Log interni per Microsoft 365 Engineering

Oltre agli eventi e ai dati di registro disponibili per i clienti, è disponibile anche un sistema di raccolta dei dati di log interno disponibile per i tecnici di Microsoft 365 presso Microsoft. Molti tipi diversi di dati di registro vengono caricati dai server Microsoft 365 in un servizio di elaborazione dei big data interno denominato Cosmos. Ogni team del servizio carica i log di controllo dai rispettivi server nel database Cosmos per l'aggregazione e l'analisi. Questo trasferimento di dati avviene tramite una connessione TLS convalidata da FIPS 140-2 su porte e protocolli approvati in modo specifico utilizzando uno strumento di automazione proprietario denominato Office Data Loader (ODL). Gli strumenti utilizzati in Microsoft 365 per raccogliere ed elaborare i record di controllo non consentono modifiche permanenti o irreversibili al contenuto del record di controllo originale o all'ordinamento temporale.

I team di servizio utilizzano Cosmos come archivio centralizzato per eseguire un'analisi dell'utilizzo delle applicazioni, per misurare le prestazioni di sistema e operative e per cercare anomalie e modelli che potrebbero indicare problemi o problemi di sicurezza. Ogni team del servizio carica una linea di base dei log in Cosmos, a seconda di ciò che sta cercando di analizzare, che spesso includono:

- Registri eventi
- Log di AppLocker
- Dati sulle prestazioni
- Dati di System Center
- Record dettagli chiamata
- Dati sulla qualità dell'esperienza
- Registri del server Web IIS
- SQL Server log
- Dati Syslog
- Log di controllo della sicurezza

Prima di caricare dati in Cosmos, l'applicazione ODL utilizza un servizio di scrubbing per offuscare tutti i campi che contengono i dati dei clienti, ad esempio informazioni sul tenant e informazioni identificabili dall'utente finale, e sostituire tali campi con un valore hash. I log anonimi e con hash vengono riscritti e quindi caricati in Cosmos. I team di servizio eseguono query con ambito sui propri dati in Cosmos per la correlazione, l'avviso e la creazione di report. Il periodo di conservazione dei dati del log di controllo in Cosmos è determinato dai team del servizio; la maggior parte dei dati del log di controllo viene conservata per 90 giorni o più per supportare le indagini degli incidenti di sicurezza e per soddisfare i requisiti di conservazione normativi.

L'accesso ai dati di Microsoft 365 archiviati in Cosmos è limitato al personale autorizzato. Microsoft limita la gestione delle funzionalità di controllo al sottoinsieme limitato di membri del team di servizio responsabili della funzionalità di controllo. Questi membri del team non hanno la possibilità di modificare o eliminare dati da Cosmos e tutte le modifiche apportate ai meccanismi di registrazione per Cosmos vengono registrate e verificate.

Ogni team del servizio accede ai propri dati di log per l'analisi autorizzando determinate applicazioni a eseguire analisi specifiche. Ad esempio, il team di sicurezza di Microsoft 365 usa i dati di Cosmos tramite un parser del registro eventi proprietario per correlare, avvisare e generare report utilizzabili su possibili attività sospette nell'ambiente di produzione di Microsoft 365. I report di questi dati vengono utilizzati per correggere le vulnerabilità e migliorare le prestazioni complessive del servizio. Se un avviso o un report specifico richiede ulteriori indagini, il personale del servizio può richiedere che i dati siano importati di nuovo nel servizio Microsoft 365. Poiché il registro specifico importato da Cosmos è crittografato e il personale del servizio non ha accesso alle chiavi di decrittografia, il registro di destinazione viene passato a livello di programmazione tramite un servizio di decrittografia che restituisce risultati con ambito al personale del servizio autorizzato. Tutte le vulnerabilità riscontrate in questo esercizio vengono segnalate e riassegnate utilizzando i canali standard di gestione degli incidenti di sicurezza di Microsoft.
