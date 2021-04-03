---
title: Eliminazione dei dati di Microsoft 365 SharePoint Online
description: Informazioni sul funzionamento dell'eliminazione dei dati in SharePoint Online, ad esempio dove è archiviato il contenuto eliminato e per quanto tempo.
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
- SPO_Content
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: e89a261e44ef4eb4a1399027b70be88fffb82036
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497408"
---
# <a name="sharepoint-online-data-deletion-in-microsoft-365"></a>Eliminazione dei dati di SharePoint Online in Microsoft 365

SharePoint Online archivia gli oggetti come codice astratto all'interno dei database dell'applicazione. Quando un utente carica un file in SharePoint Online, tale file viene disassemblato e convertito nel codice dell'applicazione e archiviato in più tabelle in più database. In SharePoint Online, tutto il contenuto caricato da un cliente viene suddiviso in blocchi, crittografato (potenzialmente con più chiavi AES a 256 bit) e distribuito nel datacenter. Per informazioni dettagliate sul processo di crittografia e suddivisione in blocchi, vedere [Crittografia nel cloud Microsoft.](/microsoft-365/compliance/office-365-encryption-in-the-microsoft-cloud-overview) 

In SharePoint Online, gli elementi vengono conservati per 93 giorni dal momento in cui vengono eliminati dalla posizione originale. Rimangono nel Cestino del sito per tutto il tempo, a meno che un utente non li elimini o lo svuota. In tal caso, gli elementi vengono visualizzati nel Cestino della raccolta siti, dove rimangono per il resto dei 93 giorni. Per informazioni sul ripristino degli elementi eliminati, vedere [Restore items in the Recycle Bin of a SharePoint site](https://support.office.com/article/6df466b6-55f2-4898-8d6e-c0dff851a0be#ID0EAADAAA=Online
) e Restore deleted items from the site collection recycle [bin.](https://support.office.com/article/5fa924ee-16d7-487b-9a0a-021b9062d14b) Il tempo di conservazione del Cestino non è configurabile in SharePoint Online.

Quando si elimina una raccolta siti, si elimina anche la gerarchia dei siti nella raccolta e tutto il contenuto in esse contenuto:

- Documenti e raccolte documenti
- Elenchi e dati elenco
- Impostazioni di configurazione del sito
- Informazioni sui ruoli e sulla sicurezza correlate al sito o ai relativi siti secondari
- Siti secondari del sito Web principale, relativi contenuti e informazioni utente

Se si elimina accidentalmente una raccolta siti, è possibile ripristinarla da un amministratore globale o di SharePoint tramite l'interfaccia di amministrazione di SharePoint.

Le raccolte siti eliminate vengono conservate per 93 giorni. Dopo 93 giorni, i siti e tutto il relativo contenuto e le impostazioni vengono eliminati definitivamente, inclusi elenchi, raccolte, pagine e siti secondari.

L'eliminazione definitiva si verifica quando un utente elimina gli elementi eliminati dal Cestino della raccolta siti, quando scadono i periodi di conservazione e backup o quando un amministratore elimina definitivamente una raccolta siti utilizzando il [cmdlet Remove-SPODeletedSite](/powershell/module/sharepoint-online/remove-spodeletedsite). Quando un utente elimina definitivamente (elimina definitivamente o elimina) il contenuto da SharePoint Online, vengono eliminate anche tutte le chiavi di crittografia per i blocchi eliminati. I blocchi nei dischi che in precedenza hanno archiviato i blocchi eliminati sono contrassegnati come inutilizzati e disponibili per il nuovo utilizzo.
