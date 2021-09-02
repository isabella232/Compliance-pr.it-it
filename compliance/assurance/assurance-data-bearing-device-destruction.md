---
title: Distruzione dei dispositivi di rilevamento dei dati
description: In questo articolo viene fornita una panoramica del processo di distruzione dei dispositivi per i data center Microsoft.
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.localizationpriority: medium
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
ms.openlocfilehash: 6a26334b805be069298302d3ad1e8e5b9e728150
ms.sourcegitcommit: 1fd50ef5f165228109a3f2f0aef4b0c2aa59b2ff
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/02/2021
ms.locfileid: "58862400"
---
# <a name="data-bearing-device-destruction"></a>Distruzione dei dispositivi di rilevamento dei dati

## <a name="data-destruction-overview"></a>Panoramica della distruzione dei dati

Microsoft dispone di linee guida, criteri, requisiti di sicurezza e procedure per la gestione e la gestione dei DBD all'interno dei datacenter Microsoft.

Un DBD è qualsiasi dispositivo di archiviazione in grado di archiviare i dati microsoft proprietari o dei clienti:

- Unità disco rigido
- Unità SSD (Solid-State Drive)
- Unità USB
- Schede acceleratore I/O
- Schede flash SD/Compact
- Schede HSM
- Schede PCIe SSD
- NVDIMM (modulo di memoria dual-in-line non volatile)

I DBD non riusciti utilizzati nei datacenter Microsoft vengono controllati ed distrutti all'interno del campus del datacenter. Qualsiasi risorsa ritirata dal servizio viene valutata per l'eliminazione in modo proporzionale ai requisiti di sicurezza/privacy e alla classificazione degli asset e in conformità con eventuali regole, leggi e normative applicabili.

Microsoft usa tre categorie di sanitizzazione dei dati per DBD e asset contenenti dati:

- **Clear**: si riferisce alle tecniche logiche che consentono di disinfettare i dati in tutte le posizioni di archiviazione indirizzabili dall'utente per la protezione da semplici tecniche di recupero dati non invasive. Si tratta di tecniche in genere applicate tramite i comandi standard di lettura e scrittura al dispositivo di archiviazione, ad esempio riscrittura con un nuovo valore o l'uso di un'opzione di menu per ripristinare lo stato di fabbrica del dispositivo (in cui la riscrittura non è supportata).
- **Purge**: si riferisce a tecniche fisiche o logiche che rendono impossibile il ripristino dei dati di destinazione utilizzando tecniche di laboratorio all'avanguardia.
- **Destroy**: rende il ripristino dei dati di destinazione infeasible utilizzando tecniche di laboratorio all'avanguardia e comporta l'impossibilità successiva di utilizzare i supporti per l'archiviazione dei dati.

L'eliminazione e l'eliminazione della sanificazione vengono eseguite utilizzando strumenti e processi approvati dal gruppo di sicurezza. I record vengono conservati per la cancellazione e la distruzione degli asset. I dispositivi che non riescono a completare la cancellazione vengono degaussati correttamente (solo per supporti magnetici), punzonati a più pin (per schede basate su scheggiate come SSD) o distrutti.

## <a name="clear"></a>Clear

Se un asset ritirato viene valutato e considerato non accessibile, viene cancellato da una soluzione approvata per l'eliminazione dei dati. I datacenter Microsoft usano le linee guida chiare NIST SP-800-88.

## <a name="purge"></a>Eliminazione

A seconda della configurazione locale e della disponibilità del dispositivo, alcuni dispositivi vengono eliminati prima della distruzione. I dispositivi di eliminazione includono degausser approvati dall'NSA per supporti magnetici e dispositivi di punzone a più pin per supporti a stato solido. I datacenter Microsoft usano le linee guida per l'eliminazione di NIST SP-800-88.

## <a name="destroy"></a>Distruggi

Se un asset ritirato viene valutato e considerato accessibile, viene distrutto in sede utilizzando una procedura operativa standard approvata che soddisfa le linee guida NIST SP-800-88. Questi DBD vengono monitorati fisicamente e logicamente per mantenere la catena di custodia attraverso l'eliminazione finale.

Ogni datacenter Microsoft usa un processo in loco per disinfettare ed eliminare dbD non riusciti e ritirati. Durante questo processo, il personale Microsoft garantisce che la catena di custodia sia mantenuta durante tutto il processo di eliminazione.

## <a name="resources"></a>Risorse

- [Pubblicazione speciale NIST 800-88](https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-88r1.pdf)
