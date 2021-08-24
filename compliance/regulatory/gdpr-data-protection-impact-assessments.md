---
title: Valutazioni d'impatto sulla protezione dei dati
description: Questi documenti forniscono informazioni ai titolari del trattamento dei dati per aiutarli a determinare se è necessaria una DPIA e, in tal caso, quali dettagli includere.
keywords: Valutazione impatto protezione dati, DPIA, Dynamics 365, servizi professionali Microsoft, Microsoft 365, documentazione Microsoft 365, RGPD
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
ms.openlocfilehash: c634e1c63a123232f600cbe085964cf9d2e366a9
ms.sourcegitcommit: 4c00fd65d418065d7f53216c91f455ccb3891c77
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/23/2021
ms.locfileid: "58479798"
---
# <a name="data-protection-impact-assessment-for-the-gdpr"></a>Valutazione dell'impatto sulla protezione dei dati per il GDPR

Il regolamento generale sulla protezione dei dati (GDPR) introduce nuove regole per le organizzazioni che offrono beni e servizi alle persone che risiedono nell'Unione europea (UE) o che raccolgono e analizzano i dati dei residenti nell'UE in qualunque luogo si trovi l'utente o la sua azienda. Altri dettagli sono disponibili [nell'argomento Riepilogo sul GDPR](gdpr.md). Questo documento illustra le informazioni relative alle valutazioni d’impatto sulla protezione dei dati (DPIA) con il GDPR quando si usano i prodotti e i servizi Microsoft.

## <a name="terminology"></a>Terminologia

Definizioni utili per i termini relativi al GDPR usati nel documento:

- *Titolare del trattamento dei dati (titolare)*: una persona giuridica, un'autorità pubblica, un'agenzia o un altro organismo che, da solo o congiuntamente con altri, determina le finalità e le modalità di trattamento dei dati personali.  
- *Dati personali* e *interessato*: qualsiasi informazione relativa a una persona fisica identificata o identificabile (interessato); una persona fisica identificabile è una persona che può essere identificata, direttamente o indirettamente.  
- *Responsabile*: una persona fisica o giuridica, un'autorità pubblica o un altro ente che si occupa del trattamento dei dati personali per conto del titolare.  
- *Dati dei clienti*: dati prodotti e archiviati nelle attività quotidiane di gestione della propria attività.

## <a name="what-is-a-dpia"></a>Cos’è una DPIA?

Il GDPR richiede che i titolari preparino una valutazione dell'impatto sulla protezione dei dati (DPIA) per le operazioni che "potrebbero comportare un rischio elevato per i diritti e le libertà delle persone fisiche". Non c'è nulla di insito ai prodotti e servizi Microsoft che richieda la creazione di una DPIA. Tuttavia, dato che i prodotti e i servizi Microsoft sono altamente personalizzabili, può essere necessaria una DPIA a seconda dei dettagli della configurazione di Microsoft. Microsoft non ha alcun controllo su e quasi nessuna conoscenza in merito a queste informazioni. È necessario che il titolare del trattamento determini il corretto utilizzo dei dati.

## <a name="dpia-in-action"></a>Scopri come funziona la DPIA

Le indicazioni DPIA si applicano a Office 365, Azure, Dynamics 365, al supporto tecnico Microsoft e ai servizi professionali. Tali indicazioni includono le seguenti considerazioni:

**Quando è necessaria una DPIA?**

Quando si valuta se completare una DPIA devono essere considerati i fattori di rischio elencati di seguito. Altri fattori potenziali e altri dettagli si trovano nella Parte 1 di ogni linea guida.  

- Una valutazione sistematica e approfondita dei dati basata sull'elaborazione automatica.  
- Elaborazione su vasta scala di categorie speciali di dati (dati che rivelano informazioni che identificano in modo unico una persona fisica) o di dati personali relativi a condanne penali o crimini.
- Monitoraggio sistematico di un'area pubblicamente accessibile su vasta scala.

Il GDPR chiarisce che: "Il trattamento di dati personali non dovrebbe essere considerato un trattamento su larga scala qualora riguardi dati personali di pazienti o clienti da parte di un singolo medico, operatore sanitario o avvocato. In tali casi non dovrebbe essere obbligatorio procedere a una valutazione d'impatto sulla protezione dei dati".

**Cosa è necessario per completare una DPIA?**

Una DPIA deve fornire informazioni specifiche sulle elaborazioni previste, descritte nella Parte 2 delle indicazioni. Tali informazioni includono:

- Una valutazione della necessità e proporzionalità dell’elaborazione dei dati in relazione agli scopi della DPIA.  
- Una valutazione dei rischi per i diritti e le libertà delle persone fisiche.
- Misure previste per risolvere i rischi, tra cui garanzie, misure di sicurezza e meccanismi per garantire la protezione dei dati personali e dimostrare la conformità con il GDPR.
- Finalità dell’elaborazione  
- Categorie di dati personali elaborate  
- Conservazione dei dati  
- Ubicazione e trasferimento dei dati personali  
- Condivisione dei dati con terze parti responsabili del trattamento  
- Condivisione dei dati con terze parti indipendenti  
- Diritti del soggetto interessato

## <a name="additional-considerations"></a>Considerazione aggiuntive

Di seguito sono riportati dettagli specifici che possono essere rilevanti per l'implementazione di Microsoft.

- [Office 365](gdpr-dpia-office365.md): questo documento riguarda le applicazioni e i servizi di Office 365, inclusi, a titolo esemplificativo, Exchange Online, SharePoint Online, Yammer, Skype for Business e Power BI. Per altre informazioni, vedere le Tabelle [1](/microsoft-365/compliance/gdpr-dpia-office365#part-1--determining-whether-a-dpia-is-needed) e [2](/microsoft-365/compliance/gdpr-dpia-office365#part-2--contents-of-a-dpia).  
- [Azure](gdpr-dpia-azure.md): i clienti sono invitati a collaborare con i responsabili della privacy e il consiglio legale per determinare la necessità e il contenuto di qualsiasi DPIA relativa all'uso di Microsoft Azure.  
- [Dynamics 365](gdpr-dpia-dynamics.md): il contenuto di una DPIA può variare in base al tipo di strumenti di Dynamics 365 che si usano. Per informazioni dettagliate, fare riferimento alla [Parte 2 Contenuti di una DPIA](/microsoft-365/compliance/gdpr-dpia-dynamics#part-2--contents-of-a-dpia).
- [Windows](/compliance/regulatory/gdpr-dpia-windows): il documento si applica alla [configurazione del responsabile del trattamento dei dati di diagnostica Windows](/windows/privacy/configure-windows-diagnostic-data-in-your-organization). I clienti sono invitati a collaborare con i responsabili della privacy e il proprio consulente legale per determinare la necessità e il contenuto di qualsiasi DPIA relativa all'uso della configurazione del responsabile del trattamento dei dati di diagnostica Windows.
- [Supporto tecnico Microsoft e servizi professionali](gdpr-dpia-prof-services.md): i servizi professionali non conducono determinate routine o elaborazioni automatizzate dei dati, né il trattamento di categorie speciali o l'esecuzione di attività che facilitino o richiedano il monitoraggio di dati accessibili pubblicamente. Per informazioni dettagliate, vedere [Parte 1: Determinare se è necessaria una DPIA](/microsoft-365/compliance/gdpr-dpia-prof-services#part-1--determining-whether-a-dpia-is-needed). I titolari devono considerare gli elementi DPIA descritti sopra, insieme ad altri fattori rilevanti, nel contesto delle implementazioni e degli usi specifici dei servizi professionali da parte del titolare. Per informazioni sui servizi professionali, vedere la [Parte 2: Contenuti di una DPIA](/microsoft-365/compliance/gdpr-dpia-prof-services#part-2--contents-of-a-dpia).

## <a name="learn-more"></a>Ulteriori informazioni

- [Centro protezione Microsoft](https://www.microsoft.com/trust-center/privacy/gdpr-overview)
