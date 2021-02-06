---
title: Eliminazione dei dati di Microsoft 365 Exchange Online
description: Informazioni su come vengono gestite le eliminazioni di dati soft e hard per le cassette postali e gli elementi all'interno delle cassette postali in Exchange Online.
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
ms.openlocfilehash: 527fb2d7ca1536c549990b0c7a4615e4fe3e8436
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120495"
---
# <a name="exchange-online-data-deletion-in-microsoft-365"></a>Eliminazione dei dati di Exchange Online in Microsoft 365

All'interno di Exchange Online, esistono due tipi di eliminazioni: eliminazioni soft ed eliminazioni hard. Questo vale sia per le cassette postali che per gli elementi all'interno di una cassetta postale.

## <a name="soft-deleted-and-hard-deleted-mailboxes"></a>Cassette postali eliminate in modo reciso ed eliminate definitivamente

Una cassetta postale utente eliminata in modo reciso è una cassetta postale che è stata eliminata utilizzando l'interfaccia di amministrazione di Microsoft 365 o il cmdlet Remove-Mailbox ed è ancora presente nel Cestino di Azure Active Directory da meno di 30 giorni. Una cassetta postale può essere eliminata in modo reverso in uno dei modi seguenti:

- L'account utente di Azure Active Directory associato alla cassetta postale utente viene eliminato in modo reciso (l'oggetto utente non è in ambito o nel contenitore del Cestino).
- L'account utente di Azure Active Directory associato alla cassetta postale dell'utente è stato eliminato definitivamente, ma la cassetta postale di Exchange Online è in stato di conservazione per controversia legale o eDiscovery.
- L'account utente di Azure Active Directory associato alla cassetta postale utente è stato eliminato negli ultimi 30 giorni; che è la lunghezza massima di conservazione che Exchange Online mantiene la cassetta postale in uno stato di eliminazione reversibile prima che venga eliminata definitivamente e irreversibile.

Una cassetta postale utente eliminata definitivamente è una cassetta postale che è stata eliminata in uno dei modi seguenti:

- La cassetta postale utente è stata eliminata in modo reciso per più di 30 giorni e l'utente di Azure Active Directory associato è stato eliminato definitivamente. Tutto il contenuto della cassetta postale, ad esempio messaggi di posta elettronica, contatti e file, viene eliminato definitivamente.
- L'account utente associato alla cassetta postale utente è stato eliminato definitivamente da Azure Active Directory. La cassetta postale dell'utente viene eliminata in modo reciso in Exchange Online e rimane in uno stato di eliminazione recisa per 30 giorni. Se nel periodo di 30 giorni un nuovo utente di Azure Active Directory viene sincronizzato dall'account del destinatario originale con lo stesso **ExchangeGuid** o **ArchiveGuid** e il nuovo account viene concesso in licenza per Exchange Online, verrà eliminata la cassetta postale dell'utente originale. Tutto il contenuto della cassetta postale, ad esempio messaggi di posta elettronica, contatti e file, viene eliminato definitivamente.
- Una cassetta postale eliminata temporaneamente viene eliminata utilizzando **Remove-Mailbox -PermanentlyDelete.**

Gli scenari di eliminazione precedenti presuppongono che la cassetta postale dell'utente non sia in uno degli stati di blocco, ad esempio il blocco per controversia legale o eDiscovery. Se nella cassetta postale è presente un tipo di blocco, la cassetta postale non può essere eliminata. Per tutti i tipi di [](https://support.office.com/article/manage-legal-investigations-in-office-365-2e5fbe9f-ee4d-4178-8ff8-4356bc1b168e?ui=en-US&rs=en-US&ad=US) destinatario dell'utente di posta, le impostazioni di blocco vengono ignorate e non hanno alcun effetto sulle eliminazioni definitiva o sulle eliminazioni non definitiva.

## <a name="soft-deleted-and-hard-deleted-items"></a>Elementi eliminati in modo resciso e eliminati definitivamente

Quando un utente elimina un elemento della cassetta postale (ad esempio un messaggio di posta elettronica, un contatto, un appuntamento del calendario o un'attività), l'elemento viene spostato nella cartella Elementi ripristinabili e in una sottocartella denominata "Eliminazioni". Questa operazione viene definita eliminazione rescisa. Il periodo di conservazione degli elementi eliminati nella cartella Eliminazioni dipende dal periodo di conservazione impostato per la cassetta postale. Per impostazione predefinita, una cassetta postale di Exchange Online mantiene gli elementi eliminati per 14 giorni, ma gli amministratori di Exchange Online possono modificare questa impostazione per aumentare il periodo fino a un massimo di 30 giorni. Per la procedura dettagliata per aumentare il periodo di conservazione degli elementi eliminati per una cassetta postale di Exchange Online, vedere Modificare il periodo di conservazione degli elementi eliminati definitivamente per una cassetta postale [di Exchange Online.](/exchange/recipients-in-exchange-online/manage-user-mailboxes/change-deleted-item-retention) Gli utenti possono ripristinare o eliminare gli elementi eliminati prima della scadenza del periodo di conservazione di un elemento eliminato. A tale scopo, viene utilizzata la funzionalità Recupera posta eliminata in Microsoft Outlook o Outlook sul Web.

Se un utente elimina un elemento eliminato utilizzando la funzionalità Recupera elementi eliminati in Outlook o Outlook sul Web, questa operazione è nota come eliminazione definitiva. In Exchange Online, il ripristino di un singolo elemento è abilitato [](/Exchange/recipients/user-mailboxes/recover-deleted-messages) per impostazione predefinita quando viene creata una nuova cassetta postale, in modo che un amministratore possa comunque recuperare gli elementi eliminati definitivamente prima della scadenza del periodo di conservazione degli elementi eliminati. Inoltre, se il messaggio viene modificato da un utente o da un processo, le copie dell'elemento originale vengono conservate quando il ripristino del singolo elemento viene abilitato.

## <a name="page-zeroing"></a>Azzeramento delle pagine

*L'azzeramento* è un meccanismo di sicurezza che scrive zeri o un modello binario sui dati eliminati in modo che i dati eliminati sono più difficili da recuperare. In Exchange Online,  i database delle cassette postali utilizzano le pagine come unità di archiviazione e implementano un processo di sovrascrittura denominato *azzeramento delle pagine.* L'azzeramento delle pagine è abilitato per impostazione predefinita e non può essere disabilitato dai clienti o da Microsoft. Le operazioni di azzeramento delle pagine vengono registrate nei file di registro delle transazioni in modo che tutte le copie di un determinato database siano azzerate in modo analogo. L'azzeramento di una pagina in una copia attiva del database determina l'azzeramento della pagina sulle copie passive del database.

L'azzeramento delle pagine scrive un modello binario sui record eliminati definitivamente. Il modello di azzeramento delle pagine è specifico per le operazioni ESE (Extensible Storage Engine), ovvero il nome del motore di database interno utilizzato dai server in Exchange Online, ed è diverso per le operazioni di run-time rispetto alle operazioni di manutenzione dei database in background. La manutenzione in background dei database è un processo che esegue continuamente il checksum e l'analisi di ogni database. La funzione principale è il checksum delle pagine del database, ma gestisce anche la pulizia dello spazio e l'azzeramento di record e pagine non azzerati a causa di un arresto anomalo dello Store.

La tabella seguente elenca le sequenze di riempimento che corrispondono a specifiche operazioni runtime.

| Operazione runtime di ESE   | Sequenza di riempimento |
|--------------------------|--------------|
| Sostituisci                  | R            |
| Elimina record/valore lungo | D            |
| Spazio pagina liberato         | H            |

La tabella che segue elenca le sequenze di riempimento che corrispondono alle specifiche operazioni che avvengono durante le operazioni di manutenzione in background di ESE.

| Operazioni di manutenzione in background del database ESE | Motivo riempimento |
|-----------------------------------------------|--------------|
| Elimina record                                 | D            |
| Elimina valore lungo                             | L            |
| Spazio pagina liberato della pagina parzialmente utilizzata       | Z            |
| Spazio pagina liberato della pagina inutilizzata               | U            |

### <a name="page-zeroing-process"></a>Processo di azzeramento delle pagine

Il processo di azzeramento delle pagine dipende dallo scenario di eliminazione. La tabella seguente illustra gli scenari di eliminazione nel database e quando viene attivata la funzione di azzeramento delle pagine.

| Scenario di eliminazione dal database | Processo di ESE e tempi di azzeramento dei dati del database |
|:--------------------------|:------------------------------------------------|
| L'elemento scade in base al periodo di conservazione degli elementi eliminati. | Un thread asincrono scrive una sequenza binaria sui dati eliminati. Questa azione si verifica entro pochi millisecondi dall'eliminazione del record. Se il processo di archiviazione si arresta in modo anomalo mentre il lavoro di azzeramento asincrono è ancora in sospeso (o la pulizia dell'archivio delle versioni viene annullata a causa dell'aumento dell'archivio delle versioni), l'azzeramento viene completato quando la manutenzione del database in background elabora tale sezione del database. |
| View Scenario: Expiration of items from Outlook/Outlook on the web folder view (for example, Conversation view) | L'azzeramento dei dati avviene quando la manutenzione in background del database elabora questa sezione del database. |
| Scenario di spostamento/eliminazione della cassetta postale: cassetta postale di origine eliminata (scadenza della cassetta postale eliminata) | L'azzeramento dei dati avviene quando la manutenzione in background del database elabora questa sezione del database. |

### <a name="mailbox-data-types-without-page-zeroing"></a>Tipi di dati delle cassette postali senza azzeramento delle pagine

I seguenti tipi di dati delle cassette postali non dispongono di disposizioni per l'azzeramento delle pagine:

- **Registri delle transazioni del database** delle cassette postali- Quando i registri delle transazioni vengono eliminati come parte delle normali operazioni, non è necessario azzerare i blocchi nel file system in cui sono archiviati i file di registro eliminati. È probabile che il file system reutilizzi rapidamente lo spazio libero per i log appena creati, ma non c'è alcuna garanzia che ciò accada.
- **File di catalogo dell'indice di** contenuto: Exchange Online utilizza Search Foundation (noto anche come FAST) per la funzionalità di indicizzazione della ricerca. Il catalogo dell'indice di ricerca è composto da diverse decine di file archiviati nello stesso volume del file del database delle cassette postali. Quando un messaggio viene eliminato in modo definitivo dal database delle cassette postali, il contenuto nel catalogo di ricerca ad esso associato non viene eliminato immediatamente. L'eliminazione del contenuto si verifica quando Search Foundation esegue un'ombreggiatura (o unione master) di molti piccoli file di catalogo in un singolo file di dimensioni maggiori. Una volta completata l'unione master, i piccoli file del catalogo vengono eliminati. Non esiste alcun processo per azzerare i blocchi che hanno archiviato i file di catalogo eliminati.

## <a name="continuous-replication"></a>Replica continua

La replica continua (nota anche come log shipping e riesecuzione) è una tecnologia di Exchange Online che crea e gestisce copie di ogni database delle cassette postali per fornire disponibilità elevata, resilienza del sito e ripristino di emergenza. La replica continua utilizza il Exchange Server di ripristino di arresto anomalo del database per fornire una tecnologia che esegue l'aggiornamento asincrono di una o più copie di un database delle cassette postali. Ogni server Cassette postali registra gli aggiornamenti del database effettuati su un database attivo (ad esempio, attività di posta elettronica degli utenti) come record di registro in un set sequenziale di file di registro delle transazioni da 1 MB. Questo set di file viene definito flusso di log. Nella replica continua, il flusso di log viene utilizzato anche per aggiornare in modo asincrono una o più copie di un database. A tale scopo, i registri vengono trasmessi in un percorso contenente una copia passiva del database attivo e quindi riprodotti nella copia passiva del database. Se tutti i registri del database attivo vengono riprodotti su una copia passiva del database, i due database sono equivalenti ed è attraverso questo processo che qualsiasi modifica fisica apportata a un database attivo viene replicata in tutte le copie passive del database.

Qualsiasi eliminazione da un database delle cassette postali, che si tratta di un elemento della cassetta postale o di un'intera cassetta postale e di eliminazione rescisa o definitiva, rappresenta una modifica fisica al database attivo. L'azzeramento delle pagine comporta inoltre l'esecuzione di modifiche fisiche al database attivo. Queste modifiche vengono scritte nei file di registro tramite un processo denominato replica continua e, quando tali file di registro vengono riprodotti su copie passive del database, le stesse modifiche fisiche vengono apportate a tali database passivi.
