---
title: Flusso di lavoro dei contributi GitHub per modifiche principali
description: Scopri come apportare contributi alla documentazione di Adobe sull’Experience League.
exl-id: ad467ad4-abd2-4166-8659-e29c48d268ec
source-git-commit: 90122796acee9214ba96360eb7b5ff5c321a4bd6
workflow-type: tm+mt
source-wordcount: '944'
ht-degree: 82%

---

# Flusso di lavoro dei contributi GitHub per modifiche principali

<!--
>[!IMPORTANT]
>All repositories that publish to docs.adobe.com have adopted the [Adobe Open Source Code of Conduct](../../code-of-conduct.md) or the [.NET Foundation Code of Conduct](https://dotnetfoundation.org/code-of-conduct). For more information, see the [Contributing](../../contributing.md) article.
>
> Minor corrections or clarifications to documentation and code examples in public repositories are covered by the [Adobe Documentation Terms of Use](https://www.adobe.com/legal/terms.html). New or significant changes generate a comment in the pull request, asking you to submit an online Contribution License Agreement (CLA) if you are not an employee of Adobe. We need you to complete the online form before we can review or accept your pull request.
--->

## Panoramica

Il presente flusso di lavoro è indicato per i collaboratori che devono apportare una modifica principale o che saranno collaboratori frequenti in un archivio. Di solito i collaboratori frequenti hanno modifiche continuative (di lunga durata), che attraversano più cicli di creazione/convalida/staging o si estendono per più giorni prima dell’autorizzazione della richiesta di pull e dell’unione.

### Terminologia

Prima di iniziare, esaminiamo alcuni dei termini Git/GitHub utilizzati in questo flusso di lavoro.

| Nome | Descrizione |
|-----------|-------------|
| fork | Utilizzato normalmente come sostantivo, quando si fa riferimento a una copia di un archivio GitHub principale. Nella pratica, un fork è solo un altro archivio, ma è speciale perché GitHub mantiene una connessione bidirezionale all’archivio principale. A volte è utilizzato come verbo, come in “Per prima cosa devi effettuare il forking dell’archivio”. |
| remoto | Una connessione con nome a un archivio remoto, come ad esempio il remoto “origine” o “a monte”. Git fa riferimento a tali elementi come remoti poiché sono utilizzati per fare riferimento a un archivio ospitato su un altro computer. In questo flusso di lavoro, un remoto è sempre un archivio GitHub. |
| origine | Nome assegnato alla connessione tra l’archivio locale e l’archivio dal quale è stato clonato. In questo flusso di lavoro, l’origine rappresenta la connessione al fork. A volte viene usato come appellativo per l’archivio di origine stesso, come in “Ricorda di inviare le modifiche all’origine”. |
| a monte | Analogamente al remoto di origine, a monte è una connessione con nome a un altro archivio. In questo flusso di lavoro, a monte rappresenta la connessione tra l’archivio locale e l’archivio principale, da cui è stato creato il fork. A volte viene usato come appellativo per l’archivio a monte stesso, come in “Ricorda di estrarre le modifiche da a monte”. |

Se non conosci concetti Git e GitHub quali archivio o ramo, per prima cosa consulta [Principi di base Git e GitHub](git-fundamentals.md).

## Flusso di lavoro

>[!IMPORTANT]
> Se non lo hai già fatto, devi completare i passaggi nella sezione [Setup](github-signup.md).

In questo flusso di lavoro, le modifiche attraversano un ciclo ripetitivo. A partire dall’archivio locale del dispositivo, queste vengono reindirizzate al fork GitHub, nell’archivio GitHub principale, e tornano di nuovo a livello locale man mano che le modifiche di altri collaboratori vengono incorporate.

### Usare il flusso GitHub

Ricorda da [Principi di base di Git e GitHub](git-fundamentals.md) che un archivio Git contenga un ramo principale, più eventuali rami work-in-progress aggiuntivi che non sono stati integrati nel principale. Ogni volta che introduci un set di modifiche a livello logico, è consigliabile creare un *filiale* per gestire le modifiche tramite il flusso di lavoro. In questo caso si tratta di un ramo di lavoro, in quanto si tratta di un’area di lavoro per l’iterazione o la definizione delle modifiche, fino a quando queste non possono essere integrate nuovamente nel ramo principale.

L’isolamento delle modifiche correlate a un ramo specifico consente di controllare e introdurre tali modifiche in modo indipendente, indirizzandole a un determinato tempo di rilascio nel ciclo di pubblicazione. In realtà, in base al tipo di lavoro svolto, puoi facilmente ritrovarti con diversi rami di lavoro nell’archivio. Non è raro lavorare contemporaneamente su più rami, ognuno dei quali rappresenta un progetto diverso.

>[!NOTE]
>
>Apportare le modifiche nel ramo principale *non è una buona pratica*. Immagina di utilizzare il ramo principale per introdurre un set di modifiche per un rilascio di funzioni temporizzate. Hai terminato le modifiche e sei in attesa del rilascio. Nel frattempo, hai una richiesta urgente per correggere qualcosa, quindi apporti la modifica a un file nel ramo principale e poi pubblichi la modifica. In questo esempio, pubblichi inavvertitamente sia la correzione *sia* le modifiche che stavi tenendo per il rilascio in una data specifica.

La fase successiva consiste nel creare un nuovo ramo di lavoro nell’archivio locale per acquisire le modifiche proposte. Ciascun client Git è diverso, quindi consulta l’Aiuto per il tuo client preferito. Puoi vedere una panoramica del processo nella Guida GitHub sul [Flusso GitHub](https://guides.github.com/introduction/flow/).

## Elaborazione della richiesta di pull

Puoi inviare le modifiche proposte raggruppandole in una nuova richiesta di pull (PR) che viene aggiunta alla coda di PR dell’archivio di destinazione. Una richiesta di pull abilita il modello di collaborazione di GitHub, chiedendo che le modifiche dal ramo di lavoro vengano estratte e unite a un altro ramo. Nella maggior parte dei casi, l’altro ramo è il ramo predefinito/principale nell’archivio principale.

### Convalida

Prima che la richiesta di pull possa essere unita al relativo ramo di destinazione, potrebbe essere necessario superare uno o più processi di convalida PR. I processi di convalida possono variare in base alla portata delle modifiche proposte e delle regole dell’archivio di destinazione. Una volta inviata la richiesta di pull, puoi aspettarti che il contenuto venga rivisto e, se e quando appropriato, unito all’archivio principale.

### Revisione e autorizzazione

Al termine dell’elaborazione di tutte le PR, esamina i risultati (commenti PR, URL di anteprima, ecc.) per determinare se sono necessarie modifiche aggiuntive ai file prima di autorizzare l’unione. Se un revisore di PR ha rivisto la richiesta di pull, può anche fornire un feedback tramite commenti in caso di problemi/domande in sospeso da risolvere prima dell’unione.

Quando la richiesta di pull è priva di problemi e autorizzata, le modifiche vengono unite nuovamente al ramo principale e la richiesta di pull viene chiusa.

### Pubblicazione

Ricorda che la richiesta di pull deve essere unita da un revisore PR prima che le modifiche possano essere incluse nella successiva pubblicazione pianificata. Le richieste di pull vengono normalmente riviste/unite in ordine di invio. Se la richiesta di pull richiede l’unione per una pubblicazione specifica, sarà necessario collaborare anticipatamente con il revisore PR per garantire che l’unione avvenga prima della pubblicazione.
