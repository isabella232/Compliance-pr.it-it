---
title: Controlli di accesso di Microsoft 365 Yammer Enterprise
description: In questo articolo è incluso un breve riepilogo sui controlli di accesso di Yammer Enterprise nell'ambiente di produzione.
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
ms.openlocfilehash: d44bead3627ed9b99c93bcffc9f29f87731f7407
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/30/2020
ms.locfileid: "49508406"
---
# <a name="yammer-enterprise-access-controls"></a>Controlli di accesso di Yammer Enterprise 

L'accesso fisico e logico all'ambiente di produzione di Yammer è limitato a un piccolo gruppo di utenti (Infrastructure and Operations). Come per gli altri ingegneri di Microsoft 365, gli ingegneri di Yammer hanno accesso a zero diritti ai dati dei clienti. L'accesso deve essere richiesto utilizzando un sistema di controllo dell'accesso basato su approvazione analogo all'archivio protetto con un numero limitato di responsabili approvazione. I responsabili approvazione verificano la richiesta (ad esempio, verificano se la richiesta è legittima in base alle esigenze, al caso aziendale, al tempo e così via) e quindi approva o rifiuta la richiesta. Se la richiesta viene approvata, l'accesso JIT viene concesso per un periodo di tempo definito e limitato. Dopo aver superato il tempo di accesso, l'accesso scade automaticamente.

Come per gli altri servizi Microsoft 365, tutti gli accessi all'ambiente di produzione di Yammer utilizzano l'autenticazione a più fattori. Tutti gli accessi e la cronologia dei comandi vengono assegnati a un utente e registrati e recensiti regolarmente dal team di sicurezza di Yammer.

Per ulteriori informazioni sull'amministrazione e la gestione di Yammer, vedere la Guida di amministrazione di [Yammer](https://docs.microsoft.com/yammer/yammer-landing-page).