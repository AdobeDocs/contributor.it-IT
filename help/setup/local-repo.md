---
title: Configurare localmente l’archivio Git
seo-title: Configurare localmente l’archivio Git per la documentazione di Adobe
description: Il presente articolo fornisce indicazioni per creare l’archivio locale Git e contribuire alla documentazione di Adobe, compresi i processi di forking e di clonazione.
seo-description: Il presente articolo fornisce indicazioni per creare l’archivio locale Git e contribuire alla documentazione di Adobe, compresi i processi di forking e di clonazione.
translation-type: tm+mt
source-git-commit: e7382ef4aefc69c6b4e7d78b7f34eaf897596eaf

---


# Configurare localmente l’archivio Git per la documentazione

Il presente articolo descrive la procedura per configurare un archivio Git sul computer locale, con lo scopo di contribuire alla documentazione di Adobe. I collaboratori possono utilizzare un archivio clonato localmente per aggiungere nuovi articoli, apportare modifiche principali agli articoli esistenti o modificare le immagini.

> [!IMPORTANT]
> Se apporti solo modifiche minori a un articolo, *non* devi completare i passaggi descritti nel presente articolo. Puoi semplicemente fare clic sull’icona Modifica e apportare modifiche testuali nel browser.

## Panoramica

Per contribuire alla documentazione di Adobe, puoi effettuare il forking dell’archivio appropriato nell’account GitHub, così da disporre delle autorizzazioni di lettura e scrittura. Quindi puoi creare e modificare localmente i file Markdown clonando l’archivio della documentazione corrispondente. Puoi infine utilizzare le richieste di pull per unire (inviare) le modifiche all’archivio condiviso centrale di sola lettura.

* Determinare l’archivio appropriato
* Effettuare il forking dell’archivio nell’account GitHub
* Scegliere una cartella locale per i file clonati
* Clonare l’archivio sul computer locale
* Configurare il valore remoto a monte

## Determinare l’archivio

Puoi effettuare il forking dell’archivio appropriato nell’account GitHub in modo da disporre delle autorizzazioni di lettura e scrittura per archiviare le modifiche proposte. [!UICONTROL Adobe Experience Cloud] la documentazione risiede in diversi archivi all&#39;indirizzo [github.com](https://www.github.com/adobedocs).

1. Se non sai con certezza quale archivio utilizzare, consulta l’articolo dal browser Web. Fai clic sul collegamento **Edit** (icona della matita) in alto a destra nell’articolo (se non vedi il collegamento Modifica, tale contenuto non è ancora disponibile in GitHub.)

Per contribuire alla documentazione di Adobe è possibile creare e modificare localmente i file Markdown clonando l’archivio della documentazione corrispondente. Puoi quindi utilizzare le richieste di pull per unire le modifiche all’archivio condiviso centrale di sola lettura.

<!---
![GitHub Triangle](/assets/git-and-github-initial-setup.png)

If you're new to GitHub, watch the following video for a conceptual overview of the forking and cloning process:

>[!VIDEO https://channel9.msdn.com/Blogs/CoolMoose/Git-Repository-Setup/player]
-->

## Effettuare il forking dell’archivio

Utilizzando l’archivio appropriato, crea un fork dell’archivio nell’account GitHub utilizzando il sito Web GitHub.

È necessario un fork personale in quanto tutti gli archivi principali della documentazione forniscono accesso in sola lettura, ovvero non è possibile apportare modifiche direttamente al contenuto degli archivi. Per apportare modifiche devi inviare una richiesta di pull (PR) dal fork all’archivio principale. Per semplificare questo processo, devi innanzitutto disporre della copia dell’archivio in cui disponi di accesso in scrittura. Un *fork* GitHub è utile a tale scopo.

1. Passa alla pagina GitHub dell’archivio principale e fai clic sul pulsante **Fork** in alto a destra.

   ![GitHub fork](assets/fork-simple.png)

1. Se viene richiesto, seleziona la sezione dell’account GitHub come destinazione in cui creare il fork. Questo prompt crea una copia dell’archivio all’interno dell’account GitHub, nota come fork.

1. Scegli un nome cartella facile da ricordare e digitare.

   Alcuni archivi possono essere di grandi dimensioni. Scegli una posizione con spazio su disco disponibile.

   > [!NOTE]
   > Evita di scegliere il percorso di una cartella locale nidificata all’interno della posizione di un’altra cartella dell’archivio Git. Sebbene sia accettabile archiviare le cartelle clonate Git in modo che siano adiacenti le une alle altre, la nidificazione delle cartelle Git l’una nell’altra causa errori per il tracciamento dei file.

## Creare un clone locale dell’archivio

Creando un clone dell’archivio, viene scaricata una copia dei file nel computer. Quando sei pronto, puoi inviare le modifiche dall’unità locale all’archivio con fork sul server. Puoi quindi inviare una richiesta di pull per unire le modifiche a monte all’archivio principale.

Questi passaggi presuppongono l’utilizzo di GitHub Desktop. Se utilizzi un client diverso, apporta le regolazioni necessarie.

1. Fai clic su **Clone or download** e scegli **Open in Desktop** per estrarre una copia dell’archivio (il fork) sul computer nella directory corrente.

  ![Clone repo](assets/clone-pulldown.png)

1. Utilizza GitHub Desktop per mantenere i file locali sincronizzati con il fork dell’archivio.

Per informazioni, consulta [GitHub Desktop Documentation](https://help.github.com/desktop/).
