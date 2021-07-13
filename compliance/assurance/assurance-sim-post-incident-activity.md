---
title: 'Gestione degli incidenti di sicurezza Microsoft: attività post-incidente'
description: In questo articolo viene fornita una panoramica del processo di attività post-incidente di gestione degli incidenti di sicurezza nei servizi online Microsoft.
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
hideEdit: true
ms.openlocfilehash: 965c7d6d0d469b9eea981252805bda598c92a4c8
ms.sourcegitcommit: 8bf2602d56eedee4447ddb374ef95b0587f254e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/12/2021
ms.locfileid: "53377533"
---
# <a name="microsoft-security-incident-management-post-incident-activity"></a><span data-ttu-id="517cc-103">Gestione degli incidenti di sicurezza Microsoft: attività post-incidente</span><span class="sxs-lookup"><span data-stu-id="517cc-103">Microsoft security incident management: Post-incident activity</span></span>

## <a name="postmortem"></a><span data-ttu-id="517cc-104">Postmortem</span><span class="sxs-lookup"><span data-stu-id="517cc-104">Postmortem</span></span>

<span data-ttu-id="517cc-105">Alcuni incidenti di sicurezza, in particolare quelli che hanno un impatto sul cliente o che causano una violazione dei dati, sono soggetti a un evento imprevisto completo post-mortem.</span><span class="sxs-lookup"><span data-stu-id="517cc-105">Some security incidents, especially those incidents that are customer impacting or result in a data breach, are subject to a full incident postmortem.</span></span> <span data-ttu-id="517cc-106">Il team di risposta alla sicurezza conduce un postmortem dettagliato con tutte le parti coinvolte nella risposta a eventi imprevisti di sicurezza a:</span><span class="sxs-lookup"><span data-stu-id="517cc-106">The security response team conducts a detailed postmortem with all the parties involved in security incident response to:</span></span>

- <span data-ttu-id="517cc-107">Documentare la sequenza di eventi che hanno causato l'evento imprevisto.</span><span class="sxs-lookup"><span data-stu-id="517cc-107">Document the sequence of events that caused the incident.</span></span>
- <span data-ttu-id="517cc-108">Creare un riepilogo tecnico dell'incidente come supportato dalle prove che includono gli attori coinvolti nella violazione (se noto).</span><span class="sxs-lookup"><span data-stu-id="517cc-108">Create a technical summary of the incident as supported by the evidence that includes the actors involved in the breach (if known).</span></span> <span data-ttu-id="517cc-109">Questo riepilogo includerà la modalità di esecuzione della risposta e altre operazioni da asporto chiave.</span><span class="sxs-lookup"><span data-stu-id="517cc-109">This summary will include how the response was executed and other key takeaways.</span></span>
- <span data-ttu-id="517cc-110">Identificare le interruzioni tecniche, gli errori procedurali, gli errori manuali, i difetti del processo e glitch di comunicazione e/o eventuali vettori di attacco precedentemente sconosciuti identificati durante la risposta agli incidenti di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="517cc-110">Identify technical lapses, procedural failures, manual errors, process flaws, and communication glitches, and/or any previously unknown attack vectors that were identified during the security incident response.</span></span>

<span data-ttu-id="517cc-111">Il postmortem influirà direttamente sul miglioramento dei servizi online Microsoft, sui processi operativi e sulla documentazione impostando nuove priorità nel ciclo di sviluppo di progettazione dei servizi online Microsoft.</span><span class="sxs-lookup"><span data-stu-id="517cc-111">The postmortem will directly influence Microsoft online service improvement, operational processes, and documentation by setting new priorities in the Microsoft online services engineering development cycle.</span></span>

## <a name="documentation"></a><span data-ttu-id="517cc-112">Documentazione</span><span class="sxs-lookup"><span data-stu-id="517cc-112">Documentation</span></span>

<span data-ttu-id="517cc-113">Tutti i principali risultati tecnici del processo post-mortem vengono acquisiti in un report e gli investimenti o le correzioni dei servizi sotto forma di bug o richieste di modifica dello sviluppo.</span><span class="sxs-lookup"><span data-stu-id="517cc-113">All key technical findings in the postmortem process are captured in a report and service investments or fixes in the form of bugs or development change requests.</span></span> <span data-ttu-id="517cc-114">Questi risultati vengono seguiti dai team di progettazione appropriati.</span><span class="sxs-lookup"><span data-stu-id="517cc-114">These findings are followed-up with the appropriate engineering teams.</span></span> <span data-ttu-id="517cc-115">Per gli errori di processo e i problemi inter-organizzativi, i problemi sono documentati nel database del team di risposta alla sicurezza e seguiti con i gruppi appropriati per affrontarli.</span><span class="sxs-lookup"><span data-stu-id="517cc-115">For process failures and cross-organizational issues, issues are documented in the security response team's database and followed-up with the appropriate groups to address them.</span></span>

## <a name="process-improvement"></a><span data-ttu-id="517cc-116">Miglioramento dei processi</span><span class="sxs-lookup"><span data-stu-id="517cc-116">Process improvement</span></span>

<span data-ttu-id="517cc-117">La risposta a un incidente di sicurezza nei servizi online Microsoft implica il coordinamento con più gruppi distribuiti tra organizzazioni diverse all'interno di Microsoft e organizzazioni esterne potenzialmente appropriate come le forze dell'ordine.</span><span class="sxs-lookup"><span data-stu-id="517cc-117">Responding to a security incident in Microsoft online services involves coordination with multiple groups spread across different organizations within Microsoft, and potentially even appropriate external organizations such as law enforcement.</span></span> <span data-ttu-id="517cc-118">Sappiamo che è fondamentale valutare le nostre risposte dopo ogni incidente di sicurezza sia per la sufficienza che per la completezza.</span><span class="sxs-lookup"><span data-stu-id="517cc-118">We know that it is critical to evaluate our responses after every security incident for both sufficiency and completeness.</span></span> <span data-ttu-id="517cc-119">Per eventuali miglioramenti o modifiche identificati, il team di risposta alla sicurezza valuta i suggerimenti in consultazione con i team e gli stakeholder appropriati e, se appropriato, li incorpora nelle procedure operative standard.</span><span class="sxs-lookup"><span data-stu-id="517cc-119">For any identified improvements or changes, the security response team evaluates the suggestions in consultation with the appropriate teams and stakeholders, and where appropriate incorporates them into standard operating procedures.</span></span> <span data-ttu-id="517cc-120">Tutte le modifiche, i bug o i miglioramenti del servizio necessari identificati durante l'attività post-postmortem o di risposta agli incidenti di sicurezza vengono registrati e registrati in un database di progettazione Microsoft interno.</span><span class="sxs-lookup"><span data-stu-id="517cc-120">All required changes, bugs, or service improvements identified during the security incident response or postmortem activity are logged and tracked in an internal Microsoft engineering database.</span></span> <span data-ttu-id="517cc-121">Tutti i potenziali bug o funzionalità vengono assegnati al proprietario appropriato.</span><span class="sxs-lookup"><span data-stu-id="517cc-121">All potential bugs or features are assigned to the appropriate owner.</span></span> <span data-ttu-id="517cc-122">Il team di risposta alla sicurezza Microsoft esamina tutte le voci finché il problema non viene risolto.</span><span class="sxs-lookup"><span data-stu-id="517cc-122">The Microsoft security response team reviews all entries until the issue is resolved.</span></span>

## <a name="related-articles"></a><span data-ttu-id="517cc-123">Articoli correlati</span><span class="sxs-lookup"><span data-stu-id="517cc-123">Related articles</span></span>

- [<span data-ttu-id="517cc-124">Gestione degli incidenti di sicurezza Microsoft</span><span class="sxs-lookup"><span data-stu-id="517cc-124">Microsoft security incident management</span></span>](assurance-security-incident-management.md)
- [<span data-ttu-id="517cc-125">Gestione degli incidenti di sicurezza Microsoft: preparazione</span><span class="sxs-lookup"><span data-stu-id="517cc-125">Microsoft security incident management: Preparation</span></span>](assurance-sim-preparation.md)
- [<span data-ttu-id="517cc-126">Gestione degli incidenti di sicurezza Microsoft: rilevamento e analisi</span><span class="sxs-lookup"><span data-stu-id="517cc-126">Microsoft security incident management: Detection and analysis</span></span>](assurance-sim-detection-analysis.md)
- [<span data-ttu-id="517cc-127">Gestione degli incidenti di sicurezza Microsoft: contenimento, eliminazione e ripristino</span><span class="sxs-lookup"><span data-stu-id="517cc-127">Microsoft security incident management: Containment, eradication, and recovery</span></span>](assurance-sim-containment-eradication-recovery.md)
- [<span data-ttu-id="517cc-128">Come registrare un ticket di supporto per gli eventi di sicurezza</span><span class="sxs-lookup"><span data-stu-id="517cc-128">How to Log a Security Event Support Ticket</span></span>](/azure/security/fundamentals/event-support-ticket)
- [<span data-ttu-id="517cc-129">Notifica di violazione nell'ambito del GDPR in Azure e Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="517cc-129">Azure and Dynamics 365 breach notification under the GDPR</span></span>](/compliance/regulatory/gdpr-breach-azure-dynamics)
