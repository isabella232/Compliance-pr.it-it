---
title: Creare un framework di classificazione dei dati ben progettato
description: In questo articolo è possibile trovare una panoramica di come creare un framework di classificazione dei dati ben progettato per Microsoft 365.
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
ms.openlocfilehash: 88a07e5c6d5e3e84260c5099d957ebf38745819e239f951df62a5d04886f3fa4
ms.sourcegitcommit: af1925730de60c3b698edc4e1355c38972bdd759
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/05/2021
ms.locfileid: "54288724"
---
# <a name="create-a-well-designed-data-classification-framework"></a>Creare un framework di classificazione dei dati ben progettato

Durante lo sviluppo, il revamp o il perfezionamento del framework di classificazione dei dati, prendere in considerazione le procedure principali seguenti:

- Non aspettarti di passare da 0 a **100** il giorno 1 : Microsoft consiglia un approccio crawl-walk-run, assegnando priorità alle funzionalità critiche per l'organizzazione e mappandole in base a una sequenza temporale. Completare il primo passaggio, verificare che abbia avuto esito positivo e quindi passare alla fase successiva applicando le lezioni apprese. Tenere presente che l'organizzazione potrebbe essere ancora esposta a rischi durante la progettazione del framework di classificazione dei dati, quindi è possibile iniziare con pochi livelli di classificazione ed espandersi in un secondo momento in base alle esigenze.
- **Non si sta scrivendo solo** per i professionisti della sicurezza informatica: i framework di classificazione dei dati sono destinati a un pubblico ampio, tra cui il membro medio del personale, i team legali e di conformità e il team IT. È importante scrivere definizioni chiare e di facile comprensione per i livelli di classificazione dei dati, fornendo esempi reali dove possibile. Cerca di evitare il gergo e considera un glossario per acronimi e termini altamente tecnici. Ad esempio, usa "Informazioni personali" e fornisci una definizione invece di dire semplicemente "PII".
- **I framework di classificazione dei dati devono essere implementati:** per la corretta esecuzione dei framework di classificazione dei dati, è necessario che siano implementati. È particolarmente rilevante per la creazione dei requisiti di controllo per ogni livello di classificazione dei dati. Assicurati che i requisiti siano definiti in modo chiaro e che prevedono e soddegnino qualsiasi ambiguità che potrebbe verificarsi durante l'implementazione. Ad esempio, se si dispone di un controllo sulle informazioni personali, assicurarsi di precisare esattamente il significato del controllo, ad esempio previdenza sociale o numero di passaporto.
- **Passare alla granularità solo se è necessario:** i framework di classificazione dei dati in genere contengono da 3 a 5 livelli di classificazione dei dati. Tuttavia, solo perché *puoi* includere cinque livelli non significa *che* dovresti . Quando si decide il numero di livelli di classificazione necessari, considerare i criteri seguenti:

    - Il settore e gli obblighi normativi associati (i settori altamente regolamentati tendono ad avere bisogno di più livelli di classificazione)
    - Il sovraccarico operativo necessario per mantenere un framework più complesso
    - Gli utenti e la loro capacità di conformarsi alla maggiore complessità e sfumatura associata a più livelli di classificazione
    - Esperienza utente e accessibilità quando si cerca di applicare la classificazione manuale tra più tipi di dispositivi

- **Coinvolgere le persone giuste:** avere una parte interessata senior è fondamentale per il successo, poiché molti progetti faticano a iniziare o a richiedere più tempo senza il supporto dei dirigenti. I framework di classificazione dei dati sono in genere di proprietà dei team di information technology, ma possono avere implicazioni legali, di conformità, di privacy e di gestione delle modifiche. Per garantire la creazione di un framework che aiuti a proteggere l'azienda, assicurati di includere gli stakeholder legali e della privacy, ad esempio il Chief Privacy Officer e il Office of General Counsel nello sviluppo della tua politica. Se l'organizzazione dispone di una divisione conformità, professionisti della governance delle informazioni o di un team di gestione dei record, potrebbe anche avere un valido input. Durante l'implementazione del framework per l'azienda, il reparto Comunicazioni ha anche un ruolo chiave da svolgere per la messaggistica interna e l'adozione.
- **Bilanciare la sicurezza con la** comodità : un errore comune è quello di bozza di un framework di classificazione dei dati sicuro ma eccessivamente restrittivo. Questo framework potrebbe essere stato progettato in base alla sicurezza, ma spesso è difficile da implementare nella pratica. Se gli utenti devono seguire procedure complesse, rigide e dispendiose in termini di tempo per applicare il framework nella loro vita quotidiana, esiste sempre il rischio che non creda più al suo valore e che alla fine smettano di seguire le procedure. Questo rischio esiste a tutti i livelli dell'organizzazione, inclusi i manager a livello esecutivo (C-suite) all'interno dell'organizzazione. Un buon equilibrio tra sicurezza e comodità insieme a strumenti facili da usare in genere porta a un'adozione e un uso più ampi degli utenti. In caso di lacune nel framework, non attendere che tutto sia perfetto per avviare l'implementazione. Valuta invece il rischio o il gap, crea un piano per mitigare e continua ad andare avanti. Tenere presente che la protezione delle informazioni è un viaggio, non è qualcosa che viene attivato durante la notte e quindi fatto. Pianificare, implementare alcune funzionalità, confermare l'esito positivo e eseguire un'iterazione alla fase cardine successiva man appena gli strumenti si evolvono e gli utenti ottengono maturità ed esperienza.

Tenere inoltre presente che un framework  di classificazione dei dati si rivolge solo alle esigenze dell'organizzazione per proteggere i dati sensibili. I framework di classificazione dei dati sono spesso accompagnati da regole o linee guida per la gestione dei dati che definiscono come mettere in atto questi criteri dal punto di vista tecnico e tecnologico.  Nelle sezioni seguenti vengono fornite alcune indicazioni pratiche su come trasformare il framework di classificazione dei dati da un documento di criteri a un'iniziativa completamente implementata e praticabile.

## <a name="pain-points-in-creating-a-data-classification-framework"></a>Punti di riferimento per la creazione di un framework di classificazione dei dati

Gli sforzi di classificazione dei dati sono per natura di vasta portata, toccando quasi tutte le funzioni aziendali all'interno di un'azienda. A causa di questo ampio ambito e della complessità della gestione dei contenuti negli ambienti digitali moderni, le aziende devono spesso affrontare difficoltà nel sapere da dove iniziare, come gestire un'implementazione corretta e come misurarne lo stato di avanzamento. I punti di dolore più comuni spesso includono:

- Progettazione di un framework di classificazione dei dati affidabile e facile da comprendere, inclusa la determinazione dei livelli di classificazione e dei controlli di sicurezza associati.
- Sviluppo di un piano di implementazione che includa la conferma della soluzione tecnologica appropriata, l'allineamento del piano ai processi aziendali esistenti e l'identificazione dell'impatto sulla forza lavoro.
- Configurare un framework di classificazione dei dati all'interno della soluzione tecnologica scelta e risolvere eventuali lacune tra le funzionalità tecnologiche dello strumento e il framework stesso.
- Definizione di una struttura di governance che sovrintende alla manutenzione in corso e all'integrità degli sforzi di classificazione dei dati.
- Identificazione di indicatori di prestazioni chiave specifici (KPI) per monitorare e misurare lo stato di avanzamento.
- Aumentare la consapevolezza e la comprensione dei criteri di classificazione dei dati, perché sono importanti e come rispettarli.
- Conformità alle revisioni di controllo interne mirate alla perdita di dati e ai controlli di cybersecurity.
- Formazione e coinvolgimento degli utenti in modo che diventino coscienti della necessità di una classificazione corretta nel lavoro quotidiano e di applicare le misure di classificazione corrette.

## <a name="change-management-and-training"></a>Gestione delle modifiche e formazione

Le organizzazioni usano oggi strumenti come Microsoft 365 per implementare il framework di classificazione dei dati. Lo scopo è quello di automatizzare la classificazione dei dati e non aumentare il carico di lavoro. Questa struttura non significa che l'organizzazione non abbia alcuna responsabilità di aumentare la consapevolezza della necessità di gestire il contenuto e proteggere l'organizzazione dai rischi descritti in questo documento. La pratica principale continua a essere condurre una formazione di sensibilizzazione all'interno dell'organizzazione nell'ambito della pianificazione annuale della formazione. La nostra esperienza dimostra che l'impegno solido e completo per formare gli utenti, che sono i principali destinatari che eseguono questo lavoro, aumenta il loro "buy-in" per lo sforzo e può aumentare l'adozione e la qualità. [L'aggiunta di suggerimenti](/microsoft-365/compliance/apply-sensitivity-label-automatically#recommend-that-the-user-apply-a-sensitivity-label) per etichette e suggerimenti in-app può amplificare questi sforzi. Questa formazione non deve essere un corso completo autonomo. L'organizzazione può incorporarlo in altri corsi di formazione regolari, ad esempio la formazione annuale sulla sicurezza delle informazioni e quindi includere una panoramica dei livelli e delle definizioni di classificazione dei dati. Il punto principale è che la forza lavoro ha la comprensione che, anche se lo strumento automatizza la classificazione dei dati, ciò non elimina la responsabilità generale di ogni utente di proteggere i dati in conformità ai criteri aziendali.

È inoltre consigliabile prendere in considerazione una formazione più approfondita per i team IT e di sicurezza delle informazioni per rafforzare la preparazione operativa. I team che gestiscono lo strumento e il framework di classificazione dei dati devono essere nella stessa pagina. Questo coordinamento può richiedere di investire in una pianificazione della formazione più affidabile che può essere più spesso di ogni anno. L'investimento in corsi di formazione più frequenti rappresenta un'altra strada per ridurre i rischi per l'organizzazione. Questo team è responsabile dell'implementazione e pertanto potrebbe essere un punto di errore se non è stato addestrato sullo strumento e sui criteri.

Se devi aggiungere manualmente tag al contenuto nello strumento, è appropriato sviluppare un gruppo di utenti con privilegi avanzati che hanno ricevuto una formazione più avanzata. Questi utenti con privilegi super sarebbero coinvolti in situazioni in cui gli utenti sono tenuti a contrassegnare manualmente i documenti con etichette di riservatezza dei dati e avrebbero una conoscenza approfondita del framework di classificazione dei dati e dei requisiti normativi dell'organizzazione.

Infine, i dirigenti devono dare priorità alla protezione dei comportamenti di sicurezza delle informazioni per rafforzare alla forza lavoro l'importanza delle iniziative di gestione dei rischi. Questi includono lo sviluppo e l'implementazione di un solido framework di classificazione dei dati e l'assegnazione di leader chiave per promuovere l'iniziativa, a volte indicati come ambasciatori o promotori del cambiamento.

## <a name="governance-and-maintenance"></a>Governance e manutenzione

Dopo aver sviluppato e implementato il framework di classificazione dei dati, la governance e la manutenzione continue saranno fondamentali per il successo. Oltre a tenere traccia del modo in cui le etichette di riservatezza vengono utilizzate nella pratica, è necessario aggiornare i requisiti di controllo in base alle modifiche apportate alle normative, alle procedure di guida per la sicurezza informatica e alla natura del contenuto che gestisci. Gli sforzi di governance e manutenzione possono includere:

- Creazione di un ente di governance dedicato alla classificazione dei dati o all'aggiunta di una responsabilità di classificazione dei dati alla carta di un ente di sicurezza delle informazioni esistente.
- Definizione di ruoli e responsabilità per gli utenti che supervisionano la classificazione dei dati.
- Definizione di indicatori KPI per monitorare e misurare lo stato di avanzamento.
- Monitoraggio delle procedure guida per la sicurezza informatica e dei cambiamenti normativi.
- Sviluppo di procedure operative standard che supportano e applicano un framework di classificazione dei dati.

## <a name="industry-considerations"></a>Considerazioni sul settore

Sebbene i principi di base per lo sviluppo di un framework di classificazione dei dati solido siano universali, i dettagli del framework dipendono dalla natura del settore e dai fattori di conformità e sicurezza specifici che i dati richiede.

Ad esempio, le società di servizi finanziari potrebbero dover prendere in considerazione la conformità a diversi quadri normativi a seconda dell'ambito dell'attività e delle aree geografiche in cui operano. Le società di titoli negli Stati Uniti devono conformarsi a normative contabili come la regola [SEC 17a-4(f)](/compliance/regulatory/offering-sec-17a-4) o la regola [FINRA 4511](/microsoft-365/compliance/offering-finra-4511) che affrontano i requisiti relativi alla sicurezza e alla conservazione di libri e record. Analogamente, le aziende che operano nel Regno Unito devono considerare la [conformità FCA.](/microsoft-365/compliance/offering-fca-uk)

Le agenzie governative devono affrontare diverse normative che regolano i propri dati, che variano in base al territorio e alla natura del loro lavoro. Negli Stati Uniti, ad esempio, le agenzie governative e i loro agenti che accedono alle informazioni fiscali federali (FTI) sono soggetti [all'IRS 1075,](/microsoft-365/compliance/offering-irs-1075)che mira a ridurre al minimo il rischio di perdita, violazione o uso improprio delle informazioni fiscali federali.

Mentre le società di servizi finanziari e le agenzie governative sono tra le organizzazioni più regolamentate al mondo, la maggior parte delle aziende ha considerazioni specifiche del settore che devono essere considerate. Ecco alcuni esempi:

- Organizzazioni del settore sanitario [che garantiscono la conformità con HIPAA](/microsoft-365/compliance/offering-hipaa-hitech).
- Istituti di istruzione, dalle scuole K-12 alle università, che gestiscono [la conformità FERPA.](/microsoft-365/compliance/offering-ferpa)
- I produttori di farmaci che lavorano per rispettare [le linee guida GxP](/microsoft-365/compliance/offering-gxp) nel proprio paese o area geografica in base alla sicurezza delle informazioni.
- Media, vendita al dettaglio e molte altre aziende che si occupano della [conformità al GDPR](/microsoft-365/compliance/gdpr).
- Distribuzione e archiviazione di contenuti di intrattenimento, software e informazioni che gestiscono [CDSA.](/microsoft-365/compliance/offering-cdsa)
- Sicurezza delle informazioni del settore energetico conforme agli [standard NERC CIP](/microsoft-365/compliance/offering-nerc-cip).

## <a name="implementing-your-data-classification-framework-in-microsoft-365"></a>Implementazione del framework di classificazione dei dati in Microsoft 365

Dopo aver sviluppato il framework di classificazione dei dati, il passaggio successivo è l'implementazione. Il [Centro conformità Microsoft 365](https://compliance.microsoft.com/) consente agli amministratori di individuare, classificare, esaminare e monitorare i dati in base al framework di classificazione dei dati. Le etichette di riservatezza possono essere utilizzate per proteggere i dati mediante l'applicazione di diverse protezioni, ad esempio la crittografia e il contrassegno del contenuto. Possono essere applicati ai dati manualmente. per impostazione predefinita, in base alle impostazioni dei criteri; o automaticamente, come risultato di una condizione, ad esempio informazioni personali identificate.

Per organizzazioni di piccole dimensioni o organizzazioni con un framework di classificazione dei dati relativamente semplificato, potrebbe essere sufficiente creare una singola etichetta di riservatezza per ogni livello di classificazione dei dati. L'esempio seguente mostra un livello di classificazione dei dati uno-a-uno per il mapping delle etichette di riservatezza:

|**Etichetta di classificazione**|**Etichetta di riservatezza**|**Impostazioni etichetta**|**Pubblicato in**|
|:-----------------------|:--------------------|:-----------------|:---------------|
| Senza restrizioni | Senza restrizioni | Applicare il piè di pagina "Senza restrizioni" | Tutti gli utenti |
| Generale | Generale | Applica piè di pagina "Generale" | Tutti gli utenti |

>[!TIP]
>Durante un progetto pilota per la protezione delle informazioni interne di Microsoft, si sono verificate difficoltà con la comprensione e l'uso dell'etichetta "Personale". Gli utenti erano confusi sul fatto che si trattasse di informazioni personali o semplicemente correlate a una questione personale. L'etichetta è stata modificata in "non aziendale" per essere più chiara. Questo esempio mostra che la tassonomia non deve essere perfetta fin dall'inizio. Iniziare con ciò che ritieni giusto, pilotarlo e regolare l'etichetta in base al feedback, se necessario

Per organizzazioni di grandi dimensioni con una portata globale o esigenze di sicurezza delle informazioni più complesse, questa relazione uno-a-uno tra il numero di livelli di classificazione nei criteri e il numero di etichette di riservatezza nell'ambiente Microsoft 365 può essere una sfida. Questa sfida è particolarmente valida nelle organizzazioni globali in cui un determinato livello di classificazione dei dati, ad esempio "Con restrizioni", può avere una definizione diversa o un set di controlli diverso a seconda dell'area geografica.

Per ulteriori informazioni sull'implementazione, vedere [Informazioni sulla classificazione dei dati](/microsoft-365/compliance/data-classification-overview) e Informazioni sulle etichette di [riservatezza.](/microsoft-365/compliance/sensitivity-labels)

## <a name="references"></a>Riferimenti

- [Offerte per la conformità Microsoft](/microsoft-365/compliance/offering-home)
