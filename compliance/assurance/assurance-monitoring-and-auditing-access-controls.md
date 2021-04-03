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
# <a name="monitoring-and-auditing-access-controls-in-microsoft-365"></a>Monitoraggio e controllo dei controlli di accesso in Microsoft 365

Microsoft esegue un monitoraggio e un controllo approfonditi di tutte le operazioni, privilegi e delega che si verificano all'interno di Microsoft 365. Il controllo di accesso di Microsoft 365 è un processo automatizzato basato sul principio dei privilegi minimi e che include controlli e controlli di accesso ai dati:

- Tutti gli accessi consentiti sono tracciabili a un utente univoco. Gli amministratori sono responsabili della gestione dei contenuti dei clienti.
- Le richieste di controllo di accesso, le approvazioni e i log delle operazioni amministrative vengono acquisiti per l'analisi della sicurezza e degli eventi dannosi.
- I livelli di accesso vengono esaminati quasi in tempo reale in base all'appartenenza ai gruppi di sicurezza per garantire che solo gli utenti che hanno giustificazioni aziendali autorizzate e che soddisfano i requisiti di idoneità hanno accesso ai sistemi.
- Microsoft 365, i controlli di accesso e i servizi di supporto, tra cui Azure Active Directory e i datacenter fisici, vengono regolarmente controllati da terze parti indipendenti per la conformità con [ISO/IEC 27001,](https://www.microsoft.com/TrustCenter/Compliance/iso-iec-27001) [ISO/IEC 27018,](https://www.microsoft.com/TrustCenter/Compliance/iso-iec-27018) [SOC,](https://www.microsoft.com/TrustCenter/Compliance/SOC) [FedRAMP (Office 365)](https://www.microsoft.com/TrustCenter/Compliance/FedRAMP)e altri [standard.](https://www.microsoft.com/TrustCenter/Compliance?service=Office#Icons)
- I tecnici di Microsoft 365 devono tenere una formazione annuale sulla sicurezza, esaminare le procedure consigliate per l'accesso con privilegi elevati e accettare i criteri di sicurezza e privacy di Microsoft per mantenere i diritti al servizio.

Gli avvisi automatici vengono attivati quando vengono rilevate attività sospette, ad esempio più accessi non riusciti in un breve periodo. Il team di Microsoft 365 Security Response usa l'apprendimento automatico e l'analisi dei Big Data per esaminare e analizzare le attività, cercare modelli di accesso irregolare e rispondere in modo proattivo ad attività anomale e illecite. Microsoft impiega anche un team dedicato di tester di penetrazione e si impegna in esercitazioni periodiche di Red Team e Blue Team per individuare i problemi di sicurezza e controllo degli accessi nel servizio. I clienti possono verificare l'efficacia dei sistemi di controllo di accesso usando i report di controllo e l'API di attività di gestione fornita da Microsoft 365.

Per ulteriori informazioni, vedere Informazioni di riferimento sulle API delle attività di gestione di [Office 365](/office/office-365-management-api/office-365-management-activity-api-reference) e Controllo e creazione di [report in Microsoft 365.](assurance-auditing-and-reporting-overview.md)
