---
title: 'Gestione degli incidenti di sicurezza di Microsoft 365: attività post-incidente'
description: Questo articolo fornisce una panoramica del processo di attività post-incidente di gestione degli incidenti di sicurezza in Microsoft 365.
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
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: 66c25503ac574de512f5201981112a0e54714968
ms.sourcegitcommit: 2973d25e9e0185b84d281f963553a332eac1c1a3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/28/2021
ms.locfileid: "50040349"
---
# <a name="microsoft-365-security-incident-management-post-incident-activity"></a><span data-ttu-id="1dbbe-103">Gestione degli incidenti di sicurezza di Microsoft 365: attività post-incidente</span><span class="sxs-lookup"><span data-stu-id="1dbbe-103">Microsoft 365 security incident management: Post-incident activity</span></span>

## <a name="postmortem"></a><span data-ttu-id="1dbbe-104">Postmortem</span><span class="sxs-lookup"><span data-stu-id="1dbbe-104">Postmortem</span></span>

<span data-ttu-id="1dbbe-105">Alcuni incidenti di sicurezza, in particolare quelli che hanno un impatto sul cliente o che causano una violazione dei dati, sono soggetti a un incidente completo post-mortem.</span><span class="sxs-lookup"><span data-stu-id="1dbbe-105">Some security incidents, especially those incidents that are customer impacting or result in a data breach, are subject to a full incident postmortem.</span></span> <span data-ttu-id="1dbbe-106">Il team di Microsoft 365 Security Response esegue un postmortem dettagliato con tutte le parti coinvolte nella risposta agli incidenti di sicurezza a:</span><span class="sxs-lookup"><span data-stu-id="1dbbe-106">The Microsoft 365 Security Response team conducts a detailed postmortem with all the parties involved in security incident response to:</span></span>

- <span data-ttu-id="1dbbe-107">Documentare la sequenza di eventi che hanno causato l'incidente</span><span class="sxs-lookup"><span data-stu-id="1dbbe-107">Document the sequence of events that caused the incident</span></span>
- <span data-ttu-id="1dbbe-108">Creare un riepilogo tecnico dell'incidente come supportato dalle prove che includono gli interessati coinvolti nella violazione (se noto).</span><span class="sxs-lookup"><span data-stu-id="1dbbe-108">Create a technical summary of the incident as supported by the evidence that includes the actors involved in the breach (if known).</span></span> <span data-ttu-id="1dbbe-109">Questo riepilogo includerà la modalità di esecuzione della risposta e altri elementi chiave da prendere.</span><span class="sxs-lookup"><span data-stu-id="1dbbe-109">This summary will include how the response was executed and other key takeaways.</span></span>
- <span data-ttu-id="1dbbe-110">Identificare gli insuccessi tecnici, gli errori procedurali, gli errori manuali, i difetti dei processi e glitch di comunicazione e/o eventuali vettori di attacco precedentemente sconosciuti identificati durante la risposta agli incidenti di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="1dbbe-110">Identify technical lapses, procedural failures, manual errors, process flaws, and communication glitches, and/or any previously unknown attack vectors that were identified during the security incident response.</span></span>

<span data-ttu-id="1dbbe-111">Il postmortem influenzerà direttamente il miglioramento dei servizi di Microsoft 365, i processi operativi e la documentazione impostando nuove priorità nel ciclo di sviluppo di progettazione di Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="1dbbe-111">The postmortem will directly influence Microsoft 365 service improvement, operational processes, and documentation by setting new priorities in the Microsoft 365 engineering development cycle.</span></span>

## <a name="documentation"></a><span data-ttu-id="1dbbe-112">Documentazione</span><span class="sxs-lookup"><span data-stu-id="1dbbe-112">Documentation</span></span>

<span data-ttu-id="1dbbe-113">Tutti i principali risultati tecnici del processo post-mortem vengono acquisiti in un report e gli investimenti o le correzioni dei servizi sotto forma di bug o richieste di modifica allo sviluppo.</span><span class="sxs-lookup"><span data-stu-id="1dbbe-113">All key technical findings in the postmortem process are captured in a report and service investments or fixes in the form of bugs or development change requests.</span></span> <span data-ttu-id="1dbbe-114">Questi risultati vengono seguiti con i team di progettazione appropriati.</span><span class="sxs-lookup"><span data-stu-id="1dbbe-114">These findings are followed-up with the appropriate engineering teams.</span></span> <span data-ttu-id="1dbbe-115">Per gli errori di processo e i problemi tra le organizzazione, i problemi sono documentati nel database del team di Microsoft 365 Security Response e seguiti con i gruppi appropriati per risolvere i problemi.</span><span class="sxs-lookup"><span data-stu-id="1dbbe-115">For process failures and cross-organizational issues, issues are documented in the Microsoft 365 Security Response team's database and followed-up with the appropriate groups to address them.</span></span>

## <a name="process-improvement"></a><span data-ttu-id="1dbbe-116">Miglioramento dei processi</span><span class="sxs-lookup"><span data-stu-id="1dbbe-116">Process improvement</span></span>

<span data-ttu-id="1dbbe-117">Rispondere a un incidente di sicurezza in Microsoft 365 implica il coordinamento con più gruppi distribuiti tra organizzazioni diverse all'interno di Microsoft e organizzazioni esterne potenzialmente appropriate, come le forze dell'ordine.</span><span class="sxs-lookup"><span data-stu-id="1dbbe-117">Responding to a security incident in Microsoft 365 involves coordination with multiple groups spread across different organizations within Microsoft, and potentially even appropriate external organizations such as law enforcement.</span></span> <span data-ttu-id="1dbbe-118">Sappiamo che è fondamentale valutare le risposte dopo ogni incidente di sicurezza sia per la sufficienza che per la completezza.</span><span class="sxs-lookup"><span data-stu-id="1dbbe-118">We know that it is critical to evaluate our responses after every security incident for both sufficiency and completeness.</span></span> <span data-ttu-id="1dbbe-119">Per eventuali miglioramenti o modifiche identificati, il team di Microsoft 365 Security Response valuta i suggerimenti in consultazione con i team e gli stakeholder appropriati e, se appropriato, li incorpora nelle procedure operative standard.</span><span class="sxs-lookup"><span data-stu-id="1dbbe-119">For any identified improvements or changes, the Microsoft 365 Security Response team evaluates the suggestions in consultation with the appropriate teams and stakeholders, and where appropriate incorporates them into standard operating procedures.</span></span> <span data-ttu-id="1dbbe-120">Tutte le modifiche, i bug o i miglioramenti del servizio necessari identificati durante la risposta a un evento imprevisto di sicurezza o l'attività post-disaggregata vengono registrati e registrati in un database di progettazione interno di Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="1dbbe-120">All required changes, bugs, or service improvements identified during the security incident response or postmortem activity are logged and tracked in an internal Microsoft 365 engineering database.</span></span> <span data-ttu-id="1dbbe-121">Tutti i potenziali bug o funzionalità vengono assegnati al proprietario appropriato.</span><span class="sxs-lookup"><span data-stu-id="1dbbe-121">All potential bugs or features are assigned to the appropriate owner.</span></span> <span data-ttu-id="1dbbe-122">Il team di Microsoft 365 Security Response esamina tutte le voci finché il problema non viene risolto.</span><span class="sxs-lookup"><span data-stu-id="1dbbe-122">The Microsoft 365 Security Response team reviews all entries until the issue is resolved.</span></span>

## <a name="related-articles"></a><span data-ttu-id="1dbbe-123">Articoli correlati</span><span class="sxs-lookup"><span data-stu-id="1dbbe-123">Related articles</span></span>

- [<span data-ttu-id="1dbbe-124">Gestione degli incidenti di sicurezza di Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="1dbbe-124">Microsoft 365 security incident management</span></span>](assurance-security-incident-management.md)
- [<span data-ttu-id="1dbbe-125">Preparazione della gestione degli incidenti di sicurezza di Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="1dbbe-125">Microsoft 365 security incident management preparation</span></span>](assurance-sim-preparation.md)
- [<span data-ttu-id="1dbbe-126">Rilevamento e analisi degli incidenti di sicurezza di Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="1dbbe-126">Microsoft 365 security incident management detection and analysis</span></span>](assurance-sim-detection-analysis.md)
- [<span data-ttu-id="1dbbe-127">Contenimento, eliminazione e ripristino della gestione degli incidenti di sicurezza di Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="1dbbe-127">Microsoft 365 security incident management containment, eradication, and recovery</span></span>](assurance-sim-containment-eradication-recovery.md)
