---
title: Limiti delle risorse di Microsoft 365
description: In questo articolo sono disponibili informazioni sui limiti delle risorse per le varie applicazioni in Microsoft 365.
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
hideEdit: true
ms.openlocfilehash: 54ea001e542cdd1ab078546cf96bd011e27ab1dc
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497503"
---
# <a name="service-resource-limits"></a><span data-ttu-id="397cc-103">Limiti della risorsa servizio</span><span class="sxs-lookup"><span data-stu-id="397cc-103">Service resource limits</span></span>

<span data-ttu-id="397cc-104">I limiti delle risorse vengono applicati utilizzando quote (limiti) e limitazione.</span><span class="sxs-lookup"><span data-stu-id="397cc-104">Resource limits are enforced using quotas (limits) and throttling.</span></span> <span data-ttu-id="397cc-105">Azure Active Directory (Azure AD) e i singoli servizi di Microsoft 365 usano entrambi.</span><span class="sxs-lookup"><span data-stu-id="397cc-105">Azure Active Directory (Azure AD) and the individual Microsoft 365 services use both.</span></span> <span data-ttu-id="397cc-106">I limiti sono specifici del servizio e cambiano nel tempo quando vengono aggiunte nuove funzionalità.</span><span class="sxs-lookup"><span data-stu-id="397cc-106">Limits are service-specific and change over time as new capabilities are added.</span></span> <span data-ttu-id="397cc-107">Per informazioni dettagliate sui limiti correnti per i vari servizi, vedere i seguenti argomenti:</span><span class="sxs-lookup"><span data-stu-id="397cc-107">For details on the current limits for the various services, see the following topics:</span></span>

- [<span data-ttu-id="397cc-108">Limiti e restrizioni del servizio Azure AD</span><span class="sxs-lookup"><span data-stu-id="397cc-108">Azure AD service limits and restrictions</span></span>](/azure/azure-resource-manager/management/azure-subscription-service-limits)
- [<span data-ttu-id="397cc-109">Limiti di Exchange Online</span><span class="sxs-lookup"><span data-stu-id="397cc-109">Exchange Online Limits</span></span>](/office365/servicedescriptions/exchange-online-service-description/exchange-online-limits)
- [<span data-ttu-id="397cc-110">Limiti software e limiti di SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="397cc-110">SharePoint Online software boundaries and limits</span></span>](https://support.office.com/article/SharePoint-Online-software-boundaries-and-limits-8F34FF47-B749-408B-ABC0-B605E1F6D498)
- [<span data-ttu-id="397cc-111">Limiti di Skype for Business</span><span class="sxs-lookup"><span data-stu-id="397cc-111">Skype for Business Limits</span></span>](https://technet.microsoft.com/library/skype-for-business-online-limits.aspx)
- [<span data-ttu-id="397cc-112">API REST di Yammer e limiti di frequenza</span><span class="sxs-lookup"><span data-stu-id="397cc-112">Yammer REST API and Rate Limits</span></span>](https://developer.yammer.com/docs/rest-api-rate-limits)
- [<span data-ttu-id="397cc-113">Limiti delle dimensioni dei file in Sway</span><span class="sxs-lookup"><span data-stu-id="397cc-113">File Size Limits in Sway</span></span>](https://support.office.com/article/File-size-limits-in-Sway-4db21bc6-b42b-499f-9272-66e089db109f)

<span data-ttu-id="397cc-114">Oltre a questi limiti, in Azure AD e Microsoft 365 vengono utilizzati diversi meccanismi di limitazione.</span><span class="sxs-lookup"><span data-stu-id="397cc-114">In addition to these limits, several throttling mechanisms are used throughout Azure AD and Microsoft 365.</span></span> <span data-ttu-id="397cc-115">La limitazione all'interno del servizio è particolarmente importante, dato che le risorse di rete nei data center di Microsoft sono ottimizzate per l'ampio set di clienti che usano i servizi.</span><span class="sxs-lookup"><span data-stu-id="397cc-115">Throttling within the service is especially important, given that network resources in Microsoft's datacenters are optimized for the broad set of customers that use the services.</span></span> <span data-ttu-id="397cc-116">I meccanismi di limitazione includono:</span><span class="sxs-lookup"><span data-stu-id="397cc-116">Throttling mechanisms include:</span></span>

- <span data-ttu-id="397cc-117">Azure AD e Microsoft 365 presentano limitazioni a livello di utente, che limitano il numero di transazioni o chiamate simultanee (tramite script o codice) che possono essere eseguite da un singolo utente.</span><span class="sxs-lookup"><span data-stu-id="397cc-117">Azure AD and Microsoft 365 feature user-level throttling, which limit the number of transactions or concurrent calls (by script or code) that can be performed by a single user.</span></span>
- <span data-ttu-id="397cc-118">Un criterio di limitazione di PowerShell predefinito viene assegnato a ogni tenant durante la creazione del tenant.</span><span class="sxs-lookup"><span data-stu-id="397cc-118">A default PowerShell throttling policy is assigned to each tenant at tenant creation.</span></span> <span data-ttu-id="397cc-119">Queste impostazioni influiscono su altri elementi, ad esempio il numero massimo di sessioni di PowerShell simultanee che possono essere aperte da un singolo amministratore.</span><span class="sxs-lookup"><span data-stu-id="397cc-119">These settings affect other items, such as the maximum number of simultaneous PowerShell sessions that can be opened by a single administrator.</span></span>
- <span data-ttu-id="397cc-120">Ogni cliente di Exchange Online dispone di un criterio EWS (Exchange Web Services) predefinito ottimizzato per le operazioni dei client EWS e di limitazione che si applica a tutti i client Outlook.</span><span class="sxs-lookup"><span data-stu-id="397cc-120">Each Exchange Online customer has a default Exchange Web Services (EWS) policy that is tuned for EWS client operations, and throttling that applies to all Outlook clients.</span></span>
