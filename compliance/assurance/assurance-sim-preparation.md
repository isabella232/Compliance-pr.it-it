---
title: 'Gestione degli incidenti di sicurezza di Microsoft 365: Preparazione'
description: In questo articolo viene fornita una panoramica del processo di preparazione della gestione degli incidenti di sicurezza in Microsoft 365.
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
f1.keywords:
- NOCSH
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: b14a9fa236cd71cff7dd02baf04a30c249bc4346
ms.sourcegitcommit: 2973d25e9e0185b84d281f963553a332eac1c1a3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/28/2021
ms.locfileid: "50040339"
---
# <a name="microsoft-365-security-incident-management-preparation"></a>Gestione degli incidenti di sicurezza di Microsoft 365: Preparazione

## <a name="training-and-background-checks"></a>Formazione e controlli in background

A ogni dipendente che lavora su Microsoft 365 viene fornita una formazione sugli incidenti di sicurezza e sulle procedure di risposta appropriate al proprio ruolo. Ogni dipendente di Microsoft 365 riceve una formazione al momento della partecipazione e una formazione annuale per gli aggiornamenti ogni anno. La formazione è progettata per fornire al dipendente una conoscenza di base dell'approccio di Microsoft alla sicurezza, in modo che, al termine della formazione, tutti i dipendenti comprenda:

- Definizione di un incidente di sicurezza
- Responsabilità di tutti i dipendenti di segnalare gli incidenti di sicurezza
- Come inoltrare un potenziale incidente di sicurezza al team di Microsoft 365 Security Response
- Risposta del team di Risposta agli incidenti di sicurezza di Microsoft 365 agli incidenti di sicurezza
- Problemi speciali relativi alla privacy, in particolare alla privacy dei clienti
- Dove trovare ulteriori informazioni su sicurezza e privacy e contatti di escalation
- Eventuali altre aree di sicurezza rilevanti (in base alle esigenze)

I dipendenti appropriati ricevono una formazione più aggiornata sulla sicurezza ogni anno. La formazione annuale per gli aggiornamenti è incentrata su:

- Eventuali modifiche apportate alle procedure operative standard nell'anno precedente
- Responsabilità di tutti gli utenti di segnalare gli incidenti di sicurezza e come procedere
- Dove trovare ulteriori informazioni su sicurezza e privacy e contatti di escalation
- Eventuali altre aree di interesse della sicurezza che possono essere rilevanti ogni anno

Ogni dipendente che lavora a Microsoft 365 deve inoltre eseguire un controllo approfondito e appropriato del background che include l'istruzione, l'impiego, la storia penale del candidato e altre informazioni specifiche in base alle normative degli Stati Uniti, come HIPAA (Health Insurance Portability and Accountability Act), International Traffic in Arms Regulations (ITAR), Federal Risk and Authorization Management Program (FedRAMP) e altri.

I controlli in background sono obbligatori per tutti i dipendenti che lavorano all'interno di Microsoft 365 Engineering. Alcuni ambienti Microsoft 365 e ruoli dell'operatore possono anche richiedere l'impronta digitale completa, i requisiti di cittadinanza, i requisiti di autorizzazione per il governo e altri controlli più stringenti. Inoltre, alcuni team di servizio e ruoli possono passare attraverso una formazione specializzata sulla sicurezza in base alle esigenze. Infine, i membri del team di sicurezza ottengono una formazione specializzata e la partecipazione alle conferenze direttamente correlate alla sicurezza. Questa formazione varia in base alle necessità del team e dei dipendenti, ma include aspetti come conferenze del settore, conferenze interne sulla sicurezza Microsoft e corsi di formazione esterni attraverso noti fornitori di formazione sulla sicurezza nel settore. Abbiamo anche articoli dedicati alla formazione sulla sicurezza pubblicati durante tutto l'anno per la community della sicurezza di Microsoft e specializzati regolarmente in Microsoft 365.

## <a name="penetration-testing--assessment"></a>Test di penetrazione & valutazione

Microsoft collabora con diversi organismi del settore ed esperti della sicurezza per comprendere le nuove minacce e le tendenze in evoluzione. Microsoft valuta continuamente i propri sistemi per le vulnerabilità e stipula contratti con diversi esperti esterni indipendenti che fanno lo stesso.

I test eseguiti per la protezione avanzata dei servizi in Microsoft 365 possono essere raggruppati in quattro categorie generali:

1. **Test di sicurezza automatizzati:** Il personale interno ed esterno analizza regolarmente l'ambiente Microsoft 365 in base alle procedure SDL di Microsoft, ai 10 rischi principali di Open Web Application Security Project (OWASP) e alle minacce emergenti segnalate da diversi organismi del settore.
2. **Valutazioni della vulnerabilità:** Gli impegni formali con tester indipendenti di terze parti verificano regolarmente se i controlli logici chiave operano in modo efficace per soddisfare gli obblighi di servizio di vari organismi normativi. Le valutazioni vengono eseguite dal personale certificato CREST (Council of Registered Ethical Security Testers) e si basano sui 10 rischi OWASP Top 10 e altre minacce applicabili ai servizi. Tutte le minacce rilevate vengono monitorate fino alla chiusura.
3. **Test continui della vulnerabilità del sistema:** Microsoft esegue test regolari in cui i team tentano di violare il sistema utilizzando minacce emergenti, minacce miste e/o minacce persistenti avanzate, mentre altri team tentano di bloccare tali tentativi di violazione.
4. **Microsoft Online Services Bug Bounty Program:** questo programma gestisce un criterio che consente valutazioni limitate, originate dal cliente, della vulnerabilità in Microsoft 365. Per ulteriori informazioni, vedere [Microsoft Online Services Bug Bounty Terms.](https://www.microsoft.com/msrc/bounty-terms)

Il team di progettazione di Microsoft 365 pubblica periodicamente diversi documenti di conformità. Molti di questi documenti sono disponibili nell'ambito di un contratto di non divulgazione da [Microsoft Cloud Service Trust Portal](https://aka.ms/STP) o dall'area Service Assurance del Centro conformità Microsoft [365](https://compliance.office.com)

>[!NOTE]
>Per informazioni dettagliate su come accedere al Service Trust Portal, vedere Introduzione al Service Trust Portal per gli abbonamenti a Office 365 per le aziende, Azure e Dynamics CRM Online. È necessario un abbonamento a Microsoft 365 per accedere al Centro conformità Microsoft 365.

## <a name="attack-simulation"></a>Simulazione degli attacchi

Microsoft si impegna in esercitazioni di simulazione degli attacchi in corso e test di penetrazione del sito in tempo reale dei piani di sicurezza e risposta con l'intento di migliorare le funzionalità di rilevamento e risposta. Microsoft simula regolarmente violazioni del mondo reale, esegue un monitoraggio continuo della sicurezza e pratica la risposta agli incidenti di sicurezza per convalidare e migliorare la sicurezza di Microsoft 365 e Azure.

Microsoft esegue una strategia di sicurezza presupporre che si utilizzino due team di base:

### <a name="red-teams"></a>Team rossi

Il team rosso per la sicurezza di Microsoft 365 è un gruppo di personale a tempo pieno all'interno di Microsoft che si concentra sulla violazione dell'infrastruttura, della piattaforma e delle applicazioni di Microsoft. Sono gli avversari dedicati (un gruppo di hacker etici) che eseguono attacchi mirati e persistenti contro i servizi online (ma non le applicazioni o i dati dei clienti). Forniscono una convalida "completa" continua (ad esempio, controlli tecnici, criteri cartacei, risposta umana e così via) delle funzionalità di intervento in caso di incidenti di servizio.

### <a name="blue-teams"></a>Team blu

Il team blu per la sicurezza di Microsoft 365 è costituito da un set dedicato di risponditori della sicurezza e membri di tutti i team di intervento, progettazione e gestione degli incidenti di sicurezza. Sono indipendenti e operano separatamente dal Team Rosso. Il team blu segue i processi di sicurezza stabiliti e utilizza gli strumenti e le tecnologie più recenti per rilevare e rispondere ad attacchi e tentativi di penetrazione. Proprio come gli attacchi del mondo reale, il team blu non sa quando o come si verificheranno gli attacchi del Team Rosso o quali metodi possono essere utilizzati. Il loro compito, che si tratta di un attacco del team rosso o di un attacco vero e proprio, è quello di rilevare e rispondere a tutti gli incidenti di sicurezza. Per questo motivo, il Team blu è costantemente in servizio e deve rispondere alle violazioni del Red Team allo stesso modo di qualsiasi altro antagono.

Il personale Microsoft separa i team rossi a tempo pieno e i team blu tra Microsoft in varie divisioni che eservino operazioni sia tra i servizi che all'interno di essi. Denominato Red *Teaming,* l'approccio consiste nel testare i sistemi e le operazioni dei servizi Microsoft usando le stesse tattiche, tecniche e procedure degli antagoni reali, rispetto all'infrastruttura di produzione in tempo reale, senza il foreknowledge dell'infrastruttura e dei team tecnici o operativi della piattaforma. Questo test consente di testare le funzionalità di rilevamento e risposta della sicurezza e consente di identificare le vulnerabilità di produzione, gli errori di configurazione, i presupposti non validi o altri problemi di sicurezza in modo controllato. Ogni violazione del Red Team è seguita dalla divulgazione completa tra il team rosso e il team blu, inclusi i team di servizio, per identificare le lacune, risolvere i risultati e migliorare significativamente la risposta alle violazioni.

>[!NOTE]
>Nessun dato del cliente viene mirato durante gli esercizi di red teaming o di penetrazione del sito in tempo reale. I test sono in base all'infrastruttura e alle piattaforme di Microsoft 365 e Azure, nonché ai tenant, alle applicazioni e ai dati di Microsoft. I tenant dei clienti, le applicazioni e i dati ospitati in Microsoft 365 o Azure non sono mai mirati in base alle regole di coinvolgimento concordate.

### <a name="joint-exercises"></a>Esercitazioni congiunte

In alcuni casi, i team blu e rosso della sicurezza di Microsoft 365 condurranno operazioni congiunte in cui la relazione durante l'operazione è più partner che antagonale con un set selezionato di dipendenti di ogni team. Questi esercizi sono ben coordinati tra i team per guidare un set di risultati più mirato attraverso la collaborazione in tempo reale tra hacker e risponditori etici. Questi esercizi del "team viola" sono altamente personalizzati per ogni operazione per ottimizzare le opportunità, ma fondamentale per ogni operazione è la condivisione di informazioni a larghezza di banda elevata e la collaborazione per raggiungere gli obiettivi.

## <a name="related-articles"></a>Articoli correlati

- [Gestione degli incidenti di sicurezza di Microsoft 365](assurance-security-incident-management.md)
- [Rilevamento e analisi degli incidenti di sicurezza di Microsoft 365](assurance-sim-detection-analysis.md)
- [Contenimento, eliminazione e ripristino della gestione degli incidenti di sicurezza di Microsoft 365](assurance-sim-containment-eradication-recovery.md)
- [Attività post-incidente di gestione degli incidenti di sicurezza di Microsoft 365](assurance-sim-post-incident-activity.md)
