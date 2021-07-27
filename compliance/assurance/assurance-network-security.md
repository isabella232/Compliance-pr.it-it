---
title: Sicurezza di rete
description: Informazioni sulla sicurezza di rete in Microsoft 365
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
ms.openlocfilehash: 9fd4c904992f26949aed66c345dfbe9bdff47e5f
ms.sourcegitcommit: 12cec299197fbc7b05c8d7604e7047b9392e3bc8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/26/2021
ms.locfileid: "53589665"
---
# <a name="network-security-overview"></a>Panoramica sulla sicurezza di rete

## <a name="how-do-microsoft-online-services-secure-the-network-boundary"></a>In che modo i servizi online Microsoft possono proteggere il limite di rete?

I servizi online Microsoft utilizzano più strategie per proteggere i propri limiti di rete, tra cui il rilevamento e la prevenzione automatizzati degli attacchi basati sulla rete, dispositivi firewall specializzati e Exchange Online Protection (EOP) per la protezione da posta indesiderata e antimalware. Inoltre, i servizi online Microsoft separano gli ambienti di produzione in segmenti di rete logicamente isolati, con solo le comunicazioni necessarie consentite tra i segmenti. Il traffico di rete viene protetto utilizzando firewall di rete aggiuntivi nei punti di confine per rilevare, prevenire e ridurre gli attacchi di rete.

## <a name="how-do-microsoft-online-services-defend-against-ddos-attacks"></a>In che modo i servizi online Microsoft si difendono dagli attacchi DDoS?

La presenza internet di Grandi dimensioni di Microsoft la isola dagli effetti negativi di molti attacchi DDoS (Distributed Denial of Service). Le istanze distribuite di ogni servizio online Microsoft e più route per ogni servizio limitano l'impatto degli attacchi DDoS sul sistema. Questa ridondanza migliora la capacità dei servizi online Microsoft di assorbire gli attacchi DDoS e aumenta la quantità di tempo disponibile per rilevare e ridurre gli attacchi DDoS prima che incidono sulla disponibilità del servizio.

Oltre all'architettura di sistema ridondante di Microsoft, Microsoft usa sofisticati strumenti di rilevamento e mitigazione per rispondere agli attacchi DDoS. I firewall speciali monitorano e rilasciano il traffico indesiderato prima che attraversi il limite nella rete, riducendo lo stress sui sistemi che si trovano all'interno del limite di rete. Per proteggere ulteriormente i servizi cloud, Microsoft utilizza un sistema di difesa DDoS distribuito come parte di Microsoft Azure. Il sistema di difesa DDoS di Azure è progettato per resistere agli attacchi dall'esterno e da altri tenant di Azure.

## <a name="how-does-microsoft-protect-users-against-spam-and-malware-being-uploaded-or-sent-through-online-services"></a>In che modo Microsoft protegge gli utenti da posta indesiderata e malware caricati o inviati tramite servizi online?

I servizi online Microsoft generano la protezione antimalware in servizi che potrebbero essere vettori di codice dannoso, ad esempio Exchange Online e SharePoint Online. Exchange Online Protection (EOP) analizza tutti i messaggi di posta elettronica e gli allegati di posta elettronica alla ricerca di malware all'ingresso e all'uscita dal sistema, impedendo il recapito di messaggi e allegati infetti. Il filtro avanzato della posta indesiderata viene applicato automaticamente ai messaggi in ingresso e in uscita per impedire alle organizzazioni dei clienti di ricevere e inviare posta indesiderata. Questo livello di protezione protegge dagli attacchi che sfruttano la posta elettronica non richiesta o non autorizzata, ad esempio gli attacchi di phishing. SharePoint Online usa lo stesso motore di rilevamento virus per analizzare in modo selettivo i file caricati alla ricerca di malware. Se un file è contrassegnato come infetto, agli utenti viene impedito di scaricare o sincronizzare il file per proteggere gli endpoint client. Analogamente, Azure confronta gli hash relativi ai file caricati in Archiviazione di Azure con gli hash del malware noto. Quando vengono trovate corrispondenze, viene generato un avviso nel Centro sicurezza di Azure in cui viene presa una decisione sulla legittimità dell'avviso e su come deve essere indirizzato.

## <a name="related-external-regulations--certifications"></a>Normative esterne correlate & certificazioni

I servizi online di Microsoft vengono regolarmente controllati per la conformità alle normative e alle certificazioni esterne. Fare riferimento alla tabella seguente per la convalida dei controlli correlati alla sicurezza di rete.

### <a name="azure-and-dynamics-365"></a>Azure e Dynamics 365

| **Controlli esterni** | **Sezione** | **Data ultimo report** |
|:--------------------|:------------|:-----------------------|
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b8721ebd-af20-42fe-b22f-8332b0a19517&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=234a0f57-83c1-4afc-a586-a0e7a59592f7&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 3](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=75c8cbf6-e456-473c-a05e-34fea888ec2a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | VM-1: registrazione eventi di sicurezza <br> VM-3: rilevamento e monitoraggio delle intrusioni <br> VM-4: indagine sugli eventi dannosi <br> VM-6: analisi delle vulnerabilità <br> VM-7: configurazione dei dispositivi di rete <br> VM-8: test di penetrazione <br> VM-9: registrazione eventi di sicurezza dei dispositivi di rete <br> VM-13: mitigazione della vulnerabilità dei dispositivi di rete | 31 marzo. 2021 |

### <a name="office-365"></a>Office 365

| **Controlli esterni** | **Sezione** | **Data ultimo report** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP](https://compliance.microsoft.com/compliancemanager) | SC-5: Protezione denial of service <br> SC-7: Protezione dei limiti <br> SI-2: correzione dei difetti <br> SI-3: protezione da codice dannoso <br> SI-8: Protezione da posta indesiderata | 24 settembre 2020 |
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-27: Analisi delle vulnerabilità | 24 dicembre 2020 |
| [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-27: Analisi delle vulnerabilità <br> CA-45: Antimalware | 24 dicembre 2020 |