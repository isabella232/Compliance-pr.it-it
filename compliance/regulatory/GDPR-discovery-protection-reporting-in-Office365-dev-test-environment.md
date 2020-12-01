---
title: Individuazione, protezione e creazione di report secondo il GDPR nell'ambiente di sviluppo/test di Microsoft 365
description: Informazioni su come configurare e dimostrare la gestione delle informazioni personali per il GDPR in un ambiente di sviluppo/test di Microsoft 365.
f1.keywords:
- NOCSH
ms.author: bcarter
author: brendacarter
manager: laurawi
audience: ITPro
ms.topic: article
ms.collection:
- Ent_O365
- Strat_O365_Enterprise
- M365-security-compliance
- MS-Compliance
ms.service: O365-seccomp
localization_priority: Priority
search.appverid:
- MET150
ms.assetid: c2112ce8-1c4b-424f-b200-59e161db2d21
titleSuffix: Microsoft GDPR
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: 246c39c3bfd8f59cd2dab9c3a1b942d36942370f
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/30/2020
ms.locfileid: "49507738"
---
# <a name="gdpr-discovery-protection-and-reporting-in-the-devtest-environment"></a><span data-ttu-id="db47f-103">Individuazione, protezione e creazione di report secondo il GDPR nell'ambiente di sviluppo/test</span><span class="sxs-lookup"><span data-stu-id="db47f-103">GDPR discovery, protection, and reporting in the dev/test environment</span></span>

 <span data-ttu-id="db47f-104">**Riepilogo:** dimostrazione delle funzionalità correlate al GDPR in Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="db47f-104">**Summary:** Demonstrate GDPR capabilities in Microsoft 365.</span></span>

<span data-ttu-id="db47f-105">In questo articolo viene descritto come configurare e dimostrare l'individuazione, la protezione e la creazione di report per le informazioni personali secondo il Regolamento generale sulla protezione dei dati (GDPR) in un ambiente di sviluppo/test di Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="db47f-105">This article describes how you configure and demonstrate personally identifiable information (PII) discovery, protection, and reporting for the General Data Protection Regulation (GDPR) in a Microsoft 365 dev/test environment.</span></span>

## <a name="phase-1-create-and-configure-your-trial-microsoft-365-subscription"></a><span data-ttu-id="db47f-106">Fase 1: creare e configurare la sottoscrizione di valutazione di Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="db47f-106">Phase 1: Create and configure your trial Microsoft 365 subscription</span></span>

<span data-ttu-id="db47f-107">Per prima cosa, attenersi alla procedura descritta nell'articolo [Fase 2 dell'ambiente di sviluppo/test di Microsoft 365](https://docs.microsoft.com/Office365/Enterprise/office-365-dev-test-environment#phase-2-create-an-office-365-trial-subscription).</span><span class="sxs-lookup"><span data-stu-id="db47f-107">First, follow the steps in [Phase 2 of the Microsoft 365 dev/test environment](https://docs.microsoft.com/Office365/Enterprise/office-365-dev-test-environment#phase-2-create-an-office-365-trial-subscription) article.</span></span>

<span data-ttu-id="db47f-108">Successivamente, seguire questa procedura per configurare il responsabile di eDiscovery:</span><span class="sxs-lookup"><span data-stu-id="db47f-108">Next, use these steps to configure the eDiscovery manager:</span></span>

1. <span data-ttu-id="db47f-109">Accedere al tenant di valutazione di Microsoft 365 con l'account di amministratore globale.</span><span class="sxs-lookup"><span data-stu-id="db47f-109">Sign in to your Microsoft 365 trial tenant with your global administrator account.</span></span>
2. <span data-ttu-id="db47f-110">Dalla home page di Microsoft 365, fare clic su **Sicurezza e conformità**.</span><span class="sxs-lookup"><span data-stu-id="db47f-110">From the Microsoft 365 home page, click **Security & Compliance**.</span></span>
3. <span data-ttu-id="db47f-111">Nella nuova scheda Sicurezza e conformità, fare clic su **Autorizzazioni** > **Responsabile di eDiscovery**.</span><span class="sxs-lookup"><span data-stu-id="db47f-111">From the new Security & Compliance tab, click **Permissions** > **eDiscovery Manager**.</span></span>
4. <span data-ttu-id="db47f-112">Fare clic su **Modifica** per il responsabile di eDiscovery, quindi fare clic su **Scegli responsabile di eDiscovery**.</span><span class="sxs-lookup"><span data-stu-id="db47f-112">Click **Edit** for eDiscovery Manager, and then click **Choose eDiscovery Manager**.</span></span>
5. <span data-ttu-id="db47f-113">Fare clic su **+ Aggiungi**, cercare il nome dell'account amministratore globale e aggiungere il proprio account amministratore globale come responsabile di eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="db47f-113">Click **+ Add**, search for your global administrator account name and add your global administrator account as an eDiscovery Manager.</span></span>
6. <span data-ttu-id="db47f-114">Fare clic su **Fine** > **Salva** > **Chiudi**.</span><span class="sxs-lookup"><span data-stu-id="db47f-114">Click **Done** > **Save** > **Close**.</span></span>

## <a name="phase-2-add-personally-identifiable-information-to-your-tenant"></a><span data-ttu-id="db47f-115">Fase 2: aggiungere informazioni personali al tenant</span><span class="sxs-lookup"><span data-stu-id="db47f-115">Phase 2: Add personally identifiable information to your tenant</span></span>

<span data-ttu-id="db47f-116">In questa fase, viene creato un documento con le informazioni personali per una serie di IBAN di esempio; tale documento viene quindi archiviato su un sito di SharePoint Online nell'ambiente di sviluppo/test di Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="db47f-116">In this phase, you create a document with PII for a set of example International Banking Account Numbers (IBANs) and store it on a SharePoint Online site in your Microsoft 365 dev/test environment.</span></span>

1. <span data-ttu-id="db47f-117">Nel computer locale, aprire Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="db47f-117">On your local computer, open Microsoft Word.</span></span>
2. <span data-ttu-id="db47f-118">Incollare la tabella seguente nel file Word e salvarlo come "IBAN.docx" nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="db47f-118">Paste the following table in the Word file and save it as 'IBANs.docx' on your local computer.</span></span>

   |<span data-ttu-id="db47f-119">Numero </span><span class="sxs-lookup"><span data-stu-id="db47f-119">Number</span></span>|<span data-ttu-id="db47f-120">Paese</span><span class="sxs-lookup"><span data-stu-id="db47f-120">Country</span></span>|<span data-ttu-id="db47f-121">Codice</span><span class="sxs-lookup"><span data-stu-id="db47f-121">Code</span></span>|<span data-ttu-id="db47f-122">IBAN</span><span class="sxs-lookup"><span data-stu-id="db47f-122">IBAN</span></span>|
   |---|---|---|---|
   |<span data-ttu-id="db47f-123">1</span><span class="sxs-lookup"><span data-stu-id="db47f-123">1</span></span>|<span data-ttu-id="db47f-124">Austria SEPA</span><span class="sxs-lookup"><span data-stu-id="db47f-124">Austria SEPA</span></span>|<span data-ttu-id="db47f-125">AT</span><span class="sxs-lookup"><span data-stu-id="db47f-125">AT</span></span>|<span data-ttu-id="db47f-126">AT611904300234573201</span><span class="sxs-lookup"><span data-stu-id="db47f-126">AT611904300234573201</span></span>|
   |<span data-ttu-id="db47f-127">2</span><span class="sxs-lookup"><span data-stu-id="db47f-127">2</span></span>|<span data-ttu-id="db47f-128">Bulgaria SEPA</span><span class="sxs-lookup"><span data-stu-id="db47f-128">Bulgaria SEPA</span></span>|<span data-ttu-id="db47f-129">BG</span><span class="sxs-lookup"><span data-stu-id="db47f-129">BG</span></span>|<span data-ttu-id="db47f-130">BG80BNBG96611020345678</span><span class="sxs-lookup"><span data-stu-id="db47f-130">BG80BNBG96611020345678</span></span>|
   |<span data-ttu-id="db47f-131">3</span><span class="sxs-lookup"><span data-stu-id="db47f-131">3</span></span>|<span data-ttu-id="db47f-132">Danimarca SEPA</span><span class="sxs-lookup"><span data-stu-id="db47f-132">Denmark SEPA</span></span>|<span data-ttu-id="db47f-133">DK</span><span class="sxs-lookup"><span data-stu-id="db47f-133">DK</span></span>|<span data-ttu-id="db47f-134">DK5000400440116243</span><span class="sxs-lookup"><span data-stu-id="db47f-134">DK5000400440116243</span></span>|
   |<span data-ttu-id="db47f-135">4</span><span class="sxs-lookup"><span data-stu-id="db47f-135">4</span></span>|<span data-ttu-id="db47f-136">Finlandia SEPA</span><span class="sxs-lookup"><span data-stu-id="db47f-136">Finland SEPA</span></span>|<span data-ttu-id="db47f-137">FI</span><span class="sxs-lookup"><span data-stu-id="db47f-137">FI</span></span>|<span data-ttu-id="db47f-138">FI2112345600000785</span><span class="sxs-lookup"><span data-stu-id="db47f-138">FI2112345600000785</span></span>|
   |<span data-ttu-id="db47f-139">5</span><span class="sxs-lookup"><span data-stu-id="db47f-139">5</span></span>|<span data-ttu-id="db47f-140">Francia SEPA</span><span class="sxs-lookup"><span data-stu-id="db47f-140">France SEPA</span></span>|<span data-ttu-id="db47f-141">FR</span><span class="sxs-lookup"><span data-stu-id="db47f-141">FR</span></span>|<span data-ttu-id="db47f-142">FR1420041010050500013M02606</span><span class="sxs-lookup"><span data-stu-id="db47f-142">FR1420041010050500013M02606</span></span>|
   |<span data-ttu-id="db47f-143">6</span><span class="sxs-lookup"><span data-stu-id="db47f-143">6</span></span>|<span data-ttu-id="db47f-144">Germania SEPA</span><span class="sxs-lookup"><span data-stu-id="db47f-144">Germany SEPA</span></span>|<span data-ttu-id="db47f-145">DE</span><span class="sxs-lookup"><span data-stu-id="db47f-145">DE</span></span>|<span data-ttu-id="db47f-146">DE89370400440532013000</span><span class="sxs-lookup"><span data-stu-id="db47f-146">DE89370400440532013000</span></span>|
   |<span data-ttu-id="db47f-147">7</span><span class="sxs-lookup"><span data-stu-id="db47f-147">7</span></span>|<span data-ttu-id="db47f-148">Grecia SEPA</span><span class="sxs-lookup"><span data-stu-id="db47f-148">Greece SEPA</span></span>|<span data-ttu-id="db47f-149">GR</span><span class="sxs-lookup"><span data-stu-id="db47f-149">GR</span></span>|<span data-ttu-id="db47f-150">GR1601101250000000012300695</span><span class="sxs-lookup"><span data-stu-id="db47f-150">GR1601101250000000012300695</span></span>|
   |<span data-ttu-id="db47f-151">8</span><span class="sxs-lookup"><span data-stu-id="db47f-151">8</span></span>|<span data-ttu-id="db47f-152">Italia SEPA</span><span class="sxs-lookup"><span data-stu-id="db47f-152">Italy SEPA</span></span>|<span data-ttu-id="db47f-153">IT</span><span class="sxs-lookup"><span data-stu-id="db47f-153">IT</span></span>|<span data-ttu-id="db47f-154">GR1601101250000000012300695</span><span class="sxs-lookup"><span data-stu-id="db47f-154">GR1601101250000000012300695</span></span>|
   |<span data-ttu-id="db47f-155">9</span><span class="sxs-lookup"><span data-stu-id="db47f-155">9</span></span>|<span data-ttu-id="db47f-156">Paesi Bassi SEPA</span><span class="sxs-lookup"><span data-stu-id="db47f-156">Netherlands SEPA</span></span>|<span data-ttu-id="db47f-157">NL</span><span class="sxs-lookup"><span data-stu-id="db47f-157">NL</span></span>|<span data-ttu-id="db47f-158">NL91ABNA0417164300</span><span class="sxs-lookup"><span data-stu-id="db47f-158">NL91ABNA0417164300</span></span>|
   |<span data-ttu-id="db47f-159">10</span><span class="sxs-lookup"><span data-stu-id="db47f-159">10</span></span>|<span data-ttu-id="db47f-160">Polonia SEPA</span><span class="sxs-lookup"><span data-stu-id="db47f-160">Poland SEPA</span></span>|<span data-ttu-id="db47f-161">PL</span><span class="sxs-lookup"><span data-stu-id="db47f-161">PL</span></span>|<span data-ttu-id="db47f-162">PL27114020040000300201355387</span><span class="sxs-lookup"><span data-stu-id="db47f-162">PL27114020040000300201355387</span></span>|

   <span data-ttu-id="db47f-163">Nota:- questo esempio di set di dati deriva da informazioni pubblicamente disponibili e deve essere utilizzato solo a scopo di test.</span><span class="sxs-lookup"><span data-stu-id="db47f-163">Note:- This sample data set is derived from publicly available information and is intended to be used for test purposes only.</span></span>

3. <span data-ttu-id="db47f-164">In una nuova scheda del browser, digitare:  **https://**\<YourTenantName\>**.sharepoint.com**</span><span class="sxs-lookup"><span data-stu-id="db47f-164">In a new tab of your browser, type:  **https://**\<YourTenantName\>**.sharepoint.com**</span></span>
4. <span data-ttu-id="db47f-p101">Fare clic su **Documenti** per aprire la raccolta documenti di questo sito. Se viene richiesto di seguire una presentazione di nuovi elenchi, fare clic su **Avanti** fino al suo termine.</span><span class="sxs-lookup"><span data-stu-id="db47f-p101">Click **Documents** to open the document library for this site. If you're prompted for a new list experience tour, click **Next** until it's finished.</span></span>
5. <span data-ttu-id="db47f-167">Fare clic su **Carica** > **File** e selezionare il file IBAN.docx creato nella Fase 2.</span><span class="sxs-lookup"><span data-stu-id="db47f-167">Click **Upload** > **Files** and select the IBANs.docx you created in step 2.</span></span>

## <a name="phase-3-demonstrate-data-discovery"></a><span data-ttu-id="db47f-168">Fase 3: dimostrare l'individuazione dei dati</span><span class="sxs-lookup"><span data-stu-id="db47f-168">Phase 3: Demonstrate data discovery</span></span>

<span data-ttu-id="db47f-169">In questa fase, viene dimostrato come cercare il documento creato e archiviato nella Fase 2, in base agli IBAN che vi sono contenuti.</span><span class="sxs-lookup"><span data-stu-id="db47f-169">In this phase, you demonstrate search to find the document created and stored in Phase 2, based on its content containing IBANs.</span></span>

1. <span data-ttu-id="db47f-170">Nella scheda Sicurezza e conformità, fare clic su **Home**, quindi fare clic su **Ricerca e indagini** > **Ricerca di contenuto**.</span><span class="sxs-lookup"><span data-stu-id="db47f-170">From the Security & Compliance tab, click **Home**, and then click **Search & investigation** > **Content search**.</span></span>
2. <span data-ttu-id="db47f-171">Creare un nuovo elemento da cercare facendo clic su **+**.</span><span class="sxs-lookup"><span data-stu-id="db47f-171">Create a new search item by clicking on **+**.</span></span>
3. <span data-ttu-id="db47f-172">In una nuova finestra, fornire le seguenti informazioni: a.</span><span class="sxs-lookup"><span data-stu-id="db47f-172">In a new window, provide the following information: a.</span></span> <span data-ttu-id="db47f-173">Nome: Ricerca IBAN b.</span><span class="sxs-lookup"><span data-stu-id="db47f-173">Name: IBAN Search b.</span></span> <span data-ttu-id="db47f-174">Indicare dove si desidera eseguire la ricerca: **scegliere siti specifici in cui eseguire la ricerca** (fare clic su **+**), and quindi immettere l'URL del sito: **https://**\<YourTenantName\>**.sharepoint.com/** c.</span><span class="sxs-lookup"><span data-stu-id="db47f-174">Where do you want us to look?: **Choose specific sites to search** (click **+**), and then enter the site's URL: **https://**\<YourTenantName\>**.sharepoint.com/** c.</span></span> <span data-ttu-id="db47f-175">Fare clic su **Aggiungi** e quindi su **OK**.</span><span class="sxs-lookup"><span data-stu-id="db47f-175">Click **Add**, and then click **OK**.</span></span> <span data-ttu-id="db47f-176">Se viene visualizzato un avviso, fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="db47f-176">If you see a Warning, click **OK**.</span></span>
    <span data-ttu-id="db47f-177">d.</span><span class="sxs-lookup"><span data-stu-id="db47f-177">d.</span></span> <span data-ttu-id="db47f-178">Fare clic su **Avanti** in una finestra **Nuova ricerca**.</span><span class="sxs-lookup"><span data-stu-id="db47f-178">Click **Next** on a **New search** window.</span></span>
    <span data-ttu-id="db47f-179">e.</span><span class="sxs-lookup"><span data-stu-id="db47f-179">e.</span></span> <span data-ttu-id="db47f-180">**Indicare cosa si desidera cercare**: **SensitiveType:"International Banking Account Number (IBAN)"**, quindi **Cerca**.</span><span class="sxs-lookup"><span data-stu-id="db47f-180">For **What do you want us to look for?**: **SensitiveType:"International Banking Account Number (IBAN)"**, and then click **Search**.</span></span>

4. <span data-ttu-id="db47f-181">Assicurarsi che nei risultati di **Ricerca IBAN** sia presente almeno una voce.</span><span class="sxs-lookup"><span data-stu-id="db47f-181">Make sure you see at least one item listed in the **IBAN Search** results.</span></span>

## <a name="phase-4-create-a-custom-sensitive-information-type-via-powershell"></a><span data-ttu-id="db47f-182">Fase 4: creare un tipo di informazione riservata personalizzato tramite PowerShell</span><span class="sxs-lookup"><span data-stu-id="db47f-182">Phase 4: Create a custom sensitive information type via PowerShell</span></span>

<span data-ttu-id="db47f-p103">In questa fase, viene creato un tipo di informazione riservata personalizzato per l'azienda fittizia Contoso Corporation tramite Microsoft PowerShell. Contoso si avvale di un Contoso Customer Number (CCN) per identificare ogni cliente nel proprio database dei clienti. Un CCN ha la struttura seguente:</span><span class="sxs-lookup"><span data-stu-id="db47f-p103">In this phase, you create a custom sensitive information type for the fictional Contoso Corporation using Microsoft PowerShell.  Contoso uses a Contoso Customer Number (CCN) to identify each customer in their customer database. A CCN consists of the following structure:</span></span>

- <span data-ttu-id="db47f-186">Due cifre che rappresentano l'anno in cui è stato creato il record.</span><span class="sxs-lookup"><span data-stu-id="db47f-186">Two digits to represent the year that the record was created.</span></span>
  - <span data-ttu-id="db47f-187">Contoso è stata fondata nel 2002; di conseguenza, il primo valore utile sarebbe 02.</span><span class="sxs-lookup"><span data-stu-id="db47f-187">Contoso was founded in 2002; therefore, the earliest possible value would be 02.</span></span>
- <span data-ttu-id="db47f-188">Tre cifre che rappresentano l'agenzia partner che ha creato il record.</span><span class="sxs-lookup"><span data-stu-id="db47f-188">Three digits to represent the partner agency that created the record.</span></span>
  - <span data-ttu-id="db47f-189">I valori possibili per l'agenzia sono compresi tra 000 e 999.</span><span class="sxs-lookup"><span data-stu-id="db47f-189">Possible agency values range from 000 to 999.</span></span>
- <span data-ttu-id="db47f-190">Un carattere alfabetico che rappresenta la linea di business.</span><span class="sxs-lookup"><span data-stu-id="db47f-190">An alphabetic character to represent the line of business.</span></span>
  - <span data-ttu-id="db47f-191">I valori possibili sono compresi tra a e z, senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="db47f-191">Possible values are a-z and should be case insensitive.</span></span>
- <span data-ttu-id="db47f-192">Un numero di serie di quattro cifre.</span><span class="sxs-lookup"><span data-stu-id="db47f-192">A four-digit serial number.</span></span>
  - <span data-ttu-id="db47f-193">I possibili valori per il numero di serie sono compresi tra 0000 e 9999.</span><span class="sxs-lookup"><span data-stu-id="db47f-193">Possible serial number values range from 0000 to 9999.</span></span>

<span data-ttu-id="db47f-p104">Contoso fa sempre riferimento ai clienti utilizzando un CCN nella corrispondenza interna/esterna, nei documenti e in altri moduli. Contoso ha bisogno di un tipo di elemento riservato personalizzato che rilevi l'uso di CCN nei contenuti di Microsoft 365 per poter applicare la protezione per l'utilizzo di questo modulo di informazioni personali.</span><span class="sxs-lookup"><span data-stu-id="db47f-p104">Contoso always refers to customers by using a CCN in internal correspondence, external correspondence, documents, and other forms. Contoso needs a custom sensitive item type to detect the use of CCNs in Microsoft 365 content so that they may apply protection to the use of this form of personal identifiable information.</span></span>

1. <span data-ttu-id="db47f-196">Usare le istruzioni per la connessione con autenticazione a più fattori (AMF) in [Connettersi a PowerShell nel centro sicurezza e conformità](https://docs.microsoft.com/powershell/exchange/connect-to-scc-powershell) e connettersi al centro sicurezza e conformità con l'UPN dell'account del proprio amministratore globale.</span><span class="sxs-lookup"><span data-stu-id="db47f-196">Use the multi-factor authentication (MFA) connection instructions in [Connect to Security & Compliance Center PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-scc-powershell) and connect to the Security & Compliance Center with UPN of your global administrator account.</span></span>

2. <span data-ttu-id="db47f-197">Eseguire i seguenti comandi PowerShell.</span><span class="sxs-lookup"><span data-stu-id="db47f-197">Run the following PowerShell commands.</span></span>

   ```powershell
   #Create & start search for sample data
   $searchName = "Sample Customer Information Search"
   $searchQuery = "15080P9562 OR 14040O1119 OR 15020J8317 OR 14050E2330 OR 16050E2166 OR 17040O1118"
   New-ComplianceSearch -Name $searchName -SharePointLocation All -ExchangeLocation All -ContentMatchQuery $searchQuery
   Start-ComplianceSearch -Identity $searchName#Create & start search for sample data
   $searchName = "Sample Customer Information Search"
   $searchQuery = "15080P9562 OR 14040O1119 OR 15020J8317 OR 14050E2330 OR 16050E2166 OR 17040O1118"
   New-ComplianceSearch -Name $searchName -SharePointLocation All -ExchangeLocation All -ContentMatchQuery $searchQuery
   Start-ComplianceSearch -Identity $searchName
   ```

3. <span data-ttu-id="db47f-198">Eseguire i seguenti comandi PowerShell e copiare i GUID generati in un'istanza aperta di Blocco note sul computer in uso nell'ordine in cui vengono visualizzati.</span><span class="sxs-lookup"><span data-stu-id="db47f-198">Run the following PowerShell commands and copy the generated GUIDs to an open instance of Notepad on your computer in the order in which they are listed.</span></span>

   ```powershell
   #Generate three unique GUIDs
   Write-Host "GUID1 = "([guid]::NewGuid().Guid)
   Write-Host "GUID2 = "([guid]::NewGuid().Guid)
   Write-Host "GUID3 = "([guid]::NewGuid().Guid)
   ```

4. <span data-ttu-id="db47f-199">Nel computer locale, aprire un'altra istanza di Blocco note e incollarla nel contenuto seguente:</span><span class="sxs-lookup"><span data-stu-id="db47f-199">On your local computer, open another instance of Notepad and paste in the following content:</span></span>

   ```text
   <?xml version="1.0" encoding="utf-8"?>
   <RulePackage xmlns="https://schemas.microsoft.com/office/2011/mce">
   <RulePack id="GUID1">
   <Version major="1" minor="0" build="0" revision="0" />
   <Publisher id="GUID2" />
   <Details defaultLangCode="en">
   <LocalizedDetails langcode="en">
   <PublisherName>Contoso Ltd.</PublisherName>
   <Name>Contoso Rule Package</Name>
   <Description>Defines Contoso's custom set of classification rules</Description>
   </LocalizedDetails>
   </Details>
   </RulePack>
   <Rules>
   <!-- Contoso Customer Number (CCN) -->
   <Entity id="GUID3" patternsProximity="300" recommendedConfidence="85">
   <Pattern confidenceLevel="85">
   <IdMatch idRef="Regex_contoso_ccn" />
   <Match idRef="Keyword_contoso_ccn" />
   <Match idRef="Regex_eu_date" />
   </Pattern>
   </Entity>
   <Regex id="Regex_contoso_ccn">[0-1][0-9][0-9]{3}[A-Za-z][0-9]{4}</Regex>
   <Keyword id="Keyword_contoso_ccn">
   <Group matchStyle="word">
   <Term caseSensitive="false">customer number</Term>
   <Term caseSensitive="false">customer no</Term>
   <Term caseSensitive="false">customer #</Term>
   <Term caseSensitive="false">customer#</Term>
   <Term caseSensitive="false">Contoso customer</Term>
   </Group>
   </Keyword>
   <Regex id="Regex_eu_date"> (0?[1-9]|[12][0-9]|3[0-1])[\/-](0?[1-9]|1[0-2]|j\x00e4n(uar)?|jan(uary|uari|uar|eiro|vier|v)?|ene(ro)?|genn(aio)? |feb(ruary|ruari|rero|braio|ruar|br)?|f\x00e9vr(ier)?|fev(ereiro)?|mar(zo|o|ch|s)?|m\x00e4rz|maart|apr(ile|il)?|abr(il)?|avril |may(o)?|magg(io)?|mai|mei|mai(o)?|jun(io|i|e|ho)?|giugno|juin|jul(y|io|i|ho)?|lu(glio)?|juil(let)?|ag(o|osto)?|aug(ustus|ust)?|ao\x00fbt|sep|sept(ember|iembre|embre)?|sett(embre)?|set(embro)?|oct(ober|ubre|obre)?|ott(obre)?|okt(ober)?|out(ubro)? |nov(ember|iembre|embre|embro)?|dec(ember)?|dic(iembre|embre)?|dez(ember|embro)?|d\x00e9c(embre)?)[ \/-](19|20)?[0-9]{2}</Regex>
   <LocalizedStrings>
   <Resource idRef="GUID3">
   <Name default="true" langcode="en-us">Contoso Customer Number (CCN)</Name>
   <Description default="true" langcode="en-us">Contoso Customer Number (CCN) that looks for additional keywords and EU formatted date</Description>
   </Resource>
   </LocalizedStrings>
   </Rules>
   </RulePackage>
   ```

5. <span data-ttu-id="db47f-200">Sostituire i valori di GUID1, GUID2 e GUID3 nel testo XML del passaggio 4 con i rispettivi valori del passaggio 3, quindi salvare i contenuti sul computer locale con il nome di ContosoCCN.xml.</span><span class="sxs-lookup"><span data-stu-id="db47f-200">Replace the values of GUID1, GUID2, and GUID3 in the XML text of step 4 with their values from step 3, and then save the contents on your local computer with the name ContosoCCN.xml.</span></span>

6. <span data-ttu-id="db47f-201">Inserire il percorso al file ContosoCCN.xml ed eseguire i seguenti comandi.</span><span class="sxs-lookup"><span data-stu-id="db47f-201">Fill in the path to your ContosoCCN.xml file and run the following commands.</span></span>

   ```powershell
   #Create new Sensitive Information Type
   $path="<path to the ContosoCCN.xml file, such as C:\Scripts\ContosoCCN.xml>"
   New-DlpSensitiveInformationTypeRulePackage -FileData (Get-Content -Path $path -Encoding Byte -ReadCount 0)
   ```

7. <span data-ttu-id="db47f-p105">Dalla scheda Sicurezza e conformità, fare clic su **Classificazioni** > **Tipi di informazioni riservate**. Il Contoso Customer Number (CCN) dovrebbe essere visualizzato nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="db47f-p105">From the Security & Compliance tab, click **Classifications** > **Sensitive information types**. You should see the Contoso Customer Number (CCN) in the list.</span></span>

## <a name="phase-5-demonstrate-data-protection"></a><span data-ttu-id="db47f-204">Fase 5: dimostrare la protezione dei dati</span><span class="sxs-lookup"><span data-stu-id="db47f-204">Phase 5: Demonstrate data protection</span></span>

<span data-ttu-id="db47f-205">La protezione delle informazioni personali di Microsoft 365 include l'uso delle funzionalità di prevenzione della perdita dei dati (DPL).</span><span class="sxs-lookup"><span data-stu-id="db47f-205">Protection of personal information in Microsoft 365 includes using data loss prevention (DLP) capabilities.</span></span>  <span data-ttu-id="db47f-206">Con i criteri DPL, è possibile proteggere automaticamente le informazioni riservate in Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="db47f-206">With DLP policies, you can automatically protect sensitive information across Microsoft 365.</span></span>

<span data-ttu-id="db47f-p107">Esistono molti modi per applicare la protezione. Investire nella formazione e nella sensibilizzazione in merito alla posizione in cui i dati degli utenti che risiedono nell'UE vengono memorizzati nell'ambiente e a come i dipendenti sono autorizzati a gestirli, rappresenta un livello di protezione delle informazioni tramite i criteri di prevenzione della perdita dei dati di Office 365.</span><span class="sxs-lookup"><span data-stu-id="db47f-p107">There are multiple ways you can apply the protection. Educating and raising awareness to where EU resident data is stored in your environment and how your employees are permitted to handle it represents one level of information protection using Office 365 DLP.</span></span>

<span data-ttu-id="db47f-209">In questa fase, viene creato un nuovo criterio DLP e viene dimostrato come applicarlo al file IBAN.docx archiviato in SharePoint Online nella Fase 2 e quando si tenta di inviare un'e-mail contenente IBAN.</span><span class="sxs-lookup"><span data-stu-id="db47f-209">In this phase, you create a new DLP policy and demonstrate how it gets applied to the IBANs.docx file you stored in SharePoint Online in Phase 2 and when you attempt to send an email containing IBANs.</span></span>

1. <span data-ttu-id="db47f-210">Dalla scheda Sicurezza e conformità del browser fare clic su **Home**.</span><span class="sxs-lookup"><span data-stu-id="db47f-210">From the Security & Compliance tab of your browser, click **Home**.</span></span>
2. <span data-ttu-id="db47f-211">Fare clic su **Prevenzione della perdita dei dati** > **Criteri**.</span><span class="sxs-lookup"><span data-stu-id="db47f-211">Click **Data loss prevention** > **Policy**.</span></span>
3. <span data-ttu-id="db47f-212">Fare clic su **+ Crea un criterio**.</span><span class="sxs-lookup"><span data-stu-id="db47f-212">Click **+ Create a policy**.</span></span>
4. <span data-ttu-id="db47f-213">In **Inizia da un modello o Crea criteri personalizzati** fare clic su **Personalizzato** > **Criteri personalizzati** > **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="db47f-213">In **Start with a template or create a custom policy**, click **Custom** > **Custom policy** > **Next**.</span></span>
5. <span data-ttu-id="db47f-p108">In **Denomina il criterio** fornire i seguenti dettagli e quindi fare clic su **Avanti**:  a. Nome: **Criterio informazioni personali cittadino UE** b. Descrizione: **Proteggere le informazioni personali dei cittadini europei**</span><span class="sxs-lookup"><span data-stu-id="db47f-p108">In **Name your policy**, provide the following details and then click **Next**:  a. Name: **EU Citizen PII Policy** b. Description: **Protect the personally identifiable information of European citizens**</span></span>
6. <span data-ttu-id="db47f-p109">In **Seleziona posizioni**, scegliere **Tutte le posizioni in Microsoft 365**. Ciò include i contenuti nella posta di Exchange e nei documenti di OneDrive e SharePoint. Infine, fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="db47f-p109">In **Choose locations**, select **All locations in Microsoft 365**. This will include content in Exchange email and OneDrive and SharePoint documents. And then click **Next**.</span></span>
7. <span data-ttu-id="db47f-220">In **Personalizza il tipo di contenuti d proteggere** fare clic su **Trova contenuti che includono:** e quindi fare clic su **Modifica**.</span><span class="sxs-lookup"><span data-stu-id="db47f-220">In **Customize the type of content you want to protect**, click **Find content that contains:** and then click **Edit**.</span></span>
8. <span data-ttu-id="db47f-221">In **Scegli il tipo di contenuti da proteggere** fare clic su **Aggiungi** > **Tipi di informazioni riservate**.</span><span class="sxs-lookup"><span data-stu-id="db47f-221">In **Choose the types of content to protect**, click **Add** > **Sensitive info types**.</span></span>
9. <span data-ttu-id="db47f-222">In **Tipi di informazioni riservate** fare clic su **+ Aggiungi**.</span><span class="sxs-lookup"><span data-stu-id="db47f-222">In **Sensitive info types**, click **+ Add**.</span></span>
10. <span data-ttu-id="db47f-223">In **Tipi di informazioni riservate** cercare **IBAN**, selezionare la casella di controllo per **International Banking Account Number (IBAN)** e infine fare clic su **Aggiungi**.</span><span class="sxs-lookup"><span data-stu-id="db47f-223">In **Sensitive info types**, search for **IBAN**, select the check box for **International Banking Account Number (IBAN)**, and then click **Add**.</span></span>
11. <span data-ttu-id="db47f-224">Verificare che il tipo di informazione riservata **International Banking Account Number (IBAN)** sia stato aggiunto, quindi fare clic su **Fine**.</span><span class="sxs-lookup"><span data-stu-id="db47f-224">Confirm that the **International Banking Account Number (IBAN)** sensitive information type was added, and then click **Done**.</span></span>
12. <span data-ttu-id="db47f-225">In **I contenuti includono** verificare che i tipi di informazioni riservate siano stati aggiunti e quindi fare clic su **Salva**.</span><span class="sxs-lookup"><span data-stu-id="db47f-225">In **Content contains**, confirm that the sensitive information types were added and then click **Save**.</span></span>
13. <span data-ttu-id="db47f-226">In **Personalizza il tipo di contenuti d proteggere**, verificare che **Trova contenuti che includono:** contenga **International Banking Account Number (IBAN)**, quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="db47f-226">In **Customize the type of content you want to protect**, confirm  **Find content that contains:** contains the **International Banking Account Number (IBAN)**, and then click **Next**.</span></span>
14. <span data-ttu-id="db47f-227">In **Rileva quando i contenuti condivisi includono:**, modificare il valore da **10** a **1** e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="db47f-227">In **Detect when content that's being shared contains:**, change the value from **10** to **1**, and then click **Next**.</span></span>
15. <span data-ttu-id="db47f-228">In **Abilitare il criterio o eseguire prima un test?**, scegliere le impostazioni seguenti, quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="db47f-228">In **Do you want to turn on the policy or test things out first?**, choose the following settings, and then click **Next**.</span></span>
    <span data-ttu-id="db47f-229">a.</span><span class="sxs-lookup"><span data-stu-id="db47f-229">a.</span></span> <span data-ttu-id="db47f-230">Selezionare l'opzione per **Eseguire prima un test** b.</span><span class="sxs-lookup"><span data-stu-id="db47f-230">Select the option for **I'd like to test it out first** b.</span></span> <span data-ttu-id="db47f-231">Selezionare la casella di controllo per **Mostra i suggerimenti per i criteri in modalità di test**</span><span class="sxs-lookup"><span data-stu-id="db47f-231">Select the check box for **Show policy tips while in test mode**</span></span>
16. <span data-ttu-id="db47f-p111">In **Verifica impostazioni** fare clic su **Crea** dopo aver controllato le impostazioni. NOTA: dopo aver creato un nuovo criterio DLP, sarà necessario attendere un po' di tempo prima che la modifica diventi effettiva.</span><span class="sxs-lookup"><span data-stu-id="db47f-p111">In **Review your settings**, click **Create** after reviewing the settings. NOTE: After you create a new DLP policy, it will take a while for it to take effect.</span></span>
17. <span data-ttu-id="db47f-234">Nel computer locale, aprire un'istanza privata del browser.</span><span class="sxs-lookup"><span data-stu-id="db47f-234">On your local computer, open a private instance of your browser.</span></span>
18. <span data-ttu-id="db47f-235">Nella barra degli indirizzi, digitare **https://**\<YourTenantName\>**.sharepoint.com** e accedere con il proprio account amministratore globale.</span><span class="sxs-lookup"><span data-stu-id="db47f-235">In the address bar, type **https://**\<YourTenantName\>**.sharepoint.com** and sign in using your global administrator account.</span></span>
19. <span data-ttu-id="db47f-236">Fare clic su **Documenti**.</span><span class="sxs-lookup"><span data-stu-id="db47f-236">Click **Documents**.</span></span>
20. <span data-ttu-id="db47f-p112">Fare clic sul file denominato "IBAN.docx". Dovrebbe essere visualizzato "Suggerimento per i criteri per IBAN.docx". Il file IBAN.docx è stato condiviso con destinatari esterni, cosa che viola il criterio DLP.</span><span class="sxs-lookup"><span data-stu-id="db47f-p112">Click the file named 'IBANs.docx'. You should see 'Policy tip for IBANs.docx'.  The IBANs.docx file was shared with external recipients, which violates the DLP policy.</span></span>
21. <span data-ttu-id="db47f-240">Nella barra degli indirizzi digitare: `https://outlook.office365.com`</span><span class="sxs-lookup"><span data-stu-id="db47f-240">In the address bar, type: `https://outlook.office365.com`</span></span>
22. <span data-ttu-id="db47f-241">Fare clic su **Nuovo** - **Messaggio di posta elettronica** e fornire quanto segue:</span><span class="sxs-lookup"><span data-stu-id="db47f-241">Click **New** - **Email message** and provide the following:</span></span>

    - <span data-ttu-id="db47f-242">**A:** \<a personal email address\></span><span class="sxs-lookup"><span data-stu-id="db47f-242">**To:** \<a personal email address\></span></span>
    - <span data-ttu-id="db47f-243">**Oggetto:** Test GDPR</span><span class="sxs-lookup"><span data-stu-id="db47f-243">**Subject:** GDPR Test</span></span>
    - <span data-ttu-id="db47f-244">**Corpo:** copiare la tabella dei valori riportata di seguito.</span><span class="sxs-lookup"><span data-stu-id="db47f-244">**Body:** Copy in the table of values shown below.</span></span>

      |<span data-ttu-id="db47f-245">Numero</span><span class="sxs-lookup"><span data-stu-id="db47f-245">Number</span></span>|<span data-ttu-id="db47f-246">Paese</span><span class="sxs-lookup"><span data-stu-id="db47f-246">Country</span></span>|<span data-ttu-id="db47f-247">Codice</span><span class="sxs-lookup"><span data-stu-id="db47f-247">Code</span></span>|<span data-ttu-id="db47f-248">IBAN</span><span class="sxs-lookup"><span data-stu-id="db47f-248">IBAN</span></span>|
      |---|---|---|---|
      |<span data-ttu-id="db47f-249">1</span><span class="sxs-lookup"><span data-stu-id="db47f-249">1</span></span>|<span data-ttu-id="db47f-250">Austria SEPA</span><span class="sxs-lookup"><span data-stu-id="db47f-250">Austria SEPA</span></span>|<span data-ttu-id="db47f-251">AT</span><span class="sxs-lookup"><span data-stu-id="db47f-251">AT</span></span>|<span data-ttu-id="db47f-252">AT611904300234573201</span><span class="sxs-lookup"><span data-stu-id="db47f-252">AT611904300234573201</span></span>|
      |<span data-ttu-id="db47f-253">2</span><span class="sxs-lookup"><span data-stu-id="db47f-253">2</span></span>|<span data-ttu-id="db47f-254">Bulgaria SEPA</span><span class="sxs-lookup"><span data-stu-id="db47f-254">Bulgaria SEPA</span></span>|<span data-ttu-id="db47f-255">BG</span><span class="sxs-lookup"><span data-stu-id="db47f-255">BG</span></span>|<span data-ttu-id="db47f-256">BG80BNBG96611020345678</span><span class="sxs-lookup"><span data-stu-id="db47f-256">BG80BNBG96611020345678</span></span>|
      |<span data-ttu-id="db47f-257">3</span><span class="sxs-lookup"><span data-stu-id="db47f-257">3</span></span>|<span data-ttu-id="db47f-258">Danimarca SEPA</span><span class="sxs-lookup"><span data-stu-id="db47f-258">Denmark SEPA</span></span>|<span data-ttu-id="db47f-259">DK</span><span class="sxs-lookup"><span data-stu-id="db47f-259">DK</span></span>|<span data-ttu-id="db47f-260">DK5000400440116243</span><span class="sxs-lookup"><span data-stu-id="db47f-260">DK5000400440116243</span></span>|
      |<span data-ttu-id="db47f-261">4</span><span class="sxs-lookup"><span data-stu-id="db47f-261">4</span></span>|<span data-ttu-id="db47f-262">Finlandia SEPA</span><span class="sxs-lookup"><span data-stu-id="db47f-262">Finland SEPA</span></span>|<span data-ttu-id="db47f-263">FI</span><span class="sxs-lookup"><span data-stu-id="db47f-263">FI</span></span>|<span data-ttu-id="db47f-264">FI2112345600000785</span><span class="sxs-lookup"><span data-stu-id="db47f-264">FI2112345600000785</span></span>|
      |<span data-ttu-id="db47f-265">5</span><span class="sxs-lookup"><span data-stu-id="db47f-265">5</span></span>|<span data-ttu-id="db47f-266">Francia SEPA</span><span class="sxs-lookup"><span data-stu-id="db47f-266">France SEPA</span></span>|<span data-ttu-id="db47f-267">FR</span><span class="sxs-lookup"><span data-stu-id="db47f-267">FR</span></span>|<span data-ttu-id="db47f-268">FR1420041010050500013M02606</span><span class="sxs-lookup"><span data-stu-id="db47f-268">FR1420041010050500013M02606</span></span>|
      |<span data-ttu-id="db47f-269">6</span><span class="sxs-lookup"><span data-stu-id="db47f-269">6</span></span>|<span data-ttu-id="db47f-270">Germania SEPA</span><span class="sxs-lookup"><span data-stu-id="db47f-270">Germany SEPA</span></span>|<span data-ttu-id="db47f-271">DE</span><span class="sxs-lookup"><span data-stu-id="db47f-271">DE</span></span>|<span data-ttu-id="db47f-272">DE89370400440532013000</span><span class="sxs-lookup"><span data-stu-id="db47f-272">DE89370400440532013000</span></span>|
      |<span data-ttu-id="db47f-273">7</span><span class="sxs-lookup"><span data-stu-id="db47f-273">7</span></span>|<span data-ttu-id="db47f-274">Grecia SEPA</span><span class="sxs-lookup"><span data-stu-id="db47f-274">Greece SEPA</span></span>|<span data-ttu-id="db47f-275">GR</span><span class="sxs-lookup"><span data-stu-id="db47f-275">GR</span></span>|<span data-ttu-id="db47f-276">GR1601101250000000012300695</span><span class="sxs-lookup"><span data-stu-id="db47f-276">GR1601101250000000012300695</span></span>|
      |<span data-ttu-id="db47f-277">8</span><span class="sxs-lookup"><span data-stu-id="db47f-277">8</span></span>|<span data-ttu-id="db47f-278">Italia SEPA</span><span class="sxs-lookup"><span data-stu-id="db47f-278">Italy SEPA</span></span>|<span data-ttu-id="db47f-279">IT</span><span class="sxs-lookup"><span data-stu-id="db47f-279">IT</span></span>|<span data-ttu-id="db47f-280">GR1601101250000000012300695</span><span class="sxs-lookup"><span data-stu-id="db47f-280">GR1601101250000000012300695</span></span>|
      |<span data-ttu-id="db47f-281">9</span><span class="sxs-lookup"><span data-stu-id="db47f-281">9</span></span>|<span data-ttu-id="db47f-282">Paesi Bassi SEPA</span><span class="sxs-lookup"><span data-stu-id="db47f-282">Netherlands SEPA</span></span>|<span data-ttu-id="db47f-283">NL</span><span class="sxs-lookup"><span data-stu-id="db47f-283">NL</span></span>|<span data-ttu-id="db47f-284">NL91ABNA0417164300</span><span class="sxs-lookup"><span data-stu-id="db47f-284">NL91ABNA0417164300</span></span>|
      |<span data-ttu-id="db47f-285">10</span><span class="sxs-lookup"><span data-stu-id="db47f-285">10</span></span>|<span data-ttu-id="db47f-286">Polonia SEPA</span><span class="sxs-lookup"><span data-stu-id="db47f-286">Poland SEPA</span></span>|<span data-ttu-id="db47f-287">PL</span><span class="sxs-lookup"><span data-stu-id="db47f-287">PL</span></span>|<span data-ttu-id="db47f-288">PL27114020040000300201355387</span><span class="sxs-lookup"><span data-stu-id="db47f-288">PL27114020040000300201355387</span></span>|
      |

    <span data-ttu-id="db47f-289">Nota:- questo esempio di set di dati deriva da informazioni pubblicamente disponibili e deve essere utilizzato solo a scopo di test.</span><span class="sxs-lookup"><span data-stu-id="db47f-289">Note:- This sample data set is derived from publicly available information and is intended to be used for test purposes only.</span></span>

23. <span data-ttu-id="db47f-290">Si noterà che il criterio DLP ha riconosciuto che il corpo dell'e-mail include IBAN e fornisce un suggerimento per i criteri nella parte superiore della finestra del messaggio.</span><span class="sxs-lookup"><span data-stu-id="db47f-290">You will see that the DLP policy recognized that body of the email contains IBANs and provides you with the policy tip at the top of the message window.</span></span>
24. <span data-ttu-id="db47f-291">Chiudere l'istanza privata del browser.</span><span class="sxs-lookup"><span data-stu-id="db47f-291">Close the private instance of your browser.</span></span>

## <a name="phase-6-demonstrate-reporting"></a><span data-ttu-id="db47f-292">Fase 6: dimostrare la creazione di report</span><span class="sxs-lookup"><span data-stu-id="db47f-292">Phase 6: Demonstrate reporting</span></span>

<span data-ttu-id="db47f-293">In questa fase, viene dimostrata la creazione di report di Microsoft 365 in base al criterio DLP configurato nella Fase 5.</span><span class="sxs-lookup"><span data-stu-id="db47f-293">In this phase, you demonstrate Microsoft 365 reporting based on the DLP policy configured in Phase 5.</span></span>

   1. <span data-ttu-id="db47f-294">Dalla scheda Sicurezza e conformità del browser fare clic su **Home**.</span><span class="sxs-lookup"><span data-stu-id="db47f-294">From the Security & Compliance tab of your browser, click **Home**.</span></span>
   2. <span data-ttu-id="db47f-295">Fare clic su **Report** > **Dashboard** > **Risultati dei criteri di prevenzione della perdita dei dati**.</span><span class="sxs-lookup"><span data-stu-id="db47f-295">Click **Reports** > **Dashboard** > **DLP policy matches**.</span></span>
   3. <span data-ttu-id="db47f-p113">I criteri di prevenzione della perdita dei dati consentono di identificare e proteggere le informazioni riservate dell'organizzazione. Ad esempio, il report indicherà che i criteri hanno identificato il documento che include IBAN archiviati in SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="db47f-p113">Your DLP policy helps identify and protect organization's sensitive information. For example, in the report you will see that the policy identified the document that contains IBANs stored in SharePoint Online.</span></span>
