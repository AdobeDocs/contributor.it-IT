---
title: Guida collaboratore per la documentazione di Adobe
seo-title: Panoramica dei collaboratori per la documentazione tecnica di Adobe Experience
  Cloud
description: La guida descrive come contribuire con suggerimenti e aggiunte al sito
  della documentazione di Adobe.
seo-description: La guida descrive come contribuire alla documentazione tecnica [!UICONTROL
  Adobe Experience Cloud].
translation-type: tm+mt
source-git-commit: 4d8d741544e5fefe6d186e75ce4157ea127d5b16

---


# Panoramica della Guida introduttiva per la documentazione di Adobe

## Documentazione di collaborazione

Durante il 2019, tutta la documentazione tecnica e il contenuto di abilitazione per Adobe Experience Cloud passeranno a una nuova piattaforma, in base ai principi open source, utilizzando le soluzioni Github, Markdown e Adobe Experience Cloud, inclusi Adobe Experience Manager, Analytics, Launch e Target.

Questo modello open source migliora la qualità dei contenuti e la comunicazione tra clienti, team di documentazione e team di prodotto. In ogni pagina è ora possibile valutare l'utilità dei contenuti, i problemi di registro e persino i suggerimenti di contenuto come richieste pull Git (PR). I team di documentazione Adobe controllano i contributi e i problemi su base giornaliera e effettuano aggiornamenti, tweaks e regolazioni, a seconda delle necessità.

## Utilizzo della documentazione collaborativa

Come utente di questo materiale, a prescindere da se sei un dipendente, un partner, un cliente o anche un potenziale cliente, hai la possibilità di contribuire a questa documentazione in diversi modi semplici;

* rate della pagina
* registrare un problema rispetto a una pagina specifica
* even submit a quick edits through to authoring entire articles, complete with assets and code samples

Questa guida delinea tutti gli elementi necessari per interagire con e contribuire a questo set di materiale.

<!--
> [!IMPORTANT]
> All repositories that publish to docs.adobe.com have adopted the [Adobe Open Source Code of Conduct](../code-of-conduct.md) or the [.NET Foundation Code of Conduct](https://dotnetfoundation.org/code-of-conduct). For more information, see the [Contributing](../contributing.md) article.
>
> Minor corrections or clarifications to documentation and code examples in public repositories are covered by the [Adobe Documentation Terms of Use](https://www.adobe.com/legal/terms.html). New or significant changes generate a comment in the pull request, asking you to submit an online Contribution License Agreement (CLA) if you are not an employee of Adobe. We need you to complete the online form before we can review or accept your pull request.
--->

## Apportare modifiche rapide ai documenti esistenti

Apportare delle modifiche rapide è un modo utile per correggere piccoli errori e omissioni nei documenti. Se un articolo visualizza un pulsante di modifica come mostrato di seguito, puoi apportare autonomamente una correzione rapida. Quando modifichi il documento, invii una richiesta di pull (PR) per inviare la correzione o il suggerimento e quest’ultimo può essere esaminato, approvato e pubblicato.

1. Firmare il [Contratto di licenza Collaboratore (CLA)](http://opensource.adobe.com/cla.html) se è accettabile.

   È necessario inviare un solo Adobe CLA una volta.
1. Fai clic su ** nella colonna di destra per passare al file Markdown di origine su GitHub.`Edit this page`**
1. Fate clic sull'icona a forma di matita per modificare l'articolo.

   > [!NOTE]
   > Se l’icona della matita è disattivata, devi accedere all’account GitHub oppure creare un nuovo account.

   ![Location of the pencil icon](assets/edit-icon.png)

1. Apporta le modifiche nell’editor Web. Puoi fare clic sulla scheda **Preview changes** per controllare la formattazione delle modifiche.
1. Dopo aver apportato le modifiche, scorri fino alla parte inferiore della pagina. Immetti un titolo e una descrizione per la PR e fai clic su **Suggest file change** come mostrato nella figura seguente:

   ![proposing your change](assets/submit-pull-request.png)

   >[!NOTE] Se si riceve un messaggio di errore relativo alla firma di un contratto di licenza collaboratore (CLA), fare clic su **Dettagli per** aprire il contratto di licenza. Firmare il contratto, se accettabile. Quindi chiudi e apri la richiesta di pull e continua.

Tutto qui. Grazie. I membri del team della documentazione potranno esaminare e unire la tua richiesta di pull.

## Segnalare un problema

Un altro semplice modo per riportare un problema con dei contenuti è “Segnalare un problema”.

1. Se noti un problema con uno dei contenuti, fai clic sul collegamento `Log an Issue` in basso a destra di qualsiasi pagina. Vedi la figura seguente:

   ![](assets/git_log_issue.png)

   > [!NOTE]
   > Per segnalare un problema dovrai accedere all’account GitHub o creare un nuovo account.

   Facendo clic su questo collegamento, potrai registrare una segnalazione rapida utilizzando l’interfaccia GitHub Issue.

1. L’URL della pagina che contiene il problema viene automaticamente popolato nel campo di descrizione. Inserisci il titolo, scrivi una breve descrizione del problema, quindi fai clic su *Submit new issue*.

   ![](assets/git_issue_example.png)

L'invio di un'edizione notifica direttamente al team dei contenuti di questa pagina chi sarà in grado di intervenire. Una volta aggiornato il contenuto, verrai informato nell’interfaccia GitHub Issues e riceverai una notifica tramite e-mail dopo l’aggiornamento o la chiusura.

## Comprendere le autorizzazioni GitHub

L’interfaccia utente di modifica di GitHub si adatta alle autorizzazioni dell’archivio. Le immagini precedenti sono rese in modo accurato per i collaboratori che non dispongono delle autorizzazioni di scrittura per l’archivio di destinazione. GitHub crea automaticamente un fork dell’archivio di destinazione nell’account. Se disponi di accesso in scrittura per l’archivio di destinazione, GitHub crea un nuovo ramo nell’archivio di destinazione.

Adobe utilizza le richieste di pull per tutte le modifiche, anche per i collaboratori con accesso in scrittura. La maggior parte degli archivi presenta il ramo `master` protetto, perciò gli aggiornamenti devono essere inviati come richieste di pull.

L’esperienza di modifica nel browser è ideale per modifiche minori o non frequenti. Se apporti contributi di grandi dimensioni o utilizzi funzioni Git avanzate, ti consigliamo di [effettuare il forking dell’archivio e lavorare localmente](setup/full-workflow.md).

## Fornire feedback

Con un set di soluzioni quello di Adobe, la documentazione è in continua elaborazione. Se noti degli errori, segnala un problema; se hai suggerimenti sul materiale, comunicali. Indicaci quali informazioni stavi cercando. Comunicaci se non hai trovato ciò di cui avevi bisogno o se hai incontrato difficoltà a completare l’attività; informaci su come possiamo aiutarti a scoprire di più sulle soluzioni.

Grazie al team della documentazione collaborativa e a tutti gli autori e i produttori di contenuti in [!UICONTROL Adobe Experience Cloud].
