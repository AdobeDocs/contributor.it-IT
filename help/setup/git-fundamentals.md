---
title: Nozioni di base sulla documentazione Git e GitHub
seo-title: Nozioni di base sulla documentazione Git e GitHub
description: Il presente articolo illustra una panoramica dell’archivio Git, GitHub, il modo in cui il contenuto viene organizzato e le convenzioni di denominazione che vengono utilizzate per la documentazione di Adobe.
seo-description: Il presente articolo illustra una panoramica dell’archivio Git, GitHub, il modo in cui il contenuto viene organizzato e le convenzioni di denominazione che vengono utilizzate per la documentazione di Adobe.
translation-type: ht
source-git-commit: 4d8d741544e5fefe6d186e75ce4157ea127d5b16

---

# Nozioni di base sulla documentazione Git e GitHub

## Panoramica

Se si desidera apportare solo modifiche secondarie testuali agli articoli, non è necessario comprendere i dettagli del presente articolo. Il presente articolo descrive il flusso di lavoro per l’applicazione di modifiche principali, ad esempio la creazione di nuovi articoli, l’aggiunta di immagini o l’applicazione di modifiche continuative alla documentazione di Adobe.

In qualità di collaboratore al contenuto della documentazione di Adobe, puoi interagire con più strumenti e processi. Puoi lavorare in parallelo con altri collaboratori sullo stesso progetto, potenzialmente lo stesso contenuto, anche nello stesso momento. Tutto ciò è consentito dal software Git e GitHub.

Git è un sistema di controllo della versione open source che consente la collaborazione. Più collaboratori possono lavorare su file che risiedono in degli *archivi*.

GitHub è un servizio di hosting basato su Web per gli archivi Git, ad esempio quelli utilizzati per archiviare i contenuti di [docs.adobe.com](https://docs.adobe.com). Per qualsiasi progetto, GitHub ospita l’archivio principale, dal quale i collaboratori possono effettuare copie per il proprio lavoro.

## Git

Git dispone di un flusso di lavoro e di una terminologia univoci per supportare il proprio modello distribuito. Ad esempio, non esiste un blocco file normalmente associato alle operazioni di check-out/check-in. Git consente di risolvere le modifiche a un livello ancora più preciso, confrontando i file byte per byte.

Git utilizza inoltre una struttura a livelli per archiviare e gestire il contenuto per un progetto:

- *Archivio*: anche noto come *repo* o repository, è l’unità di archiviazione di livello più alto. Un archivio contiene uno o più rami.
- *Ramo*: tutti gli archivi contengono un ramo predefinito (in genere denominato “principale”) e uno o più rami destinati a essere uniti nuovamente al ramo principale. Il ramo principale rappresenta la versione corrente e la fonte dalla quale il contenuto viene pubblicato. È l’elemento superiore da cui vengono creati tutti gli altri rami nell’archivio.

I collaboratori interagiscono con Git per aggiornare e manipolare archivi a livello locale e di GitHub:

- Localmente mediante strumenti quali GitHub Desktop.
- Tramite [www.github.com](https://www.github.com), che integra Git per gestire la riconciliazione dei contributi che torneranno nell’archivio principale.

## GitHub

Tutti i flussi di lavoro iniziano e terminano a livello di GitHub, dove viene conservato l’archivio principale per qualsiasi progetto della documentazione di Adobe. Le copie create dai collaboratori per il proprio utilizzo vengono distribuite su più computer. Tali copie vengono infine riconciliate nell’archivio GitHub principale del progetto.

### Organizzazione della directory

Il ramo predefinito/principale di un progetto rappresenta la versione corrente del contenuto per il progetto. Il contenuto del ramo principale (e dei rami creati da esso) è allineato all’organizzazione degli argomenti dell’articolo. Le sottodirectory vengono utilizzate per organizzare il contenuto e le risorse immagine.

Di solito è possibile trovare una directory `help` principale dalla radice dell’archivio. La directory degli articoli contiene un set di sottodirectory. Gli articoli nelle sottodirectory vengono formattati come file Markdown che utilizzano un’estensione *.md*.

Nella radice di tale directory, puoi trovare articoli generali che si riferiscono al servizio o al prodotto generale. In genere, puoi trovare un’altra serie di sottodirectory che corrispondono a funzioni/servizi o scenari comuni.

### Directory risorse

Le directory della guida utente contengono sottodirectory `/assets` per i file immagine a cui si fa riferimento all’interno di una directory.

<!---
### Markdown file template

For convenience, the root directory of each repository typically contains a Markdown template file named `template.md`. You can use this template file as a "starter file" if you need to create a new article for submission to the repository. The file contains:

- A **metadata header** at the top of the file, delineated by two, 3-hyphen lines. It contains the various tags used for tracking information related to the article. It also includes SEO optimizations and reporting processes that Adobe uses to evaluate the performance of the content. So the metadata is important!
- Various **examples of using Markdown** to format the elements of an article.
- General **instructions on the use of Markdown extensions**, which you can use for various types of alerts.
- Examples of **embedding video** by using an iframe.
- General **instructions on the use of docs.adobe.com extensions**, which you can use for special controls such as buttons and selectors.
-->

## Richieste di pull

Una *richiesta di pull* consente a un collaboratore di proporre in modo pratico un insieme di modifiche da applicare al ramo predefinito. Le modifiche (dette anche *proposte*) vengono archiviate nel ramo di un collaboratore, così da consentire per prima cosa a GitHub di modellare l’impatto della loro *unione* al ramo predefinito. Una richiesta di pull funge anche da meccanismo per fornire al collaboratore un feedback da un processo di creazione/convalida o dal revisore di una richiesta di pull, per risolvere potenziali problemi o domande prima che le modifiche vengano unite al ramo predefinito.

Vi sono due modi per contribuire tramite richiesta di pull, in base alla portata delle modifiche che desideri proporre. Tale descrizione verrà fornita in dettaglio più avanti, nella sezione [Flusso di lavoro GitHub](local-repo.md) della presente guida.
