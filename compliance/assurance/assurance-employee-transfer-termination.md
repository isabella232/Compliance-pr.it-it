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
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
search.appverid:
- MET150
- MOE150
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 4a71ab3ddf6688df5480a8f260e004778aa6212b
ms.sourcegitcommit: 07578a8e03b931f47c49f4e34b78cf8ba0605e8f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/23/2021
ms.locfileid: "53573361"
---
# <a name="microsoft-employee-transfer-and-termination"></a>Trasferimento e cessazione dei dipendenti Microsoft

Microsoft, come tutte le altre organizzazioni, gestisce i trasferimenti e le terminazioni dei dipendenti come parte del normale funzionamento aziendale. Quando un dipendente cambia posizione o lascia l'azienda, è essenziale revocare l'accesso inappropriato in modo rapido. Per facilitare le modifiche di accesso e le revoche di accesso efficienti, Microsoft utilizza procedure standardizzate e processi automatizzati per coordinare il sistema HRIS (Human Resources Information System) con il sistema IDM (Identity Management). L'orchestrazione automatizzata tra questi due sistemi è essenziale per mantenere la coerenza operativa, salvaguardare i dati e i servizi online di Microsoft, evitare il rischio di perdita dei privilegi e ridurre i rischi correlati alle minacce insider.

I servizi online Microsoft sono progettati per funzionare senza un accesso amministrativo permanente agli ambienti di produzione per i nostri tecnici. Microsoft usa un modello JEA (Just-In-Time), Just-Enough-Access (JEA) per fornire ai tecnici l'accesso temporaneo necessario per supportare il servizio quando necessario. Per richiedere e utilizzare un account del team di servizio per l'accesso JIT, i tecnici devono richiedere e mantenere le autorizzazioni tramite lo strumento IDM. Quando i dipendenti vengono trasferiti o terminati, l'account del team di servizio e le relative autorizzazioni vengono modificati automaticamente per impedire l'accesso inappropriato.

## <a name="transfer-and-reassignment"></a>Trasferimento e riassegnazione

I trasferimenti dei dipendenti vengono avviati tramite una richiesta di transazione di trasferimento da parte del manager del dipendente. Il manager crea una richiesta e interagisce con Global Talent Acquisition per il processo della lettera di offerta. Una volta che il dipendente accetta l'offerta per il nuovo ruolo, i servizi hr completano il trasferimento negli strumenti di base delle risorse umane, attivando IDM per impostare una data di scadenza per tutte le autorizzazioni del dipendente. Il dipendente deve inviare una richiesta e ricevere l'approvazione del nuovo manager per conservare le autorizzazioni. Se non si invia una richiesta o si riceve l'approvazione del manager, viene revocata l'idoneità del dipendente trasferito. Per i trasferimenti che includono implicazioni di sicurezza specifiche, gli accessi al sistema e le appartenenze ai gruppi di sicurezza vengono rivalutati immediatamente per riflettere il nuovo ruolo.

## <a name="termination"></a>Terminazione

Microsoft usa criteri e procedure chiaramente definiti per revocare prontamente l'accesso fisico e logico ai sistemi e alle risorse Microsoft quando un dipendente viene terminato. Quando un dipendente dà il suo preavviso, il manager del dipendente immette la data di risoluzione nell'HRIS. Dopo l'ultimo giorno lavorativo del dipendente, l'HRIS contrassegna il dipendente come terminato e condivide le informazioni a IDM, che rimuove automaticamente tutti gli account e le idoneità del team di servizio.

Per le terminazioni involontarie, hr collabora con il manager del dipendente per seguire i passaggi appropriati per terminare e disconnettere il dipendente. Analogamente a una terminazione volontaria, le informazioni sulla risoluzione vengono immesse nell'HRIS insieme a tutti i passaggi necessari, ad esempio il coordinamento della data di validità, la rimozione dell'accesso. ed eventuali altri passaggi relativi alla transizione dal ruolo.
