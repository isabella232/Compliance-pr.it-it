---
title: Controlli di isolamento Microsoft 365
description: Informazioni sui controlli di isolamento in Microsoft 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: Admin
ms.topic: article
f1.keywords:
- NOCSH
ms.service: O365-seccomp
ms.localizationpriority: medium
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
search.appverid:
- MET150
- MOE150
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 312de9f1417ba6298898d47b2b7e05b5fa7034fe
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2021
ms.locfileid: "58947116"
---
# <a name="microsoft-365-isolation-controls"></a>Controlli di isolamento Microsoft 365

Microsoft lavora continuamente per garantire che l'architettura multi-tenant di Microsoft 365 supporti gli standard di sicurezza, riservatezza, privacy, integrità, locale, internazionale e disponibilità a [livello aziendale.](https://www.microsoft.com/trust-center/compliance/compliance-overview) La scalabilità e l'ambito dei servizi forniti da Microsoft rendono difficile e non economica la gestione delle Microsoft 365 con un'interazione umana significativa. Microsoft 365 servizi vengono forniti tramite data center distribuiti a livello globale, ognuno altamente automatizzato con poche operazioni che richiedono un tocco umano o qualsiasi accesso al contenuto dei clienti. Il nostro staff supporta questi servizi e data center utilizzando strumenti automatizzati e un accesso remoto estremamente sicuro.

Microsoft 365 è costituito da più servizi che forniscono importanti funzionalità aziendali e contribuiscono all'intera Microsoft 365 esperienza. Ognuno di questi servizi è autonomo e progettato per l'integrazione tra loro. Microsoft 365 è progettato con i principi seguenti:

- Architettura orientata ai servizi: progettazione e sviluppo di software sotto forma di servizi interoperabili che forniscono funzionalità aziendali ben definite.
- [Garanzia](https://www.microsoft.com/securityengineering/osa)di sicurezza operativa : un framework che incorpora le conoscenze acquisite tramite varie funzionalità uniche per Microsoft, tra cui [Il](https://www.microsoft.com/sdl/default.aspx)ciclo di vita dello sviluppo della sicurezza Microsoft, [Microsoft Security Response Center](https://www.microsoft.com/msrc)e una profonda consapevolezza del panorama delle minacce alla sicurezza informatica.

Microsoft 365 i servizi operano tra loro, ma sono progettati e implementati in modo che possano essere distribuiti e gestiti come servizi autonomi, indipendenti l'uno dall'altro. Microsoft separa i compiti e le aree di responsabilità Microsoft 365 ridurre le opportunità di modifica non autorizzata o involontaria o l'uso improprio delle risorse dell'organizzazione. Microsoft 365 team hanno definito ruoli come parte di un meccanismo completo di controllo degli accessi basato sui ruoli.

## <a name="tenant-isolation"></a>Isolamento dei tenant

Uno dei principali vantaggi del cloud computing è il concetto di un'infrastruttura condivisa e comune tra numerosi clienti contemporaneamente, che porta a un'economia di scala. Microsoft lavora continuamente per garantire che le architetture multi-tenant dei nostri servizi cloud supportino gli standard di sicurezza, riservatezza, privacy, integrità e disponibilità a livello aziendale.

I servizi cloud Microsoft sono stati progettati presupponendo che tutti i tenant siano potenzialmente dannosi per tutti gli altri tenant e sono state implementate misure di sicurezza per evitare che le azioni di un tenant influiscano sulla sicurezza o sul servizio di un altro tenant o sull'accesso al contenuto di un altro tenant.

I due obiettivi principali della gestione dell'isolamento del tenant in un ambiente multi-tenant sono:

- Impedire la perdita o l'accesso non autorizzato al contenuto dei clienti tra tenant; e
- Impedire alle azioni di un tenant di influire negativamente sul servizio per un altro tenant

In tutto il Microsoft 365 sono state implementate più forme di protezione per impedire ai clienti di compromettere servizi o applicazioni di Microsoft 365 o di ottenere l'accesso non autorizzato alle informazioni di altri tenant o del sistema Microsoft 365 stesso, tra cui:

- L'isolamento logico del contenuto dei clienti all'interno di ogni tenant per Microsoft 365 servizi viene ottenuto Azure Active Directory'autorizzazione e il controllo dell'accesso basato sui ruoli.
- SharePoint Online fornisce meccanismi di isolamento dei dati a livello di archiviazione.
- Microsoft usa una rigorosa sicurezza fisica, screening in background e una strategia di crittografia a più livelli per proteggere la riservatezza e l'integrità dei contenuti dei clienti. Tutti Microsoft 365 data center dispongono di controlli di accesso biometrici, con la maggior parte delle stampe palm per ottenere l'accesso fisico. Inoltre, tutti i dipendenti Microsoft con sede negli Stati Uniti devono completare correttamente un controllo in background standard nell'ambito del processo di assunzione. Per ulteriori informazioni sui controlli utilizzati per l'accesso amministrativo in Microsoft 365, vedere [Microsoft 365 Account Management](assurance-microsoft-365-account-management.md).
- Microsoft 365 utilizza tecnologie sul lato servizio che crittografano i contenuti dei clienti in fase di riposo e in transito, tra cui BitLocker, crittografia per file, TLS (Transport Layer Security) e IPsec (Internet Protocol Security). Per informazioni dettagliate sulla crittografia in Microsoft 365, vedere [Data Encryption Technologies in Microsoft 365](/microsoft-365/compliance/office-365-encryption-in-the-microsoft-cloud-overview).

Insieme, le protezioni sopra elencate forniscono controlli di isolamento logico affidabili che forniscono la protezione dalle minacce e la mitigazione equivalenti a quella fornita solo dall'isolamento fisico.

## <a name="resources"></a>Risorse

- [Isolamento e controllo di accesso in Azure Active Directory](/microsoft-365/enterprise/microsoft-365-isolation-in-azure-active-directory)
- [Monitoraggio e test dei limiti del tenant](assurance-monitoring-and-testing.md)
- [Isolamento e controllo di accesso in Microsoft 365](/microsoft-365/enterprise/microsoft-365-isolation-in-microsoft-365)
