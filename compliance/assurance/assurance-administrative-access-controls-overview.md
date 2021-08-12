---
title: Controlli di accesso amministrativo in Microsoft 365
description: In questo articolo viene fornita una panoramica dei controlli di accesso amministrativo e della categorizzazione dei dati in Microsoft 365.
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
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 06bdd239e2845d3495a40fc83bd33cbb0e43dbdb3d025bd8fa77b5d5451a680c
ms.sourcegitcommit: af1925730de60c3b698edc4e1355c38972bdd759
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/05/2021
ms.locfileid: "54289264"
---
# <a name="administrative-access-controls-in-microsoft-365"></a>Controlli di accesso amministrativo in Microsoft 365 

Microsoft ha investito molto in sistemi e controlli che automatizzano la maggior parte delle Microsoft 365, limitando intenzionalmente l'accesso ai contenuti dei clienti da parte di Microsoft. Gli utenti controllano il servizio e il software lo gestisce. Questa struttura consente a Microsoft di gestire i Microsoft 365 su larga scala e di gestire i rischi delle minacce interne al contenuto dei clienti.

Per impostazione predefinita, i tecnici Microsoft non hanno privilegi amministrativi permanenti e zero accesso permanente ai contenuti dei clienti in Microsoft 365. Un tecnico Microsoft può avere accesso limitato, controllati e protetti al contenuto di un cliente per un periodo di tempo limitato. L'accesso è necessario solo se necessario per le operazioni di servizio e solo se approvato da un membro del senior management Microsoft. Per i clienti con licenza Customer Lockbox, il cliente fornisce l'approvazione dell'accesso al contenuto ospitato in Microsoft 365.

Microsoft fornisce servizi online utilizzando più forme di distribuzione cloud:

- **Cloud pubblici:** Include versioni multi-tenant di Microsoft 365, Azure e altri servizi ospitati in Nord America, Sud America, Europa, Asia, Australia e così via.
- **Cloud nazionali:** Include tutti i cloud sovrani e gestiti da terze parti al di fuori degli Stati Uniti (ad eccezione di quelli menzionati in precedenza), ad esempio Microsoft 365 in Cina (gestito da 21Vianet) e Microsoft 365 in Germania (gestito da Microsoft, ma con un modello in cui un trustee di dati tedesco, Deutsche Telekom, controlla e monitora l'accesso di Microsoft ai dati dei clienti e ai sistemi che contengono i dati dei clienti).
- **Cloud per enti pubblici:** Include Microsoft 365 e azure disponibili per i clienti del governo degli Stati Uniti.

Ai fini di questo articolo, i servizi Microsoft 365 includono:

- [Exchange Online](/Exchange/exchange-online)
- [Exchange Online Protection](/Office365/SecurityCompliance/eop/exchange-online-protection-overview)
- [SharePoint Online](/sharepoint/sharepoint-online)
- [OneDrive for Business](/OneDrive/onedrive)
- [Skype for Business](/SkypeForBusiness/skype-for-business-online)
- [Microsoft Teams](/MicrosoftTeams/Teams-overview)
- [Yammer](/yammer/yammer-landing-page)

## <a name="microsoft-365-access-controls"></a>Microsoft 365 di accesso

Ai fini del controllo di accesso, Microsoft classifica Microsoft 365 dati come dati dei clienti o altri tipi di dati.

### <a name="customer-data"></a>Dati del cliente

I dati dei clienti sono tutti i dati forniti da o per conto di un cliente quando si utilizzano Microsoft 365 servizi. Questi dati sono contenuti dei clienti creati o caricati direttamente da Microsoft 365 utenti, tra cui:

- Messaggi di posta elettronica
- SharePoint Contenuto online
- Messaggi istantanei
- Elementi del calendario
- Documenti
- Contatti
- Informazioni di identificazione dell'utente finale (EUII) (dati univoci per un utente o collegabili a un singolo utente ma che non includono il contenuto del cliente)

### <a name="other-types-of-data"></a>Altri tipi di dati

Altri tipi di dati includono:

- **Dati account:** Include i dati amministrativi (informazioni fornite dagli amministratori durante l'iscrizione o l'acquisto di servizi) e i dati di pagamento (informazioni sugli strumenti di pagamento, ad esempio i dettagli della carta di credito).
- **Informazioni identificabili dall'organizzazione:** Include i dati utilizzati per identificare un tenant, i dati di utilizzo e non collegabili a un singolo utente o inclusi nel contenuto del cliente.
- **Metadati di sistema:** Include i log dei servizi che contengono impostazioni di configurazione, stato del sistema, indirizzi IP Microsoft e informazioni tecniche sulle sottoscrizioni e i tenant.

Microsoft ha stabilito meccanismi di controllo dell'accesso per garantire che nessuno abbia accesso non approvato ai dati dei clienti o ai dati di controllo di accesso. I dati del controllo di accesso gestiscono l'accesso ad altri tipi di dati o funzioni all'interno dell'ambiente, tra cui l'accesso al contenuto del cliente o all'IME, alle password Microsoft, ai certificati di sicurezza e ad altri dati correlati all'autenticazione. I meccanismi di controllo dell'accesso sono inoltre in grado di proteggersi dall'accesso fisico, logico o remoto non approvato all'Microsoft 365 di produzione.

Esistono tre categorie di controlli di accesso utilizzati da Microsoft per le attività Microsoft 365:

- Controlli di isolamento
- Controlli del personale
- Controlli della tecnologia

Se combinati, questi controlli consentono di prevenire e rilevare azioni dannose in Microsoft 365. Oltre ai controlli di isolamento, personale e tecnologia utilizzati da Microsoft, esiste una quarta categoria di controlli: i controlli implementati dai clienti.

Microsoft 365 consente di gestire i dati nello stesso modo in cui i dati vengono gestiti in ambienti locali. La persona che si i signs up an organization for Microsoft 365 diventa automaticamente un amministratore globale. L'amministratore globale ha accesso a tutte le funzionalità dei portali di gestione e può:

- Creare o modificare utenti
- Assegnare ruoli di amministratore ad altri utenti
- Reimposta password utente
- Gestire le licenze utente
- Gestire domini
- Approvare le richieste di Customer Lockbox

È consigliabile configurare almeno due account amministratore per ogni organizzazione. Per le organizzazioni di grandi dimensioni, è consigliabile utilizzare account di amministrazione specializzati che sconsigliano funzioni diverse.

Per informazioni sull'assegnazione di ruoli e autorizzazioni di amministratore, vedere [Assegnare](/microsoft-365/admin/add-users/assign-admin-roles) ruoli di amministratore e [Informazioni sui ruoli di amministratore.](/microsoft-365/admin/add-users/about-admin-roles)

## <a name="related-links"></a>Collegamenti correlati

- [Isolamento in Microsoft 365](assurance-isolation-in-microsoft-365.md)
- [Screening precedente all'impiego presso Microsoft](assurance-pre-employment-screening.md)
- [Controllo in background di Microsoft Cloud](assurance-cloud-background-check.md)
- [Monitoraggio e controllo dei controlli di accesso ](assurance-monitoring-and-auditing-access-controls.md)
- [Controlli di accesso di Yammer Enterprise](assurance-yammer-enterprise-access-controls.md)
