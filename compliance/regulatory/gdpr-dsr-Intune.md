---
title: Richieste degli interessati per Intune nell'ambito del GDPR e del CCPA
description: Comprendi come trovare i dati personali e agire su di essi, e come rispondere alle richieste DSR e CCPA dei clienti usando Microsoft Intune.
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
ms.custom:
- seo-marvel-mar2020
hideEdit: true
titleSuffix: Microsoft GDPR
ms.openlocfilehash: b718c4121ebf32e1c87342f778b66ecb07203738
ms.sourcegitcommit: 4c00fd65d418065d7f53216c91f455ccb3891c77
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/23/2021
ms.locfileid: "58482399"
---
# <a name="intune-data-subject-requests-for-the-gdpr-and-ccpa"></a>Richieste degli interessati per Intune nell'ambito del GDPR e del CCPA

Il [Regolamento generale sulla protezione dei dati (GDPR)](https://ec.europa.eu/justice/data-protection/reform/index_en.htm) dell'Unione europea garantisce alle persone (denominate nel regolamento *interessati*) il diritto di gestire i dati personali raccolti da un datore di lavoro o da un'altra organizzazione o agenzia (definiti *titolari del trattamento dei dati* o semplicemente *titolari*). I dati personali sono descritti nel GDPR come dati che si riferiscono a una persona fisica identificata o identificabile. Il GDPR garantisce agli interessati diritti specifici sui propri dati personali; tali diritti includono la possibilità di ottenere delle copie dei dati personali, richiedere di apportare delle modifiche ai dati, limitare il trattamento dei dati, eliminarli o riceverli in un formato elettronico affinché possano essere trasferiti a un altro titolare. Una richiesta formale di un interessato rivolta a un titolare in merito a un'operazione da effettuare sui propri dati personali è denominata *Richiesta dell'interessato* (DSR).

Analogamente, il California Consumer Privacy Act (CCPA) prevede obblighi e diritti in materia di privacy per i consumatori della California, inclusi diritti simili a quelli che il GDPR riconosce all'interessato, ad esempio il diritto di eliminare, ricevere e accedere alle informazioni personali (portabilità).  Nell'ambito dei diritti che i consumatori possono esercitare, il CCPA prevede inoltre l'obbligo per determinate divulgazioni, di protezioni contro la discriminazione e requisiti di consenso o rifiuto esplicito per alcuni trasferimenti di dati classificati come "vendite". In generale, la definizione di vendite include la condivisione di dati a titolo oneroso. Per altre informazioni sul CCPA, vedere il [California Consumer Privacy Act](offering-ccpa.md) e le [Domande frequenti sul California Consumer Privacy Act](ccpa-faq.yml).

La guida descrive come utilizzare i prodotti, i servizi e gli strumenti di amministrazione Microsoft per aiutare i clienti titolari del trattamento dei dati a individuare e gestire i dati personali per rispondere alle richieste degli interessati. In particolare, questa guida informazioni su come identificare, accedere e gestire i dati o le informazioni personali che si trovano nel cloud Microsoft. Di seguito è riportata una rapida panoramica delle procedure descritte in questa guida:

- **Scoprire**: utilizzo degli strumenti di ricerca e individuazione per trovare più facilmente i dati dei clienti che potrebbero essere oggetto di una richiesta DSR. Dopo aver raccolto dei documenti potenzialmente reattivi, è possibile eseguire una o più delle azioni DSR descritte nella seguente procedura per rispondere alla richiesta. In alternativa, si potrebbe determinare che la richiesta non soddisfa le linee guida dell'organizzazione relative alla risposta alle richieste DSR.
- **Accesso:** recuperare i dati personali che risiedono nel cloud Microsoft e, se richiesto, crearne una copia che può essere disponibile per l'interessato.
- **Rettificare:** apportare modifiche o implementare le azioni richieste sui dati personali, ove applicabile.
- **Limitare**: limitare il trattamento dei dati personali, tramite la rimozione delle licenze per vari servizi di Azure o disattivando i servizi desiderati ove possibile. È anche possibile rimuovere i dati dal cloud Microsoft e mantenerli in locale o in un altro posto.
- **Eliminare:** rimuovere in modo definitivo i dati personali che risiedono nel cloud Microsoft.
- **Esportazione/ricezione (portabilità):** fornire all'interessato una copia elettronica dei dati o delle informazioni personali in un formato leggibile da una macchina. Secondo il CCPA, le informazioni personali sono qualsiasi informazione riguardante una persona fisica identificata o identificabile. Non esiste distinzione tra i ruoli privati, pubblici o professionali di una persona. Il termine definito "informazioni personali" combacia con il termine "dati personali" del GDPR. Tuttavia, il CCPA include anche i dati relativi alla famiglia e al nucleo familiare. Per altre informazioni sul CCPA, vedere il [California Consumer Privacy Act](offering-ccpa.md) e le [Domande frequenti sul California Consumer Privacy Act](ccpa-faq.yml).

Ogni sezione di questa guida illustra le procedure tecniche che un'organizzazione titolare del trattamento dei dati può adottare per rispondere a una richiesta DSR per i dati personali nel cloud Microsoft.

#### <a name="terminology"></a>Terminologia

Di seguito vengono fornite le definizioni dei termini importanti nella presente guida.

- **Titolare:** la persona fisica o giuridica, l'autorità pubblica, l'agenzia o altro ente che, autonomamente o unitamente ad altri soggetti, determina gli obiettivi e i mezzi del trattamento dei dati personali; laddove gli obiettivi e i mezzi di tale trattamento sono determinati da una normativa europea o di uno specifico Stato membro dell'UE, il titolare del trattamento dei dati o i criteri specifici per la sua designazione potrebbero essere forniti da tale normativa europea o di uno specifico Stato membro dell'UE.
- **Dati personali e interessato:** tutte le informazioni concernenti una persona fisica identificata o identificabile ("interessato"). Una persona fisica è identificabile se può essere identificata, direttamente o indirettamente, in particolare facendo riferimento a un identificatore (ad esempio un nome, un numero di identificazione, dati di posizione o un identificatore online) o a uno o più fattori relativi all'identità fisica, fisiologica, genetica, mentale, economica, culturale o sociale di tale persona fisica.
- **Responsabile:** una persona fisica o giuridica, un'autorità pubblica o altro ente che si occupa del trattamento dei dati personali per conto del titolare.
- **Dati dei clienti**: tutti i dati, compresi tutti i file di testo, audio o immagini e il software, che vengono forniti a Microsoft da, o per conto di, un cliente tramite l'uso del servizio aziendale. I dati dei clienti includono (1) informazioni che consentono l'identificazione personale degli utenti finali (ad esempio, nomi utente e informazioni di contatto in Azure Active Directory) e contenuti per i clienti che un cliente stesso carica o crea in servizi specifici (ad esempio, contenuti per i clienti in un account di archiviazione di Azure, contenuti per i clienti in un database SQL di Azure o un'immagine della macchina virtuale di un cliente in Macchine virtuali di Azure).
- **Log generati dal sistema:** log e dati relativi generati da Microsoft che consentono a Microsoft di fornire servizi aziendali agli utenti. I log generati dal sistema contengono dati principalmente presentati con l'uso di pseudonimi come identificatori univoci (in genere, un numero generato dal sistema con cui non è possibile identificare direttamente un soggetto, ma che viene utilizzato per fornire i servizi aziendali agli utenti). I log generati dal sistema possono anche contenere informazioni personali sugli utenti finali, come un nome utente.

#### <a name="how-to-use-this-guide"></a>Come usare questa guida

Questa guida è costituita da due parti:

- **Parte 1: rispondere alle richieste dei soggetti dei dati per i dati dei clienti** — Nella Parte 1 di questa guida viene illustrato come accedere, rettificare, eliminare ed esportare i dati dalle applicazioni in cui sono presenti dati creati dall'utente. In questa sezione viene descritto in modo dettagliato come gestire le richieste DSR rispetto ai contenuti per i clienti e alle informazioni personali degli utenti finali.
- **Parte 2: rispondere alle richieste dei soggetti dei dati per i log generati dal sistema** — Quando si utilizzano i servizi aziendali, Microsoft genera alcune informazioni, note come log generati dal sistema, per fornire il servizio. Nella Parte 2 di questa guida viene illustrato come accedere, eliminare ed esportare tali informazioni per Azure.

### <a name="understanding-dsrs-for-azure-active-directory-and-microsoft-intune"></a>Informazioni sulle richieste DSR per Azure Active Directory e Microsoft Intune

Quando si considerano i servizi forniti ai clienti aziendali, l'esecuzione delle richieste dell'interessato si intende sempre nel contesto di uno specifico tenant di Azure Active Directory (AAD). In particolare, le richieste DSR vengono sempre eseguite all'interno di un determinato tenant di AAD. Se un utente fa parte di più tenant, è importante sottolineare che una determinata richiesta DSR viene eseguita *solo* nel contesto del tenant specifico nel quale è stata ricevuta. Questo è un aspetto fondamentale da comprendere perché significa che l'esecuzione di una richiesta DSR da parte di un cliente aziendale **non** avrà effetto sui dati di un cliente aziendale adiacente.

Lo stesso vale anche per Microsoft Intune fornito a un cliente aziendale: l'esecuzione di una richiesta DSR rispetto a un account Intune *associato a un tenant di Azure Active Directory* sarà relativa **solo** ai dati all'interno del tenant. Inoltre, quando si gestiscono account Intune all'interno di un tenant, è importante comprendere quanto descritto di seguito:

- Se un utente di Intune crea una sottoscrizione di Azure, la sottoscrizione verrà gestita come se fosse un tenant di Azure Active Directory. Di conseguenza, le richieste dell'interessato sono limitate all'ambito del tenant come descritto in precedenza.
- Se si elimina una sottoscrizione di Azure creata con un account Intune, **non ci saranno effetti** sull'account Intune. Come detto in precedenza, l'esecuzione di richieste DSR nell'ambito della sottoscrizione di Azure è limitata all'ambito del tenant stesso.

Le richieste DSR rispetto a un account Intune, **al di fuori di un determinato tenant**, vengono eseguite tramite la Dashboard di privacy dell'utente. Per ulteriori informazioni, fare riferimento alla guida per le richieste degli interessati di Windows.

## <a name="part-1-dsr-guide-for-customer-data"></a>Parte 1: guida sulle richieste DSR per i dati dei clienti

### <a name="executing-dsrs-against-customer-data"></a>Esecuzione delle richieste DSR rispetto ai dati dei clienti

Microsoft consente di accedere, eliminare ed esportare alcuni dati dei clienti tramite il portale di Azure e anche direttamente tramite le API (Application Programming Interface) o le interfacce utente preesistenti per servizi specifici, dette anche *esperienze nel prodotto*. Informazioni dettagliate su tali esperienze nel prodotto sono disponibili nella documentazione di riferimento dei servizi corrispondenti.

>[!IMPORTANT]  
>I servizi che supportano le richieste dell'interessato all'interno dei prodotti richiedono l'uso diretto dell'API (Application Programming Interface) o dell'interfaccia utente del servizio, con la descrizione delle operazioni di creazione, lettura, aggiornamento ed eliminazione applicabili. Pertanto, l'esecuzione di richieste dell'interessato all'interno di un determinato servizio deve essere accompagnata dall'esecuzione di una richiesta dell'interessato nel portale Azure per completare una richiesta completa di un determinato interessato. Per ulteriori dettagli, consultare la documentazione di riferimento per i relativi servizi.

### <a name="step-1-discover"></a>Passaggio 1: scoprire

Il primo passo nella risposa a una richiesta DSR consiste nell'individuare i dati personali oggetto della richiesta. Questa fase (individuazione e analisi dei dati personali in questione) consente di determinare se una richiesta DSR soddisfa i requisiti dell'organizzazione per accettare o rifiutare una DSR. Ad esempio, dopo aver individuato e analizzato i dati personali in questione, si potrebbe stabilire che la richiesta non soddisfa i requisiti dell'organizzazione perché potrebbe ledere i diritti e le libertà altrui.

Dopo aver trovato i dati, è quindi possibile eseguire un'azione specifica per soddisfare la richiesta dell'interessato. Per ulteriori dettagli, vedere le risorse seguenti:

- [Raccolta dati](/intune/privacy-data-collect)
- [Trattamento e archiviazione dei dati](/intune/privacy-data-store-process)
- [Visualizzazione dei dati personali](/intune/privacy-data-view-correct#view-personal-data)

### <a name="step-2-access"></a>Passaggio 2: accedere

Dopo aver individuato i dati dei clienti che contengono dati personali potenzialmente reattivi a una richiesta DSR, l'utente e l'organizzazione devono decidere quali dati fornire all'interessato. Si può fornire una copia del documento effettivo, una versione opportunamente oscurata o una cattura da schermo delle parti che si ritiene appropriato condividere. Per ognuna di queste risposte a una richiesta di accesso, sarà necessario recuperare una copia del documento o altri elementi che contengono i dati sensibili.

Quando si invia una copia all'interessato, potrebbe essere necessario rimuovere o redigere informazioni personali su altri interessati ed eventuali informazioni riservate.

Di seguito viene descritto come ottenere una copia dei dati in risposta a una richiesta di accesso DSR.

#### <a name="azure-active-directory"></a>Azure Active Directory

Microsoft mette a disposizione un portale ed esperienze nel prodotto per offrire all'amministratore tenant del cliente aziendale la possibilità di gestire richieste di accesso dell'interessatp. Tali richieste consentono di accedere ai dati personali dell'utente, tra cui: (a) informazioni personali su un utente finale e (b) log generati dal sistema.

#### <a name="service-specific-interfaces"></a>Interfacce specifiche dei servizi

Microsoft Intune consente di [Individuare i dati dei clienti](#step-1-discover) direttamente tramite le interfacce utente (UI) o le interfacce di programmazione dell'applicazione preesistenti (API).

### <a name="step-3-rectify"></a>Passaggio 3: rettificare

Se un interessato ha chiesto di rettificare i dati personali che fanno parte dei dati dell'organizzazione, l’utente e l’organizzazione dovranno determinare se la richiesta possa essere accettata. La rettifica dei dati potrebbe includere operazioni quali la modifica, la revisione o la rimozione di dati personali da un documento o un altro elemento.

In quanto responsabile del trattamento dei dati, Microsoft non offre la possibilità di correggere i log generati dal sistema, in quanto rappresentano attività concrete e costituiscono una cronologia degli eventi avvenuti all'interno dei servizi Microsoft. Per quanto riguarda Intune, gli amministratori non possono aggiornare le informazioni specifiche relative ai dispositivi o alle app. Se un utente finale desidera correggere dei dati personali (come il nome del dispositivo) dovrà farlo direttamente dal dispositivo interessato. Tali modifiche verranno sincronizzate al prossimo accesso a Intune.

### <a name="step-4-restrict"></a>Passaggio 4: limitare

Gli interessati potrebbero richiedere la limitazione del trattamento dei loro dati personali. Microsoft fornisce il portale di Azure e le interfacce di programmazione dell'applicazione (API) o le interfacce utente (UI) pre-esistenti. Tali esperienze consentono all'amministratore tenant del cliente aziendale di gestire le richieste dell'interessato con una combinazione di esportazione ed eliminazione dei dati. Per ulteriori dettagli, vedere [Trattamento dei dati personali](/intune/privacy-data-store-process#processing-personal-data).

### <a name="step-5-delete"></a>Passaggio 5: eliminare

Il "diritto di eliminazione" tramite la rimozione dei dati personali dai dati dei clienti di un'organizzazione è una protezione chiave del GDPR. La rimozione dei dati personali include la cancellazione di tutti i dati personali e dei log generati dal sistema, ad eccezione delle informazioni del log di controllo. Per informazioni dettagliate, vedere [Eliminare i dati personali degli utenti finali](/intune/privacy-data-audit-export-delete#delete-end-user-personal-data).

## <a name="part-2-system-generated-logs"></a>Parte 2: log generati dal sistema

I log di controllo forniscono agli amministratori tenant un record di attività che genera una modifica in Microsoft Intune. I log di controllo sono disponibili per molte attività di gestione e generalmente consentono di creare, aggiornare (modificare), eliminare e assegnare azioni. È possibile esaminare anche le attività remote che generano eventi di controllo. Questi log di controllo possono contenere dati personali degli utenti i cui dispositivi sono registrati in Intune. Gli amministratori non possono eliminare i log di controllo. Per informazioni dettagliate, vedere [Controllare i dati personali](/intune/privacy-data-audit-export-delete#audit-personal-data).

## <a name="notify-about-exporting-or-deleting-issues"></a>Notificare problemi riguardanti l'esportazione o l'eliminazione.

Se si verificano problemi durante l'esportazione o l'eliminazione di dati dal portale di Azure, accedere al pannello **Guida e Supporto** del portale di Azure e inviare un nuovo ticket in **Gestione dell'abbonamento > Privacy e richieste di conformità per gli abbonamenti > Pannello privacy e richieste GDPR**.

## <a name="learn-more"></a>Altre informazioni

- [Centro protezione Microsoft](https://www.microsoft.com/trust-center/privacy/gdpr-overview)
