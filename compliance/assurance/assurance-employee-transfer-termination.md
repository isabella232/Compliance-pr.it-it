---
title: Trasferimento e cessazione dei dipendenti Microsoft
description: Informazioni sul processo di trasferimento e risoluzione dei dipendenti Microsoft in Microsoft 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: Admin
ms.topic: article
f1.keywords:
- NOCSH
ms.service: O365-seccomp
ms.localizationpriority: medium
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
search.appverid:
- MET150
- MOE150
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 2450a075d1ae3922cf047e92109a399d10d269ac
ms.sourcegitcommit: 4c00fd65d418065d7f53216c91f455ccb3891c77
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/23/2021
ms.locfileid: "58482038"
---
# <a name="microsoft-employee-transfer-and-termination"></a>Trasferimento e cessazione dei dipendenti Microsoft

Microsoft, come tutte le altre organizzazioni, gestisce i trasferimenti e le terminazioni dei dipendenti come parte del normale funzionamento aziendale. Quando un dipendente cambia posizione o lascia l'azienda, è essenziale revocare l'accesso inappropriato in modo rapido. Per facilitare le modifiche di accesso e le revoche di accesso efficienti, Microsoft utilizza procedure standardizzate e processi automatizzati per coordinare il sistema HRIS (Human Resources Information System) con il sistema IDM (Identity Management). L'orchestrazione automatizzata tra questi due sistemi è essenziale per mantenere la coerenza operativa, salvaguardare i dati e i servizi online di Microsoft, evitare il rischio di perdita dei privilegi e ridurre i rischi correlati alle minacce insider.

I servizi online Microsoft sono progettati per funzionare senza un accesso amministrativo permanente agli ambienti di produzione per i nostri tecnici. Microsoft utilizza un modello JEA (Just-In-Time), Just-Enough-Access (JEA) per fornire ai tecnici l'accesso temporaneo necessario per supportare il servizio quando necessario. Per richiedere e utilizzare un account del team di servizio per l'accesso JIT, i tecnici devono richiedere e mantenere le autorizzazioni tramite lo strumento IDM. Quando i dipendenti vengono trasferiti o terminati, l'account del team di servizio e le relative autorizzazioni vengono modificati automaticamente per impedire l'accesso inappropriato.

## <a name="transfer-and-reassignment"></a>Trasferimento e riassegnazione

I trasferimenti dei dipendenti vengono avviati tramite una richiesta di transazione di trasferimento da parte del manager del dipendente. Il manager crea una richiesta e interagisce con Global Talent Acquisition per il processo della lettera di offerta. Una volta che il dipendente accetta l'offerta per il nuovo ruolo, i servizi hr completano il trasferimento negli strumenti di base delle risorse umane, attivando IDM per impostare una data di scadenza per tutte le autorizzazioni del dipendente. Il dipendente deve inviare una richiesta e ricevere l'approvazione dal nuovo manager per conservare le autorizzazioni. Se non si invia una richiesta o si riceve l'approvazione del manager, viene revocata l'idoneità del dipendente trasferito. Per i trasferimenti che includono implicazioni di sicurezza specifiche, gli accessi al sistema e le appartenenze ai gruppi di sicurezza vengono rivalutati immediatamente per riflettere il nuovo ruolo.

## <a name="termination"></a>Licenziamento

Microsoft applica criteri e procedure chiaramente definiti per revocare tempestivamente l'accesso fisico e logico ai sistemi e alle risorse Microsoft in caso di licenziamento di un dipendente. Quando un dipendente dà il suo preavviso, il manager del dipendente immette la data di risoluzione nell'HRIS. Dopo l'ultimo giorno lavorativo del dipendente, L'HRIS contrassegna il dipendente come terminato e condivide le informazioni a IDM, che rimuove automaticamente tutti gli account e le idoneità del team di servizio.

Per le terminazioni involontarie, HR collabora con il manager del dipendente per seguire i passaggi appropriati per terminare e disconnettere il dipendente. Analogamente a una terminazione volontaria, le informazioni sulla risoluzione vengono immesse nell'HRIS insieme a tutti i passaggi necessari, ad esempio il coordinamento della data di validità, la rimozione dell'accesso e qualsiasi altro passaggio relativo alla transizione fuori dal ruolo.
