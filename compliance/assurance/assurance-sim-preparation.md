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
hideEdit: true
ms.openlocfilehash: b3f16620564d525245c21c375bbc9a3f5b0923b7
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497394"
---
# <a name="microsoft-365-security-incident-management-preparation"></a>Gestione degli incidenti di sicurezza di Microsoft 365: Preparazione

## <a name="training-and-background-checks"></a>Formazione e controlli in background

A ogni dipendente che lavora su Microsoft 365 viene fornita una formazione sugli incidenti di sicurezza e sulle procedure di risposta appropriate al proprio ruolo. Ogni dipendente di Microsoft 365 riceve una formazione al momento dell'adesione e ogni anno una formazione annuale per gli aggiornamenti. La formazione è progettata per fornire al dipendente una conoscenza di base dell'approccio microsoft alla sicurezza in modo che al termine della formazione tutti i dipendenti comprenda:

- Definizione di un evento imprevisto di sicurezza
- Responsabilità di tutti i dipendenti di segnalare gli incidenti di sicurezza
- Come inoltrare un potenziale incidente di sicurezza al team di Microsoft 365 Security Response
- Risposta del team di Risposta agli incidenti di sicurezza di Microsoft 365 agli incidenti di sicurezza
- Particolari problemi relativi alla privacy, in particolare alla privacy dei clienti
- Dove trovare ulteriori informazioni su sicurezza, privacy e contatti di escalation
- Eventuali altre aree di sicurezza rilevanti (in base alle esigenze)

I dipendenti appropriati ricevono una formazione di aggiornamento sulla sicurezza ogni anno. La formazione annuale sull'aggiornamento è incentrata su:

- Eventuali modifiche apportate alle procedure operative standard nell'anno precedente
- Responsabilità di tutti gli utenti di segnalare gli incidenti di sicurezza e come eseguire questa operazione
- Dove trovare ulteriori informazioni su sicurezza, privacy e contatti di escalation
- Eventuali altre aree di interesse della sicurezza che possono essere rilevanti ogni anno

Ogni dipendente che lavora a Microsoft 365 viene inoltre oggetto di un controllo approfondito e appropriato che include l'istruzione, l'occupazione, la cronologia penale del candidato e altre informazioni specifiche per le normative degli Stati Uniti, come HIPAA (Health Insurance Portability and Accountability Act), International Traffic in Arms Regulations (ITAR), Federal Risk and Authorization Management Program (FedRAMP) e altri.

I controlli in background sono obbligatori per tutti i dipendenti che lavorano nella progettazione di Microsoft 365. Alcuni ambienti e ruoli operatore di Microsoft 365 possono anche richiedere l'impronta digitale completa, i requisiti di cittadinanza, i requisiti di autorizzazione del governo e altri controlli più stringenti. Inoltre, alcuni team di servizio e ruoli possono passare attraverso una formazione di sicurezza specializzata in base alle esigenze. Infine, i membri del team di sicurezza ottengono formazione specializzata e partecipazione alle conferenze direttamente correlate alla sicurezza. Questa formazione varia in base alle necessità del team e dei dipendenti, ma include aspetti come conferenze del settore, conferenze interne di Microsoft Security e corsi di formazione esterni attraverso fornitori noti di formazione sulla sicurezza nel settore. Abbiamo anche articoli di formazione sulla sicurezza dedicati pubblicati durante tutto l'anno per la community di sicurezza di Microsoft e specializzati regolarmente in Microsoft 365.

## <a name="penetration-testing--assessment"></a>Test di penetrazione & valutazione

Microsoft collabora con diversi organismi del settore ed esperti di sicurezza per comprendere le nuove minacce e le tendenze in evoluzione. Microsoft valuta continuamente i propri sistemi per le vulnerabilità e stipula contratti con diversi esperti esterni indipendenti che fanno lo stesso.

I test eseguiti per la protezione avanzata dei servizi in Microsoft 365 possono essere raggruppati in quattro categorie generali:

1. **Test di sicurezza automatizzati:** Il personale interno ed esterno analizza regolarmente l'ambiente Di Microsoft 365 in base alle procedure SDL Microsoft, Open Web Application Security Project (OWASP) I 10 rischi principali e le minacce emergenti segnalate da diversi organismi del settore.
2. **Valutazioni delle vulnerabilità:** Gli impegni formali con tester indipendenti di terze parti verificano regolarmente se i controlli logici chiave operano in modo efficace per adempiere agli obblighi di servizio di vari organismi normativi. Le valutazioni vengono eseguite dal personale certificato CREST (Council of Registered Ethical Security Testers) e si basano sui 10 rischi OWASP Top 10 e altre minacce applicabili al servizio. Tutte le minacce trovate vengono monitorate fino alla chiusura.
3. **Test continuo delle vulnerabilità del sistema:** Microsoft esegue test regolari in cui i team tentano di violare il sistema utilizzando minacce emergenti, minacce miste e/o minacce persistenti avanzate, mentre altri team tentano di bloccare tali tentativi di violazione.
4. **Microsoft Online Services Bug Bounty Program**: Questo programma gestisce un criterio per consentire valutazioni di vulnerabilità limitate, originate dal cliente in Microsoft 365. Per ulteriori informazioni, vedere [Microsoft Online Services Bug Bounty Terms](https://www.microsoft.com/msrc/bounty-terms).

Il team di progettazione di Microsoft 365 pubblica periodicamente diversi documenti di conformità. Molti di questi documenti sono disponibili in base a un contratto di non divulgazione da [Microsoft Cloud Service Trust Portal](https://aka.ms/STP) o dall'area Service Assurance del Centro conformità Microsoft [365](https://compliance.office.com)

>[!NOTE]
>Per informazioni dettagliate su come accedere al Service Trust Portal, vedere Get started with the Service Trust Portal for Office 365 for business, Azure, and Dynamics CRM Online subscriptions. Per accedere al Centro conformità Microsoft 365 è necessario un abbonamento a Microsoft 365.

## <a name="attack-simulation"></a>Simulazione di attacco

Microsoft si impegna in esercitazioni di simulazione degli attacchi in corso e test di penetrazione in loco dei piani di sicurezza e risposta con l'intento di migliorare le funzionalità di rilevamento e risposta. Microsoft simula regolarmente violazioni reali, esegue un monitoraggio continuo della sicurezza e pratica la risposta agli incidenti di sicurezza per convalidare e migliorare la sicurezza di Microsoft 365 e Azure.

Microsoft esegue una strategia di sicurezza presuppongono la violazione utilizzando due team principali:

### <a name="red-teams"></a>Team rossi

Microsoft 365 Security Red Team è un gruppo di personale a tempo pieno all'interno di Microsoft che si concentra sulla violazione dell'infrastruttura, della piattaforma e delle applicazioni di Microsoft. Si tratta dell'avversario dedicato (un gruppo di hacker etici) che esegue attacchi mirati e persistenti contro i servizi online (ma non le applicazioni o i dati dei clienti). Forniscono una convalida continua "a spettro completo" (ad esempio, controlli tecnici, criteri cartacei, risposta umana e così via) delle funzionalità di risposta agli incidenti di servizio.

### <a name="blue-teams"></a>Team blu

Il team blu per la sicurezza di Microsoft 365 è composto da un set dedicato di risponditori di sicurezza e membri di tutti i team di intervento, progettazione e gestione degli incidenti di sicurezza. Sono indipendenti e operano separatamente dal Red Team. Il team blu segue i processi di sicurezza stabiliti e usa gli strumenti e le tecnologie più recenti per rilevare e rispondere ad attacchi e tentativi di penetrazione. Proprio come gli attacchi reali, il team blu non sa quando o come si verificheranno gli attacchi del Team Rosso o quali metodi possono essere utilizzati. Il loro compito, che si tratta di un attacco del Team Rosso o di un attacco vero e proprio, è quello di rilevare e rispondere a tutti gli incidenti di sicurezza. Per questo motivo, il team blu è costantemente in servizio e deve reagire alle violazioni del Team Rosso come farebbe per qualsiasi altro avversario.

Il personale Microsoft separa i team rossi a tempo pieno e i team blu tra Microsoft in varie divisioni che eservitino le operazioni sia tra i servizi che all'interno di essi. Denominato Red *Teaming*, l'approccio consiste nel testare i sistemi e le operazioni dei servizi Microsoft utilizzando le stesse tattiche, tecniche e procedure degli avversari reali, rispetto all'infrastruttura di produzione in tempo reale, senza l'avanza dell'infrastruttura e dei team di progettazione della piattaforma o operativi. Questo test consente di testare le funzionalità di rilevamento e risposta della sicurezza e consente di identificare le vulnerabilità di produzione, gli errori di configurazione, i presupposti non validi o altri problemi di sicurezza in modo controllato. Ogni violazione del Red Team è seguita dalla divulgazione completa tra il Team Rosso e il Team Blu, inclusi i team di servizio, per identificare le lacune, risolvere i risultati e migliorare in modo significativo la risposta alle violazioni.

>[!NOTE]
>Durante gli esercizi di red teaming o di penetrazione del sito in tempo reale non viene preso di mira alcun dato del cliente. I test sono in base all'infrastruttura e alle piattaforme di Microsoft 365 e Azure, nonché ai tenant, alle applicazioni e ai dati di Microsoft. I tenant dei clienti, le applicazioni e i dati ospitati in Microsoft 365 o Azure non sono mai mirati in base alle regole di coinvolgimento concordate.

### <a name="joint-exercises"></a>Esercitazioni congiunte

A volte, i team blu e rosso di Microsoft 365 Security eseguiranno operazioni congiunte in cui la relazione durante l'operazione è più partner che contraddittoria con un set selezionato di dipendenti di ogni team. Questi esercizi sono ben coordinati tra i team per guidare un insieme più mirato di risultati attraverso la collaborazione in tempo reale tra hacker e risponditori etici. Questi esercizi del "team viola" sono altamente personalizzati per ogni operazione per ottimizzare le opportunità, ma fondamentale per ogni operazione è la condivisione delle informazioni a larghezza di banda elevata e la collaborazione per raggiungere gli obiettivi.

## <a name="related-articles"></a>Articoli correlati

- [Gestione degli incidenti di sicurezza di Microsoft 365](assurance-security-incident-management.md)
- [Rilevamento e analisi della gestione degli incidenti di sicurezza di Microsoft 365](assurance-sim-detection-analysis.md)
- [Microsoft 365 security incident management containment, eradication, and recovery](assurance-sim-containment-eradication-recovery.md)
- [Attività post-incidente di gestione degli incidenti di sicurezza di Microsoft 365](assurance-sim-post-incident-activity.md)
