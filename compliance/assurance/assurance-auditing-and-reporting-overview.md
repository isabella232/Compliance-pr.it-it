---
title: Controllo e creazione di report nei servizi cloud Microsoft
description: Panoramica delle funzionalità di controllo e creazione di report in Office 365, Microsoft 365 e Service Assurance.
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
- M365-analytics
- SPO_Content
- MS-Compliance
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: 4cb9f68f2c5861905a4246582a3b4530c30988ca
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120705"
---
# <a name="auditing-and-reporting-in-microsoft-cloud-services"></a>Controllo e creazione di report nei servizi cloud Microsoft

I servizi cloud Microsoft includono diverse funzionalità di controllo e creazione di report che è possibile utilizzare per tenere traccia delle attività amministrative e degli utenti all'interno del tenant, tra cui le modifiche apportate alle impostazioni di configurazione del tenant di Exchange Online e SharePoint Online e le modifiche apportate dagli utenti ai documenti e ad altri elementi. È possibile utilizzare le informazioni di controllo e i report disponibili nei servizi cloud Microsoft per gestire in modo più efficace l'esperienza utente, ridurre i rischi e adempiere agli obblighi di conformità.

## <a name="security--compliance-centers"></a>Centri & conformità

Il Centro sicurezza e conformità di [Microsoft 365 &,](https://protection.office.com)il Centro sicurezza [Microsoft 365](https://security.microsoft.com)e il Centro conformità [Microsoft 365](https://compliance.microsoft.com) sono portali one-stop per la protezione dei dati nell'organizzazione e includono molte funzionalità di controllo e creazione di report. Questi centri consentono di soddisfare le esigenze di protezione o conformità dei dati e di controllare le attività di utenti e amministratori. Puoi accedere a questi centri usando il tuo account di amministratore dell'abbonamento.

Questi centri includono riquadri di spostamento per l'accesso a diverse funzionalità:

- **Avvisi:** Consente di gestire gli avvisi, visualizzare gli avvisi correlati alla sicurezza e gestire gli avvisi avanzati tramite [Cloud App Security.](/cloud-app-security/what-is-cloud-app-security)
- **Autorizzazioni:** Consente di [assegnare autorizzazioni](/microsoft-365/security/office-365-security/grant-access-to-the-security-and-compliance-center) quali Amministratore conformità, Gestore di eDiscovery e altri utenti all'interno dell'organizzazione in modo che possano eseguire attività in questi centri. Si assegnano le autorizzazioni per la maggior parte delle funzionalità in ogni centro, ma altre autorizzazioni devono essere configurate utilizzando l'interfaccia di amministrazione di Exchange e l'interfaccia di amministrazione di SharePoint.
- **Gestione delle minacce:** Consente di creare e applicare i criteri di gestione dei dispositivi con Basic Mobility and Security per [Microsoft 365,](https://support.microsoft.com/office/overview-of-basic-mobility-and-security-for-microsoft-365-faa7d8e5-645d-4d59-839c-c8d4c1869e4a)per configurare i criteri di prevenzione della perdita dei dati [(DLP)](/microsoft-365/compliance/data-loss-prevention-policies) per l'organizzazione, per configurare il filtro della posta elettronica, antimalware, DKIM (DomainKeys Identified Mail), allegati sicuri, collegamenti sicuri e app OAuth.
- **Governance dei dati:** Consente di importare dati di posta elettronica o SharePoint [](https://support.office.com/article/Enable-archive-mailboxes-in-the-Office-365-Security-Compliance-Center-268a109e-7843-405b-bb3d-b9393b2342ce)da altri sistemi [](/microsoft-365/compliance/retention-policies) [in Microsoft 365,](https://support.office.com/article/Import-PST-files-or-SharePoint-data-to-Office-365-ba688e0a-0fcb-4bd7-8e57-2b669564ea84)configurare le cassette postali di archiviazione e impostare criteri di conservazione per la posta elettronica e altri contenuti all'interno dell'organizzazione.
- **Ricerca & indagini:** Fornisce [strumenti per](https://support.office.com/article/Run-a-Content-Search-in-the-Office-365-Security-Compliance-Center-61852fd9-fe8a-4880-a339-cb19ed3bff4a)la ricerca di contenuti, il [log](https://support.office.com/article/Search-the-audit-log-in-the-Office-365-Security-Compliance-Center-0d4d0f35-390b-4518-800e-0c7ec95e946c)di controllo, la quarantena e la gestione dei casi di [eDiscovery](https://support.office.com/article/Manage-eDiscovery-cases-in-the-Office-365-Security-Compliance-Center-edea80d6-20a7-40fb-b8c4-5e8c8395f6da) per analizzare rapidamente l'attività tra le cassette postali, i gruppi e le cartelle pubbliche di Exchange Online, SharePoint Online e OneDrive for Business.
- **Report:** Consente di accedere rapidamente [ai report](https://support.office.com/article/Reports-in-the-Office-365-Security-Compliance-Center-7acd33ce-1ec8-49fb-b625-43bac7b58c5a) per SharePoint Online, OneDrive for Business, Exchange Online e Azure AD.
- **Garanzia del servizio:** Fornisce informazioni su come Microsoft gestisce la sicurezza, la privacy e la conformità agli standard globali per Microsoft 365, Azure, Microsoft Dynamics CRM Online, Microsoft Intune e altri servizi cloud. Include anche l'accesso a report ISO, SOC e altri report di controllo di terze parti, nonché controlli controllati, che forniscono informazioni dettagliate sui vari controlli che sono stati testati e verificati da revisori di terze parti di Microsoft 365.

## <a name="service-assurance"></a>Garanzia del servizio

Molte organizzazioni in settori regolamentati sono soggette a requisiti di conformità estesi. Per eseguire le proprie valutazioni dei rischi, i clienti spesso hanno bisogno di informazioni approfondite su come Microsoft 365 gestisce la sicurezza e la privacy dei propri dati. Microsoft si impegna a garantire la sicurezza e la privacy dei dati dei clienti nei servizi cloud e a ottenere la fiducia dei clienti fornendo una visione trasparente delle operazioni e un facile accesso a report e valutazioni di conformità indipendenti.

La garanzia del servizio garantisce la trasparenza delle operazioni e le informazioni su come Microsoft gestisce la sicurezza, la privacy e la conformità dei dati dei clienti in Microsoft 365. Include report di controllo di terze parti insieme a una raccolta di white paper, domande frequenti e altri materiali su argomenti di Microsoft 365 come la crittografia dei dati, la resilienza dei dati, la gestione degli incidenti di sicurezza e altro ancora. I clienti possono utilizzare queste informazioni per eseguire le proprie valutazioni dei rischi normativi. I responsabili della conformità possono assegnare il ruolo "Service Assurance User" per consentire agli utenti di accedere a Service Assurance. L'amministratore tenant può anche fornire agli utenti esterni, ad esempio revisori indipendenti, l'accesso alle informazioni nel dashboard di Service Assurance tramite [Microsoft Cloud Service Trust Portal](https://aka.ms/STP) (STP).

## <a name="onedrive-for-business-admin-center"></a>Interfaccia di amministrazione di OneDrive for Business

L'interfaccia di amministrazione di Microsoft OneDrive consente di gestire in modo semplice e rapido le impostazioni di OneDrive for Business dell'organizzazione in un'unica posizione. Per usare l'interfaccia di amministrazione di OneDrive, è necessario onedrive.com accesso. È inoltre necessario essere un amministratore globale dell'organizzazione o un amministratore personalizzato con il ruolo di amministratore di SharePoint. Accedere all'interfaccia di amministrazione di OneDrive for Business all'indirizzo [https://admin.onedrive.com](https://admin.onedrive.com/) .

Le funzionalità principali includono un'area di conformità che fornisce agli amministratori collegamenti al centro di gestione appropriato per scenari chiave come la ricerca nel log di controllo, l'uso di DLP, conservazione, eDiscovery e avvisi.

## <a name="related-links"></a>Collegamenti correlati

- [Funzionalità di reporting di Microsoft 365](assurance-reporting-features.md)
- [Log interni per Microsoft 365 Engineering](assurance-internal-logging.md)
