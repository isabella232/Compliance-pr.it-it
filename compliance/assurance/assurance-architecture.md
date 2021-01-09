---
title: Panoramica dell'architettura
description: Informazioni sull'architettura in Microsoft 365
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
ms.openlocfilehash: e1b4e9701e76c1e758f683750c8ebfeda2bc1f1f
ms.sourcegitcommit: 7a5b6bc58fc4613b38f3fda20aebee5cec6a5730
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "49787490"
---
# <a name="architecture-overview"></a>Panoramica dell'architettura

## <a name="what-is-microsoft-365"></a>Che cos'è Microsoft 365?

Microsoft 365 è la versione basata su cloud e su sottoscrizione di Office, Windows 10, Enterprise Mobility + Security e compliance. I clienti Microsoft 365 ricevono client quali Outlook e Windows e usufruiscono anche dei servizi ospitati da Microsoft per loro conto, ad esempio Exchange Online, Microsoft teams e SharePoint Online. Tutti i componenti del servizio vengono aggiornati regolarmente come parte del modello di sottoscrizione, in modo che i clienti abbiano un prodotto ' Evergreen '. Microsoft gestisce l'infrastruttura di servizio per conto dei clienti, pertanto Microsoft è responsabile della protezione dell'infrastruttura in cui sono archiviati i dati dei clienti.

In termini di scala, attualmente usiamo quasi un milione di macchine per alimentare i servizi di Microsoft 365. L'infrastruttura che alimenta questi servizi varia ampiamente tra l'hardware specifico del servizio e gli ambienti virtualizzati in Azure, Windows e Linux e nelle piattaforme multi-tenant e dedicate. Microsoft 365 è un'azienda globale e la nostra infrastruttura viene distribuita nei datacenter di tutto il mondo, consentendo ai clienti di soddisfare i requisiti di residenza e sovranità dei dati.

In breve, il servizio è complesso, viene eseguito su scala incredibile e richiede migliaia di ingegneri Microsoft per la creazione e la manutenzione. Questa è la priorità assoluta per garantire la sicurezza di tutte le infrastrutture.

## <a name="how-does-microsoft-365-ensure-isolation-between-customer-tenants"></a>In che modo Microsoft 365 garantisce l'isolamento tra i tenant del cliente?

I servizi cloud di Microsoft sono basati sul presupposto che tutti i tenant siano potenzialmente ostili a tutti gli altri tenant. Per isolare correttamente i tenant l'uno dall'altro, Microsoft implementa una vasta gamma di tecnologie e controlli di isolamento. Questi controlli sono stati concepiti per garantire la perdita di informazioni o l'accesso non autorizzato ai dati dei clienti tra i tenant e impedire che le azioni di un tenant influiscano negativamente sul servizio per un altro tenant.

Il contenuto del cliente è isolato logicamente all'interno dei tenant di Microsoft 365 utilizzando Azure Active Directory (Azure AD). L'autenticazione utente in Microsoft 365 verifica non solo l'identità dell'utente, ma anche l'identità del tenant di cui fa parte l'account utente, impedendo agli utenti di accedere a dati esterni all'ambiente tenant. Per completare l'isolamento logico di Azure AD, il contenuto del cliente è sempre crittografato a riposo e in transito. I singoli servizi possono inoltre fornire ulteriori livelli di isolamento del tenant, ad esempio l'isolamento di SharePoint Online dei dati del tenant in database crittografati separati.

## <a name="how-does-microsoft-365-engineer-resilient-services-that-avoid-single-points-of-failure"></a>In che modo Microsoft 365 è in grado di progettare servizi resilienti che evitano singoli punti di errore?

Microsoft progetta e crea servizi cloud per massimizzare l'affidabilità e ridurre al minimo gli effetti negativi sui clienti di fronte a errori e problemi alle normali operazioni. Questa strategia inizia con la progettazione della rete che collega i datacenter distribuiti geograficamente. L'architettura di rete di Microsoft include interconnessioni dirette e percorsi di rete multipli. I servizi Microsoft 365 sfruttano questa ridondanza per instradare automaticamente il traffico attorno a errori per migliorare la qualità del servizio.

A livello di servizio, la strategia di resilienza di Microsoft 365 dà la priorità alla resilienza del software. Laddove possibile, i servizi sono distribuiti in configurazioni attive/attive con il monitoraggio dell'integrità dei servizi automatizzati, consentendo al servizio di rilevare e recuperare da numerosi errori e guasti comuni senza l'intervento dell'uomo. Oltre alle configurazioni attive/attive, i servizi Microsoft 365 aumentano la tolleranza di errore assicurando che il servizio sia distribuito in aree di errore separate, impedendo a un errore in un'area di influenzare la disponibilità di altre aree.

La resilienza dei dati integra la resilienza del servizio proteggendo l'integrità e la disponibilità dei dati nei servizi Microsoft 365. I nostri servizi utilizzano la ridondanza di archiviazione locale e la ridondanza geografica per replicare le copie dei dati del cliente in aree di errore diverse. Se i dati vengono danneggiati o persi in un'area di errore, è possibile accedervi in un'altra area di errore senza perdita di disponibilità. Il controllo dell'integrità automatizzata ripristina automaticamente i dati interessati da molti tipi di danneggiamenti fisici o logici. Microsoft 365 fornisce inoltre ai clienti strumenti per il ripristino dei dati eliminati o modificati accidentalmente dal cliente in Exchange Online e SharePoint Online.

## <a name="how-does-microsoft-365-track-dependencies-and-prevent-unauthorized-external-system-connections"></a>In che modo Microsoft 365 tiene conto delle dipendenze e impedisce connessioni di sistema esterne non autorizzate?

I team di servizio Microsoft 365 identificano i componenti critici del sistema e le relative dipendenze nell'ambito della gestione della continuità aziendale. Inoltre, Microsoft 365 documenta e tiene traccia di tutte le connessioni di sistema esterne per garantire che siano consentite solo le connessioni autorizzate nelle configurazioni del firewall di rete. Microsoft 365 sistemi, dipendenze e connessioni esterne sono documentate nell'architettura di sicurezza delle informazioni di Microsoft 365. Sia l'architettura di sicurezza delle informazioni che i diagrammi del flusso di dati corrispondenti vengono esaminati e aggiornati ogni anno almeno ogni volta che vengono apportate modifiche significative al sistema.

L'architettura di Microsoft 365 viene convalidata regolarmente e automaticamente tramite gli strumenti basati sul cloud per verificare l'allineamento con i principi di sicurezza e per testare continuamente le funzionalità di isolamento e resilienza. La convalida dell'architettura consente di identificare automaticamente le istanze in cui lo stato corrente del servizio deriva dallo stato desiderato, contrassegnando eventuali deviazioni per la revisione e la mitigazione. L'obiettivo della convalida dell'architettura è garantire che le funzionalità di sicurezza dell'infrastruttura di servizio continuino a funzionare come previsto.

## <a name="related-external-regulations--certifications"></a>Normative esterne correlate & certificazioni

I servizi online di Microsoft vengono controllati regolarmente per la conformità con le certificazioni e le normative esterne. Fare riferimento alla seguente tabella per la convalida dei controlli relativi all'architettura di Microsoft 365.

| **Verifiche esterne** | **Sezione** | **Data ultimo rapporto** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | AC-4: applicazione del flusso di informazioni <br> CP-9: backup del sistema di informazioni <br> PL-8: architettura di sicurezza delle informazioni <br> SC-7: protezione da confini <br> SC-22: architettura e provisioning | 24 settembre 2020 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Dichiarazione di applicabilità](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certificazione](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A. 6: organizzazione della sicurezza delle informazioni <br> A. 13.1: gestione della sicurezza di rete <br> A. 17,2: ridondanze | 22 febbraio 2020 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Dichiarazione di applicabilità](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certificazione](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A. 6: organizzazione della sicurezza delle informazioni <br> A. 13.1: gestione della sicurezza di rete | 22 febbraio 2020 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-37: isolamento tenant <br> CA-49: criteri di backup <br> CA-51: replica dei dati | 24 dicembre 2020 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-05: diagrammi di flusso di dati <br> CA-37: isolamento tenant <br> CA-49: criteri di backup <br> CA-51: replica dei dati | 24 dicembre 2020 |