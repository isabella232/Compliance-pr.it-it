---
title: Controlli di accesso aziendale di Microsoft 365 Yammer
description: Questo articolo contiene un breve riepilogo dei controlli di accesso di Yammer Enterprise nell'ambiente di produzione.
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
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: 916f26d5f2defdfb21cb9babe3a64cf618e8cd4a
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120365"
---
# <a name="yammer-enterprise-access-controls"></a><span data-ttu-id="a89e5-103">Controlli di accesso aziendali di Yammer</span><span class="sxs-lookup"><span data-stu-id="a89e5-103">Yammer enterprise access controls</span></span> 

<span data-ttu-id="a89e5-104">L'accesso fisico e logico all'ambiente di produzione di Yammer è limitato a un piccolo gruppo di persone (infrastruttura e operazioni).</span><span class="sxs-lookup"><span data-stu-id="a89e5-104">Physical and logical access to the Yammer production environment is restricted to a small set of people (infrastructure and operations).</span></span> <span data-ttu-id="a89e5-105">Come per gli altri tecnici di Microsoft 365, i tecnici di Yammer non hanno accesso permanente ai dati dei clienti.</span><span class="sxs-lookup"><span data-stu-id="a89e5-105">As with other Microsoft 365 engineers, Yammer engineers have zero standing access to customer data.</span></span> <span data-ttu-id="a89e5-106">L'accesso deve essere richiesto utilizzando un sistema di controllo di accesso just-in-time basato sull'approvazione simile a Lockbox con un numero limitato di responsabili approvazione.</span><span class="sxs-lookup"><span data-stu-id="a89e5-106">Access must be requested using an approval-based just-in-time access control system similar to Lockbox with a limited number of approvers.</span></span> <span data-ttu-id="a89e5-107">I responsabili approvazione verificano la richiesta (ad esempio, verificano se la richiesta è legittima in base alle esigenze, al caso aziendale, al tempo e così via) e quindi approvano o negano la richiesta.</span><span class="sxs-lookup"><span data-stu-id="a89e5-107">Approvers verify the request (for example, they verify whether the request is legitimate based on need, business case, time, etc.), and then approve or deny the request.</span></span> <span data-ttu-id="a89e5-108">Se la richiesta viene approvata, l'accesso JIT viene concesso per un periodo di tempo definito e limitato.</span><span class="sxs-lookup"><span data-stu-id="a89e5-108">If the request is approved, JIT access is granted for a defined and limited time.</span></span> <span data-ttu-id="a89e5-109">Una volta superato il tempo di accesso, l'accesso scade automaticamente.</span><span class="sxs-lookup"><span data-stu-id="a89e5-109">After access time is exceeded, the access automatically expires.</span></span>

<span data-ttu-id="a89e5-110">Come per altri servizi di Microsoft 365, tutti gli accessi all'ambiente di produzione di Yammer utilizzano l'autenticazione a più fattori.</span><span class="sxs-lookup"><span data-stu-id="a89e5-110">As with other Microsoft 365 services, all access to the Yammer production environment uses multi-factor authentication.</span></span> <span data-ttu-id="a89e5-111">Tutti gli accessi e la cronologia dei comandi vengono attribuiti a un utente e registrati e esaminati regolarmente dal team di sicurezza di Yammer.</span><span class="sxs-lookup"><span data-stu-id="a89e5-111">All access and command history is attributed to a user, and logged and reviewed regularly by the Yammer security team.</span></span>

<span data-ttu-id="a89e5-112">Per ulteriori informazioni sull'amministrazione e la gestione di Yammer, vedere la Guida [per gli amministratori di Yammer.](/yammer/yammer-landing-page)</span><span class="sxs-lookup"><span data-stu-id="a89e5-112">For more information about Yammer administration and management, see [Yammer admin help](/yammer/yammer-landing-page).</span></span>