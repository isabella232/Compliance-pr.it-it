---
title: Microsoft 365 registrazione interna per Microsoft 365 progettazione
description: In questo articolo viene fornita una spiegazione del funzionamento della registrazione interna per Microsoft 365 team di progettazione.
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
ms.openlocfilehash: 71b08509ae920ad88ecfa1566b9a11d640b0534f
ms.sourcegitcommit: fb379d1110a9a86c7f9bab8c484dc3f4b3dfd6f0
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/23/2021
ms.locfileid: "53088595"
---
# <a name="internal-logging-for-microsoft-365-engineering"></a><span data-ttu-id="aebde-103">Log interni per Microsoft 365 Engineering</span><span class="sxs-lookup"><span data-stu-id="aebde-103">Internal logging for Microsoft 365 engineering</span></span>

<span data-ttu-id="aebde-104">Oltre agli eventi e ai dati di registro disponibili per i clienti, Microsoft gestisce un sistema di raccolta dei dati di registro interno disponibile per Microsoft 365 tecnici.</span><span class="sxs-lookup"><span data-stu-id="aebde-104">In addition to the events and log data available for customers, Microsoft maintains an internal log data collection system that is available to Microsoft 365 engineers.</span></span> <span data-ttu-id="aebde-105">Molti tipi diversi di dati di registro vengono caricati dai server Microsoft 365 in una soluzione di monitoraggio della sicurezza proprietaria per l'analisi NRT (Near Real-Time) e un servizio di elaborazione dei big data (Cosmos) interno per l'archiviazione a lungo termine.</span><span class="sxs-lookup"><span data-stu-id="aebde-105">Many different types of log data are uploaded from Microsoft 365 servers to a proprietary security monitoring solution for near real-time (NRT) analysis and an internal, big data computing service (Cosmos) for long-term storage.</span></span> <span data-ttu-id="aebde-106">Questo trasferimento dei dati avviene tramite una connessione TLS convalidata da FIPS 140-2 su porte e protocolli approvati utilizzando uno strumento di automazione proprietario denominato Office Data Loader (ODL).</span><span class="sxs-lookup"><span data-stu-id="aebde-106">This data transfer occurs over a FIPS 140-2-validated TLS connection on approved ports and protocols using a proprietary automation tool called the Office Data Loader (ODL).</span></span> <span data-ttu-id="aebde-107">Gli strumenti utilizzati in Microsoft 365 per raccogliere ed elaborare i record di controllo non consentono modifiche permanenti o irreversibili al contenuto del record di controllo originale o all'ordinamento temporale.</span><span class="sxs-lookup"><span data-stu-id="aebde-107">The tools used in Microsoft 365 to collect and process audit records do not allow permanent or irreversible changes to the original audit record content or time ordering.</span></span>

<span data-ttu-id="aebde-108">I team di servizio utilizzano Cosmos come archivio centralizzato per eseguire un'analisi dell'utilizzo delle applicazioni, per misurare le prestazioni del sistema e delle operazioni e per cercare anomalie e modelli che potrebbero indicare problemi o problemi di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="aebde-108">Service teams use Cosmos as a centralized repository to conduct an analysis of application usage, to measure system and operational performance, and to look for abnormalities and patterns that may indicate problems or security issues.</span></span> <span data-ttu-id="aebde-109">Ogni team del servizio carica una linea di base che include:</span><span class="sxs-lookup"><span data-stu-id="aebde-109">Each service team uploads a baseline that includes:</span></span>

- <span data-ttu-id="aebde-110">Registri eventi</span><span class="sxs-lookup"><span data-stu-id="aebde-110">Event logs</span></span>
- <span data-ttu-id="aebde-111">Log di AppLocker</span><span class="sxs-lookup"><span data-stu-id="aebde-111">AppLocker logs</span></span>
- <span data-ttu-id="aebde-112">Dati sulle prestazioni</span><span class="sxs-lookup"><span data-stu-id="aebde-112">Performance data</span></span>
- <span data-ttu-id="aebde-113">System Center dati</span><span class="sxs-lookup"><span data-stu-id="aebde-113">System Center data</span></span>
- <span data-ttu-id="aebde-114">Record dettagli chiamata</span><span class="sxs-lookup"><span data-stu-id="aebde-114">Call detail records</span></span>
- <span data-ttu-id="aebde-115">Dati sulla qualità dell'esperienza</span><span class="sxs-lookup"><span data-stu-id="aebde-115">Quality of experience data</span></span>
- <span data-ttu-id="aebde-116">Registri del server Web IIS</span><span class="sxs-lookup"><span data-stu-id="aebde-116">IIS Web Server logs</span></span>
- <span data-ttu-id="aebde-117">SQL Server log</span><span class="sxs-lookup"><span data-stu-id="aebde-117">SQL Server logs</span></span>
- <span data-ttu-id="aebde-118">Dati Syslog</span><span class="sxs-lookup"><span data-stu-id="aebde-118">Syslog data</span></span>
- <span data-ttu-id="aebde-119">Log di controllo della sicurezza</span><span class="sxs-lookup"><span data-stu-id="aebde-119">Security audit logs</span></span>

<span data-ttu-id="aebde-120">Prima del caricamento, l'applicazione ODL utilizza un servizio di scrubbing per rimuovere tutti i campi che contengono i dati dei clienti, ad esempio le informazioni sul tenant e le informazioni identificabili dall'utente finale, e sostituire tali campi con un valore hash.</span><span class="sxs-lookup"><span data-stu-id="aebde-120">Prior to uploading, the ODL application uses a scrubbing service to remove any fields that contain customer data, such as tenant information and end-user identifiable information, and replace those fields with a hash value.</span></span> <span data-ttu-id="aebde-121">I log scrubbed vengono caricati in Cosmos e nella soluzione di monitoraggio della sicurezza NRT che analizza i registri alla ricerca di potenziali eventi di sicurezza e indicatori di prestazioni.</span><span class="sxs-lookup"><span data-stu-id="aebde-121">The scrubbed logs are uploaded to Cosmos and to the NRT security monitoring solution that analyzes the logs for potential security events and performance indicators.</span></span> <span data-ttu-id="aebde-122">Il periodo di conservazione dei dati del log di controllo Cosmos è determinato dai team del servizio; la maggior parte dei dati del log di controllo viene conservata per 90 giorni o più per supportare le indagini degli incidenti di sicurezza e per soddisfare i requisiti di conservazione normativi.</span><span class="sxs-lookup"><span data-stu-id="aebde-122">The period of audit log data retention in Cosmos is determined by the service teams; most audit log data is retained for 90 days or longer to support security incident investigations and to meet regulatory retention requirements.</span></span>

<span data-ttu-id="aebde-123">L'accesso Microsoft 365 dati archiviati in Cosmos è limitato al personale autorizzato.</span><span class="sxs-lookup"><span data-stu-id="aebde-123">Access to Microsoft 365 data stored in Cosmos is restricted to authorized personnel.</span></span> <span data-ttu-id="aebde-124">Microsoft limita la gestione dei log di controllo a un sottoinsieme limitato di membri del team di sicurezza responsabili della funzionalità di controllo.</span><span class="sxs-lookup"><span data-stu-id="aebde-124">Microsoft restricts the management of audit logs to a limited subset of Security Team members responsible for audit functionality.</span></span> <span data-ttu-id="aebde-125">Il team di sicurezza non dispone dell'accesso amministrativo permanente Cosmos e tutte le modifiche vengono registrate e verificate.</span><span class="sxs-lookup"><span data-stu-id="aebde-125">The Security Team does not have standing administrative access to Cosmos, and all changes are recorded and audited.</span></span>

<span data-ttu-id="aebde-126">Dopo l'analisi NRT, ogni team del servizio può utilizzare strumenti di analisi e dashboard per la correlazione dei dati, le query interattive e l'analisi dei dati.</span><span class="sxs-lookup"><span data-stu-id="aebde-126">After NRT analysis, each service team can use analysis tools and dashboards for data correlation, interactive queries, and data analytics.</span></span> <span data-ttu-id="aebde-127">Questi report vengono utilizzati per monitorare e migliorare le prestazioni complessive del servizio.</span><span class="sxs-lookup"><span data-stu-id="aebde-127">These reports are used to monitor and improve the overall performance of the service.</span></span>
