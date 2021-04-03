---
title: Microsoft 365 Che si occupa del danneggiamento dei dati
description: Questo articolo illustra il danneggiamento dei dati in Microsoft 365 e gli sforzi intrapresi da Microsoft per prevenire e ripristinare i dati.
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
ms.openlocfilehash: 9e9f0951f7e349cc70bc96bb6a2d62275848cf04
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497588"
---
# <a name="dealing-with-data-corruption-in-microsoft-365"></a><span data-ttu-id="283f7-103">Gestione del danneggiamento dei dati in Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="283f7-103">Dealing with data corruption in Microsoft 365</span></span>

<span data-ttu-id="283f7-104">Uno degli aspetti più impegnativi dell'esecuzione di un servizio cloud su larga scala è come gestire il danneggiamento dei dati, dato l'elevato volume di dati e sistemi indipendenti.</span><span class="sxs-lookup"><span data-stu-id="283f7-104">One of the challenging aspects of running a large-scale cloud service is how to handle data corruption, given the large volume of data and independent systems.</span></span> <span data-ttu-id="283f7-105">Il danneggiamento dei dati può essere causato da:</span><span class="sxs-lookup"><span data-stu-id="283f7-105">Data corruption can be caused by:</span></span>

- <span data-ttu-id="283f7-106">Bug dell'applicazione o dell'infrastruttura, danneggiando parte o tutto lo stato dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="283f7-106">Application or infrastructure bugs, corrupting some or all of the application state</span></span>
- <span data-ttu-id="283f7-107">Problemi hardware che causano la perdita di dati o l'impossibilità di leggere i dati</span><span class="sxs-lookup"><span data-stu-id="283f7-107">Hardware issues that result in lost data or an inability to read data</span></span>
- <span data-ttu-id="283f7-108">Errori operativi umani</span><span class="sxs-lookup"><span data-stu-id="283f7-108">Human operational errors</span></span>
- <span data-ttu-id="283f7-109">Hacker dannosi e dipendenti scontenti</span><span class="sxs-lookup"><span data-stu-id="283f7-109">Malicious hackers and disgruntled employees</span></span>
- <span data-ttu-id="283f7-110">Eventi imprevisti in servizi esterni che comportano la perdita di dati</span><span class="sxs-lookup"><span data-stu-id="283f7-110">Incidents in external services that result in some loss of data</span></span>

<span data-ttu-id="283f7-111">Poiché una maggiore resilienza nell'integrità dei dati significa un minor numero di incidenti di danneggiamento dei dati, Microsoft ha integrato i meccanismi di protezione di Microsoft 365 per impedire il danneggiamento, nonché sistemi e processi che ci consentono di recuperare i dati in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="283f7-111">Because greater resiliency in data integrity means fewer data corruption incidents, Microsoft has built into Microsoft 365 protection mechanisms to prevent corruption from happening, as well as systems and processes that enable us to recover data if it does.</span></span> <span data-ttu-id="283f7-112">I controlli e i processi sono presenti nelle varie fasi del processo di rilascio della progettazione per aumentare la resilienza contro il danneggiamento dei dati, tra cui:</span><span class="sxs-lookup"><span data-stu-id="283f7-112">Checks and processes exist within the various stages of the engineering release process to increase resiliency against data corruption, including:</span></span>

- <span data-ttu-id="283f7-113">Progettazione del sistema</span><span class="sxs-lookup"><span data-stu-id="283f7-113">System Design</span></span>
- <span data-ttu-id="283f7-114">Organizzazione e struttura del codice</span><span class="sxs-lookup"><span data-stu-id="283f7-114">Code organization and structure</span></span>
- <span data-ttu-id="283f7-115">Revisione del codice</span><span class="sxs-lookup"><span data-stu-id="283f7-115">Code review</span></span>
- <span data-ttu-id="283f7-116">Unit test, test di integrazione e test di sistema</span><span class="sxs-lookup"><span data-stu-id="283f7-116">Unit tests, integration tests, and system tests</span></span>
- <span data-ttu-id="283f7-117">Test/cancelli dei cavi di viaggio</span><span class="sxs-lookup"><span data-stu-id="283f7-117">Trip wires tests/gates</span></span>

<span data-ttu-id="283f7-118">All'interno degli ambienti di produzione di Microsoft 365, la replica peer tra datacenter garantisce che siano sempre presenti più copie in tempo reale di tutti i dati.</span><span class="sxs-lookup"><span data-stu-id="283f7-118">Within Microsoft 365 production environments, peer replication between datacenters ensures that there are always multiple live copies of any data.</span></span> <span data-ttu-id="283f7-119">Le immagini e gli script standard vengono utilizzati per ripristinare i server persi e i dati replicati vengono utilizzati per ripristinare i dati dei clienti.</span><span class="sxs-lookup"><span data-stu-id="283f7-119">Standard images and scripts are used to recover lost servers, and replicated data is used to restore customer data.</span></span> <span data-ttu-id="283f7-120">A causa dei controlli e dei processi di resilienza dei dati incorporati, Microsoft gestisce i backup solo della documentazione del sistema di informazioni di Microsoft 365 (inclusa la documentazione relativa alla sicurezza), utilizzando la replica incorporata in SharePoint Online e il nostro strumento di repository di codice interno, Source Depot.</span><span class="sxs-lookup"><span data-stu-id="283f7-120">Because of the built-in data resiliency checks and processes, Microsoft maintains backups only of Microsoft 365 information system documentation (including security-related documentation), using built-in replication in SharePoint Online and our internal code repository tool, Source Depot.</span></span> <span data-ttu-id="283f7-121">La documentazione di sistema è archiviata in SharePoint Online e Source Depot contiene immagini di sistema e applicazioni.</span><span class="sxs-lookup"><span data-stu-id="283f7-121">System documentation is stored in SharePoint Online, and Source Depot contains system and application images.</span></span> <span data-ttu-id="283f7-122">Sia SharePoint Online che Source Depot usano il controllo delle versioni e vengono replicati quasi in tempo reale.</span><span class="sxs-lookup"><span data-stu-id="283f7-122">Both SharePoint Online and Source Depot use versioning and are replicated in near real time.</span></span>
