---
lastModified: 2018-06-28T00:00:00Z
title: Utilizzo di collegamenti nella documentazione
seo-title: Utilizzo di collegamenti nella documentazione Git/Markdown di Adobe
description: Questo articolo fornisce indicazioni sulla creazione di collegamenti a contenuti e immagini.
seo-description: Questo articolo fornisce indicazioni sulla creazione di collegamenti a contenuti e immagini per la documentazione di Adobe.
exl-id: f9d61aa9-931c-4654-ab21-c6e47936954e
translation-type: ht
source-git-commit: dad1df81797e6078645449501ed0661cf4bcf3ce
workflow-type: ht
source-wordcount: '340'
ht-degree: 100%

---

# Utilizzo di collegamenti nella documentazione

Questo articolo descrive l’utilizzo dei collegamenti ipertestuali nelle pagine della documentazione. In Markdown è facile aggiungere collegamenti con poche diverse convenzioni. I collegamenti indicano agli utenti contenuti nella stessa pagina, conducono ad altre pagine o indirizzano a siti e URL esterni.

>[!IMPORTANT]
>Tutti i collegamenti dovrebbero, idealmente, essere collegamenti protetti (`https` anziché `http`) ogni volta che viene supportato dal target (dovrebbe trattarsi della stragrande maggioranza dei casi).

## Collegamento a URL

Le parole incluse nel testo del collegamento devono essere il titolo della pagina oggetto del collegamento oppure un testo specifico e descrittivo.

**Esempi:**

- `For more information, see the [overview article](https://github.com/AdobeDocs/target.en/help/overview.md).`

- `For more details, see [Adobe Legal Concerns](https://www.adobe.com/legal).`

## Collegamento da un articolo a un altro

Per creare un collegamento in linea da un articolo a un altro articolo all’interno dello stesso archivio, utilizza la seguente sintassi di collegamento:

- Un articolo in una directory effettua un collegamento a un altro articolo nella stessa directory:

   `[link text](article-name.md)`

- Un articolo effettua un collegamento da una sottodirectory a un articolo nella directory principale:

   `[link text](../article-name.md)`

- Un articolo effettua un collegamento da una sottodirectory a un articolo nella directory principale:

   `[link text](../../article-name.md)`

- Un articolo nella directory principale effettua un collegamento a un articolo in una sottodirectory:

   `[link text](./directory/article-name.md)`

- Un articolo in una sottodirectory effettua un collegamento a un articolo in un’altra sottodirectory:

   `[link text](../directory/article-name.md)`

- Un articolo in una sottodirectory effettua un collegamento a un articolo in un’altra sottodirectory:

   `[link text](../../directory/article-name.md)`

## Collegamento ad ancoraggi

Non è necessario creare ancoraggi. Vengono generati automaticamente in fase di pubblicazione per tutte le intestazioni H2. L’unica cosa da fare è creare collegamenti alle sezioni H2 (##).

- Per effettuare un collegamento a un’intestazione all’interno dello stesso articolo:

   `[link](#the-text-of-the-level2-section-separated-by-hyphens)`

   `[Link to anchors](#links-to-anchors)`

- Per effettuare un collegamento a un ancoraggio in un altro articolo nella stessa sottodirectory:

   `[link text](article-name.md#anchor-name)`

   `[Configure your profile](overview.md#getting-started)`

- Per effettuare un collegamento a un ancoraggio in un’altra sottodirectory del servizio:

   `[link text](../directory/article-name.md#anchor-name)`

   `[Configure your profile](../overview.md#configure-your-profile)`

## Collegamento a immagini

Come procedura ottimale, le immagini e i file vengono archiviati in una directory `assets` allo stesso livello del file Markdown che vi è collegato.

- Un articolo effettua un collegamento a un’immagine nella `assets` sottodirectory:

   `![alt text](assets/image-name.png)`

- Un articolo effettua un collegamento a un’immagine nella `assets/no-localize` sottodirectory:

   `![alt text](assets/no-localize/image-name.png)`
