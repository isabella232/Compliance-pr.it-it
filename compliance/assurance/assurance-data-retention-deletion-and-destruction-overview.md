---
title: Conservazione, eliminazione e distruzione dei dati in Microsoft 365
description: Panoramica dei criteri Microsoft per la Microsoft 365 sulla conservazione, l'eliminazione e la distruzione dei dati.
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
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: c851b235a70104720457d08c51529ee7b25c65e4
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2021
ms.locfileid: "58947074"
---
# <a name="data-retention-deletion-and-destruction-in-microsoft-365"></a>Conservazione, eliminazione e distruzione dei dati in Microsoft 365

Microsoft ha un criterio standard per la gestione dei dati per Microsoft 365 che specifica per quanto tempo i dati dei clienti vengono conservati dopo l'eliminazione. In genere, i dati dei clienti vengono eliminati in due scenari:

- **Eliminazione attiva:** il tenant ha una sottoscrizione attiva e un utente o un amministratore elimina i dati oppure gli amministratori eliminano un utente.
- **Eliminazione passiva:** la sottoscrizione tenant termina.

## <a name="data-retention"></a>Conservazione dei dati

Per ognuno di questi scenari di eliminazione, la tabella seguente mostra il periodo massimo di conservazione dei dati, in base alla categoria e alla classificazione dei dati:

| Categoria dati | Classificazione dei dati | Descrizione | Esempi | Periodo di conservazione |
|-----------------|-----------------|-----------------|----------------------------------|-------------------------------|
| Dati cliente
 | Contenuto del cliente| Contenuto direttamente fornito/creato da amministratori e utenti <br><br> Include tutti i file di testo, audio, video, immagini e software creati e archiviati nei data center Microsoft quando si utilizzano i servizi in Microsoft 365 | Esempi delle applicazioni di Microsoft 365 più comunemente utilizzate che consentono agli utenti di creare dati includono Word, Excel, PowerPoint, Outlook e OneNote <br><br> Il contenuto del cliente include anche segreti forniti/di proprietà del cliente (password, certificati, chiavi di crittografia, chiavi di archiviazione) | **Scenario di eliminazione attiva:** al massimo 30 giorni <br><br> **Scenario di eliminazione passiva:** al massimo 180 giorni |
| Dati cliente
 | Informazioni di identificazione dell'utente finale (EUII) | Dati che identificano o potrebbero essere utilizzati per identificare l'utente di un servizio Microsoft. L'UEII non contiene contenuto del cliente | Nome utente o nome visualizzato (DOMINIO\NomeUtente) <br><br> Nome entità utente (name@domain) <br><br>  Indirizzi IP specifici dell'utente | **Scenario di eliminazione attiva:** al massimo 180 giorni (solo un'azione di amministratore tenant) <br><br> **Scenario di eliminazione passiva:** al massimo 180 giorni |
| Dati personali <br> (dati non inclusi nei dati dei clienti) | Identificatori pseudonimi dell'utente finale (EUPI) | Identificatore creato da Microsoft associato all'utente di un servizio Microsoft. Se combinato con altre informazioni, ad esempio una tabella di mapping, EUPI identifica l'utente finale <br><br> EUPI non contiene informazioni caricate o create dal cliente | GUID utente, GUID o SID <br><br> ID sessione | **Scenario di eliminazione attiva:** al massimo 30 giorni <br><br> **Scenario di eliminazione passiva:** al massimo 180 giorni |

## <a name="subscription-retention"></a>Conservazione della sottoscrizione

Nel termine di una sottoscrizione attiva, un sottoscrittore può accedere, estrarre o eliminare i dati dei clienti archiviati in Microsoft 365. Se una sottoscrizione a pagamento termina o viene terminata, Microsoft conserva i dati dei clienti archiviati in Microsoft 365 in un account a funzione limitata per 90 giorni per consentire al sottoscrittore di estrarre i dati. Al termine del periodo di conservazione di 90 giorni, Microsoft disabilita l'account ed elimina i dati del cliente. Non più di 180 giorni dopo la scadenza o la chiusura di un abbonamento a Microsoft 365, Microsoft disabilita l'account ed elimina tutti i dati dei clienti dall'account. Una volta trascorso il periodo di conservazione massimo per tutti i dati, il rendering dei dati viene reso commercialmente irreversibile.

Per una versione di valutazione gratuita, l'account passa allo stato di tolleranza per 30 giorni nella maggior parte dei paesi e delle aree geografiche. Durante questo periodo di tolleranza è possibile acquistare Microsoft 365. Se si decide di non acquistare Microsoft 365, è possibile annullare la versione di valutazione o lasciar scadere il periodo di tolleranza e le informazioni sull'account di valutazione e i relativi dati verranno eliminati.

## <a name="expedited-deletion"></a>Eliminazione accelerata

Per qualsiasi abbonamento, un sottoscrittore può contattare il Supporto tecnico Microsoft e richiedere il deprovisioning rapido della sottoscrizione. In questo processo, tutti i dati utente vengono eliminati tre giorni dopo che l'amministratore ha immesso il codice di blocco fornito da Microsoft. Sono inclusi i dati in SharePoint Online ed Exchange Online in attesa o archiviati in cassette postali inattive.

Per altre informazioni sul de-provisioning rapido, vedi [Annullare l'abbonamento.](/microsoft-365/commerce/subscriptions/cancel-your-subscription)

## <a name="related-links"></a>Collegamenti correlati

- [Distruzione di dispositivi contenenti dati](assurance-data-bearing-device-destruction.md)
- [Capacità di immutabilità in Office 365](assurance-data-immutability.md)
- [Eliminazione dei dati di Exchange Online](assurance-exchange-online-data-deletion.md)
- [Eliminazione dei dati di SharePoint Online](assurance-sharepoint-online-data-deletion.md)
