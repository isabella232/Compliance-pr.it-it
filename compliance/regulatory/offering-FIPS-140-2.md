---
title: Pubblicazione FIPS (Federal Information Processing Standard) 140-2
description: Microsoft certifica che i suoi moduli crittografici sono conformi al Federal Information Processing Standard statunitense.
keywords: Microsoft 365, conformità, offerte
ms.localizationpriority: medium
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
ms.openlocfilehash: 0e087393901b76a798c4a4ea3bef25fad8dcda84
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2021
ms.locfileid: "58947915"
---
# <a name="federal-information-processing-standard-fips-publication-140-2"></a>Pubblicazione FIPS (Federal Information Processing Standard) 140-2

## <a name="fips-140-2-standard-overview"></a>Panoramica degli standard FIPS 140-2

La pubblicazione FIPS (Federal Information Processing Standard) 140-2 è uno standard governativo statunitense che definisce i requisiti minimi di sicurezza per i moduli crittografici nei prodotti information technology, come definito nella sezione 5131 dell'Information Technology Management Reform Act del 1996.

Il [Programma](https://csrc.nist.gov/Projects/cryptographic-module-validation-program) di convalida dei moduli di crittografia (CMVP), uno sforzo congiunto del National Institute of Standards and Technology (NIST) e del Canadian Centre for Cyber Security (CCCS), convalida i moduli crittografici secondo lo standard *Security Requirements for Cryptographic Modules* (ad esempio, FIPS 140-2) e gli standard di crittografia FIPS correlati. I requisiti di sicurezza FIPS 140-2 riguardano 11 aree correlate alla progettazione e all'implementazione di un modulo crittografico. Il NIST Information Technology Laboratory gestisce un programma correlato che convalida gli algoritmi di crittografia approvati da FIPS nel modulo.

## <a name="microsofts-approach-to-fips-140-2-validation"></a>Approccio di Microsoft alla convalida FIPS 140-2

Microsoft mantiene un impegno attivo a soddisfare i requisiti 140-2, dopo aver convalidato i moduli crittografici dall'inizio dello standard nel 2001. Microsoft convalida i propri moduli crittografici nell'ambito del National Institute of Standards and Technology (NIST) [Cryptographic Module Validation Program](https://csrc.nist.gov/Projects/cryptographic-module-validation-program) (CMVP). Più prodotti Microsoft, inclusi molti servizi cloud, usano questi moduli di crittografia.

Per informazioni tecniche sui moduli di crittografia di Microsoft Windows, sui criteri di sicurezza per ogni modulo e sul catalogo dei dettagli del certificato CMVP, vedere il contenuto [di Windows e Windows Server FIPS 140-2.](https://aka.ms/AA6ehud)

## <a name="microsoft-in-scope-cloud-platforms--services"></a>Piattaforme e servizi cloud Microsoft inclusi nell'ambito

Mentre la guida all'implementazione FIPS 140-2 CMVP corrente preclude una convalida FIPS 140-2 per un servizio cloud stesso; I provider di servizi cloud possono scegliere di ottenere e utilizzare moduli di crittografia convalidati FIPS 140 per gli elementi di calcolo che costituiscono il servizio cloud. I servizi online Microsoft che includono componenti convalidati da FIPS 140-2 includono, tra gli altri:

- Azure e Azure per enti pubblici
- Dynamics 365 e Dynamics 365 Government
- Office 365, Office 365 U.S. Government e Office 365 U.S. Government Defense

## <a name="azure-dynamics-365-and-fips-140-2"></a>Azure, Dynamics 365 e FIPS 140-2

Per altre informazioni sulla conformità di Azure, Dynamics 365 e altri servizi online, vedi l'offerta [Azure FIPS 140-2.](/azure/compliance/offerings/offering-fips-140-2)

## <a name="office-365-and-fips-140-2"></a>Office 365 e FIPS 140-2

### <a name="office-365-cloud-environments"></a>Ambienti cloud di Office 365

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a>Applicabilità di Office 365 e servizi inclusi nell'ambito

Usare la tabella seguente per determinare l'applicabilità per i servizi e l'abbonamento a Office 365:

| **Applicabilità** | **Servizi inclusi nell'ambito** |
|:------------------|:----------------------|
| Office 365, GCC, GCC High, DoD | Vedere [Convalida FIPS 140-2](/windows/security/threat-protection/fips-140-validation) |

### <a name="frequently-asked-questions"></a>Domande frequenti

**Qual è la differenza tra 'FIPS 140 Validated' e 'FIPS 140 compliant'?**

"FIPS 140 Validated" significa che il modulo di crittografia o un prodotto che incorpora il modulo è stato convalidato ('certificato') dal CMVP come soddisfare i requisiti FIPS 140-2. "FiPS 140 compliant" è un termine di settore per i prodotti IT che si basano su prodotti convalidati FIPS 140 per la funzionalità di crittografia.

**Quando Microsoft esegue una convalida FIPS 140?**

La cadenza per l'avvio di una convalida del modulo è allineata agli aggiornamenti delle funzionalità di Windows 10 e Windows Server. Con l'evoluzione del settore software, i sistemi operativi vengono rilasciati con maggiore frequenza, con aggiornamenti software mensili. Microsoft avvia la convalida per i rilasci di funzionalità, ma tra una versione e l'altra cerca di ridurre al minimo le modifiche apportate ai moduli crittografici.

**Quali computer sono inclusi in una convalida FIPS 140?**

Microsoft convalida i moduli di crittografia in un campione rappresentativo di configurazioni hardware che eseguono Windows 10 e Windows Server. È pratica comune accettare questa convalida FIPS 140-2 quando un ambiente utilizza hardware, simile agli esempi utilizzati per il processo di convalida.

**Nel sito Web NIST sono elencati molti moduli. Come posso sapere quale si applica alla mia agenzia?**

Se è necessario utilizzare moduli di crittografia convalidati tramite FIPS 140-2, è necessario verificare che la versione utilizzata sia visualizzata nell'elenco di convalida. CMVP e Microsoft gestiscono un elenco di moduli crittografici convalidati, organizzati in base al rilascio del prodotto, insieme alle istruzioni per identificare i moduli installati in un Windows sistema. Per ulteriori informazioni sulla configurazione di sistemi conformi, vedere il contenuto Windows e [Windows Server FIPS 140-2](https://aka.ms/AA6ehud).

**Cosa significa "Se gestito in modalità FIPS" in un certificato?**

Questo avviso informa il lettore che è necessario seguire le regole di configurazione e sicurezza necessarie per utilizzare il modulo di crittografia in modo coerente con i criteri di sicurezza FIPS 140-2. Ogni modulo ha un proprio criterio di sicurezza, ovvero una specifica precisa delle regole di sicurezza in base alle quali verrà utilizzato, e utilizza algoritmi di crittografia approvati, la gestione delle chiavi crittografiche e le tecniche di autenticazione. Le regole di sicurezza sono definite nei criteri di sicurezza per ogni modulo. Per ulteriori informazioni, inclusi i collegamenti ai criteri di sicurezza per ogni modulo convalidato tramite CMVP, vedere il contenuto [di Windows e Windows Server FIPS 140-2.](https://aka.ms/AA6ehud)

**FedRAMP richiede la convalida FIPS 140-2?**

Sì, il Federal Risk and Authorization Management Program (FedRAMP) si basa sulle linee di base di controllo definite dal [NIST SP 800-53 Revisione 4,](https://nvd.nist.gov/800-53/Rev4/)inclusa la protezione crittografica [SC-13](https://nvd.nist.gov/800-53/Rev4/control/SC-13) che impone l'uso della crittografia convalidata da FIPS o della crittografia approvata dall'NSA.

**Posso usare l'adesione di Microsoft a FIPS 140-2 nel processo di certificazione della mia agenzia?**

Per essere conforme a FIPS 140-2, il sistema deve essere configurato per l'esecuzione in una modalità di funzionamento approvata da FIPS, che include la garanzia che un modulo crittografico utilizzi solo algoritmi approvati da FIPS. Per ulteriori informazioni sulla configurazione di sistemi conformi, vedere il contenuto Windows e [Windows Server FIPS 140-2](https://aka.ms/AA6ehud).

**Qual è la relazione tra FIPS 140-2 e Criteri comuni?**

Si tratta di due standard di sicurezza separati con scopi diversi, ma complementari. FIPS 140-2 è progettato specificamente per la convalida dei moduli crittografici software e hardware, mentre Common Criteria è progettato per valutare le funzioni di sicurezza nei prodotti hardware e software IT. Le valutazioni dei criteri comuni spesso si basano sulle convalide FIPS 140-2 per garantire che la funzionalità di crittografia di base sia implementata correttamente.

### <a name="resources"></a>Risorse

- [Requisiti di sicurezza FIPS Pub 140-2 per i moduli crittografici](https://csrc.nist.gov/publications/fips/fips140-2/fips1402.pdf)
- [Programma di convalida del modulo di crittografia NIST](https://csrc.nist.gov/groups/STM/cmvp/index.html)
- [Windows, Windows Server e FIPS 140-2](/windows/security/threat-protection/fips-140-validation)
- [Conformità in Microsoft Trust Center](https://www.microsoft.com/trust-center/compliance/compliance-overview)
