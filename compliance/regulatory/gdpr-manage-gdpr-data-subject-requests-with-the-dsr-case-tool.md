---
title: Gestire le richieste dell'oggetto dei dati GDPR con lo strumento del caso DSR nel Centro sicurezza & conformità
description: Scopri come gestire le richieste degli utenti del Regolamento generale sulla protezione dei dati (GDPR) dell'UE con lo strumento del caso DSR.
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- SPO_Content
- MS-Compliance
ms.assetid: ce9eb942-3589-42cb-88fd-1576ecb09c5c
ms.custom: seo-marvel-apr2020
hideEdit: true
ms.openlocfilehash: f89faf915e31e375674020fda1fe56fe7cd78410
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/01/2021
ms.locfileid: "51496064"
---
# <a name="manage-gdpr-data-subject-requests-with-the-dsr-case-tool-in-the-security--compliance-center"></a>Gestire le richieste dell'oggetto dei dati GDPR con lo strumento del caso DSR nel Centro sicurezza & conformità

Il regolamento generale sulla protezione dei dati (GDPR) dell'UE riguarda la protezione e l'abilitazione dei diritti di privacy degli utenti all'interno dell'Unione Europea (UE). Il GDPR concede ai singoli utenti dell'Unione Europea (noti come soggetti dei dati) il diritto di accedere, recuperare, correggere, cancellare e limitare il trattamento dei propri dati personali. Ai sensi del GDPR, i dati personali significano qualsiasi informazione relativa a una persona naturale identificata o identificabile. Una richiesta formale da parte di una persona all'organizzazione di intraprendere un'azione sui propri dati personali è chiamata richiesta dell'oggetto dei dati o DSR. Per informazioni dettagliate sulla risposta alle richieste DSR per i dati in Office 365, vedere Guida alla richiesta dell'oggetto [dati di Office 365.](https://go.microsoft.com/fwlink/?linkid=871169 )
  
Per gestire le indagini in risposta a una richiesta DSR inviata da una persona dell'organizzazione, è possibile utilizzare lo strumento caso DSR nel Centro sicurezza & conformità per trovare il contenuto archiviato in:
  
- Qualsiasi cassetta postale utente nell'organizzazione. Sono incluse le conversazioni di Skype for Business e le chat uno-a-uno in Microsoft Teams
    
- Tutte le cassette postali associate a un gruppo di Microsoft 365 e tutte le cassette postali del team in Microsoft Teams
    
- Tutti i siti di SharePoint Online e gli account di OneDrive for Business nell'organizzazione
    
- Tutti i siti di Teams e i siti del gruppo di Microsoft 365 nell'organizzazione
    
- Tutte le cartelle pubbliche in Exchange Online
    
Usando lo strumento del caso DSR puoi:
  
- Creare un caso distinto per ogni indagine DSR.
    
- Controllare chi ha accesso al caso DSR aggiungendo persone come membri del caso; solo i membri possono accedere al caso e possono visualizzare i relativi casi solo nell'elenco dei casi nella pagina **Casi DSR** nel Centro sicurezza & conformità. È inoltre possibile assegnare autorizzazioni diverse a membri diversi dello stesso caso. Ad esempio, è possibile consentire ad alcuni membri di visualizzare solo il caso e i risultati della ricerca e consentire ad altri membri di creare ricerche ed esportare i risultati della ricerca. 
    
- Usa la ricerca incorporata per cercare tutto il contenuto creato o caricato da uno specifico soggetto di dati.
    
- Facoltativamente, rivedere la query di ricerca incorporata ed eseguire di nuovo la ricerca per restringere i risultati della ricerca.
    
- Aggiungere altre ricerche di contenuto associate al caso DSR. Ciò include la creazione di ricerche che restituiscono elementi parzialmente indicizzati e log generati dal sistema dal servizio di roaming di Office.
    
- Esportare i dati in risposta a una richiesta di accesso o esportazione DSR.
    
- Eliminare i casi in cui il processo di indagine DSR è completato. In questo modo vengono rimosse tutte le ricerche e i processi di esportazione associati al caso.
    
Ecco il processo di alto livello per l'utilizzo dello strumento caso DSR per gestire le indagini DSR:
  
[Step 1: Assign eDiscovery permissions to potential case members](#step-1-assign-ediscovery-permissions-to-potential-case-members)

[Passaggio 2: Creare un caso DSR e aggiungere membri](#step-2-create-a-dsr-case-and-add-members)

[Passaggio 3: Eseguire la query di ricerca](#step-3-run-the-search-query)

[Passaggio 4: Esportare i dati](#step-4-export-the-data)

[(Facoltativo) Passaggio 5: Rivedere la query di ricerca incorporata](#optional-step-5-revise-the-built-in-search-query)

[Ulteriori informazioni sull'uso dello strumento del caso DSR](#more-information-about-using-the-dsr-case-tool)
  
> [!IMPORTANT]
> I nostri strumenti consentono agli amministratori di eseguire richieste di accesso o esportazione DSR consentendo loro di utilizzare la funzionalità di ricerca ed esportazione incorporata disponibile nello strumento del caso DSR. Lo strumento consente di facilitare un metodo ottimale per esportare i dati rilevanti per una richiesta DSR inviata da un soggetto dei dati. Tuttavia, è importante notare che i risultati della ricerca possono variare in base all'oggetto dei dati o alle azioni dell'amministratore intraprese che possono influire sul fatto che un elemento venga o meno considerato come "dati personali" ai fini dell'esportazione. Ad esempio, se l'oggetto dati è stato l'ultima persona a modificare un file che non ha creato, è possibile che il file non venga restituito nei risultati della ricerca. Analogamente, un amministratore potrebbe esportare i dati senza includere elementi parzialmente indicizzati o tutte le versioni dei documenti di SharePoint. Di conseguenza, gli strumenti forniti possono facilitare l'accesso e l'esportazione delle richieste di dati; Tuttavia, i risultati sono soggetti a specifici scenari di utilizzo dell'amministratore e dell'oggetto dei dati. 
  
## <a name="step-1-assign-ediscovery-permissions-to-potential-case-members"></a>Passaggio 1: Assegnare autorizzazioni di eDiscovery a potenziali membri del caso

Per impostazione predefinita, un amministratore globale può accedere al caso DSR nel Centro sicurezza & conformità. Per impostazione predefinita, altri utenti, ad esempio un responsabile della privacy dei dati, un responsabile delle risorse umane o altre persone coinvolte nelle indagini DSR, non hanno accesso al case tool DSR e doranno disporre delle autorizzazioni appropriate per accedere a tale strumento. Il modo più semplice per eseguire  questa operazione è passare alla pagina Autorizzazioni nel Centro sicurezza & conformità e aggiungere utenti al gruppo di ruoli Manager eDiscovery. È inoltre necessario assegnare queste autorizzazioni in modo da poterle aggiungere come membri del caso DSR creato nel passaggio 2. 
  
Per istruzioni dettagliate, vedere [Assign eDiscovery permissions in the Office 365 Security & Compliance Center.](/microsoft-365/compliance/assign-ediscovery-permissions)
  
> [!NOTE]
> Per impostazione predefinita, un amministratore globale (o altri membri del gruppo di ruoli Gestione organizzazione nel Centro sicurezza & conformità non dispone delle autorizzazioni necessarie per esportare i risultati della ricerca di contenuto (vedere il passaggio 4 in questo articolo). Per risolvere questo problema, un amministratore può aggiungersi come membro del gruppo di ruoli Manager eDiscovery. 
  
## <a name="step-2-create-a-dsr-case-and-add-members"></a>Passaggio 2: Creare un caso DSR e aggiungere membri

Il passaggio successivo consiste nel creare un caso DSR. Quando si crea un caso, è possibile scegliere di avviare la ricerca incorporata oppure creare il caso senza avviare la ricerca. La procedura seguente indica di creare il caso senza avviare la ricerca e quindi di illustrare come aggiungere membri al caso.
  
1. Vai a [https://protection.office.com](https://protection.office.com) e accedi usando il tuo account aziendale o dell'istituto di istruzione. 
    
2. Nel Centro sicurezza & conformità fare clic su **Privacy** dati Richieste dell'oggetto e quindi fare clic su Aggiungi \> icona Nuovo ![ caso ](../media/ITPro-EAC-AddIcon.gif) **DSR.**
    
3. Nella pagina riquadro a comparsa Nuovo **caso DSR** assegnare un nome al caso, digitare una descrizione facoltativa e quindi fare clic su **Avanti.** Il nome del caso deve essere univoco nell'organizzazione.
    
    > [!TIP]
    > Prendi in considerazione l'aggiunta del nome della persona che ha inviato la richiesta DSR su cui stai indagando nel nome e/o nella descrizione del nuovo caso. Si noti che solo i membri di questo caso (e gli amministratori di eDiscovery) potranno visualizzare il caso nell'elenco dei casi nella **pagina Richieste dell'oggetto dei** dati. 
  
4. Nella pagina **Dettagli richiesta,** in Oggetto dati (la persona che ha richiesto **la richiesta)** selezionare la persona per cui si desidera trovare ed esportare i dati e quindi fare clic su **Avanti.**
    
5. Nella pagina **Conferma le impostazioni del caso** è possibile modificare il nome e la descrizione del caso e selezionare un oggetto dati diverso. In caso contrario, fare clic **su Salva.**
    
    Viene visualizzata una pagina che conferma la creazione del nuovo caso DSR.
    
    ![Avviare la ricerca o chiudere la pagina Nuovo caso DSR](../media/b5e62c2c-cafe-4a8d-a38c-789ed9f9ccbd.png)
  
    A questo punto, è possibile eseguire una delle due operazioni seguenti:
    
    a. Facendo **clic su Mostra risultati di ricerca** viene avviata la ricerca. Questa è la selezione predefinita. La ricerca incorporata che viene eseguita quando si seleziona questa opzione e i risultati restituiti vengono illustrati nel passaggio 3.
    
    b. Se **si fa** clic su Fine, il nuovo caso DSR verrà chiuso senza avviare la ricerca incorporata. Quando si seleziona questa opzione, il nuovo caso DSR viene visualizzato nella **pagina Richieste dell'oggetto** dei dati.
    
6. Fare **clic** su Fine per passare al nuovo caso DSR e aggiungervi membri. 
    
7. Nella pagina **Richieste dell'oggetto** dati fare clic sul nome del caso DSR creato. 
    
8. Nella pagina **a comparsa Gestisci questo caso,** in Gestisci **membri,** fare clic su **Aggiungi.** 
    
    In **Utenti** viene visualizzato un elenco di persone a cui sono assegnate le autorizzazioni di eDiscovery appropriate. Le persone a cui sono state assegnate le autorizzazioni di eDiscovery nel passaggio 1 verranno visualizzate in questo elenco. 
    
9. Selezionare le persone da aggiungere come membri del caso DSR, fare clic **su Aggiungi** e quindi salvare le modifiche.
    
    È inoltre possibile aggiungere gruppi di ruoli come membri del caso DSR facendo clic **su Aggiungi** in Gestisci gruppi **di ruoli.** 
    
## <a name="step-3-run-the-search-query"></a>Passaggio 3: Eseguire la query di ricerca

Dopo aver creato un caso DSR e aver aggiunto membri, il passaggio successivo consiste nell'eseguire la ricerca incorporata associata al caso. Questa query di ricerca predefinita esegue le operazioni seguenti:
  
- Cerca in tutte le cassette postali dell'organizzazione tutti gli elementi di posta elettronica inviati o ricevuti dall'oggetto dati. Questa operazione viene eseguita utilizzando la proprietà di posta elettronica  *Partecipanti,*  che consente di cercare l'oggetto dati in tutti i campi degli utenti in un messaggio di posta elettronica. Questa proprietà restituisce gli elementi in cui l'oggetto dati si trova nei **campi From,** **To,** **CC** e **BCC.** Le cartelle pubbliche in Exchange Online vengono inoltre cercate per i messaggi inviati o ricevuti dall'oggetto dati. 
    
- Cerca documenti ed elementi creati o caricati dall'oggetto dati in tutti i siti dell'organizzazione. Questa operazione viene eseguita utilizzando le proprietà del sito seguenti:
    
  - La  *proprietà Author*  restituisce gli elementi in cui l'oggetto dati è elencato nel campo author nei documenti di Office. Questo valore persiste, anche se il documento viene copiato e caricato da un altro utente. 
    
  - La  *proprietà CreatedBy*  restituisce gli elementi creati o caricati dall'oggetto dati. 
    
Ecco l'aspetto della query con parole chiave per la ricerca incorporata che viene creata automaticamente quando si crea un caso DSR.
  
```powershell
participants:"<email address>" OR author:"<display name>" OR createdby:"<display name>"
```

Ad esempio, se il nome dell'oggetto dati è Ina Leonte, la query con parole chiave sarà simile alla seguente:
  
```powershell
participants:"ina@contoso.com" OR author:"Ina Leonte" OR createdby:"Ina Leonte"
```

 **Per eseguire la ricerca incorporata per un caso DSR:**
  
1. Nel Centro sicurezza & conformità  fare clic su Privacy dei dati Richieste dell'oggetto e quindi fare clic su Apri accanto al caso \> DSR creato nel passaggio 2.  
    
    Fare **clic sulla** scheda Cerca nella parte superiore della pagina e quindi fare clic sulla casella di controllo accanto alla ricerca incorporata creata al momento della creazione del caso DSR. La ricerca ha lo stesso nome del caso DSR. 
    
2. Nella pagina del riquadro a comparsa di ricerca fare clic **su Apri query.**
    
    Quando si apre la query, la ricerca viene avviata e verrà completata in pochi istanti. 
    
3. Al termine della ricerca, fare clic su **Anteprima risultati** per visualizzare un'anteprima dei risultati della ricerca. Per ulteriori informazioni, vedere [Anteprima dei risultati della ricerca.](/microsoft-365/compliance/content-search#preview-search-results)
    
    > [!TIP]
    > È inoltre possibile visualizzare le statistiche delle query di ricerca per visualizzare il numero di elementi della cassetta postale e del sito restituiti dalla ricerca e le posizioni di contenuto principali che contengono elementi che corrispondono alla query di ricerca. Per ulteriori informazioni, vedere [Visualizzare informazioni e statistiche su una ricerca.](/microsoft-365/compliance/content-search#view-information-and-statistics-about-a-search) 
  
È possibile modificare la query di ricerca predefinita, modificare i percorsi di contenuto in cui viene eseguita la ricerca ed eseguire di nuovo la ricerca. Per ulteriori informazioni, vedere passaggio [5.](#optional-step-5-revise-the-built-in-search-query) 
  
## <a name="step-4-export-the-data"></a>Passaggio 4: Esportare i dati

Dopo aver eseguito la ricerca predefinita, è possibile esportare i risultati della ricerca. In alternativa, prima di esportare i dati, è possibile modificare la query per ridurre il numero di risultati della ricerca. Per ulteriori informazioni sulla restringezione dei risultati della ricerca, vedere Passaggio 5.
  
Quando si esportano i risultati della ricerca, gli elementi delle cassette postali possono essere scaricati in file PST o come singoli messaggi. Quando si esporta contenuto da account di SharePoint e OneDrive, vengono esportate copie dei documenti nativi di Office e di altri documenti. I risultati della ricerca includono un file dei risultati contenente informazioni su ogni elemento esportato. Per informazioni più dettagliate sull'esportazione, vedere [Export Content Search results](/microsoft-365/compliance/export-search-results).
  
> [!NOTE]
> Per impostazione predefinita, un amministratore globale (o altri membri del gruppo di ruoli Gestione organizzazione nel Centro sicurezza & conformità) non dispone delle autorizzazioni necessarie per esportare i risultati della ricerca contenuto. Per risolvere questo problema, un amministratore può aggiungersi come membro del gruppo di ruoli Manager eDiscovery. 
  
Il computer utilizzato per esportare i dati deve soddisfare i requisiti di sistema seguenti:
  
- Versioni a 32 bit o a 64 bit di Windows 7 e versioni successive
    
- Microsoft .NET Framework 4.7
    
- Browser supportato:
    
  - Microsoft Edge
    
    Oppure
    
  - Microsoft Internet Explorer 10 e versioni successive
    
    > [!NOTE]
    > Microsoft non produce estensioni o componenti aggiuntivi di terze parti per ClickOnce applicazioni. L'esportazione di dati con un browser non supportato con estensioni o componenti aggiuntivi di terze parti non è supportata. 
  
 **Per esportare i dati dalla ricerca incorporata in un caso DSR:**
  
1. Nel Centro sicurezza & conformità fare  clic su Privacy dei dati Richieste degli utenti e quindi su Apri accanto al caso DSR da cui si desidera esportare \> i dati.  
    
2. Fare **clic sulla** scheda Cerca nella parte superiore della pagina e quindi fare clic sulla casella di controllo accanto alla ricerca incorporata creata al momento della creazione del caso DSR. Oppure fare clic su un'altra ricerca per esportare i dati da tale ricerca. 
    
3. Nella pagina del riquadro a comparsa di ricerca fare clic su Esporta risultati di ricerca Icona Altro e quindi ![ ](../media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) selezionare Esporta **risultati** nell'elenco a discesa. 
    
4. Nella pagina **Esporta risultati** selezionare le opzioni consigliate seguenti per le richieste di esportazione DSR. 
    
    ![Configurare le impostazioni di esportazione](../media/25416b79-57da-46a1-ae07-e640602a8fa4.png)
  
    a. In **Opzioni** di output selezionare la prima opzione ( Tutti gli elementi, esclusi quelli con un formato non **riconosciuto,** crittografati o non indicizzati per altri motivi) per esportare solo gli elementi indicizzati. Il motivo per cui non si desidera esportare elementi parzialmente indicizzati dalla ricerca incorporata è che verranno esportati anche elementi parzialmente indicizzati da altri utenti. Per esportare solo gli elementi parzialmente indicizzati per l'oggetto dati, è consigliabile creare una ricerca separata. Per ulteriori informazioni, vedere [Esportazione di elementi parzialmente indicizzati](#exporting-partially-indexed-items) nella sezione "Ulteriori informazioni sull'utilizzo dello strumento caso DSR".
    
    b. In **Esporta contenuto di Exchange come** selezionare la terza opzione, Un file PST contenente tutti i messaggi in una singola **cartella.** Poiché alcuni dei risultati possono essere per gli elementi che hanno origine nella cassetta postale di un altro utente, questa opzione elenca solo l'elemento in una singola cartella senza indicare la cassetta postale effettiva ed è l'opzione migliore da utilizzare quando si de-duplica i risultati come consigliato nell'elemento successivo. Questa opzione consente inoltre all'oggetto dati di esaminare gli elementi in ordine cronologico (gli elementi vengono ordinati in base alla data di invio) senza dover esplorare la struttura di cartelle della cassetta postale originale per ogni elemento.
    
    c. Selezionare **l'opzione Abilita deduplicazione** per escludere i messaggi di posta elettronica duplicati. È consigliabile utilizzare questa opzione perché la ricerca incorporata esegue la ricerca in tutte le cassette postali dell'organizzazione. Pertanto, se nelle cassette postali in cui è stata ricercata vengono trovate più copie dello stesso messaggio, questa opzione significa che verrà esportata una sola copia di un messaggio. Questa opzione, insieme, consente di esportare i messaggi in un file PST in una singola cartella e di ottenere la migliore esperienza utente per le richieste di esportazione DSR. Il Results.csv di esportazione elenca tutti i percorsi in cui sono stati trovati messaggi duplicati.
    
    Facoltativamente, è possibile selezionare **l'opzione** Includi versioni per i documenti di SharePoint per esportare tutte le versioni dei documenti di SharePoint e OneDrive. A tale scopo, è necessario che il controllo delle versioni sia attivato per le raccolte documenti. Questa opzione consente di garantire che tutti i dati pertinenti siano esportati.
    
5. Dopo aver scelto le impostazioni di esportazione, fare clic su **Esporta.**
    
    I risultati della ricerca sono preparati per il download, ovvero vengono caricati nell'area di archiviazione di Azure per l'organizzazione nel cloud Microsoft. I passaggi successivi illustrano come scaricare questi dati nel computer locale.
    
6. Fare clic **sulla scheda** Esporta per visualizzare il processo di esportazione creato. I processi di esportazione hanno lo stesso nome della ricerca corrispondente **con _Export** alla fine del nome di ricerca. 
    
7. Fare clic sul processo di esportazione appena creato per visualizzare la pagina del riquadro a comparsa di esportazione. Questa pagina mostra informazioni sulla ricerca, ad esempio le dimensioni e il numero totale di elementi da esportare e la percentuale di elementi trasferiti in un'area di archiviazione di Azure. Fare **clic su Aggiorna** per aggiornare le informazioni sullo stato del caricamento. 
    
8. In **Chiave di esportazione**, fare clic su **Copia negli Appunti**. Questa chiave viene utilizzata nel passaggio 11 per scaricare i risultati della ricerca.
    
9. Fare clic su Esporta risultati di ricerca Icona Scarica i risultati nella parte superiore della pagina del ![ riquadro a comparsa di ](../media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png)  esportazione. 
    
10. Nella finestra popup nella parte inferiore della pagina fare clic su **Apri** per aprire lo strumento **di esportazione di eDiscovery.** Lo **strumento di esportazione di eDiscovery** verrà installato la prima volta che si scaricano i risultati della ricerca. 
    
11. Nello strumento **di esportazione di eDiscovery** incollare la chiave di esportazione copiata nel passaggio 8 nella casella appropriata.
    
12. Fare clic su **Sfoglia** per specificare il percorso in cui si desidera scaricare i file dei risultati della ricerca. 
    
    > [!NOTE]
    > A causa dell'elevata attività del disco (lettura e scrittura), è consigliabile scaricare i risultati della ricerca in un'unità disco locale. non scaricarli in un'unità di rete mappata o in un altro percorso di rete. 
  
13. Fare clic su **Avvia** per scaricare i risultati della ricerca nel computer. 
    
    Lo **Strumento di esportazione eDiscovery** consente di visualizzare informazioni sullo stato delle informazioni relative al processo di esportazione, incluso il numero stimato (e le dimensioni) degli elementi rimanenti da scaricare. Al termine del processo di esportazione, è possibile accedere ai file nel percorso in cui sono stati scaricati. Per ulteriori informazioni sui report inclusi quando si scaricano i risultati di Ricerca contenuto, vedere la sezione Ulteriori informazioni in "Esportare i risultati di Ricerca contenuto". [](/microsoft-365/compliance/export-search-results#more-information) 
    
Dopo l'esportazione dei dati, i risultati della ricerca e i report di esportazione si trovano in una cartella con lo stesso nome del caso DSR. I file PST che contengono elementi delle cassette postali si trovano in una sottocartella denominata **Exchange.** I documenti e altri elementi dei siti si trovano in una sottocartella denominata **SharePoint.** 
  
## <a name="optional-step-5-revise-the-built-in-search-query"></a>(Facoltativo) Passaggio 5: Rivedere la query di ricerca incorporata

Dopo aver eseguito la ricerca incorporata, è possibile rivedirla per restringere l'ambito per restituire un numero minore di risultati della ricerca. A tale scopo, è possibile aggiungere condizioni alla query. Una condizione è collegata logicamente alla query con parole chiave tramite l'operatore **AND.** Ciò significa che devono essere restituiti nei risultati della ricerca, gli elementi devono soddisfare sia la query con parole chiave che qualsiasi condizione aggiunta. Questo è il modo in cui le condizioni consentono di restringere i risultati. Se si aggiungono due o più condizioni univoche a una query di ricerca (condizioni che specificano proprietà diverse), tali condizioni vengono connesse logicamente dall'operatore **AND.** Ciò significa che vengono restituiti solo gli elementi che soddisfano tutte le condizioni ,oltre alla query con parole chiave. Se si aggiungono più valori (separati da virgole o punti e virgola) a una singola condizione, tali valori vengono connessi tramite l'operatore **OR.** Ciò significa che gli elementi vengono restituiti se contengono uno dei valori specificati per la proprietà nella condizione. 
  
Ecco alcuni esempi delle condizioni che è possibile aggiungere alla query di ricerca incorporata di un caso DSR. Il nome della proprietà effettiva utilizzata in una query di ricerca viene visualizzato tra parentesi.
  
- **Tipo di file ( `filetype` )** - Specifica l'estensione di un documento o di un file. Utilizzare questa condizione per cercare documenti e file creati da applicazioni di Office specifiche, ad esempio Word, Excel e OneNote. 
    
- **Tipo di messaggio ( `kind` )** - Specifica il tipo di elemento di posta elettronica da cercare. Ad esempio, è possibile utilizzare la sintassi per restituire solo messaggi di posta elettronica e conversazioni skype for business o  `kind:email OR kind:im` chat uno-a-uno in Microsoft Teams. 
    
- **Tag di conformità ( `compliancetag` )** - Specifica un'etichetta assegnata a un messaggio di posta elettronica o a un documento. Questa condizione restituisce gli elementi classificati con un'etichetta specifica. Le etichette vengono utilizzate per classificare la posta elettronica e i documenti per la governance dei dati e per applicare regole di conservazione in base alla classificazione definita dall'etichetta. Si tratta di una condizione utile per le indagini DSR perché l'organizzazione potrebbe usare etichette per classificare il contenuto relativo alla privacy dei dati o che contiene dati personali o informazioni riservate. Per il valore di questa condizione, utilizzare il nome completo dell'etichetta o la prima parte del nome dell'etichetta con un carattere jolly. Per ulteriori informazioni, vedere [Informazioni sui criteri di conservazione e sulle etichette di conservazione in Office 365.](/microsoft-365/compliance/retention)
    
Per un elenco e una descrizione di tutte le [](/microsoft-365/compliance/keyword-queries-and-search-conditions#search-conditions) condizioni disponibili nello strumento caso DSR, vedere Condizioni di ricerca nell'articolo "Query con parole chiave e condizioni di ricerca per ricerca contenuto". 
  
### <a name="changing-the-content-locations-that-are-searched"></a>Modifica dei percorsi di contenuto in cui viene ricercata

Oltre a rivedere la ricerca incorporata per un caso DSR, è anche possibile modificare i percorsi di contenuto in cui viene ricercata. Come spiegato in precedenza, la ricerca incorporata esegue la ricerca in ogni cassetta postale e sito dell'organizzazione e in tutte le cartelle pubbliche di Exchange Online. Ad esempio, è possibile restringere la ricerca per cercare solo la cassetta postale dell'oggetto dati e l'account di OneDrive e i siti di SharePoint selezionati. Se si sceglie di eseguire ricerche in siti specifici, è necessario aggiungere ogni sito in cui si desidera eseguire la ricerca.
  
Per modificare i percorsi di contenuto in cui eseguire la ricerca:
  
1. Aprire la ricerca incorporata per la quale si desidera modificare i percorsi del contenuto.
    
2. Nella query di ricerca, in **Percorsi,** fare clic **su Modifica** accanto all'opzione **Percorsi** specifici. 
    
    ![Fare clic su Modifica per modificare i percorsi del contenuto della query di ricerca incorporata](../media/d66f7ba7-b71f-4ff5-a030-460ff02e3123.png)
  
    Viene **visualizzata la** pagina a comparsa Modifica posizioni. Ecco una descrizione dei percorsi del contenuto nella ricerca incorporata e alcune informazioni sulla modifica delle posizioni in cui viene ricercata. 
    
    ![Pagina a comparsa Modifica posizioni](../media/56c033f6-6735-46ba-abb2-a263a2b79836.png)
  
    a. **L'interruttore** nella sezione Seleziona tutto nella cassetta postale nella parte superiore della pagina a comparsa è selezionato, che indica che vengono cercate tutte le cassette postali. Per restringere l'ambito della ricerca, fare clic sull'interruttore per deselezionarlo, quindi fare clic su **Scegli utenti,** gruppi o team e selezionare cassette postali specifiche in cui eseguire la ricerca.
    
    b. L'interruttore in **Seleziona** tutto nella sezione siti al centro della pagina a comparsa è selezionato, che indica che viene ricercata in tutti i siti. Per restringere la ricerca ai siti selezionati, è necessario deselezionare l'interruttore e quindi fare clic **su Scegli siti.** È necessario aggiungere ogni sito specifico in cui si desidera eseguire la ricerca, incluso l'account OneDrive dell'oggetto dati.
    
    c. L'interruttore nella sezione Cartelle pubbliche di Exchange è selezionato, il che significa che vengono cercate tutte le cartelle pubbliche di Exchange. È possibile eseguire ricerche solo in tutte le cartelle pubbliche di Exchange o in nessuna di esse. Non è possibile scegliere quelli specifici in cui eseguire la ricerca.
    
3. Se si modificano i percorsi del contenuto nella ricerca predefinita, fare clic su **Salva &amp; esecuzione** per riavviare la ricerca. 

> [!NOTE]
> Quando si esegue una ricerca in tutte le posizioni delle cassette postali o solo in cassette postali specifiche, i dati di altre applicazioni di Office 365 salvate nelle cassette postali degli utenti vengono inclusi quando si esportano i risultati della ricerca. I dati non vengono inclusi nei risultati della ricerca stimati e non vengono visualizzati in anteprima. Ma viene incluso quando si esportano e si scaricano i risultati della ricerca. Per ulteriori informazioni sulle applicazioni che archiviano i dati nella cassetta postale di un utente, vedere [Content stored in Exchange Online mailboxes](/microsoft-365/compliance/what-is-stored-in-exo-mailbox).
  
## <a name="more-information-about-using-the-dsr-case-tool"></a>Ulteriori informazioni sull'uso dello strumento del caso DSR

Le sezioni seguenti contengono ulteriori informazioni sull'utilizzo dello strumento caso DSR per rispondere alle richieste di esportazione DSR.
  
[Esportazione di dati dal servizio di roaming di Office](#exporting-data-from-the-office-roaming-service)

[Esportazione di elementi parzialmente indicizzati](#exporting-partially-indexed-items)

[Ricerca ed esportazione di dati da Microsoft Teams e gruppi di Microsoft 365](#searching-and-exporting-data-from-microsoft-teams-and-microsoft-365-groups)

[Ricerca nelle cartelle pubbliche di Exchange](#searching-exchange-public-folders)
  
### <a name="exporting-data-from-the-office-roaming-service"></a>Esportazione di dati dal servizio di roaming di Office

È possibile utilizzare lo strumento caso DSR per cercare ed esportare i dati di utilizzo generati dal servizio di roaming di Office. Roaming è un servizio che archivia le impostazioni correlate a Office, ad esempio il tema di Office, il dizionario personalizzato, le impostazioni della lingua, la modalità sviluppatore e la correzione automatica. 
    
I dati del servizio Di roaming di Office vengono archiviati nella cassetta postale di un soggetto dei dati in una cartella nascosta che si trova in un sottoalbero di messaggi non interpersonali (non IPM) delle cassette postali di Exchange Online. Ciò significa che i dati vengono nascosti dalla visualizzazione dell'utente quando utilizzano Outlook o altri client di posta per accedere alla propria cassetta postale. Per ulteriori informazioni sulle cartelle nascoste, vedere [Cartelle nascoste MAPI.](https://go.microsoft.com/fwlink/?linkid=872758)
  
È possibile creare una ricerca di contenuto separata (e associarla a un caso DSR) che restituisce i dati di utilizzo del servizio di roaming di Office nella cassetta postale dell'oggetto dati. Questi dati non sono inclusi nelle statistiche di ricerca e non saranno disponibili per l'anteprima. Tuttavia, puoi esportarlo e quindi darlo all'oggetto dei dati in risposta a una richiesta di esportazione DSR.
  
Quando si esportano dati dal servizio di roaming di Office, i dati vengono salvati in una cartella separata che si trova nella **cartella ApplicationDataRoot,** che si trova in una cartella con il nome con l'indirizzo di posta elettronica dell'oggetto dei dati. Questi dati vengono esportati come file JSON, ovvero file di testo leggibili dall'utente simili ai file XML o TXT, allegati ai messaggi di posta elettronica. Attualmente, questa cartella è denominata con l'identificatore univoco globale (GUID): **1caee58f-eb14-4a6b-9339-1fe2ddf6692b**. Nelle versioni future dello strumento per la distinzione tra maiuscole e minuscole DSR, il GUID verrà sostituito con il nome dell'applicazione effettiva. 

   
 **Per cercare ed esportare i dati del servizio roaming di Office:**
  
1. Nel Centro sicurezza & conformità  fare clic su Privacy dei dati Richieste degli utenti e quindi su Apri accanto al caso DSR per l'oggetto dati per cui si desidera esportare i dati \> di utilizzo.  
    
2. Fare clic **sulla scheda** Cerca nella parte superiore della pagina e quindi fare clic su Aggiungi icona ![ Ricerca ](../media/ITPro-EAC-AddIcon.gif) **guidata.**
    
3. Fare **clic su** Annulla nella pagina **Assegnare un nome alla** ricerca. 
    
4. In **Query di ricerca** selezionare la casella **di** controllo accanto a Servizio roaming di Office nella condizione **Tipo.** 
    
    ![Selezionare la casella di controllo Servizio roaming di Office per esportare i dati di utilizzo](../media/O365_DSRCase_SDSDataExport1.png)
  
    La **condizione Type** ( che sono classi di messaggi di posta elettronica) deve essere l'unico elemento nella query di ricerca. È possibile eliminare la **casella Parole** chiave o lasciarla vuota. 
    
5. In **Percorsi** verificare che l'opzione **Percorsi specifici** sia selezionata e quindi fare clic su **Modifica.**
    
6. Nella parte superiore della pagina a comparsa **Modifica posizioni** (sezione cassetta postale), fare clic su **Scegli utenti, gruppi o team.**
    
7. Nella pagina **Modifica posizioni** fare clic su Scegli utenti, gruppi **o team,** scegliere la cassetta postale dell'oggetto dati e quindi salvare la selezione. 
    
8. Fare **clic su & e** quindi assegnare un nome alla ricerca e salvarla.
    
    Viene avviata la ricerca.
    
 **Per esportare i dati del servizio roaming di Office:**
  
1. Al termine della ricerca creata nel passaggio precedente, fare clic sulla scheda Cerca nella parte superiore della pagina e quindi fare clic sulla casella di controllo accanto alla ricerca.  Potrebbe essere necessario fare clic ![ su ](../media/165fb3ad-38a8-4dd9-9e76-296aefd96334.png) **Aggiorna** aggiorna per visualizzare la ricerca. 
    
2. Nella pagina del riquadro a comparsa di ricerca fare clic su Esporta risultati di ricerca Icona Altro e quindi ![ ](../media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) selezionare Esporta **risultati** nell'elenco a discesa. 
    
3. Nella pagina **Esporta risultati** selezionare le opzioni consigliate per esportare i dati di utilizzo. 
    
    ![Opzioni di esportazione durante l'esportazione dei dati di utilizzo del servizio roaming di Office](../media/470a7d1e-eeae-4b42-95aa-15cb82ce2f68.png)
  
    a. In **Opzioni** di output selezionare la prima opzione ( Tutti gli elementi, esclusi quelli con un formato non **riconosciuto,** crittografati o non indicizzati per altri motivi) per esportare solo gli elementi indicizzati.
    
    b. In **Esporta contenuto di Exchange come** selezionare la seconda opzione, Un file PST contenente tutti i **messaggi.**
    
    c. Lasciare deselezionate le opzioni di esportazione rimanenti.
    
4. Dopo aver scelto le impostazioni di esportazione, fare clic su **Esporta.**
    
    I risultati della ricerca sono preparati per il download, ovvero vengono caricati nell'area di archiviazione di Azure per l'organizzazione nel cloud Microsoft. I passaggi successivi illustrano come scaricare questi dati nel computer locale.
    
5. Fare clic **sulla scheda** Esporta per visualizzare il processo di esportazione creato. I processi di esportazione hanno lo stesso nome della ricerca corrispondente **con _Export** alla fine del nome di ricerca. 
    
6. Fare clic sul processo di esportazione appena creato per visualizzare la pagina del riquadro a comparsa di esportazione. 
    
7. In **Chiave di esportazione**, fare clic su **Copia negli Appunti**. Questa chiave viene utilizzata nel passaggio 10 per scaricare i risultati della ricerca.
    
8. Fare clic su Esporta risultati di ricerca Icona Scarica i risultati nella parte superiore della pagina del ![ riquadro a comparsa di ](../media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png)  esportazione. 
    
9. Nella finestra popup nella parte inferiore della pagina fare clic su **Apri** per aprire lo strumento **di esportazione di eDiscovery.** Lo **strumento di esportazione di eDiscovery** verrà installato la prima volta che si scaricano i risultati della ricerca. 
    
10. Nello **strumento di esportazione di eDiscovery** incollare nella casella appropriata la chiave di esportazione copiata nel passaggio 7.
    
11. Fare clic su **Sfoglia** per specificare il percorso in cui si desidera scaricare i file dei risultati della ricerca. 
    
    > [!NOTE]
    > A causa dell'elevata attività del disco (lettura e scrittura), è consigliabile scaricare i risultati della ricerca in un'unità disco locale. non scaricarli in un'unità di rete mappata o in un altro percorso di rete. 
  
12. Fare clic su **Avvia** per scaricare i risultati della ricerca nel computer. 
    
    Lo **Strumento di esportazione eDiscovery** consente di visualizzare informazioni sullo stato delle informazioni relative al processo di esportazione, incluso il numero stimato (e le dimensioni) degli elementi rimanenti da scaricare. Al termine del processo di esportazione, è possibile aprire il file PST di Exchange in Outlook e quindi passare alla **cartella ApplicationDataRoot** per accedere alla sottocartella per il servizio roaming. 
    
    Come spiegato in precedenza, i file JSON che contengono dati di utilizzo vengono allegati ai messaggi. Per visualizzare un file JSON, fare clic su un messaggio e quindi aprire il file JSON allegato. 
  
### <a name="exporting-partially-indexed-items"></a>Esportazione di elementi parzialmente indicizzati

È consigliabile non esportare elementi parzialmente indicizzati (denominati anche elementi non indicizzati) dalla ricerca incorporata creata quando si crea un caso DSR. Questo perché i risultati della ricerca includeranno probabilmente elementi parzialmente indicizzati per altri utenti dell'organizzazione e non solo elementi parzialmente indicizzati per l'oggetto dati). È consigliabile invece creare una ricerca contenuto separata associata al caso DSR progettata per esportare solo gli elementi parzialmente indicizzati correlati all'oggetto dati. 
  
Ecco un processo di alto livello per esportare elementi parzialmente indicizzati. Dopo l'esportazione, puoi esaminarli per determinare se un elemento risponde a una richiesta di accesso o esportazione DSR.
  
1. Aprire il caso DSR e creare una ricerca nella **pagina** Cerca. 
    
2. Utilizzare i criteri seguenti per configurare la query di ricerca e i percorsi di contenuto per la ricerca:
    
    - Utilizzare una query con parole chiave vuota o vuota. In questo modo vengono restituiti tutti gli elementi nei percorsi di contenuto in cui viene ricercata.
    
    - Cercare solo la cassetta postale di Exchange Online dell'oggetto dati e il relativo account OneDrive.
    
3. Dopo aver eseguito la ricerca e completata, è possibile esportare e scaricare i risultati della ricerca (come descritto [nel passaggio 4](#step-4-export-the-data)). Utilizzare le impostazioni seguenti per esportare elementi parzialmente indicizzati. 
    
    - In **Opzioni di** output selezionare la terza opzione ( Solo gli elementi con un formato non **riconosciuto,** crittografati o non indicizzati per altri motivi) per esportare solo elementi parzialmente indicizzati.
    
    - In **Esporta contenuto di Exchange come** è possibile selezionare qualsiasi opzione in base alle proprie preferenze. 
    
    - Se si seleziona l'opzione Includi versioni per **documenti di SharePoint,** le versioni dei documenti vengono esportate se una versione è parzialmente indicizzata. 
    
Per ulteriori informazioni sugli elementi parzialmente indicizzati, vedere: 
  
- [Partially indexed items in Content Search in Office 365](/microsoft-365/compliance/partially-indexed-items-in-content-search) (Elementi parzialmente indicizzati in Ricerca contenuto in Office 365)

- [Esportazione di elementi parzialmente indicizzati](/microsoft-365/compliance/export-search-results#exporting-partially-indexed-items)

### <a name="searching-and-exporting-data-from-microsoft-teams-and-microsoft-365-groups"></a>Ricerca ed esportazione di dati da Microsoft Teams e gruppi di Microsoft 365

Le conversazioni che fanno parte dell'elenco Chat in Microsoft Teams (denominate chat del team o chat uno-a-uno) vengono archiviate nella cassetta postale di Exchange Online degli utenti che partecipano alle chat. Inoltre, i file condivisi da una persona in una chat uno-a-uno vengono archiviati nell'account OneDrive della persona che condivide il file. Poiché la ricerca incorporata cerca tutte le cassette postali e gli account di OneDrive nell'organizzazione, le chat del team e i documenti condivisi in una sessione di chat (che l'oggetto dati ha creato o caricato) vengono restituiti dalla ricerca incorporata in un caso DSR.
  
In alternativa, le conversazioni che fanno parte di un canale di Teams (denominate anche messaggi di canale) vengono archiviate nella cassetta postale associata a un team. Anche questi tipi di conversazioni a cui ha partecipato l'oggetto dei dati vengono restituiti dalla ricerca incorporata, perché vengono cercate tutte le cassette postali associate a Teams. Inoltre, i file condivisi da un soggetto dei dati in un canale di Teams vengono archiviati nel sito di SharePoint del team. I file creati o caricati dall'oggetto dati vengono restituiti dalla ricerca incorporata in un caso DSR perché i siti associati a Teams sono inclusi nella ricerca.
  
Analogamente, anche le cassette postali e i siti di SharePoint che corrispondono a un gruppo di Microsoft 365 sono inclusi nella ricerca incorporata. Ciò significa che vengono restituiti i messaggi di posta elettronica inviati o ricevuti dall'oggetto dei dati e i file creati o caricati dall'oggetto dati. 
  
Per ulteriori informazioni sull'utilizzo di Ricerca contenuto per cercare elementi nei gruppi di Microsoft Teams e Microsoft 365 o per informazioni su come ottenere un elenco di membri, vedere la sezione "Ricerca di microsoft Teams e gruppi di Microsoft 365" [in Ricerca contenuto in Microsoft 365.](/microsoft-365/compliance/content-search#searching-microsoft-teams-and-microsoft-365-groups) 
  
### <a name="searching-exchange-public-folders"></a>Ricerca nelle cartelle pubbliche di Exchange

La ricerca incorporata in un caso DSR restituirà solo i messaggi di posta elettronica inviati dall'oggetto dati a una cartella pubblica abilitata alla posta o i messaggi inviati da un altro utente a una cartella pubblica e l'oggetto dati copiato. Non restituisce i messaggi che l'oggetto dati ha pubblicato in una cartella pubblica. Per cercare gli elementi che l'oggetto dati ha pubblicato in una cartella pubblica, è possibile creare una ricerca di contenuto separata che cerca qualsiasi elemento pubblicato in una cartella pubblica dall'oggetto dati.
  
Ecco un processo di alto livello per cercare gli elementi che l'oggetto dei dati ha pubblicato in una cartella pubblica. 
  
1. Aprire il caso DSR e creare una ricerca nella **pagina** Cerca. 
    
2. Utilizzare i criteri seguenti per configurare la query di ricerca e i percorsi di contenuto per la ricerca:
    
  - Nella casella **Parole** chiave utilizzare la query di ricerca seguente: 
    
    ```powershell
    itemclass:ipm.post AND "<email address of the data subject>"
    ```

  - Cerca in tutte le cartelle pubbliche di Exchange
    
  - Dopo aver eseguito la ricerca e completata, è possibile esportare e scaricare i risultati della ricerca (come descritto [nel passaggio 4](#step-4-export-the-data)). Utilizzare le impostazioni seguenti per esportare elementi parzialmente indicizzati. 
