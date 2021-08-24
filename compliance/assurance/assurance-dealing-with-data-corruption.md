---
title: Microsoft 365 Gestione del danneggiamento dei dati
description: In questo articolo vengono illustrati il danneggiamento dei Microsoft 365 e gli sforzi intrapresi da Microsoft per prevenire e ripristinare i dati.
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
ms.openlocfilehash: 860a150760e080df4a577d73478a75ac94b8700b
ms.sourcegitcommit: 4c00fd65d418065d7f53216c91f455ccb3891c77
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/23/2021
ms.locfileid: "58482079"
---
# <a name="dealing-with-data-corruption-in-microsoft-365"></a>Gestione del danneggiamento dei dati in Microsoft 365

Uno degli aspetti più impegnativi dell'esecuzione di un servizio cloud su larga scala è come gestire il danneggiamento dei dati, dato l'elevato volume di dati e sistemi indipendenti. Il danneggiamento dei dati può essere causato da:

- Bug dell'applicazione o dell'infrastruttura, danneggiando parte o tutto lo stato dell'applicazione
- Problemi hardware che causano la perdita di dati o l'impossibilità di leggere i dati
- Errori operativi umani
- Hacker malintenzionati e dipendenti scontenti
- Eventi imprevisti in servizi esterni che comportano la perdita di dati

Poiché una maggiore resilienza nell'integrità dei dati significa un numero minore di incidenti di danneggiamento dei dati, Microsoft ha integrato meccanismi di protezione di Microsoft 365 per evitare che si verifichino danneggiamenti, nonché sistemi e processi che consentono di ripristinare i dati in caso contrario. I controlli e i processi sono presenti nelle varie fasi del processo di rilascio della progettazione per aumentare la resilienza contro il danneggiamento dei dati, tra cui:

- Progettazione del sistema
- Organizzazione e struttura del codice
- Revisione del codice
- Unit test, test di integrazione e test di sistema
- Test/cancelli dei cavi di viaggio

All'Microsoft 365 di produzione, la replica peer tra datacenter garantisce che siano sempre presenti più copie live di tutti i dati. Le immagini e gli script standard vengono utilizzati per ripristinare i server persi e i dati replicati vengono utilizzati per ripristinare i dati dei clienti. A causa dei controlli e dei processi di resilienza dei dati incorporati, Microsoft gestisce i backup solo della documentazione del sistema di informazioni di Microsoft 365 (inclusa la documentazione relativa alla sicurezza), utilizzando la replica incorporata in SharePoint Online e il nostro strumento di repository di codice interno, Source Depot. La documentazione di sistema è archiviata in SharePoint Online e Source Depot contiene immagini di sistema e applicazioni. Sia SharePoint Online che Source Depot usano il controllo delle versioni e vengono replicati quasi in tempo reale.
