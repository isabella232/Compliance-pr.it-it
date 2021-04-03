---
title: Controlli di accesso aziendale di Microsoft 365 Yammer
description: In questo articolo è contenuto un breve riepilogo sui controlli di accesso a Yammer Enterprise nell'ambiente di produzione.
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
hideEdit: true
ms.openlocfilehash: df345d922bbd0c9106cf0714377803a9c0870d82
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497350"
---
# <a name="yammer-enterprise-access-controls"></a>Controlli di accesso aziendale di Yammer 

L'accesso fisico e logico all'ambiente di produzione di Yammer è limitato a un piccolo gruppo di persone (infrastruttura e operazioni). Come per altri tecnici di Microsoft 365, i tecnici di Yammer non hanno accesso permanente ai dati dei clienti. L'accesso deve essere richiesto utilizzando un sistema di controllo di accesso just-in-time basato sull'approvazione simile a Lockbox con un numero limitato di responsabili approvazione. I responsabili approvazione verificano la richiesta (ad esempio, verificano se la richiesta è legittima in base a necessità, caso aziendale, tempo e così via) e quindi approvano o negano la richiesta. Se la richiesta viene approvata, l'accesso JIT viene concesso per un periodo di tempo definito e limitato. Dopo il superamento del tempo di accesso, l'accesso scade automaticamente.

Come per altri servizi di Microsoft 365, tutti gli accessi all'ambiente di produzione di Yammer utilizzano l'autenticazione a più fattori. Tutti gli accessi e la cronologia dei comandi sono attribuiti a un utente e registrati e esaminati regolarmente dal team di sicurezza di Yammer.

Per ulteriori informazioni sull'amministrazione e la gestione di Yammer, vedere la Guida [dell'amministratore di Yammer.](/yammer/yammer-landing-page)