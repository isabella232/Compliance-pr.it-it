---
title: Simulazione di un attacco in Microsoft 365
description: In questo articolo, scopri come Microsoft monitora e testa continuamente i limiti del tenant per Microsoft 365.
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
ms.openlocfilehash: ff5860197375d6504bc85f257a442915dfff50cc
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/12/2021
ms.locfileid: "59159631"
---
# <a name="attack-simulation-in-microsoft-365"></a>Simulazione di un attacco in Microsoft 365

Microsoft monitora costantemente e verifica in modo esplicito i punti deboli e le vulnerabilità nei limiti del tenant, tra cui il monitoraggio delle intrusioni, i tentativi di violazione delle autorizzazioni e la carestia delle risorse. Usiamo anche più sistemi interni per monitorare continuamente l'utilizzo improprio delle risorse, che, se rilevato, attiva la limitazione predefinita.

Microsoft 365 dispone di sistemi di monitoraggio interni che monitorano continuamente eventuali errori e guidano il ripristino automatico quando viene rilevato un errore. Microsoft 365 i sistemi di analisi delle deviazioni nel comportamento del servizio e avviano processi di auto-riparazione incorporati nel sistema. Microsoft 365 utilizza anche il monitoraggio esterno in cui il monitoraggio viene eseguito da più posizioni sia da servizi di terze parti attendibili (per la verifica indipendente del contratto di servizio) che dai nostri datacenter per generare avvisi. Per la diagnostica, sono stati evasi la registrazione, il controllo e l'analisi. La traccia granulare e il monitoraggio ci aiutano a isolare i problemi ed eseguire un'analisi rapida ed efficace delle cause radice.

Anche se Microsoft 365 ha azioni di ripristino automatizzate, ove possibile, i tecnici microsoft sono disponibili 24x7 per analizzare tutte le escalation di sicurezza di gravità 1 e le revisioni post-mortem di ogni incidente di servizio contribuiscono all'apprendimento continuo e al miglioramento. Questo team include tecnici del supporto, sviluppatori di prodotti, program manager, product manager e dirigenti senior. I nostri professionisti di chiamata forniscono un backup rapido e spesso possono automatizzare le azioni di ripristino, in modo che la prossima volta che si verifica un evento, possa essere auto-curato.

Microsoft esegue un'analisi approfondita post-incidente ogni volta che si verifica un Microsoft 365 di sicurezza indipendentemente dalla grandezza dell'impatto. Una revisione post-incidente consiste in un'analisi di ciò che è successo, di come abbiamo risposto e di come preveniamo incidenti simili in futuro. Nell'interesse della trasparenza e della responsabilità, condividiamo le revisioni post-incidente per eventuali incidenti di servizio principali con i clienti interessati. Per informazioni dettagliate, vedere [Gestione degli incidenti di sicurezza Microsoft.](assurance-security-incident-management.md)

## <a name="assume-breach-methodology"></a>Presupporre la metodologia di violazione

Sulla base di un'analisi dettagliata delle tendenze della sicurezza, Microsoft sostiene ed evidenzia la necessità di altri investimenti in processi e tecnologie di sicurezza reattivi incentrati sul rilevamento e sulla risposta alle minacce emergenti, anziché solo sulla prevenzione di tali minacce. A causa dei cambiamenti nel panorama delle minacce e dell'analisi approfondita, Microsoft ha perfezionato la propria strategia di sicurezza oltre a impedire le violazioni della sicurezza a uno più dotato per gestire le violazioni quando si verificano; una strategia che considera gli eventi di sicurezza principali non come una questione di se, ma quando.

Sebbene le procedure [di](https://www.microsoft.com/TrustCenter/Security/default.aspx) violazione di Microsoft siano in atto da molti anni, molti clienti non sono a conoscenza del lavoro svolto dietro le quinte per mettere in sicurezza il cloud Microsoft. Presupporre che la violazione sia una mentalità che guida gli investimenti nella sicurezza, le decisioni di progettazione e le procedure operative di sicurezza. Presupporre che la violazione limiti il trust posto in applicazioni, servizi, identità e reti trattandoli tutti, interni ed esterni, come insicuri e già compromessi. Sebbene la strategia di violazione non sia stata derivata da una violazione effettiva di servizi cloud o aziendali Microsoft, è stato riconosciuto che molte organizzazioni, in tutto il settore, sono state violate nonostante tutti i tentativi di impedirla. Sebbene la prevenzione delle violazioni sia una parte critica delle operazioni di qualsiasi organizzazione, tali procedure devono essere continuamente testate e aumentate per affrontare efficacemente gli avversari moderni e le minacce persistenti avanzate. Per fare in modo che qualsiasi organizzazione si prepari a una violazione, deve innanzitutto creare e mantenere procedure di risposta di sicurezza affidabili, ripetibili e testate in modo approfondito.

Sebbene i processi di sicurezza di prevenzione delle violazioni, ad esempio la modellazione delle minacce, le revisioni del codice e i test di sicurezza siano molto utili nell'ambito del ciclo di vita dello sviluppo della [sicurezza,](https://www.microsoft.com/securityengineering/sdl/)presuppongono che la violazione offra numerosi vantaggi che consentono di valutare la sicurezza complessiva esercitando e misurando le funzionalità reattive in caso di violazione.

Microsoft si è posta l'obiettivo di ottenere questo risultato attraverso esercitazioni di giochi di guerra in corso e test di penetrazione del sito in tempo reale dei piani di risposta alla sicurezza con l'obiettivo di migliorare le funzionalità di rilevamento e risposta. Microsoft simula regolarmente violazioni reali, esegue il monitoraggio continuo della sicurezza e pratica la gestione degli incidenti di sicurezza per convalidare e migliorare la sicurezza di Microsoft 365, Azure e altri servizi cloud Microsoft.

Microsoft esegue la strategia di sicurezza presuppongono che la violazione utilizzi due gruppi principali:

- Rosso Teams (utenti malintenzionati)
- Blu Teams (difensori)

Sia Microsoft Azure che Microsoft 365 il personale separano il Teams e il Teams a tempo Teams.

Definito "[Red Teaming](https://go.microsoft.com/fwlink/?linkid=518599)", l'approccio consiste nel testare i sistemi e le operazioni di Azure e Microsoft 365 utilizzando le stesse tattiche, tecniche e procedure degli avversari reali, rispetto all'infrastruttura di produzione in tempo reale, senza il foreknowledge dei team di progettazione o operazioni. Questo test consente di testare le funzionalità di risposta e rilevamento della sicurezza di Microsoft e consente di identificare le vulnerabilità di produzione, gli errori di configurazione, i presupposti non validi e altri problemi di sicurezza in modo controllato. Ogni violazione del Team Rosso è seguita dalla divulgazione completa tra entrambi i team per identificare le lacune, risolvere i risultati e migliorare la risposta alle violazioni.

**NOTA:** durante il red teaming o i test di penetrazione del sito in tempo reale, non viene intenzionalmente preso di mira alcun dato del cliente. I test sono a Microsoft 365 e alle piattaforme di Azure, nonché ai tenant, alle applicazioni e ai dati di Microsoft. I tenant dei clienti, le applicazioni e il contenuto ospitato in Microsoft 365 o Azure non sono mai destinati.

## <a name="red-teams"></a>Rosso Teams

Il Team Rosso è un gruppo di personale a tempo pieno all'interno di Microsoft che si concentra sulla violazione dell'infrastruttura, della piattaforma e delle applicazioni di Microsoft. Si tratta dell'avversario dedicato (un gruppo di hacker etici) che esegue attacchi mirati e persistenti contro i Servizi online (infrastruttura, piattaforme e applicazioni Microsoft ma non le applicazioni o il contenuto dei clienti finali).

Il ruolo del team rosso è quello di attaccare e penetrare in ambienti usando gli stessi passaggi di un avversario:

![Fasi di violazione.](../media/office-365-isolation-breach-stages.png)

Tra le altre funzioni, i team rossi tentano in modo specifico di violare i limiti di isolamento del tenant per individuare bug o lacune nella progettazione dell'isolamento.

Per facilitare la scalabilità degli sforzi di simulazione degli attacchi, il team rosso ha creato uno strumento di emulazione degli attacchi automatizzato che viene eseguito in modo sicuro in ambienti di Microsoft 365 specifici su base ricorrente. Lo strumento ha un'ampia gamma di attacchi predefiniti costantemente espansi e migliorati per riflettere l'evoluzione del panorama delle minacce. Oltre ad ampliare la copertura dei test red team, consente al team blu di convalidare e migliorare la logica di monitoraggio della sicurezza. L'emulazione di attacchi regolare e continua fornisce al team blu un flusso coerente e diversificato di segnali che vengono confrontati e convalidati rispetto alle risposte previste. Ciò consente di migliorare la logica di Microsoft 365 di sicurezza e le funzionalità di risposta.

## <a name="blue-teams"></a>Blu Teams

Il team blu è composto da un set dedicato di risponditori di sicurezza o membri di tutte le organizzazioni di risposta agli incidenti di sicurezza, progettazione e operazioni. Indipendentemente dal loro make-up, sono indipendenti e operano separatamente dal Team Rosso. Il team blu segue i processi di sicurezza stabiliti e usa gli strumenti e le tecnologie più recenti per rilevare e rispondere agli attacchi e alla penetrazione. Proprio come gli attacchi reali, il team blu non sa quando o come si verificheranno gli attacchi del Team Rosso o quali metodi possono essere utilizzati. Il loro compito, che si tratta di un attacco del Team Rosso o di un attacco vero e proprio, è quello di rilevare e rispondere a tutti gli incidenti di sicurezza. Per questo motivo, il team blu è costantemente in servizio e deve reagire alle violazioni del Team Rosso nello stesso modo in cui verrebbero violate per qualsiasi altra violazione.

Quando un avversario, ad esempio un team rosso, ha violato un ambiente, il team blu deve:

- Raccogliere le prove lasciati dall'avversario
- Rilevare le prove come indicazione di compromissione
- Avvisare i team di progettazione e funzionamento appropriati
- Valuta gli avvisi per determinare se giustificano ulteriori indagini
- Raccogliere il contesto dall'ambiente per l'ambito della violazione
- Formare un piano di correzione per contenere o eliminare l'avversario
- Eseguire il piano di correzione e ripristinare la violazione

Questi passaggi formano la risposta agli incidenti di sicurezza che viene eseguita in parallelo a quella dell'avversario, come illustrato di seguito:

![Fasi di risposta alla violazione.](../media/office-365-isolation-breach-response-stages.png)

Le violazioni del team rosso consentono di esercitare la capacità del team blu di rilevare e rispondere agli attacchi del mondo reale end-to-end. Soprattutto, consente una risposta pratica agli incidenti di sicurezza prima di una violazione autentica. Inoltre, a causa delle violazioni del Red Team, il team blu migliora la propria consapevolezza della situazione, che può essere utile quando si tratta di violazioni future (dal Team Rosso o da un altro avversario). Durante tutto il processo di rilevamento e risposta, il team blu produce un'intelligenza utilizzabile e ottiene visibilità nelle condizioni effettive degli ambienti che stanno cercando di difendere. Spesso questa operazione viene eseguita tramite analisi dei dati e analisi forensi, eseguite dal team blu, quando si risponde agli attacchi del Team Rosso e stabilendo indicatori di minaccia, ad esempio indicatori di compromissione. Analogamente al modo in cui il team rosso identifica le lacune nella storia della sicurezza, i team blu identificano le lacune nella loro capacità di rilevare e rispondere. Inoltre, dal momento che i team rossi modellano gli attacchi reali, il team blu può essere valutato in modo accurato in base alla loro capacità o incapacità di gestire gli avversari determinati e persistenti. Infine, le violazioni del team rosso misurano sia la prontezza che l'impatto della nostra risposta di violazione.
