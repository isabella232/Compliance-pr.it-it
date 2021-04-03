---
title: Crittografia per i dati in transito
description: In questo articolo, trovare una breve spiegazione del modo in cui Microsoft crittografa i dati dei clienti di Microsoft 365 in transito.
ms.author: krowley
author: kccross
manager: laurawi
ms.reviewer: sosstah
f1.keywords:
- NOCSH
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: None
search.appverid:
- MET150
ms.collection:
- Strat_O365_Enterprise
- M365-security-compliance
- Strat_O365_Enterprise
- MS-Compliance
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 227f74140ecd9b6283b92e8b0e87bd70912ec8e3
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497256"
---
# <a name="encryption-for-data-in-transit"></a><span data-ttu-id="8a9cf-103">Crittografia per i dati in transito</span><span class="sxs-lookup"><span data-stu-id="8a9cf-103">Encryption for data-in-transit</span></span>

<span data-ttu-id="8a9cf-104">Oltre a proteggere i dati dei clienti in pausa, Microsoft usa tecnologie di crittografia per proteggere i dati dei clienti in transito.</span><span class="sxs-lookup"><span data-stu-id="8a9cf-104">In addition to protecting customer data at rest, Microsoft uses encryption technologies to protect customer data in transit.</span></span> <span data-ttu-id="8a9cf-105">I dati sono in transito:</span><span class="sxs-lookup"><span data-stu-id="8a9cf-105">Data is in transit:</span></span>

- <span data-ttu-id="8a9cf-106">quando un computer client comunica con un server Microsoft;</span><span class="sxs-lookup"><span data-stu-id="8a9cf-106">when a client machine communicates with a Microsoft server;</span></span>
- <span data-ttu-id="8a9cf-107">quando un server Microsoft comunica con un altro server Microsoft; e</span><span class="sxs-lookup"><span data-stu-id="8a9cf-107">when a Microsoft server communicates with another Microsoft server; and</span></span>
- <span data-ttu-id="8a9cf-108">quando un server Microsoft comunica con un server non Microsoft (ad esempio, Exchange Online che recapita la posta elettronica a un server di posta elettronica di terze parti).</span><span class="sxs-lookup"><span data-stu-id="8a9cf-108">when a Microsoft server communicates with a non-Microsoft server (for example, Exchange Online delivering email to a third-party email server).</span></span>

<span data-ttu-id="8a9cf-109">Le comunicazioni tra data center tra i server Microsoft si svolgono su TLS o IPsec e tutti i server rivolti ai clienti negoziano una sessione sicura utilizzando TLS con i computer client (ad esempio, Exchange Online usa TLS 1.2 con la forza di crittografia a 256 bit è usata (convalidato da FIPS 140-2 livello 2).</span><span class="sxs-lookup"><span data-stu-id="8a9cf-109">Inter-data center communications between Microsoft servers take place over TLS or IPsec, and all customer-facing servers negotiate a secure session using TLS with client machines (for example, Exchange Online uses TLS 1.2 with 256-bit cipher strength is used (FIPS 140-2 Level 2-validated).</span></span> <span data-ttu-id="8a9cf-110">Per un [elenco delle](/microsoft-365/compliance/technical-reference-details-about-encryption) suite di crittografia TLS supportate da Office 365, vedere Dettagli tecnici sulla crittografia. Questo vale per i protocolli utilizzati da client come Outlook, Skype for Business, Microsoft Teams e Outlook sul Web (ad esempio, HTTP, POP3 e così via).</span><span class="sxs-lookup"><span data-stu-id="8a9cf-110">(See [Technical reference details about encryption](/microsoft-365/compliance/technical-reference-details-about-encryption) for a list of TLS cipher suites supported by Office 365.) This applies to the protocols that are used by clients such as Outlook, Skype for Business, Microsoft Teams, and Outlook on the web (for example, HTTP, POP3, etc.).</span></span>

<span data-ttu-id="8a9cf-111">I certificati pubblici vengono emessi da MICROSOFT IT SSL utilizzando SSLAdmin, uno strumento Microsoft interno per proteggere la riservatezza delle informazioni trasmesse.</span><span class="sxs-lookup"><span data-stu-id="8a9cf-111">The public certificates are issued by Microsoft IT SSL using SSLAdmin, an internal Microsoft tool to protect confidentiality of transmitted information.</span></span> <span data-ttu-id="8a9cf-112">Tutti i certificati emessi da Microsoft IT hanno una lunghezza minima di 2048 bit e la conformità Webtrust richiede SSLAdmin per assicurarsi che i certificati siano emessi solo agli indirizzi IP pubblici di proprietà di Microsoft.</span><span class="sxs-lookup"><span data-stu-id="8a9cf-112">All certificates issued by Microsoft IT have a minimum of 2048 bits in length, and Webtrust compliance requires SSLAdmin to make sure that certificates are issued only to public IP addresses owned by Microsoft.</span></span> <span data-ttu-id="8a9cf-113">Tutti gli indirizzi IP che non soddisfano questo criterio vengono instradati attraverso un processo di eccezione.</span><span class="sxs-lookup"><span data-stu-id="8a9cf-113">Any IP addresses that fail to meet this criterion are routed through an exception process.</span></span>

<span data-ttu-id="8a9cf-114">Tutti i dettagli di implementazione, ad esempio la versione di TLS in uso, se Forward Secrecy (FS) è abilitato, l'ordine delle suite di crittografia e così via, sono disponibili pubblicamente.</span><span class="sxs-lookup"><span data-stu-id="8a9cf-114">All implementation details such as the version of TLS being used, whether Forward Secrecy (FS) is enabled, the order of cipher suites, etc., are available publicly.</span></span> <span data-ttu-id="8a9cf-115">Un modo per visualizzare questi dettagli è usare un sito Web di terze parti, ad esempio [Qualys SSL Labs.](https://www.ssllabs.com)</span><span class="sxs-lookup"><span data-stu-id="8a9cf-115">One way to see these details is to use a third-party website, such as [Qualys SSL Labs](https://www.ssllabs.com).</span></span> <span data-ttu-id="8a9cf-116">Di seguito sono riportati i collegamenti alle pagine di test automatizzate di Qualys che visualizzano informazioni per i servizi seguenti:</span><span class="sxs-lookup"><span data-stu-id="8a9cf-116">Below are the links to automated test pages from Qualys that display information for the following services:</span></span>

- [<span data-ttu-id="8a9cf-117">Portale di Office 365</span><span class="sxs-lookup"><span data-stu-id="8a9cf-117">Office 365 Portal</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=portal.office.com&hideResults=on)
- [<span data-ttu-id="8a9cf-118">Exchange Online</span><span class="sxs-lookup"><span data-stu-id="8a9cf-118">Exchange Online</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=outlook.office365.com&hideResults=on)
- [<span data-ttu-id="8a9cf-119">SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="8a9cf-119">SharePoint Online</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=microsoft-my.sharepoint.com&hideResults=on)
- [<span data-ttu-id="8a9cf-120">Skype for Business (SIP)</span><span class="sxs-lookup"><span data-stu-id="8a9cf-120">Skype for Business (SIP)</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=sipdir.online.lync.com)
- [<span data-ttu-id="8a9cf-121">Skype for Business (Web)</span><span class="sxs-lookup"><span data-stu-id="8a9cf-121">Skype for Business (Web)</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=webdir.online.lync.com&hideResults=on)
- [<span data-ttu-id="8a9cf-122">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="8a9cf-122">Exchange Online Protection</span></span>](https://ssl-tools.net/mailservers/microsoft-com.mail.protection.outlook.com)
- [<span data-ttu-id="8a9cf-123">Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="8a9cf-123">Microsoft Teams</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=teams.microsoft.com&latest)

<span data-ttu-id="8a9cf-124">Per Exchange Online Protection, gli URL variano in base ai nomi dei tenant. Tuttavia, tutti i clienti possono testare Microsoft 365 **usando microsoft-com.mail.protection.outlook.com**.</span><span class="sxs-lookup"><span data-stu-id="8a9cf-124">For Exchange Online Protection, URLs vary by tenant names; however, all customers can test Microsoft 365 using **microsoft-com.mail.protection.outlook.com**.</span></span>
