---
title: Monitoraggio dei dati e auto-riparazione in Microsoft 365
description: In questo articolo sono disponibili informazioni sulle funzionalità di monitoraggio e auto-riparazione di Microsoft 365.
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
ms.custom:
- seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: d4188448038a3b47c2cf7a0a8193f1772740eb7f
ms.sourcegitcommit: 4c00fd65d418065d7f53216c91f455ccb3891c77
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/23/2021
ms.locfileid: "58481848"
---
# <a name="data-monitoring-and-self-healing-in-microsoft-365"></a>Monitoraggio dei dati e auto-riparazione in Microsoft 365

Data la scala di Microsoft 365, sarebbe impossibile mantenere i dati dei clienti resilienti e sicuri dal malware senza un monitoraggio integrato che sia completo, un avviso intelligente e un'auto-riparazione veloce e affidabile. Il monitoraggio di un set di servizi su scala Microsoft 365 è molto impegnativo. È necessario introdurre nuove metodologie e nuove tecnologie per gestire il servizio in un ambiente globale connesso. Ci siamo allontanati dal tradizionale approccio di monitoraggio della raccolta e del filtro dei dati per creare avvisi per un approccio basato sull'analisi dei dati; prendere segnali e creare fiducia in questi dati e quindi usare l'automazione per ripristinare o risolvere il problema. Questo approccio consente agli utenti di uscire dall'equazione di ripristino, il che a sua volta rende le operazioni meno costose, veloci e meno erre di errore. 

Fondamentale per Microsoft 365 è una raccolta di tecnologie che costituiscono il motore di data Insights, basato su Azure, SQL Azure e la tecnologia di database di [streaming open source.](https://cassandra.apache.org/) È progettato per raccogliere e aggregare i dati e raggiungere conclusioni. Attualmente, elabora più di 500 milioni di eventi all'ora da più di 100.000 server (circa 15 TB al giorno) distribuiti in decine di datacenter in molte aree geografiche e questi numeri sono in crescita. 

Microsoft 365 utilizza *il monitoraggio esterno,* che implica la creazione di transazioni sintetiche per testare tutto ciò che è importante. Ad esempio, in Exchange Online ogni scenario testa ogni database in tutto il mondo ogni cinque minuti in modo sparso, fornendo una copertura quasi continua di tutto ciò che risiede nel sistema. Da più posizioni, vengono eseguite 250 milioni di transazioni di test al giorno per creare una solida previsione o heartbeat per il servizio. 

Microsoft 365 usa anche il concetto di Red *Alert,* che riduce tutti i segnali di monitoraggio da tutti i computer dei nostri datacenter a qualcosa di gestibile da un essere umano. Il concetto è piuttosto semplice: se qualcosa accade su più segnali, deve essere presente qualcosa. Non si tratta di creare fiducia in un segnale, ma di avere una fedeltà ragionevole per ogni segnale in modo da ottenere una maggiore accuratezza. Questo sistema di monitoraggio è così potente che non abbiamo personale 24x7 che guarda i monitor; tutto ciò che abbiamo è il macchinario che si sveglia se rileva un problema, nel qual caso verrà visualizzato il personale di chiamata appropriato, o più spesso, come nel caso, andrà avanti e risolverà il problema. Una volta che iniziamo a raccogliere segnali e a creare avvisi rossi, possiamo iniziare a triangolare tutte le partizioni del servizio. 

In base alla combinazione dell'avviso di errore e degli avvisi rossi, questo avviso indica esattamente quali componenti potrebbero avere un problema e che il sistema tenterà di risolvere il problema da solo riavviando un server cassette postali. 

Oltre alle funzionalità di auto-correzione, ad esempio il ripristino di una singola pagina, Exchange Online include diverse funzionalità che accettano un approccio al monitoraggio e all'auto-correzione che si concentra sulla conservazione dell'esperienza dell'utente finale. Queste funzionalità includono *Disponibilità gestita*, che fornisce azioni di monitoraggio e ripristino integrate, e AutoReseed, che ripristina automaticamente la ridondanza del database dopo un errore del disco. 

## <a name="managed-availability"></a>Disponibilità gestita 

La disponibilità gestita offre una soluzione nativa per il controllo dell'integrità e il ripristino che monitora e protegge l'esperienza dell'utente finale tramite azioni orientate al ripristino. La disponibilità gestita è l'integrazione di azioni di monitoraggio e ripristino integrate con la Exchange a disponibilità elevata. Tale piattaforma è stata progettata per rilevare e risolvere i problemi non appena si verificano e vengono rilevati dal sistema. Diversamente dalle precedenti soluzioni e tecniche di monitoraggio esterno di Exchange, la disponibilità gestita non cerca di identificare o comunicare la causa principale di un problema. Al contrario, si concentra sugli aspetti di ripristino che riguardano tre aree chiave dell'esperienza dell'utente finale:

- **Disponibilità:** gli utenti possono accedere al servizio? 
- **Latenza-** Come si verifica l'esperienza per gli utenti? 
- **Errori:** gli utenti sono in grado di eseguire le attività desiderate? 

La disponibilità gestita è una funzionalità interna che viene eseguita in Microsoft 365 server che esegue Exchange Online. Effettua il polling e analizza centinaia di metriche di integrità ogni secondo. Se viene rilevato un problema, la maggior parte delle volte viene risolto automaticamente. Tuttavia, ci saranno sempre problemi che la disponibilità gestita non sarà in grado di risolvere da sola. In questi casi, la disponibilità gestita inoltrare il problema a un team Microsoft 365 supporto tecnico tramite la registrazione degli eventi.

## <a name="autoreseed"></a>Reseeding automatico

Exchange Online server vengono distribuiti in una configurazione che archivia più database e i relativi flussi di log sullo stesso disco non RAID. Questa configurazione viene spesso  definita solo un gruppo di dischi (JBOD) perché non vengono utilizzati meccanismi di ridondanza di archiviazione, ad esempio RAID, per duplicare i dati sul disco. Quando si verifica un errore di un disco in un ambiente JBOD, i dati su tale disco vengono persi. 

Date le dimensioni di Exchange Online e il fatto che la distribuzione al suo interno è di milioni di unità disco, gli errori delle unità disco sono un'occorrenza regolare in Exchange Online. Infatti, più di 100 errori ogni giorno. Quando si verifica un errore di un disco in una distribuzione aziendale locale, un amministratore deve sostituire manualmente il disco con errori e ripristinare i dati interessati. In una distribuzione cloud le dimensioni Microsoft 365, la sostituzione manuale dei dischi da parte degli operatori (amministratori cloud) non è pratica né economicamente fattibile. 

Il reseeding automatico, o *AutoReseed,* è una funzionalità che rappresenta la sostituzione di un'azione normalmente guidata dall'operatore in risposta a un errore del disco, a un evento di danneggiamento del database o a un altro problema che richiede il reseeding di una copia del database. L'AutoReseed è stato ideato per ripristinare automaticamente la ridondanza del database a seguito di un errore del disco utilizzando dischi di riserva forniti con il sistema. In caso di errore di un disco, le copie del database archiviate su tale disco vengono reseede automaticamente su un disco di riserva preconfigurato nel server, ripristinando in tal modo la ridondanza. 