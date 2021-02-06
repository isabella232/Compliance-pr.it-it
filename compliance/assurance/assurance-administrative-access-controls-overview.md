---
title: Controlli di accesso amministrativo in Microsoft 365
description: Questo articolo offre una panoramica dei controlli di accesso amministrativo e della categorizzazione dei dati in Microsoft 365.
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
f1.keywords:
- NOCSH
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: d3d6cd30fbe682de979d5c04943c57cedc86552f
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120715"
---
# <a name="administrative-access-controls-in-microsoft-365"></a><span data-ttu-id="07214-103">Controlli di accesso amministrativo in Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="07214-103">Administrative access controls in Microsoft 365</span></span> 

<span data-ttu-id="07214-104">Microsoft ha investito molto in sistemi e controlli che automatizzano la maggior parte delle operazioni di Microsoft 365 limitando intenzionalmente l'accesso ai contenuti dei clienti da parte di Microsoft.</span><span class="sxs-lookup"><span data-stu-id="07214-104">Microsoft has invested heavily in systems and controls that automate most Microsoft 365 operations while intentionally limiting access to customer content by Microsoft.</span></span> <span data-ttu-id="07214-105">Gli umani regolano il servizio e il software gestisce il servizio.</span><span class="sxs-lookup"><span data-stu-id="07214-105">Humans govern the service, and software operates the service.</span></span> <span data-ttu-id="07214-106">Questa struttura consente a Microsoft di gestire Microsoft 365 su larga scala e di gestire i rischi delle minacce interne ai contenuti dei clienti.</span><span class="sxs-lookup"><span data-stu-id="07214-106">This structure enables Microsoft to manage Microsoft 365 at scale and manage the risks of internal threats to customer content.</span></span>

<span data-ttu-id="07214-107">Per impostazione predefinita, i tecnici Microsoft non hanno privilegi amministrativi permanenti e non hanno accesso permanente ai contenuti dei clienti in Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="07214-107">By default, Microsoft engineers have zero standing administrative privileges and zero standing access to customer content in Microsoft 365.</span></span> <span data-ttu-id="07214-108">Un tecnico Microsoft può avere accesso limitato, controllati e protetto ai contenuti di un cliente per un periodo di tempo limitato.</span><span class="sxs-lookup"><span data-stu-id="07214-108">A Microsoft engineer can have limited, audited, and secured access to a customer's content for a limited amount of time.</span></span> <span data-ttu-id="07214-109">L'accesso è solo quando necessario per le operazioni di servizio e solo se approvato da un membro del senior management Microsoft.</span><span class="sxs-lookup"><span data-stu-id="07214-109">Access is only when necessary for service operations and only when approved by a member of Microsoft senior management.</span></span> <span data-ttu-id="07214-110">Per i clienti con licenza Customer Lockbox, il cliente fornisce l'approvazione dell'accesso ai contenuti ospitati in Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="07214-110">For Customer Lockbox licensed customers, the customer provides access approval to their content hosted on Microsoft 365.</span></span>

<span data-ttu-id="07214-111">Microsoft fornisce servizi online utilizzando più forme di distribuzione cloud:</span><span class="sxs-lookup"><span data-stu-id="07214-111">Microsoft provides online services using multiple forms of cloud delivery:</span></span>

- <span data-ttu-id="07214-112">**Cloud pubblici:** Include le versioni multi-tenant di Microsoft 365, Azure e altri servizi ospitati in Nord America, Sud America, Europa, Asia, Australia e così via.</span><span class="sxs-lookup"><span data-stu-id="07214-112">**Public clouds:** Includes multi-tenant versions of Microsoft 365, Azure, and other services hosted in North America, South America, Europe, Asia, Australia, etc.</span></span>
- <span data-ttu-id="07214-113">**Cloud nazionali:** Include tutti i cloud sovrani e gestiti da terze parti al di fuori degli Stati Uniti (ad eccezione di quelli menzionati in precedenza), come Microsoft 365 in Cina (gestito da 21Vianet) e Microsoft 365 in Germania (gestito da Microsoft, ma secondo un modello in cui un trustee dei dati tedesco, Deutsche Telekom, controlla e monitora l'accesso di Microsoft ai dati dei clienti e ai sistemi che contengono i dati dei clienti).</span><span class="sxs-lookup"><span data-stu-id="07214-113">**National clouds:** Includes all sovereign and third party-operated clouds outside of the United States (except ones noted previously), such as Microsoft 365 in China (operated by 21Vianet), and Microsoft 365 in Germany (operated by Microsoft, but under a model in which a German data trustee, Deutsche Telekom, controls and monitors Microsoft's access to customer data and systems that contain customer data).</span></span>
- <span data-ttu-id="07214-114">**Cloud per enti pubblici:** Include i servizi di Microsoft 365 e Azure disponibili per i clienti del governo degli Stati Uniti.</span><span class="sxs-lookup"><span data-stu-id="07214-114">**Government clouds:** Includes Microsoft 365 and Azure services that are available to United States government customers.</span></span>

<span data-ttu-id="07214-115">Ai fini di questo articolo, i servizi di Microsoft 365 includono:</span><span class="sxs-lookup"><span data-stu-id="07214-115">For purposes of this article, Microsoft 365 services include:</span></span>

- [<span data-ttu-id="07214-116">Exchange Online</span><span class="sxs-lookup"><span data-stu-id="07214-116">Exchange Online</span></span>](/Exchange/exchange-online)
- [<span data-ttu-id="07214-117">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="07214-117">Exchange Online Protection</span></span>](/Office365/SecurityCompliance/eop/exchange-online-protection-overview)
- [<span data-ttu-id="07214-118">SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="07214-118">SharePoint Online</span></span>](/sharepoint/sharepoint-online)
- [<span data-ttu-id="07214-119">OneDrive for Business</span><span class="sxs-lookup"><span data-stu-id="07214-119">OneDrive for Business</span></span>](/OneDrive/onedrive)
- [<span data-ttu-id="07214-120">Skype for Business</span><span class="sxs-lookup"><span data-stu-id="07214-120">Skype for Business</span></span>](/SkypeForBusiness/skype-for-business-online)
- [<span data-ttu-id="07214-121">Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="07214-121">Microsoft Teams</span></span>](/MicrosoftTeams/Teams-overview)
- [<span data-ttu-id="07214-122">Yammer</span><span class="sxs-lookup"><span data-stu-id="07214-122">Yammer</span></span>](/yammer/yammer-landing-page)

## <a name="microsoft-365-access-controls"></a><span data-ttu-id="07214-123">Controlli di accesso di Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="07214-123">Microsoft 365 access controls</span></span>

<span data-ttu-id="07214-124">Ai fini del controllo di accesso, Microsoft classifica i dati di Microsoft 365 come dati dei clienti o altri tipi di dati.</span><span class="sxs-lookup"><span data-stu-id="07214-124">For access control purposes, Microsoft categorizes Microsoft 365 data as customer data or other types of data.</span></span>

### <a name="customer-data"></a><span data-ttu-id="07214-125">Dati cliente
</span><span class="sxs-lookup"><span data-stu-id="07214-125">Customer data</span></span>

<span data-ttu-id="07214-126">I dati dei clienti sono tutti i dati forniti da o per conto di un cliente quando si usano i servizi di Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="07214-126">Customer data is all data provided by or on behalf of a customer when using Microsoft 365 services.</span></span> <span data-ttu-id="07214-127">Questi dati sono contenuti dei clienti creati o caricati direttamente dagli utenti di Microsoft 365, tra cui:</span><span class="sxs-lookup"><span data-stu-id="07214-127">This data is customer content directly created or uploaded by Microsoft 365 users, including:</span></span>

- <span data-ttu-id="07214-128">Messaggi di posta elettronica</span><span class="sxs-lookup"><span data-stu-id="07214-128">Emails</span></span>
- <span data-ttu-id="07214-129">Contenuto di SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="07214-129">SharePoint Online content</span></span>
- <span data-ttu-id="07214-130">Messaggi istantanei</span><span class="sxs-lookup"><span data-stu-id="07214-130">Instant messages</span></span>
- <span data-ttu-id="07214-131">Elementi del calendario</span><span class="sxs-lookup"><span data-stu-id="07214-131">Calendar items</span></span>
- <span data-ttu-id="07214-132">Documenti</span><span class="sxs-lookup"><span data-stu-id="07214-132">Documents</span></span>
- <span data-ttu-id="07214-133">Contatti</span><span class="sxs-lookup"><span data-stu-id="07214-133">Contacts</span></span>
- <span data-ttu-id="07214-134">Informazioni di identificazione dell'utente finale (EUII) (dati univoci per un utente o che sono collegabili a un singolo utente ma che non includono il contenuto del cliente)</span><span class="sxs-lookup"><span data-stu-id="07214-134">End-user identifiable information (EUII) (data that is unique to a user or that is linkable to an individual user but does not include customer content)</span></span>

### <a name="other-types-of-data"></a><span data-ttu-id="07214-135">Altri tipi di dati</span><span class="sxs-lookup"><span data-stu-id="07214-135">Other types of data</span></span>

<span data-ttu-id="07214-136">Altri tipi di dati includono:</span><span class="sxs-lookup"><span data-stu-id="07214-136">Other types of data include:</span></span>

- <span data-ttu-id="07214-137">**Dati dell'account:** Include i dati amministrativi (informazioni fornite dagli amministratori durante l'iscrizione o l'acquisto di servizi) e i dati di pagamento (informazioni sugli strumenti di pagamento, ad esempio i dettagli della carta di credito).</span><span class="sxs-lookup"><span data-stu-id="07214-137">**Account data:** Includes administrative data (information provided by administrators when they sign-up or purchase services), and payment data (information about payment instruments, such as credit card details).</span></span>
- <span data-ttu-id="07214-138">**Informazioni identificabili dall'organizzazione:** Include i dati usati per identificare un tenant, dati di utilizzo e non collegabili a un singolo utente o inclusi nel contenuto del cliente.</span><span class="sxs-lookup"><span data-stu-id="07214-138">**Organizationally identifiable information:** Includes data used to identify a tenant, usage data, and not linkable to an individual user or included in customer content.</span></span>
- <span data-ttu-id="07214-139">**Metadati di sistema:** Include log di servizio che contengono impostazioni di configurazione, stato del sistema, indirizzi IP Microsoft e informazioni tecniche su sottoscrizioni e tenant.</span><span class="sxs-lookup"><span data-stu-id="07214-139">**System metadata:** Includes service logs that contain configuration settings, system status, Microsoft IP addresses, and technical information about subscriptions and tenants.</span></span>

<span data-ttu-id="07214-140">Microsoft ha stabilito meccanismi di controllo degli accessi per garantire che nessuno abbia accesso non approvato ai dati dei clienti o ai dati di controllo di accesso.</span><span class="sxs-lookup"><span data-stu-id="07214-140">Microsoft has established access control mechanisms to ensure that no one has unapproved access to Customer Data or access control data.</span></span> <span data-ttu-id="07214-141">I dati di controllo di accesso gestiscono l'accesso ad altri tipi di dati o funzioni all'interno dell'ambiente, tra cui l'accesso al contenuto dei clienti o all'euiie, alle password Microsoft, ai certificati di sicurezza e ad altri dati correlati all'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="07214-141">Access control data manages access to other types of data or functions within the environment, including access to customer content or EUII, Microsoft passwords, security certificates, and other authentication-related data.</span></span> <span data-ttu-id="07214-142">I meccanismi di controllo dell'accesso sono anche di protezione dall'accesso fisico, logico o remoto non approvato all'ambiente di produzione di Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="07214-142">Access control mechanisms also guard against unapproved physical, logical, or remote access to the Microsoft 365 production environment.</span></span>

<span data-ttu-id="07214-143">Esistono tre categorie di controlli di accesso usati da Microsoft per l'utilizzo di Microsoft 365:</span><span class="sxs-lookup"><span data-stu-id="07214-143">There are three categories of access controls used by Microsoft for operating Microsoft 365:</span></span>

- <span data-ttu-id="07214-144">Controlli di isolamento</span><span class="sxs-lookup"><span data-stu-id="07214-144">Isolation controls</span></span>
- <span data-ttu-id="07214-145">Controlli del personale</span><span class="sxs-lookup"><span data-stu-id="07214-145">Personnel controls</span></span>
- <span data-ttu-id="07214-146">Controlli tecnologia</span><span class="sxs-lookup"><span data-stu-id="07214-146">Technology controls</span></span>

<span data-ttu-id="07214-147">Se combinati, questi controlli consentono di prevenire e rilevare azioni dannose in Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="07214-147">When combined, these controls help prevent and detect malicious actions in Microsoft 365.</span></span> <span data-ttu-id="07214-148">Oltre ai controlli di isolamento, personale e tecnologia utilizzati da Microsoft, esiste una quarta categoria di controlli: i controlli implementati dai clienti.</span><span class="sxs-lookup"><span data-stu-id="07214-148">In addition to the isolation, personnel, and technology controls used by Microsoft, there is a fourth category of controls: those controls implemented by customers.</span></span>

<span data-ttu-id="07214-149">Microsoft 365 consente di gestire i dati nello stesso modo in cui vengono gestiti in ambienti locali.</span><span class="sxs-lookup"><span data-stu-id="07214-149">Microsoft 365 allows you to manage data the same way data is managed in on-premises environments.</span></span> <span data-ttu-id="07214-150">La persona che si i annota un'organizzazione per Microsoft 365 diventa automaticamente un amministratore globale.</span><span class="sxs-lookup"><span data-stu-id="07214-150">The person who signs up an organization for Microsoft 365 automatically becomes a global administrator.</span></span> <span data-ttu-id="07214-151">L'amministratore globale ha accesso a tutte le funzionalità dei portali di gestione e può:</span><span class="sxs-lookup"><span data-stu-id="07214-151">The global admin has access to all features in Management Portals and can:</span></span>

- <span data-ttu-id="07214-152">Creare o modificare utenti</span><span class="sxs-lookup"><span data-stu-id="07214-152">Create or edit users</span></span>
- <span data-ttu-id="07214-153">Assegnare ruoli di amministratore ad altri utenti</span><span class="sxs-lookup"><span data-stu-id="07214-153">Assign admin roles to others</span></span>
- <span data-ttu-id="07214-154">Reimposta password utente</span><span class="sxs-lookup"><span data-stu-id="07214-154">Reset user passwords</span></span>
- <span data-ttu-id="07214-155">Gestire le licenze utente</span><span class="sxs-lookup"><span data-stu-id="07214-155">Manage user licenses</span></span>
- <span data-ttu-id="07214-156">Gestire domini</span><span class="sxs-lookup"><span data-stu-id="07214-156">Manage domains</span></span>
- <span data-ttu-id="07214-157">Approvare le richieste di Customer Lockbox</span><span class="sxs-lookup"><span data-stu-id="07214-157">Approve Customer Lockbox requests</span></span>

<span data-ttu-id="07214-158">È consigliabile configurare almeno due account amministratore per ogni organizzazione.</span><span class="sxs-lookup"><span data-stu-id="07214-158">We recommend that each organization configure at least two admin accounts.</span></span> <span data-ttu-id="07214-159">Per le organizzazioni aziendali di grandi dimensioni, è consigliabile utilizzare account di amministratore specializzati che si servono di funzioni diverse.</span><span class="sxs-lookup"><span data-stu-id="07214-159">For large enterprise organizations, we recommend specialized admin accounts that serve different functions.</span></span>

<span data-ttu-id="07214-160">Per informazioni sull'assegnazione di ruoli e autorizzazioni di amministratore, vedere [Assegnare](/microsoft-365/admin/add-users/assign-admin-roles) ruoli di amministratore e [Informazioni sui ruoli di amministratore.](/microsoft-365/admin/add-users/about-admin-roles)</span><span class="sxs-lookup"><span data-stu-id="07214-160">For information about assigning admin roles and permissions, see [Assign admin roles](/microsoft-365/admin/add-users/assign-admin-roles) and [About admin roles](/microsoft-365/admin/add-users/about-admin-roles).</span></span>

## <a name="related-links"></a><span data-ttu-id="07214-161">Collegamenti correlati</span><span class="sxs-lookup"><span data-stu-id="07214-161">Related Links</span></span>

- [<span data-ttu-id="07214-162">Isolamento in Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="07214-162">Isolation in Microsoft 365</span></span>](assurance-isolation-in-microsoft-365.md)
- [<span data-ttu-id="07214-163">Screening precedente all'impiego presso Microsoft</span><span class="sxs-lookup"><span data-stu-id="07214-163">Microsoft pre-employment screening</span></span>](assurance-pre-employment-screening.md)
- [<span data-ttu-id="07214-164">Controllo in background di Microsoft Cloud</span><span class="sxs-lookup"><span data-stu-id="07214-164">Microsoft cloud background check</span></span>](assurance-cloud-background-check.md)
- [<span data-ttu-id="07214-165">Monitoraggio e controllo dei controlli di accesso </span><span class="sxs-lookup"><span data-stu-id="07214-165">Monitoring and Auditing Access Controls</span></span>](assurance-monitoring-and-auditing-access-controls.md)
- [<span data-ttu-id="07214-166">Controlli di accesso di Yammer Enterprise</span><span class="sxs-lookup"><span data-stu-id="07214-166">Yammer Enterprise Access Controls</span></span>](assurance-yammer-enterprise-access-controls.md)
