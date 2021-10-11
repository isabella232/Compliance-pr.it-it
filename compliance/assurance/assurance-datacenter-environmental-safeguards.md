---
title: Misure di sicurezza ambientali del datacenter
description: Altre informazioni sulle misure di protezione ambientale dei datacenter Microsoft.
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
ms.openlocfilehash: 525aab55d3f56490ecd1f1da1e00d6c5ddd32dc4
ms.sourcegitcommit: cf424cb1e7c12048120977f294f780b776119a96
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/11/2021
ms.locfileid: "60265110"
---
# <a name="datacenter-environmental-safeguards"></a>Misure di sicurezza ambientali del datacenter

Microsoft usa diverse misure di sicurezza per proteggere dalle minacce ambientali alla disponibilità dei datacenter. Queste misure di sicurezza consentono a Microsoft di fornire piattaforme cloud sicure e disponibili attendibili dai clienti.

## <a name="site-selection"></a>Selezione della sede

La protezione dei data center Microsoft dai rischi ambientali inizia con la selezione della sede. Le località dei data center Microsoft vengono sottoposte a una valutazione rigorosa prima della selezione per la costruzione del data center. I siti datacenter Microsoft sono selezionati strategicamente per ridurre al minimo i rischi causati da diversi fattori, tra cui alluvioni, sisma, uragani e altre catastrofi naturali. Inoltre per ridurre al minimo i rischi ambientali, l'accesso a energia a basso costo e un'infrastruttura di telecomunicazioni affidabile sono tra i principali fattori chiave che influenzano la selezione della sede del data center.

## <a name="climate-control"></a>Controllo del clima

Il controllo del clima è un componente fondamentale dell'infrastruttura cruciale all'interno di un data center e viene usato per monitorare e mantenere spazi condizionati ottimizzati per il personale e le apparecchiature/hardware. Il carico termico (come biprodotto del consumo di energia) e l'umidità devono essere gestiti per garantire condizioni operative appropriate tramite l'intervento meccanico. Le condizioni climatiche locali, i vari requisiti normativi e i vincoli determineranno il modo più efficiente per ottenerlo.

I livelli di temperatura e umidità vengono mantenuti in conformità ai requisiti ambientali dell'hardware IT previsto in ogni datacenter. I data center Microsoft mantengono un contratto di livello operativo con i propri clienti in modo che l'efficienza ottimale sia soddisfatta pur mantenendo i requisiti ambientali minimi. I livelli di temperatura e umidità vengono monitorati continuamente dal sistema BMS (Building Management System) del datacenter. I membri del team di Ambienti critici (CE) monitorano il sistema BMS dal Centro operativo delle strutture (FOC), in modo che possano gestire la temperatura e l'umidità all'interno del datacenter prima del superamento dei punti di allarme. BMS è configurato per inviare una notifica al team CE quando vengono raggiunti determinati indicatori, che quindi analizzano e apportano modifiche per risolvere il problema del clima. Gli intervalli accettabili per la temperatura e l'umidità sono coerenti con le linee guida dell'American Society of Heating, Refrigerating, and Air-conditioning Engineers (ASHRAE) o linee guida applicabili localmente simili. L'umidità del datacenter è misurata in base alla percentuale di umidità relativa, non di condensa con l'intervallo corrente compreso tra il 40%-55%. L'intervallo di temperatura è in genere compreso tra 18 gradi Celsius e 27 gradi Celsius (tra 64,4 gradi Fahrenheit e 80,6 gradi Fahrenheit).

## <a name="fire-and-water-damage-protection"></a>Protezione da danni causati da incendi e inondazioni

Microsoft impiega sistemi di rilevamento e estinzione di incendi all’avanguardia all'interno di ogni stabilimento dei data center. I sistemi di prevenzione degli incendi sono supportati da una fonte di energia indipendente per garantire la protezione dei dipendenti e dell'infrastruttura Microsoft in caso di incendio. Gli stabilimenti dei data center sono inoltre protetti dai danni causati dalle inondazioni grazie a sensori d'acqua posizionati in aree ritenute a rischio di perdita. Questi sensori d’acqua informano rapidamente il personale preposto in caso di emergenza correlata all'acqua. Le valvole di arresto dell'acqua sono progettate per essere accessibili e i dipendenti vengono debitamente addestrati sul loro funzionamento e sulla loro collocazione.

I datacenter Microsoft implementano meccanismi di rilevamento degli incendi affidabili, tra cui rilevatori di fumo fotoelettrici installati sotto il pavimento e sul soffitto, sistemi VESDA (Very Early Smoke Detection Apparatus) Xtralis in ogni colocation, caselle di allarme antincendio della stazione di pull-station installate in tutti i datacenter, estintori situati in tutti i datacenter, pattuglie del personale di sicurezza in tutte le aree di costruzione più volte ogni turno di otto ore,  e i sistemi di rilevamento/eliminazione e illuminazione di emergenza sono collegati ai sistemi di alimentazione di backup del datacenter che forniscono una fonte di alimentazione ridondante. Le aree contenenti apparecchiature elettriche sensibili sono protette da sistemi di spolvero a doppio interblocco pre-azione (condotto a secco).

Il team CE esegue una procedura walk-through giornaliera del sito (DSWT) per controllare ogni sala e molte parti componenti in esse contenute per garantire che vengano soddisfatti tutti i requisiti di controllo antincendio.

Microsoft utilizza dispositivi/sistemi di rilevamento degli incendi per il sistema di informazioni che si attivano automaticamente e informano il personale del datacenter insieme ai soccorritori in caso di incendio. Se uno dei meccanismi di rilevamento degli incendi viene attivato in qualsiasi spazio di colocation, il reparto antincendio locale e il Global Security Operations Center di Redmond, Washington vengono automaticamente avvisati. I sistemi di protezione antincendio e rilevamento sono collegati al sistema di sicurezza che notifica la struttura locale e il personale di sicurezza.

Microsoft fornisce il rilevamento di acqua/perdite in aree con rischio di perdite d'acqua. I sistemi di eliminazione degli incendi hanno anche allarmi di rilevamento delle perdite monitorati. Il sistema di rilevamento dell'acqua/perdita è integrato con il sistema di allarme e notifica della struttura e i sistemi di spolvero all'interno dei datacenter sono distribuiti in zone. I team DI E e Datacenter Management hanno familiarità con le procedure di emergenza che richiedono l'uso delle valvole di arresto dell'acqua e delle loro posizioni. I risertori per la cosparsa possono essere spenti singolarmente o come gruppo tramite valvole cancello. Tutti gli spolveratori nello spazio critico sono due tipi di anti-azione interlock che richiedono due forme di attivazione prima dell'avvio del flusso. La pressione del sistema di spolvero viene monitorata e allarmata dalle perdite d'acqua.

## <a name="health-and-safety"></a>Salute e sicurezza

L'impegno per la salute e la sicurezza dei dipendenti Microsoft è fondamentale per misurare il successo. I data center Microsoft operano in conformità alle normative locali, regionali, nazionali e federali in materia di salute e sicurezza. Nella maggior parte dei casi, i criteri di integrità e sicurezza di Microsoft superano i requisiti normativi e governativi per garantire la protezione dell'integrità, della sicurezza e del benessere di tutti i lavoratori del datacenter durante tutte le fasi del ciclo di vita del datacenter, dalla costruzione alla rimozione delle autorizzazioni. I piani di gestione della sicurezza, la valutazione dei rischi, la gestione delle attività ad alto rischio e la formazione sulla sicurezza sono elementi centrali per fornire un ambiente di lavoro sicuro per tutti i dipendenti.

## <a name="energy-efficiency"></a>Efficienza energetica

Microsoft opera ad emissioni zero dal 2012. Entro il 2030, Microsoft sarà carbon negative e, entro il 2050, Microsoft avrà rimosso dall'ambiente tutto il carbone emesso dall'azienda direttamente o dal consumo elettrico dalla sua fondazione nel 1975. Entro il 2025, i datacenter Microsoft saranno forniti da energia rinnovabile al 100%. Per raggiungere questo obiettivo, Microsoft ha implementato strumenti contrattuali come i contratti di acquisto di energia per la generazione di proxy per l'energia verde per fornire il 100% dell'energia elettrica a emissione di co2 consumata da tutti i datacenter.
