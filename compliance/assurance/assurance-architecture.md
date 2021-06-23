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
hideEdit: true
ms.openlocfilehash: 9af5296cce34db6362638f025f38315f2e1d7b05
ms.sourcegitcommit: fb379d1110a9a86c7f9bab8c484dc3f4b3dfd6f0
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/23/2021
ms.locfileid: "53088535"
---
# <a name="architecture-overview"></a>Panoramica dell'architettura

## <a name="what-is-microsoft-365"></a>Che cos'è Microsoft 365?

Microsoft 365 è la versione basata su sottoscrizione basata su cloud di Office, Windows 10, Enterprise Mobility + Security e conformità. Microsoft 365 clienti ottengono client come Outlook e Windows e beneficiano anche di servizi ospitati da Microsoft per loro conto, ad esempio Exchange Online, Microsoft Teams e SharePoint Online. Tutti i componenti del servizio vengono aggiornati regolarmente come parte del modello di sottoscrizione, in modo che i nostri clienti hanno un prodotto "sempreverde". Microsoft gestisce l'infrastruttura di servizio per conto dei clienti, il che significa che Microsoft è responsabile della protezione dell'infrastruttura che archivia i dati dei clienti.

In termini di scala, attualmente usiamo quasi un milione di computer per alimentare Microsoft 365 servizi. L'infrastruttura di alimentazione di questi servizi varia notevolmente nell'hardware specifico del servizio e negli ambienti virtualizzati in Azure, Windows e Linux e nelle piattaforme multi-tenant e dedicate. Microsoft 365 è un'azienda globale e l'infrastruttura è distribuita in data center in tutto il mondo, consentendo ai clienti di soddisfare i requisiti di residenza e sovranità dei dati.

In breve, il servizio è complesso, viene eseguito su scala incredibile e richiede migliaia di tecnici Microsoft per la creazione e la manutenzione. È nostra priorità mantenere sicura tutta questa infrastruttura.

## <a name="how-does-microsoft-365-ensure-isolation-between-customer-tenants"></a>In che modo Microsoft 365 l'isolamento tra i tenant dei clienti?

I servizi cloud di Microsoft si basano sul presupposto che tutti i tenant siano potenzialmente dannosi per tutti gli altri tenant. Per isolare correttamente i tenant l'uno dall'altro, Microsoft implementa un'ampia gamma di tecnologie e controlli di isolamento. Questi controlli sono progettati per evitare perdite di informazioni o accessi non autorizzati ai dati dei clienti nei tenant e per impedire che le azioni di un tenant influiscano negativamente sul servizio per un altro tenant.

Il contenuto del cliente è isolato logicamente Microsoft 365 tenant usando Azure Active Directory (Azure AD). L'autenticazione utente in Microsoft 365 verifica non solo l'identità utente, ma anche l'identità del tenant di cui fa parte l'account utente, impedendo agli utenti di accedere ai dati all'esterno dell'ambiente tenant. Per integrare l'isolamento logico di Azure AD, il contenuto del cliente viene sempre crittografato in fase di riposo e in transito. I singoli servizi possono inoltre fornire livelli aggiuntivi di isolamento del tenant, ad esempio l SharePoint in linea dei dati del tenant in database separati crittografati.

## <a name="how-does-microsoft-365-engineer-resilient-services-that-avoid-single-points-of-failure"></a>In che modo Microsoft 365 servizi resilienti che evitano singoli punti di errore?

Microsoft progetta e crea servizi cloud per ottimizzare l'affidabilità e ridurre al minimo gli effetti negativi sui clienti di fronte a errori e sfide alle normali operazioni. Questa strategia inizia con la progettazione della rete che collega i datacenter geograficamente distribuiti. L'architettura di rete di Microsoft include interconnessioni dirette e più percorsi di rete. Microsoft 365 servizi sfruttano questa ridondanza per instradare automaticamente il traffico intorno agli errori per migliorare la qualità del servizio.

A livello di servizio, la Microsoft 365 di resilienza assegna priorità alla resilienza del software. Ove possibile, i servizi vengono distribuiti in configurazioni attive/attive con il monitoraggio automatico dell'integrità dei servizi, consentendo al servizio di rilevare e ripristinare da molti errori e errori comuni senza l'intervento umano. Oltre alle configurazioni attive/attive, i servizi di Microsoft 365 aumentano la tolleranza di errore assicurando che il servizio sia distribuito in aree di errore separate, impedendo che un errore in una zona influisca sulla disponibilità di altre aree.

La resilienza dei dati integra la resilienza del servizio proteggendo l'integrità e la disponibilità dei dati nei Microsoft 365 servizi. I nostri servizi usano la ridondanza di archiviazione locale e la ridondanza geografica per replicare le copie dei dati dei clienti in diverse aree di errore. Se i dati sono danneggiati o persi in una zona di errore, è possibile accedervi in un'altra zona di errore senza perdita di disponibilità. Il controllo automatico dell'integrità ripristina automaticamente i dati influenzati da molti tipi di danneggiamento fisico o logico. Microsoft 365 fornisce inoltre ai clienti strumenti per ripristinare i dati eliminati o modificati accidentalmente dal cliente in Exchange Online e SharePoint Online.

## <a name="how-does-microsoft-365-track-dependencies-and-prevent-unauthorized-external-system-connections"></a>In che modo Microsoft 365 tenere traccia delle dipendenze e impedire connessioni al sistema esterno non autorizzate?

Microsoft 365 team di servizio identificano i componenti di sistema critici e le relative dipendenze nell'ambito della gestione della continuità aziendale. Inoltre, è Microsoft 365 e tiene traccia di tutte le connessioni al sistema esterno per garantire che solo le connessioni autorizzate siano consentite nelle configurazioni del firewall di rete. Microsoft 365, le dipendenze e le connessioni esterne sono documentate nell'architettura Microsoft 365 sicurezza delle informazioni. Sia l'architettura di sicurezza delle informazioni che i diagrammi del flusso di dati corrispondenti vengono esaminati e aggiornati ogni anno come minimo, nonché ogni volta che vengono apportate modifiche significative al sistema.

Microsoft 365'architettura viene convalidata regolarmente e automaticamente usando strumenti basati su cloud per verificare l'allineamento con i principi di sicurezza e per testare continuamente le funzionalità di isolamento e resilienza. La convalida dell'architettura consente di identificare automaticamente le istanze in cui lo stato corrente del servizio si è allontanato dallo stato desiderato, contrassegnando eventuali deviazioni per la revisione e la mitigazione. L'obiettivo della convalida dell'architettura è garantire che le funzionalità di sicurezza dell'infrastruttura di servizio continuino a funzionare come previsto.

## <a name="related-external-regulations--certifications"></a>Normative esterne correlate & certificazioni

I servizi online di Microsoft vengono regolarmente controllati per la conformità alle normative e alle certificazioni esterne. Fare riferimento alla tabella seguente per la convalida dei controlli correlati all'architettura di Microsoft 365.

| **Controlli esterni** | **Sezione** | **Data ultimo report** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | AC-4: applicazione del flusso di informazioni <br> CP-9: backup del sistema di informazioni <br> PL-8: architettura di sicurezza delle informazioni <br> SC-7: Protezione dei limiti <br> SC-22: architettura e provisioning | 24 settembre 2020 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Dichiarazione di applicabilità](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Certificazione](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.6: Organizzazione della sicurezza delle informazioni <br> A.13.1: Gestione della sicurezza di rete <br> A.17.2: Licenzianze | 20 aprile 2021 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Dichiarazione di applicabilità](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Certificazione](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.6: Organizzazione della sicurezza delle informazioni <br> A.13.1: Gestione della sicurezza di rete | 20 aprile 2021 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-37: Isolamento tenant <br> CA-49: Criteri di backup <br> CA-51: Replica dei dati | 24 dicembre 2020 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-05: Diagrammi del flusso di dati <br> CA-37: Isolamento tenant <br> CA-49: Criteri di backup <br> CA-51: Replica dei dati | 24 dicembre 2020 |