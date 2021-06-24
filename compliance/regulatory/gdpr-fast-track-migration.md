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
ms.openlocfilehash: d3429d3fb35317146e32fddc71bae2f12c40269d
ms.sourcegitcommit: fb379d1110a9a86c7f9bab8c484dc3f4b3dfd6f0
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/23/2021
ms.locfileid: "53089509"
---
# <a name="fasttrack-migration-toolset-for-submitting-delete-request"></a><span data-ttu-id="f3ad7-104">Set di strumenti di migrazione di FastTrack per inviare una richiesta di eliminazione</span><span class="sxs-lookup"><span data-stu-id="f3ad7-104">FastTrack Migration Toolset for Submitting Delete Request</span></span>

## <a name="toolset-purpose"></a><span data-ttu-id="f3ad7-105">Scopo del set di strumenti</span><span class="sxs-lookup"><span data-stu-id="f3ad7-105">Toolset purpose</span></span>

<span data-ttu-id="f3ad7-p101">Se si è un cliente attualmente coinvolto in una migrazione di FastTrack, eliminando l'account utente non sarà eliminata la copia dei dati utilizzata dal team di Microsoft FastTrack, che viene conservata con il solo scopo di completare la migrazione. Se durante la migrazione si desidera che il team di Microsoft FastTrack elimini anche la copia dei dati, è possibile inviare una richiesta tramite questo set di strumenti. In condizioni normali di attività, Microsoft FastTrack eliminerà tutte le copie dei dati una volta completata la migrazione.</span><span class="sxs-lookup"><span data-stu-id="f3ad7-p101">In the event that you are a customer currently engaged in FastTrack migrations, deleting the user account will not delete the data copy held by the Microsoft FastTrack team, which is held for the sole purpose of completing the migration. If during the migration you would like the Microsoft FastTrack team to also delete the data copy, submit a request via this tool set. In the ordinary course of business, Microsoft FastTrack will delete all data copies once the migration is complete.</span></span>

### <a name="supported-platforms"></a><span data-ttu-id="f3ad7-109">Piattaforme supportate</span><span class="sxs-lookup"><span data-stu-id="f3ad7-109">Supported platforms</span></span>

<span data-ttu-id="f3ad7-p102">Microsoft supporta la versione iniziale di questo set di strumenti nella piattaforma Windows e nella console di PowerShell. Il set di strumenti supporta le seguenti piattaforme:</span><span class="sxs-lookup"><span data-stu-id="f3ad7-p102">Microsoft supports the initial release of this  toolset in the Windows platform and PowerShell console. The following known platforms are supported by this toolset:</span></span>

<span data-ttu-id="f3ad7-112">\***Tabella 1 - Piattaforme supportate da questo set di strumenti** _</span><span class="sxs-lookup"><span data-stu-id="f3ad7-112">\***Table 1 — Platforms supported by this toolset** _</span></span>

<span data-ttu-id="f3ad7-113">_\*\*\*</span><span class="sxs-lookup"><span data-stu-id="f3ad7-113">_\*\*\*</span></span>

|<span data-ttu-id="f3ad7-114">Versione di PowerShell</span><span class="sxs-lookup"><span data-stu-id="f3ad7-114">PowerShell version</span></span>|<span data-ttu-id="f3ad7-115">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f3ad7-115">Windows 7</span></span>|<span data-ttu-id="f3ad7-116">Windows 8</span><span class="sxs-lookup"><span data-stu-id="f3ad7-116">Windows 8</span></span>|<span data-ttu-id="f3ad7-117">Windows 10</span><span class="sxs-lookup"><span data-stu-id="f3ad7-117">Windows 10</span></span>|<span data-ttu-id="f3ad7-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f3ad7-118">Windows Server 2012</span></span>|<span data-ttu-id="f3ad7-119">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="f3ad7-119">Windows Server 2016</span></span>|
|:---:|:---:|:---:|:---:|:---:|:---:|
|<span data-ttu-id="f3ad7-120">5.0</span><span class="sxs-lookup"><span data-stu-id="f3ad7-120">5.0</span></span>|<span data-ttu-id="f3ad7-121">Non supportato</span><span class="sxs-lookup"><span data-stu-id="f3ad7-121">Not Supported</span></span>|<span data-ttu-id="f3ad7-122">Supportato</span><span class="sxs-lookup"><span data-stu-id="f3ad7-122">Supported</span></span>|<span data-ttu-id="f3ad7-123">Supportato</span><span class="sxs-lookup"><span data-stu-id="f3ad7-123">Supported</span></span>|<span data-ttu-id="f3ad7-124">Supportato</span><span class="sxs-lookup"><span data-stu-id="f3ad7-124">Supported</span></span>|<span data-ttu-id="f3ad7-125">Supportato</span><span class="sxs-lookup"><span data-stu-id="f3ad7-125">Supported</span></span>|
|<span data-ttu-id="f3ad7-126">5.1</span><span class="sxs-lookup"><span data-stu-id="f3ad7-126">5.1</span></span>|<span data-ttu-id="f3ad7-127">Non supportato</span><span class="sxs-lookup"><span data-stu-id="f3ad7-127">Not Supported</span></span>|<span data-ttu-id="f3ad7-128">Supportato</span><span class="sxs-lookup"><span data-stu-id="f3ad7-128">Supported</span></span>|<span data-ttu-id="f3ad7-129">Supportato</span><span class="sxs-lookup"><span data-stu-id="f3ad7-129">Supported</span></span>|<span data-ttu-id="f3ad7-130">Supportato</span><span class="sxs-lookup"><span data-stu-id="f3ad7-130">Supported</span></span>|<span data-ttu-id="f3ad7-131">Supportato</span><span class="sxs-lookup"><span data-stu-id="f3ad7-131">Supported</span></span>|
|

### <a name="obtaining-the-toolset"></a><span data-ttu-id="f3ad7-132">Ottenere il set di strumenti</span><span class="sxs-lookup"><span data-stu-id="f3ad7-132">Obtaining the toolset</span></span>

<span data-ttu-id="f3ad7-p103">Il set di strumenti è disponibile in PowerShell Gallery nell'applicazione console di PowerShell. Per individuare e caricare questo modulo cmdlet, aprire PowerShell in modalità di amministratore in modo da avere le autorizzazioni adeguate per installare il modulo. Se PowerShell non è mai stato utilizzato in precedenza, passare alla barra delle applicazioni di Windows e digitare nella casella di ricerca "PowerShell". Selezionare l'applicazione console facendo clic con il pulsante destro del mouse e scegliere l'opzione **Esegui come amministratore**, quindi fare clic su **Sì** per eseguire Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f3ad7-p103">This toolset is available in the PowerShell Gallery on the PowerShell console application.  To locate and load this cmdlet module, first open PowerShell in administrator mode so it has the appropriate permissions to install the module. If you have not used PowerShell previously go to your Windows Task Bar and in the search box type 'PowerShell”. Select the console app using right-click and choose **Run as administrator**, then click **Yes** to run Windows PowerShell.</span></span>

![PowerShell — Esegui come amministratore](../media/fasttrack-powershell_image.png)

![PowerShell — Consenti all'app di apportare modifiche](../media/fasttrack-run-powershell_image.png)

<span data-ttu-id="f3ad7-p104">Una volta aperta la console, è necessario impostare le autorizzazioni per l'esecuzione dello script. Digitare il comando seguente per consentire l'esecuzione di script:</span><span class="sxs-lookup"><span data-stu-id="f3ad7-p104">Now that the console is open, you need to set permissions for script execution. Type the following command to allow the scripts to run:</span></span>

```powershell
Set-ExecutionPolicy -ExecutionPolicy Bypass -Scope Process
```

<span data-ttu-id="f3ad7-141">Verrà richiesto di confermare l'azione, poiché l'amministratore può modificare l'ambito a propria discrezione.</span><span class="sxs-lookup"><span data-stu-id="f3ad7-141">You will be prompted to confirm this action, as the administrator can change the scope at their discretion.</span></span>

<span data-ttu-id="f3ad7-142">\**_Impostare criteri di esecuzione_* _</span><span class="sxs-lookup"><span data-stu-id="f3ad7-142">\**_Set Execution Policy_* _</span></span>

![Impostare la modifica dei criteri di esecuzione in PowerShell](../media/powershell-set-execution-policy_image.png)

<span data-ttu-id="f3ad7-144">Dopo che la console è impostata per consentire lo script, eseguire il seguente comando per installare il modulo:</span><span class="sxs-lookup"><span data-stu-id="f3ad7-144">Now that the console is set to allow the script, run this next command to install the module:</span></span>

```powershell
Install-Module -Name Microsoft.FastTrack -Repository PSGallery -WarningAction SilentlyContinue -Force
```

### <a name="prerequisites-for-module"></a><span data-ttu-id="f3ad7-145">Prerequisiti per il modulo</span><span class="sxs-lookup"><span data-stu-id="f3ad7-145">Prerequisites for module</span></span>

<span data-ttu-id="f3ad7-p105">Per eseguire correttamente il modulo, è necessario installare moduli dipendenti da utilizzare, nel caso in cui non siano già installati. Potrebbe essere necessario riavviare PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f3ad7-p105">To successfully execute this module, you may need to install dependent modules for use if they are not already installed. You may need to restart PowerShell.</span></span>

<span data-ttu-id="f3ad7-p106">Per poter inviare un richiesta dell'interessato, è necessario accedere prima con le credenziali di Office 365. Immettendo le credenziali appropriate viene convalidato lo stato di amministratore globale e vengono raccolte le informazioni del tenant.</span><span class="sxs-lookup"><span data-stu-id="f3ad7-p106">In order to submit a DSR, you must first log in using your Office 365 credentials. Entering the proper credentials will validate your global administrator status and collect tenant information.</span></span>

```powershell
Login-FastTrackAccount -ApiKey <API Key provided by FastTrack MVM>
```

<span data-ttu-id="f3ad7-150">Una volta eseguito l'accesso, le credenziali e la chiave saranno conservate per l'utilizzo con i moduli FastTrack per il resto della sessione corrente di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f3ad7-150">Once successfully logged in, the credentials and key will be stored for use with FastTrack modules for the remainder of the current PowerShell session.</span></span>

<span data-ttu-id="f3ad7-151">Se è necessario connettersi a un ambiente cloud diverso da quello commerciale, sarà necessario aggiungere _-Environment\* al comando *Login* con uno dei seguenti ambienti validi:</span><span class="sxs-lookup"><span data-stu-id="f3ad7-151">If you need to connect to a cloud environment, other than commercial, _-Environment\* will need to be added to *Log in* command with one of the following valid environments:</span></span>

- <span data-ttu-id="f3ad7-152">AzureCloud</span><span class="sxs-lookup"><span data-stu-id="f3ad7-152">AzureCloud</span></span>
- <span data-ttu-id="f3ad7-153">AzureChinaCloud</span><span class="sxs-lookup"><span data-stu-id="f3ad7-153">AzureChinaCloud</span></span>
- <span data-ttu-id="f3ad7-154">AzureGermanCloud</span><span class="sxs-lookup"><span data-stu-id="f3ad7-154">AzureGermanCloud</span></span>
- <span data-ttu-id="f3ad7-155">AzureUSGovernmentCloud</span><span class="sxs-lookup"><span data-stu-id="f3ad7-155">AzureUSGovernmentCloud</span></span>

```powershell
Login-FastTrackAccount -ApiKey <API Key provided by FastTrack MVM> -Environment <cloud environment>
```

<span data-ttu-id="f3ad7-156">Per inviare una richiesta di DSR, eseguire il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="f3ad7-156">To submit a DSR request, run the following command:</span></span>

```powershell
Submit-FastTrackGdprDsrRequest -DsrRequestUserEmail SubjectUserEmail@mycompany.com
```

<span data-ttu-id="f3ad7-p107">Al termine dell'operazione, il cmdlet restituirà un oggetto ID transazione, che è consigliabile conservare.</span><span class="sxs-lookup"><span data-stu-id="f3ad7-p107">On success, the cmdlet will return a Transaction ID object. Please retain the Transaction ID.</span></span>

#### <a name="checking-the-status-of-a-request-transaction"></a><span data-ttu-id="f3ad7-159">Verificare lo stato di una richiesta transazione</span><span class="sxs-lookup"><span data-stu-id="f3ad7-159">Checking the status of a request transaction</span></span>

<span data-ttu-id="f3ad7-160">Eseguire la seguente funzione con l'ID della transazione ottenuto in precedenza:</span><span class="sxs-lookup"><span data-stu-id="f3ad7-160">Run the following function using the previously obtained Transaction ID:</span></span>

```powershell
Get-FastTrackGdprDsrRequest -TransactionID "YourTransactionID"
```

#### <a name="transaction-status-codes"></a><span data-ttu-id="f3ad7-161">Codici di stato transazione</span><span class="sxs-lookup"><span data-stu-id="f3ad7-161">Transaction Status Codes</span></span>

|<span data-ttu-id="f3ad7-162">Transazione</span><span class="sxs-lookup"><span data-stu-id="f3ad7-162">Transaction</span></span>|<span data-ttu-id="f3ad7-163">Stato</span><span class="sxs-lookup"><span data-stu-id="f3ad7-163">Status</span></span>|
|---|---|
|<span data-ttu-id="f3ad7-164">**Creato**</span><span class="sxs-lookup"><span data-stu-id="f3ad7-164">**Created**</span></span>|<span data-ttu-id="f3ad7-165">La richiesta è stata creata.</span><span class="sxs-lookup"><span data-stu-id="f3ad7-165">Request has been created.</span></span>|
|<span data-ttu-id="f3ad7-166">**Operazione non riuscita**</span><span class="sxs-lookup"><span data-stu-id="f3ad7-166">**Failed**</span></span>|<span data-ttu-id="f3ad7-167">Non è stato possibile creare la richiesta; inviarla nuovamente o contattare l'assistenza.</span><span class="sxs-lookup"><span data-stu-id="f3ad7-167">Request failed to create, please resubmit, or contact support.</span></span>|
|<span data-ttu-id="f3ad7-168">**Operazione completata**</span><span class="sxs-lookup"><span data-stu-id="f3ad7-168">**Completed**</span></span>|<span data-ttu-id="f3ad7-169">La richiesta è stata completata e purificata.</span><span class="sxs-lookup"><span data-stu-id="f3ad7-169">Request has been completed and sanitized.</span></span>|
|

<!-- original version: **Created**  Request has been created<br/>**Failed** Request failed to create, please resubmit, or contact support<br/>**Completed** Request has been completed and sanitized -->

## <a name="learn-more"></a><span data-ttu-id="f3ad7-170">Altre informazioni</span><span class="sxs-lookup"><span data-stu-id="f3ad7-170">Learn more</span></span>

[<span data-ttu-id="f3ad7-171">Centro protezione Microsoft</span><span class="sxs-lookup"><span data-stu-id="f3ad7-171">Microsoft Trust Center</span></span>](https://www.microsoft.com/trust-center/privacy/gdpr-overview)
