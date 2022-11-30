---
lastModified: 2018-06-28T00:00:00Z
title: Linee guida sullo stile di authoring per i collaboratori esterni
description: Scopri le linee guida per l’authoring e l’editoriale per i collaboratori esterni a titolo di Experience League.
exl-id: 874f88d7-18ad-4ac8-bfa3-737255652bbc
source-git-commit: 03d46c9ffb664824f9526f781d776069d486f271
workflow-type: tm+mt
source-wordcount: '2227'
ht-degree: 7%

---

# Linee guida sullo stile di authoring per i collaboratori esterni{#guidelines}

Questa pagina fornisce linee guida editoriali per gli autori esterni che creano contenuti o aggiornano contenuti esistenti all’Experience League. Prima di iniziare, assicurati di:

* Acquisisci familiarità con [Markdown](markdown.md) authoring
* Controlla l’ortografia e la grammatica degli articoli
* Utilizza un tono amichevole, presentazione coerente e frasi semplici per migliorare la traduzione automatica
* Segui [best practice](#writing-tips) e gli standard editoriali in questa pagina

## Linee guida sugli stili{#style-guidelines}

Tieni presente quanto segue durante la scrittura della documentazione.

* **Scrivi in modo sintetico**: non sprecare parole. Mantieni le frasi brevi e concise. Mantieni l’articolo mirato. Mantieni al minimo il numero di note.
* **Concentrati sul pubblico e sullo scopo**: prima di iniziare a scrivere, stabilisci chiaramente chi sia il cliente e quale attività sta tentando di svolgere. Scrivi l’articolo per aiutare il cliente a svolgere quell’attività.
* **Utilizza esempi**: fornisci esempi per spiegare i concetti.
* **Organizza i contenuti**: crea delle sezioni per suddividere le istruzioni in gruppi di passaggi più gestibili. Aggiungi una schermata quando serve per maggiore chiarezza.

## Best practice per la scrittura tecnica{#writing-tips}

La scrittura tecnica, in particolare per la documentazione del software, è un settore specializzato. Persino il romanziere più prolifico si agita quando si tenta di scrivere tecniche—non perché il materiale sia complesso o tecnico, ma perché non è facile fare informazioni tecniche complesse _semplice_. Per avere successo, il contenuto deve essere strutturalmente coerente, scalabile, riutilizzabile e fluire attraverso la pipeline di pubblicazione senza errori di struttura e sintassi.

Le sezioni seguenti descrivono i problemi comuni per i quali i nuovi scrittori devono prestare attenzione:

### Intestazioni non separate da testo (titoli doppi){#double-headings}

Se sono presenti due intestazioni senza testo separato, aggiungi il testo mancante (per introdurre il secondo titolo dell’argomento). In alternativa, è possibile rimuovere una delle intestazioni. La seconda è probabilmente superflua.

Ad esempio: _Panoramica_ non ha uno scopo qui:

![Intestazioni doppie](assets/headings-double.png)

* Inoltre, se la seconda intestazione è _Panoramica_ Probabilmente non è necessario. L’H1 e il primo paragrafo fungono da panoramica concettuale sull’argomento dell’articolo.

* Analogamente, per l’ottimizzazione SEO (Search Engine Optimization), titoli autonomi come _Panoramica_ e _Introduzione_ non sono utili da soli. Denomina il prodotto o la funzione che stai introducendo. (Esempio: _Panoramica dei rapporti di abbandono_)

### Intestazioni di riferimento incrociato incoerenti{#maps}

Utilizzo _Ulteriori informazioni_ intestazioni per gli elenchi di riferimenti incrociati (o mappe). Esempio:

![Elenco dei riferimenti incrociati](assets/headings-more-info.png)

**Indicazioni per gli elenchi di riferimenti incrociati**

* Utilizzare un elenco puntato per i riferimenti incrociati
* Usa il corsivo per i nomi formali delle guide o dei nomi di pagina (quando non utilizzi il testo di collegamento)
* Non eseguire la punteggiatura dell’intestazione (o di qualsiasi intestazione)
* Evitare i numeri nelle intestazioni

### Voce di sommario, breadcrumb e nome della pagina non corrispondenti{#toc}

Poiché gestiamo manualmente il file TOC (sommario), queste mancate corrispondenze sono semplici errori. Assicurati che la voce del sommario corrisponda al nome della pagina (H1). Inoltre, assicurati che corrisponda strettamente al breadcrumb.

**Indicazioni sui sommario e sugli elenchi**

* Potrebbe essere necessario ridurre la voce del sommario, ma deve essere chiaramente correlata al nome della pagina e alla breadcrumb.
* Le breadcrumb vengono estratte dai metadati del titolo, in modo che possano essere diverse (a scopo di SEO).

### Virgolette invece del corsivo{#quotes}

È difficile resistere all&#39;aggiunta di citazioni intorno a una parola o una frase. Tuttavia, le citazioni sono destinate a citazioni vocali e non sono quasi mai utilizzate nella documentazione del prodotto.

**Indicazioni sulle virgolette**

* Di solito il corsivo funziona meglio delle virgolette (per messaggi di errore, parole univoche o straniere e così via).
* Per gli elementi dell’interfaccia, utilizza bold e UICONTROL.

### Procedure{#steps}

Scrittura di una procedura (il _compito_ tipo di contenuto) non è un talento con cui siamo nati. La creazione di una procedura chiara e leggibile è pratica.

**Guida alle fasi**

* Una procedura è una serie di passaggi. Un passo è breve, numerato, _a frase singola_ comando.
* Inizia ogni passo con un verbo o con _A_ infinito (per orientare il lettore verso l&#39;obiettivo, come in, _Per mantenere l&#39;accesso, abilita **Resta connesso**_). Se un passaggio ha un obiettivo specifico nell’ambito della procedura generale, indica l’obiettivo prima dell’azione.
* Se disponi di informazioni sul passaggio (un tipo di contenuto denominato _informazioni sul passaggio_, aggiungilo dopo il passaggio (rientrato con il passaggio ) o dopo la risorsa (una schermata, un video o un elenco di descrizioni dell’interfaccia).
* Se il passaggio include due azioni, ad esempio _Seleziona questo, quindi quello_), scrivetela come una singola, breve frase.
* Limita l&#39;attività a circa sette o dieci passaggi. Se si creano più di dieci passaggi in un&#39;attività, è probabile che sia necessario suddividerlo in due attività. Usa il tuo miglior giudizio qui.
* Nella documentazione del prodotto, non utilizzare le intestazioni come passaggi. (Eccezione riportata di seguito per i tutorial.)
* Per le esercitazioni su più pagine, è possibile assegnare le intestazioni come passaggi. Tuttavia, non numerarli. Piuttosto, fatevi un&#39;idea. _Passaggio 1:_, _Passaggio 2:_ e così via.

**Procedura di esempio**

Di seguito è riportata una procedura ben strutturata per l’accesso, ad Adobe:

Per accedere ad Adobe:

1. On `Adobe.com`, seleziona **Experience Cloud**.
1. Seleziona **Accesso**.
1. Seleziona **Account personale**.
1. Per effettuare l&#39;accesso, seleziona **Resta connesso**.
1. Digita il tuo nome e la tua password.
1. Seleziona **Accesso**.

### Elenchi paralleli{#lists}

L&#39;utilizzo della costruzione parallela per gli elenchi facilita la lettura e la scansione. Gli elenchi includono un sommario (sommario), elenchi puntati (non ordinati) o elenchi numerati.

Esempio di sommario con voci parallele:

![TOC parallelo](assets/parallel-toc.png)

Il sommario precedente è un buon esempio perché:

* Le voci principali concettuali sono parole o frasi noun
* Le procedure (attività) sono verbi attivi (non germi)
* Tutte le voci utilizzano la maiuscola frase

## Metadati di titolo e descrizione{#metadata}

_Titolo_ e _descrizione_ I metadati sono importanti per SEO (Search Engine Optimization), l’individuazione dei contenuti e i punteggi di qualità dei contenuti, ad Experience League.

Di seguito sono riportati alcuni esempi di titoli e descrizioni:

**Descrizioni degli articoli di concetto**

* _Scopri i segmenti in Adobe Analytics. Scopri come configurare il pannello Segmentazione in un’area di lavoro._
* _Trova aiuto sull’utilizzo dei segmenti in un rapporto Visualizzazioni di pagina in Adobe Analytics._

**Descrizioni degli articoli di routine/task**

* _Scopri come creare un segmento in Adobe Analytics._
* _Crea un segmento in Adobe Analytics. Scopri come selezionare, configurare ed eseguire un rapporto basato sul segmento creato._

Quello che utilizzi dipende dalle dimensioni e dall’ambito dell’articolo.

**Titolo di un articolo concettuale**

* _Segmenti nei rapporti Visualizzazioni di pagina_

**Titolo per una procedura/un articolo di attività**

* _Creare un segmento per un rapporto Visualizzazioni di pagina_

(Ricordate che la tubazione e il nome del prodotto vengono aggiunti automaticamente ai titoli.)

## Modi per migliorare la chiarezza (e i punteggi di Acrolinx){#tips}

Di seguito sono riportati metodi semplici per migliorare la progettazione, la chiarezza e la leggibilità dei contenuti. Questi contribuiscono anche a migliorare i punteggi di stile Acrolinx e i punteggi CQI su ExL.

| Guida | Informazioni su |
|---|---|
| Usa voce attiva | Cambia voce passiva in voce attiva |
| Usa tensione presente | **Debole:** *La versione v8 di Campaign verrà rilasciata a giugno.* <p>**Forte:** *Versioni di Campaign v8 a giugno.*<p>La tensione presente è sempre più facile da leggere per i clienti. |
| Evitare avvertimenti deboli e inutili | *Molto*, *estremamente*, *incredibilmente*.... <p>Gli avverbi sono parole extra che non aggiungono significato significativo se si utilizzano verbi, clausole e aggettivi forti e precisi. |
| Usa verbi forti per titoli e [Voci TOC](#using-toc) | Esempi:<p>**Debole:** *Creazione e gestione delle caratteristiche* <p>**Forte:** *Creare e gestire le caratteristiche* |
| Usa frase [capitalizzazione](https://docs.microsoft.com/en-us/style-guide/capitalization) | Nel dubbio, non capitalizzare. Nei titoli, utilizza la capitalizzazione in stile frase. Capitalizzare i sostantivi propri e la prima parola dopo un due punti. Nelle procedure, fai corrispondere le maiuscole visualizzate nell’interfaccia. |
| Scopri questi piccoli suggerimenti per chiarezza | <ul><li>Evitare *Al fine di* (non aggiunge alcun significato). Tutto quello di cui hai bisogno è *a.*</li><li>Evitare *Utilizzare.* Potrebbe sembrare più tecnico, però non lo è. *Utilizzare* mezzi *per fare buon uso, soprattutto di qualcosa che non era destinato allo scopo ma servirà*.</li><li>Evitare i punti e virgola: Utilizza invece un punto e inizia una nuova frase. I semi colon introducono una complessità inutile.</li><li>Due punti: Usa i due punti per introdurre un elenco. Usa i due punti con moderazione all&#39;interno delle frasi. Capitalizza la prima parola dopo un due punti in una frase.</li><li>Utilizzare la virgola Oxford (tre virgole in un elenco).</li><li>Mantieni la lunghezza della frase sotto le 39 parole.</li><li>Navigazione: use _vai a_ o _naviga a_.</li><li>Evita il testo non elaborato dell’URL (usa testo di collegamento intuitivo) a meno che la visualizzazione del percorso non sia un’informazione importante.</li></ul> |
| Utilizzare un controllo ortografico in VSC | Installare Controllo ortografia del codice (estensione) in Visual Studio Code. |
| Modifica _click_ a _vai a_ o _select_ | _Fai clic su_ è una parola specifica per il dispositivo (con problemi di accessibilità) e la tendenza è allontanarsi da essa. Di seguito sono riportati alcuni suggerimenti per la modifica:<ul><li>Navigazione: _Vai a File > Stampa_.</li><li>Fai clic su: _Selezionare File > Stampa_ o _Seleziona OK_. </li></ul>Vedi [Descrizione delle interazioni con l’interfaccia utente](https://docs.microsoft.com/en-us/style-guide/procedures-instructions/describing-interactions-with-ui) per ulteriori idee sulla scelta migliore della parola in varie situazioni. |
| Eseguire Acrolinx in VSC | L&#39;acrolinx verifica la presenza di problemi di stile e grammatica. Controlla URL, terminologia, ortografia e altro ancora. Consente di migliorare la chiarezza e la traduzione dei contenuti di Experience League. |

{style=&quot;table-layout:auto&quot;}

Altre best practice e risorse:

* [Contenuto scannable](https://docs.microsoft.com/en-us/style-guide/scannable-content/): Aiuta i lettori a trovare rapidamente ciò di cui hanno bisogno o a riconoscerlo altrettanto rapidamente quando non sono dove devono essere. Scrivere per facilitare la scansione può aiutare.
* **Numeri:** Nel corpo del testo, specificare numeri interi da zero a nove e utilizzare numeri per 10 o più. Vedi [Numeri](https://docs.microsoft.com/en-us/style-guide/numbers).
* Scrivi come parli, progetta cordialità, e arrivare al punto in fretta.

Vedi [Primi 10 suggerimenti per la scrittura](https://docs.microsoft.com/en-us/style-guide/top-10-tips-style-voice) in [Guida allo stile di Microsoft®](https://docs.microsoft.com/en-us/style-guide/welcome/) per ulteriori informazioni.

## Testo Alt{#alt-text}

Aggiungi testo alternativo significativo alle risorse (immagini). Considera alt-text corrispondente:

* L’obiettivo che i clienti possono raggiungere (nome dell’attività o del concetto)
* Funzione o pagina da visualizzare
* Nome dell&#39;icona che stai mostrando

Google considera il testo alternativo nei risultati SEO (Search Engine Optimization).

## Localizzazione - DNL e UICONTROL{#localization}

Non devi preoccuparti se il tuo prodotto è localizzato o le lingue utilizzate da ExL. Tuttavia, puoi contribuire a migliorare la qualità della localizzazione applicando i due tag Markdown seguenti (necessari), se appropriato:

* `DNL`

   DNL significa _non localizzare_. Lo si utilizza solo per i nomi di prodotti Adobi con marchio registrato, che devono rimanere in inglese.

   Esempi di sintassi: `[!DNL Adobe Campaign]` o `[!DNL Workfront]`

   DNL non è destinato a nomi di file o URL.

* `UICONTROL`

   UICONTROL indica un controllo dell’interfaccia (ad esempio un’opzione, un campo, una scheda, una pagina, un gruppo di opzioni o un nome di funzione nell’interfaccia utente).

   Esempio di sintassi: `Select **[!UICONTROL Project]**, then select **[!UICONTROL Save]**.`

>[!IMPORTANT]
>
>È necessario applicare questi tag prima di localizzare il contenuto.

### Utilizzo di un Adobe nei nomi dei prodotti{#product-names}

Per l&#39;identità aziendale, di solito includiamo _Adobe_ nel primo riferimento di un prodotto a livello di guida. A seconda dello spazio, è possibile rilasciare l’Adobe in un’intestazione, ma il primo riferimento nella copia corpo deve includere il nome completo. Taluni prodotti, quali _Adobe Audition_ e _Adobe Premiere Pro_, richiedere l&#39;uso dell&#39;Adobe sul primo o il riferimento più importante in ogni elemento di garanzia, in quanto fa parte del nome legale, marchio di fabbrica.

## Primi paragrafi{#firstparas}

Il primo paragrafo deve definire l’argomento e descrivere ciò che il lettore apprende dalla lettura dell’articolo.

Primo paragrafo del campione (concetto):

_I tipi di pubblico sono raccolte di visitatori (un elenco di ID visitatore). Il servizio audience di Adobe gestisce la trasformazione dei dati dei visitatori in segmentazione del pubblico. La creazione e la gestione dei tipi di pubblico sono simili alla creazione e all’uso dei segmenti, e in più permettono di condividere i segmenti di pubblico nell’Experience Cloud._

Primo paragrafo di esempio (attività):

_Creazione della sorgente attributo cliente (file CSV e FIN) e caricamento dei dati. Puoi attivare l&#39;origine dati quando lo desideri. Quando la sorgente dati è attiva, condividi i dati attributo in Analytics e Target._

### Suggerimenti SEO per i primi paragrafi{#seo}

* Includi i termini di ricerca nei primi paragrafi.
* Utilizzare termini utilizzati dai lettori.
* Includere i sinonimi e, se necessario, l’uso precedente dei termini. Ad esempio, &quot;Il servizio Experience Cloud ID (ECID), noto in precedenza come _ID visitatore_ o come acronimi come MID, MCVID, fornisce un ID universale e costante che identifica i visitatori.&quot;
* Includi termini SEO nei collegamenti.
* Evitare di inserire termini essenziali in tabelle complesse. Tabelle complesse non producono risultati di ricerca affidabili. Il testo nelle immagini non è una ricerca. La ricerca viene eseguita nei sottotitoli.

## Capitalizzazione{#capitalization}

* Lo stile di Adobe utilizza le maiuscole in stile frase per tutti i titoli, le intestazioni, le sottotitoli e gli elementi di navigazione della pagina.
* Tutte le parole sono minuscole ad eccezione della prima parola e dei nomi propri, come i nomi di marchi, soluzioni e servizi.
* Corrispondenza con le maiuscole nei nomi dei prodotti degli strumenti, delle opzioni, delle voci di menu, delle finestre di dialogo e dei campi.

## Sommario{#using-toc}

La `TOC.md` è il sommario. Ogni guida dovrebbe averne una.

**Guida editoriale per un sommario**

* Capitalizzazione: Utilizzare sempre il caso di frase per ogni voce (esclusi gli acronimi). Inserisci in maiuscolo solo i nomi dei prodotti formali o gli elementi dell’interfaccia (pagine, schede, campi, opzioni e così via). Fai riferimento all’interfaccia utente con le stesse preferenze.
* Forma del verbo e parallelismo: Usa il verbo imperativo ed evita i germogli. I sommario sono elenchi, quindi cercano sempre di mantenere gli elenchi paralleli la maggior parte delle volte. Ci sono eccezioni che a volte non possono essere evitate. Per le pagine concettuali, utilizzare sostantivi e frasi noun. Per le attività, utilizzare verbi.

**Guida alla sintassi**

* Un’intestazione di sezione (padre) nel sommario non può essere un collegamento; non ha una pagina con contenuto. Deve contenere un ancoraggio come `{#processing-rules}`.
* È necessario utilizzare la sintassi corretta per le intestazioni della sezione sommario (ad esempio, `+ Processing rules {#processing-rules}`) e collegamenti agli articoli sommario (ad esempio, `+ [Article name](article.md)`).
* Le voci dell’articolo sommario possono essere una versione ridotta del titolo dell’articolo. Seguire gli standard per la scrittura di panorami, concetti e attività contenuti in questo documento.
* Evita di aggiungere lo stesso file più volte a un sommario (o a più sommario). Fare così causa un comportamento strano.
* Se il repository contiene più guide utente, le directory della guida utente devono trovarsi allo stesso livello, ad esempio le sottodirectory all&#39;interno del `help` directory. Ogni directory della guida utente deve disporre di un file TOC. Nessuna guida utente nidificata.

## Grassetto e corsivo{#bold}

* Utilizzare il testo in grassetto solo per gli elementi di interfaccia su cui si fa clic in una procedura (e con UICONTROL).
* Utilizza il corsivo per enfasi o quando una parola confonde senza di essa. Ad esempio, una parola straniera o quando si descrive una parola o si definisce un termine.
