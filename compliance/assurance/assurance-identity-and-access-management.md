---
title: Panoramica sulla gestione delle identità e degli accessi
description: Informazioni sulla gestione delle identità e degli accessi in Microsoft 365
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
ms.openlocfilehash: c07801fe5ef571ddb4c9efcbfe04a7b3e5faedb6
ms.sourcegitcommit: 7a5b6bc58fc4613b38f3fda20aebee5cec6a5730
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "49787475"
---
# <a name="identity-and-access-management-overview"></a>Panoramica sulla gestione delle identità e degli accessi

## <a name="how-does-microsoft-365-protect-production-systems-from-unauthorized-or-malicious-access"></a>In che modo Microsoft 365 protegge i sistemi di produzione da accessi non autorizzati o dannosi?

Microsoft 365 è stato creato per consentire agli ingegneri di Microsoft di gestire il servizio senza accedere al contenuto del cliente. Per impostazione predefinita, i tecnici Microsoft 365 hanno accesso a zero standing (ZSA) ai contenuti dei clienti e non hanno accesso privilegiato all'ambiente di produzione. Microsoft 365 utilizza un modello JIT (just-in-Time), just-enough-Access (JEA) per fornire agli ingegneri del team di servizio un accesso privilegiato temporaneo agli ambienti di produzione quando tale accesso è necessario per supportare Microsoft 365. Il modello di accesso JIT sostituisce l'accesso amministrativo tradizionale e persistente con un processo che consente agli ingegneri di richiedere l'elevazione temporanea ai ruoli privilegiati quando necessario.

Gli ingegneri assegnati a un team di servizio per supportare i servizi di produzione richiedono l'idoneità per un account del team di servizio tramite lo strumento di gestione delle identità (IDM). La richiesta di idoneità attiva una serie di controlli del personale per garantire che il tecnico abbia superato tutti i requisiti di screening cloud, ha completato la formazione necessaria e ha ricevuto l'approvazione di gestione appropriata prima della creazione dell'account. Solo dopo aver incontrato tutti i requisiti di idoneità, è possibile creare un account del team di servizio per l'ambiente richiesto.

Gli account del team di servizio non garantiscono privilegi di amministratore o accesso al contenuto del cliente. Quando un tecnico richiede ulteriore accesso per supportare il servizio Microsoft 365, richiedono un accesso temporaneo elevato alle risorse necessarie per l'utilizzo di uno strumento di gestione di Access denominato archivio protetto. L'archivio protetto limita l'accesso elevato ai privilegi, alle risorse e al tempo minimi necessari per completare l'attività assegnata. Se un revisore autorizzato approva la richiesta di accesso JIT, al tecnico viene concesso un account temporaneo con solo i privilegi necessari per completare il lavoro assegnato. Questo account temporaneo richiede l'autenticazione a più fattori e viene eliminato automaticamente dopo la scadenza del periodo approvato.

## <a name="how-does-microsoft-365-handle-remote-access-to-production-systems"></a>In che modo Microsoft 365 gestisce l'accesso remoto ai sistemi di produzione?

I componenti di sistema Microsoft 365 sono alloggiati nei datacenter geograficamente separati dai team operativi. Il personale del datacenter non dispone dell'accesso logico ai sistemi Microsoft 365. Di conseguenza, il personale del team del servizio Microsoft 365 gestisce l'ambiente tramite l'accesso remoto. Il personale del team di servizio che richiede l'accesso remoto al supporto di Microsoft 365 viene concesso l'accesso remoto solo dopo l'approvazione da un responsabile autorizzato. Tutti gli accessi a distanza utilizzano TLS compatibile con FIPS 140-2 per connessioni remote sicure.

Microsoft 365 utilizza workstation di amministrazione sicure (SAWs) per l'accesso remoto del team di servizio per proteggere gli ambienti Microsoft 365 dal compromesso. Queste workstation sono studiate appositamente per impedire la perdita intenzionale o involontaria dei dati di produzione, tra cui il blocco delle porte USB e la limitazione del software disponibile sulla sega a quanto richiesto per il supporto dell'ambiente. Le seghe sono accuratamente monitorate e controllate per rilevare e prevenire un compromesso dannoso o involontario dei dati del cliente da ingegneri Microsoft.

## <a name="how-does-customer-lockbox-add-additional-protection-for-customer-content"></a>In che modo il servizio Archivio clienti aggiunge ulteriore protezione per il contenuto dei clienti?

I clienti possono aggiungere un ulteriore livello di controllo di accesso ai propri contenuti abilitando l'archivio protetto dei clienti. Quando una richiesta di elevazione dell'archivio protetto implica l'accesso al contenuto del cliente, il servizio di archivio clienti richiede l'approvazione del cliente come passaggio finale del flusso di lavoro di approvazione. In questo modo le organizzazioni offrono la possibilità di approvare o negare queste richieste e fornisce il controllo di accesso diretto al cliente. Se il cliente rifiuta la richiesta di un archivio protetto dei clienti, l'accesso al contenuto richiesto è negato. Se il cliente non rifiuta o approva la richiesta entro un determinato periodo di tempo, la richiesta scadrà automaticamente senza che Microsoft ottenga l'accesso al contenuto del cliente. Se il cliente approva la richiesta, l'accesso temporaneo di Microsoft al contenuto del cliente verrà registrato, controllato e revocato automaticamente dopo la scadenza del tempo assegnato per completare l'operazione di risoluzione dei problemi.

## <a name="related-external-regulations--certifications"></a>Normative esterne correlate & certificazioni

I servizi online di Microsoft vengono controllati regolarmente per la conformità con le certificazioni e le normative esterne. Fare riferimento alla seguente tabella per la convalida dei controlli relativi all'identità e al controllo di accesso.

| **Verifiche esterne** | **Sezione** | **Data ultimo rapporto** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | AC-2: gestione account <br> AC-3: applicazione di accesso <br> AC-5: separazione dei compiti <br> AC-6: privilegio minimo <br> AC-17: accesso remoto | 24 settembre 2020 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Dichiarazione di applicabilità](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certificazione](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A. 9.1: requisiti aziendali per il controllo di accesso <br> A. 9.2: gestione dell'accesso degli utenti <br> A. 9.3: responsabilità degli utenti <br> A. 9.4: controllo di accesso a sistemi e applicazioni <br> A. 15.1: sicurezza delle informazioni nelle relazioni con i fornitori | 22 febbraio 2020 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Dichiarazione di applicabilità](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certificazione](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A. 9.2: gestione dell'accesso degli utenti <br> A. 9.4: controllo di accesso a sistemi e applicazioni <br> A. 15.1: sicurezza delle informazioni nelle relazioni con i fornitori | 22 febbraio 2020 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-33: modifica dell'account <br> CA-34: autenticazione dell'utente <br> CA-35: accesso con privilegi <br> CA-36: accesso remoto <br> CA-57: approvazione dell'archivio clienti di Microsoft Management <br> CA-58: richieste del servizio protetto dall'utente <br> CA-59: notifiche dell'archivio protetto dei clienti <br> CA-61: Revisione e approvazione JIT | 24 dicembre 2020 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-32: criterio account condiviso <br> CA-33: modifica dell'account <br> CA-34: autenticazione dell'utente <br> CA-35: accesso con privilegi <br> CA-36: accesso remoto <br> CA-53: monitoraggio di terze parti <br> CA-56: approvazione del cliente per l'archivio protetto dei clienti <br> CA-57: approvazione dell'archivio clienti di Microsoft Management <br> CA-58: richieste del servizio protetto dall'utente <br> CA-59: notifiche dell'archivio protetto dei clienti <br> CA-61: Revisione e approvazione JIT | 24 dicembre 2020 |
| [SOC 3 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=274054e5-4968-48d2-bf94-9a8eda5d7a93&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CUEC-15: richieste dell'archivio protetto dei clienti | 24 dicembre 2020 |