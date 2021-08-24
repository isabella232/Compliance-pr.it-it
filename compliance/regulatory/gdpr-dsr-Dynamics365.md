---
title: Richieste degli interessati per Dynamics 365 nell'ambito del GDPR e del CCPA
description: Informazioni su come trovare i dati personali e agire su di essi, e su come rispondere alle richieste DSR e CCPA dei clienti Dynamics 365.
keywords: Microsoft 365, Microsoft 365 Education, Documentazione Microsoft 365, GDPR, CCPA
ms.localizationpriority: high
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
hideEdit: true
ms.custom:
- seo-marvel-mar2020
titleSuffix: Microsoft GDPR
ms.openlocfilehash: 7b6919cbdf2ece468eeec8931b652972a74b07dc
ms.sourcegitcommit: 4c00fd65d418065d7f53216c91f455ccb3891c77
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/23/2021
ms.locfileid: "58482409"
---
# <a name="dynamics-365-data-subject-requests-for-the-gdpr-and-ccpa"></a>Richieste degli interessati per Dynamics 365 nell'ambito del GDPR e del CCPA

Il [Regolamento generale sulla protezione dei dati (GDPR)](https://ec.europa.eu/justice/data-protection/reform/index_en.htm) dell'Unione europea garantisce alle persone (denominate nel regolamento *interessati*) il diritto di gestire i dati personali raccolti da un datore di lavoro o da un'altra organizzazione o agenzia (definiti *titolari del trattamento dei dati* o semplicemente *titolari*). I dati personali sono descritti nel GDPR come dati che si riferiscono a una persona fisica identificata o identificabile. Il GDPR garantisce agli interessati diritti specifici sui propri dati personali; tali diritti includono la possibilità di ottenerne copie, richiedere di apportare delle modifiche ai dati, limitare il trattamento dei dati, eliminarli o riceverli in un formato elettronico affinché possano essere trasferiti a un altro titolare. Una richiesta formale di un interessato rivolta a un titolare in merito a un'operazione da effettuare sui propri dati personali è indicata in questo documento come *Richiesta del soggetto interessato* o Richiesta DSR (Data Subject Rights, Diritti del soggetto dei dati).

Analogamente, il California Consumer Privacy Act (CCPA) prevede obblighi e diritti in materia di privacy per i consumatori della California, inclusi diritti simili a quelli che il GDPR riconosce all'interessato, ad esempio il diritto di eliminare, ricevere e accedere alle informazioni personali (portabilità).  Nell'ambito dei diritti che i consumatori possono esercitare, il CCPA prevede inoltre l'obbligo per determinate divulgazioni, di protezioni contro la discriminazione e requisiti di consenso o rifiuto esplicito per alcuni trasferimenti di dati classificati come "vendite". In generale, la definizione di vendite include la condivisione di dati a titolo oneroso. Per altre informazioni sul CCPA, vedere il [California Consumer Privacy Act](offering-ccpa.md) e le [Domande frequenti sul California Consumer Privacy Act](ccpa-faq.yml).

La guida descrive come utilizzare i prodotti, i servizi e gli strumenti di amministrazione Microsoft per aiutare i nostri clienti titolari del trattamento dei dati a individuare e gestire i dati personali per rispondere alle richieste DSR. In particolare, ciò include come identificare, accedere e usare i dati e le informazioni personali che risiedono nel cloud Microsoft. Di seguito viene riportata una rapida panoramica dei processi descritti in questa guida:

- **Individuazione**: usare gli strumenti di ricerca e individuazione per trovare più facilmente i dati dei clienti che potrebbero essere oggetto di una richiesta dell'interessato. Dopo aver raccolto dei documenti potenzialmente reattivi, è possibile eseguire una o più delle azioni DSR descritte nella seguente procedura per rispondere alla richiesta. In alternativa, si può determinare che la richiesta non soddisfa le linee guida dell'organizzazione relative alla risposta alle richieste degli interessati.
- **Accesso:** recuperare i dati personali che risiedono nel cloud Microsoft e, se richiesto, crearne una copia che è disponibile per l'interessato.
- **Rettifica:** apportare modifiche o implementare le azioni richieste sui dati personali, ove applicabile.
- **Limitazione**: limitare il trattamento dei dati personali, rimuovendo le licenze per vari servizi online o disattivando i servizi desiderati, dove possibile.
- **Eliminazione:** rimuovere in modo definitivo i dati personali che risiedono nel cloud Microsoft.
- **Esportazione/ricezione (portabilità):** fornire all'interessato una copia elettronica dei dati o delle informazioni personali in un formato leggibile da una macchina. Secondo il CCPA, le informazioni personali sono qualsiasi informazione riguardante una persona fisica identificata o identificabile. Non esiste distinzione tra i ruoli privati, pubblici o professionali di una persona. Il termine definito "informazioni personali" combacia con il termine "dati personali" del GDPR. Tuttavia, il CCPA include anche i dati relativi alla famiglia e al nucleo familiare. Per altre informazioni sul CCPA, vedere il [California Consumer Privacy Act](offering-ccpa.md) e le [Domande frequenti sul California Consumer Privacy Act](ccpa-faq.yml).

Ogni sezione di questa guida illustra le procedure tecniche che un'organizzazione titolare del trattamento dei dati può adottare per rispondere a una richiesta DSR per i dati personali nel cloud Microsoft

## <a name="gdpr-terminology"></a>Terminologia del GDPR

Di seguito vengono fornite le definizioni dei termini importanti nella presente guida:

- **Titolare:** la persona fisica o giuridica, l'autorità pubblica, l'agenzia o altro ente che, autonomamente o unitamente ad altri soggetti, determina gli obiettivi e i mezzi del trattamento dei dati personali; laddove gli obiettivi e i mezzi di tale trattamento sono determinati da una normativa europea o di uno specifico Stato membro dell'UE, il titolare del trattamento dei dati o i criteri specifici per la sua designazione potrebbero essere forniti da tale normativa europea o di uno specifico Stato membro dell'UE.
- **Dati personali e interessato:** tutte le informazioni concernenti una persona fisica identificata o identificabile ("interessato"). Una persona fisica è identificabile se può essere identificata, direttamente o indirettamente, in particolare facendo riferimento a un identificatore (ad esempio un nome, un numero di identificazione, dati di posizione o un identificatore online) o a uno o più fattori relativi all'identità fisica, fisiologica, genetica, mentale, economica, culturale o sociale di tale persona fisica.
- **Responsabile:** una persona fisica o giuridica, un'autorità pubblica o altro ente che si occupa del trattamento dei dati personali per conto del titolare.
- **Dati dei clienti**: tutti i dati, compresi tutti i file di testo, audio o immagini e il software, che vengono forniti a Microsoft da, o per conto di, un cliente tramite l'uso del servizio aziendale. I dati dei clienti includono (1) informazioni che consentono l'identificazione personale degli utenti finali (ad esempio, nomi utente e informazioni di contatto in Azure Active Directory) e contenuti per i clienti che un cliente stesso carica o crea in servizi specifici (ad esempio, contenuti per i clienti in un account di archiviazione di Azure, contenuti per i clienti in un database SQL di Azure o un'immagine della macchina virtuale di un cliente in Macchine virtuali di Azure).
- **Log generati dal sistema:** log e dati relativi generati da Microsoft che consentono a Microsoft di fornire servizi aziendali agli utenti. I log generati dal sistema contengono dati principalmente presentati con l'uso di pseudonimi come identificatori univoci (in genere, un numero generato dal sistema con cui non è possibile identificare direttamente un soggetto, ma che viene utilizzato per fornire i servizi aziendali agli utenti). I log generati dal sistema possono anche contenere informazioni personali sugli utenti finali, come un nome utente.

## <a name="how-this-guide-can-help-you-meet-your-controller-responsibilities"></a>Come questa guida consente di adempiere alle proprie responsabilità di titolare del trattamento dei dati

La guida, suddivisa in due parti, descrive come usare prodotti, servizi e strumenti di amministrazione di Dynamics 365 per aiutare l'utente a individuare e gestire i dati nel cloud Microsoft per rispondere alle richieste degli interessati che esercitano i diritti previsti dal GDPR. La prima parte riguarda i dati personali inclusi nei dati del cliente e la seconda parte riguarda altri dati personali con pseudonimi acquisiti nei log generati dal sistema.

- **Parte 1: rispondere alle richieste degli interessati relative ai dati personali, inclusi i dati del cliente.** La parte 1 di questa guida spiega come accedere, risolvere, limitare, eliminare ed esportare i dati personali da applicazioni di Dynamics 365 (software-as-a-service), elaborati come parte dei dati del cliente forniti al servizio online.
- **Parte 2: rispondere alle richieste DSR per dati con pseudonimi.** Quando si usano servizi aziendali Dynamics 365, Microsoft genera alcune informazioni (denominate in questo documento come *log generati dal sistema*) per fornire il servizio, che è limitato al footprint di utilizzo lasciato dall'utente finale per identificare le azioni nel sistema. Sebbene questi dati non possano essere attribuiti a un soggetto dei dati specifico senza l'ausilio di informazioni aggiuntive, alcuni possono essere considerati personali in base all'RGPD. La parte 2 di questa guida spiega come accedere, eliminare ed esportare i log generati dal sistema creati da Dynamics 365.

## <a name="preparing-for-data-subject-rights-investigations"></a>Preparazione per indagini sui diritti degli interessati.

Quando gli interessati esercitano i propri diritti ed effettuano richieste, considerare quanto segue:

- Identificare correttamente la persona e il ruolo (ad esempio se si tratta di un dipendente, cliente o fornitore) attraverso le informazioni fornite dall'interessato durante la richiesta. Tali informazioni potrebbero essere un nome, un ID dipendente, un numero cliente o altro identificatore.
- Registrare i dati e l'ora della richiesta (sono disponibili 30 giorni per completare la richiesta).
- Dichiarare che la richiesta soddisfa i requisiti della propria organizzazione quando si assolve o si rifiuta una richiesta dell'interessato. Ad esempio, assicurarsi che l'esecuzione della richiesta non sia in conflitto con altri obblighi legali, normativi o finanziari e che non pregiudichi i diritti e la libertà altrui.
- Verificare di disporre delle informazioni relative alla richiesta.

## <a name="part-1-responding-to-data-subject-rights-requests-for-personal-data-included-in-customer-data"></a>Parte 1: rispondere alle richieste degli interessati relative ai dati personali inclusi nei dati del cliente

Negli articoli seguenti sono disponibili informazioni che consentono di pianificare e rispondere alle richieste degli interessati relative ai dati personali inclusi nei dati del cliente elaborati in Dynamics 365. È importante tenere presente che i dati personali possono essere presenti in altre categorie di dati elaborati da Microsoft nel corso del servizio di una sottoscrizione a servizi online (ad esempio i dati dell'amministratore o del supporto definiti nell'informativa sulla privacy di Microsoft). Questo documento si limita a fornire supporto per l'individuazione e la gestione delle richieste degli interessati che riguardano i dati personali presenti nei dati del cliente forniti a Dynamics 365.

Dynamics 365 è un servizio online che offre più funzioni di elaborazione dati di un software sotto forma di software come servizio (SaaS). Di conseguenza, Dynamics 365 offre un'ampia gamma di funzionalità per l'elaborazione di ampie raccolte di dati, che possono variare in base alla natura, allo scopo o ad altri attributi specifici (ad esempio, dati delle vendite, transazioni, contabilità, informazioni delle risorse umane e così via). Alla luce di tali varietà, Dynamics 365 offre più moduli, campi, schemi, endpoint e logica per elaborare i dati del cliente, che rispecchiano i vari modi in cui le richieste degli interessati possono essere rivolte a ogni applicazione. In questa guida è possibile osservare i diversi modi per soddisfare le specifiche richieste degli interessati, selezionando le descrizioni tecniche di ogni applicazione Dynamics 365.

### <a name="dynamics-365"></a>Dynamics 365

#### <a name="finding-customer-data"></a>Trovare i dati del cliente

Il primo passaggio per rispondere a una richiesta dell'interessato consiste nel cercare e identificare i dati del cliente che costituiscono l'oggetto della richiesta.

Per usare i dati personali presenti nelle applicazioni di lavoro in Dynamics 365 - Customer Engagement, è importante classificarli correttamente. Dynamics 365 - Customer Engagement offre la flessibilità necessaria per creare un'estensione dell'applicazione relativa alla classificazione dei dati. Una corretta classificazione consente di identificare le informazioni come dati personali, facilitandone l'individuazione e il recupero durante le operazioni di risposta alle richieste degli interessati. Può anche essere utile per esigenze di conformità a requisiti normativi sulla raccolta e gestione dei dati personali.

Microsoft offre funzionalità che possono essere utili per rispondere alle richieste degli interessati e per accedere ai dati del cliente. Tuttavia, spetta dell'utente assicurare che i dati personali siano collocati e classificati in modo appropriato.

***Dynamics 365 - Customer Engagement*** offre diversi metodi per cercare dati personali nei record, ad esempio: ricerca avanzata e ricerca per record. Tutte queste funzioni consentono di identificare (trovare) i dati personali.

- [Ricerca avanzata](/dynamics365/customer-engagement/basics/save-advanced-find-search)
- [Ricerca per record](/dynamics365/customer-engagement/basics/search-records) tra più tipi di record

In Dynamics 365 for Marketing, sono disponibili le seguenti funzionalità aggiuntive:

1. [Creare report Power BI](/power-bi/service-connect-to-microsoft-dynamics-crm) per filtrare e identificare i dati del cliente.
2. Utilizzare Insight Views su contatti e oggetti di esecuzione marketing per identificare punti dati aggiuntivi che possono contenere i dati del cliente.

***Dynamics 365 Customer Service Insights*** offre un elenco di risorse utili per [trovare i dati del cliente](/dynamics365/ai/customer-service-insights/gdpr-discovery) e rispondere alle richieste dei clienti relative al GDPR.

***Dynamics 365 for Finance and Operations*** offre diversi modi per cercare dati del cliente. In qualità di amministratore tenant è possibile effettuare le seguenti operazioni per cercare dati del cliente:

- Organizzare i dati del cliente al fine di poter individuare rapidamente i dati personali. A tale scopo, vedere [come classificare l'inventario dati](/dynamics365/unified-operations/dev-itpro/gdpr/gdpr-guide#detailed-inventory).
- Usare il [rapporto di ricerca persone](/dynamics365/unified-operations/dev-itpro/gdpr/gdpr-guide#the-person-search-report) per trovare e raccogliere dati personali dell'utente.
- [Estendere il rapporto di ricerca persone](/dynamics365/unified-operations/dev-itpro/gdpr/gdpr-extend-person-search-report) creando una nuova entità o estendendone una esistente.
- Usare le funzionalità di ricerca e filtro per trovare dati personali specifici ed esportarli tramite la funzionalità di esportazione di Microsoft Office o stampare le informazioni in un PDF con le estensioni del browser.
- Creare un modulo personalizzato che consente di individuare ed esportare i dati personali.
- Creare un portale esterno o sito Web che consente a un cliente autenticato di visualizzare i propri dati personali.

***Dynamics 365 Business Central*** fornisce vari modi per cercare i dati dei clienti. Per informazioni dettagliate, vedere [Ricerca, filtro e ordinamento di dati](/dynamics365/business-central/ui-enter-criteria-filters).

***Dynamics 365 for Talent*** fornisce funzionalità di ricerca avanzata e filtro per trovare dati personali, mentre la funzionalità di esportazione di Microsoft Office consente di esportare o stampare le informazioni in un PDF con le estensioni del browser.

- Usare il [rapporto di ricerca persone](/dynamics365/unified-operations/dev-itpro/gdpr/gdpr-guide#the-person-search-report) per trovare e raccogliere i dati del cliente.
- [Estendere il rapporto di ricerca persone](/dynamics365/unified-operations/dev-itpro/gdpr/gdpr-extend-person-search-report) creando una nuova entità o estendendone una esistente.

### <a name="providing-a-copy-of-customer-data"></a>Fornire una copia dei dati dei clienti

I dati del cliente in ***Dynamics 365 for Customer Engagement*** possono essere esportati utilizzando le funzionalità di esportazione entità complete o in un file di Excel statico. Tramite Excel, è possibile modificare i dati personali da includere nella richiesta di portabilità e salvarli in un formato leggibile di uso comune, ad esempio con estensione CSV o XML. I record di Dynamics 365 for Customer Engagement possono essere esportati anche tramite l'[API Web Common Data Service](/powerapps/developer/common-data-service/webapi/overview).

Inoltre, per Dynamics 365 for Marketing è fornita un'[API dedicata](/dynamics365/customer-engagement/marketing/developer/retrieve-interactions-contact) che consente ai clienti di creare estensioni che permettono di recuperare record aggiuntivi di interazioni cliente acquisite che possono contenere dati personali. L'API carica tutte le informazioni pertinenti dal sistema di back-end e le assembla in un unico documento portatile.

***Dynamics 365 Customer Service Insights*** consente di [fornire una copia dei dati del cliente](/dynamics365/ai/customer-service-insights/gdpr-export) usando l'esportazione dei dati.

I dati del cliente in ***Dynamics 365 for Finance and Operations** _ possono essere esportati utilizzando le funzionalità di esportazione entità complete. Tramite le [_entità di gestione e integrazione dei dati*](/dynamics365/unified-operations/dev-itpro/data-entities/data-management-integration-data-entity), gli amministratori tenant possono utilizzare le entità disponibili, crearne di nuove o estendere quelle esistenti, per un'esportazione di dati personali ripetibile in Excel o in altri formati comuni tramite [*processi di esportazione e importazione dei dati*](/dynamics365/unified-operations/dev-itpro/data-entities/data-import-export-job). In alternativa, molti elenchi possono essere esportati in un file Excel statico per facilitare una richiesta di portabilità dei dati. Quando i dati del cliente vengono esportati in Excel, è possibile modificare i dati personali da includere nella richiesta di portabilità e quindi salvare il file in un formato leggibile di uso comune, ad esempio con estensione CSV o XML. Si può usare anche il *rapporto di ricerca persone* per fornire all'interessato i dati classificati come dati personali.

In ***Dynamics 365 - Business Central*** è possibile usare due caratteristiche per inviare una copia dei dati del cliente all'interessato:

È possibile esportare i dati del cliente in un file Excel. In Excel, modificare i dati del cliente da includere nella richiesta di portabilità e salvarli in un formato leggibile di uso comune, ad esempio con estensione .csv o .xml. Per informazioni dettagliate, vedere [Esportazione dei dati aziendali in Excel.](/dynamics365/business-central/about-export-data)

In ***Dynamics 365 for Talent***, è possibile utilizzare [Estendere il rapporto di ricerca persone](/dynamics365/unified-operations/dev-itpro/gdpr/gdpr-extend-person-search-report) per raccogliere informazioni per una richiesta di una copia dei dati personali dell'interessato.

### <a name="rectifying-customer-data"></a>Rettificare i dati del cliente

***Dynamics 365 for Customer Engagement*** offre i seguenti metodi per correggere i dati del cliente incompleti o non corretti o per cancellarli:

- Cercare i dati del cliente tramite le funzionalità descritte in "Ricerca di dati del cliente" e modificare direttamente i dati nei moduli Customer Engagement. Le modifiche possono essere eseguite a livello di riga singola o più righe possono essere modificate direttamente.
- Modificare più record Customer Engagement in blocco tramite il componente aggiuntivo di Microsoft Office per esportare i dati in Microsoft Excel, apportare le modifiche desiderate e quindi importare i dati modificati da Excel in Dynamics 365 for Customer Engagement.

Inoltre, per Dynamics 365 for Marketing è anche possibile:

- Aggiornare i dati personali nella pagina di destinazione, modificando direttamente una o più righe
- Preparare una pagina di [centri di sottoscrizione](/dynamics365/customer-engagement/marketing/set-up-subscription-center) contenente tutti i campi di contatto modificabili che possono essere inclusi. In questo modo gli utenti finali possono aggiornare le proprie informazioni il più possibile.

***Dynamics 365 Customer Service Insights*** offre inoltre alle organizzazioni le funzionalità per [rettificare o modificare i dati del cliente](/dynamics365/ai/customer-service-insights/gdpr-summary).

In **Dynamics 365 for Finance and Operations** _, è inoltre possibile usare [_strumenti di personalizzazione*](/dynamics365/unified-operations/dev-itpro/dev-tools/developer-home-page), ma la decisione e l'implementazione spettano comunque all'utente.

***Dynamics 365 Business Central*** offre due modi per correggere i dati del cliente che sono incompleti o non corretti.

Per una rapida modifica in blocco di più record Business Central, esportare gli elenchi in Excel con il [componente aggiuntivo di Excel per Business Central](/dynamics365/business-central/finance-analyze-excel#the--excel-add-in), correggere più record e quindi pubblicare i dati modificati da Excel in Business Central. Per informazioni dettagliate, vedere [Esportazione dei dati aziendali in Excel](/dynamics365/business-central/about-export-data).

È possibile modificare i dati del cliente archiviati in un campo, ad esempio le informazioni relative a un cliente nella scheda del cliente, modificando manualmente l'elemento dati che contiene dati personali di destinazione. Per informazioni dettagliate, vedere [Immissione di dati](/dynamics365/business-central/ui-enter-data).

#### <a name="brief-note-about-modifying-entries-in-business-transactions"></a>Breve nota sulla modifica delle voci nelle transazioni commerciali

I record di transazione, ad esempio le voci generali, del cliente e dei documenti fiscali, sono essenziali per l'integrità di un sistema di pianificazione delle risorse dell'organizzazione. I dati personali che fanno parte della transazione finanziaria o di altro tipo resteranno "così come sono" in conformità alle leggi finanziarie (ad esempio, alle norme fiscali), alla politica di prevenzione delle frodi (ad esempio, controllo di sicurezza) o alle certificazioni di settore. Di conseguenza, Dynamics 365 for Finance and Operations e Dynamics 365 Business Central limitano la modifica dei dati in tali record.

Archiviando dati personali nei record delle transazioni aziendali, l'unico modo per correggere, eliminare o limitare l'elaborazione dei dati personali per soddisfare la richiesta del titolare dei dati è quello di usare le [funzionalità di personalizzazione](/dynamics365/business-central/dev-itpro/index) di Dynamics 365 Business Central. [La decisione di soddisfare una richiesta di modifica dei dati dell'interessato](/dynamics365/unified-operations/dev-itpro/gdpr/gdpr-guide#reasons-why-certain-personal-data-may-not-be-modified-or-deleted) e la successiva implementazione è di responsabilità dell'utente.

### <a name="restricting-the-processing-of-customer-data"></a>Limitazione del trattamento dei dati del cliente

Quando si riceve una richiesta da un interessato volta a limitare l'elaborazione dei dati del cliente, è possibile estrarre facilmente i dati del cliente dal servizio online e archiviarli in un contenitore separato (ad esempio in un archivio locale o in un servizio di Web separato con funzionalità di isolamento dei dati) e isolato dalle funzioni di elaborazione fornite dalle applicazioni cloud.

È disponibile un meccanismo alternativo, ad esempio il blocco di elaborazione dei dati di ***Dynamics 365 Business Central***, in cui gli utenti possono bloccare i record del soggetto dei dati specifico. Per informazioni dettagliate, [vedere Limitazione dell'elaborazione dei dati per un soggetto dei dati](/dynamics365/business-central/admin-responding-to-requests-about-personal-data#restrict-data-processing-for-a-data-subject). Quando un record è contrassegnato come bloccato, Dynamics 365 Business Central sospende l'elaborazione dei dati del cliente dell'interessato. Non è possibile creare nuove transazioni con un record bloccato, ad esempio, non è possibile creare una nuova fattura per un cliente, quando il cliente o l'agente di vendita è bloccato.

### <a name="deleting-customer-data"></a>Eliminare i dati del cliente

Quando un interessato chiede di eliminare i dati del cliente, esistono diversi modi per eseguire questa operazione:

- Modificare più record Dynamics 365 in blocco tramite il componente aggiuntivo di Microsoft Office per esportare i dati in Microsoft Excel, apportare le modifiche desiderate e quindi importare di nuovo i dati modificati da Excel nel servizio online.
- È possibile eliminare i dati del cliente archiviati in un campo qualsiasi, individuando i dati da eliminare ed eliminando manualmente l'elemento dati che contiene i dati del cliente di destinazione, ad esempio eliminando definitivamente il record del contatto che rappresenta l'interessato e altri record che contengono dati personali

Inoltre, in Dynamics 365 Marketing, l'eliminazione di un contatto garantisce che vengano rimossi anche i dati di interazione marketing in uscita con le informazioni personali. Per i campi o le entità personalizzate, è necessario personalizzare il sistema per assicurarsi che elimini tutti i dati del cliente dai record correlati e/o li scolleghi dal record del contatto in modo che tutte le informazioni personali vengano rimosse. I clienti che usano il modulo di marketing in tempo reale devono anche inviare un ticket di supporto con la richiesta di eliminazione in modo che tutti i dati di interazione in tempo reale vengano rimossi. Per altre informazioni, vedere la [guida per sviluppatori (marketing)](/dynamics365/customer-engagement/marketing/developer/marketing-developer-guide).

***Dynamics 365 Customer Service Insights*** offre inoltre alle organizzazioni funzionalità per [eliminare i dati del cliente](/dynamics365/ai/customer-service-insights/gdpr-delete).

In alternativa, in ***Dynamics 365 for Finance and Operations** _ è possibile usare [_strumenti di personalizzazione*](/dynamics365/unified-operations/dev-itpro/dev-tools/developer-home-page) per cancellare e modificare i dati del cliente.

Quando in ***Dynamics 365 Business Central*** un interessato chiede di eliminare i propri dati personali inclusi nei dati del cliente, esistono diversi modi per soddisfare questa richiesta:

- Per una rapida modifica in blocco di più record Business Central, esportare i dati in Excel con il [componente aggiuntivo di Excel per Business Central](/dynamics365/business-central/finance-analyze-excel#the--excel-add-in), eliminare più record e quindi pubblicare le modifiche da Excel di nuovo in Business Central. Per informazioni dettagliate, vedere [Esportazione dei dati aziendali in Excel](/dynamics365/business-central/about-export-data).
- È possibile eliminare i dati del cliente archiviati in un campo qualsiasi, eliminando manualmente l'elemento dati che contiene i dati del cliente di destinazione. Per informazioni dettagliate, vedere [Immissione di dati](/dynamics365/business-central/ui-enter-data).
- È possibile eliminare i dati del cliente direttamente, ad esempio eliminando un contatto e quindi eseguendo il processo batch Delete Canceled Interaction Log Entries per eliminare le interazioni di quel contatto.
- È possibile [eliminare documenti](/dynamics365/business-central/admin-manage-documents) contenenti dati del cliente, ad esempio note e fatture di acquisto e vendita pubblicate.

Oltre all'eliminazione in blocco o individuale di record distinti, tenere presente che solo gli utenti che hanno cessato la collaborazione possono essere eliminati completamente da ***Dynamics 365 for Talent***. [Seguire la procedura riportata di seguito per eliminare gli utenti che hanno cessato la collaborazione](/dynamics365/unified-operations/dev-itpro/gdpr/respond-dsr-request-talent#additional-notes-that-apply-to-requests-for-personal-data).

### <a name="exporting-customer-data"></a>Esportazione dei dati del cliente

Per rispondere alla richiesta di portabilità dei dati, i dati del cliente in ***Dynamics 365 for Customer Engagement*** possono essere esportati utilizzando le funzionalità di esportazione entità complete o in un file di Excel statico. Tramite Excel, è possibile modificare i dati personali da includere nella richiesta di portabilità e salvarli in un formato leggibile di uso comune, ad esempio con estensione CSV o XML.

Inoltre, per Dynamics 365 for Marketing è fornita un'[API dedicata](/dynamics365/customer-engagement/marketing/developer/retrieve-interactions-contact) che consente ai clienti di creare estensioni che permettono di recuperare record aggiuntivi di interazioni cliente acquisite che possono contenere dati personali. L'API carica tutte le informazioni pertinenti dal sistema di back-end e le assembla in un unico documento portatile.

Per ***Dynamics 365 Customer Service Insights*** è possibile [esportare i dati del cliente](/dynamics365/ai/customer-service-insights/gdpr-export) usando il portale di gestione di Azure.

***Dynamics 365 for Finance and Operations*** offre entità di gestione e integrazione dei dati, che consentono alle entità disponibili, appena create o estese, un'esportazione di dati personali ripetibile in Excel o in altri formati comuni tramite [processi di esportazione e importazione dei dati](/dynamics365/unified-operations/dev-itpro/data-entities/data-import-export-job). In alternativa, molti elenchi possono essere esportati in un file Excel statico per facilitare una richiesta di portabilità dei dati. Quando i dati del cliente vengono esportati in Excel, è possibile modificare i dati personali da includere nella richiesta di portabilità e quindi salvare il file in un formato leggibile di uso comune, ad esempio con estensione CSV o XML.

Dynamics 365 for Finance and Operations e ***Dynamics 365 for Talent*** offrono il rapporto di ricerca persone per fornire dati ai soggetti dei dati classificati come dati personali.

***Dynamics 365 Business Central*** offre le caratteristiche seguenti:

- È possibile esportare i dati del cliente in un file Excel, modificare i dati del cliente da includere nella richiesta di portabilità e salvarli in un formato leggibile di uso comune, ad esempio con estensione CSV o XML. Per informazioni dettagliate, vedere [Esportazione dei dati aziendali in Excel](/dynamics365/business-central/about-export-data).
- È possibile esportare i dati del cliente in un file Excel, modificare i dati del cliente da includere nella richiesta di portabilità e salvarli in un formato leggibile di uso comune, ad esempio con estensione CSV o XML. Per informazioni dettagliate, vedere [Esportazione dei dati aziendali in Excel](/dynamics365/business-central/about-export-data).


## <a name="part-2-responding-to-dsrs-for-system-generated-logs"></a>Parte 2: rispondere alle richieste DSR per i log generati dal sistema

Microsoft offre la possibilità di accedere, esportare ed eliminare log generati dal sistema che possono essere considerati personali secondo una definizione ampia di "dati personali" del GDPR. Esempi di log generati dal sistema che possono essere considerati personali ai sensi del GDPR includono:

- Dati di utilizzo di prodotti e servizi, ad esempio log di attività dell'utente
- Richieste di ricerca degli utenti e dati della query
- Dati generati da prodotti e servizi, come risultato della funzionalità del sistema e dell'interazione da parte di utenti o di altri sistemi

La possibilità di limitare o rettificare dati nei log generati dal sistema non è supportata. I dati nei log generati dal sistema costituiscono le azioni effettive eseguite del cloud Microsoft e i dati di diagnostica e le modifiche a tali dati possono compromettere il record cronologico delle azioni, aumentando i rischi per la sicurezza e le truffe.

### <a name="accessing-and-exporting-system-generated-logs"></a>Accesso ed esportazione di log generati dal sistema

Gli amministratori possono accedere ai log generati dal sistema legati all'uso da parte di uno specifico utente dei servizi e delle applicazioni di Dynamics 365. Per accedere ed esportare i log generati dal sistema:

1. Passare a [Microsoft Service Trust Portal](https://servicetrust.microsoft.com/) ed eseguire l'accesso con le credenziali di amministratore globale di Dynamics 365.
2. Nell'elenco a discesa **Privacy** nella parte superiore della pagina, fare clic su **Richiesta DSR**.
3. Nella pagina **Richiesta DSR**, in **Log generati dal sistema**, fare clic su **Esportazione log di dati**.
    > [!NOTE]
    > Viene visualizzato **Esportazione log di dati**. Si noti che viene visualizzato un elenco di richieste di esportazione dati inviate dall'organizzazione.
4. Per creare una nuova richiesta per un utente, fare clic su **Crea richiesta di esportazione dati**.

Dopo aver creato una nuova richiesta, questa sarà inserita nella pagina **Esportazione log di dati**, in cui è possibile tenere traccia del suo stato. Una volta completata una richiesta, è possibile fare clic su un collegamento per accedere ai log generati dal sistema, che verranno esportati in un percorso di archiviazione di Azure dell'organizzazione entro 30 giorni dalla creazione della richiesta. I dati verranno salvati in formati leggibili da macchina di uso comune, ad esempio JSON o XML. Se non si dispone di un account Azure e di un percorso di archiviazione di Azure, sarà necessario creare l’account e/o il percorso di archiviazione per l'organizzazione affinché lo strumento Esportazione log di dati possa esportare i log generati dal sistema.

Azure supporta questa richiesta, consentendo all'organizzazione di esportare i dati in formato JSON nativo nel contenitore di archiviazione di Azure specificato[. Vedere l'articolo di introduzione su Archiviazione BLOB di Archiviazione di Microsoft Azure](/azure/storage/common/storage-introduction#blob-storage). I dati recuperati non includeranno dati che possono compromettere la sicurezza e la stabilità del servizio.

> [!IMPORTANT]
> È necessario essere un amministratore tenant per esportare i dati di un utente dal tenant.

La tabella seguente riepiloga l'accesso e l'esportazione dei log generati dal sistema:

| **Domanda** | **Risposta** |
|:----|:---|
|**Quanto tempo impiega lo strumento di esportazione di log di dati di Microsoft per completare una richiesta?**| Ciò può dipendere da diversi fattori. Nella maggior parte dei casi l'operazione deve essere completata in uno o due giorni, ma può richiedere fino a 30 giorni. |
|**In quale formato sarà l'output?**| L'output sarà fornito in file leggibili strutturati come XML, CSV o JSON. |
|**Quali dati vengono restituiti dallo strumento di esportazione di log di dati?**| Lo strumento di esportazione di log di dati restituisce log generati dal sistema che vengono archiviati da Microsoft. I dati esportati includono vari servizi Microsoft, tra cui Office 365, Azure e Dynamics. |
|***Chi ha accesso allo strumento di esportazione dei log di dati per inviare richieste di accesso a log generati dal sistema?**| Gli amministratori globali di Dynamics 365 avranno accesso all'utilità di gestione file registro dell'RGDP. |
|**Come vengono restituiti i dati all'utente?**| I dati verranno esportati nel percorso di Archiviazione di Microsoft Azure dell'organizzazione. Spetterà agli amministratori dell'organizzazione stabilire come questi dati verranno visualizzati/restituiti agli utenti. |
|**Che aspetto avranno i dati nei log generati dal sistema?**| Esempio di un record di log generato dal sistema in formato JSON: <br><br> "DateTime": "2017-04-28T12:09:29-07:00", <br> "AppName": "SharePoint", <br> "Action": "OpenFile", <br> "IP": "154.192.13.131", <br> "DevicePlatform": "Windows 1.0.1607" |

### <a name="deleting-system-generated-logs"></a>Eliminazione di log generati dal sistema

Per eliminare i log generati dal sistema recuperati durante una richiesta di accesso, è necessario rimuovere l'utente dal servizio ed eliminare definitivamente il suo account Azure Active Directory. Per istruzioni su come eliminare definitivamente un utente, vedere la sezione [Passaggio 5: eliminazione](gdpr-dsr-azure.md#step-5-delete) nell'argomento relativo alle richieste degli interessati in Azure. È importante tenere presente che l'eliminazione definitiva di un account utente, un volta avviata, è irreversibile. Se si elimina definitivamente un account utente, i dati dell'utente, ad eccezione dei dati che possono compromettere la sicurezza e la stabilità del servizio, verranno rimossi dai log generati dal sistema per quasi tutti i servizi di Dynamics 365 entro 30 giorni.

## <a name="learn-more"></a>Altre informazioni

- [Centro protezione Microsoft](https://www.microsoft.com/trust-center/privacy/gdpr-overview)
