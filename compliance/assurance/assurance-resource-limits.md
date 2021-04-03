---
title: Limiti delle risorse di Microsoft 365
description: In questo articolo sono disponibili informazioni sui limiti delle risorse per le varie applicazioni in Microsoft 365.
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
ms.openlocfilehash: 54ea001e542cdd1ab078546cf96bd011e27ab1dc
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497503"
---
# <a name="service-resource-limits"></a>Limiti della risorsa servizio

I limiti delle risorse vengono applicati utilizzando quote (limiti) e limitazione. Azure Active Directory (Azure AD) e i singoli servizi di Microsoft 365 usano entrambi. I limiti sono specifici del servizio e cambiano nel tempo quando vengono aggiunte nuove funzionalità. Per informazioni dettagliate sui limiti correnti per i vari servizi, vedere i seguenti argomenti:

- [Limiti e restrizioni del servizio Azure AD](/azure/azure-resource-manager/management/azure-subscription-service-limits)
- [Limiti di Exchange Online](/office365/servicedescriptions/exchange-online-service-description/exchange-online-limits)
- [Limiti software e limiti di SharePoint Online](https://support.office.com/article/SharePoint-Online-software-boundaries-and-limits-8F34FF47-B749-408B-ABC0-B605E1F6D498)
- [Limiti di Skype for Business](https://technet.microsoft.com/library/skype-for-business-online-limits.aspx)
- [API REST di Yammer e limiti di frequenza](https://developer.yammer.com/docs/rest-api-rate-limits)
- [Limiti delle dimensioni dei file in Sway](https://support.office.com/article/File-size-limits-in-Sway-4db21bc6-b42b-499f-9272-66e089db109f)

Oltre a questi limiti, in Azure AD e Microsoft 365 vengono utilizzati diversi meccanismi di limitazione. La limitazione all'interno del servizio è particolarmente importante, dato che le risorse di rete nei data center di Microsoft sono ottimizzate per l'ampio set di clienti che usano i servizi. I meccanismi di limitazione includono:

- Azure AD e Microsoft 365 presentano limitazioni a livello di utente, che limitano il numero di transazioni o chiamate simultanee (tramite script o codice) che possono essere eseguite da un singolo utente.
- Un criterio di limitazione di PowerShell predefinito viene assegnato a ogni tenant durante la creazione del tenant. Queste impostazioni influiscono su altri elementi, ad esempio il numero massimo di sessioni di PowerShell simultanee che possono essere aperte da un singolo amministratore.
- Ogni cliente di Exchange Online dispone di un criterio EWS (Exchange Web Services) predefinito ottimizzato per le operazioni dei client EWS e di limitazione che si applica a tutti i client Outlook.
