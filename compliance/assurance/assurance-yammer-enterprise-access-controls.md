---
title: Controlli di accesso aziendale di Microsoft 365 Yammer
description: Questo articolo contiene un breve riepilogo dei controlli di accesso di Yammer Enterprise nell'ambiente di produzione.
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
ms.openlocfilehash: 916f26d5f2defdfb21cb9babe3a64cf618e8cd4a
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120365"
---
# <a name="yammer-enterprise-access-controls"></a>Controlli di accesso aziendali di Yammer 

L'accesso fisico e logico all'ambiente di produzione di Yammer è limitato a un piccolo gruppo di persone (infrastruttura e operazioni). Come per gli altri tecnici di Microsoft 365, i tecnici di Yammer non hanno accesso permanente ai dati dei clienti. L'accesso deve essere richiesto utilizzando un sistema di controllo di accesso just-in-time basato sull'approvazione simile a Lockbox con un numero limitato di responsabili approvazione. I responsabili approvazione verificano la richiesta (ad esempio, verificano se la richiesta è legittima in base alle esigenze, al caso aziendale, al tempo e così via) e quindi approvano o negano la richiesta. Se la richiesta viene approvata, l'accesso JIT viene concesso per un periodo di tempo definito e limitato. Una volta superato il tempo di accesso, l'accesso scade automaticamente.

Come per altri servizi di Microsoft 365, tutti gli accessi all'ambiente di produzione di Yammer utilizzano l'autenticazione a più fattori. Tutti gli accessi e la cronologia dei comandi vengono attribuiti a un utente e registrati e esaminati regolarmente dal team di sicurezza di Yammer.

Per ulteriori informazioni sull'amministrazione e la gestione di Yammer, vedere la Guida [per gli amministratori di Yammer.](/yammer/yammer-landing-page)