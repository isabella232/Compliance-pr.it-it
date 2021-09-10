---
title: Gestione account in Microsoft 365
description: Informazioni sulla gestione degli account in Microsoft 365
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
ms.openlocfilehash: d525edfb9854df156f5b7b8571199b7a0102a0bf
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2021
ms.locfileid: "58947103"
---
# <a name="account-management-in-microsoft-365"></a>Gestione account in Microsoft 365

Microsoft ha investito molto in sistemi e controlli che automatizzano la maggior parte delle operazioni Microsoft 365, limitando intenzionalmente la necessità di accedere direttamente ai server e ai dati dei clienti da parte del personale di servizio. Gli utenti controllano il servizio e il software gestisce il servizio. Questa struttura consente a Microsoft di gestire Microsoft 365 su larga scala e riduce al minimo i rischi di minacce interne ed esterne. Microsoft si avvicina al controllo degli accessi presupponendo che tutti gli utenti sono una potenziale minaccia per i Microsoft 365 e i dati dei clienti. Per questo motivo, il principio ZSA (Zero Standing Access) è la base per l'intera struttura di controllo di accesso utilizzata da Microsoft 365.

Per impostazione predefinita, il personale Microsoft non dispone di alcun accesso privilegiato permanente a qualsiasi Microsoft 365 o ai dati dei clienti per un'organizzazione. Solo attraverso un solido sistema di controlli e approvazioni, il personale del team di servizio può ottenere l'accesso privilegiato con un ambito di azione e tempo limitato. Grazie a questo sistema, Microsoft può ridurre in modo significativo il potenziale del personale del servizio Microsoft 365 e degli utenti malintenzionati di ottenere accesso non autorizzato o causare danni dannosi o accidentali a servizi Microsoft e clienti.

## <a name="account-types"></a>Tipi di account

Microsoft 365 tutte le missioni organizzative e le funzioni aziendali utilizzando tre categorie di account: account del team di servizio, account di servizio e account dei clienti. La gestione di questi account è una responsabilità condivisa tra Microsoft e i clienti. Microsoft gestisce sia gli account del team di servizio che gli account di servizio, utilizzati per gestire e supportare prodotti e servizi Microsoft. Gli account dei clienti sono gestiti dal cliente e consentono loro di personalizzare l'accesso all'account per soddisfare i requisiti di controllo di accesso interno.

![Responsabilità condivisa per gli account](../media/assurance-shared-responsibility-for-accounts.png)

## <a name="microsoft-managed-accounts"></a>Account gestiti da Microsoft

**Gli account del team di** servizio vengono utilizzati dal Microsoft 365 del team del servizio che sviluppa e mantiene Microsoft 365 servizi. Questi account non dispongono dell'accesso con privilegi permanenti ai servizi Microsoft 365, ma possono essere utilizzati per richiedere l'accesso con privilegi temporanei e limitati per eseguire una funzione di processo specificata. Non tutti gli account del team di servizio possono eseguire le stesse azioni, la separazione dei compiti viene applicata tramite il controllo dell'accesso basato sui ruoli (RBAC). I ruoli garantiscono che i membri del team di servizio e i relativi account dispongono solo dell'accesso minimo necessario per eseguire mansioni specifiche. Inoltre, gli account del team di servizio non possono appartenere a più ruoli in cui possono agire come responsabili approvazione per le proprie azioni.

**Gli account di** servizio vengono utilizzati dai Microsoft 365 per eseguire l'autenticazione quando comunicano con altri servizi tramite processi automatizzati. Proprio come agli account del team di servizio viene concesso solo l'accesso minimo necessario per eseguire le mansioni del personale specifico, agli account di servizio viene concesso solo l'accesso minimo necessario per lo scopo previsto. Sono inoltre disponibili più tipi di account di servizio progettati per soddisfare esigenze specifiche. Un Microsoft 365 può avere più account di servizio, ognuno con un ruolo diverso da eseguire.

## <a name="customer-managed-accounts"></a>Account gestiti dal cliente

**Gli account** dei clienti vengono utilizzati per accedere Microsoft 365 servizio e sono gli unici account di cui ogni cliente è responsabile. È compito del cliente creare e gestire gli account nell'organizzazione per mantenere un ambiente sicuro. La gestione degli account dei clienti viene eseguita tramite Azure Active Directory (AAD) o federati con Active Directory locale (AD). Ogni cliente ha un set univoco di requisiti di controllo di accesso che deve soddisfare e gli account dei clienti concedono a ogni cliente la possibilità di soddisfare le proprie esigenze individuali. Gli account dei clienti non possono accedere ai dati al di fuori dell'organizzazione del cliente.

## <a name="service-team-account-management"></a>Gestione degli account del team di servizio

Microsoft 365 gli account del team di servizio per tutto il ciclo di vita utilizzando un sistema di gestione degli account denominato Identity Management (IDM). IDM usa una combinazione di processi di verifica automatizzati e approvazione gestionale per applicare i requisiti di sicurezza correlati all'accesso all'account del team di servizio.

I membri del team di servizio non ottengono automaticamente un account del team di servizio, devono prima soddisfare i requisiti di idoneità e ottenere l'approvazione da un manager autorizzato. Per essere idoneo per un account del team di servizio, il personale del team di servizio deve prima passare attraverso lo screening del personale [pre-impiego,](assurance-pre-employment-screening.md)un controllo del [background cloud](assurance-cloud-background-check.md)e completare tutta la formazione standard e necessaria basata sui ruoli. Una volta soddisfatti tutti i requisiti di idoneità, una richiesta per un account del team di servizio può essere effettuata e deve essere approvata da un manager autorizzato.

![Processo di screening del personale](../media/assurance-personnel-screening-process.png)

IDM è anche responsabile del monitoraggio della rischermazione periodica e della formazione necessarie per mantenere un account del team di servizio. Il controllo del background del cloud Microsoft deve essere completato ogni due anni e tutto il materiale di formazione deve essere esaminato ogni anno. Se uno di questi requisiti non è soddisfatto entro la data di scadenza, l'idoneità viene revocata e l'account del team di servizio viene disabilitato automaticamente.

Inoltre, l'idoneità all'account del team di servizio viene aggiornata automaticamente dal [trasferimento e dalla terminazione del personale.](assurance-employee-transfer-termination.md) Le modifiche apportate al sistema HRIS (Human Resources Information System) attivano l'azione IDM, che varia a seconda della situazione. Il personale trasferito a un altro team del servizio avrà una data di scadenza impostata per i propri idonei e una richiesta di mantenimento delle autorizzazioni deve essere inviata dal membro del team di servizio e approvata dal nuovo manager. Al personale terminato vengono automaticamente revocate tutte le autorizzazioni e l'account del team di servizio viene disabilitato l'ultimo giorno. È possibile richiedere urgentemente la revoca dell'account per le terminazioni involontarie.

Per impostazione predefinita, gli account del team di servizio dispongono di accesso in lettura limitato ai metadati di sistema generali utilizzati per la risoluzione dei problemi regolari. Inoltre, gli account del team di servizio di base non possono richiedere l'accesso con privilegi Microsoft 365 o ai dati dei clienti. È necessario effettuare un'altra richiesta per l'aggiunta dell'account del team di servizio a un ruolo che consenta al membro del team di servizio di richiedere privilegi elevati per eseguire attività e operazioni specifiche.
