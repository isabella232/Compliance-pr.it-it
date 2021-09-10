---
title: Microsoft 365 Yammer di accesso aziendale
description: Questo articolo contiene un breve riepilogo dei controlli di Yammer Enterprise di accesso nell'ambiente di produzione.
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
ms.openlocfilehash: 5bc064ccf982b9a67ec5cedc33e85f58e1d7dfc1
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2021
ms.locfileid: "58947428"
---
# <a name="yammer-enterprise-access-controls"></a>Yammer di accesso aziendale 

L'accesso fisico e logico all'Yammer di produzione è limitato a un piccolo gruppo di persone (infrastruttura e operazioni). Come per altri Microsoft 365 tecnici, Yammer non hanno accesso permanente ai dati dei clienti. L'accesso deve essere richiesto utilizzando un sistema di controllo di accesso just-in-time basato sull'approvazione simile a Lockbox con un numero limitato di responsabili approvazione. I responsabili approvazione verificano la richiesta (ad esempio, verificano se la richiesta è legittima in base a necessità, caso aziendale, tempo e così via) e quindi approvano o negano la richiesta. Se la richiesta viene approvata, l'accesso JIT viene concesso per un periodo di tempo definito e limitato. Dopo il superamento del tempo di accesso, l'accesso scade automaticamente.

Come per altri servizi Microsoft 365, tutti gli accessi all'ambiente Yammer di produzione utilizzano l'autenticazione a più fattori. Tutti gli accessi e la cronologia dei comandi sono attribuiti a un utente e registrati e esaminati regolarmente dal team Yammer sicurezza.

Per ulteriori informazioni sull'amministrazione Yammer gestione, vedere Yammer [guida dell'amministratore.](/yammer/yammer-landing-page)