---
title: Gestione delle risorse del datacenter
description: Panoramica della gestione degli asset del datacenter Microsoft.
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
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: fafba29a25c5b01fa37d091fb210185a98365192
ms.sourcegitcommit: b228be59e13ae2e05ba85f65c1d4648fef5e9260
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/14/2021
ms.locfileid: "60356385"
---
# <a name="datacenter-asset-management"></a>Gestione delle risorse del datacenter

I datacenter Microsoft sono formati da vari componenti fisici e virtuali, ognuno dei quali viene definito asset. Il gruppo di progettazione Microsoft Cloud Operations and Innovation (CO+I) segue processi standardizzati sicuri per la distribuzione, il monitoraggio e la rimozione delle autorizzazioni degli asset fisici e virtuali.

## <a name="supply-chain-integrity"></a>Integrità della catena di fornitura

La protezione degli asset inizia con la protezione della catena di approvvigionamento. Microsoft si impegna a garantire l'integrità della catena di fornitura e la sicurezza della catena di fornitura end-to end. I fornitori seguono rigorose procedure di catena di custodia durante il trasporto dei componenti cloud per ridurre il rischio di alterazione e manomissione. Tutto l'inventario in entrata e in uscita è attentamente ispezionato e monitorato per garantire l'integrità del firmware e dei componenti.

Le consegne di componenti del sistema in informazioni ai datacenter Microsoft sono in genere pianificate. Per le consegne non pianificate, Microsoft esamina attentamente e garantisce che siano approvati per l'ingresso in una sala computer Microsoft prima dell'immissione fisica. Quando un componente del sistema di informazioni entra nell'edificio, il team di gestione delle risorse confronta l'elemento ricevuto con il ticket di riferimento e analizza il dispositivo nello strumento di gestione delle risorse. Tutti i componenti del sistema di informazioni ricevuti o spediti vengono monitorati dallo strumento di gestione dei ticket del flusso di lavoro e nei log di spedizione nello strumento di gestione delle risorse. Ai visitatori è proibito l'uso di portatili e cellulari personali (ad eccezione delle chiamate di emergenza e delle note), anche se sono consentiti nell'ambiente di produzione (colocation). È vietato collegare cellulari a un dispositivo o scattare foto per ogni criterio del datacenter. Se l'attrezzatura che entra nel datacenter viene utilizzata a scopo di manutenzione, l'attrezzatura richiede l'approvazione di Gestione datacenter nel sistema Datacenter Access Tool.

## <a name="asset-inventory"></a>Inventario delle risorse

Microsoft richiede che tutte le risorse del data center siano contabilizzate e che abbiano un proprietario designato. I proprietari sono responsabili di mantenere aggiornate le informazioni per le risorse fisiche e virtuali. Quando nuove risorse fisiche vengono aggiunte a un data center, vengono firmate, scansionate, contrassegnate in modo univoco e archiviate nei sistemi di controllo dell'inventario. Gli strumenti di monitoraggio automatico aiutano a verificare le risorse fisiche e virtuali.

## <a name="asset-maintenance"></a>Manutenzione degli asset

Microsoft dispone di due team che forniscono diversi tipi di manutenzione delle risorse: i team ambiente critico (CE) e Servizi sito. Il team CE fornisce la gestione delle strutture per i sistemi elettrici, meccanici e fisici che costituiscono l'infrastruttura operativa della struttura. Pianificano, eseguono, documentano ed esaminano anche tutte le attività di manutenzione eseguite sui componenti CE. I datacenter Microsoft si basano su un sistema di gestione della manutenzione computerizzato per gestire le pianificazioni di manutenzione e gli ordini di lavoro. Il team di Site Services servizi tutti gli asset dei servizi online Microsoft che si trovano nei datacenter Microsoft. Inoltre, il team di Servizi sito fornisce supporto tecnico in loco e servizio di correzione delle interruzioni per gli asset appartenenti ai servizi di provisioning delle proprietà dal datacenter.

## <a name="asset-classification"></a>Classificazione delle risorse

Gli asset Microsoft, inclusi i dati, sono classificati in Enterprise linee guida per la tassonomia dei dati. Queste linee guida promuovono la standardizzazione nell'azienda e vengono esaminate e aggiornate ogni anno. Gli standard di classificazione e protezione degli asset delineano le procedure di sicurezza che i dipendenti devono seguire quando interagiscono con ogni risorsa. I clienti sono considerati proprietari dei propri dati memorizzati nell'ambiente cloud Microsoft. Le risorse di dati classificate come contenuto del cliente o dati del cliente sono protette dalle procedure di sicurezza applicabili.

Microsoft considera tutta la documentazione come risorsa di sistema. Il team di Site Services è responsabile della classificazione delle risorse e dell'utilizzo delle misure di sicurezza associate in base agli standard di classificazione e protezione degli asset, nonché agli eventuali requisiti aggiuntivi definiti dal team del servizio.

I proprietari degli asset devono assegnare ai propri asset una classificazione delle risorse, senza eccezioni. Negli ambienti datacenter Microsoft, gli asset fanno riferimento a server e dispositivi di rete. Altri supporti digitali come unità flash USB, dischi rigidi esterni o CD/DVD non vengono utilizzati per il funzionamento dei servizi. I supporti non digitali non vengono utilizzati nei datacenter.

## <a name="media-storage"></a>Spazio di archiviazione dei supporti

Gli asset multimediali digitali Microsoft sono archiviati fisicamente e in modo sicuro nelle sale di colocation del datacenter Microsoft. Sono disponibili più livelli di controlli di accesso fisico e videosorveglianza per proteggere e monitorare queste risorse. Quando gli asset multimediali digitali raggiungono la fine del ciclo di vita, vengono cancellati, eliminati o distrutti utilizzando metodi coerenti con NIST SP 800-88 prima dell'eliminazione. [L'articolo sulla distruzione dei dispositivi](assurance-data-bearing-device-destruction.md) di rilevamento dei dati illustra il processo di eliminazione sicura degli asset.

## <a name="media-transport"></a>Trasporto dei supporti

Microsoft limita le attività di trasporto degli asset al personale autorizzato attraverso protezioni a catena di custodia. L'uso di blocchi, sigilli a prova di manomissione e convalida obbligatoria dell'inventario delle risorse garantisce che solo il personale autorizzato sia coinvolto nel trasporto degli asset.

Tutti i supporti trasportati dai datacenter Microsoft richiedono un monitoraggio accurato. Microsoft ha stipulato contratti con diversi fornitori approvati per fornire servizi di spedizione sicuri. Il trasporto sicuro inizia con un inventario accurato e una catena di custodia. Nel luogo di consegna, il personale approvato dell'azienda di trasporto deve assistere alla rimozione del sigillo anti-manomissione e allo sblocco del contenitore. Il personale ricevente inventa la spedizione e invia un messaggio di conferma della ricezione delle risorse. Microsoft stipula inoltre contratti con un fornitore per fornire la distruzione delle attrezzature. A seconda della classificazione delle risorse, alcune attrezzature devono essere distrutte in sede.

Il trasporto di supporti digitali Microsoft al di fuori dello spazio controllato dalla sicurezza richiede la supervisione di due membri del team Datacenter Operations. Le risorse vengono continuamente accompagnate e supervisionate dal personale autorizzato fino a quando non vengono distrutte.

Il team di gestione del datacenter controlla la distribuzione e la rimozione dei componenti del sistema di informazioni tramite i ticket tracciati nello strumento di ticketing. Il recapito e la rimozione dei componenti del sistema di informazioni sono autorizzati dai proprietari del sistema.

## <a name="asset-retention"></a>Conservazione degli asset

Le risorse di proprietà di Microsoft vengono conservate nel modo appropriato in base ai requisiti di conservazione impostati da Gestione record aziendali, dalla classificazione delle risorse o dai requisiti contrattuali. Per ulteriori informazioni sulla conservazione dei dati, vedere [Conservazione, eliminazione](assurance-data-retention-deletion-and-destruction-overview.md)e distruzione dei dati in Microsoft 365 .
