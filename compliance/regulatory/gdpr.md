---
title: Regolamento generale sulla protezione dei dati
description: Informazioni sulla documentazione tecnica di Microsoft e altre informazioni utili per il Regolamento generale sulla protezione dei dati (GDPR)
keywords: Microsoft 365, Microsoft 365 Education, Documentazione Microsoft 365, GDPR
localization_priority: Priority
ms.prod: microsoft-365-enterprise
ms.topic: article
f1.keywords:
- NOCSH
ms.author: robmazz
author: robmazz
manager: laurawi
audience: itpro
ms.collection:
- GDPR
- M365-security-compliance
- MS-Compliance
titleSuffix: Microsoft GDPR
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: 2d4c319bd5c0d3d264ae67179dc4d55e0a0e4fe8
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/30/2020
ms.locfileid: "49508927"
---
# <a name="general-data-protection-regulation-summary"></a>Riepilogo del Regolamento generale sulla protezione dei dati

Il Regolamento generale sulla protezione dei dati (GDPR) introduce nuove regole per le organizzazioni che offrono beni e servizi alle persone che risiedono nell'Unione europea (UE) o che raccolgono e analizzano i dati dei residenti nell'UE in qualunque luogo si trovi l'utente o la sua azienda. Questo documento illustra le informazioni che consentono di rispettare i diritti e adempiere agli obblighi in conformità al GDPR quando si usano i prodotti e i servizi Microsoft. Un [piano d'azione consigliato per il GDPR](gdpr-action-plan.md) e gli [elenchi di controllo di preparazione della conformità](gdpr-arc.md) forniscono ulteriori risorse per la valutazione e l'implementazione della conformità al GDPR.

## <a name="terminology"></a>Terminologia

Definizioni utili per i termini relativi al GDPR usati nel documento:

- **Titolare del trattamento dei dati (titolare)**: una persona giuridica, un'autorità pubblica, un'agenzia o un altro organismo che, da solo o congiuntamente con altri, determina le finalità e le modalità di trattamento dei dati personali.  
- **Dati personali e interessato**: qualsiasi informazione relativa a una persona fisica identificata o identificabile (interessato); una persona fisica identificabile è una persona che può essere identificata, direttamente o indirettamente.  
- **Responsabile**: una persona fisica o giuridica, un'autorità pubblica o un altro ente che si occupa del trattamento dei dati personali per conto del titolare.  
- **Dati dei clienti**: dati prodotti e archiviati relativi alle attività quotidiane di gestione della propria attività.

## <a name="what-is-the-gdpr"></a>Che cos'è il GDPR?

Il GDPR attribuisce alle persone il diritto di gestire i dati personali raccolti da un'organizzazione. Tali diritti possono essere esercitati tramite una richiesta dell'interessato (DSR). L'organizzazione è tenuta a fornire informazioni tempestive relative alle richieste dell'interessato e alle violazioni dei dati e a eseguire valutazioni d'impatto sulla protezione dei dati (DPIA). 

Nell'implementazione o nella valutazione dei requisiti del GDPR, è opportuno tenere in considerazione diversi punti:

- Sviluppo e valutazione dell'informativa sulla privacy relativa ai dati in conformità al GDPR.
- Valutazione della sicurezza dei dati dell'organizzazione.
- Chi è il titolare del trattamento dei dati?
- Quali processi per la sicurezza dei dati potrebbe essere necessario eseguire?

Il [piano d'azione consigliato per il GDPR](gdpr-action-plan.md) e gli [elenchi di controllo di preparazione della conformità](gdpr-arc.md) potrebbero richiedere la considerazione di ulteriori fattori.

Sono previsti i seguenti passaggi per soddisfare gli standard del GDPR. Per i dettagli relativi all'implementazione, seguire i collegamenti nell'elenco.  

- **[Richieste dell’interessato (DSR)](gdpr-data-subject-requests.md)**. Una richiesta formale da parte di un interessato a un titolare del trattamento di effettuare un’operazione (modifica, limitazione, accesso) sui dati personali.
- **[Notifica di violazione](gdpr-breach-notification.md)**. Secondo il GDPR, una violazione dei dati personali è "una violazione di sicurezza che comporta accidentalmente o in modo illecito la distruzione, la perdita, la modifica, la divulgazione non autorizzata o l'accesso ai dati personali trasmessi, conservati o comunque trattati".
- **[Valutazione d'impatto sulla protezione dei dati (DPIA)](gdpr-data-protection-impact-assessments.md)**. Ai sensi del GDPR, i titolari del trattamento devono preparare una DPIA per le operazioni di trattamento che "presentano un rischio elevato per i diritti e le libertà delle persone fisiche".

Come già accennato, il piano d'azione consigliato per il GDPR e gli elenchi di controllo di preparazione della conformità forniscono una guida per l'implementazione o la valutazione della conformità al GDPR quando si usano i prodotti e i servizi Microsoft.

## <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a>Usare Microsoft Compliance Manager per valutare i rischi

[Microsoft Compliance Manager](https://docs.microsoft.com/microsoft-365/compliance/compliance-manager) è una funzionalità del [Centro conformità Microsoft 365](https://docs.microsoft.com/microsoft-365/compliance/microsoft-365-compliance-center) utile per comprendere lo stato di conformità dell'organizzazione e adottare misure per ridurre i rischi. Compliance Manager fornisce una valutazione predefinita per questa normativa per i clienti di Enterprise E5. È possibile trovare il modello per la creazione della valutazione nella pagina dei **modelli di valutazione** in Compliance Manager. Informazioni su come [creare le valutazioni in Compliance Manager](https://docs.microsoft.com/microsoft-365/compliance/compliance-manager-assessments).

## <a name="data-subject-request-dsr"></a>Richiesta dell'interessato (DSR)

Il GDPR attribuisce alle persone (o interessati) determinati diritti in connessione con il trattamento dei loro dati personali, tra cui il diritto di correggere i dati non esatti, di cancellare i dati o limitarne il trattamento, di ricevere i dati e completare una richiesta di trasmissione dei dati a un altro titolare del trattamento. Il titolare del trattamento deve fornire una risposta tempestiva in accordo con il GDPR. Per i dettagli tecnici, vedere [Richieste dell’interessato](gdpr-data-subject-requests.md).  

### <a name="dsr-faqs"></a>Domande frequenti sulle richieste degli interessati

**Quali azioni saranno necessarie per completare una richiesta dell'interessato?**

Le richieste degli interessati implicano sei attività, ovvero individuazione, accesso, rettifica, limitazione, esportazione ed eliminazione.

**Quali sono le origini dati?**

Una considerevole quantità dei dati dell'organizzazione viene generata da [applicazioni di Office](https://docs.microsoft.com/microsoft-365/compliance/gdpr-dsr-office365#using-the-content-search-ediscovery-tool-to-respond-to-dsrs) come Excel e Outlook. È possibile trovare dati rilevanti per una richiesta dell’interessato anche nelle [Informazioni dettagliate](https://docs.microsoft.com/microsoft-365/compliance/gdpr-dsr-office365#part-2-responding-to-dsrs-with-respect-to-insights-generated-by-office-365) generate da prodotti e servizi Microsoft e nei [log generati dal sistema](https://docs.microsoft.com/microsoft-365/compliance/gdpr-dsr-office365#part-3-responding-to-dsrs-for-system-generated-logs). 

**Quali tipi di dati è necessario cercare?**

I dati personali possono essere presenti nei dati dei clienti, nelle informazioni approfondite generate dai prodotti e dai servizi Microsoft e nei log generati dal sistema.

**In che modo è possibile cercare i dati personali?**

La ricerca dei dati personali può essere diversa in base ai prodotti e ai servizi Microsoft. Gli strumenti di ricerca includono [Ricerca contenuto](https://docs.microsoft.com/microsoft-365/compliance/gdpr-dsr-office365#using-the-content-search-ediscovery-tool-to-respond-to-dsrs) o la funzionalità di [ricerca in-app](https://docs.microsoft.com/microsoft-365/compliance/gdpr-dsr-office365#using-in-app-functionality-to-respond-to-dsrs). Gli amministratori possono accedere ai [log generati dal sistema](https://docs.microsoft.com/microsoft-365/compliance/gdpr-dsr-office365#part-3-responding-to-dsrs-for-system-generated-logs) associati all’attività di un utente.  

**In che formato dovrebbero essere resi disponibili i dati personali?**

Il "diritto alla portabilità dei dati" del GDPR consente all'interessato di richiedere una copia dei dati personali in un "formato strutturato, di uso comune e leggibile da dispositivo automatico" e di richiedere che l'organizzazione trasmetta questi file a un altro titolare del trattamento dei dati.

**Cosa richiede il GDPR e quali sono le responsabilità del titolare del trattamento?**

In base al GDPR, il titolare del trattamento è tenuto a fare quanto segue:

- Fornire agli interessati una copia dei loro dati personali, insieme a una spiegazione delle categorie di dati oggetto di trattamento, delle finalità di tale trattamento e delle categorie di terze parti a cui i dati possono essere comunicati.
- Consentire a ogni persona di esercitare il proprio diritto di correggere i dati personali non corretti, di cancellare i dati o di limitarne il trattamento, di ricevere i propri dati in un formato leggibile e, se applicabile, di accogliere una richiesta di trasmissione di tali dati a un altro titolare del trattamento.

**Cosa richiede il GDPR e quali sono le responsabilità di Microsoft in quanto responsabile del trattamento dei dati?**

Dobbiamo implementare misure tecniche e organizzative appropriate per consentire di rispondere alle richieste degli interessati che esercitano i loro diritti indicati in precedenza.

**Dove è possibile trovare informazioni relative al GDPR per i server locali?**

È possibile trovare di seguito una serie di articoli relativi al GDPR. Sono prodotti da Microsoft e illustrano gli approcci consigliati per il carico di lavoro locale per SharePoint Server, Exchange Server, Project Server, Office Web Apps Server, Office Online Server e le condivisioni di file locali.

**In che modo Microsoft consente di rispondere alle richieste degli interessati?**

Online Services offre una serie di funzionalità che consentono al titolare del trattamento di rispondere a una richiesta dell'interessato. I servizi online aziendali di Microsoft e i controlli amministrativi consentono di intervenire sui dati personali in risposta alle richieste di esercizio dei diritti degli interessati, permettendo di individuare, accedere, rettificare, limitare, eliminare ed esportare i dati personali inclusi nei dati gestiti dal titolare del trattamento archiviati nel cloud Microsoft. Inoltre, in caso di necessità, Online Services fornisce i dati in un formato leggibile da computer.

## <a name="data-protection-impact-assessment"></a>Valutazione d'impatto sulla protezione dei dati

Ai sensi del GDPR, i titolari del trattamento devono preparare una [valutazione d'impatto sulla protezione dei dati ](gdpr-data-protection-impact-assessments.md) (DPIA) per le operazioni di trattamento che "presentano un rischio elevato per i diritti e le libertà delle persone fisiche". Non c'è nulla nelle caratteristiche dei prodotti e servizi Microsoft che richieda per la loro natura la creazione di una DPIA. Al contrario, questa dipende dai dettagli della configurazione di Microsoft. Un elenco dei dettagli di Office che devono essere tenuti in considerazione è disponibile in [Contenuti della DPIA](https://docs.microsoft.com/microsoft-365/compliance/gdpr-dpia-office365#part-2--contents-of-a-dpia)

### <a name="dpia-faqs"></a>Domande frequenti sulla valutazione d'impatto sulla protezione dei dati

**Quando dovrebbe essere eseguita una DPIA?**

I titolari del trattamento devono eseguire una DPIA per rispondere ai rischi relativi alla sicurezza dei dati personali o in seguito a una violazione dei dati. Esempi specifici di fattori di rischio di Office sono trattati in [Determinare se è necessaria una DPIA](https://docs.microsoft.com/microsoft-365/compliance/gdpr-dpia-office365#part-1--determining-whether-a-dpia-is-needed).  

**Cosa è necessario per completare una DPIA?**

Secondo il GDPR, una DPIA deve includere quanto segue:

- Una valutazione della necessità e proporzionalità delle operazioni di trattamento dei dati in relazione agli scopi della DPIA.
- Una valutazione dei rischi per i diritti e le libertà dell'interessato.
- Misure previste per risolvere i rischi, garanzie, misure di sicurezza e meccanismi per garantire la protezione dei dati personali e dimostrare la conformità al GDPR.

**Quali sono le responsabilità del titolare del trattamento?**

In base al GDPR, il titolare del trattamento deve svolgere una valutazione d'impatto sulla protezione dei dati prima di eseguire trattamenti dei dati che possono presentare un rischio elevato per i diritti e le libertà delle persone (in particolare quelli che comportano l'utilizzo di nuove tecnologie). Il GDPR prevede un elenco non esaustivo, riportato di seguito, dei casi in cui deve essere eseguita una DPIA: 

- Trattamento automatizzato per finalità di profilatura e attività simili che producono effetti giuridici o che incidono in modo analogamente significativo nei confronti degli interessati;  
- Trattamento su larga scala di categorie particolari di dati personali (dati che rivelano origini etniche o razziali, opinioni politiche e simili) o di dati relativi a condanne penali o reati;  
- Sorveglianza sistematica su larga scala di una zona accessibile al pubblico.  

Il GDPR richiede inoltre di consultare l'autorità incaricata della protezione dei dati personali prima di iniziare qualsiasi trattamento se non è possibile identificare processi sufficienti per ridurre al minimo i rischi elevati per gli interessati.

**Quali sono le responsabilità di Microsoft?**

Microsoft aderisce ai principi di "privacy by design" (privacy fin dalla progettazione) e "privacy by default" (privacy per impostazione predefinita) nelle sue attività di business e progettazione. Nell’ambito di questo impegno, Microsoft esegue controlli completi della privacy sulle operazioni di trattamento dei dati che potrebbero avere un impatto sui diritti e sulle libertà degli interessati. I team che si occupano della privacy nei gruppi dei servizi controllano la progettazione e l'implementazione dei servizi per verificare che il trattamento dei dati personali avvenga nel rispetto delle leggi internazionali, delle aspettative degli utenti e dell'impegno espresso da Microsoft.

Tali controlli della privacy tendono ad essere granulari: un determinato servizio può essere sottoposto a decine o centinaia di controlli. Questi controlli granulari della privacy confluiscono nelle valutazioni d'impatto sulla protezione dei dati che riguardano le principali categorie di trattamento, che in seguito verranno sottoposte al controllo del Responsabile della protezione dei dati dell'Unione europea di Microsoft. Il Responsabile della protezione dei dati valuta i rischi relativi al trattamento dei dati per assicurare che siano implementate soluzioni sufficienti. Se individua dei rischi privi di soluzione, suggerisce le modifiche da apportare al gruppo di progettazione. Le DPIA vengono riviste e aggiornate in caso di modifica dei rischi per la protezione dei dati.


Microsoft, in qualità di responsabile del trattamento, ha l’obbligo di supportare i titolari del trattamento nel garantire la conformità ai requisiti della DPIA stabiliti dal GDPR. A questo scopo, le sezioni pertinenti delle valutazioni d'impatto sulla protezione dei dati svolte da Microsoft verranno fornite in questa sezione negli aggiornamenti futuri, per consentire ai titolari del trattamento che usano i servizi Microsoft di sfruttare queste informazioni per creare le proprie valutazioni d'impatto.

## <a name="breach-notification"></a>Notifica di violazione

Il GPDR impone ai titolari e ai responsabili del trattamento dei dati l'obbligo di notifica in caso di violazione dei dati personali. In qualità di responsabile del trattamento dei dati, Microsoft mette i clienti in condizione di soddisfare i requisiti di notifica delle violazioni previsti dal GDPR. I titolari del trattamento dei dati sono tenuti a valutare i rischi per la privacy di tali dati e a stabilire se una violazione richieda la notifica all'autorità per la protezione dei dati di un cliente. Microsoft fornisce le informazioni necessarie per eseguire tale valutazione. Per ulteriori informazioni su come Microsoft rileva e gestisce un caso di violazione dei dati personali, vedere [Notifica di violazione dei dati secondo il GDPR](gdpr-breach-notification.md).

### <a name="breach-notification-faqs"></a>Domande frequenti sulla notifica di violazione

**Cosa costituisce una violazione dei dati personali secondo il GDPR?**

Per dati personali si intendono tutte le informazioni relative a un individuo che possono essere utilizzate per identificare tale soggetto direttamente o indirettamente. Una violazione dei dati personali è "una violazione di sicurezza che comporta accidentalmente o in modo illecito la distruzione, la perdita, la modifica, la divulgazione non autorizzata o l'accesso ai dati personali trasmessi, conservati o comunque trattati".

**Quali sono le responsabilità del titolare del trattamento?**

Se si verifica una violazione dei dati personali che presenta un rischio elevato per i diritti e le libertà delle persone (come discriminazione, furto di identità, frodi, perdite finanziarie o danni alla reputazione), il GDPR richiede di:

- Informare l'autorità incaricata della protezione dei dati competente entro 72 ore dal momento in cui se ne viene a conoscenza, ad esempio dopo la ricezione della notifica da Microsoft. Se non si invia una notifica all'autorità per la protezione dei dati entro tale termine, sarà necessario fornirle una spiegazione. Questa notifica all'autorità incaricata della protezione dei dati è necessaria anche in caso di rischi non elevati per gli individui.
- Informare immediatamente gli interessati della violazione.
- Documentare la violazione includendo una descrizione della natura della violazione, indicando ad esempio quante persone sono interessate, il numero dei record di dati interessati, le conseguenze della violazione ed eventuali azioni correttive programmate o attuate dall'organizzazione.

**Quali sono le responsabilità di Microsoft in quanto responsabile del trattamento dei dati?**

Secondo il GDPR, Microsoft ha l’obbligo di informare immediatamente gli interessati, nel momento in cui viene a conoscenza di una violazione dei dati personali. In qualità di responsabile del trattamento dei dati, Microsoft si attiene sia ai requisiti del GDPR, sia alle proprie disposizioni contrattuali standard a livello mondiale. Tutte le violazioni dei dati personali confermate sono considerate incluse; non è prevista alcuna soglia di rischio di danno. Microsoft comunica ai clienti se la violazione dei dati è stata subita direttamente da Microsoft o da uno dei sub-titolari del trattamento. Sono stati implementati processi che consentono a Microsoft di identificare e contattare rapidamente il personale addetto agli incidenti di sicurezza di un'organizzazione. Inoltre, tutti i sub-titolari del trattamento sono obbligati per contratto a segnalare le proprie violazioni a Microsoft e a fornire garanzie in tal senso.

**Come fa Microsoft a identificare una violazione dei dati?**

Tutti i servizi e il personale di Microsoft seguono le procedure interne di gestione degli incidenti per garantire che siano adottate precauzioni adatte per evitare che si verifichino violazioni dei dati. Inoltre, Online Services dispone di controlli di sicurezza specifici per tutte le piattaforme per rilevare le violazioni di dati nei rari casi in cui si verificano.

**Come interviene Microsoft in caso di violazione dei dati?**

Per supportare il cliente nell'ambito di una violazione dei dati personali, Microsoft:
    - Personale di sicurezza qualificato per le procedure specifiche da seguire.
    - Ha implementato criteri, procedure e controlli per garantire la tenuta di registri dettagliati. Questa risposta include la documentazione che riguarda le circostanze dell'evento, le sue conseguenze e i provvedimenti adottati per porvi rimedio, oltre a monitorare e memorizzare le informazioni nei sistemi di gestione degli incidenti.

**In che modo Microsoft comunica una violazione dei dati?**

Microsoft ha adottato criteri e procedure per notificare tempestivamente le violazioni. Per soddisfare i requisiti di notifica all'autorità incaricata della protezione dei dati, viene fornita descrizione del processo usato per determinare se si è verificata una violazione dei dati personali, una descrizione della natura della violazione e una descrizione delle misure adottate per mitigare le conseguenze della violazione.

## <a name="accountability-readiness-checklists-for-the-gdpr"></a>Elenchi di controllo di preparazione della conformità al GDPR

Questi [elenchi di controllo](gdpr-arc.md) offrono un modo pratico per accedere alle informazioni necessarie per l'applicazione del GDPR quando si usano i prodotti Microsoft. È possibile gestire le voci dell’elenco di controllo con [Microsoft Compliance Manager](https://docs.microsoft.com/microsoft-365/compliance/compliance-manager) facendo riferimento all’ID controllo e al titolo del controllo nei controlli gestiti dal cliente nella sezione GDPR.

## <a name="gdpr-faqs"></a>Domande frequenti sul GDPR

**Microsoft assume degli impegni nei confronti dei propri clienti per quanto riguarda il GDPR?**

Sì. Il GDPR prevede che i titolari del trattamento (ad esempio le organizzazioni che usano i servizi online aziendali di Microsoft) si avvalgano solo di responsabili del trattamento (ad esempio Microsoft) che forniscono le garanzie necessarie per soddisfare i requisiti del GDPR. Microsoft ha previsto tali impegni per tutti i clienti con contratti multilicenza nell’ambito dei relativi accordi.

**In che modo Microsoft supporta i clienti nel garantire la conformità?**

Microsoft fornisce gli strumenti e la documentazione necessaria per supportare i clienti nel garantire la conformità al GDPR. Sono inclusi il supporto per i diritti dell'interessato, l'esecuzione delle valutazioni d'impatto sulla protezione dei dati e la collaborazione per risolvere eventuali violazioni dei dati personali.

**Quali impegni sono inclusi nelle Condizioni del GDPR?**

Le Condizioni del GDPR di Microsoft riflettono gli obblighi previsti dall’articolo 28 per i responsabili del trattamento. Ai sensi dell’articolo 28 il responsabile del trattamento si impegna a:

- Avvalersi di sub-responsabili soltanto con il consenso del titolare del trattamento e rimane responsabile per le operazioni eseguite dal sub-responsabile.
- Trattare i dati personali esclusivamente in base alle istruzioni del titolare, anche in merito al trasferimento.
- Assicurarsi che le persone che trattano i dati personali rispettino la riservatezza.
- Implementare misure tecniche e organizzativa appropriate per garantire un livello di sicurezza dei dati personali idoneo in base al rischio.
- Aiutare i titolari del trattamento nell'ambito dei loro obblighi di risposta alle richieste degli interessati di esercitare i propri diritti in base al GDPR.
- Soddisfare i requisiti di assistenza e notifica delle violazioni.
- Assistere i titolari del trattamento nella realizzazione delle valutazioni d'impatto sulla protezione dei dati e nei rapporti con le autorità garanti.
- Eliminare o restituire i dati personali alla fine della fornitura dei servizi.
- Supportare il titolare del trattamento nella dimostrazione della conformità al GDPR.

**Su quali basi Microsoft semplifica il trasferimento dei dati personali al di fuori dell'Unione Europea?**

Microsoft utilizza da molto le clausole contrattuali standard (note anche come clausole contrattuali tipo) come base per il trasferimento dei dati per i propri servizi online aziendali. Le clausole contrattuali standard sono condizioni standard fornite dalla Commissione Europea che possono essere usate per trasferire i dati al di fuori dello Spazio economico europeo in modo conforme. Microsoft ha integrato le clausole contrattuali standard in tutti i suoi contratti multilicenza tramite le [Condizioni dei servizi online ](http://www.microsoftvolumelicensing.com/DocumentSearch.aspx?Mode=3&DocumentTypeId=46). L'implementazione delle clausole contrattuali standard da parte di Microsoft è stata ritenuta conforme dal Gruppo di lavoro ex articolo 29. Quando è divenuto disponibile il Privacy Shield UE-USA, Microsoft è stata la prima società a ottenere la certificazione. Vedere [Certificazione di Microsoft per il Privacy Shield](https://www.privacyshield.gov/participant?id=a2zt0000000KzNaAAK&status=Active) e leggere le [Condizioni dei servizi online](http://www.microsoftvolumelicensing.com/DocumentSearch.aspx?Mode=3&DocumentTypeId=46). Il Privacy Shield EU-USA consente ai clienti che vogliono trasferire i propri dati negli Stati Uniti di farlo in maniera conforme ai propri obblighi di protezione dei dati.

**Quali sono le altre offerte di Microsoft per la conformità?**

Essendo una società internazionale con clienti in quasi ogni paese del mondo, Microsoft offre un insieme consistente di soluzioni di conformità per aiutare i clienti. Per un elenco completo delle offerte di conformità tra cui FedRamp, HIPAA/HITECH, ISO 27001, ISO 27002, ISO 27018, NIST 800-171, UK G-Cloud e molto altro, consultare gli [argomenti dedicati alle offerte di conformità](offering-home.yml).

**In che modo il GDPR interesserà la società?**

Il GDPR impone alle organizzazioni che raccolgono o trattano dati personali un'ampia gamma di requisiti, tra cui quello di rispettare sei principi chiave:

- *Trasparenza*,*correttezza* e *liceità* nella gestione e nell’utilizzo dei dati personali. Sarà necessario spiegare chiaramente alle persone in che modo vengono usati i dati personali e avere una "base giuridica" per trattarli.
- Limitare il trattamento dei dati personali per *finalità specifiche*, *esplicite* e *legittime*. Non è consentito riutilizzare o divulgare i dati personali per scopi non "compatibili" con le finalità per cui sono stati raccolti in origine.
- *Minimizzare la raccolta e la conservazione dei dati personali* a quanto sia adeguato e pertinente per le finalità previste.
- Garantire l'*esattezza dei dati personali* e consentirne la *cancellazione o rettifica*. Devono essere adottate tutte le misure necessarie affinché i dati personali conservati siano esatti e possano essere corretti in caso di errori.
- *Limitare la conservazione dei dati personali*. I dati personali devono essere conservati solo per il periodo necessario a raggiungere gli scopi per i quali sono stati raccolti.
- Garantire la *sicurezza*, *integrità* e *confidenzialità* dei dati personali. L'organizzazione deve adoperarsi per proteggere i dati personali adottando le misure di sicurezza tecniche e organizzative adeguate.

Occorre comprendere quali sono gli obblighi specifici dell'organizzazione per quanto riguarda il GDPR e in che modo è possibile rispettarli, potendo contare sull'aiuto di Microsoft lungo il percorso di adeguamento al GDPR.

**Quali diritti devono essere garantiti dalle aziende in base al GDPR?**

Il GDPR offre ai residenti dell'Unione Europea il controllo dei propri dati personali attraverso un insieme di "diritti dell'interessato". Tali diritti includono il diritto a:

- Accedere alle informazioni sulle modalità di utilizzo dei dati personali.
- Accedere ai dati personali di cui un'organizzazione è in possesso.
- Far eliminare o correggere dati personali non corretti.
- Far modificare e cancellare i dati personali in determinate circostanze (il cosiddetto "diritto all'oblio").
- Limitare o opporsi al trattamento automatico dei dati personali.
- Ricevere una copia dei dati personali.

**Cosa si intende per responsabili del trattamento e titolari del trattamento?**

Un titolare del trattamento è una persona fisica o giuridica, una pubblica autorità, un'agenzia o un altro organismo che, da solo o congiuntamente ad altri, determina le finalità e le modalità del trattamento dei dati personali. Un responsabile del trattamento è una persona fisica o giuridica, un'autorità pubblica o altro ente che tratta i dati personali per conto del titolare del trattamento.

**Il GDPR si applica ai responsabili e titolari del trattamento?**

Sì, il GDPR si applica sia ai titolari del trattamento sia ai responsabili del trattamento. I titolari devono servirsi esclusivamente di responsabili che attuano misure per soddisfare i requisiti del GDPR. Ai sensi del GDPR, i responsabili del trattamento sono soggetti a obblighi e responsabilità per la mancata conformità, o per violazione delle istruzioni fornite dal titolare del trattamento, aggiuntivi rispetto a quanto previsto dalla Direttiva sulla protezione dei dati. Gli obblighi del responsabile del trattamento includono, a titolo esemplificativo:

- Il trattamento dei dati solo in base alle istruzioni fornite dal titolare.
- Attuazione di misure tecniche e organizzative appropriate per proteggere i dati personali.
- Assistenza al titolare per quanto riguarda le richieste degli interessati.
- Garanzia che i responsabili secondari a cui si affida soddisfino questi requisiti.

**Quali sanzioni possono essere applicate alle aziende per la mancata conformità?**

Le sanzioni per il mancato rispetto di determinati requisiti del GDPR possono arrivare fino a 20 milioni di &euro; o al 4% del fatturato globale annuo, se superiore. Altre misure di riparazione individuali potrebbero aumentare il rischio in caso di mancato rispetto dei requisiti del GDPR.

**L'azienda deve nominare un responsabile della protezione dei dati?**

Ciò dipende da diversi fattori individuati dal regolamento. L'articolo 37 del GDPR prevede che i titolari e i responsabili del trattamento devono nominare un responsabile della protezione dei dati nei casi in cui: (a) il trattamento sia effettuato da un'autorità pubblica o da un organismo pubblico, ad eccezione delle autorità giurisdizionali nell'esercizio delle loro funzioni giurisdizionali; (b) le attività principali del titolare del trattamento o del responsabile del trattamento consistano in operazioni di trattamento che, per loro natura, ambito di applicazione e/o finalità, richiedono il monitoraggio regolare e sistematico degli interessati su larga scala; o (c) le attività principali del titolare del trattamento o del responsabile del trattamento consistano nel trattamento, su larga scala, di categorie particolari di dati personali di cui all'articolo 9 o di dati relativi a condanne penali e a reati di cui all'articolo 10.

**Quanto costerà adeguarsi al GDPR?**

La conformità al GDPR costerà tempo e denaro alla maggior parte delle organizzazioni, anche se la transizione può essere meno complessa per quelle organizzazioni che già operano secondo un modello di servizi cloud ben progettato e che hanno già attuato un programma efficace di governance dei dati.

**Come si fa a sapere se i dati trattati dall'organizzazione rientrano nell'ambito di applicazione del GDPR?**

Il GDPR regola la raccolta, la conservazione, l'elaborazione e la condivisione dei “dati personali”. I dati personali sono definiti in modo molto ampio nel GDPR, come qualsiasi dato relativo a una persona fisica identificata o identificabile.

I dati personali possono includere, ad esempio, identificatori online (come gli indirizzi IP), informazioni sui dipendenti, database di vendita, dati sui servizi al cliente, moduli per i feedback dei clienti, dati sulla posizione, dati biometrici, riprese a circuito chiuso, record relativi a programmi di fidelizzazione, informazioni sanitarie e finanziare e molto altro. Possono anche includere informazioni che potrebbero non sembrare personali, ad esempio la foto di un panorama senza persone, nel caso in cui le informazioni sono collegate tramite un numero di account o un codice univoco a una persona identificabile. Anche i dati personali pseudonimizzati possono essere dati personali se lo pseudonimo può essere ricondotto a una persona specifica. 

Il trattamento di alcune categorie "speciali" di dati personali, come i dati che rivelano l'origine etnica o razziale di una persona oppure relativi alla sua salute o al suo orientamento sessuale, è soggetto a regole ancora più rigide rispetto al trattamento dei dati personali "normali". La valutazione di tali dati personali è fatta caso per caso ed è consigliabile nominare un esperto per la valutazione delle specifiche circostanze.

**L’organizzazione tratta dati solo per conto di altri. Deve comunque adeguarsi al GDPR?**

Sì. Anche se le regole possono essere diverse in qualche modo, il GDPR si applica alle organizzazioni che raccolgono e trattano i dati per i propri scopi ("titolari del trattamento") e alle organizzazioni che trattano i dati per conto di altri ("responsabili del trattamento"). Questo requisito si differenzia dalla Direttiva sulla protezione dei dati, che si applica solo ai titolari del trattamento.

**Cosa si intende nello specifico per dati personali?**

Per dati personali si intende qualsiasi informazione riguardante una persona identificata o identificabile. Non vi è distinzione tra i ruoli privati, pubblici o professionali di una persona. I dati personali possono includere:

- Nome
- Indirizzo di residenza
- Indirizzo di lavoro
- Numero di telefono
- Numero di cellulare
- Indirizzo di posta elettronica
- Numero di passaporto
- Numero di carta di identità
- Numero di previdenza sociale (o equivalente)
- Patente di guida
- Informazioni fisiche, psicologiche o genetiche
- Informazioni mediche
- Identità culturale
- Dettagli bancari/numeri di conto
- Codice fiscale
- Indirizzo di lavoro
- Numeri di carta di credito/debito
- Post sui social media
- Indirizzo IP (area geografica Unione Europea)
- Posizione/dati GPS
- Cookies

**È consentito trasferire i dati al di fuori dell'Unione Europea?**

Sì, tuttavia il GDPR disciplina in modo rigido i trasferimenti dei dati personali delle persone residenti nell’UE al di fuori dello Spazio economico europeo. Potrebbe essere necessario creare un meccanismo legale specifico, ad esempio un contratto, o aderire a un meccanismo di certificazione per poter effettuare questi trasferimenti. I meccanismi usati da Microsoft sono descritti nelle Condizioni dei servizi online.

**La conformità prevede requisiti di conservazione dei dati. Questi requisiti prevalgono sul diritto di cancellazione?**

Nel caso in cui il trattamento prolungato e la conservazione dei dati abbiano una base giuridica, ad esempio "per l'adempimento di un obbligo legale che richieda il trattamento previsto dal diritto dell'Unione o dello Stato membro cui è soggetto il titolare del trattamento" (Articolo 17(3)(b)), il GDPR riconosce che le organizzazioni potrebbero essere obbligate a conservare i dati. È comunque necessario rivolgersi a un consulente legale per assicurarsi che le basi per la conservazione siano valutate tenendo in considerazione i diritti e le libertà degli interessati, le loro aspettative al momento della raccolta dei dati e così via.

**Il GDPR si occupa della crittografia?**

Nell'ambito del GDPR, la crittografia è identificata come misura protettiva che rende i dati personali incomprensibili in caso di violazione. Pertanto, il fatto che la crittografia venga utilizzata o meno può influire sui requisiti di notifica in caso di violazione dei dati personali. Il GDPR considera inoltre la crittografia come una misura tecnica o organizzativa appropriata in alcuni casi, a seconda del rischio. La crittografia è anche un requisito per la conformità al Payment Card Industry Data Security Standard e fa parte delle rigorose linee guida di conformità specifiche del settore dei servizi finanziari. I prodotti e servizi Microsoft come Azure, Dynamics 365, Enterprise Mobility + Security, Microsoft Office 365, SQL Server/Database SQL di Azure e Windows 10 offrono una solida crittografia dei dati in transito e dei dati inattivi.

**In che modo il GDPR cambia la risposta di un'organizzazione alle violazioni dei dati personali?**

Il GDPR cambia i requisiti in materia di protezione dei dati e rende più stringenti gli obblighi dei titolari e responsabili del trattamento per quanto riguarda la notifica delle violazioni dei dati personali. In base al nuovo regolamento, il responsabile del trattamento è tenuto a informare il titolare del trattamento senza ingiustificato ritardo dopo essere venuto a conoscenza di una violazione dei dati personali. Quando viene a conoscenza di una violazione dei dati personali, il titolare del trattamento è tenuto a informare l'autorità incaricata della protezione dei dati competente entro 72 ore. Se la violazione presenta un rischio elevato per i diritti e le libertà delle persone, i titolari dovranno anche informare gli interessati senza ingiustificato ritardo. Ulteriori indicazioni su questo argomento sono in fase di sviluppo da parte del Gruppo di lavoro ex articolo 29 dell'Unione Europea.

I prodotti e servizi Microsoft, quali Azure, Dynamics 365, Enterprise Mobility + Security, Microsoft Office 365 e Windows 10, offrono soluzioni utili per rilevare e valutare le violazioni e le minacce per la sicurezza e a ottemperare agli obblighi di notifica delle violazioni previsti dal GDPR.

## <a name="additional-resources"></a>Risorse aggiuntive

- [Per affrontare le tue esigenze relative al GDPR, rivolgiti a uno dei nostri partner globali che offrono soluzioni basate su Microsoft](https://aka.ms/findgdprpartner)
- [Scopri in che modo Microsoft gestisce i dati, dove si trovano, chi può accedervi e a quali condizioni e altro.](https://www.microsoft.com/trust-center/privacy)
- [Scopri in che modo Microsoft rispetta i principi del framework EU-U.S. Privacy Shield](https://blogs.microsoft.com/eupolicy/2016/07/11/eu-u-s-privacy-shield-progress-for-privacy-rights/)
- [Scopri quali sono le modalità di rilevamento, risposta e notifica da parte di Microsoft in caso di violazione dei dati personali ai sensi del GDPR](https://www.microsoft.com/trust-center/privacy/gdpr-data-breach)
- [Valutare subito il tuo grado di preparazione al GDPR](https://discover.microsoft.com/gdpr-readiness-assessment/)
