---
title: Strategia di Microsoft 365 per la protezione contro gli attacchi Denial of Service
description: In questo articolo è possibile trovare una panoramica della strategia di difesa Microsoft per gli attacchi Denial of Service (DoS).
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
ms.openlocfilehash: 56888f704d3cc5da5e820e3cb80a3d10cbb1ef95
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/12/2021
ms.locfileid: "59159169"
---
# <a name="microsoft-365-denial-of-service-defense-strategy"></a>Strategia di Microsoft 365 per la protezione contro gli attacchi Denial of Service

## <a name="core-principles-of-defense-against-denial-of-service-attacks"></a>Principi fondamentali di protezione contro gli attacchi Denial of Service

Esistono tre principi di base per la difesa da attacchi DoS (Denial of Service) basati sulla rete: l'assorbimento, il rilevamento e la mitigazione. L'absorption avviene prima del rilevamento e il rilevamento deve verificarsi prima di iniziare la mitigazione. Se anche un piccolo attacco DoS non può essere assorbito, i servizi non sopravviveranno abbastanza a lungo da poter essere rilevato. Rilevando un attacco prima che il sistema venga sovraccaricato, i difensori possono implementare un piano di risposta.

La formula seguente consente di approssimare il tempo di impatto di un attacco DoS:

  **Capacità massima (in byte/sec) / Velocità di crescita (in byte/sec) = Tempo di impatto (in sec)**

Se il time-to-detection è più lungo del time-to-impact, l'attacco DoS avrà probabilmente esito positivo. Se il time-to-detection è più breve del time-to-impact, i servizi attaccati devono rimanere online e accessibili se le strategie di mitigazione hanno esito positivo.

Di conseguenza, esistono due strategie principali per la difesa dagli attacchi DoS:

- Aumentare la capacità per aumentare il limite massimo di capacità (che a sua volta fornisce più tempo per rilevare un attacco); o
- Ridurre il tempo necessario per rilevare un attacco.

Un vantaggio per la sicurezza dell'utilizzo dei servizi cloud Microsoft è il modo in cui i servizi cloud su servizi Microsoft offrono una protezione di rete solida ai clienti cloud in modo conveniente. Anche su larga scala, deve esserci un equilibrio tra l'assorbimento, il rilevamento e la mitigazione. Per trovare questo equilibrio, Microsoft valuta i tassi di crescita degli attacchi per stimare la servizi Microsoft necessario assorbire.

## <a name="denial-of-service-defense-strategy"></a>Strategia di difesa da attacchi Denial of Service

La strategia di Microsoft per difendersi dagli attacchi DoS basati sulla rete è unica a causa della scalabilità e del footprint globale. Questa scala consente a Microsoft di utilizzare strategie e tecniche non disponibili per la maggior parte delle altre organizzazioni. Il cardine della strategia DoS è la presenza globale. Microsoft interagisce con provider Internet, provider di peering (pubblici e privati) e società private in tutto il mondo. Questo impegno offre a Microsoft una presenza significativa su Internet e consente a Microsoft di assorbire gli attacchi su una superficie di grandi dimensioni.

Poiché la capacità perimetrale di Microsoft è aumentata nel tempo, il significato degli attacchi contro i singoli bordi è notevolmente diminuito. A causa di questa diminuzione, Microsoft ha separato i componenti di rilevamento e mitigazione del sistema di prevenzione DoS. Microsoft distribuisce sistemi di rilevamento a più livelli nei datacenter regionali per rilevare gli attacchi più vicini ai loro punti di saturazione, mantenendo la mitigazione globale nei nodi perimetrali. Questa strategia garantisce che servizi Microsoft gestire più attacchi simultanei.

Una delle difese più efficaci e a basso costo impiegate da Microsoft contro gli attacchi DoS è la riduzione delle superfici di attacco del servizio. Il traffico indesiderato viene rilasciato sul perimetro di rete invece di analizzare, elaborare e pulire i dati inline.

Nell'interfaccia con la rete pubblica, Microsoft usa dispositivi di sicurezza speciali per le funzioni di firewall, conversione degli indirizzi di rete e filtro IP. Microsoft utilizza anche il routing ECMP (Equal-Cost Multi-Path) globale. Il routing ECMP globale è un framework di rete per garantire che siano presenti più percorsi globali per raggiungere un servizio. Con più percorsi per ogni servizio, gli attacchi DoS sono limitati all'area da cui proviene l'attacco. Le altre aree geografiche non devono essere interessate dall'attacco, poiché gli utenti finali userebbero altri percorsi per raggiungere il servizio in tali aree. Microsoft ha inoltre sviluppato sistemi di correlazione e rilevamento DoS interni che utilizzano dati di flusso, metriche delle prestazioni e altre informazioni per rilevare rapidamente gli attacchi DoS.

Per proteggere ulteriormente i servizi cloud, Microsoft 365 usa un sistema di difesa DDoS (Denial of Service) distribuito integrato nei processi di monitoraggio continuo e test di penetrazione di Microsoft Azure. Il sistema di difesa DDoS di Azure è progettato non solo per resistere agli attacchi esterni, ma anche per gli attacchi di altri tenant di Azure. Azure usa tecniche di rilevamento e mitigazione standard come i cookie SYN, la limitazione della velocità e i limiti di connessione per proteggere dagli attacchi DDoS. Per supportare le protezioni automatizzate, un team di risposta agli incidenti DoS tra carichi di lavoro identifica i ruoli e le responsabilità tra i team, i criteri per le escalation e i protocolli per la gestione degli incidenti tra i team interessati.

La maggior parte degli attacchi DoS lanciati contro destinazioni si tratta dei livelli Rete (L3) e Trasporto (L4) del modello [OSI (Open Systems Interconnection).](/windows-hardware/drivers/network/windows-network-architecture-and-the-osi-model) Gli attacchi indirizzati ai livelli L3 e L4 sono progettati per inondare un'interfaccia di rete o un servizio con traffico di attacco per sovraccaricare le risorse e negare la possibilità di rispondere al traffico legittimo. Per proteggersi dagli attacchi L3 e L4, le soluzioni DoS di Microsoft usano i dati di campionamento del traffico provenienti dai router del datacenter per salvaguardare l'infrastruttura e gli obiettivi dei clienti. I dati di campionamento del traffico vengono analizzati da un servizio di monitoraggio della rete per rilevare gli attacchi. Quando viene rilevato un attacco, vengono avviati meccanismi di difesa automatizzati per mitigare l'attacco e garantire che il traffico di attacco diretto a un cliente non si trascino in danni collaterali o una riduzione della qualità del servizio di rete per altri clienti.

## <a name="application-level-defenses"></a>Difese a livello di applicazione

I team di progettazione Microsoft seguono i rigorosi standard impostati da [Microsoft Operational Security Assurance](https://www.microsoft.com/SDL/OperationalSecurityAssurance) per proteggere i dati dei clienti. I servizi cloud di Microsoft sono stati creati intenzionalmente per supportare carichi elevati, che consentono di proteggere dagli attacchi DoS a livello di applicazione. Microsoft 365'architettura con scalabilità orizzontale distribuisce i servizi tra più datacenter globali con funzionalità di isolamento regionale e limitazione specifiche del carico di lavoro per i carichi di lavoro pertinenti.

Il paese o l'area geografica di ogni cliente, identificato dall'amministratore del cliente durante la configurazione iniziale dei servizi, determina la posizione di archiviazione principale per i dati del cliente. I dati dei clienti vengono replicati tra datacenter ridondanti in base a una strategia principale/di backup. Un datacenter principale ospita il software dell'applicazione insieme a tutti i dati principali dei clienti in esecuzione sul software. Un datacenter di backup fornisce il failover automatico. Se il datacenter principale smette di funzionare per qualsiasi motivo, le richieste vengono reindirizzate alla copia del software e dei dati dei clienti nel datacenter di backup. In un determinato momento, i dati dei clienti possono essere elaborati nel datacenter principale o di backup. La distribuzione dei dati tra più datacenter riduce l'area di superficie interessata nel caso in cui un datacenter sia stato attaccato. Inoltre, i servizi nel datacenter interessato possono essere reindirizzati rapidamente al datacenter secondario per mantenere la disponibilità durante un attacco e reindirizzati di nuovo al datacenter principale dopo aver attenuato un attacco.

Come ulteriore mitigazione dagli attacchi DoS, i singoli carichi di lavoro includono funzionalità integrate che gestiscono l'utilizzo delle risorse. Ad esempio, i meccanismi di limitazione in Exchange Online e SharePoint Online fanno parte di un approccio a più livelli per la difesa dagli attacchi DoS.
