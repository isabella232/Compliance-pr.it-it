---
title: Crittografia per i dati in transito
description: In questo articolo, trovare una breve spiegazione del modo in cui Microsoft crittografa Microsoft 365 dati dei clienti in transito.
ms.author: krowley
author: kccross
manager: laurawi
ms.reviewer: sosstah
f1.keywords:
- NOCSH
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.localizationpriority: medium
search.appverid:
- MET150
ms.collection:
- Strat_O365_Enterprise
- M365-security-compliance
- Strat_O365_Enterprise
- MS-Compliance
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: ebeface33b0d5ba419773c13305c277d681e8400
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2021
ms.locfileid: "58947104"
---
# <a name="encryption-for-data-in-transit"></a>Crittografia per i dati in transito

Oltre a proteggere i dati dei clienti in pausa, Microsoft usa tecnologie di crittografia per proteggere i dati dei clienti in transito. I dati sono in transito:

- quando un computer client comunica con un server Microsoft;
- quando un server Microsoft comunica con un altro server Microsoft; e
- quando un server Microsoft comunica con un server non Microsoft (ad esempio, Exchange Online la posta elettronica a un server di posta elettronica di terze parti).

Le comunicazioni tra data center tra i server Microsoft si svolgono su TLS o IPsec e tutti i server rivolti ai clienti negoziano una sessione sicura utilizzando TLS con i computer client (ad esempio, Exchange Online usa TLS 1.2 con forza di crittografia a 256 bit (convalidato da FIPS 140-2 livello 2). Per un [elenco delle](/microsoft-365/compliance/technical-reference-details-about-encryption) suite di crittografia TLS supportate da Office 365, vedere Dettagli tecnici sulla crittografia. Ciò vale per i protocolli utilizzati da client quali Outlook, Skype for Business, Microsoft Teams e Outlook sul web (ad esempio, HTTP, POP3 e così via).

I certificati pubblici vengono emessi da MICROSOFT IT SSL utilizzando SSLAdmin, uno strumento Microsoft interno per proteggere la riservatezza delle informazioni trasmesse. Tutti i certificati emessi da Microsoft IT hanno una lunghezza minima di 2048 bit e la conformità Webtrust richiede SSLAdmin per assicurarsi che i certificati siano rilasciati solo agli indirizzi IP pubblici di proprietà di Microsoft. Tutti gli indirizzi IP che non soddisfano questo criterio vengono instradati attraverso un processo di eccezione.

Tutti i dettagli di implementazione, ad esempio la versione di TLS in uso, se Forward Secrecy (FS) è abilitato, l'ordine delle suite di crittografia e così via, sono disponibili pubblicamente. Un modo per visualizzare questi dettagli è usare un sito Web di terze parti, ad esempio [Qualys SSL Labs.](https://www.ssllabs.com) Di seguito sono riportati i collegamenti alle pagine di test automatizzate di Qualys che visualizzano informazioni per i servizi seguenti:

- [Office 365 Portale](https://www.ssllabs.com/ssltest/analyze.html?d=portal.office.com&hideResults=on)
- [Exchange Online](https://www.ssllabs.com/ssltest/analyze.html?d=outlook.office365.com&hideResults=on)
- [SharePoint Online](https://www.ssllabs.com/ssltest/analyze.html?d=microsoft-my.sharepoint.com&hideResults=on)
- [Skype for Business (SIP)](https://www.ssllabs.com/ssltest/analyze.html?d=sipdir.online.lync.com)
- [Skype for Business (Web)](https://www.ssllabs.com/ssltest/analyze.html?d=webdir.online.lync.com&hideResults=on)
- [Exchange Online Protection](https://ssl-tools.net/mailservers/microsoft-com.mail.protection.outlook.com)
- [Microsoft Teams](https://www.ssllabs.com/ssltest/analyze.html?d=teams.microsoft.com&latest)

Ad Exchange Online Protection, gli URL variano in base ai nomi dei tenant. tuttavia, tutti i clienti possono testare Microsoft 365 utilizzando **microsoft-com.mail.protection.outlook.com**.
