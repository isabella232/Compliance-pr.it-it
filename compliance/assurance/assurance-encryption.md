---
title: Panoramica della crittografia e della gestione delle chiavi
description: Informazioni sulla crittografia e la gestione delle chiavi in Microsoft 365
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
ms.openlocfilehash: 96a3871657dc1e6021949ca9fc2376df382fe15b
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/30/2020
ms.locfileid: "49508198"
---
# <a name="encryption-and-key-management-overview"></a>Panoramica della crittografia e della gestione delle chiavi

## <a name="what-role-does-encryption-play-in-protecting-customer-content"></a>Quale ruolo svolge la crittografia nella protezione dei contenuti dei clienti?

La maggior parte dei servizi cloud di Microsoft Business è multitenant, ovvero il contenuto del cliente può essere archiviato nello stesso hardware fisico di altri clienti. Per proteggere la riservatezza del contenuto dei clienti, Microsoft 365 crittografa tutti i dati a riposo e in transito con alcuni dei protocolli di crittografia più forti e sicuri disponibili.

La crittografia non è un sostituto per i controlli di accesso forti. Il criterio di controllo dell'accesso di Microsoft 365 (ZSA) consente di proteggere il contenuto dei clienti da accessi non autorizzati da parte dei dipendenti Microsoft. La crittografia integra il controllo di accesso proteggendo la riservatezza del contenuto dei clienti dovunque sia memorizzato e impedendo la lettura del contenuto durante il transito tra Microsoft 365 Systems o tra Microsoft 365 e il cliente.

## <a name="how-does-microsoft-365-encrypt-data-at-rest"></a>In che modo Microsoft 365 crittografa i dati-at-rest?

Tutto il contenuto del cliente in Microsoft 365 è protetto da una o più forme di crittografia. I server Microsoft utilizzano BitLocker per crittografare le unità disco che contengono contenuto del cliente a livello di volume. La crittografia fornita da BitLocker protegge il contenuto del cliente in caso di lapsus in altri processi o controlli, ad esempio il controllo dell'accesso o il riciclo dell'hardware, che potrebbe causare l'accesso fisico non autorizzato ai dischi contenenti contenuto del cliente.

Exchange Online, Microsoft teams, SharePoint Online e OneDrive for business utilizzano anche la crittografia del servizio a livello di applicazione per crittografare il contenuto del cliente. La crittografia del servizio fornisce funzionalità di protezione e gestione dei diritti oltre alla protezione avanzata dalla crittografia. Consente inoltre la separazione tra i sistemi operativi Windows e i dati dei clienti archiviati o elaborati da tali sistemi operativi.

## <a name="how-does-microsoft-365-encrypt-data-in-transit"></a>In che modo Microsoft 365 crittografa i dati in transito?

I prodotti e servizi Microsoft 365 utilizzano protocolli di trasporto forti, come TLS, per impedire alle parti non autorizzate di intercettare i dati dei clienti mentre si sposta su una rete. Tra gli esempi di dati in transito sono inclusi i messaggi di posta elettronica in fase di recapito, le conversazioni che si svolgono in una riunione online o i file che vengono replicati tra i datacenter.

In Microsoft 365, i dati vengono considerati ' in transito ' quando il dispositivo di un utente comunica con un server Microsoft o un server Microsoft comunica con un altro server. Exchange Online, SharePoint Online, Microsoft teams e Office Online tutti utilizzano TLS per garantire che i dati rimangano riservati durante il transito.

## <a name="how-does-microsoft-365-manage-the-keys-used-for-encryption"></a>In che modo Microsoft 365 gestisce le chiavi utilizzate per la crittografia?

La crittografia avanzata è sicura solo come le chiavi utilizzate per crittografare i dati. Microsoft utilizza i propri certificati di sicurezza per crittografare le connessioni TLS per i dati in transito. Per i dati di riposo, i volumi protetti da BitLocker sono crittografati con una chiave di crittografia a volume completo, crittografata con una chiave master del volume, che a sua volta è associata al TPM (Trusted Platform Module) nel server. BitLocker utilizza algoritmi FIPS conformi per garantire che le chiavi di crittografia non vengano mai archiviate o inviate tramite cavo in chiaro.

La crittografia dei servizi fornisce un ulteriore livello di crittografia per i dati dei clienti-at-rest in Exchange Online, Microsoft teams, SharePoint Online e OneDrive for business. La crittografia dei servizi fornisce ai clienti due opzioni per la gestione delle chiavi di crittografia: chiavi gestite da Microsoft o chiave del cliente. Quando si utilizzano le chiavi gestite da Microsoft, i servizi Microsoft 365 generano e archiviano in modo sicuro le chiavi principali utilizzate per la crittografia del servizio.

I clienti con requisiti per controllare le proprie chiavi di crittografia radice possono sfruttare la crittografia del servizio con la chiave del cliente. Utilizzando la chiave del cliente, i clienti possono generare le proprie chiavi di crittografia utilizzando un modulo di servizio hardware (HSM) locale o un Vault Key di Azure (AKV). Le chiavi radice del cliente sono archiviate in AKV, dove possono essere utilizzate come radice di uno dei portachiavi che crittografa i dati o i file delle cassette postali dei clienti. Le chiavi principali del cliente possono essere accessibili solo indirettamente dal codice del servizio Microsoft 365 per la crittografia dei dati e non possono essere accessibili direttamente dai dipendenti di Microsoft.

## <a name="related-external-regulations--certifications"></a>Normative esterne correlate & certificazioni

I servizi online di Microsoft vengono controllati regolarmente per la conformità con le certificazioni e le normative esterne. Per la convalida dei controlli relativi alla crittografia e alla gestione delle chiavi, vedere la tabella seguente.

| **Verifiche esterne** | **Sezione** | **Data ultimo rapporto** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | SC-8: riservatezza e integrità della trasmissione <br> SC-13: utilizzo della crittografia <br> SC-28: protezione delle informazioni a riposo <br>  | 24 settembre 2020 |
| [ISO 27001/27002 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Dichiarazione di applicabilità](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certificazione](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A. 10.1: controlli di crittografia <br> A. 18.1.5: controlli di crittografia | 22 febbraio 2020 |
| [ISO 27017 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Dichiarazione di applicabilità](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certificazione](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A. 10.1: controlli di crittografia <br> A. 18.1.5: controlli di crittografia | 22 febbraio 2020 |
| [ISO 27018 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Dichiarazione di applicabilità](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [Certificazione](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=43e89534-f48d-42ea-a7a7-3523ff516036&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A. 11,6: crittografia delle informazioni personali trasmesse tramite reti di trasmissione di dati pubbliche | 22 febbraio 2020 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=fa062990-e758-4ddc-ace3-7fb21a301d09&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Rep-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-44: crittografia dei dati in transito <br> CA-54: crittografia data-at-rest <br> CA-62: crittografia della cassetta postale chiave del cliente <br> CA-63: eliminazione dei dati chiave del cliente <br> CA-64: chiave del cliente | 30 settembre 2019 |
| [SOC 3 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=9df8b99b-96ce-49a9-bff4-268031dcc9a6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CUEC-16: chiavi di crittografia dei clienti <br> CUEC-17: chiave del Vault del cliente <br>  CUEC-18: rotazione della chiave del cliente| 30 settembre 2019 |
