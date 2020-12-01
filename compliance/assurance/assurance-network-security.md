---
title: Protezione di rete
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
ms.openlocfilehash: c063460fdfba44265b3a1504a049a4772b484dff
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/30/2020
ms.locfileid: "49507758"
---
# <a name="network-security-overview"></a>Panoramica della sicurezza di rete

## <a name="how-does-microsoft-365-secure-the-network-boundary"></a>In che modo Microsoft 365 protegge il limite di rete?

Microsoft 365 impiega diverse strategie per la protezione dei limiti di rete, tra cui il rilevamento e la prevenzione automatici degli attacchi basati sulla rete, i dispositivi firewall specializzati e Exchange Online Protection (EOP) per l'utilizzo di posta indesiderata e antimalware. Inoltre, Microsoft 365 separa l'ambiente di produzione in segmenti di rete isolati logicamente, con la sola comunicazione necessaria consentita tra i segmenti. Il traffico di rete è protetto utilizzando ulteriori firewall di rete nei punti limite per consentire di rilevare, prevenire e mitigare gli attacchi di rete.

## <a name="how-does-microsoft-365-defend-against-ddos-attacks"></a>In che modo Microsoft 365 difende gli attacchi DDoS?

La presenza Internet di grandi dimensioni di Microsoft lo isola dagli effetti negativi di molti attacchi DDoS (Denial of Service) distribuiti. Le istanze distribuite di ogni servizio Microsoft 365 e di più route per ogni servizio limitano l'impatto degli attacchi DDoS sul sistema. Questa ridondanza migliora la capacità di Microsoft 365 di assorbire attacchi DDoS e aumenta la quantità di tempo disponibile per rilevare e mitigare gli attacchi DDoS prima che influenzino la disponibilità del servizio.

Oltre all'architettura del sistema ridondante Microsoft, Microsoft utilizza sofisticati strumenti di rilevamento e attenuazione per rispondere agli attacchi DDoS. I firewall speciali monitorano e rilasciano il traffico indesiderato prima che attraversi il limite nella rete, riducendo lo stress sui sistemi situati all'interno del limite di rete. Per proteggere ulteriormente i servizi cloud, Microsoft utilizza un sistema di difesa DDoS distribuito come parte di Microsoft Azure. Il sistema di protezione DDoS di Azure è stato creato per resistere agli attacchi dall'esterno e da altri tenant di Azure.

## <a name="how-does-microsoft-365-protect-users-against-spam-and-malware-being-uploaded-or-sent-through-online-services"></a>In che modo Microsoft 365 protegge gli utenti da messaggi di posta indesiderata e malware caricati o inviati tramite i servizi online?

Microsoft 365 genera la protezione antimalware in servizi che possono essere vettori per codice dannoso, ad esempio Exchange Online e SharePoint Online. Exchange Online Protection (EOP) esegue la ricerca di tutti i messaggi di posta elettronica e gli allegati per il malware quando entrano ed escono dal sistema, impedendo la recapito dei messaggi e degli allegati infetti. Il filtro di posta indesiderata avanzato viene applicato automaticamente ai messaggi in ingresso e in uscita per evitare che le organizzazioni dei clienti ricevano e inviino posta indesiderata. Questo livello di protezione protegge gli attacchi che sfruttano la posta elettronica indesiderata o non autorizzata, ad esempio attacchi di phishing. SharePoint Online utilizza lo stesso motore di rilevamento dei virus per analizzare selettivamente i file caricati per la presenza di malware. Se un file è contrassegnato come infetto, agli utenti viene impedito di scaricare o sincronizzare il file per proteggere gli endpoint client.

## <a name="related-external-regulations--certifications"></a>Normative esterne correlate & certificazioni

I servizi online di Microsoft vengono controllati regolarmente per la conformità con le certificazioni e le normative esterne. Per la convalida dei controlli relativi alla sicurezza di rete, fare riferimento alla tabella seguente.

| **Verifiche esterne** | **Sezione** | **Data ultimo rapporto** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365)](https://compliance.microsoft.com/compliancemanager) | SC-5: Denial of Service Protection <br> SC-7: protezione da confini <br> SI-2: correzione del difetto <br> SI-3: protezione da codice dannoso <br> SI-8: protezione dalla posta indesiderata | 24 settembre 2020 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b07c0f7b-6bd5-4544-8255-7a5f14bf914a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-27: analisi della vulnerabilità | 30 settembre 2019 |
| [SOC 2 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=fa062990-e758-4ddc-ace3-7fb21a301d09&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Rep-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-27: analisi della vulnerabilità <br> CA-45: anti-malware | 30 settembre 2019 |