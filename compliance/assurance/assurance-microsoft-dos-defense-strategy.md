---
title: Strategia di difesa Denial of Service Microsoft
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
ms.openlocfilehash: ba0d0bbea11000144d7091455c6ee204f2c17037
ms.sourcegitcommit: 856111c112a30160950fdd0ce94369aff7e176dc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/23/2021
ms.locfileid: "59489373"
---
# <a name="microsoft-denial-of-service-defense-strategy"></a>Strategia di difesa Denial of Service Microsoft

## <a name="denial-of-service-defense-strategy"></a>Strategia di difesa da attacchi Denial of Service

La strategia di Microsoft per la difesa dagli attacchi DDoS (Distributed Denial-of-Service) basati sulla rete è unica a causa di un'ampia impronta globale, consentendo a Microsoft di utilizzare strategie e tecniche non disponibili per la maggior parte delle altre organizzazioni. Inoltre, Microsoft contribuisce e si attinge da conoscenze collettive aggregate da una vasta rete di intelligence sulle minacce, che include partner Microsoft e la più ampia community di sicurezza Internet. Questa intelligence, insieme alle informazioni raccolte dai servizi online e dalla base di clienti globale di Microsoft, migliora continuamente il sistema di difesa DDoS di Microsoft che protegge tutti gli asset dei servizi online Microsoft.

Il cardine della strategia DDoS di Microsoft è la presenza globale. Microsoft interagisce con provider Internet, provider di peering (pubblici e privati) e società private in tutto il mondo. Questo impegno garantisce a Microsoft una presenza internet significativa e consente a Microsoft di assorbire gli attacchi su una superficie di grandi dimensioni

Poiché la capacità perimetrale di Microsoft è aumentata nel tempo, il significato degli attacchi contro i singoli bordi è notevolmente diminuito. A causa di questa diminuzione, Microsoft ha separato i componenti di rilevamento e mitigazione del sistema di prevenzione DDoS. Microsoft distribuisce sistemi di rilevamento a più livelli nei datacenter regionali per rilevare gli attacchi più vicini ai loro punti di saturazione, mantenendo la mitigazione globale nei nodi perimetrali. Questa strategia garantisce che servizi Microsoft gestire più attacchi simultanei.

Una delle difese più efficaci e a basso costo impiegate da Microsoft contro gli attacchi DDoS è la riduzione delle superfici di attacco del servizio. Il traffico indesiderato viene rilasciato sul perimetro di rete invece di analizzare, elaborare e pulire i dati inline.

Nell'interfaccia con la rete pubblica, Microsoft usa dispositivi di sicurezza speciali per le funzioni di firewall, conversione degli indirizzi di rete e filtro IP. Microsoft utilizza anche il routing ECMP (Equal-Cost Multi-Path) globale. Il routing ECMP globale è un framework di rete per garantire che siano presenti più percorsi globali per raggiungere un servizio. Con più percorsi per ogni servizio, gli attacchi DDoS sono limitati all'area da cui proviene l'attacco. Le altre aree geografiche non devono essere interessate dall'attacco, poiché gli utenti finali userebbero altri percorsi per raggiungere il servizio in tali aree. Microsoft ha inoltre sviluppato sistemi di correlazione e rilevamento DDoS interni che utilizzano dati di flusso, metriche delle prestazioni e altre informazioni per rilevare rapidamente gli attacchi DDoS.

Per proteggere ulteriormente i servizi cloud, Microsoft usa Azure DDoS Protection, un sistema di difesa DDoS integrato nei processi di monitoraggio continuo e test di penetrazione di Microsoft Azure. Azure DDoS Protection è progettato non solo per resistere agli attacchi esterni, ma anche per gli attacchi di altri tenant di Azure. Azure usa tecniche di rilevamento e mitigazione standard come i cookie SYN, la limitazione della velocità e i limiti di connessione per proteggere dagli attacchi DDoS. Per supportare le protezioni automatizzate, un team di risposta agli incidenti DDoS tra carichi di lavoro identifica i ruoli e le responsabilità tra i team, i criteri per le escalation e i protocolli per la gestione degli incidenti tra i team interessati.

La maggior parte degli attacchi DDoS lanciati contro destinazioni si tratta dei livelli Rete (L3) e Trasporto (L4) del modello [OSI (Open Systems Interconnection).](/windows-hardware/drivers/network/windows-network-architecture-and-the-osi-model) Gli attacchi indirizzati ai livelli L3 e L4 sono progettati per inondare un'interfaccia di rete o un servizio con traffico di attacco per sovraccaricare le risorse e negare la possibilità di rispondere al traffico legittimo. Per proteggersi dagli attacchi L3 e L4, le soluzioni DDoS di Microsoft usano i dati di campionamento del traffico dai router del datacenter per salvaguardare l'infrastruttura e gli obiettivi dei clienti. I dati di campionamento del traffico vengono analizzati da un servizio di monitoraggio della rete per rilevare gli attacchi. Quando viene rilevato un attacco, vengono avviati meccanismi di difesa automatizzati per mitigare l'attacco e garantire che il traffico di attacco diretto a un cliente non si trascino in danni collaterali o una riduzione della qualità del servizio di rete per altri clienti.

Microsoft adotta anche un approccio offensivo alla difesa DDoS. Le botnet sono una comune fonte di comando e controllo per condurre attacchi DDoS per amplificare gli attacchi e mantenere l'anonimato. L'unità microsoft per crimini digitali (DCU) si concentra sull'identificazione, l'analisi e l'interruzione dell'infrastruttura di distribuzione e comunicazione di malware per ridurre la scalabilità e l'impatto delle botnet.

## <a name="application-level-defenses"></a>Difese a livello di applicazione

I servizi cloud di Microsoft sono creati intenzionalmente per supportare carichi elevati, che consentono di proteggere dagli attacchi DDoS a livello di applicazione. L'architettura con scalabilità orizzontale di Microsoft distribuisce i servizi tra più datacenter globali con funzionalità di isolamento regionale e limitazione specifiche del carico di lavoro per i carichi di lavoro pertinenti.

Il paese o l'area geografica di ogni cliente, identificato dall'amministratore del cliente durante la configurazione iniziale dei servizi, determina la posizione di archiviazione principale per i dati del cliente. I dati dei clienti vengono replicati tra datacenter ridondanti in base a una strategia principale/di backup. Un datacenter principale ospita il software dell'applicazione insieme a tutti i dati principali dei clienti in esecuzione sul software. Un datacenter di backup fornisce il failover automatico. Se il datacenter principale smette di funzionare per qualsiasi motivo, le richieste vengono reindirizzate alla copia del software e dei dati dei clienti nel datacenter di backup. In un determinato momento, i dati dei clienti possono essere elaborati nel datacenter principale o di backup. La distribuzione dei dati tra più datacenter riduce l'area di superficie interessata nel caso in cui un datacenter sia stato attaccato. Inoltre, i servizi nel datacenter interessato possono essere reindirizzati rapidamente al datacenter secondario per mantenere la disponibilità durante un attacco e reindirizzati di nuovo al datacenter principale dopo aver attenuato un attacco.

Come ulteriore mitigazione degli attacchi DDoS, i singoli carichi di lavoro includono funzionalità integrate che gestiscono l'utilizzo delle risorse. Ad esempio, i meccanismi di limitazione in Exchange Online e SharePoint Online fanno parte di un approccio multistrato per la difesa dagli attacchi DDoS.

database SQL di Azure dispone di un ulteriore livello di sicurezza sotto forma di un servizio gateway denominato DoSGuard che tiene traccia dei tentativi di accesso non riusciti in base all'indirizzo IP. Se viene raggiunta la soglia per i tentativi di accesso non riusciti dallo stesso IP, DoSGuard blocca l'indirizzo per un periodo di tempo prestadeterminato.

## <a name="resources"></a>Risorse

- [Panoramica di Azure DDoS Protection Standard](/azure/ddos-protection/ddos-protection-overview)
- [Procedure consigliate fondamentali di Azure DDoS Protection Standard](/azure/ddos-protection/fundamental-best-practices)
- [Componenti di una strategia di risposta DDoS](/azure/ddos-protection/ddos-response-strategy)
