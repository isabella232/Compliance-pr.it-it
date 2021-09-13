---
title: Microsoft 365 Limiti delle risorse
description: In questo articolo sono disponibili informazioni sui limiti delle risorse per le varie applicazioni in Microsoft 365.
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
ms.openlocfilehash: 764259e22b23ecc7cea363283fc313a94875a2d1
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/12/2021
ms.locfileid: "59159348"
---
# <a name="service-resource-limits"></a>Limiti della risorsa servizio

I limiti delle risorse vengono applicati utilizzando quote (limiti) e limitazione. Azure Active Directory (Azure AD) e i singoli Microsoft 365 usano entrambi. I limiti sono specifici del servizio e cambiano nel tempo quando vengono aggiunte nuove funzionalità. Per informazioni dettagliate sui limiti correnti per i vari servizi, vedere gli argomenti seguenti:

- [Limiti e restrizioni del servizio Azure AD](/azure/azure-resource-manager/management/azure-subscription-service-limits)
- [Limiti di Exchange Online](/office365/servicedescriptions/exchange-online-service-description/exchange-online-limits)
- [SharePoint Limiti e limiti del software online](https://support.office.com/article/SharePoint-Online-software-boundaries-and-limits-8F34FF47-B749-408B-ABC0-B605E1F6D498)
- [Skype for Business Limiti](https://technet.microsoft.com/library/skype-for-business-online-limits.aspx)
- [Yammer API REST e limiti di frequenza](https://developer.yammer.com/docs/rest-api-rate-limits)
- [Limiti delle dimensioni dei file in Sway](https://support.office.com/article/File-size-limits-in-Sway-4db21bc6-b42b-499f-9272-66e089db109f)

Oltre a questi limiti, vengono usati diversi meccanismi di limitazione in Azure AD e Microsoft 365. La limitazione all'interno del servizio è particolarmente importante, dato che le risorse di rete nei datacenter di Microsoft sono ottimizzate per l'ampio set di clienti che usano i servizi. I meccanismi di limitazione includono:

- Azure AD e Microsoft 365 funzionalità di limitazione a livello di utente, che limitano il numero di transazioni o chiamate simultanee (tramite script o codice) che possono essere eseguite da un singolo utente.
- Un criterio di limitazione di PowerShell predefinito viene assegnato a ogni tenant durante la creazione del tenant. Queste impostazioni influiscono su altri elementi, ad esempio il numero massimo di sessioni di PowerShell simultanee che possono essere aperte da un singolo amministratore.
- Ogni Exchange Online cliente dispone di un criterio predefinito di servizi Web Exchange (EWS) ottimizzato per le operazioni client EWS e di limitazione che si applica a tutti i client Outlook.
