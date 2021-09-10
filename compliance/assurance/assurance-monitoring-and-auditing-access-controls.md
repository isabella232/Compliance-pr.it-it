---
title: Microsoft 365 Monitoraggio e controllo dei controlli di accesso
description: "Riepilogo: riepilogo dei vari controlli di accesso di monitoraggio e controllo disponibili all'interno Microsoft 365."
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
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: bf760bf68169092f99fe5a668c9f0087060f7ea2
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2021
ms.locfileid: "58947152"
---
# <a name="monitoring-and-auditing-access-controls-in-microsoft-365"></a>Monitoraggio e controllo dei controlli di accesso in Microsoft 365

Microsoft esegue un monitoraggio e un controllo approfonditi di tutte le operazioni, i privilegi e le delegazioni che si verificano all'interno di Microsoft 365. Microsoft 365 controllo di accesso è un processo automatizzato basato sul principio dei privilegi minimi e che incorpora controlli e controlli di accesso ai dati:

- Tutti gli accessi consentiti sono tracciabili a un utente univoco. Gli amministratori sono responsabili della gestione dei contenuti dei clienti.
- Le richieste di controllo di accesso, le approvazioni e i log delle operazioni amministrative vengono acquisiti per l'analisi della sicurezza e degli eventi dannosi.
- I livelli di accesso vengono esaminati quasi in tempo reale in base all'appartenenza ai gruppi di sicurezza per garantire che solo gli utenti che hanno giustificazioni aziendali autorizzate e che soddisfano i requisiti di idoneità hanno accesso ai sistemi.
- Microsoft 365, i relativi controlli di accesso e i servizi di supporto, inclusi Azure Active Directory e datacenter fisici, vengono regolarmente controllati da terze parti indipendenti per la conformità con [ISO/IEC 27001,](https://www.microsoft.com/TrustCenter/Compliance/iso-iec-27001) [ISO/IEC 27018,](https://www.microsoft.com/TrustCenter/Compliance/iso-iec-27018) [SOC,](https://www.microsoft.com/TrustCenter/Compliance/SOC) [FedRAMP (Office 365)](https://www.microsoft.com/TrustCenter/Compliance/FedRAMP)e altri [standard.](https://www.microsoft.com/TrustCenter/Compliance?service=Office#Icons)
- Microsoft 365 tecnici devono tenere una formazione annuale sulla sicurezza, esaminare le procedure consigliate per l'accesso con privilegi elevati e accettare i criteri di sicurezza e privacy di Microsoft per mantenere i diritti al servizio.

Gli avvisi automatici vengono attivati quando vengono rilevate attività sospette, ad esempio più accessi non riusciti in un breve periodo. Il team Microsoft 365 Security Response usa l'apprendimento automatico e l'analisi dei Big Data per esaminare e analizzare le attività, cercare modelli di accesso irregolare e rispondere in modo proattivo ad attività anomale e illecite. Microsoft impiega anche un team dedicato di tester di penetrazione e si impegna in esercitazioni periodiche di Red Team e Blue Team per individuare i problemi di sicurezza e controllo degli accessi nel servizio. I clienti possono verificare l'efficacia dei sistemi di controllo di accesso usando i report di controllo e l'API di attività di gestione fornita da Microsoft 365.

Per altre informazioni, vedi informazioni [Office 365 riferimento all'API attività di](/office/office-365-management-api/office-365-management-activity-api-reference) gestione e Controllo e creazione di report in [Microsoft 365](assurance-auditing-and-reporting-overview.md).
