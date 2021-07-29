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
ms.openlocfilehash: ecb66b923f1d9ce239000910ad282ae3e69514de
ms.sourcegitcommit: 76553d505d88ea868622bebebda17c27df5f7a39
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/28/2021
ms.locfileid: "53617687"
---
# <a name="architecture-overview"></a>Panoramica dell'architettura

## <a name="what-are-microsoft-online-services"></a>Che cosa sono i servizi online Microsoft?

I servizi online Microsoft fanno riferimento ai servizi basati sul cloud offerti da Microsoft, che includono Azure, Dynamics 365 e Microsoft 365.  Ogni servizio offre soluzioni uniche per le esigenze di produttività e di funzionamento aziendali comuni, al servizio dei clienti di tutto il mondo, dalle piccole imprese alle grandi imprese e ai governi. I data center distribuiti a livello globale connessi dall'infrastruttura di rete gestita in modo indipendente da Microsoft fungono da backbone per supportare i servizi online, offrendo la possibilità di mantenere la disponibilità in quasi tutte le situazioni e di scalare in base a una domanda globale di grandi dimensioni.

Tutti i servizi online Microsoft hanno lo stesso obiettivo di salvaguardare l'infrastruttura di servizio che gestiscono e i dati dei clienti, ma ogni servizio online è gestito da una business unit separata. In molti casi, i controlli di sicurezza vengono implementati nello stesso modo in tutti i servizi, ma in alcuni casi hanno un approccio diverso per adempiere alle promesse dei clienti e agli obblighi di conformità.

## <a name="what-is-azure"></a>Che cos'è Azure?

Microsoft Azure è una piattaforma di cloud computing per la creazione, la distribuzione e la gestione di applicazioni tramite una rete globale di datacenter gestiti da Microsoft e di terze parti. Supporta i modelli di servizio cloud Platform as a Service (PaaS) e Infrastructure as a Service (IaaS) e consente soluzioni ibride che integrano i servizi cloud con le risorse locali dei clienti. Microsoft Azure supporta molti clienti, partner e organizzazioni governative che si estendono su un'ampia gamma di prodotti e servizi, aree geografiche e settori. Microsoft Azure è progettato per soddisfare i requisiti di sicurezza, riservatezza e conformità.

## <a name="what-is-dynamics-365"></a>Che cos'è Dynamics 365?

Dynamics 365 è una famiglia di applicazioni aziendali online che integra le funzionalità crm (Customer Relationship Management) e le relative estensioni con le funzionalità ERP (Enterprise Resource Planning). Queste applicazioni aziendali end-to-end consentono ai clienti di trasformare le relazioni in ricavi, guadagnare clienti e accelerare la crescita aziendale. Dynamics 365 è una famiglia di prodotti Software as a Service (SaaS) che si basa sull'infrastruttura di Azure ed è resa disponibile per i clienti di tutto il mondo tramite i datacenter distribuiti a livello globale.

## <a name="what-is-microsoft-365"></a>Che cos'è Microsoft 365?

Microsoft 365 è la versione basata su sottoscrizione basata su cloud di Office, Windows 10, Enterprise Mobility + Security e conformità. Microsoft 365 clienti ottengono client come Outlook e Windows e beneficiano anche di servizi ospitati da Microsoft per loro conto, ad esempio Exchange Online, Microsoft Teams e SharePoint Online. Tutti i componenti del servizio vengono aggiornati regolarmente come parte del modello di sottoscrizione, in modo che i nostri clienti hanno un prodotto "sempreverde". Microsoft gestisce l'infrastruttura di servizio per conto dei clienti, il che significa che Microsoft è responsabile della protezione dell'infrastruttura che archivia i dati dei clienti.

In termini di scalabilità, Microsoft attualmente usa quasi un milione di computer per alimentare Microsoft 365 servizi. L'infrastruttura di alimentazione di questi servizi varia notevolmente nell'hardware specifico del servizio e negli ambienti virtualizzati in Azure, Windows e Linux e nelle piattaforme multi-tenant e dedicate. Microsoft 365 è un'azienda globale e l'infrastruttura è distribuita in data center in tutto il mondo, consentendo ai clienti di soddisfare i requisiti di residenza e sovranità dei dati.

## <a name="how-do-microsoft-online-services-ensure-isolation-between-customer-tenants"></a>In che modo i servizi online Microsoft garantiscono l'isolamento tra i tenant dei clienti?

I servizi cloud di Microsoft si basano sul presupposto che tutti i tenant siano potenzialmente dannosi per tutti gli altri tenant. Per isolare correttamente i tenant l'uno dall'altro, Microsoft implementa diverse tecnologie e controlli di isolamento. Questi controlli sono progettati per evitare perdite di informazioni o accessi non autorizzati ai dati dei clienti nei tenant e per impedire che le azioni di un tenant influiscano negativamente sul servizio per un altro tenant.

Il contenuto dei clienti è isolato logicamente all'interno dei tenant tramite Azure Active Directory (Azure AD). L'autenticazione utente nei Servizi online Microsoft verifica non solo l'identità utente, ma anche l'identità del tenant di cui fa parte l'account utente, impedendo agli utenti di accedere ai dati all'esterno dell'ambiente tenant. Per integrare l'isolamento logico di Azure AD, il contenuto del cliente viene sempre crittografato in fase di riposo e in transito. I singoli servizi possono inoltre fornire livelli aggiuntivi di isolamento del tenant, ad esempio l SharePoint in linea dei dati del tenant in database separati crittografati.

## <a name="how-do-microsoft-online-services-engineer-resilient-services-that-avoid-single-points-of-failure"></a>In che modo i Servizi online Microsoft possono progettare servizi resilienti che evitano singoli punti di errore?

Microsoft progetta e crea servizi cloud per ottimizzare l'affidabilità e ridurre al minimo gli effetti negativi sui clienti di fronte a errori e sfide alle normali operazioni. Questa strategia inizia con la progettazione della rete che collega i datacenter geograficamente distribuiti. L'architettura di rete di Microsoft include interconnessioni dirette e più percorsi di rete. I servizi online Microsoft usano questa ridondanza per instradare automaticamente il traffico intorno agli errori per migliorare la qualità del servizio.

Se possibile, i servizi online Microsoft vengono distribuiti in configurazioni attive/attive con monitoraggio automatico dell'integrità dei servizi, consentendo al servizio di rilevare e ripristinare da molti errori e errori comuni senza l'intervento umano. Oltre alle configurazioni attive/attive, i servizi online Microsoft aumentano la tolleranza di errore assicurando che il servizio sia distribuito in aree di errore separate, impedendo a un errore in un'area di influire sulla disponibilità di altre aree.

La resilienza dei dati integra la resilienza del servizio proteggendo l'integrità e la disponibilità dei dati nei servizi online Microsoft. I nostri servizi usano la ridondanza di archiviazione locale e la ridondanza geografica per replicare le copie dei dati dei clienti in diverse aree di errore. Se i dati sono danneggiati o persi in una zona di errore, è possibile accedervi in un'altra zona di errore senza perdita di disponibilità. Il controllo automatico dell'integrità ripristina automaticamente i dati influenzati da molti tipi di danneggiamento fisico o logico. Microsoft fornisce inoltre ai clienti strumenti per ripristinare i dati eliminati o modificati accidentalmente dal cliente in servizi come Exchange Online e SharePoint Online.

## <a name="how-do-microsoft-online-services-track-dependencies-and-prevent-unauthorized-external-system-connections"></a>In che modo i servizi online Microsoft rilevano le dipendenze e impediscono connessioni al sistema esterno non autorizzate?

I team dei servizi online Microsoft identificano i componenti di sistema critici e le relative dipendenze nell'ambito della gestione della continuità aziendale. Inoltre, Microsoft documenta e tiene traccia di tutte le connessioni al sistema esterno per garantire che solo le connessioni autorizzate siano consentite nelle configurazioni del firewall di rete. I sistemi, le dipendenze e le connessioni esterne dei Servizi online Microsoft sono documentati nell'architettura di sicurezza delle informazioni dei Servizi online Microsoft. Sia l'architettura di sicurezza delle informazioni che i diagrammi del flusso di dati corrispondenti vengono esaminati e aggiornati ogni anno come minimo, nonché ogni volta che vengono apportate modifiche significative al sistema.

L'architettura dei servizi online Microsoft viene convalidata regolarmente e automaticamente utilizzando strumenti basati su cloud per verificare l'allineamento con i principi di sicurezza e per testare continuamente le funzionalità di isolamento e resilienza. La convalida dell'architettura consente di identificare automaticamente le istanze in cui lo stato corrente del servizio si è allontanato dallo stato desiderato, contrassegnando eventuali deviazioni per la revisione e la mitigazione. L'obiettivo della convalida dell'architettura è garantire che le funzionalità di sicurezza dell'infrastruttura di servizio continuino a funzionare come previsto.

## <a name="related-external-regulations--certifications"></a>Normative esterne correlate & certificazioni

I servizi online di Microsoft vengono regolarmente controllati per la conformità alle normative e alle certificazioni esterne. Fare riferimento alla tabella seguente per la convalida dei controlli correlati all'architettura.

### <a name="azure-and-dynamics-365"></a>Azure e Dynamics 365

| **Controlli esterni** | **Sezione** | **Data ultimo report** |
|:--------------------|:------------|:-----------------------|
| [ISO 27001/27002](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Dichiarazione di applicabilità](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=00af6c3e-7f3e-4e0d-8b0e-79f45ef2cef1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Certificazione](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7af5304-3a31-40e6-9abb-e26352305d41&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.6: Organizzazione della sicurezza delle informazioni <br> A.13.1: Gestione della sicurezza di rete <br> A.17.2: Licenzianze | 2 dicembre 2020 |
| [ISO 27017](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Dichiarazione di applicabilità](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a3bca0ac-867d-4204-b66b-13665f5f1e8d&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Certificazione](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=25718a8a-f34d-41e1-a95a-c49246508787&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.6: Organizzazione della sicurezza delle informazioni <br> A.13.1: Gestione della sicurezza di rete <br> A.17.2: Licenzianze | 2 dicembre 2020 |
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b8721ebd-af20-42fe-b22f-8332b0a19517&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=234a0f57-83c1-4afc-a586-a0e7a59592f7&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 3](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=75c8cbf6-e456-473c-a05e-34fea888ec2a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | BC-1: Piani di continuità aziendale <br> BC-3: procedure BCDR <br> BC-4: test BCDR <br> BC-5: Valutazioni dei rischi di continuità aziendale <br> BC-6: continuità aziendale di terze parti <br> BC-7: procedure di continuità aziendale del datacenter <br> BC-8: Test di continuità aziendale del datacenter <br> BC-9: valutazione della resilienza del datacenter <br>  DS-6: ridondanza di componenti critici <br> DS-7: replica dei dati dei clienti <br> DS-14: Ripristino dei servizi clienti <br> DS-16: separazione dei dati dei clienti | 31 marzo 2021 |

### <a name="office-365"></a>Office 365

| **Controlli esterni** | **Sezione** | **Data ultimo report** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP](https://compliance.microsoft.com/compliancemanager) | AC-4: applicazione del flusso di informazioni <br> CP-9: backup del sistema di informazioni <br> PL-8: architettura di sicurezza delle informazioni <br> SC-7: Protezione dei limiti <br> SC-22: architettura e provisioning | 24 settembre 2020 |
| [ISO 27001/27002/27017](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Dichiarazione di applicabilità](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.6: Organizzazione della sicurezza delle informazioni <br> A.13.1: Gestione della sicurezza di rete <br> A.17.2: Licenzianze | 20 aprile 2021 |
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-37: Isolamento tenant <br> CA-49: Criteri di backup <br> CA-51: Replica dei dati | 24 dicembre 2020 |
| [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-05: Diagrammi del flusso di dati <br> CA-37: Isolamento tenant <br> CA-49: Criteri di backup <br> CA-51: Replica dei dati | 24 dicembre 2020 |