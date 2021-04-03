---
title: Panoramica sulla gestione delle identità e degli accessi
description: Informazioni sulla gestione di identità e accessi in Microsoft 365
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
ms.openlocfilehash: d431a7f04b156b003f5f4e213aef9bb9792874fe
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497162"
---
# <a name="identity-and-access-management-overview"></a>Panoramica sulla gestione delle identità e degli accessi

## <a name="how-does-microsoft-365-protect-production-systems-from-unauthorized-or-malicious-access"></a>In che modo Microsoft 365 protegge i sistemi di produzione da accessi non autorizzati o dannosi?

Microsoft 365 è progettato per consentire ai tecnici Microsoft di gestire il servizio senza accedere ai contenuti dei clienti. Per impostazione predefinita, i tecnici di Microsoft 365 hanno accesso zero permanente (ZSA) al contenuto del cliente e nessun accesso privilegiato all'ambiente di produzione. Microsoft 365 usa un modello JIT (Just-In-Time), Just-Enough-Access (JEA) per fornire ai tecnici del team di assistenza l'accesso con privilegi temporanei agli ambienti di produzione quando tale accesso è necessario per supportare Microsoft 365. Il modello di accesso JIT sostituisce l'accesso amministrativo permanente tradizionale con un processo che consente ai tecnici di richiedere l'elevazione temporanea dei ruoli con privilegi quando necessario.

I tecnici assegnati a un team di servizio per supportare i servizi di produzione richiedono l'idoneità per un account del team di servizio tramite lo strumento di gestione delle identità (IDM). La richiesta di idoneità attiva una serie di controlli del personale per garantire che il tecnico abbia superato tutti i requisiti di screening cloud, abbia completato la formazione necessaria e abbia ricevuto l'approvazione della gestione appropriata prima della creazione dell'account. Solo dopo aver soddisfatti tutti i requisiti di idoneità, è possibile creare un account del team di servizio per l'ambiente richiesto.

Gli account del team di servizio non concedono privilegi di amministratore permanente o accesso al contenuto del cliente. Quando un tecnico richiede l'accesso aggiuntivo per supportare il servizio Microsoft 365, richiede l'accesso temporaneo con privilegi elevati alle risorse necessarie usando uno strumento di gestione degli accessi denominato Lockbox. Lockbox limita l'accesso con privilegi elevati ai privilegi minimi, alle risorse e al tempo necessari per completare l'attività assegnata. Se un revisore autorizzato approva la richiesta di accesso JIT, al tecnico viene concesso un account temporaneo con solo i privilegi necessari per completare il lavoro assegnato. Questo account temporaneo richiede l'autenticazione a più fattori e viene eliminato automaticamente alla scadenza del periodo approvato.

## <a name="how-does-microsoft-365-handle-remote-access-to-production-systems"></a>In che modo Microsoft 365 gestisce l'accesso remoto ai sistemi di produzione?

I componenti di sistema di Microsoft 365 sono ospitati in datacenter geograficamente separati dai team di gestione. Il personale del datacenter non ha accesso logico ai sistemi Microsoft 365. Di conseguenza, il personale del team del servizio Microsoft 365 gestisce l'ambiente tramite accesso remoto. Al personale del team del servizio che richiede l'accesso remoto per supportare Microsoft 365 viene concesso l'accesso remoto solo dopo l'approvazione da parte di un manager autorizzato. Tutti gli accessi remoti utilizzano TLS compatibile FIPS 140-2 per connessioni remote sicure.

Microsoft 365 usa Secure Admin Workstations (SAWs) per l'accesso remoto del team di servizio per proteggere gli ambienti Microsoft 365 da una compromissione. Queste workstation sono progettate in modo specifico per impedire la perdita intenzionale o involontaria dei dati di produzione, tra cui il blocco delle porte USB e la limitazione del software disponibile nel SAW a ciò che è necessario per supportare l'ambiente. I saW sono monitorati e monitorati per rilevare e prevenire la compromissione dannosa o accidentale dei dati dei clienti da parte dei tecnici Microsoft.

## <a name="how-does-customer-lockbox-add-additional-protection-for-customer-content"></a>In che modo Customer Lockbox aggiunge ulteriore protezione per i contenuti dei clienti?

I clienti possono aggiungere un ulteriore livello di controllo di accesso al contenuto abilitando Customer Lockbox. Quando una richiesta di elevazione lockbox implica l'accesso al contenuto del cliente, Customer Lockbox richiede l'approvazione del cliente come passaggio finale nel flusso di lavoro di approvazione. In questo modo le organizzazioni possono approvare o rifiutare queste richieste e fornisce il controllo di accesso diretto al cliente. Se il cliente rifiuta una richiesta Customer Lockbox, l'accesso al contenuto richiesto viene negato. Se il cliente non rifiuta o approva la richiesta entro un determinato periodo, la richiesta scadrà automaticamente senza che Microsoft oseva l'accesso al contenuto del cliente. Se il cliente approva la richiesta, l'accesso temporaneo di Microsoft al contenuto del cliente verrà registrato, controllabile e revocato automaticamente alla scadenza del tempo assegnato per completare l'operazione di risoluzione dei problemi.

## <a name="related-external-regulations--certifications"></a>Normative esterne correlate & certificazioni

I servizi online di Microsoft vengono regolarmente controllati per la conformità alle normative e alle certificazioni esterne. Per la convalida dei controlli relativi all'identità e al controllo di accesso, fare riferimento alla tabella seguente.

| **Controlli esterni** | **Sezione** | **Data ultimo report** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | AC-2: Gestione account <br> AC-3: applicazione dell'accesso <br> AC-5: separazione dei compiti <br> AC-6: privilegi minimi <br> AC-17: Accesso remoto | 24 settembre 2020 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Dichiarazione di applicabilità](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certificazione](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.9.1: Requisiti aziendali del controllo di accesso <br> A.9.2: Gestione dell'accesso utente <br> A.9.3: Responsabilità degli utenti <br> A.9.4: Controllo dell'accesso a sistema e applicazioni <br> A.15.1: Sicurezza delle informazioni nelle relazioni con i fornitori | 22 febbraio 2020 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Dichiarazione di applicabilità](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certificazione](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.9.2: Gestione dell'accesso utente <br> A.9.4: Controllo dell'accesso a sistema e applicazioni <br> A.15.1: Sicurezza delle informazioni nelle relazioni con i fornitori | 22 febbraio 2020 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-33: Modifica dell'account <br> CA-34: autenticazione utente <br> CA-35: Accesso con privilegi <br> CA-36: Accesso remoto <br> CA-57: Approvazione della gestione Microsoft Customer Lockbox <br> CA-58: Richieste del servizio Customer Lockbox <br> CA-59: Notifiche di Customer Lockbox <br> CA-61: revisione e approvazione JIT | 24 dicembre 2020 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-32: Criteri account condivisi <br> CA-33: Modifica dell'account <br> CA-34: autenticazione utente <br> CA-35: Accesso con privilegi <br> CA-36: Accesso remoto <br> CA-53: Monitoraggio di terze parti <br> CA-56: Approvazione del cliente Customer Lockbox <br> CA-57: Approvazione della gestione Microsoft Customer Lockbox <br> CA-58: Richieste del servizio Customer Lockbox <br> CA-59: Notifiche di Customer Lockbox <br> CA-61: revisione e approvazione JIT | 24 dicembre 2020 |
| [SOC 3 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=274054e5-4968-48d2-bf94-9a8eda5d7a93&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CUEC-15: richieste Customer Lockbox | 24 dicembre 2020 |