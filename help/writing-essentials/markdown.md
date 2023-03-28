---
title: Come utilizzare Markdown per la scrittura della documentazione
description: Scopri le nozioni di base sull’authoring Markdown. Trova informazioni di riferimento per il linguaggio Markdown utilizzato per la scrittura di articoli.
exl-id: 3e5726e2-139e-4e44-ae5b-8a3ae4782faf
source-git-commit: 065e43d5251f80050deef02e9c18b3fb4e9c1204
workflow-type: ht
source-wordcount: '1430'
ht-degree: 100%

---

# Come utilizzare Markdown per la scrittura della documentazione tecnica

Gli articoli della documentazione tecnica di Adobe sono scritti in un linguaggio di markup leggero chiamato [Markdown](https://daringfireball.net/projects/markdown/), facile da leggere e da apprendere.

Poiché il contenuto dei documenti Adobe viene archiviato in GitHub, è possibile utilizzare una versione di Markdown denominata [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), che offre funzionalità aggiuntive per le esigenze di formattazione comuni. Inoltre, Adobe ha esteso Markdown in diversi modi per supportare determinate funzionalità relative alla Guida, come note, suggerimenti e video incorporati.

## Nozioni di base su Markdown

Le sezioni seguenti descrivono le nozioni di base sull’authoring in Markdown.

### Intestazioni

Per creare un’intestazione, utilizza un cancelletto (#) all’inizio di una riga:

```
# This is level 1 (article title)
## This is level 2
### This is level 3
#### This is level 4
##### This is level 5
```

### Testo di base

Un paragrafo non richiede una sintassi speciale in Markdown.

Per formattare il testo in **grassetto**, è necessario racchiuderlo in due asterischi. Per formattare il testo in *corsivo*, è necessario racchiuderlo in un singolo asterisco:

```markdown
   This text is **bold**.
   This text is *italic*.
   This text is both ***bold and italic***.
```

Per ignorare i caratteri di formattazione di Markdown, utilizza \ prima del carattere:

```markdown
This is not \*italicized\* type.
```

### Elenchi numerati ed elenchi puntati

Per creare elenchi numerati, inizia una riga con `1.` o `1)`, ma non combinare i formati all’interno dello stesso elenco. Non è necessario specificare i numeri, che sono gestiti automaticamente da GitHub.

```markdown
1. This is step 1.
1. This is the next step.
1. This is yet another step, the third.
```

Visualizzato:

1. This is step 1.
1. This is the next step.
1. This is yet another step, the third.

Per creare degli elenchi puntati, inizia una riga con \* o - o + ma non combinare i formati all’interno dello stesso elenco (non mescolare formati punto elenco, ad esempio \* e \+ all’interno dello stesso documento).

```markdown
* First item in an unordered list.
* Another item.
* Here we go again.
```

Visualizzato:

* First item in an unordered list.
* Another item.
* Here we go again.

È inoltre possibile incorporare elenchi all’interno di elenchi e aggiungere contenuto tra gli elementi di un elenco.

```markdown
1. Set up your table and code blocks.
1. Perform this step.

   ![screen](assets/no-localize/adobe_standard_logo.png)

1. Make sure that your table looks like this: 

   | Hello | World |
   |---|---|
   | How | are you? |  

1. This is the fourth step.

   >[!NOTE]
   >
   >This is note text.

1. Do another step.
```

Visualizzato:

1. Set up your table and code blocks.
1. Perform this step.

   ![screen](assets/no-localize/adobe_standard_logo.png)

1. Make sure that your table looks like this:

   | Hello | World |
   |---|---|
   | How | are you? |

1. This is the fourth step.

   >[!NOTE]
   >
   >This is note text.

1. Do another step.

### Tabelle

Le tabelle non fanno parte della specifica di base di Markdown ma sono supportate in parte da Adobe. Gli elenchi su più righe in una cella non sono supportati da Markdown. Si consiglia di evitare di utilizzare più righe nelle tabelle. Puoi creare tabelle utilizzando il carattere barra verticale (|) per delineare colonne e righe. I trattini creano l’intestazione di ogni colonna, mentre le barre verticali separano ciascuna colonna. Includi una riga vuota prima della tabella affinché venga riprodotta correttamente.

```markdown
| Header | Another header | Yet another header |
|--- |--- |--- |
| row 1 | column 2 | column 3 |
| row 2 | row 2 column 2 | row 2 column 3 |
```

Visualizzato:

| Header | Another header | Yet another header |
|--- |--- |--- |
| row 1 | column 2 | column 3 |
| row 2 | row 2 column 2 | row 2 column 3 |

Le tabelle semplici funzionano correttamente in Markdown, mentre le tabelle che includono più paragrafi o elenchi all’interno di una cella sono difficili da utilizzare. Per tali contenuti, si consiglia di utilizzare un altro formato, ad esempio intestazioni e testo.

Per ulteriori informazioni sulla creazione di tabelle, vedi:

* Da GitHub, [Organizing information with tables](https://help.github.com/articles/organizing-information-with-tables/)
* La web app [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables)
* [Convertire tabelle HTML in Markdown](https://jmalarcon.github.io/markdowntables/)

### Collegamenti

La sintassi Markdown per un collegamento in linea è costituita dalla porzione `[link text]`, che è il testo che avrà un collegamento ipertestuale, seguita dalla porzione `(file-name.md)`, ovvero l’URL o il nome file al quale verrà effettuato il collegamento:

`[link text](file-name.md)`

```markdown
[Adobe](https://www.adobe.com)
```

Visualizzato:

[Adobe](https://www.adobe.com)

Per i collegamenti agli articoli (rimandi) all’interno dell’archivio, utilizza i collegamenti relativi. Puoi utilizzare tutti gli operandi di collegamento relativo, come ad esempio ./ (directory corrente), ../ (indietro di una directory), e ../../ (indietro di due directory).

```markdown
See [Overview example article](../../overview.md)
```

Per ulteriori informazioni sui collegamenti, consulta l’articolo [Collegamenti](linking.md) di questa guida per la sintassi di collegamento.

### Immagini

```markdown
![Adobe Logo](assets/no-localize/adobe_standard_logo.png "Hover text")
```

Visualizzato:

![Adobe Logo](assets/no-localize/adobe_standard_logo.png "Hover text")

### Blocchi di codice

Markdown supporta il posizionamento di blocchi di codice sia in linea in una frase sia come un blocco separato “delimitato” tra due frasi. Per informazioni, consulta [Supporto nativo dei blocchi di codice di Markdown.](https://daringfireball.net/projects/markdown/syntax#precode)

Utilizza gli apici retroversi (`` ` ``) per creare stili di codice in linea all’interno di un paragrafo. Per creare un blocco di codice specifico su più righe, aggiungi tre apici retroversi (` ``` `) prima e dopo il blocco di codice (denominato “blocco di codice delimitato” in Markdown e semplicemente componente “blocco di codice” in AEM). Per i blocchi di codice delimitati, aggiungi il linguaggio del codice dopo il primo set di apici retroversi affinché la sintassi del codice venga evidenziata correttamente da Markdown. Esempio: ` ```javascript`

Esempi:

```markdown
This is `inline code` within a paragraph of text.
```

Visualizzato:

This is `inline code` within a paragraph of text.

Questo è un blocco di codice delimitato:

```javascript
function test() {
 console.log("notice the blank line before this function?");
```

## Estensioni personalizzate Markdown

Gli articoli Adobe utilizzano Markdown standard per la maggior parte della formattazione degli articoli, come paragrafi, collegamenti, elenchi e intestazioni. Per una formattazione più completa, gli articoli possono utilizzare funzioni estese di Markdown quali:

* Blocchi per le note
* Video incorporati
* Tag di traduzione
* Proprietà dei componenti, ad esempio l’assegnazione di un ID intestazione diverso a un’intestazione e la specifica delle dimensioni immagine

Utilizza il blockquote di Markdown ( > ) all’inizio di ogni riga per collegare un componente esteso, come ad esempio una nota.

Alcuni elementi comuni di Markdown come le intestazioni e i blocchi di codice includono proprietà estese. Se devi modificare le proprietà predefinite, aggiungi i parametri tra parentesi graffe /{ /} dopo il componente. Le proprietà estese vengono descritte nel contesto.

### Blocchi per le note

Per richiamare l’attenzione su contenuti specifici, puoi scegliere tra questi quattro tipi di blocchi per le note:

* `[!NOTE]`
* `[!TIP]`
* `[!IMPORTANT]`
* `[!CAUTION]`
* `[!WARNING]`
* `[!ADMINISTRATION]`
* `[!AVAILABILITY]`
* `[!PREREQUISITES]`

In generale, i blocchi per le note devono essere utilizzati con cautela poiché possono risultare di disturbo. Anche se supportano a loro volta blocchi di codice, immagini, elenchi e collegamenti, prova a mantenere i blocchi per le note semplici e chiari.

```markdown
>[!NOTE]
>
>This is a standard NOTE block.
```

Visualizzato:

>[!NOTE]
>
>This is a standard NOTE block.

```markdown
>[!TIP]
>
>This is a standard tip.
```

Visualizzato:

>[!TIP]
>
>This is a standard tip.

### Video

I video incorporati non vengono renderizzati in modo nativo in Markdown ma puoi utilizzare questa estensione Markdown.

```markdown
>[!VIDEO](https://video.tv.adobe.com/v/29770/?quality=12)
```

Visualizzato:

>[!VIDEO](https://video.tv.adobe.com/v/29770/?quality=12)

### Altri argomenti correlati

Il componente “Altri argomenti correlati” in AEM viene visualizzato alla fine di un articolo. Permette di visualizzare collegamenti correlati. Quando viene eseguito il rendering dell’articolo, questo può essere formattato come intestazione di livello 2 (##) senza essere aggiunto al minisommario.

```markdown
>[!MORELIKETHIS]
>
>* [Article 1](https://helpx.adobe.com/support/analytics.html)
>* [Article 2](https://helpx.adobe.com/support/audience-manager.html)
```

Visualizzato:

>[!MORELIKETHIS]
>
>* [Article 1](https://helpx.adobe.com/it/support/analytics.html)
>* [Article 2](https://helpx.adobe.com/it/support/audience-manager.html)


### UICONTROL e DNL

Tutto il contenuto della guida Markdown viene localizzato inizialmente utilizzando la traduzione automatica. Se la guida non è mai stata localizzata, viene mantenuta la traduzione automatica. Se invece il contenuto della guida è stato localizzato in passato, la traduzione automatica verrà temporaneamente utilizzata come segnaposto finché la traduzione umana non sarà stata finalizzata.

**``**

Durante la traduzione automatica, gli elementi con i tag `` vengono verificati rispetto a un database di localizzazione. Nel caso in cui l’interfaccia utente non sia localizzata, questo tag consentirà al sistema di lasciare il riferimento all’interfaccia utente in inglese per quella particolare lingua (ad es. riferimenti di Analytics in italiano).

**Esempio:**

1. Passa alla schermata **[!UICONTROL Run Process]**.
1. Scegli **[!UICONTROL File > Print > Print All]** per stampare tutti i file sul server.
1. Viene visualizzata la finestra di dialogo [!UICONTROL Processing Rules].

**Origine:**

```markdown
1. Go to the **[!UICONTROL Run Process]** screen.
1. Choose **[!UICONTROL File > Print > Print All]** to print all the files on your server.
1. The [!UICONTROL Processing Rules] dialog box appears.
```

**NOTA:** tra le tre opzioni di assegnazione dei tag, questa è la più importante per offrire un’elevata qualità ed è obbligatoria.

**`[!DNL]`**

Di regola, usiamo un elenco di termini da “Non tradurre” per istruire i motori di traduzione automatica su ciò che mantenere in inglese. Gli elementi più importanti sono ad esempio nomi di soluzioni lunghi, come “Adobe Analytics”, “Adobe Campaign” e “Adobe Target”. Tuttavia, ci possono essere casi in cui è necessario costringere il motore a usare l’inglese perché il termine in questione può essere utilizzato in modo specifico o generale. Il caso più evidente sarebbe quello dei nomi brevi delle soluzioni come “Analytics”, “Campaign”, “Target”, ecc. In questo caso è difficile per una macchina capire che si tratta di nomi di soluzioni e non di termini generici. Il tag può essere utilizzato anche per nomi/funzioni di terze parti che rimangono sempre in inglese o per sezioni più brevi di testo, come un termine o una frase, che devono rimanere in inglese.

**Esempio:**

* Con [!DNL Target], puoi creare test A/B per trovare il metodo ottimale
* Adobe Analytics è una soluzione potente che ti permette di raccogliere dati analitici sul tuo sito. [!DNL Analytics] può anche aiutarti nella generazione di rapporti per utilizzare facilmente tali dati.

**Origine:**

```markdown
* With [!DNL Target], you can create A/B tests to find the optimal 
* Adobe Analytics is a powerful solution to collect analytics on your site. [!DNL Analytics] can also help you with reporting to easily digest that data.
```

## Suggerimenti e risoluzione dei problemi

### Testo alternativo

Il testo alternativo che contiene caratteri di sottolineatura non viene visualizzato correttamente. Ad esempio, invece di utilizzare quanto segue:

```markdown
![Settings_Step_2](/assets/settings_step_2.png)
```

La best practice prevede l’utilizzo dei trattini (-) anziché dei caratteri di sottolineatura (_) nei nomi dei file.

```markdown
![Settings-Step-2](/assets/settings-step-2.png)
```

### Apostrofi e virgolette

Se copi del testo in un editor di Markdown, il testo potrebbe contenere apostrofi o virgolette “intelligenti” (curvi). Questi devono essere codificati o modificati in apostrofi o virgolette semplici. In caso contrario, quando il file viene pubblicato si ottengono caratteri come questi: Itâ€™s

Queste sono le codifiche per le versioni “intelligenti” di tali segni di punteggiatura:

* Virgolette (aperte) a sinistra: `&#8220;`
* Virgolette (chiuse) a destra: `&#8221;`
* Virgoletta singola (chiusa) a destra o apostrofo: `&#8217;`
* Virgoletta singola (aperta) a sinistra (usata raramente): `&#8216;`

### Parentesi acute

Se utilizzi delle parentesi acute nel testo (non nel codice) del file (ad esempio, per indicare un segnaposto) devi codificare manualmente le parentesi acute. In caso contrario, verranno interpretate da Markdown come un tag HTML.

Ad esempio, codificare `<script name>` come `&lt;script name&gt;`

### E commerciale nei titoli

Le e commerciali (&amp;) non sono consentite nei titoli. Utilizza invece “e” oppure la codifica `&amp;`.

## Vedi anche

### Risorse su Markdown

* [Introduzione a Markdown](https://daringfireball.net/projects/markdown/syntax)
* [Nozioni di base su Markdown di GitHub](https://help.github.com/articles/markdown-basics/)
