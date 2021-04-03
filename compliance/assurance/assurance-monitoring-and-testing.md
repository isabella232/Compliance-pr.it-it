---
title: Simulazione di un attacco in Microsoft 365
description: In questo articolo scopri come Microsoft monitora e testa continuamente i limiti del tenant per Microsoft 365.
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
ms.openlocfilehash: b37ca23fa403bd0a4a657be78654a02bf23721b3
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497528"
---
# <a name="attack-simulation-in-microsoft-365"></a>Simulazione di un attacco in Microsoft 365

Microsoft monitora costantemente e verifica in modo esplicito i punti deboli e le vulnerabilità nei limiti del tenant, tra cui il monitoraggio delle intrusioni, i tentativi di violazione delle autorizzazioni e la carestia delle risorse. Usiamo anche più sistemi interni per monitorare continuamente l'utilizzo improprio delle risorse, che, se rilevato, attiva la limitazione incorporata.

Microsoft 365 dispone di sistemi di monitoraggio interni che monitorano continuamente eventuali errori e guidano il ripristino automatico quando viene rilevato un errore. I sistemi Microsoft 365 analizzano le deviazioni nel comportamento dei servizi e avviano processi di auto-riparazione incorporati nel sistema. Microsoft 365 usa anche il monitoraggio esterno in cui il monitoraggio viene eseguito da più posizioni sia da servizi di terze parti attendibili (per la verifica indipendente del contratto di servizio) che dai nostri datacenter per generare avvisi. Per la diagnostica, sono stati evasi la registrazione, il controllo e l'analisi. La traccia granulare e il monitoraggio ci aiutano a isolare i problemi ed eseguire un'analisi rapida ed efficace delle cause radice.

Anche se Microsoft 365 ha azioni di ripristino automatizzato, ove possibile, i tecnici di chiamata Microsoft sono disponibili 24x7 per analizzare tutte le escalation di sicurezza di gravità 1 e le revisioni post-mortem di ogni incidente di servizio contribuiscono all'apprendimento continuo e al miglioramento. Questo team include tecnici del supporto, sviluppatori di prodotti, program manager, product manager e dirigenti senior. I nostri professionisti di chiamata forniscono un backup rapido e spesso possono automatizzare le azioni di ripristino, in modo che la prossima volta che si verifica un evento, possa essere auto-curato.

Microsoft esegue un'analisi approfondita post-incidente ogni volta che si verifica un incidente di sicurezza di Microsoft 365 indipendentemente dalla grandezza dell'impatto. Una revisione post-incidente consiste in un'analisi di ciò che è successo, di come abbiamo risposto e di come preveniamo incidenti simili in futuro. Nell'interesse della trasparenza e della responsabilità, condividiamo la revisione post-incidente per eventuali incidenti di servizio principali con i clienti interessati. Per informazioni dettagliate, vedere [Office 365 Security Incident Management.](https://aka.ms/Office365SIM)

## <a name="assume-breach-methodology"></a>Presupporre la metodologia di violazione

Sulla base di un'analisi dettagliata delle tendenze della sicurezza, Microsoft sostiene ed evidenzia la necessità di altri investimenti in processi e tecnologie di sicurezza reattivi incentrati sul rilevamento e sulla risposta alle minacce emergenti, anziché solo sulla prevenzione di tali minacce. A causa dei cambiamenti nel panorama delle minacce e dell'analisi approfondita, Microsoft ha perfezionato la propria strategia di sicurezza oltre a impedire le violazioni della sicurezza a uno più dotato per gestire le violazioni quando si verificano; una strategia che considera gli eventi di sicurezza principali non come una questione di se, ma quando.

Anche se le procedure [di](https://www.microsoft.com/TrustCenter/Security/default.aspx) Microsoft presuppongono che le violazioni siano in atto da molti anni, molti clienti non sono a conoscenza del lavoro svolto dietro le quinte per mettere in sicurezza il cloud Microsoft. Presupporre che breach sia una mentalità che guida gli investimenti nella sicurezza, le decisioni di progettazione e le procedure operative di sicurezza. Presupporre che la violazione limiti il trust posto in applicazioni, servizi, identità e reti trattandoli tutti, interni ed esterni, come insicuri e già compromessi. Sebbene la strategia Presupponga violazione non sia stata derivata da una violazione effettiva di servizi cloud o aziendali Microsoft, è stato riconosciuto che molte organizzazioni, in tutto il settore, sono state violate nonostante tutti i tentativi di impedirla. Sebbene la prevenzione delle violazioni sia una parte critica delle operazioni di qualsiasi organizzazione, tali procedure devono essere continuamente testate e aumentate per affrontare efficacemente gli avversari moderni e le minacce persistenti avanzate. Per fare in modo che qualsiasi organizzazione si prepari a una violazione, deve innanzitutto creare e mantenere procedure di risposta di sicurezza affidabili, ripetibili e accuratamente testate.

Sebbene i processi di sicurezza Prevent Breach, ad esempio la modellazione delle minacce, le revisioni del codice e i test di sicurezza siano molto utili nell'ambito del ciclo di vita dello sviluppo della [sicurezza,](https://www.microsoft.com/securityengineering/sdl/)Assume Breach offre numerosi vantaggi che consentono di valutare la sicurezza complessiva esercitando e misurando le funzionalità reattive in caso di violazione.

Microsoft si è posta l'obiettivo di ottenere questo risultato attraverso esercitazioni di giochi di guerra in corso e test di penetrazione del sito in tempo reale dei piani di risposta alla sicurezza con l'obiettivo di migliorare le funzionalità di rilevamento e risposta. Microsoft simula regolarmente violazioni reali, esegue un monitoraggio continuo della sicurezza e pratica la gestione degli incidenti di sicurezza per convalidare e migliorare la sicurezza di Microsoft 365, Azure e altri servizi cloud Microsoft.

Microsoft esegue la strategia di sicurezza Assume Breach usando due gruppi principali:

- Red Teams (utenti malintenzionati)
- Blue Teams (difensori)

Sia microsoft Azure che il personale di Microsoft 365 separano i team rossi a tempo pieno e i team blu.

Definito "[Red Teaming](https://go.microsoft.com/fwlink/?linkid=518599)", l'approccio consiste nel testare i sistemi e le operazioni di Azure e Microsoft 365 utilizzando le stesse tattiche, tecniche e procedure degli avversari reali, rispetto all'infrastruttura di produzione in tempo reale, senza il supporto dei team di progettazione o delle operazioni. Questo test consente di testare le funzionalità di risposta e rilevamento della sicurezza di Microsoft e consente di identificare le vulnerabilità di produzione, gli errori di configurazione, i presupposti non validi e altri problemi di sicurezza in modo controllato. Ogni violazione del team rosso è seguita dalla divulgazione completa tra entrambi i team per identificare le lacune, risolvere i risultati e migliorare la risposta alle violazioni.

**NOTA:** durante il red teaming o i test di penetrazione del sito in tempo reale, non viene intenzionalmente preso di mira alcun dato del cliente. I test sono in base all'infrastruttura e alle piattaforme di Microsoft 365 e Azure, nonché ai tenant, alle applicazioni e ai dati di Microsoft. I tenant dei clienti, le applicazioni e il contenuto ospitato in Microsoft 365 o Azure non sono mai destinati.

## <a name="red-teams"></a>Team rossi

Il team rosso è un gruppo di personale a tempo pieno all'interno di Microsoft che si concentra sulla violazione dell'infrastruttura, della piattaforma e delle applicazioni di Microsoft. Si tratta dell'avversario dedicato (un gruppo di hacker etici) che esegue attacchi mirati e persistenti contro i Servizi online (infrastruttura, piattaforme e applicazioni Microsoft ma non le applicazioni o il contenuto dei clienti finali).

Il ruolo del team rosso è quello di attaccare e penetrare in ambienti usando gli stessi passaggi di un avversario:

![Fasi di violazione](../media/office-365-isolation-breach-stages.png)

Tra le altre funzioni, i team rossi tentano in modo specifico di violare i limiti di isolamento del tenant per individuare bug o lacune nella progettazione dell'isolamento.

## <a name="blue-teams"></a>Team blu

Il team blu è composto da un set dedicato di risponditori di sicurezza o membri di tutte le organizzazioni di risposta agli incidenti di sicurezza, progettazione e operazioni. Indipendentemente dal loro make-up, sono indipendenti e operano separatamente dal team rosso. Il team blu segue i processi di sicurezza stabiliti e usa gli strumenti e le tecnologie più recenti per rilevare e rispondere agli attacchi e alla penetrazione. Proprio come gli attacchi reali, il team blu non sa quando o come si verificheranno gli attacchi della squadra rossa o quali metodi possono essere utilizzati. Il loro compito, che si tratta di un attacco di squadra rosso o di un attacco effettivo, è quello di rilevare e rispondere a tutti gli incidenti di sicurezza. Per questo motivo, il team blu è costantemente in servizio e deve reagire alle violazioni del team rosso come farebbe per qualsiasi altra violazione.

Quando un avversario, ad esempio una squadra rossa, ha violato un ambiente, il team blu deve:

- Raccogliere le prove lasciati dall'avversario
- Rilevare le prove come indicazione di compromissione
- Avvisare i team di progettazione e funzionamento appropriati
- Valuta gli avvisi per determinare se giustificano ulteriori indagini
- Raccogliere il contesto dall'ambiente per l'ambito della violazione
- Formare un piano di correzione per contenere o eliminare l'avversario
- Eseguire il piano di correzione e ripristinare la violazione

Questi passaggi formano la risposta agli incidenti di sicurezza che viene eseguita in parallelo a quella dell'avversario, come illustrato di seguito:

![Fasi di risposta alle violazioni](../media/office-365-isolation-breach-response-stages.png)

Le violazioni del team rosso consentono di esercitare la capacità del team blu di rilevare e rispondere agli attacchi del mondo reale end-to-end. Soprattutto, consente una risposta pratica agli incidenti di sicurezza prima di una violazione autentica. Inoltre, a causa delle violazioni del team rosso, il team blu migliora la propria consapevolezza della situazione, che può essere utile quando si tratta di violazioni future (dal team rosso o da un altro avversario). Durante tutto il processo di rilevamento e risposta, il team blu produce un'intelligenza utilizzabile e ottiene visibilità nelle condizioni effettive degli ambienti che stanno cercando di difendere. Spesso questa operazione viene eseguita tramite analisi dei dati e analisi forensi, eseguite dal team blu, quando si risponde agli attacchi del team rosso e stabilendo indicatori di minaccia, ad esempio indicatori di compromissione. Analogamente al modo in cui il team rosso identifica le lacune nella storia della sicurezza, i team blu identificano le lacune nella loro capacità di rilevare e rispondere. Inoltre, dal momento che i team rossi modellano gli attacchi reali, il team blu può essere valutato in modo accurato in base alla loro capacità o incapacità di gestire gli avversari determinati e persistenti. Infine, le violazioni del team rosso misurano sia la prontezza che l'impatto della nostra risposta di violazione.
