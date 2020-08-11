---
lastModified: 2018-06-28T00:00:00Z
title: Utilizzo di collegamenti nella documentazione
seo-title: Utilizzo di collegamenti nella documentazione Git/Markdown di Adobe
description: Questo articolo fornisce indicazioni sulla creazione di collegamenti a contenuti e immagini.
seo-description: Questo articolo fornisce indicazioni sulla creazione di collegamenti a contenuti e immagini per la documentazione di Adobe.
translation-type: ht
source-git-commit: 73ec3b8b63769a192ee16bec2720930ea6a9aaed
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

<!--
## Bob's link test

<table id="table_C27955F6B52A45B28BEEAAF14FFC86D8"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> File Type </th> 
   <th colname="col2" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="filepath"> .csv </span> </p> </td> 
   <td colname="col2"> <p>A comma-separated values file (such as one created in Excel). This is the file that contains the customer attribute data. See [Link TEST](/help/setup/full-workflow.md) </p> <p> <b>Naming requirements:</b> Ensure that file name extensions do not contain white spaces. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="filepath"> .fin </span> </p> </td> 
   <td colname="col2"> <p>(Required) The <span class="filepath"> .fin </span> file tells the system that you are finished uploading data. The name of the <span class="filepath"> .fin </span> file must match the name of the <span class="filepath"> .csv </span> file. </p> <p>Adobe recommends creating an empty text file with a <span class="filepath"> .fin </span> extension. An empty file saves space and upload time. </p> <p> <p>Note:  Renaming a <span class="filepath"> .fin </span> file is not allowed after it is uploaded. The <span class="filepath"> .fin </span> file must be uploaded separately and cannot be a renamed, previously uploaded file. </p> </p> <p>After you upload the <span class="filepath"> .fin </span> file in the customer attributes FTP, the system retrieves data quickly (within one minute). This differs from other Adobe FTP-based systems, which pick up data less frequently (around once per hour). </p> <p>The <span class="filepath"> .fin </span> file is not required when using the drag-and-drop upload method. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="filepath"> .gz </span> or <span class="filepath"> .zip </span> </p> </td> 
   <td colname="col2"> <p> <span class="filepath"> .gz </span> (gzip) or <span class="filepath"> .zip </span> - for compressed files. A <span class="filepath"> .zip </span> file cannot contain more than one file in the archive. </p> <p> <b>Naming requirements:</b> The name of the <span class="filepath"> .zip </span> or <span class="filepath"> .gz </span> should match the name of the <span class="filepath"> .csv </span>. For example, if your <span class="filepath"> .csv </span> file is <span class="filepath"> crm_small.csv </span>, the <span class="filepath"> .zip </span> file should be <span class="filepath"> crm_small.csv.zip </span>. </p> <p>The .fin file must match the .csv. </p> </td> 
  </tr> 
 </tbody> 
</table>
-->
