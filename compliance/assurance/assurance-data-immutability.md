---
title: Immutabilità dei dati in Microsoft 365
description: Informazioni su come Microsoft 365 mantiene i dati in forma individuabile per affrontare i requisiti di conformità normativa, governance interna e rischi per controversia legale.
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
- MS-Compliance
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 2e86cdfe082ec35fd7fd111a13a4def6f1b01806
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497634"
---
# <a name="data-immutability-in-microsoft-365"></a>Immutabilità dei dati in Microsoft 365

La conformità normativa, i requisiti di governance interna o i rischi per controversia legale richiedono alle organizzazioni di conservare la posta elettronica e i dati associati in un formato individuabile. Tutti i dati nel sistema devono essere individuabili e nessuno di questi può essere eliminato o modificato. Il termine standard del settore è "immutabilità".

I metodi tradizionali per l'immutabilità in genere funzionavano spostando i messaggi di posta elettronica in un percorso di archiviazione separato di sola lettura. Anche se tali sistemi hanno lo scopo di conservare gli elementi delle cassette postali per l'individuazione, spesso influiscono sull'esperienza utente rimuovendo gli elementi conservati dal flusso di lavoro giornaliero personalizzato. Per i professionisti IT, questo approccio di immutabilità richiede la distribuzione e la manutenzione continua di un server e di un'infrastruttura di archiviazione separati. L'individuazione viene eseguita con strumenti esterni al sistema di posta e include i costi di distribuzione e manutenzione associati.

Grazie alle funzionalità dei criteri di conservazione e conservazione sul posto dell'archiviazione in Microsoft 365 e nei relativi servizi, è possibile conservare e conservare molte classi di dati in ingresso, interni e in uscita. Tra questi vi sono anche:

- Comunicazioni di posta elettronica in ingresso e in uscita
- Libri e record contenuti in un modulo di posta elettronica o in documenti online condivisi
- Convocazioni di riunioni
- Fax
- Messaggi istantanei
- Documenti condivisi durante le riunioni online
- Segreteria telefonica

Inoltre, Microsoft ha sviluppato funzionalità aggiuntive [](https://support.office.com/article/Archiving-third-party-data-in-Office-365-0ce338d5-3666-4a18-86ab-c6910ff408cc) per consentire l'archiviazione di dati da altre origini tramite l'integrazione con soluzioni di acquisizione e gestione dei dati di terze parti. Dopo l'importazione dei dati di terze parti, è possibile applicare le funzionalità di conformità di Microsoft 365 ai dati, tra cui:

- [Conservazione per controversia legale](/microsoft-365/compliance/create-a-litigation-hold)
- [EDiscovery e blocco sul posto](/microsoft-365/compliance/manage-legal-investigations)
- [Ricerca di conformità](/microsoft-365/compliance/search-for-content)
- [Archiviazione sul posto](/microsoft-365/compliance/enable-archive-mailboxes)
- [Controllo delle cassette postali](/microsoft-365/compliance/enable-mailbox-auditing)
- [Criteri di conservazione](/microsoft-365/compliance/retention-policies)

Ad esempio, quando una cassetta postale viene messa in conservazione per controversia legale, i dati di terze parti vengono mantenuti. È possibile eseguire ricerche nei dati di terze parti In-Place eDiscovery o ricerca di conformità. In altri termini, è possibile applicare criteri di archiviazione e conservazione ai dati di terze parti proprio come per i dati Microsoft. L'archiviazione di dati di terze parti in Microsoft 365 consente all'organizzazione di rimanere conforme ai criteri normativi e governativi.

L'archiviazione in Microsoft 365 fornisce l'archiviazione conforme alla regola 17a-4 della regola 17a-4 della Securities and Exchange Commission (SEC). Microsoft 365 mantiene i file permanenti di tutti i dati raccolti in un formato non riscrivibile e non cancellabile utilizzando criteri di conservazione e criteri di conservazione sul posto, incluso il blocco di conservazione.

In particolare:

- Tutti i record archiviati utilizzando i criteri di conservazione indicati in precedenza vengono conservati in un'area di archiviazione dedicata al di fuori della visualizzazione dell'utente ordinario. Solo gli utenti autorizzati possono accedere a questi record ed eseguire ricerche, ma non modificarli o cancellarli.
- I metadati per ogni elemento includono un timestamp utilizzato nel calcolo della durata della conservazione. I timestamp vengono applicati quando viene ricevuto o creato un nuovo elemento e non possono essere modificati o rimossi dai metadati.
- L'archiviazione in Microsoft 365 consente agli utenti di combinare criteri di conservazione diversi e di mantenere azioni per creare criteri di conservazione granulari. Questi criteri definiscono il tipo o la posizione degli elementi conservati e la durata della conservazione.
- La funzionalità di blocco dell'archiviazione consente agli utenti di scegliere se impostare il criterio come criterio restrittivo. Un criterio restrittivo impedisce a chiunque di avere la possibilità di rimuovere, disabilitare o apportare modifiche al criterio di conservazione. Ciò significa che, una volta abilitato il blocco di conservazione, non può essere disabilitato e non esiste alcun meccanismo in base al quale i dati dei depositati esistenti raccolti dai criteri di conservazione in atto possono essere sovrascritti, modificati, cancellati o eliminati durante il periodo di conservazione. Inoltre, il periodo di conservazione impostato dal blocco di conservazione potrebbe non essere ridotto o ridotto. Tuttavia, può essere allungato, nel caso di un requisito legale per continuare la conservazione dei dati archiviati, come indicato in precedenza. Preservation Lock garantisce che nessuno, nemmeno gli amministratori o gli utenti con determinati accessi di controllo, possa modificare le impostazioni o sovrascrivere o cancellare i dati archiviati, portando l'archiviazione in Microsoft 365 in linea con le indicazioni riportate nella versione 2003 della regola SEC 17a-4.

Per comprendere in che modo Microsoft 365 consente di soddisfare gli obblighi normativi, in particolare in relazione ai requisiti della regola 17a-4, vedere il [white paper](https://www.microsoft.com/microsoft-365/blog/wp-content/uploads/2015/11/Microsoft-EOA-White-Paper.pdf) relativo a Archiviazione Exchange Online, SharePoint Online, OneDrive for Business e Skype for Business. Il white paper fornisce inoltre un'analisi approfondita delle funzionalità e delle funzionalità di archiviazione di Microsoft 365 in base a ognuno dei requisiti di cui alla regola SEC 17a-4 e dimostra ai clienti regolamentati come l'archiviazione di Microsoft 365 possa consentire loro di soddisfare questi requisiti.
