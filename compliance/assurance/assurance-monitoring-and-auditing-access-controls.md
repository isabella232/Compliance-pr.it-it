---
title: Monitoraggio e controllo dei controlli di accesso di Microsoft 365
description: 'Riepilogo: riepilogo dei vari controlli di accesso di monitoraggio e controllo disponibili in Microsoft 365.'
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
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: e9a9ea713afbf7568c1ae67d31a57dd9dce51fc3
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497537"
---
# <a name="monitoring-and-auditing-access-controls-in-microsoft-365"></a><span data-ttu-id="86ac5-103">Monitoraggio e controllo dei controlli di accesso in Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="86ac5-103">Monitoring and auditing access controls in Microsoft 365</span></span>

<span data-ttu-id="86ac5-104">Microsoft esegue un monitoraggio e un controllo approfonditi di tutte le operazioni, privilegi e delega che si verificano all'interno di Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="86ac5-104">Microsoft performs extensive monitoring and auditing of all delegation, privileges, and operations that occur within Microsoft 365.</span></span> <span data-ttu-id="86ac5-105">Il controllo di accesso di Microsoft 365 è un processo automatizzato basato sul principio dei privilegi minimi e che include controlli e controlli di accesso ai dati:</span><span class="sxs-lookup"><span data-stu-id="86ac5-105">Microsoft 365 access control is an automated process built on the principle of least privilege and incorporating data access controls and audits:</span></span>

- <span data-ttu-id="86ac5-106">Tutti gli accessi consentiti sono tracciabili a un utente univoco.</span><span class="sxs-lookup"><span data-stu-id="86ac5-106">All permitted access is traceable to a unique user.</span></span> <span data-ttu-id="86ac5-107">Gli amministratori sono responsabili della gestione dei contenuti dei clienti.</span><span class="sxs-lookup"><span data-stu-id="86ac5-107">Administrators are accountable for their handling of customer content.</span></span>
- <span data-ttu-id="86ac5-108">Le richieste di controllo di accesso, le approvazioni e i log delle operazioni amministrative vengono acquisiti per l'analisi della sicurezza e degli eventi dannosi.</span><span class="sxs-lookup"><span data-stu-id="86ac5-108">Access control requests, approvals, and administrative operations logs are captured for analysis of security and malicious events.</span></span>
- <span data-ttu-id="86ac5-109">I livelli di accesso vengono esaminati quasi in tempo reale in base all'appartenenza ai gruppi di sicurezza per garantire che solo gli utenti che hanno giustificazioni aziendali autorizzate e che soddisfano i requisiti di idoneità hanno accesso ai sistemi.</span><span class="sxs-lookup"><span data-stu-id="86ac5-109">Access levels are reviewed in near real-time based on security group membership to ensure that only users who have authorized business justifications and meet the eligibility requirements have access to the systems.</span></span>
- <span data-ttu-id="86ac5-110">Microsoft 365, i controlli di accesso e i servizi di supporto, tra cui Azure Active Directory e i datacenter fisici, vengono regolarmente controllati da terze parti indipendenti per la conformità con [ISO/IEC 27001,](https://www.microsoft.com/TrustCenter/Compliance/iso-iec-27001) [ISO/IEC 27018,](https://www.microsoft.com/TrustCenter/Compliance/iso-iec-27018) [SOC,](https://www.microsoft.com/TrustCenter/Compliance/SOC) [FedRAMP (Office 365)](https://www.microsoft.com/TrustCenter/Compliance/FedRAMP)e altri [standard.](https://www.microsoft.com/TrustCenter/Compliance?service=Office#Icons)</span><span class="sxs-lookup"><span data-stu-id="86ac5-110">Microsoft 365, its access controls, and supporting services, including Azure Active Directory and physical datacenters, are regularly audited by independent third-parties for compliance with [ISO/IEC 27001](https://www.microsoft.com/TrustCenter/Compliance/iso-iec-27001), [ISO/IEC 27018](https://www.microsoft.com/TrustCenter/Compliance/iso-iec-27018), [SOC](https://www.microsoft.com/TrustCenter/Compliance/SOC), [FedRAMP (Office 365)](https://www.microsoft.com/TrustCenter/Compliance/FedRAMP), and other [standards](https://www.microsoft.com/TrustCenter/Compliance?service=Office#Icons).</span></span>
- <span data-ttu-id="86ac5-111">I tecnici di Microsoft 365 devono tenere una formazione annuale sulla sicurezza, esaminare le procedure consigliate per l'accesso con privilegi elevati e accettare i criteri di sicurezza e privacy di Microsoft per mantenere i diritti al servizio.</span><span class="sxs-lookup"><span data-stu-id="86ac5-111">Microsoft 365 engineers must take yearly security training, review elevated access best procedures, and acknowledge Microsoft's security and privacy policies to maintain entitlements to the service.</span></span>

<span data-ttu-id="86ac5-112">Gli avvisi automatici vengono attivati quando vengono rilevate attività sospette, ad esempio più accessi non riusciti in un breve periodo.</span><span class="sxs-lookup"><span data-stu-id="86ac5-112">Automated alerts trigger when suspicious activity is detected, such as multiple failed logins within a short period.</span></span> <span data-ttu-id="86ac5-113">Il team di Microsoft 365 Security Response usa l'apprendimento automatico e l'analisi dei Big Data per esaminare e analizzare le attività, cercare modelli di accesso irregolare e rispondere in modo proattivo ad attività anomale e illecite.</span><span class="sxs-lookup"><span data-stu-id="86ac5-113">The Microsoft 365 Security Response team uses machine learning and big data analysis to review and analyze activity, look for irregular access patterns, and proactively respond to anomalous and illicit activities.</span></span> <span data-ttu-id="86ac5-114">Microsoft impiega anche un team dedicato di tester di penetrazione e si impegna in esercitazioni periodiche di Red Team e Blue Team per individuare i problemi di sicurezza e controllo degli accessi nel servizio.</span><span class="sxs-lookup"><span data-stu-id="86ac5-114">Microsoft also employs a dedicated team of penetration testers and engages in periodic Red Team and Blue Team exercises to find security and access control issues in the service.</span></span> <span data-ttu-id="86ac5-115">I clienti possono verificare l'efficacia dei sistemi di controllo di accesso usando i report di controllo e l'API di attività di gestione fornita da Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="86ac5-115">Customers can verify the effectiveness of access control systems by using audit reports and the management activity API provided by Microsoft 365.</span></span>

<span data-ttu-id="86ac5-116">Per ulteriori informazioni, vedere Informazioni di riferimento sulle API delle attività di gestione di [Office 365](/office/office-365-management-api/office-365-management-activity-api-reference) e Controllo e creazione di [report in Microsoft 365.](assurance-auditing-and-reporting-overview.md)</span><span class="sxs-lookup"><span data-stu-id="86ac5-116">For more information, see [Office 365 Management Activity API reference](/office/office-365-management-api/office-365-management-activity-api-reference) and [Auditing and reporting in Microsoft 365](assurance-auditing-and-reporting-overview.md).</span></span>
