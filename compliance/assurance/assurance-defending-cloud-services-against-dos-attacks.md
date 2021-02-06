---
title: Protezione dei servizi cloud di Microsoft 365 da attacchi Denial of Service
description: In questo articolo viene illustrato come Microsoft difende i servizi cloud da attacchi Denial of Service (DoS).
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
ms.openlocfilehash: e632c1524d5cc8c21aec9dab3d95d285a3b8801e
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120575"
---
# <a name="defending-microsoft-365-cloud-services-against-denial-of-service-attacks"></a>Protezione dei servizi cloud di Microsoft 365 da attacchi Denial of Service

I data center Microsoft sono protetti da una sicurezza di difesa approfondita che include scherma perimetrale, videocamere, personale di sicurezza e accessi sicuri che usano biometria, smart card e autenticazione a più fattori. La sicurezza di difesa approfondita continua in ogni area della struttura e in ogni unità server fisica. Microsoft [Cloud Infrastructure and Operations Group](https://www.microsoft.com/cloud-platform/global-datacenters) fornisce l'infrastruttura di base e le tecnologie di base per i servizi cloud. I nostri datacenter sono conformi agli standard di settore per la sicurezza fisica e l'affidabilità e vengono gestiti, monitorati e amministrati dal personale operativo Microsoft.

Per proteggere ulteriormente i servizi cloud, Microsoft fornisce un sistema di difesa DDoS che fa parte dei processi di monitoraggio continuo e test di penetrazione di Microsoft Azure. Il sistema di difesa DDoS di Azure è progettato non solo per resistere agli attacchi dall'esterno, ma anche da altri tenant di Azure. Azure usa tecniche di rilevamento e mitigazione standard come i cookie SYN, la limitazione della velocità e i limiti di connessione per proteggere gli attacchi DDoS.

I servizi cloud di Microsoft sono soggetti alla minaccia di attacchi da più origini. Per mitigare e proteggere dalle varie minacce DoS, è stato sviluppato e implementato un sistema di rilevamento e mitigazione delle minacce altamente scalabile e dinamico basato su Azure con l'obiettivo principale di proteggere l'infrastruttura sottostante dagli attacchi DoS e di evitare interruzioni dei servizi per i clienti di servizi cloud. Il sistema di mitigazione DoS di Azure protegge il traffico in ingresso, in uscita e da area geografica a area.

La maggior parte degli attacchi DoS è stata lanciata contro destinazioni ai livelli Rete (L3) e Trasporto (L4) del modello [OSI (Open Systems Interconnection).](/windows-hardware/drivers/network/windows-network-architecture-and-the-osi-model) Gli attacchi indirizzati ai livelli L3 e L4 sono progettati per inondare un'interfaccia di rete o un servizio con traffico di attacco per sovraccaricare le risorse e negare la possibilità di rispondere al traffico legittimo. In particolare, gli attacchi L3 e L4 tentano di saturare la capacità di collegamenti di rete, dispositivi o servizi o sovraccaricare le CPU dei server o delle macchine virtuali che supportano un'applicazione.

Per proteggersi dagli attacchi L3 e L4, Microsoft ha progettato, sviluppato e distribuito una soluzione mirata in modo specifico alla protezione dell'infrastruttura e degli obiettivi dei clienti che vengono aggrediti proteggendo questi livelli. La protezione dell'infrastruttura garantisce che il traffico di attacco destinato a un cliente non comporta danni collaterali o una riduzione della qualità del servizio di rete per altri clienti. La soluzione utilizza i dati di campionamento del traffico dai router del datacenter. Questi dati vengono analizzati da un servizio di monitoraggio della rete per rilevare gli attacchi. Quando viene rilevato un attacco, vengono avviati meccanismi di difesa automatizzati.

## <a name="application-level-defenses"></a>Application-Level difesa
I team di progettazione Microsoft seguono i rigorosi standard impostati da [Microsoft Operational Security Assurance](https://www.microsoft.com/SDL/OperationalSecurityAssurance) per proteggere i dati dei clienti. I servizi cloud di Microsoft sono intenzionalmente creati per supportare un carico molto elevato e per proteggere e ridurre gli attacchi DoS a livello di applicazione. È stata implementata un'architettura con scalabilità orizzontale in cui i servizi vengono distribuiti tra più datacenter globali con isolamento regionale e funzionalità di limitazione in alcuni dei carichi di lavoro.

Il paese o l'area geografica di ogni cliente, identificato dall'amministratore del cliente durante la configurazione iniziale dei servizi, determina la posizione di archiviazione principale per i dati del cliente. I dati dei clienti vengono replicati tra datacenter ridondanti in base a una strategia principale/di backup. Un datacenter principale ospita il software dell'applicazione insieme a tutti i dati principali del cliente in esecuzione sul software. Un datacenter di backup fornisce il failover automatico. Se il datacenter principale cessa di funzionare per qualsiasi motivo, le richieste vengono reindirizzate alla copia del software e dei dati dei clienti nel datacenter di backup. In un determinato momento, i dati dei clienti possono essere elaborati nel datacenter principale o di backup. La distribuzione dei dati tra più datacenter riduce l'area di superficie interessata nel caso in cui un datacenter sia stato aggredito. Inoltre, i servizi nel datacenter interessato possono essere reindirizzati rapidamente al datacenter secondario come uno dei meccanismi di ripristino e viceversa (reindirizzati al datacenter primario dopo il ripristino del servizio).

I singoli carichi di lavoro includono funzionalità incorporate che gestiscono l'utilizzo delle risorse. Ad esempio, i meccanismi di limitazione in Exchange Online e SharePoint Online fanno parte di un approccio a più livelli per la protezione dagli attacchi DoS. La limitazione per gli utenti di Exchange Online si basa sul livello di risorse utilizzate dall'utente finale, indipendentemente dal fatto che le risorse si trovano in Active Directory, nell'archivio informazioni di Exchange Online o altrove. Un budget viene allocato a ogni client per limitare le risorse utilizzate da un utente. La limitazione di Exchange Online per l'attività degli utenti e i componenti di sistema si basa sulla [gestione del carico di lavoro.](https://technet.microsoft.com/library/jj150503(v=exchg.150).aspx) Un carico di lavoro di Exchange Online è una funzionalità, un protocollo o un servizio di Exchange Online esplicitamente definito ai fini della gestione delle risorse di sistema di Exchange Online. Ogni carico di lavoro di Exchange Online richiede risorse di sistema come CPU, operazioni del database delle cassette postali o richieste di Active Directory per eseguire richieste utente o lavoro in background. Esempi di carichi di lavoro di Exchange Online includono Outlook sul Web, Exchange ActiveSync, migrazione delle cassette postali e assistenti cassette postali. Gli amministratori tenant possono gestire le impostazioni di limitazione della gestione dei carichi di lavoro di Exchange per gli utenti con Exchange Management Shell. In Exchange Online sono state implementate varie forme di limitazione, tra cui PowerShell, Servizi Web Exchange e POP e IMAP, Exchange ActiveSync, connessioni a dispositivi mobili, destinatari e altro ancora. Anche se gli amministratori delle distribuzioni locali di Exchange possono configurare i criteri di limitazione, gli amministratori non possono configurare i criteri di limitazione per Exchange Online.

Il trigger più comune per la limitazione in SharePoint Online è il codice CSOM (Client-Side Object Model) che esegue troppe azioni con una frequenza troppo elevata. Con CSOM, è possibile eseguire molte azioni con una singola richiesta, che può superare i limiti di utilizzo e causare limitazioni per utente.

Indipendentemente dall'attività che potrebbe comportare la limitazione, quando un utente supera i limiti di utilizzo, SharePoint Online limita eventuali ulteriori richieste da tale account utente, in genere per un breve periodo. Mentre è in vigore una limitazione utente, tutte le azioni eseguite da tale utente vengono limitate fino alla scadenza della limitazione, in base ai criteri seguenti:
- Per le richieste eseguite dall'utente direttamente in un browser, SharePoint Online reindirizza a una pagina di informazioni sulla limitazione e le richieste hanno esito negativo.
- Per tutte le altre richieste, incluse le chiamate CSOM, SharePoint Online restituisce il codice di stato HTTP 429 ("troppe richieste") e le richieste hanno esito negativo.

Se il processo incrinte continua a superare i limiti di utilizzo, SharePoint Online potrebbe bloccare completamente il processo e restituire il codice di stato HTTP 503 ("servizio non disponibile").

## <a name="vulnerability-and-penetration-testing"></a>Test di vulnerabilità e penetrazione
Microsoft usa [](https://www.microsoft.com/trustcenter/security/threatmanagement) molte tecnologie e procedure di sicurezza per proteggere l'infrastruttura [cloud](https://blogs.technet.microsoft.com/hybridcloud/2015/05/05/protecting-your-datacenter-and-cloud-from-emerging-threats/) e le reti locali da minacce moderne e sofisticate, tra cui l'uso di componenti e servizi antimalware per servizi cloud, macchine virtuali (VM) e altri sistemi. Advanced Threat Analytics, che monitora i normali modelli di utilizzo per reti, sistemi e utenti e usa l'apprendimento automatico per contrassegnare qualsiasi comportamento fuori dal normale e regolare test di penetrazione.

Oltre a eseguire i test di penetrazione e offrire ai clienti un programma di test di penetrazione unificato di [Microsoft Cloud,](https://technet.microsoft.com/mt784683)ci impegniamo anche con professionisti della sicurezza di terze parti che eseguono valutazioni regolari della vulnerabilità e test di penetrazione nei servizi cloud. Rendiamo disponibili per il download i report di queste valutazioni di vulnerabilità di terze parti dai portali [Service Trust](https://aka.ms/STP) e [Service Assurance.](https://aka.ms/ServiceAssurance)
