---
title: 'Gestione degli incidenti di sicurezza Microsoft: preparazione'
description: In questo articolo viene fornita una panoramica del processo di preparazione della gestione degli incidenti di sicurezza nei servizi online Microsoft.
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.localizationpriority: medium
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
ms.openlocfilehash: ca194511e000a7d98ddd89ae9ef85a1ee1ee01bd
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/12/2021
ms.locfileid: "59159559"
---
# <a name="microsoft-security-incident-management-preparation"></a>Gestione degli incidenti di sicurezza Microsoft: preparazione

## <a name="training-and-background-checks"></a>Formazione e controlli in background

Ogni dipendente che lavora ai servizi online Microsoft viene fornito con formazione sugli incidenti di sicurezza e sulle procedure di risposta appropriate al proprio ruolo. Ogni dipendente Microsoft riceve una formazione al momento della partecipazione e una formazione annuale per l'aggiornamento ogni anno. La formazione è progettata per fornire al dipendente una conoscenza di base dell'approccio microsoft alla sicurezza in modo che al termine della formazione tutti i dipendenti comprenda:

- Definizione di un evento imprevisto di sicurezza
- Responsabilità di tutti i dipendenti di segnalare gli incidenti di sicurezza
- Come inoltrare un potenziale incidente di sicurezza al team di risposta alla sicurezza Microsoft appropriato
- Risposta dei team di risposta agli incidenti di sicurezza Microsoft agli incidenti di sicurezza
- Particolari problemi relativi alla privacy, in particolare alla privacy dei clienti
- Dove trovare ulteriori informazioni su sicurezza, privacy e contatti di escalation
- Eventuali altre aree di sicurezza rilevanti (in base alle esigenze)

I dipendenti appropriati ricevono una formazione di aggiornamento sulla sicurezza ogni anno. La formazione annuale sull'aggiornamento è incentrata su:

- Eventuali modifiche apportate alle procedure operative standard nell'anno precedente
- Responsabilità di tutti gli utenti di segnalare gli incidenti di sicurezza e come eseguire questa operazione
- Dove trovare ulteriori informazioni su sicurezza, privacy e contatti di escalation
- Eventuali altre aree di interesse della sicurezza che possono essere rilevanti ogni anno

Ogni dipendente che lavora ai servizi online Microsoft è soggetto a un controllo approfondito e appropriato che include l'istruzione, l'impiego, la cronologia penale del candidato e altre informazioni specifiche in base alle normative degli Stati Uniti, come HIPAA (Health Insurance Portability and Accountability Act), International Traffic in Arms Regulations (ITAR), Federal Risk and Authorization Management Program (FedRAMP) e altri.

I controlli in background sono obbligatori per tutti i dipendenti che lavorano all'interno di Microsoft Engineering. Alcuni ambienti di servizi online Microsoft e ruoli dell'operatore possono anche richiedere l'impronta digitale completa, i requisiti di cittadinanza, i requisiti di autorizzazione del governo e altri controlli più stringenti. Inoltre, alcuni team di servizio e ruoli possono passare attraverso una formazione di sicurezza specializzata in base alle esigenze. Infine, i membri del team di sicurezza ottengono formazione specializzata e partecipazione alle conferenze direttamente correlate alla sicurezza. Questa formazione varia in base alle necessità del team e dei dipendenti, ma include aspetti come conferenze del settore, conferenze interne di Microsoft Security e corsi di formazione esterni attraverso fornitori noti di formazione sulla sicurezza nel settore. Abbiamo anche articoli di formazione sulla sicurezza dedicati pubblicati durante tutto l'anno per la community di sicurezza di Microsoft e specializzati regolarmente nei servizi online Microsoft.

## <a name="penetration-testing--assessment"></a>Test di penetrazione & valutazione

Microsoft collabora con diversi organismi del settore ed esperti di sicurezza per comprendere le nuove minacce e le tendenze in evoluzione. Microsoft valuta continuamente i propri sistemi per le vulnerabilità e stipula contratti con diversi esperti esterni indipendenti che fanno lo stesso.

I test eseguiti per la protezione avanzata dei servizi all'interno dei servizi online Microsoft possono essere raggruppati in quattro categorie generali:

1. **Test di sicurezza automatizzati:** Il personale interno ed esterno analizza regolarmente gli ambienti dei servizi online Microsoft in base alle procedure SDL Microsoft, Open Web Application Security Project (OWASP) I 10 rischi principali e le minacce emergenti segnalate da diversi organismi del settore.
2. **Valutazioni delle vulnerabilità:** Gli impegni formali con tester indipendenti di terze parti verificano regolarmente se i controlli logici chiave operano in modo efficace per adempiere agli obblighi di servizio di vari organismi normativi. Le valutazioni vengono eseguite dal personale certificato CREST (Council of Registered Ethical Security Testers) e si basano sui 10 rischi OWASP Top 10 e altre minacce applicabili al servizio. Tutte le minacce trovate vengono monitorate fino alla chiusura.
3. **Test continuo delle vulnerabilità del sistema:** Microsoft esegue test regolari in cui i team tentano di violare il sistema utilizzando minacce emergenti, minacce miste e/o minacce persistenti avanzate, mentre altri team tentano di bloccare tali tentativi di violazione.
4. **Microsoft Online Services Bug Bounty Program**: Questo programma gestisce un criterio per consentire valutazioni di vulnerabilità limitate, originate dal cliente nei servizi online Microsoft. Per ulteriori informazioni, vedere [Microsoft Online Services Bug Bounty Terms](https://www.microsoft.com/msrc/bounty-terms).

I team di progettazione dei servizi online Microsoft pubblicano periodicamente diversi documenti di conformità. Molti di questi documenti sono disponibili nell'ambito di un contratto di non divulgazione da [Microsoft Cloud Service Trust Portal](https://aka.ms/STP) o dall'area Service Assurance del [Centro conformità Microsoft 365](https://compliance.office.com)

>[!NOTE]
>Per informazioni dettagliate su come accedere al Service Trust Portal, vedere Get started with the Service Trust Portal for Office 365 for business, Azure, and Dynamics CRM Online subscriptions. È Microsoft 365 una sottoscrizione per accedere al Centro conformità Microsoft 365.

## <a name="attack-simulation"></a>Simulazione di attacco

Microsoft si impegna in esercitazioni di simulazione degli attacchi in corso e test di penetrazione in siti live dei piani di sicurezza e risposta con l'intento di migliorare le funzionalità di rilevamento e risposta. Microsoft simula regolarmente violazioni reali, esegue un monitoraggio continuo della sicurezza e pratica la risposta agli incidenti di sicurezza per convalidare e migliorare la sicurezza dei servizi online Microsoft.

Microsoft esegue una strategia di sicurezza presuppongono la violazione utilizzando due team principali:

### <a name="red-teams"></a>Team rossi

I team di Microsoft Red sono gruppi di personale a tempo pieno all'interno di Microsoft che si concentrano sulla violazione dell'infrastruttura, della piattaforma e delle applicazioni di Microsoft. Si tratta dell'avversario dedicato (un gruppo di hacker etici) che esegue attacchi mirati e persistenti contro i servizi online (ma non le applicazioni o i dati dei clienti). Forniscono una convalida continua "a spettro completo" (ad esempio, controlli tecnici, criteri cartacei, risposta umana e così via) delle funzionalità di risposta agli incidenti di servizio.

### <a name="blue-teams"></a>Team blu

I team Microsoft Blue sono composti da set dedicati di risponditori di sicurezza e membri di tutti i team di risposta agli incidenti di sicurezza, progettazione e operazioni. Sono indipendenti e operano separatamente dai team red. I team blu seguono i processi di sicurezza stabiliti e utilizzano gli strumenti e le tecnologie più recenti per rilevare e rispondere ad attacchi e tentativi di penetrazione. Proprio come gli attacchi reali, i team blu non sanno quando o come si verificheranno gli attacchi del team rosso o quali metodi possono essere utilizzati. Il loro compito, che si tratta di un attacco del team rosso o di un attacco vero e proprio, è quello di rilevare e rispondere a tutti gli incidenti di sicurezza. Per questo motivo, i team blu sono costantemente a chiamata e devono reagire alle violazioni del team rosso come farebbe per qualsiasi altro avversario.

Il personale Microsoft separa i team rossi a tempo pieno e i team blu di Microsoft in varie divisioni che eservitino le operazioni sia tra i servizi che all'interno di essi. Noto come *Red Teaming,* l'approccio consiste nel testare i sistemi e le operazioni di servizi Microsoft usando le stesse tattiche, tecniche e procedure degli avversari reali, rispetto all'infrastruttura di produzione in tempo reale, senza il foreknowledge dell'infrastruttura e dei team di progettazione della piattaforma o operativi. Questo test consente di testare le funzionalità di rilevamento e risposta della sicurezza e consente di identificare le vulnerabilità di produzione, gli errori di configurazione, i presupposti non validi o altri problemi di sicurezza in modo controllato. Ogni violazione del team rosso è seguita dalla divulgazione completa tra il team rosso e il team blu, inclusi i team di servizio, per identificare le lacune, risolvere i risultati e migliorare in modo significativo la risposta alle violazioni.

>[!NOTE]
>Durante gli esercizi di red teaming o di penetrazione del sito in tempo reale non viene preso di mira alcun dato del cliente. I test sono a Microsoft 365 infrastruttura e piattaforme di Azure, oltre ai tenant, alle applicazioni e ai dati di Microsoft. I tenant dei clienti, le applicazioni e i dati ospitati in Azure, Dynamics 365 o Microsoft 365 non sono mai mirati in base alle regole di coinvolgimento concordate.

### <a name="joint-exercises"></a>Esercitazioni congiunte

A volte, i team Microsoft Blue e Red condurranno operazioni congiunte in cui la relazione durante l'operazione è più partner che contraddittoria con un set selezionato di dipendenti di ogni team. Questi esercizi sono ben coordinati tra i team per guidare un insieme più mirato di risultati attraverso la collaborazione in tempo reale tra hacker e risponditori etici. Questi esercizi del "team viola" sono altamente personalizzati per ogni operazione per ottimizzare l'opportunità, ma fondamentale per ogni operazione è la condivisione delle informazioni a larghezza di banda elevata e la collaborazione per raggiungere gli obiettivi.

## <a name="related-articles"></a>Articoli correlati

- [Gestione degli incidenti di sicurezza Microsoft](assurance-security-incident-management.md)
- [Gestione degli incidenti di sicurezza Microsoft: rilevamento e analisi](assurance-sim-detection-analysis.md)
- [Gestione degli incidenti di sicurezza Microsoft: contenimento, eliminazione e ripristino](assurance-sim-containment-eradication-recovery.md)
- [Gestione degli incidenti di sicurezza Microsoft: attività post-incidente](assurance-sim-post-incident-activity.md)
- [Come registrare un ticket di supporto per gli eventi di sicurezza](/azure/security/fundamentals/event-support-ticket)
- [Notifica di violazione nell'ambito del GDPR in Azure e Dynamics 365](/compliance/regulatory/gdpr-breach-azure-dynamics)