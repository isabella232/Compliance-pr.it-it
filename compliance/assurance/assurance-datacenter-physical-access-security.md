---
title: Sicurezza dell'accesso fisico del datacenter
description: Ulteriori informazioni sulla sicurezza dell'accesso fisico del datacenter Microsoft.
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
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
f1.keywords:
- NOCSH
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: f7cc71354c4be52d97c8b4b6efbe5a88ca9413a5
ms.sourcegitcommit: cf424cb1e7c12048120977f294f780b776119a96
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/11/2021
ms.locfileid: "60265113"
---
# <a name="datacenter-physical-access-security"></a>Sicurezza dell'accesso fisico del datacenter

Microsoft comprende l'importanza di proteggere i dati dei clienti e si impegna a proteggere i data center che li contengono. I data center Microsoft sono progettati, creati e gestiti per limitare rigorosamente l'accesso fisico alle aree in cui sono archiviati i dati dei clienti.

La sicurezza fisica nei datacenter è allineata al principio di difesa approfondita. Vengono implementate più misure di sicurezza per ridurre il rischio che utenti non autorizzati accedono ai dati e ad altre risorse del datacenter.

- **Sicurezza perimetrale:** i data center Microsoft sono edifici non-script con scherma perimetrale e illuminazione esterna 24 ore su 24. I recinti alti in acciaio e cemento comprendono ogni pollice del perimetro e tutti gli accessi al campus del datacenter devono passare attraverso un punto di accesso ben definito. I cancelli di ingresso monitorati dalla videocamera e le guardie di sicurezza assicurano che l'ingresso e l'uscita siano limitati alle aree designate. I dissuasori e altre misure proteggono l'esterno del data center da potenziali minacce, incluso l'accesso non autorizzato.
- **Ingresso nel datacenter**: L'ingresso del datacenter è associato a responsabili della sicurezza professionali che hanno subito rigorosi controlli di formazione e di background. I responsabili della sicurezza sorvegliano regolarmente il datacenter e i feed video dalle fotocamere all'interno del datacenter vengono sempre monitorati.
- **All'interno del centro** dati: quando si entra nell'edificio, è necessaria l'autenticazione a due fattori con biometria per continuare a spostarsi attraverso il datacenter. Una volta autenticato, l'accesso viene concesso alla parte autorizzata del datacenter e solo per il tempo approvato. All'interno del datacenter, le aree designate come estremamente sensibili richiedono un'ulteriore autenticazione a due fattori.
- **Piano del datacenter:** è possibile accedere al centro dati solo con l'approvazione precedente e dopo uno screening di rilevamento full body metal al momento dell'immissione. Per ridurre il rischio di dati non autorizzati che entrano o lasciano il datacenter, solo i dispositivi approvati possono entrare nel centro dati. Inoltre, le videocamere monitorano la parte anteriore e posteriore di ogni rack del server. Quando si esce dal centro dati, tutti gli utenti sono soggetti a un ulteriore screening di rilevamento full body metal.
- **Uscita dal datacenter:** per uscire dalla struttura del datacenter, ogni persona deve passare attraverso un checkpoint di sicurezza finale e tutti i visitatori devono rinunciare ai badge temporanei. Dopo la raccolta, tutti i badge dei visitatori hanno rimosso i livelli di accesso prima di essere riutilizzati per le visite future.

## <a name="access-provisioning"></a>Provisioning dell'accesso

Il team di gestione del datacenter (DCM) ha implementato procedure operative per limitare l'accesso fisico solo a dipendenti, appaltatori e visitatori autorizzati. Le richieste di accesso temporaneo o permanente vengono monitorate tramite un sistema di ticketing. I badge vengono emessi o attivati per il personale che richiede l'accesso dopo la verifica dell'identificazione. Le chiavi fisiche e le notifiche di accesso temporaneo sono protette all'interno del centro operativo di sicurezza (SOC).

I data center Microsoft sono soggetti a criteri di accesso con privilegi minimi, il che significa che l'accesso al datacenter è limitato al personale con un'esigenza aziendale approvata, senza più accesso del necessario. Le richieste di accesso sono limitate nel tempo e vengono rinnovate solo se le esigenze operative del richiedente rimangono valide.

I record di accesso al datacenter vengono gestiti sotto forma di richieste approvate. Le richieste possono essere approvate solo dal team DCM e le richieste di accesso dei visitatori ai datacenter vengono registrate e rese disponibili per eventuali indagini future

## <a name="datacenter-security-personnel"></a>Personale di sicurezza del datacenter

Il personale di sicurezza nelle strutture del datacenter e nel campus è responsabile delle attività seguenti:

- Utilizzare le workstation che si trovano nel Centro operativo di sicurezza all'interno dell'edificio di amministrazione principale.
- Eseguire ispezioni periodiche tramite procedure dettagliate e pattuglie della struttura.
- Rispondere agli allarmi antincendio e ai problemi di sicurezza
- Inviare personale di sicurezza per assistere le richieste di assistenza e le emergenze
- Fornire al team di gestione del datacenter aggiornamenti periodici sugli eventi di sicurezza e sui log delle voci
- Gestire e monitorare i sistemi di allarme, controllo di accesso e sorveglianza

## <a name="visitor-access"></a>Accesso dei visitatori

La verifica della sicurezza e il check-in sono necessari per il personale che richiede l'accesso temporaneo all'interno della struttura del centro dati, inclusi i gruppi di tour e altri visitatori. I visitatori del data center devono firmare un accordo di riservatezza, sottoporsi a revisione della gestione del data center e ottenere l'approvazione da parte della gestione del data center prima della relativa visita pianificata. Al momento dell’arrivo iniziale, vengono elaborate credenziali di accesso temporanee con privilegi minimi per ciascun visitatore del data center. Inoltre, viene assegnato un dipendente Microsoft a tempo pieno (FTE) o personale designato autorizzato approvato dalla gestione del data center per accompagnare i visitatori durante la visita.

Tutti i visitatori che hanno approvato l'accesso al datacenter sono designati come *Solo scorta* sui badge e devono rimanere sempre con le loro accompagnatori. I visitatori scortati non hanno alcun livello di accesso concesso loro e possono solo viaggiare sull'accesso delle loro accompagnatori. La scorta è responsabile della revisione delle azioni e dell'accesso del visitatore durante la visita al datacenter.

L'accesso dei visitatori viene monitorato dalla scorta assegnata e dal supervisore della sala di controllo tramite la tv a circuito chiuso (CCTV) e il sistema di monitoraggio degli allarmi. I visitatori con una richiesta di accesso approvata hanno la richiesta di accesso esaminata nel momento in cui la loro identificazione viene verificata in base a una forma di identificazione emessa dal governo o badge rilasciato da Microsoft. Ai visitatori approvati per l'accesso accompagnato viene emesso un badge sticky con scadenza autonoma e, al ritorno, il record di accesso all'interno dello strumento viene terminato. Se un visitatore lascia il badge, scade automaticamente entro 24 ore.

Le notifiche di accesso temporaneo vengono archiviate all'interno del SOC controllato dall'accesso e inventariate all'inizio e alla fine di ogni turno. I responsabili della sicurezza sono dipendenti 24x7 e le chiavi fisiche sono archiviate in un sistema di gestione delle chiavi elettronico collegato al sistema di accesso fisico che richiede il PIN e il badge di accesso di un responsabile della sicurezza per ottenere l'accesso.

## <a name="access-review-and-deprovisioning"></a>Revisione e deprovisioning dell'accesso

Il team DCM è responsabile della revisione regolare dell'accesso al datacenter e dell'esecuzione di un controllo trimestrale per verificare che l'accesso individuale sia ancora necessario.

Per le terminazioni o i trasferimenti, l'accesso della persona viene immediatamente rimosso dal sistema e la relativa notifica di accesso viene rimossa. In questo modo viene rimosso qualsiasi accesso al datacenter che l'utente potrebbe avere avuto. I team di DCM eseguono inoltre verifiche di accesso trimestrali per convalidare l'adeguatezza dell'elenco di accesso al datacenter nel sistema.

## <a name="key-management"></a>Gestione delle chiavi

I tasti fisici/rigidi vengono estratti a personale specifico abbinando il badge di accesso della persona alla chiave fisica. Una persona deve avere il livello di accesso appropriato nello strumento per estrarre chiavi specifiche. Le chiavi non sono consentite fuori sede.

Le chiavi rigide e le notifiche sono tenute sotto stretto controllo da Microsoft e vengono controllati ogni giorno. Microsoft riduce inoltre i rischi implementando un'assegnazione rigorosa dei livelli di accesso e la distribuzione e la gestione controllate delle chiavi. I metodi di accesso principali nei datacenter sono i badge di accesso elettronico e la biometria, che consente la revoca immediata dell'accesso in base alle esigenze. Microsoft dispone di procedure per determinare l'azione appropriata in base al rischio per tutte le chiavi perse. Queste azioni potrebbero richiedere la ridenozione della chiave di un rack o di una porta a server singolo e fino alla ri-modifica della chiave dell'intera struttura del datacenter.

## <a name="access-logging-and-monitoring"></a>Registrazione e monitoraggio dell'accesso

Le richieste di accesso e gli eventi di entrata/uscita vengono registrati e conservati come parte di un controllo di tracciabilità elettronico, consentendo poi l’interrogazione e la riconciliazione dei dati. I report del sistema di controllo di accesso e l'analisi dei dati consentono un ulteriore rilevamento delle anomalie per identificare e impedire l'accesso non necessario e non autorizzato.

I sistemi di sorveglianza del datacenter monitorano le aree critiche del centro dati come l'entrata/uscita principale del datacenter, le colocation di ingresso/uscita del datacenter, le gabbie, gli archivi bloccati, le vie di accesso, le aree di spedizione e ricezione, gli ambienti critici, le porte perimetrali e le aree di parcheggio. Le registrazioni di sorveglianza vengono conservate per un minimo di 90 giorni, a meno che la legge locale non prevede diversamente.

Un supervisore della sala di controllo è sempre nel SOC per fornire il monitoraggio dell'accesso fisico nel datacenter. La videosorveglianza viene utilizzata per monitorare l'accesso fisico al datacenter e al sistema di informazioni. Il sistema di videosorveglianza è collegato al sistema di monitoraggio degli allarmi dell'edificio per supportare il monitoraggio dell'accesso fisico dei punti di allarme. I responsabili della sicurezza assicurano che l'accesso sia consentito solo ai membri del personale con autorizzazioni appropriate e verificano che chiunque esegua o esegua le procedure appropriate per l'accesso e l'uscita di attrezzature da strutture infrastrutturali critiche.

Gli eventi di sicurezza che si verificano all'interno del datacenter sono documentati dal team di sicurezza in un report denominato Notifica evento di sicurezza (SEN). I report SEN acquisiscono i dettagli di un evento di sicurezza e devono essere documentati dopo che si verifica un evento per acquisire i dettagli nel modo più accurato possibile. I report SEN contengono anche l'analisi investigativa condotta in un Rapporto dopo l'azione (AAR), che documenta l'indagine di un evento di sicurezza, tenta di identificare la causa principale dell'evento e registra eventuali azioni di correzione e le lezioni apprese. Le azioni di correzione e le lezioni apprese vengono utilizzate per migliorare le procedure di sicurezza e ridurre la ripetibilità dell'evento. Se un evento imprevisto influisce sulle risorse o sui servizi Microsoft, il team sim (Security Incident Management) dispone di procedure dettagliate per rispondere.

Oltre alla sicurezza 24x7 in sede, i datacenter Microsoft utilizzano sistemi di monitoraggio delle sveglie che forniscono allarme in tempo reale e monitoraggio video. Le porte del datacenter hanno allarmi che segnalano ogni apertura e quando rimangono aperte oltre un periodo di tempo programmato. Il sistema di sicurezza è programmato per visualizzare l'immagine video in tempo reale quando viene attivato un allarme della porta. Le schede di accesso e i lettori biometrici vengono programmati e monitorati tramite il sistema di monitoraggio degli allarmi. Gli allarmi vengono monitorati e rispondono a 24x7 dal supervisore della sala di controllo che utilizza le fotocamere nell'area dell'incidente in fase di indagine per fornire al risponditore informazioni in tempo reale.
