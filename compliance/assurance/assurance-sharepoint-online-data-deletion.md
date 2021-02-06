---
title: Eliminazione dei dati di Microsoft 365 SharePoint Online
description: Informazioni sul funzionamento dell'eliminazione dei dati in SharePoint Online, ad esempio dove è archiviato il contenuto eliminato e per quanto tempo.
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
- SPO_Content
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: 89281b32dbc577f935224396fd358ed753348ea1
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120745"
---
# <a name="sharepoint-online-data-deletion-in-microsoft-365"></a><span data-ttu-id="ee614-103">Eliminazione dei dati di SharePoint Online in Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="ee614-103">SharePoint Online data deletion in Microsoft 365</span></span>

<span data-ttu-id="ee614-104">SharePoint Online archivia gli oggetti come codice astratto all'interno dei database dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ee614-104">SharePoint Online stores objects as abstracted code within application databases.</span></span> <span data-ttu-id="ee614-105">Quando un utente carica un file in SharePoint Online, tale file viene disassemblato e convertito nel codice dell'applicazione e archiviato in più tabelle in più database.</span><span class="sxs-lookup"><span data-stu-id="ee614-105">When a user uploads a file to SharePoint Online, that file is disassembled and translated into application code and stored in multiple tables across multiple databases.</span></span> <span data-ttu-id="ee614-106">In SharePoint Online, tutto il contenuto caricato da un cliente è suddiviso in blocchi, crittografato (potenzialmente con più chiavi AES a 256 bit) e distribuito nel datacenter.</span><span class="sxs-lookup"><span data-stu-id="ee614-106">In SharePoint Online, all content that a customer uploads is broken into chunks, encrypted (potentially with multiple AES 256-bit keys), and distributed across the datacenter.</span></span> <span data-ttu-id="ee614-107">Per informazioni dettagliate sul processo di crittografia e suddivisione in blocchi, vedere [Crittografia in Microsoft Cloud.](/microsoft-365/compliance/office-365-encryption-in-the-microsoft-cloud-overview)</span><span class="sxs-lookup"><span data-stu-id="ee614-107">For specific details about the chunking and encryption process, see [Encryption in the Microsoft Cloud](/microsoft-365/compliance/office-365-encryption-in-the-microsoft-cloud-overview).</span></span> 

<span data-ttu-id="ee614-108">In SharePoint Online, gli elementi vengono conservati per 93 giorni dal momento in cui vengono eliminati dalla posizione originale.</span><span class="sxs-lookup"><span data-stu-id="ee614-108">In SharePoint Online, items are retained for 93 days from the time you delete them from their original location.</span></span> <span data-ttu-id="ee614-109">Rimangono nel Cestino del sito per l'intero periodo, a meno che non vengano eliminati da tale cestino o svuotati.</span><span class="sxs-lookup"><span data-stu-id="ee614-109">They stay in the site Recycle Bin the entire time, unless someone deletes them from there or empties that Recycle Bin.</span></span> <span data-ttu-id="ee614-110">In tal caso, gli elementi vengono visualizzati nel Cestino della raccolta siti, dove rimangono per il resto dei 93 giorni.</span><span class="sxs-lookup"><span data-stu-id="ee614-110">In that case, the items go to the site collection Recycle Bin, where they stay for the remainder of the 93 days.</span></span> <span data-ttu-id="ee614-111">Per informazioni sul ripristino degli elementi eliminati, vedere [Restore items in the Recycle Bin of a SharePoint site](https://support.office.com/article/6df466b6-55f2-4898-8d6e-c0dff851a0be#ID0EAADAAA=Online
) and Restore deleted items from the site collection recycle [bin.](https://support.office.com/article/5fa924ee-16d7-487b-9a0a-021b9062d14b)</span><span class="sxs-lookup"><span data-stu-id="ee614-111">For info about restoring deleted items, see [Restore items in the Recycle Bin of a SharePoint site](https://support.office.com/article/6df466b6-55f2-4898-8d6e-c0dff851a0be#ID0EAADAAA=Online
) and [Restore deleted items from the site collection recycle bin](https://support.office.com/article/5fa924ee-16d7-487b-9a0a-021b9062d14b).</span></span> <span data-ttu-id="ee614-112">Il tempo di conservazione del Cestino non è configurabile in SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="ee614-112">The Recycle Bin retention time is not configurable in SharePoint Online.</span></span>

<span data-ttu-id="ee614-113">Quando si elimina una raccolta siti, si elimina anche la gerarchia dei siti della raccolta e tutto il contenuto al suo interno:</span><span class="sxs-lookup"><span data-stu-id="ee614-113">When you delete a site collection, you're also deleting the hierarchy of sites in the collection, and all content within them:</span></span>

- <span data-ttu-id="ee614-114">Documenti e raccolte documenti</span><span class="sxs-lookup"><span data-stu-id="ee614-114">Documents and document libraries</span></span>
- <span data-ttu-id="ee614-115">Elenchi e dati elenco</span><span class="sxs-lookup"><span data-stu-id="ee614-115">Lists and list data</span></span>
- <span data-ttu-id="ee614-116">Impostazioni di configurazione del sito</span><span class="sxs-lookup"><span data-stu-id="ee614-116">Site configuration settings</span></span>
- <span data-ttu-id="ee614-117">Informazioni sui ruoli e sulla sicurezza correlate al sito o ai relativi siti secondari</span><span class="sxs-lookup"><span data-stu-id="ee614-117">Role and security information that is related to the site or its subsites</span></span>
- <span data-ttu-id="ee614-118">Siti secondari del sito Web principale, relativi contenuti e informazioni utente</span><span class="sxs-lookup"><span data-stu-id="ee614-118">Subsites of the top-level website, their contents, and user information</span></span>

<span data-ttu-id="ee614-119">Se si elimina accidentalmente una raccolta siti, può essere ripristinata da un amministratore globale o di SharePoint tramite l'interfaccia di amministrazione di SharePoint.</span><span class="sxs-lookup"><span data-stu-id="ee614-119">If you accidentally delete a site collection, it can be restored by a global or SharePoint admin using the SharePoint admin center.</span></span>

<span data-ttu-id="ee614-120">Le raccolte siti eliminate vengono conservate per 93 giorni.</span><span class="sxs-lookup"><span data-stu-id="ee614-120">Deleted site collections are retained for 93 days.</span></span> <span data-ttu-id="ee614-121">Dopo 93 giorni, i siti e tutto il relativo contenuto e le impostazioni vengono eliminati definitivamente, inclusi elenchi, raccolte, pagine e siti secondari.</span><span class="sxs-lookup"><span data-stu-id="ee614-121">After 93 days, sites and all their content and settings are permanently deleted, including lists, libraries, pages, and any subsites.</span></span>

<span data-ttu-id="ee614-122">L'eliminazione definitiva si verifica quando un utente elimina gli elementi eliminati dal Cestino della raccolta siti, quando scadono i periodi di conservazione e backup o quando un amministratore elimina definitivamente una raccolta siti utilizzando il [cmdlet Remove-SPODeletedSite.](/powershell/module/sharepoint-online/remove-spodeletedsite)</span><span class="sxs-lookup"><span data-stu-id="ee614-122">Hard deletion occurs when a user purges deleted items from the site collection Recycle Bin, when the retention and backup periods expire, or when an administrator permanently deletes a site collection using the [Remove-SPODeletedSite cmdlet](/powershell/module/sharepoint-online/remove-spodeletedsite).</span></span> <span data-ttu-id="ee614-123">Quando un utente elimina definitivamente il contenuto (elimina o elimina definitivamente) da SharePoint Online, vengono eliminate anche tutte le chiavi di crittografia per i blocchi eliminati.</span><span class="sxs-lookup"><span data-stu-id="ee614-123">When a user hard deletes (permanently deletes, or purges) content from SharePoint Online, all encryption keys for the deleted chunks are also deleted.</span></span> <span data-ttu-id="ee614-124">I blocchi nei dischi in cui erano archiviati in precedenza i blocchi eliminati sono contrassegnati come inutilizzati e disponibili per il nuovo utilizzo.</span><span class="sxs-lookup"><span data-stu-id="ee614-124">The blocks on the disks that previously stored the deleted chunks are marked as unused and available for re-use.</span></span>
