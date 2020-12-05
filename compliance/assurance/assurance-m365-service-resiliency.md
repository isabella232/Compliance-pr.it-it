---
title: Resilienza del servizio incorporato in Microsoft 365
description: Descrizione della resilienza del servizio Microsoft 365
author: robmazz
ms.author: robmazz
manager: laurawi
ms.reviewer: sosstah
f1.keywords:
- NOCSH
audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Strat_O365_Enterprise
- MS-Compliance
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: ee9c7d898af13b9a1db95913a98be09eea8cd27f
ms.sourcegitcommit: 693bc6b1b51a5a9c9ff1758fa7f7ca3a204f147e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/04/2020
ms.locfileid: "49574758"
---
# <a name="built-in-service-resiliency-in-microsoft-365"></a>Resilienza del servizio incorporato in Microsoft 365

Come provider di servizi cloud, Microsoft riconosce la necessità di guadagnare continuamente la fiducia degli utenti fornendo soluzioni che funzionino in modo coerente e che piacciano agli utenti. Quando un servizio non è disponibile, si parla di tempo di inattività. La definizione del tempo di inattività varia in base a ogni servizio Microsoft 365, ma in genere sta a indicare un periodo di tempo in cui gli utenti non riescono a usare le funzionalità essenziali del servizio. Ad esempio, ecco la definizione di tempo di inattività per SharePoint Online, tratta dal contratto di servizio di Microsoft 365:

**“Tempo di inattività di SharePoint Online**: periodo di tempo in cui gli utenti non riescono né a leggere né a scrivere qualunque parte di una raccolta siti di SharePoint Online per cui dispongono delle autorizzazioni appropriate".

È possibile trovare le definizioni di tempo di inattività per ogni servizio nei [Contratti di servizio](https://www.microsoftvolumelicensing.com/DocumentSearch.aspx?Mode=3&DocumentTypeId=37).

Per ridurre al minimo i tempi di inattività, sia previsti che non previsti, i servizi di Microsoft 365 sono progettati e gestiti per essere altamente disponibili e resistenti ai guasti concentrandosi su quattro aree:

## <a name="activeactive-design"></a>Modello attivo/attivo

In Microsoft 365, stiamo guidando verso tutti i servizi architettati e gestiti in un progetto attivo/attivo che aumenta la resilienza. Ciò significa che sono sempre presenti più istanze di un servizio in esecuzione che possono rispondere alle richieste degli utenti, ospitate in data center geograficamente dispersi. Tutto il traffico degli utenti passa per il servizio Frontdoor di Microsoft e viene automaticamente instradato verso l'istanza del servizio meglio posizionata ed evitando qualsiasi errore di servizio per impedire o ridurre l'impatto sui clienti.

## <a name="reduce-incident-scope"></a>Ridurre la portata degli eventi imprevisti

La portata di un evento imprevisto relativo a un servizio viene misurata in base al livello di gravità, alla durata e al numero di clienti interessati. Per limitare la portata di tutti gli eventi imprevisti sono in atto le seguenti misure:

- avere più istanze di ogni servizio divise l’una dall’altra
- distribuire gli aggiornamenti in modo controllato e graduato usando anelli di convalida in modo che gli eventuali problemi che potrebbero derivare dall'aggiornamento possano essere individuati e attenuati all'inizio del processo di distribuzione. Questo consente di regressione dell'aggiornamento, se necessario, e si verifica per la prima volta in un piccolo gruppo all'interno di Microsoft (anello interno) prima che venga distribuito per gruppi di grandi dimensioni come tutti i 140.000 impiegati Microsoft (Ring 2), quindi per gli anelli Early Adopter (Ring 3) e infine per tutti i clienti globalmente (Ring 4).
- migliorare il monitoraggio tramite l’automazione. Microsoft 365 è un servizio di grandi dimensioni e il tempo di inesecuzione dell'obiettivo SLA è elevato. All'inizio di un evento imprevisto di un servizio, se gli esseri umani dovessero occuparsi del rilevamento e della risposta, non sarebbe possibile rispondervi abbastanza velocemente da rispettare il contratto di servizio. L'automazione è la chiave per individuare e rispondere in modo rapido ed efficace. Prima si viene a conoscenza di un problema, prima questo può essere risolto.

Insieme alle funzionalità attive/attive incorporate nell'architettura del servizio Microsoft 365, queste operazioni consentono di attenuare la gravità, la durata e il numero di clienti con impatto durante un incidente di servizio.  

## <a name="fault-isolation"></a>Isolamento del guasto

Così come i servizi sono progettati e gestiti in modo attivo/attivo e sono divisi l’uno dall’altro per evitare che un errore in uno di essi influisca su un altro, il code base del servizio viene sviluppato usando simili criteri di partizionamento denominati isolamento del guasto. Le misure di isolamento del guasto sono protezioni incrementali eseguite all'interno del code base stesso. Queste misure consentono di impedire che un problema verificatosi in un'area si propaghi ad altre aree di attività.
Le misure di isolamento del guasto vengono applicate in più fasi dello sviluppo e dell’emissione di un servizio, tra cui lo sviluppo del codice, la distribuzione del servizio, il bilanciamento del carico e la replica di database.

Il Microsoft Security Development Lifecycle (SDL) favorisce ulteriormente la resilienza e consiste in una serie di procedure che supportano i requisiti di sicurezza e conformità. SDL consente agli sviluppatori di creare servizi resilienti, sicuri e conformi. Gli elementi principali di SDL includono revisioni di codice, modellazione delle minacce, test di penetrazione e processi standard di risposta agli eventi imprevisti nel cloud di Microsoft.

I servizi di Microsoft 365 sono altamente interconnessi, ma i sistemi e le tecnologie alle loro spalle sono progettati in modo da limitare la propagazione dell’impatto dell’evento imprevisto di un servizio verso altri servizi. Un problema che colpisce Exchange Online, ad esempio, non influisce sulle funzionalità di base di Teams, e un problema relativo alla funzionalità di ricerca in SharePoint Online non influisce sulla possibilità per gli utenti di caricare o scaricare file.

## <a name="continuous-service-improvement"></a>Miglioramento continuo del servizio

Se si verifica un evento imprevisto, è importante prenderlo seriamente. Dopo tutto, l'architettura cloud ridondante e i rigorosi processi interni di Microsoft hanno l’obiettivo di mantenere accessibili i servizi. Nel corso di un evento imprevisto, il monitoraggio rileva rapidamente i servizi interessati e, se il tenant di un utente è interessato, l’utente riceve una notifica immediata attraverso diversi canali. Contemporaneamente, gli ingegneri seguono processi ben definiti per la valutazione del problema ed eseguono i passaggi necessari per ripristinare il funzionamento normale nel più breve tempo possibile. Una volta che il servizio funziona di nuovo normalmente, delle revisioni post-evento imprevisto vengono integrate nel ciclo di miglioramento continuo del servizio. Durante la revisione post-evento imprevisto vengono identificate le cause principali dell’evento imprevisto e gli elementi necessari alla risoluzione dei problemi. Infine, quello che si è imparato dalla situazione viene applicato ai modelli e alle operazioni dell’intera famiglia di prodotti. In questo modo è possibile evitare che la stessa causa principale influisca su altri servizi o altri clienti.
