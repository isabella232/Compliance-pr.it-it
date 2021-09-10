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
ms.openlocfilehash: dc53f42c6aa7ce16e1291538bfad6d63c5a1689d
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2021
ms.locfileid: "58947098"
---
# <a name="encryption-and-key-management-overview"></a>Panoramica sulla crittografia e sulla gestione delle chiavi

## <a name="what-role-does-encryption-play-in-protecting-customer-content"></a>Quale ruolo ha la crittografia nella protezione dei contenuti dei clienti?

La maggior parte dei servizi cloud aziendali Microsoft sono multi-tenant, il che significa che i contenuti dei clienti possono essere archiviati sullo stesso hardware fisico di altri clienti. Per proteggere la riservatezza dei contenuti dei clienti, i servizi online Microsoft crittografano tutti i dati in fase di riposo e in transito con alcuni dei protocolli di crittografia più sicuri e più sicuri disponibili.

La crittografia non sostituisce i controlli di accesso avanzata. Il criterio di controllo di accesso di Microsoft zero standing access (ZSA) protegge i contenuti dei clienti da accessi non autorizzati da parte dei dipendenti Microsoft. La crittografia integra il controllo di accesso proteggendo la riservatezza dei contenuti dei clienti ovunque sia archiviato e impedendo la lettura del contenuto durante il transito tra i sistemi dei servizi online Microsoft o tra i servizi online Microsoft e il cliente.

## <a name="how-do-microsoft-online-services-encrypt-data-at-rest"></a>In che modo i servizi online Microsoft crittografano i dati in fase di riposo?

Tutti i contenuti dei clienti nei servizi online Microsoft sono protetti da una o più forme di crittografia. I server Microsoft usano BitLocker per crittografare le unità disco contenenti il contenuto dei clienti a livello di volume. La crittografia fornita da BitLocker protegge i contenuti dei clienti in caso di problemi in altri processi o controlli (ad esempio, il controllo dell'accesso o il riciclo dell'hardware) che potrebbero causare l'accesso fisico non autorizzato ai dischi contenenti contenuti dei clienti.

Oltre alla crittografia a livello di volume, i servizi online Microsoft usano la crittografia dei servizi a livello di applicazione per crittografare il contenuto dei clienti. La crittografia del servizio offre funzionalità di gestione e protezione dei diritti in più di una protezione avanzata della crittografia. Consente inoltre la separazione tra Windows e i dati dei clienti archiviati o elaborati da tali sistemi operativi.

## <a name="how-do-microsoft-online-services-encrypt-data-in-transit"></a>In che modo i servizi online Microsoft crittografano i dati in transito?

I servizi online Microsoft usano protocolli di trasporto forti, come TLS, per impedire a parti non autorizzate di intercettare i dati dei clienti mentre si spostano in rete. Esempi di dati in transito includono i messaggi di posta elettronica in fase di recapito, le conversazioni in corso in una riunione online o i file replicati tra datacenter.

Per i servizi online Microsoft, i dati sono considerati "in transito" ogni volta che il dispositivo di un utente comunica con un server Microsoft o un server Microsoft comunica con un altro server.

## <a name="how-do-microsoft-online-services-manage-the-keys-used-for-encryption"></a>In che modo i servizi online Microsoft gestiscono le chiavi utilizzate per la crittografia?

La crittografia avanzata è sicura solo quanto le chiavi utilizzate per crittografare i dati. Microsoft usa i propri certificati di sicurezza per crittografare le connessioni TLS per i dati in transito. Per i dati in pausa, i volumi protetti con BitLocker vengono crittografati con una chiave di crittografia del volume completa, che viene crittografata con una chiave master del volume, che a sua volta è associata al TPM (Trusted Platform Module) nel server. BitLocker usa algoritmi conformi a FIPS per garantire che le chiavi di crittografia non siano mai archiviate o inviate in rete in chiaro.

La crittografia dei servizi offre un altro livello di crittografia per i dati dei clienti in fase di riposo, offrendo ai clienti due opzioni per la gestione delle chiavi di crittografia: chiavi gestite da Microsoft o chiave cliente. Quando si utilizzano chiavi gestite da Microsoft, i servizi online Microsoft generano e archiviano automaticamente le chiavi radice utilizzate per la crittografia dei servizi.

I clienti con requisiti per controllare le proprie chiavi di crittografia radice possono usare la crittografia del servizio con la chiave del cliente. Usando customer key, i clienti possono generare le proprie chiavi crittografiche usando un HSM (Hardware Service Module) locale o Azure Key Vault (AKV). Le chiavi radice dei clienti sono archiviate in AKV, dove possono essere utilizzate come radice di uno dei portachiavi che crittografa i file o i dati delle cassette postali dei clienti. Le chiavi radice dei clienti possono essere accessibili solo indirettamente dal codice del servizio online Microsoft per la crittografia dei dati e non sono accessibili direttamente dai dipendenti Microsoft.

## <a name="related-external-regulations--certifications"></a>Normative esterne correlate & certificazioni

I servizi online di Microsoft vengono regolarmente controllati per la conformità alle normative e alle certificazioni esterne. Fare riferimento alla tabella seguente per la convalida dei controlli relativi alla crittografia e alla gestione delle chiavi.

### <a name="azure-and-dynamics-365"></a>Azure e Dynamics 365

| **Controlli esterni** | **Sezione** | **Data ultimo report** |
|:--------------------|:------------|:-----------------------|
| [ISO 27001/27002](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Dichiarazione di applicabilità](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=00af6c3e-7f3e-4e0d-8b0e-79f45ef2cef1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Certificazione](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7af5304-3a31-40e6-9abb-e26352305d41&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.10.1: Controlli crittografici <br> A.18.1.5: Controlli crittografici | 2 dicembre 2020 |
| [ISO 27017](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Dichiarazione di applicabilità](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a3bca0ac-867d-4204-b66b-13665f5f1e8d&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Certificazione](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=25718a8a-f34d-41e1-a95a-c49246508787&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.10.1: Controlli crittografici <br> A.18.1.5: Controlli crittografici | 2 dicembre 2020 |
| [ISO 27018](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Dichiarazione di applicabilità](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=00af6c3e-7f3e-4e0d-8b0e-79f45ef2cef1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [Certificazione](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=56904fc3-0942-4ff5-9eef-7cabc751a25c&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.11.6: Crittografia delle informazioni personali trasmesse su reti di trasmissione dati pubbliche | 2 dicembre 2020 |
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b8721ebd-af20-42fe-b22f-8332b0a19517&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=234a0f57-83c1-4afc-a586-a0e7a59592f7&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 3](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=75c8cbf6-e456-473c-a05e-34fea888ec2a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | DS-1: archiviazione sicura di certificati e chiavi crittografici <br> DS-2: i dati dei clienti vengono crittografati in transito <br> DS-3: comunicazione interna dei componenti di Azure crittografati in transito <br> DS-4: controlli e procedure crittografici | 31 marzo 2021 |

### <a name="office-365"></a>Office 365

| **Controlli esterni** | **Sezione** | **Data ultimo report** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP](https://compliance.microsoft.com/compliancemanager) | SC-8: riservatezza e integrità della trasmissione <br> SC-13: utilizzo della crittografia <br> SC-28: Protezione delle informazioni in pausa <br>  | 24 settembre 2020 |
| [ISO 27001/27002/27017](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Dichiarazione di applicabilità](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.10.1: Controlli crittografici <br> A.18.1.5: Controlli crittografici | 20 aprile 2021 |
| [ISO 27018](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [Dichiarazione di applicabilità](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.11.6: Crittografia delle informazioni personali trasmesse su reti di trasmissione dati pubbliche | 20 aprile 2021 |
| [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-44: Crittografia dei dati in transito <br> CA-54: Crittografia dati in locale <br> CA-62: crittografia della cassetta postale chiave del cliente <br> CA-63: Eliminazione dei dati chiave del cliente <br> CA-64: Codice cliente | 24 dicembre 2020 |
| [SOC 3](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=274054e5-4968-48d2-bf94-9a8eda5d7a93&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CUEC-16: chiavi di crittografia dei clienti <br> CUEC-17: insieme di credenziali delle chiavi del cliente <br>  CUEC-18: rotazione dei tasti del cliente| 24 dicembre 2020 |
