---
title: Protezione dell'infrastruttura di Microsoft 365
description: Informazioni su come Microsoft protegge l'Microsoft 365 aziendale.
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
ms.openlocfilehash: d0ef6dc92820089259cd315713c0e7e4a9e11aaec50d731b15cd6e826a721107
ms.sourcegitcommit: af1925730de60c3b698edc4e1355c38972bdd759
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/05/2021
ms.locfileid: "54292753"
---
# <a name="securing-the-microsoft-365-infrastructure"></a>Protezione dell'infrastruttura di Microsoft 365

Microsoft 365 è uno dei più grandi servizi cloud aziendali e consumer al mondo e continua a crescere rapidamente, sia nella base di clienti, nei prodotti e nelle funzionalità. I clienti si Microsoft 365 non solo per le sue soluzioni di produttività di livello mondiale, ma anche per proteggere le informazioni più sensibili dal panorama delle minacce informatiche in continua evoluzione. È la priorità principale di Microsoft mantenere sicuri i dati dei clienti e mantenere la fiducia dei clienti.

La protezione di un sistema di questa scala e complessità non è possibile se la sicurezza è un'operazione di afterthought, ma è efficace solo se la sicurezza è integrata durante il processo di progettazione iniziale. Richiede un solido sistema di rilevamento delle minacce con risposte tempestive sia da sistemi automatizzati che da tecnici altamente qualificati. La valutazione continua e la convalida di questi sistemi sono essenziali per garantire che le configurazioni sicure rimangano intatte e che siano identificate vulnerabilità sconosciute in precedenza.

## <a name="core-security-principles"></a>Principi di sicurezza di base

Sette principi di sicurezza sono alla  base del nostro framework di protezione dei servizi di Microsoft 365  dalle *minacce,* rilevamento e risposta a qualsiasi minaccia e valutazione continua della posizione della sicurezza e miglioramento dei servizi in base ai risultati di tali valutazioni.

- **Privacy dei dati:** i clienti sono proprietari dei propri dati e Microsoft è il responsabile. Microsoft 365 sono progettati per funzionare senza che i tecnici accedono ai dati dei clienti, a meno che non siano esplicitamente richiesti e approvati dal cliente.
- **Presupporre** la violazione: il personale e i servizi vengono considerati come se la compromissione fosse una possibilità reale.
- **Privilegi minimi:** l'accesso e le autorizzazioni per le risorse sono limitati solo a ciò che è necessario per eseguire le attività necessarie.
- **Limiti di violazione**: le identità e l'infrastruttura in un limite sono isolate dalle risorse in altri limiti. La compromissione di un limite non dovrebbe comportare la compromissione di un altro limite.
- **Sicurezza integrata nell'infrastruttura** di servizio : le priorità e i requisiti di sicurezza sono integrati nella progettazione di nuove funzionalità e funzionalità, garantendo che una posizione di sicurezza solida si sbiluri con ogni servizio.
- **Automatizzato** e automatico: Microsoft si concentra sullo sviluppo di prodotti e architetture durevoli in grado di applicare in modo intelligente e automatico la sicurezza dei servizi, offrendo ai tecnici Microsoft la possibilità di gestire in modo sicuro le risposte alle minacce alla sicurezza su larga scala.
- **Sicurezza adattiva:** le funzionalità di sicurezza Microsoft si adattano e sono migliorate da modelli di machine learning, test di penetrazione di routine e valutazioni automatizzate.

## <a name="protection"></a>Protezione

### <a name="access-control"></a>Controllo di accesso

Per impostazione predefinita, il personale responsabile dello sviluppo e della gestione dei Microsoft 365 dispone di zero accesso permanente (ZSA) all'infrastruttura di servizio. Mentre Microsoft cerca di assumere solo i migliori tecnici e sono necessari rigorosi controlli in background, Microsoft non presuppone che siano considerati attendibili per impostazione predefinita nei servizi operativi. Inoltre, quando i tecnici vengono approvati per l'accesso con privilegi, gli viene concesso l'accesso solo per una durata limitata per eseguire solo le azioni necessarie per uno specifico ambito dell'infrastruttura di servizio. Microsoft fa riferimento a questi criteri come Just-in-Time (JIT) e Just-Enough-Access (JEA) implementati tramite un sistema denominato Lockbox.

Per acquisire privilegi elevati, i tecnici Microsoft inviano una richiesta per l'attività specifica e specificano l'intervallo di tempo per eseguirla. Dopo l'approvazione, Lockbox genera un account JIT specializzato con la possibilità di eseguire solo l'attività richiesta. Le azioni in genere hanno la forma di flussi di lavoro automatizzati che eseguono in modo sicuro qualsiasi risoluzione dei problemi o ripristino necessario. In rari casi in cui è necessario l'accesso diretto all'infrastruttura, sono necessarie workstation con accesso con privilegi (PAW) rigorosamente monitorate.

Gli utenti non autorizzati e gli account compromessi sono una possibilità reale in qualsiasi organizzazione e il nostro sistema di controllo degli accessi è progettato per proteggere da queste minacce.

Per ulteriori informazioni sul controllo di accesso, vedere [Panoramica della gestione delle identità e degli accessi.](assurance-identity-and-access-management.md)

### <a name="encryption"></a>Crittografia

Sebbene i controlli di accesso forniranno un ruolo fondamentale nella difesa dei servizi Microsoft 365, la crittografia viene utilizzata per tutto il ciclo di vita dei dati per proteggere ulteriormente la riservatezza e la privacy per i clienti Microsoft.

I dati in transito tra computer client, Microsoft 365 server e server non Microsoft 365 vengono crittografati utilizzando TLS 1.2. Controlliamo regolarmente le crittografia e i protocolli in uso, aggiungendo protocolli migliorati quando disponibili e rimuovendo quelli più deboli in base alle esigenze.

I contenuti dei clienti in pausa nei server Microsoft vengono crittografati a livello di volume tramite BitLocker. La crittografia a livello di applicazione può inoltre essere applicata utilizzando chiavi gestite da Microsoft o dal cliente. L'accesso alle chiavi gestite da Microsoft è possibile solo se autorizzato e approvato tramite il processo JIT e JEA.

Per ulteriori informazioni sulla crittografia in Microsoft 365, vedere Panoramica della crittografia e [della gestione delle chiavi.](assurance-encryption.md)

### <a name="network-isolation"></a>Isolamento della rete

In linea con il principio dei privilegi minimi, Microsoft 365 la comunicazione tra diverse parti dell'infrastruttura di servizio solo a ciò che è necessario per operare. Tutto il traffico di rete viene negato per impostazione predefinita, con la sola comunicazione esplicitamente definita consentita. Questa restrizione definisce i limiti di violazione in tutta l'infrastruttura. Teams che desidera aggiungere nuovi percorsi di rete per supportare una nuova funzionalità al servizio deve avere la richiesta valutata e approvata prima di poter essere aperta.

Per ulteriori informazioni sull'isolamento della rete in Microsoft 365, vedere Microsoft 365 [di isolamento.](/microsoft-365/enterprise/microsoft-365-isolation-controls)

## <a name="detection--response"></a>Risposta & rilevamento

### <a name="security-monitoring"></a>Monitoraggio della sicurezza

Il monitoraggio della sicurezza su vasta scala di Microsoft è possibile solo generando avvisi altamente accurati utilizzando soluzioni automatizzate basate sul cloud. I log di controllo di ogni servizio e i dati di telemetria raccolti da tutta l'infrastruttura di base vengono inviati a una soluzione di elaborazione e avviso quasi in tempo reale centralizzata proprietaria.

Le minacce rilevate vengono corretti usando azioni attivate automaticamente quando possibile. Quando le soluzioni automatizzate non hanno successo o non sono in grado di risolvere il problema, i tecnici Microsoft a chiamata prendono immediatamente misure per attenuare la minaccia.

Per ulteriori informazioni sul monitoraggio della sicurezza in Microsoft 365, vedere [Panoramica del monitoraggio della sicurezza.](assurance-security-monitoring.md)

## <a name="assessment"></a>Valutazione

### <a name="automated-assessments"></a>Valutazioni automatizzate

Indipendentemente dalla modalità di progettazione di un sistema, la postura di sicurezza può peggiorare a causa di una deriva di configurazione intenzionale e involontaria nel tempo. Gli strumenti automatizzati valutano costantemente Microsoft 365 sistemi che ricercano servizi non stampati e non configurati correttamente. Questa valutazione viene spesso definita applicazione di patch, antivirus, vulnerabilità e analisi della configurazione (PAVC).

Anche l'architettura viene spesso convalidata, identificando le istanze, ad esempio le porte aperte e gli account inutilizzati con accesso amministrativo permanente. Tutti i servizi che derivano da uno stato desiderato predefinito vengono automaticamente allineati.

Per ulteriori informazioni sul monitoraggio della sicurezza in Microsoft 365, vedere [Panoramica della gestione delle vulnerabilità.](assurance-vulnerability-management.md)

### <a name="attack-simulation-and-penetration-testing"></a>Simulazione degli attacchi e test di penetrazione

Microsoft 365 priorità principale è impedire agli attacchi di infiltrarsi nelle difese. Microsoft 365 ha un team dedicato di esperti di sicurezza che stanno costantemente conducendo attacchi simulati per identificare vulnerabilità sconosciute in precedenza e per fornire un flusso costante di dati dettagliati per migliorare le funzionalità di monitoraggio della sicurezza. Questi attacchi simulati hanno la forma di frequenti attacchi automatici su piccola scala e immersioni approfondite guidate da esperti. Da queste attività, Microsoft valuta la capacità di rilevare, rispondere ed eviti gli utenti malintenzionati.

Per ulteriori informazioni sul monitoraggio della sicurezza in Microsoft 365, vedere [Simulazione degli attacchi in Microsoft 365](assurance-monitoring-and-testing.md).

## <a name="resources"></a>Risorse

[Dietro le quinte: proteggere l'infrastruttura potenziando il servizio Microsoft 365](https://download.microsoft.com/download/c/4/5/c45b197e-f0d9-4f40-bd5f-ed8fc7d0cd8c/M365DCSecurityIntro_Whitepaper.pdf)
