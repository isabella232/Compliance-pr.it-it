---
title: Funzionalità di creazione di report di Microsoft 365
description: Informazioni sulle varie funzionalità di creazione di report in Microsoft 365, tra cui Azure Active Directory ed Exchange Online.
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
- M365-analytics
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 2cc91f650dcaf5fdafd9f32f3c6991976b49ea04
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497509"
---
# <a name="microsoft-365-reporting-features"></a>Funzionalità di creazione di report di Microsoft 365

Le funzionalità di creazione di report in Microsoft 365 forniscono vari report di controllo per Azure Active Directory (Azure AD), Exchange Online, gestione dei dispositivi, revisione di supervisione e prevenzione della perdita dei dati (DLP). Questi report sono diversi e separati dai report attività di Microsoft 365.

## <a name="microsoft-365-reports-dashboard"></a>Dashboard report di Microsoft 365

Il dashboard Report nell'anteprima dell'interfaccia di amministrazione di Microsoft 365 visualizza l'attività di utilizzo in Microsoft 365. Gli amministratori globali di Microsoft 365 o un amministratore di Exchange Online, SharePoint Online o Skype for Business possono ottenere informazioni dettagliate sull'utilizzo di tale servizio. Ad esempio, il numero di utenti in un particolare servizio Di Microsoft 365, il numero di utenti che hanno attivato Microsoft 365 Apps for enterprise (in precedenza denominato Office 365 ProPlus) e la quantità di posta che scorre nell'organizzazione. I report sono disponibili per gli ultimi 7, 30, 90 e 180 giorni.

Sono disponibili i seguenti report:

- [Report attività di posta elettronica](https://support.office.com/article/Office-365-Reports-in-the-admin-center-preview--Email-activity-1cbe2c00-ca65-4fb9-9663-1bbfa58ebe44)
- [Microsoft Office delle attivazioni](https://support.office.com/article/Office-365-Reports-in-the-admin-center-preview--Microsoft-Office-activations-87c24ae2-82e0-4d1e-be01-c3bcc3f18c60)
- [Report sull'utilizzo del sito di SharePoint Online](https://support.office.com/article/Office-365-Reports-in-the-admin-center-preview--SharePoint-site-usage-4ecfb843-e5d5-464d-8bf6-7ed512a9b213)
- [Report sull'utilizzo di OneDrive for Business](https://support.office.com/article/Office-365-Reports-in-the-Admin-Center-Preview--OneDrive-for-Business-usage-0de3b312-c4e8-4e4b-a02d-32b2f726a680)
- [Report delle attività di Yammer](https://support.office.com/article/View-the-Yammer-Activity-report-in-the-Office-365-admin-center-preview-c7c9f938-5b8e-4d52-b1a2-c7c32cb2312a)
- [Report attività di Skype for Business](/SkypeForBusiness/skype-for-business-online-reporting/activity-report)
- [Report attività peer-to-peer di Skype for Business](/SkypeForBusiness/skype-for-business-online-reporting/peer-to-peer-activity-report)
- [Report organizzatore conferenze Skype for Business](/SkypeForBusiness/skype-for-business-online-reporting/conference-organizer-activity-report)
- [Report attività partecipante a conferenze Skype for Business](/SkypeForBusiness/skype-for-business-online-reporting/conference-participant-activity-report)

Per ulteriori informazioni, vedere [Report attività nell'interfaccia di amministrazione di Microsoft 365.](https://support.office.com/article/activity-reports-in-the-office-365-admin-center-0d6dfb17-8582-4172-a9a9-aed798150263)

## <a name="azure-ad-reports"></a>Report di Azure AD

Microsoft 365 usa Azure AD per l'autenticazione e la gestione delle identità. Gli amministratori di Microsoft 365 usano i report generati da Azure per identificare attività insolite e accesso non autorizzato ai propri dati. È possibile usare i report di accesso e utilizzo in Azure AD per ottenere visibilità sull'integrità e la sicurezza della directory per l'organizzazione. Con queste informazioni, è possibile identificare e ridurre i possibili rischi per la sicurezza.

I report di Azure AD possono essere esportati in Microsoft Excel e correlati ad altri dati di Microsoft 365. Ad esempio, i risultati di una ricerca nel log di controllo possono fornire informazioni dettagliate sulle attività di accesso, autenticazione e applicazione. I report avanzati sull'anomalia e sull'utilizzo delle risorse sono disponibili con Azure AD Premium. Questi report avanzati consentono di migliorare la sicurezza e di rispondere a potenziali minacce applicando analisi sull'accesso ai dispositivi e sull'utilizzo delle applicazioni. Per ulteriori informazioni, vedere Creazione di [report di Azure Active Directory.](/azure/active-directory/reports-monitoring/overview-reports/)

## <a name="exchange-online-audit-reports"></a>Report di controllo di Exchange Online

I report di controllo di Exchange Online includono dettagli sull'accesso alle cassette postali e sulle modifiche apportate dagli amministratori al tenant di Exchange Online. Con il controllo delle cassette postali, è possibile utilizzare le attività nella tabella seguente per eseguire report ed esportare i registri di controllo di Exchange Online.

> [!NOTE]
> È necessario abilitare la registrazione di controllo delle cassette postali per ogni cassetta postale in modo che gli eventi controllati siano salvati nel registro di controllo per tale cassetta postale. Se la registrazione di controllo delle cassette postali non è abilitata per una cassetta postale, gli eventi per tale cassetta postale non verranno salvati nel registro di controllo e non verranno visualizzati nei rapporti di controllo delle cassette postali. Per ulteriori informazioni, vedere [enable mailbox auditing](https://support.office.com/article/Enable-mailbox-auditing-in-Office-365-aaca8987-5b62-458b-9882-c28476a66918).

| Attività | Descrizione |
|----------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Eseguire un rapporto di accesso non proprietario della cassetta postale](/exchange/security-and-compliance/exchange-auditing-reports/non-owner-mailbox-access-report) | Visualizza l'elenco delle cassette postali a cui accede un utente diverso dal proprietario della cassetta postale. Il report contiene informazioni sull'utente che ha eseguito l'accesso alla cassetta postale, sulle azioni intraprese nella cassetta postale e sull'esito delle azioni. |
| [Esportare i log di controllo delle cassette postali](/exchange/security-and-compliance/exchange-auditing-reports/export-mailbox-audit-logs) | I registri di controllo delle cassette postali contengono informazioni sull'accesso e sulle azioni in una cassetta postale eseguita da un utente diverso dal proprietario della cassetta postale. Gli amministratori possono specificare le cassette postali insieme a un intervallo di date per generare report. I registri vengono esportati in formato XML, allegati a un messaggio e inviati a utenti specifici come determinato dall'amministratore. |
| [Esegui il rapporto di un gruppo di ruoli amministratore](/Office365/SecurityCompliance/eop/run-an-administrator-role-group-report-in-eop-eop) | Il gruppo di ruoli amministratore assegna privilegi amministrativi agli utenti. Questi privilegi consentono agli utenti di eseguire attività amministrative come reimpostare le password, creare o modificare cassette postali e assegnare privilegi di amministratore ad altri utenti. Il report del gruppo di ruoli amministratore mostra le modifiche apportate ai gruppi di ruoli, inclusa l'aggiunta o la rimozione dei membri. |
| [Visualizzare il log di controllo dell'amministratore](/exchange/security-and-compliance/exchange-auditing-reports/view-administrator-audit-log) | Il report del registro di controllo dell'amministratore elenca tutte le funzioni di creazione, aggiornamento ed eliminazione eseguite dagli amministratori in Exchange Online. Le voci di registro forniscono informazioni sul cmdlet eseguito, sui parametri utilizzati, sull'utente che ha eseguito il cmdlet e sugli oggetti interessati. |
| [Ricerca e conservazione del contenuto delle cassette postali](/exchange/security-and-compliance/in-place-ediscovery/in-place-ediscovery) | Fornisce informazioni dettagliate su eventuali modifiche apportate alle In-Place eDiscovery o In-Place di archiviazione per le cassette postali. |
| [Esportare il log di controllo dell'amministratore](/exchange/security-and-compliance/exchange-auditing-reports/search-role-group-changes) | Il log di controllo dell'amministratore registra azioni amministrative specifiche, ad esempio la creazione, l'aggiornamento e l'eliminazione in Exchange Online. I risultati del log vengono esportati in XML e gli amministratori possono scegliere di inviare il registro a un set di utenti. |
| [Esegui un rapporto sulla conservazione per controversia legale per singola cassetta postale](/exchange/security-and-compliance/exchange-auditing-reports/per-mailbox-litigation-hold-report) | Fornisce informazioni dettagliate su eventuali modifiche alle impostazioni di conservazione per controversia legale nelle cassette postali. |
| [Visualizzare ed esportare il log di controllo dell'amministratore esterno](/exchange/security-and-compliance/exchange-auditing-reports/view-external-admin-audit-log) | Contiene i dettagli delle azioni eseguite dagli amministratori esterni. Le voci forniscono informazioni sul cmdlet eseguito, sui parametri utilizzati e sulle azioni che creano, modificano o eliminano oggetti in Exchange Online. |

## <a name="device-compliance-reports"></a>Report di conformità dei dispositivi

Puoi gestire e proteggere i dispositivi mobili connessi all'abbonamento usando Dispositivi mobili di base e sicurezza per Microsoft 365. I dispositivi mobili utilizzati per accedere alla posta elettronica, al calendario, ai contatti e ai documenti di lavoro svolgono un ruolo significativo nel garantire che i dipendenti siano in grado di lavorare in qualsiasi momento e da qualsiasi luogo. È fondamentale proteggere le informazioni dell'organizzazione. Puoi usare Dispositivi mobili e sicurezza di base per Microsoft 365 per impostare i criteri di sicurezza dei dispositivi e le regole di accesso. In caso di sperpero o furto, si usa anche Basic Mobility and Security per Microsoft 365 per cancellare i dispositivi mobili.

I report di conformità di base per dispositivi mobili e sicurezza forniscono una panoramica dei criteri impostati da un'organizzazione per proteggere i dispositivi mobili che accedono ai dati di Microsoft 365. Il report consente di filtrare i dispositivi in base allo stato di conformità, alle violazioni segnalate, ai dispositivi bloccati e al numero di dispositivi cancellati a seguito dei criteri di sicurezza. Per ulteriori informazioni, vedere [Overview of Basic Mobility and Security for Microsoft 365](https://support.microsoft.com/office/overview-of-basic-mobility-and-security-for-microsoft-365-faa7d8e5-645d-4d59-839c-c8d4c1869e4a).

## <a name="data-loss-prevention"></a>Prevenzione della perdita di dati

I criteri DLP consentono di gestire la sicurezza e il flusso di informazioni in un'organizzazione. È possibile configurare criteri per bloccare l'accesso al contenuto, crittografare i dati o notificare agli utenti le violazioni dei criteri e dei criteri utilizzando i suggerimenti per i criteri DLP in-application. I report DLP forniscono informazioni dettagliate sul numero di corrispondenze, sostituzioni e falsi positivi di criteri e regole.

Utilizzare l'interfaccia di amministrazione di Microsoft 365 per visualizzare informazioni sul numero di messaggi rilevati dai criteri DLP. I report DLP forniscono informazioni dettagliate sulle corrispondenze dei criteri e delle regole per la posta inviata e ricevuta. È inoltre possibile visualizzare il numero di corrispondenze, sostituzioni e falsi positivi per ogni criterio nelle ultime 24 ore utilizzando l'interfaccia di amministrazione di Exchange. Se si scarica un report di Excel, è possibile visualizzare ulteriori dettagli, ad esempio l'utente che ha inviato il messaggio, il giorno e le corrispondenze dei criteri attivati. Per ulteriori informazioni, vedere [View reports about DLP policy detections](/previous-versions/exchange-server/exchange-150/jj889415(v=exchg.150)).

## <a name="auditing-in-yammer-enterprise"></a>Controllo in Yammer Enterprise

Yammer Enterprise offre agli amministratori la possibilità di esportare i dati sulle attività degli utenti dalla rete Yammer tramite [l'API](https://support.office.com/article/export-data-from-yammer-enterprise-b303d8f3-007d-4ad4-81f8-54fb1ecfb3f2)di esportazione dei dati di Yammer o manualmente tramite la pagina di amministrazione della rete Yammer. La possibilità di esportare i registri è limitata agli amministratori di rete in Yammer. Tutti gli amministratori globali di Microsoft 365 sono amministratori di rete yammer.

È possibile esportare i dati seguenti:

| Filename | Descrizione |
|----------------------------|-------------------------------------------------------------------------|
| Users.csv | Tutti gli utenti nuovi, in sospeso e sospesi nella rete |
| Messages.csv | Tutti i messaggi nella rete |
| Files.csv (metadati) | Metadati come nome file, URL API file, ID del caricatore, caricati in e così via. |
| Files.csv (file originali) | File ZIP dei file originali caricati dagli utenti in Yammer |
| Topics.csv | Argomenti creati in rete |
| Pages.csv | Pagine (note) create dagli utenti nella rete |
| Admins.csv | Tutti gli amministratori verificati nella rete |
| Networks.csv | Tutte le reti esterne di Yammer |

I dati di Yammer Enterprise sono disponibili anche tramite i report attività di Microsoft 365. Inoltre, Yammer sta lavorando attivamente per esporre la registrazione aggiuntiva tramite l'API di attività di gestione di Microsoft 365 e sulla possibilità di controllare i dati con Power BI. Per ulteriori informazioni su queste funzionalità, vedere la Guida di orientamento di [Office.](https://fasttrack.microsoft.com/roadmap?filters=yammer)
