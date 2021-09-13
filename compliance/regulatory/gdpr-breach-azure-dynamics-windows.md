---
title: Notifica di violazione di Azure, Dynamics 365 e Windows ai sensi del GDPR
description: Informazioni su come Azure e Dynamics 365 proteggono da una violazione dei dati personali e su come Microsoft gestisce un'eventuale violazione e lo comunica agli utenti interessati.
keywords: Azure, Microsoft 365, Dynamics 365, documentazione di Microsoft 365, GDPR
ms.localizationpriority: high
ms.prod: microsoft-365-enterprise
ms.topic: article
f1.keywords:
- NOCSH
ms.author: robmazz
author: robmazz
manager: laurawi
audience: itpro
ms.collection:
- GDPR
- M365-security-compliance
- MS-Compliance
titleSuffix: Microsoft GDPR
hideEdit: true
ms.openlocfilehash: 23d6b1ebb30f34fcb549e3e1f44c98a0c0e11b12
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/12/2021
ms.locfileid: "59159726"
---
# <a name="azure-dynamics-365-and-windows-breach-notification-under-the-gdpr"></a>Notifica di violazione di Azure, Dynamics 365 e Windows ai sensi del GDPR

Microsoft prende in seria considerazione gli obblighi previsti dal Regolamento generale sulla protezione dei dati (GDPR). Microsoft adotta ampie misure di sicurezza nei servizi online per proteggere gi utenti dalle violazioni dei dati. Queste misure includono controlli di sicurezza sia fisica che logica, così come processi di sicurezza automatizzati, criteri completi di sicurezza delle informazioni e privacy, nonché formazione sulla sicurezza e sulla privacy per tutto il personale.

La sicurezza è integrata in Microsoft Azure, a partire dal [Security Development Lifecycle](https://www.microsoft.com/sdl/), un processo di sviluppo obbligatorio che incorpora le metodologie di privacy by design e privacy by default. Il principio guida della strategia di sicurezza di Microsoft consiste nel "presumere la violazione", che è un'estensione della strategia di difesa in profondità. Mettendo costantemente alla prova le funzionalità di sicurezza di Azure, Microsoft può stare al passo con le minacce emergenti. Per altre informazioni sulla sicurezza di Azure, consultare queste [risorse](https://www.microsoft.com/trustcenter/security/azure-security).

Microsoft dispone di un servizio globale di risposta agli incidenti, attivo 24 ore su 24 e 7 giorni su 7, che opera per mitigare gli effetti degli attacchi contro Microsoft Azure. Come attestato da più controlli di sicurezza e conformità (ad es. [ISO/IEC 27018](offering-iso-27018.md)), Microsoft segue nei suoi data center operazioni e processi rigorosi per prevenire accessi non autorizzati, tra cui monitoraggio video 24 ore su 24, 7 giorni su 7, personale di sicurezza addestrato, smart card e controlli biometrici.

## <a name="detection-of-potential-breaches"></a>Rilevamento di potenziali violazioni

A causa della natura del cloud computing moderno, non tutte le violazioni dei dati che si verificano in un ambiente cloud dei clienti implicano servizi di Microsoft Azure. Microsoft utilizza un modello di responsabilità condivisa per i servizi di Azure per definire la sicurezza e le responsabilità operative. La responsabilità condivisa è importante quando si parla di sicurezza di un servizio cloud, poiché sia il fornitore di servizi cloud sia il cliente sono responsabili di diverse parti della sicurezza del cloud.

Microsoft non monitora né risponde agli incidenti di sicurezza nell'ambito di responsabilità del cliente. Una compromissione della sicurezza che coinvolge esclusivamente il cliente non verrebbe considerata un incidente di sicurezza di Azure e gestire la risposta sarebbe responsabilità del tenant del cliente. La risposta del cliente in caso di incidente può implicare la collaborazione con il [supporto tecnico](https://azure.microsoft.com/support/options/) di Microsoft Azure, in base ai contratti di servizio appropriati. Microsoft Azure offre inoltre vari servizi (ad es., [Centro sicurezza di Azure](https://azure.microsoft.com/services/security-center/)) che i clienti possono utilizzare per lo sviluppo e la gestione della risposta agli incidenti di sicurezza.

Azure risponde a una potenziale violazione dei dati in base al processo di risposta agli incidenti di sicurezza, che è un sottoinsieme del piano di gestione degli incidenti di Microsoft Azure. La risposta agli incidenti di sicurezza di Microsoft Azure viene implementata tramite un processo costituito da cinque fasi: rilevamento, valutazione, diagnostica, stabilizzazione e chiusura. Il team dedicato può alternare le fasi di diagnosi e stabilizzazione man mano che l'indagine procede. Di seguito è riportata una panoramica del processo di risposta agli incidenti di sicurezza:

| Fase | Descrizione |
|:------- |------------- |
| ***1: Rilevamento*** | Prima indicazione di un potenziale incidente. |
| ***2: Valutazione*** | Un tecnico di turno del team di intervento per gli incidenti valuta l'impatto e la gravità dell'incidente. Secondo le prove raccolte, la valutazione può comportare o meno un'ulteriore escalation al team di intervento della sicurezza. |
| ***3: Diagnostica*** | Gli esperti del team di intervento della sicurezza svolgono le indagini tecniche o forensi, identificano le strategie di contenimento, mitigazione e le soluzioni alternative. Se il team della sicurezza ritiene che i dati del cliente potrebbero essere stati esposti a un individuo non autorizzato o a un criminale, il processo di notifica dell'incidente al cliente si svolge in parallelo. |
| ***4: Stabilizzazione e ripristino*** | Il team di intervento per gli incidenti crea un piano di ripristino per mitigare il problema. Le misure di contenimento della crisi, come l'applicazione della quarantena ai sistemi colpiti, possono verificarsi immediatamente e parallelamente alla fase di diagnosi. Si possono pianificare misure di mitigazione a lungo termine da implementare dopo che è passato il rischio immediato. |
| ***5: Chiusura e relazione finale*** | Il team di intervento per gli incidenti crea una relazione finale dettagliata dell'incidente finalizzata alla revisione di criteri, procedure e interventi per prevenire il ripetersi dell'evento. |

I processi di rilevamento utilizzati da Microsoft Azure sono progettati per rilevare eventi che mettono a rischio la riservatezza, l'integrità e la disponibilità dei servizi di Azure. Diversi eventi possono dare il via a un'indagine:

- Avvisi di sistema automatici tramite framework di monitoraggio e avviso interni. Questi avvisi potrebbero interferire con avvisi basati su firma come antimalware, rilevamento di intrusioni o tramite algoritmi progettati per tracciare il profilo dell'attività prevista e segnalare anomalie.
- Report di prima parte dei servizi Microsoft in esecuzione su Microsoft Azure e Azure per enti pubblici.
- Le vulnerabilità di sicurezza vengono segnalate a [Microsoft Security Response Center (MSRC)](https://www.microsoft.com/msrc) tramite [Segnalare un problema](https://msrc.microsoft.com/create-report). MSRC collabora con partner e ricercatori di sicurezza di tutto il mondo per prevenire gli incidenti e migliorare la sicurezza dei prodotti Microsoft.
- Report dei clienti tramite il [portale del supporto tecnico](https://www.windowsazure.com/support/contact/) o il portale di Microsoft Azure e Azure per enti pubblici, che descrivono attività sospette attribuite all'infrastruttura di Azure (al contrario delle attività che si verificano nell'ambito di responsabilità del cliente).
- Attività di [Red Team e Blue Team](https://azure.microsoft.com/blog/red-teaming-using-cutting-edge-threat-simulation-to-harden-the-microsoft-enterprise-cloud/) per la sicurezza. Questa strategia utilizza un Red Team altamente qualificato di esperti di sicurezza offensiva di Microsoft per individuare e attaccare potenziali vulnerabilità in Azure. Il Blue Team di intervento per la sicurezza deve rilevare e difendersi dall'attività del Read Team. Le azioni del Red team e del Blue Team vengono usate per verificare che gli interventi per la sicurezza di Azure gestiscano in modo efficace gli incidenti. Le attività di sicurezza del Red Team e del Blue Team vengono gestite secondo regole di ingaggio per garantire la protezione dei dati dei clienti.
- Escalation da parte degli operatori di servizi di Azure. I dipendenti Microsoft sono addestrati per identificare e inoltrare potenziali problemi riguardanti la sicurezza.

## <a name="azures-data-breach-response"></a>Intervento in caso di violazione dei dati di Azure

Microsoft assegna all'indagine i livelli di priorità e gravità appropriati determinando l'impatto funzionale, la ripristinabilità e l'impatto informativo dell'evento imprevisto. Sia la priorità che la gravità possono cambiare nel corso dell'indagine, in base a nuovi risultati e conclusioni. Gli eventi di sicurezza che comportano rischi imminenti o confermati per i dati dei clienti vengono trattati come gravità elevata e vengono risolti 24 ore su 24.

Il team di Security Response collabora con Microsoft Azure Security Engineers e SME per classificare l'evento sulla base di dati concreti tratti dalle prove raccolte. Un incidente di sicurezza può essere classificato come:

- **Falso positivo**: evento che soddisfa i criteri di rilevamento, ma che fa parte di una normale pratica aziendale e potrebbe essere necessario escluderlo. I team del servizio identificheranno la causa radice dei falsi positivi e li risolveranno in modo sistematico per ottimizzarli in base alle esigenze.
- **Evento di sicurezza**: si è verificato un evento osservabile in un sistema, un servizio e/o una rete per tentativi di attacco, aggirare i controlli di sicurezza. Oppure un problema identificato in cui i fatti indicano che i dati del cliente o i dati personali potrebbero essere stati persi, eliminati, modificati, divulgati o accessibili senza autorizzazione.
- **Incidente di sicurezza/Evento imprevisto per la sicurezza segnalabile dal cliente/Evento imprevisto sulla privacy (CRSPI)**: una violazione confermata (ad esempio dichiarata) della sicurezza che causa la distruzione accidentale o illecita, la perdita, l'alterazione, la divulgazione non autorizzata o l'accesso ai dati personali o ai dati personali dei clienti durante l'elaborazione da parte di Microsoft.
- **Evento sulla privacy**: un evento di sicurezza che influisce sui dati personali o sul trattamento dei dati che comporta conseguenze impreviste per la privacy, tra cui la non conformità alle informative sulla privacy, agli standard e ai controlli Microsoft.
- **Incidente sulla privacy/Evento imprevisto per la sicurezza segnalabile dal cliente/Evento imprevisto sulla privacy (CRSPI)**: un evento imprevisto di sicurezza che influisce sui dati personali, sui dati o sull'elaborazione dei dati che comporta conseguenze impreviste per la privacy, tra cui la mancata conformità alle informative sulla privacy, agli standard e ai controlli Microsoft.

Affinché un incidente di sicurezza segnalabile dal cliente possa essere dichiarato, Microsoft deve stabilire che l'accesso non autorizzato ai dati del cliente è avvenuto o probabilmente si è verificato e/o che esiste un impegno legale o contrattuale perché si verifichi la notifica. È auspicabile, ma non è necessario, conoscere lo specifico impatto sul cliente, l'accesso alle risorse e i passaggi di ripristino. Un incidente di sicurezza è generalmente dichiarato incidente di sicurezza segnalabile dal cliente dopo la conclusione della fase di diagnosi; tuttavia, la dichiarazione può avvenire in qualsiasi momento in cui tutte le informazioni pertinenti siano disponibili.

Microsoft verifica che il rischio per il cliente e per l'azienda sia contenuto e che vengano implementate misure correttive. Se necessario, vengono adottate misure di attenuazione dell'emergenza per risolvere i rischi di sicurezza immediati associati all'evento.

Microsoft also completes an internal post-mortem for data breaches. As a part of this exercise, sufficiency of response and operating procedures are evaluated, and any updates that may be necessary to the Security Incident Response SOP or related processes are identified and implemented. Internal postmortems for data breaches are highly confidential records not available to customers. Postmortems may, however, be summarized and included in other customer event notifications. These reports are provided to external auditors for review as part of Azure's routine audit cycle.

## <a name="customer-notification"></a>Notifica al cliente

Microsoft notifica le violazioni dei dati ai clienti e agli organismi di certificazione, come richiesto. Microsoft si basa su una forte compartimentazione interna nel funzionamento di Azure. Anche i registri del flusso di dati sono solidi. A vantaggio di questa struttura, la maggior parte degli incidenti può essere indirizzata a clienti specifici. L'obiettivo è fornire ai clienti interessati un avviso accurato, attuabile e tempestivo nel momento in cui i dati vengono violati.

Dopo aver dichiarato un CRSPI, il processo di notifica si verificherà nel modo più rapido possibile, pur considerando i rischi per la sicurezza del passaggio rapido. In generale, il processo di stesura delle notifiche avviene quando l'indagine sull'incidente è in corso. Le notifiche ai cliente vengono recapitate entro 72 ore dall'identificazione di una violazione *tranne* nei casi seguenti:

- Microsoft ritiene che l'azione di esecuzione di una notifica aumenti il rischio per gli altri clienti. Ad esempio, l'azione di notifica può fornire un suggerimento a un antagonista causando l'impossibilità di correggere.
- Altre circostanze insolite o estreme esaminate dall'ufficio legale di Microsoft e dall'Executive Incident Manager.
- Nelle 72 ore potrebbero essere disponibili alcuni dettagli sull'incidente. Questi vengono forniti ai clienti e alle autorità di regolamentazione man mano che procedono le indagini.

Microsoft fornisce ai clienti informazioni dettagliate affinché possano svolgere indagini interne e rispettare gli impegni assunti con gli utenti finali, senza ritardare ingiustificatamente il processo di notifica.

La notifica di una violazione dei dati personali verrà recapitata al cliente interessato con qualsiasi mezzo scelto da Microsoft, anche tramite posta elettronica. La notifica di una violazione dei dati verrà inviata all'elenco dei contatti di sicurezza specificato nel Centro sicurezza di Azure, che può essere configurato seguendo le [linee guida per l'implementazione](/azure/security-center/security-center-provide-security-contact-details). Se le informazioni sui contatti non sono disponibili nel Centro sicurezza di Azure, la notifica verrà inviata a uno o più amministratori di una sottoscrizione di Azure. Per fare in modo che la notifica possa essere recapitata correttamente, il cliente è tenuto a verificare la correttezza delle informazioni sui contatti amministrativi relative a ogni sottoscrizione e portale dei servizi online applicabile.

Il team di Microsoft Azure o di Azure per enti pubblici può anche decidere di notificare ulteriori informazioni al personale Microsoft, ad esempio il servizio clienti (CSS) e l'Account Manager del cliente (AM) o il Technical Account Manager (TAM). Tali figure hanno spesso strette relazioni con il cliente e possono facilitare una correzione più rapida.

## <a name="microsoft-dynamics-365-built-in-security-features"></a>Funzionalità di sicurezza integrate in Microsoft Dynamics 365

Microsoft Dynamics 365 si avvale dell'infrastruttura dei servizi del cloud e delle funzionalità di protezione integrate per proteggere i dati attraverso meccanismi e misure di sicurezza. Inoltre, Dynamics 365 fornisce accesso efficiente ai dati e collaborazione con l'integrità dei dati e la privacy nelle aree seguenti: [protezione dell'identità, protezione dei dati, protezione basata sui ruoli e gestione delle minacce](https://www.microsoft.com/trustcenter/security/dynamics365-security).

L'offerta Microsoft Dynamics 365 segue le stesse misure tecniche e organizzative adottate da uno o più team di servizi di Microsoft Azure per garantire la protezione dai processi di violazione dei dati. Di conseguenza, tutte le informazioni riportate nel documento di notifica "Violazioni di dati in Microsoft Azure" sono applicabili anche a Microsoft Dynamics 365.

## <a name="windows-diagnostic-data-processor-configuration"></a>Configurazione del processore dati di diagnostica Windows

La [configurazione del processore dati di diagnostica Windows](/windows/privacy/configure-windows-diagnostic-data-in-your-organization) sfrutta l'infrastruttura del servizio cloud e le funzionalità di sicurezza predefinite per garantire la sicurezza dei dati usando misure e meccanismi di sicurezza per proteggere i dati.

Segue le stesse misure tecniche e organizzative adottate da uno o più team di servizi di Microsoft Azure per garantire la protezione dai processi di violazione dei dati. Pertanto, tutte le informazioni documentate nel documento di notifica "violazione dei dati Microsoft Azure" sono analoghe anche alla configurazione del processore dati di diagnostica Windows.

## <a name="learn-more"></a>Ulteriori informazioni

[Centro protezione Microsoft](https://www.microsoft.com/trust-center/privacy/gdpr-overview)
