---
title: Microsoft 365 registrazione interna per Microsoft 365 progettazione
description: In questo articolo viene fornita una spiegazione del funzionamento della registrazione interna per Microsoft 365 team di progettazione.
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
ms.openlocfilehash: 71b08509ae920ad88ecfa1566b9a11d640b0534f
ms.sourcegitcommit: fb379d1110a9a86c7f9bab8c484dc3f4b3dfd6f0
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/23/2021
ms.locfileid: "53088595"
---
# <a name="internal-logging-for-microsoft-365-engineering"></a>Log interni per Microsoft 365 Engineering

Oltre agli eventi e ai dati di registro disponibili per i clienti, Microsoft gestisce un sistema di raccolta dei dati di registro interno disponibile per Microsoft 365 tecnici. Molti tipi diversi di dati di registro vengono caricati dai server Microsoft 365 in una soluzione di monitoraggio della sicurezza proprietaria per l'analisi NRT (Near Real-Time) e un servizio di elaborazione dei big data (Cosmos) interno per l'archiviazione a lungo termine. Questo trasferimento dei dati avviene tramite una connessione TLS convalidata da FIPS 140-2 su porte e protocolli approvati utilizzando uno strumento di automazione proprietario denominato Office Data Loader (ODL). Gli strumenti utilizzati in Microsoft 365 per raccogliere ed elaborare i record di controllo non consentono modifiche permanenti o irreversibili al contenuto del record di controllo originale o all'ordinamento temporale.

I team di servizio utilizzano Cosmos come archivio centralizzato per eseguire un'analisi dell'utilizzo delle applicazioni, per misurare le prestazioni del sistema e delle operazioni e per cercare anomalie e modelli che potrebbero indicare problemi o problemi di sicurezza. Ogni team del servizio carica una linea di base che include:

- Registri eventi
- Log di AppLocker
- Dati sulle prestazioni
- System Center dati
- Record dettagli chiamata
- Dati sulla qualità dell'esperienza
- Registri del server Web IIS
- SQL Server log
- Dati Syslog
- Log di controllo della sicurezza

Prima del caricamento, l'applicazione ODL utilizza un servizio di scrubbing per rimuovere tutti i campi che contengono i dati dei clienti, ad esempio le informazioni sul tenant e le informazioni identificabili dall'utente finale, e sostituire tali campi con un valore hash. I log scrubbed vengono caricati in Cosmos e nella soluzione di monitoraggio della sicurezza NRT che analizza i registri alla ricerca di potenziali eventi di sicurezza e indicatori di prestazioni. Il periodo di conservazione dei dati del log di controllo Cosmos è determinato dai team del servizio; la maggior parte dei dati del log di controllo viene conservata per 90 giorni o più per supportare le indagini degli incidenti di sicurezza e per soddisfare i requisiti di conservazione normativi.

L'accesso Microsoft 365 dati archiviati in Cosmos è limitato al personale autorizzato. Microsoft limita la gestione dei log di controllo a un sottoinsieme limitato di membri del team di sicurezza responsabili della funzionalità di controllo. Il team di sicurezza non dispone dell'accesso amministrativo permanente Cosmos e tutte le modifiche vengono registrate e verificate.

Dopo l'analisi NRT, ogni team del servizio può utilizzare strumenti di analisi e dashboard per la correlazione dei dati, le query interattive e l'analisi dei dati. Questi report vengono utilizzati per monitorare e migliorare le prestazioni complessive del servizio.
