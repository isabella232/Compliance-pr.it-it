---
title: Classificazione dei dati & tassonomia dell'etichetta di riservatezza
description: In questo articolo è possibile trovare una panoramica dell'uso della classificazione dei dati & tassonomia dell'etichetta di riservatezza con Microsoft 365.
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
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: dc2a1a27994c1f3fc69f35b4b764ae80d3df7defd3b4d0dec97520de7760f815
ms.sourcegitcommit: af1925730de60c3b698edc4e1355c38972bdd759
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/05/2021
ms.locfileid: "54288714"
---
# <a name="data-classification--sensitivity-label-taxonomy"></a>Classificazione dei dati & tassonomia dell'etichetta di riservatezza

I dati sensibili presentano rischi significativi per un'azienda se vengono rubati, condivisi inavvertitamente o esposti tramite una violazione. I fattori di rischio includono danni alla reputazione, impatto finanziario e perdita di vantaggio competitivo. La protezione dei dati e delle informazioni gestite dall'azienda è una priorità assoluta per l'organizzazione, ma potrebbe risultare difficile sapere se gli sforzi sono veramente efficaci, data la quantità di contenuto mantenuto dall'azienda.

Oltre al volume, il contenuto può essere di importanza variabile, da estremamente sensibile e di impatto a banale e transitorio. Può anche essere sotto il controllo di vari requisiti di conformità normativa. Sapere quali priorità e dove applicare i controlli può essere una sfida. Continua a leggere per informazioni sulla classificazione dei *dati,* uno strumento importante per proteggere il contenuto da furti, furti o distruzione accidentale e su come Microsoft 365 può aiutare a raggiungere gli obiettivi di sicurezza delle informazioni.

## <a name="what-is-data-classification"></a>Che cos'è la classificazione dei dati?

[La classificazione dei](/microsoft-365/compliance/data-classification-overview) dati è un termine specializzato utilizzato nei campi della cybersecurity e della governance delle informazioni per descrivere il processo di identificazione, categorizzazione e protezione dei contenuti in base al livello di riservatezza o impatto. Nella sua forma più semplice, la classificazione dei dati è un mezzo per proteggere i dati da divulgazioni, alterazioni o distruzioni non autorizzate in base al livello di riservatezza o impatto.

## <a name="what-is-a-data-classification-framework"></a>Che cos'è un framework di classificazione dei dati?

Spesso codificato in un criterio formale a livello aziendale, un framework di classificazione dei dati (talvolta denominato "criterio di classificazione dei dati") è in genere costituito da 3-5 livelli di classificazione. Questi includono in genere tre elementi: un nome, una descrizione ed esempi reali. Microsoft consiglia di non più di cinque etichette padre di primo livello, ognuna con cinque etichette secondarie (25 totali) per mantenere gestibile l'interfaccia utente. I livelli sono in genere disposti dal meno sensibile a quello più riservato, ad esempio *Public,* *Internal,* *Confidential* e *Highly* 
 *Confidential.* Altre varianti dei nomi di livello che possono verificarsi includono *Restricted,* *Unrestricted* e *Consumer Protected.* Microsoft consiglia nomi di etichette auto descrittivi che ne evidenziano chiaramente la riservatezza relativa. Ad esempio, *Confidential* e *Restricted* potrebbero lasciare agli utenti la ipotesi dell'etichetta appropriata, mentre *Confidential* e *Highly Confidential* sono più chiari su cui è più sensibile. La tabella seguente mostra esempi di livelli del framework di classificazione dei dati.

|**Livello di classificazione**|**Descrizione**|**Esempi**|
|:-----------------------|:--------------|:-----------|
| Highly Confidential (Riservatezza elevata) | I dati estremamente riservati sono il tipo più riservato di dati archiviati o gestiti dall'azienda e possono richiedere notifiche legali se violati o altrimenti divulgati. <br><br> I dati con restrizioni richiedono il massimo livello di controllo e sicurezza e l'accesso deve essere limitato a "necessità di informazioni". | Informazioni personali riservate (informazioni personali riservate) <br> Dati del titolare della carta <br> Informazioni sanitarie protette (PHI) <br> Dati del conto corrente bancario |

>[!TIP]
>Il framework di classificazione dei dati aziendali di Microsoft originariamente usava una categoria e un'etichetta denominata "Internal" durante la fase pilota, ma ha rilevato che esistevano motivi legittimi per la condivisione esterna di un documento e il passaggio all'uso di "Generale".

Un altro componente importante di un framework di classificazione dei dati è i controlli associati a ogni livello. I livelli di classificazione dei dati sono semplicemente etichette (o tag) che indicano il valore o la riservatezza del contenuto. Per *proteggere* tale contenuto, i framework di classificazione dei dati definiscono i controlli che devono essere posizionati per ogni livello di classificazione dei dati. Questi controlli possono includere requisiti correlati a:

- Archiviazione tipo e posizione
- Crittografia
- Controllo di accesso
- Distruzione dei dati
- Prevenzione della perdita dei dati
- Divulgazione pubblica
- Registrazione e verifica dell'accesso
- Altri obiettivi di controllo, in base alle esigenze

I controlli di sicurezza variano in base al livello di classificazione dei dati, in modo che le misure di protezione definite nel framework aumentino proporzionalmente alla riservatezza del contenuto. Ad esempio, i requisiti di controllo dell'archiviazione dei dati variano a seconda del supporto utilizzato e del livello di classificazione applicato a una determinata parte di contenuto. La tabella seguente mostra un esempio di controlli di classificazione dei dati per un tipo di archiviazione specifico:

|**Tipo di archiviazione**|**Riservato**|**Interno**|**Senza restrizioni**|
|:---------------|:---------------|:-----------|:---------------|
| Elementi rimovibili Archiviazione | Non consentito | Non consentito a meno che non sia crittografato | Nessun controllo necessario |

L'applicazione corretta del giusto livello di classificazione dei dati può essere complessa in situazioni reali e talvolta può sovraccaricare gli utenti finali. Dopo aver creato un criterio o uno standard che definisce i livelli necessari di classificazione dei dati, è importante guidare gli utenti finali su come dare vita a questo framework nel loro lavoro quotidiano. In quest'area vengono fornite regole o linee guida per la gestione della classificazione dei dati.

Le linee guida per la gestione della classificazione dei dati aiuteranno gli utenti finali con indicazioni specifiche su come gestire ogni livello di dati in modo appropriato, per supporti di archiviazione diversi durante tutto il ciclo di vita. Queste linee guida consentono agli utenti finali di applicare correttamente le regole in pratica, ad esempio quando si condividono documenti, si inviano messaggi di posta elettronica o si collabora tra diverse piattaforme e organizzazioni.

I clienti Microsoft indicano che circa il 50% di un progetto di Protezione delle informazioni è orientato all'azienda e non tecnico, quindi la formazione e la comunicazione degli utenti finali sono fondamentali per il successo.
