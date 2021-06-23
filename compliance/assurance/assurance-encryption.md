---
title: Panoramica sulla crittografia e sulla gestione delle chiavi
description: Informazioni sulla crittografia e sulla gestione delle chiavi in Microsoft 365
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
ms.openlocfilehash: 5e46fdb5ddc3b1b80df0bcadf9054b9353a0dc8e
ms.sourcegitcommit: fb379d1110a9a86c7f9bab8c484dc3f4b3dfd6f0
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/23/2021
ms.locfileid: "53088645"
---
# <a name="encryption-and-key-management-overview"></a>Panoramica sulla crittografia e sulla gestione delle chiavi

## <a name="what-role-does-encryption-play-in-protecting-customer-content"></a>Qual è il ruolo della crittografia nella protezione dei contenuti dei clienti?

La maggior parte dei servizi cloud aziendali Microsoft è multitenant, il che significa che i contenuti dei clienti possono essere archiviati sullo stesso hardware fisico di quello di altri clienti. Per proteggere la riservatezza dei contenuti dei clienti, Microsoft 365 tutti i dati in stato di inattività e in transito con alcuni dei protocolli di crittografia più sicuri e più sicuri disponibili.

La crittografia non sostituisce i controlli di accesso avanzata. Microsoft 365 di controllo degli accessi di Zero Standing Access (ZSA) protegge i contenuti dei clienti da accessi non autorizzati da parte dei dipendenti Microsoft. La crittografia integra il controllo di accesso proteggendo la riservatezza del contenuto del cliente ovunque sia archiviato e impedendo la lettura del contenuto durante il transito tra sistemi Microsoft 365 o tra Microsoft 365 e il cliente.

## <a name="how-does-microsoft-365-encrypt-data-at-rest"></a>In che modo Microsoft 365 crittografare i dati in fase di riposo?

Tutto il contenuto dei clienti Microsoft 365 è protetto da una o più forme di crittografia. I server Microsoft usano BitLocker per crittografare le unità disco contenenti il contenuto dei clienti a livello di volume. La crittografia fornita da BitLocker protegge i contenuti dei clienti in caso di problemi in altri processi o controlli (ad esempio, il controllo dell'accesso o il riciclo dell'hardware) che potrebbero causare l'accesso fisico non autorizzato ai dischi contenenti contenuti dei clienti.

Exchange Online, Microsoft Teams, SharePoint Online e OneDrive for Business utilizzare la crittografia del servizio a livello di applicazione per crittografare il contenuto dei clienti. La crittografia del servizio offre funzionalità di gestione e protezione dei diritti in più di una protezione avanzata della crittografia. Consente inoltre la separazione tra Windows e i dati dei clienti archiviati o elaborati da tali sistemi operativi.

## <a name="how-does-microsoft-365-encrypt-data-in-transit"></a>In che modo Microsoft 365 crittografare i dati in transito?

Microsoft 365 prodotti e servizi utilizzano protocolli di trasporto forti, ad esempio TLS, per impedire a parti non autorizzate di intercettare i dati dei clienti mentre si spostano su una rete. Esempi di dati in transito includono i messaggi di posta elettronica in fase di recapito, le conversazioni in corso in una riunione online o i file replicati tra datacenter.

In Microsoft 365, i dati vengono considerati "in transito" ogni volta che il dispositivo di un utente comunica con un server Microsoft o un server Microsoft comunica con un altro server. Exchange Online, SharePoint Online, Microsoft Teams e Office Online usano tutti TLS per garantire che i dati rimangano riservati durante il transito.

## <a name="how-does-microsoft-365-manage-the-keys-used-for-encryption"></a>In che modo Microsoft 365 le chiavi utilizzate per la crittografia?

La crittografia avanzata è sicura solo quanto le chiavi utilizzate per crittografare i dati. Microsoft usa i propri certificati di sicurezza per crittografare le connessioni TLS per i dati in transito. Per i dati in pausa, i volumi protetti con BitLocker vengono crittografati con una chiave di crittografia del volume completa, che viene crittografata con una chiave master del volume, che a sua volta è associata al TPM (Trusted Platform Module) nel server. BitLocker usa algoritmi conformi a FIPS per garantire che le chiavi di crittografia non siano mai archiviate o inviate in rete in chiaro.

La crittografia del servizio offre un ulteriore livello di crittografia per i dati dei clienti in Exchange Online, Microsoft Teams, SharePoint Online e OneDrive for Business. La crittografia del servizio offre ai clienti due opzioni per la gestione delle chiavi di crittografia: le chiavi gestite da Microsoft o la chiave cliente. Quando si utilizzano chiavi gestite da Microsoft, i servizi Microsoft 365 generano e archiviano automaticamente in modo sicuro le chiavi radice utilizzate per la crittografia dei servizi.

I clienti con requisiti per controllare le proprie chiavi di crittografia radice possono sfruttare la crittografia del servizio con la chiave del cliente. Usando customer key, i clienti possono generare le proprie chiavi crittografiche usando un HSM (Hardware Service Module) locale o Azure Key Vault (AKV). Le chiavi radice dei clienti sono archiviate in AKV, dove possono essere utilizzate come radice di uno dei portachiavi che crittografa i file o i dati delle cassette postali dei clienti. Le chiavi radice dei clienti possono essere accessibili solo indirettamente Microsoft 365 codice di servizio per la crittografia dei dati e non sono accessibili direttamente dai dipendenti Microsoft.

## <a name="related-external-regulations--certifications"></a>Normative esterne correlate & certificazioni

I servizi online di Microsoft vengono regolarmente controllati per la conformità alle normative e alle certificazioni esterne. Fare riferimento alla tabella seguente per la convalida dei controlli relativi alla crittografia e alla gestione delle chiavi.

| **Controlli esterni** | **Sezione** | **Data ultimo report** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | SC-8: riservatezza e integrità della trasmissione <br> SC-13: utilizzo della crittografia <br> SC-28: Protezione delle informazioni in pausa <br>  | 24 settembre 2020 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Dichiarazione di applicabilità](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Certificazione](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.10.1: Controlli crittografici <br> A.18.1.5: Controlli crittografici | 20 aprile 2021 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Dichiarazione di applicabilità](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Certificazione](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.10.1: Controlli crittografici <br> A.18.1.5: Controlli crittografici | 20 aprile 2021 |
| [ISO 27018 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Dichiarazione di applicabilità](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Certificazione](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=43e89534-f48d-42ea-a7a7-3523ff516036&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.11.6: Crittografia delle informazioni personali trasmesse su reti di trasmissione dati pubbliche | 20 aprile 2021 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-44: Crittografia dei dati in transito <br> CA-54: Crittografia dati in locale <br> CA-62: crittografia della cassetta postale chiave del cliente <br> CA-63: eliminazione dei dati chiave del cliente <br> CA-64: Codice cliente | 24 dicembre 2020 |
| [SOC 3 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=274054e5-4968-48d2-bf94-9a8eda5d7a93&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CUEC-16: chiavi di crittografia dei clienti <br> CUEC-17: insieme di credenziali delle chiavi del cliente <br>  CUEC-18: rotazione dei tasti del cliente| 24 dicembre 2020 |
