---
title: Richieste degli interessati della configurazione del responsabile del trattamento dei dati di diagnostica Windows relative al GDPR e al CCPA
description: Informazioni su come usare i prodotti, i servizi e gli strumenti di amministrazione Microsoft per trovare i dati personali e agire su di essi in risposta alle richieste degli interessati.
keywords: Microsoft 365, Microsoft 365 Education, Documentazione Microsoft 365, GDPR
ms.localizationpriority: high
ROBOTS: NOINDEX, NOFOLLOW
ms.prod: microsoft-365-enterprise
ms.topic: article
f1.keywords:
- NOCSH
ms.author: robmazz
author: robmaz
manager: laurawi
ms.reviewer: delinat
audience: itpro
ms.collection:
- GDPR
- M365-security-compliance
- MS-Compliance
hideEdit: true
ms.openlocfilehash: 202b8aa75d3dd6fc94025a1a30f922563fc73e7b
ms.sourcegitcommit: 4c00fd65d418065d7f53216c91f455ccb3891c77
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/23/2021
ms.locfileid: "58482379"
---
# <a name="windows-diagnostic-data-processor-configuration-data-subject-requests-for-the-gdpr-and-ccpa"></a>Richieste degli interessati della configurazione del responsabile del trattamento dei dati di diagnostica Windows relative al GDPR e al CCPA

>[!NOTE]
>Questo argomento si applica alle edizioni di Windows 10 Enterprise, Pro ed Education, versione 1809 con aggiornamento di luglio 2021 e versioni successive.

## <a name="introduction-to-data-subject-requests-dsrs"></a>Introduzione alle richieste degli interessati (DSR)

Il Regolamento generale europeo sulla protezione dei dati (GDPR) attribuisce alle persone (definite nel regolamento _soggetti interessati_) il diritto di gestire i dati personali raccolti da un datore di lavoro o da un altro tipo di ente o organizzazione (definito _titolare del trattamento dei dati_ o semplicemente _titolare del trattamento_). Nel GDPR, i dati personali sono definiti molto ampiamente come qualsiasi dato relativo a una persona fisica identificata o identificabile. In base al regolamento GDPR, ai soggetti dei dati vengono assegnati diritti specifici relativamente ai dati personali, tra i quali il diritto di ottenerne copie, richiedere correzioni, limitarne l'elaborazione, eliminarli o riceverli in formato elettronico in modo che possano essere trasferiti a un altro titolare. Una richiesta formale da un soggetto interessato a un titolare del trattamento di agire sui dati personali viene definita una _Richiesta dell’interessato_ o DSR.

Analogamente, il California Consumer Privacy Act (CCPA) prevede obblighi e diritti in materia di privacy per i consumatori della California, inclusi diritti simili a quelli che il GDPR riconosce all'interessato, ad esempio il diritto di eliminare, ricevere e accedere alle informazioni personali (portabilità). Nell'ambito dei diritti che i consumatori possono esercitare, il CCPA prevede inoltre l'obbligo per determinate divulgazioni, di protezioni contro la discriminazione e requisiti di “consenso o rifiuto esplicito” per alcuni trasferimenti di dati classificati come “vendite”. In generale, la definizione di vendite include la condivisione di dati a titolo oneroso. Per altre informazioni sul CCPA, vedere il [California Consumer Privacy Act](/microsoft-365/compliance/offering-ccpa) e le [Domande frequenti sul California Consumer Privacy Act](/microsoft-365/compliance/ccpa-faq).

La guida descrive come utilizzare i prodotti, i servizi e gli strumenti di amministrazione Microsoft per aiutare i nostri clienti titolari del trattamento dei dati a individuare e gestire i dati personali per rispondere alle richieste degli interessati. In particolare, sono incluse informazioni su come identificare, accedere e gestire i dati personali nei dati di diagnostica Windows raccolti da Microsoft quando la configurazione del responsabile del trattamento dei dati Windows è abilitata. Di seguito è riportata una rapida panoramica delle procedure descritte in questa guida:

1. **Accesso:** recuperare i dati di diagnostica Windows associati all’interessato e, se richiesto, crearne una copia che può essere disponibile per l'interessato.
2. **Eliminazione:** rimuovere definitivamente dati di diagnostica Windows associati a un interessato.
3. **Esportazione:** fornire una copia elettronica (in un formato leggibile) dei dati di diagnostica Windows all’interessato.

Secondo il CCPA, le informazioni personali sono qualsiasi informazione riguardante una persona fisica identificata o identificabile. Non esiste distinzione tra i ruoli privati, pubblici o professionali di una persona. Il termine definito "informazioni personali" combacia con il termine "dati personali" del GDPR. Tuttavia, il CCPA include anche i dati relativi alla famiglia e al nucleo familiare. Per altre informazioni sul CCPA, vedere il [California Consumer Privacy Act](/microsoft-365/compliance/offering-ccpa) e le [Domande frequenti sul California Consumer Privacy Act](/microsoft-365/compliance/ccpa-faq).

Ogni sezione di questa guida illustra le procedure tecniche che un'organizzazione titolare del trattamento dei dati può adottare per rispondere a una richiesta dell'interessato relativa ai dati di diagnostica Windows raccolti da Microsoft quando la configurazione del responsabile del trattamento dei dati di diagnostica Windows è abilitata.

## <a name="terminology"></a>Terminologia

Di seguito vengono fornite le definizioni dei termini importanti nella presente guida.

* _Titolare:_ la persona fisica o giuridica, l'autorità pubblica, l'agenzia o altro ente che, autonomamente o unitamente ad altri soggetti, determina gli obiettivi e i mezzi del trattamento dei dati personali; laddove gli obiettivi e i mezzi di tale trattamento sono determinati da una normativa europea o di uno specifico Stato membro dell'UE, il titolare del trattamento dei dati o i criteri specifici per la sua designazione potrebbero essere forniti da tale normativa europea o di uno specifico Stato membro dell'UE.

* _Dati personali e interessato:_ qualsiasi informazione riguardante una persona fisica identificata o identificabile ("interessato"); si considera identificabile la persona fisica che può essere identificata, direttamente o indirettamente, con particolare riferimento a un identificativo come il nome, un numero di identificazione, dati relativi all'ubicazione, un identificativo online o a uno o più elementi caratteristici della sua identità fisica, fisiologica, genetica, psichica, economica, culturale o sociale.

* _Responsabile del trattamento:_ una persona fisica o giuridica, un'autorità pubblica, un servizio o altro organismo che tratta dati personali per conto del titolare del trattamento.

* _Dati del cliente:_ tutti i dati compresi file di testo, audio, video o immagini e software, forniti a Microsoft per conto o dal cliente, attraverso i servizi aziendali. 

* _Dati di diagnostica Windows:_ questi sono composti da dati tecnici inviati da dispositivi Windows e relativi al dispositivo e alle prestazioni di Windows e del software correlato. Vengono utilizzati per mantenere Windows aggiornato, sicuro, affidabile, efficiente e per apportare miglioramenti ai prodotti. Alcuni esempi di dati di diagnostica Windows sono il tipo di hardware usato, le applicazioni installate con le rispettive condizioni di uso e le informazioni sull'affidabilità nei driver dei dispositivi. Alcuni componenti e app di Windows si connettono direttamente ai servizi Microsoft, tuttavia i dati scambiati non sono dati di diagnostica Windows. Ad esempio, lo scambio di informazioni relative alla posizione dell’utente per il meteo o le notizie locali non è un esempio di dati di diagnostica Windows.

## <a name="how-to-use-this-guide"></a>Come usare questa guida

Chi abilita la configurazione del responsabile del trattamento dei dati di diagnostica Windows assume il ruolo di titolare del trattamento dei dati di diagnostica Windows raccolti dai dispositivi. Per altre informazioni sulla configurazione, vedere [Configurare i dati di diagnostica Windows nell'organizzazione](/windows/privacy/configure-windows-diagnostic-data-in-your-organization).

## <a name="windows-diagnostic-data"></a>Dati di diagnostica Windows

Microsoft consente di accedere, eliminare ed esportare i dati di diagnostica Windows associati all'uso da parte dell’utente dei dispositivi abilitati alla configurazione del responsabile del trattamento dei dati di diagnostica Windows.

> [!IMPORTANT]
> Alcuni dati di diagnostica Windows sono associati solo a un identificatore di dispositivo e non a un utente specifico. Questo tipo di dati a livello di dispositivo non viene esportato e viene eliminato dai sistemi entro 30 giorni.<br><br>
> La possibilità di rettificare i dati di diagnostica Windows non è supportata. I dati di diagnostica Windows costituiscono le azioni effettive eseguite all’interno di Windows e le modifiche a tali dati potrebbero compromettere il record cronologico delle azioni, aumentare i rischi per la sicurezza e compromettere l’affidabilità.

La sezione successiva illustra le procedure per eseguire una richiesta dell'interessato relativa ai dati di diagnostica Windows associati a un ID utente di Azure Active Directory (AAD). Per altre informazioni, vedere [Windows 10 e conformità in materia di privacy: guida per professionisti IT e della conformità](/windows/privacy/windows-10-and-privacy-compliance).

## <a name="executing-dsrs-against-windows-diagnostic-data"></a>Esecuzione delle richieste degli interessati rispetto ai dati di diagnostica Windows

Microsoft consente di accedere, eliminare ed esportare alcuni dati di diagnostica Windows tramite il portale di Azure e direttamente tramite le API preesistenti.

### <a name="step-1-access"></a>Passaggio 1: accesso

Microsoft offre all’amministratore tenant all’interno dell'organizzazione un metodo per accedere ai dati di diagnostica Windows associati all'uso da parte di un utente specifico di un dispositivo abilitato alla configurazione del responsabile del trattamento dei dati di diagnostica Windows. I dati recuperati per una richiesta di accesso saranno resi disponibili, tramite esportazione, in un formato leggibile al computer e verranno forniti in file che consentiranno all'utente di comprendere a quali servizi e dispositivi sono associati i dati. Come indicato in precedenza, i dati recuperati non includeranno dati che potrebbero compromettere la sicurezza o la stabilità del dispositivo Windows.

Il portale di Azure consente all'amministratore del tenant del cliente aziendale di gestire le richieste di accesso dell'interessato. [Richiesta dell'interessato per Azure, parte 2, passaggio 3: esportazione](/microsoft-365/compliance/gdpr-dsr-azure#step-3-export) descrive come eseguire una richiesta di accesso dell’interessato relativa ai dati di diagnostica Windows, tramite esportazione, attraverso il portale di Azure.

### <a name="step-2-delete"></a>Passaggio 2: eliminazione

Microsoft offre la possibilità di eseguire le richieste di eliminazione dell’interessato, sulla base di un oggetto Azure Active Directory per un particolare utente.

Per le richieste di eliminazione basate sull'utente, Microsoft offre due soluzioni.  Un’esperienza portale consente all'amministratore tenant del cliente aziendale di gestire le richieste di eliminazione dell'interessato. [Richiesta dell'interessato per Azure, parte 1, passaggio 5: eliminazione](/microsoft-365/compliance/gdpr-dsr-azure#step-5-delete) descrive come eseguire una richiesta di eliminazione dell’interessato relativa ai dati di diagnostica Windows, tramite l’eliminazione di un utente associato ai dati, attraverso il portale di Azure.

Microsoft consente inoltre di eliminare gli utenti, che a loro volta elimineranno i dati di diagnostica Windows, direttamente tramite l’API preesistente. Informazioni dettagliate sono disponibili nella [ documentazione di riferimento dell’API](/graph/api/directory-deleteditems-delete).

>[!IMPORTANT]
>L'eliminazione dei dati raccolti non interrompe la raccolta ulteriore di dati dal dispositivo. Per disattivare la raccolta dei dati, seguire la procedura descritta nella [documentazione di riferimento del relativo servizio](/windows/privacy/configure-windows-diagnostic-data-in-your-organization#enterprise-management).

### <a name="step-3-export"></a>Passaggio 3: esportazione

L'amministratore tenant è l'unica persona all’interno dell'organizzazione che può accedere ai dati di diagnostica Windows associati all'uso da parte di un utente specifico di un dispositivo abilitato con configurazione del responsabile del trattamento dei dati di diagnostica Windows. I dati recuperati per una richiesta di esportazione saranno disponibili in un formato leggibile dal computer e verranno forniti nei file che consentiranno all'utente di comprendere a quali servizi e dispositivi sono associati i dati. Come indicato in precedenza, i dati recuperati non includeranno dati che potrebbero compromettere la sicurezza o la stabilità del dispositivo Windows. [Richiesta dell'interessato per Azure, parte 2, passaggio 3: esportazione](/microsoft-365/compliance/gdpr-dsr-azure#step-3-export) descrive come eseguire una richiesta di esportazione dell’interessato relativa ai dati di diagnostica Windows attraverso il portale di Azure.

Microsoft consente di esportare i dati di diagnostica Windows direttamente tramite l’API preesistente. Informazioni dettagliate sono disponibili nella [ documentazione di riferimento dell’API](/graph/api/user-exportpersonaldata).

## <a name="notify-us-about-exporting-or-deleting-issues"></a>Notificare problemi riguardanti l'esportazione o l'eliminazione

Se si verificano problemi durante l'esportazione o l'eliminazione di dati di diagnostica Windows dal portale di Azure, accedere al pannello **Guida e Supporto** del portale di Azure e inviare un nuovo ticket in **Gestione dell'abbonamento > Privacy e richieste di conformità per gli abbonamenti > Pannello privacy e richieste GDPR**.

>[!NOTE]
>Il completamento di una richiesta di esportazione dei dati di diagnostica Windows può richiedere fino a 5 giorni. Se si verificano problemi, attendere almeno 7 giorni prima di aprire un ticket di supporto.
