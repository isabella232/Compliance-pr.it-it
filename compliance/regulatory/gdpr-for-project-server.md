---
title: GDPR per Project Server
description: Informazioni su come gestire i requisiti del GDPR in Project Server locale.
f1.keywords:
- NOCSH
ms.author: mikeplum
author: MikePlumleyMSFT
manager: pamgreen
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.localizationpriority: high
titleSuffix: Microsoft GDPR
ms.custom: seo-marvel-apr2020
ms.collection: MS-Compliance
hideEdit: true
ms.openlocfilehash: ee4dad3a8b3c4bc6ffb67db78cb083c8524ddad5
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2021
ms.locfileid: "58948111"
---
# <a name="gdpr-for-project-server"></a>GDPR per Project Server

Project Server utilizza gli script personalizzati per esportare e redigere dati utente in Project Web App. Il processo di base è il seguente:

1.  Trovare i siti di Project Web App della farm.

2.  Trovare i progetti in ogni sito che contiene l'utente.

3.  Esportare ed esaminare i tipi di dati da esaminare.

4.  Redigere i dati in base alle esigenze.

Questi passaggi sono descritti dettagliatamente negli articoli seguenti:

- [Esportare i dati degli utenti da Project Server](/Project/export-user-data-from-project-server?toc=/Office365/Enterprise/toc.json)

- [Eliminare i dati degli utenti da Project Server](/Project/delete-user-data-from-project-server?toc=/Office365/Enterprise/toc.json)


Tenere presente che Project Server è basato su SharePoint Server e registra gli eventi nei registri del Servizio di registrazione unificato e su database servizio di utilizzo. Per ulteriori informazioni, vedere [GDPR per SharePoint Server](gdpr-for-sharepoint-server.md).
