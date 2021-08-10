---
title: GDPR
description: Suggerimenti tecnici Microsoft — SET DI STRUMENTI DI MIGRAZIONE DI FASTTRACK PER INVIARE LE RICHIESTE DI ELIMINAZIONE
keywords: Migrazione di FastTrack, Microsoft 365 Education, Documentazione Microsoft 365, GDPR
localization_priority: Priority
Robots: NOFOLLOW,NOINDEX
ms.prod: microsoft-365-enterprise
ms.topic: article
f1.keywords:
- NOCSH
ms.author: mohitku
author: MohitKumar
manager: laurawi
audience: itpro
ms.collection:
- GDPR
- M365-security-compliance
- MS-Compliance
titleSuffix: Microsoft GDPR
hideEdit: true
ms.openlocfilehash: a83a39ec6f60dae780d1082f534c094c45ac4d2c6788c851c6c1cf35b1a7d256
ms.sourcegitcommit: af1925730de60c3b698edc4e1355c38972bdd759
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/05/2021
ms.locfileid: "54293091"
---
# <a name="fasttrack-migration-toolset-for-submitting-delete-request"></a>Set di strumenti di migrazione di FastTrack per inviare una richiesta di eliminazione

## <a name="toolset-purpose"></a>Scopo del set di strumenti

Se si è un cliente attualmente coinvolto in una migrazione di FastTrack, eliminando l'account utente non sarà eliminata la copia dei dati utilizzata dal team di Microsoft FastTrack, che viene conservata con il solo scopo di completare la migrazione. Se durante la migrazione si desidera che il team di Microsoft FastTrack elimini anche la copia dei dati, è possibile inviare una richiesta tramite questo set di strumenti. In condizioni normali di attività, Microsoft FastTrack eliminerà tutte le copie dei dati una volta completata la migrazione.

### <a name="supported-platforms"></a>Piattaforme supportate

Microsoft supporta la versione iniziale di questo set di strumenti nella piattaforma Windows e nella console di PowerShell. Il set di strumenti supporta le seguenti piattaforme:

***Tabella 1 — Piattaforme supportate da questo set di strumenti***

****

|Versione di PowerShell|Windows 7|Windows 8|Windows 10|Windows Server 2012|Windows Server 2016|
|:---:|:---:|:---:|:---:|:---:|:---:|
|5.0|Non supportato|Supportato|Supportato|Supportato|Supportato|
|5.1|Non supportato|Supportato|Supportato|Supportato|Supportato|
|

### <a name="obtaining-the-toolset"></a>Ottenere il set di strumenti

Il set di strumenti è disponibile in PowerShell Gallery nell'applicazione console di PowerShell. Per individuare e caricare questo modulo cmdlet, aprire PowerShell in modalità di amministratore in modo da avere le autorizzazioni adeguate per installare il modulo. Se PowerShell non è mai stato utilizzato in precedenza, passare alla barra delle applicazioni di Windows e digitare nella casella di ricerca "PowerShell". Selezionare l'applicazione console facendo clic con il pulsante destro del mouse e scegliere l'opzione **Esegui come amministratore**, quindi fare clic su **Sì** per eseguire Windows PowerShell.

![PowerShell — Esegui come amministratore](../media/fasttrack-powershell_image.png)

![PowerShell — Consenti all'app di apportare modifiche](../media/fasttrack-run-powershell_image.png)

Una volta aperta la console, è necessario impostare le autorizzazioni per l'esecuzione dello script. Digitare il comando seguente per consentire l'esecuzione di script:

```powershell
Set-ExecutionPolicy -ExecutionPolicy Bypass -Scope Process
```

Verrà richiesto di confermare l'azione, poiché l'amministratore può modificare l'ambito a propria discrezione.

***Impostare criteri di esecuzione***

![Impostare la modifica dei criteri di esecuzione in PowerShell](../media/powershell-set-execution-policy_image.png)

Dopo che la console è impostata per consentire lo script, eseguire il seguente comando per installare il modulo:

```powershell
Install-Module -Name Microsoft.FastTrack -Repository PSGallery -WarningAction SilentlyContinue -Force
```

### <a name="prerequisites-for-module"></a>Prerequisiti per il modulo

Per eseguire correttamente il modulo, è necessario installare moduli dipendenti da utilizzare, nel caso in cui non siano già installati. Potrebbe essere necessario riavviare PowerShell.

Per poter inviare un richiesta dell'interessato, è necessario accedere prima con le credenziali di Office 365. Immettendo le credenziali appropriate viene convalidato lo stato di amministratore globale e vengono raccolte le informazioni del tenant.

```powershell
Login-FastTrackAccount -ApiKey <API Key provided by FastTrack MVM>
```

Una volta eseguito l'accesso, le credenziali e la chiave saranno conservate per l'utilizzo con i moduli FastTrack per il resto della sessione corrente di PowerShell.

Se è necessario connettersi a un ambiente cloud diverso da quello commerciale, sarà necessario aggiungere *-Environment* al comando *Login* con uno dei seguenti ambienti validi:

- AzureCloud
- AzureChinaCloud
- AzureGermanCloud
- AzureUSGovernmentCloud

```powershell
Login-FastTrackAccount -ApiKey <API Key provided by FastTrack MVM> -Environment <cloud environment>
```

Per inviare una richiesta di DSR, eseguire il comando seguente:

```powershell
Submit-FastTrackGdprDsrRequest -DsrRequestUserEmail SubjectUserEmail@mycompany.com
```

Al termine dell'operazione, il cmdlet restituirà un oggetto ID transazione, che è consigliabile conservare.

#### <a name="checking-the-status-of-a-request-transaction"></a>Verificare lo stato di una richiesta transazione

Eseguire la seguente funzione con l'ID della transazione ottenuto in precedenza:

```powershell
Get-FastTrackGdprDsrRequest -TransactionID "YourTransactionID"
```

#### <a name="transaction-status-codes"></a>Codici di stato transazione

|Transazione|Stato|
|---|---|
|**Creato**|La richiesta è stata creata.|
|**Operazione non riuscita**|Non è stato possibile creare la richiesta; inviarla nuovamente o contattare l'assistenza.|
|**Operazione completata**|La richiesta è stata completata e purificata.|
|

<!-- original version: **Created**  Request has been created<br/>**Failed** Request failed to create, please resubmit, or contact support<br/>**Completed** Request has been completed and sanitized -->

## <a name="learn-more"></a>Altre informazioni

[Centro protezione Microsoft](https://www.microsoft.com/trust-center/privacy/gdpr-overview)
