---
title: Federal Information Processing Standard (FIPS) Publication 140-2
description: Microsoft certifica che i moduli crittografici sono conformi al Federal Information Processing Standard degli Stati Uniti.
keywords: Microsoft 365, conformità, offerte
localization_priority: None
ms.prod: microsoft-365-enterprise
ms.topic: article
f1.keywords:
- NOCSH
ms.author: robmazz
author: robmazz
manager: laurawi
audience: itpro
ms.collection:
- M365-security-compliance
- MS-Compliance
hideEdit: true
titleSuffix: Microsoft Compliance
ms.openlocfilehash: d7d1f47d7f76f9fc6d3cefa6cac5be807af98cbc
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120835"
---
# <a name="federal-information-processing-standard-fips-publication-140-2"></a>Federal Information Processing Standard (FIPS) Publication 140-2

## <a name="fips-140-2-standard-overview"></a>Panoramica degli standard FIPS 140-2

La Federal Information Processing Standard (FIPS) Publication 140-2 è uno standard del governo degli Stati Uniti che definisce i requisiti minimi di sicurezza per i moduli crittografici nei prodotti information technology, come definito nella sezione 5131 dell'Information Technology Management Reform Act del 1996.

Cryptographic [Module Validation Program](https://csrc.nist.gov/Projects/cryptographic-module-validation-program) (CMVP), un impegno congiunto del National Institute of Standards and Technology (NIST) degli Stati Uniti e del Canadian Centre for Cyber Security (CCCS), convalida i moduli crittografici in base allo standard Security Requirements for *Cryptographic Modules* (ad esempio, FIPS 140-2) e agli standard di crittografia FIPS correlati. I requisiti di sicurezza FIPS 140-2 riguardano 11 aree correlate alla progettazione e all'implementazione di un modulo crittografico. Il NIST Information Technology Laboratori gestisce un programma correlato che convalida gli algoritmi crittografici approvati da FIPS nel modulo.

## <a name="microsofts-approach-to-fips-140-2-validation"></a>Approccio di Microsoft alla convalida FIPS 140-2

Microsoft si impegna attivamente a soddisfare i requisiti 140-2, dopo aver convalidato i moduli crittografici dall'inizio dello standard nel 2001. Microsoft convalida i propri moduli crittografici nell'ambito del National Institute of Standards and Technology (NIST) [Cryptographic Module Validation Program](https://csrc.nist.gov/Projects/cryptographic-module-validation-program) (CMVP). Più prodotti Microsoft, inclusi molti servizi cloud, usano questi moduli di crittografia.

Per informazioni tecniche sui moduli crittografici di Microsoft Windows, sui criteri di sicurezza per ogni modulo e sul catalogo dei dettagli del certificato CMVP, vedere il contenuto di [Windows e Windows Server FIPS 140-2.](https://aka.ms/AA6ehud)

## <a name="microsoft-in-scope-cloud-services"></a>Servizi cloud Microsoft in ambito

Mentre la guida all'implementazione FIPS 140-2 CMVP corrente preclude una convalida FIPS 140-2 per un servizio cloud stesso; I provider di servizi cloud possono scegliere di ottenere e utilizzare moduli crittografici convalidati FIPS 140 per gli elementi di elaborazione che costituiscono il servizio cloud. I servizi online Microsoft che includono componenti convalidati da FIPS 140-2 includono, tra gli altri:

- [Azure e Azure per enti pubblici](/azure/azure-government/documentation-government-plan-security)
- [Dynamics 365 e Dynamics 365 Government](/microsoft-365/compliance/office-365-encryption-in-microsoft-dynamics-365)
- [Office 365, Office 365 U.S. Government e Office 365 U.S. Government Defense](/microsoft-365/compliance/office-365-encryption-risks-and-protections)

## <a name="frequently-asked-questions"></a>Domande frequenti

**Qual è la differenza tra "FIPS 140 Validated" e "FIPS 140 compliant"?**

"FIPS 140 Validated" significa che il modulo crittografico o un prodotto che incorpora il modulo è stato convalidato ("certificato") dal CMVP come soddisfare i requisiti FIPS 140-2. "FiPS 140 compliant" è un termine del settore per i prodotti IT che si basano sui prodotti CONVALIDAti FIPS 140 per la funzionalità di crittografia.

**Quando Microsoft esegue una convalida FIPS 140?**

La cadenza per l'avvio di una convalida del modulo è allineata agli aggiornamenti delle funzionalità di Windows 10 e Windows Server. Con l'evoluzione del settore software, i sistemi operativi vengono rilasciati con maggiore frequenza, con aggiornamenti software mensili. Microsoft avvia la convalida per i rilasci di funzionalità, ma tra i rilasci cerca di ridurre al minimo le modifiche ai moduli di crittografia.

**Quali computer sono inclusi in una convalida FIPS 140?**

Microsoft convalida i moduli crittografici su un campione rappresentativo di configurazioni hardware che eseguono Windows 10 e Windows Server. È prassi comune nel settore accettare questa convalida FIPS 140-2 quando un ambiente utilizza hardware, simile agli esempi utilizzati per il processo di convalida.

**Nel sito Web NIST sono elencati molti moduli. Come posso sapere quale si applica alla mia agenzia?**

Se è necessario utilizzare moduli di crittografia convalidati tramite FIPS 140-2, è necessario verificare che la versione in uso sia presente nell'elenco di convalida. CMVP e Microsoft gestiscono un elenco di moduli crittografici convalidati, organizzati per rilascio del prodotto, insieme alle istruzioni per identificare i moduli installati in un sistema Windows. Per altre informazioni sulla configurazione di sistemi conformi, vedi il contenuto di [Windows e Windows Server FIPS 140-2.](https://aka.ms/AA6ehud)

**Cosa significa "Se gestito in modalità FIPS" su un certificato?**

Questo avviso informa il lettore che è necessario seguire le regole di configurazione e sicurezza necessarie per utilizzare il modulo di crittografia in modo coerente con i criteri di sicurezza FIPS 140-2. Ogni modulo ha un proprio criterio di sicurezza, una specifica precisa delle regole di sicurezza in base alle quali funzionerà, e utilizza algoritmi di crittografia approvati, la gestione delle chiavi crittografiche e tecniche di autenticazione. Le regole di sicurezza sono definite nei criteri di sicurezza per ogni modulo. Per altre informazioni, inclusi i collegamenti ai criteri di sicurezza per ogni modulo convalidato tramite CMVP, vedi il contenuto [FIPS 140-2](https://aka.ms/AA6ehud)di Windows e Windows Server.

**FedRAMP richiede la convalida FIPS 140-2?**

Sì, il Federal Risk and Authorization Management Program (FedRAMP) si basa sulle linee di base del controllo definite dalla [NIST SP 800-53 Revision 4,](https://nvd.nist.gov/800-53/Rev4/)inclusa la protezione crittografica [SC-13](https://nvd.nist.gov/800-53/Rev4/control/SC-13) che impone l'uso della crittografia convalidata da FIPS o della crittografia approvata dall'NSA.

**In che modo Microsoft Azure supporta FIPS 140-2?**

Azure è creato con una combinazione di hardware, sistemi operativi disponibili in commercio (Linux e Windows) e versione di Windows specifica di Azure. Tramite [il](https://www.microsoft.com/securityengineering/sdl/) Ciclo di vita dello sviluppo della sicurezza (SDL) di Microsoft, tutti i servizi di Azure usano algoritmi approvati da FIPS 140-2 per la sicurezza dei dati, perché il sistema operativo usa algoritmi approvati da FIPS 140-2 mentre opera in un cloud iper-scala.

**Posso usare l'adesione di Microsoft a FIPS 140-2 nel processo di certificazione della mia agenzia?**

Per essere conforme a FIPS 140-2, il sistema deve essere configurato per l'esecuzione in una modalità di funzionamento approvata da FIPS, che include la garanzia che un modulo di crittografia utilizzi solo algoritmi approvati da FIPS. Per altre informazioni sulla configurazione di sistemi conformi, vedi il contenuto di [Windows e Windows Server FIPS 140-2.](https://aka.ms/AA6ehud)

**Qual è la relazione tra FIPS 140-2 e Common Criteria?**

Si tratta di due standard di sicurezza separati con scopi diversi, ma complementari. FIPS 140-2 è progettato specificamente per la convalida dei moduli crittografici software e hardware, mentre Common Criteria è progettato per valutare le funzioni di sicurezza nei prodotti hardware e software IT. Le valutazioni dei criteri comuni spesso si basano sulle convalide FIPS 140-2 per garantire che le funzionalità di crittografia di base siano implementate correttamente.

## <a name="resources"></a>Risorse

- [Requisiti di sicurezza FIPS Pub 140-2 per i moduli crittografici](https://csrc.nist.gov/publications/fips/fips140-2/fips1402.pdf)
- [Programma di convalida del modulo crittografico NIST](https://csrc.nist.gov/groups/STM/cmvp/index.html)
- [Windows, Windows Server e FIPS 140-2](/windows/security/threat-protection/fips-140-validation)
- [Conformità nel Centro protezione Microsoft](https://www.microsoft.com/trust-center/compliance/compliance-overview)
