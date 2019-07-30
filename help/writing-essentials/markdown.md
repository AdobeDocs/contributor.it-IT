---
lastModified: '2018-06-28'
title: Come utilizzare Markdown per la scrittura della documentazione
seo-title: Come utilizzare Markdown per la scrittura della documentazione di Adobe
description: Il presente articolo fornisce nozioni di base e informazioni di riferimento per il linguaggio Markdown utilizzato per scrivere gli articoli.
seo-description: Il presente articolo fornisce nozioni di base e informazioni di riferimento per il linguaggio Markdown utilizzato per scrivere gli articoli per la documentazione di Adobe.
translation-type: ht
source-git-commit: e7382ef4aefc69c6b4e7d78b7f34eaf897596eaf

---


# Come utilizzare Markdown per la scrittura della documentazione tecnica

Gli articoli della documentazione tecnica di Adobe sono scritti in un linguaggio di markup leggero chiamato [Markdown](https://daringfireball.net/projects/markdown/), facile da leggere e da apprendere.

Poiché il contenuto dei documenti Adobe viene archiviato in GitHub, è possibile utilizzare una versione di Markdown denominata [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), che offre funzionalità aggiuntive per le esigenze di formattazione comuni. Inoltre, Adobe ha esteso Markdown in diversi modi per supportare determinate funzionalità relative alla Guida, come note, suggerimenti e video incorporati.

## Nozioni di base su Markdown

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

<!--
To format superscript (H<sub>2</sub>O) and subscript (e=mc<sup>2</sup>) text:

```markdown
This is subscript H<sub>2</sub>O and superscript e=mc<sup>2</sup>.
```
-->

Per ignorare i caratteri di formattazione di Markdown, utilizza \ prima del carattere:

```markdown
This is not \*italicized\* type.
```

### Elenchi numerati ed elenchi puntati

Per creare degli elenchi numerati, inizia una riga con 1. oppure 1) ma non utilizzare entrambi i formati all’interno dello stesso elenco, altrimenti verrà creato un nuovo elenco. Non è necessario specificare i numeri, che sono gestiti automaticamente da GitHub.

```markdown
1. This is step 1.
1. This is the next step.
1. This is yet another step, the third.
```

Visualizzato:

1. Questo è il passaggio 1.
1. Questo è il passaggio successivo.
1. Questo è un ulteriore passaggio, il terzo.

<!-- markdownlint-disable MD037 -->
Per creare degli elenchi puntati, inizia una riga con \* o - o + ma non combinare i formati all’interno dello stesso elenco (se si combinano i formati, ad esempio \* e \+, viene effettivamente creato un nuovo elenco.)
<!-- markdownlint-disable MD037 -->

```markdown
- First item in an unordered list.
- Another item.
- Here we go again.
```

Visualizzato:

- Primo elemento in un elenco non ordinato.
- Un altro elemento.
- Eccone un altro.

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

1. Configura la tabella e i blocchi di codice.
1. Esegui questo passaggio.

   ![screen](assets/no-localize/adobe_standard_logo.png)
1. Assicurati che la tabella sia simile alla seguente:

   | Ciao | mondo |
   |---|---|
   | Come | stai? |
1. Questo è il quarto passaggio.

   >[!NOTE]
   >
   >Questa è una nota.
1. Esegui un altro passaggio.

### Tabelle

Le tabelle non fanno parte della specifica di base di Markdown ma sono supportate in parte da Adobe. Gli elenchi su più righe in una cella non sono supportati da Markdown. Si consiglia di evitare di utilizzare più righe nelle tabelle. Puoi creare tabelle utilizzando il carattere barra verticale (|) per delineare colonne e righe. I trattini creano l’intestazione di ogni colonna, mentre le barre verticali separano ciascuna colonna. Includi una riga vuota prima della tabella affinché venga riprodotta correttamente.

```markdown
| Header | Another header | Yet another header |
|------------|:---------------:|-----------------------:|
| row 1 | centered column 2 | right-aligned column 3 |
| row 2 | row 2 column 2 | row 2 column 3 |
```

Visualizzato:

| Intestazione | Un’altra intestazione | Ancora un’altra intestazione |
|------------|:---------------:|-----------------------:|
| riga 1 | colonna centrata 2 | colonna allineata a destra 3 |
| riga 2 | riga 2 colonna 2 | riga 2 colonna 3 |

Le tabelle semplici funzionano correttamente in Markdown, mentre le tabelle che includono più paragrafi o elenchi all’interno di una cella sono difficili da utilizzare. Per tali contenuti, si consiglia di utilizzare un altro formato, ad esempio intestazioni e testo.

Per ulteriori informazioni sulla creazione di tabelle, vedi:

- Da GitHub, [Organizing information with tables](https://help.github.com/articles/organizing-information-with-tables/)
- La Web app [Generatore di tabelle Markdown](https://www.tablesgenerator.com/markdown_tables)
- [Conversione di tabelle HTML in Markdown](https://jmalarcon.github.io/markdowntables/)

### Collegamenti

La sintassi Markdown per un collegamento in linea è costituita dalla porzione `[link text]`, che è il testo che avrà un collegamento ipertestuale, seguita dalla porzione `(file-name.md)`, ovvero l’URL o il nome file al quale verrà effettuato il collegamento:

`[link text](file-name.md)`

```markdown
[Adobe](https://www.adobe.com) or <https://www.adobe.com>
```

Visualizzato:

[Adobe](https://www.adobe.com) o <https://www.adobe.com>

Per i collegamenti agli articoli (rimandi) all’interno dell’archivio, utilizza i collegamenti relativi. Puoi utilizzare tutti gli operandi di collegamento relativo, come ad esempio./ (directory corrente), ../ (indietro di una directory), e ../../ (indietro di due directory).

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

Markdown supporta il posizionamento di blocchi di codice sia in linea in una frase sia come un blocco separato “delimitato” tra due frasi. Per informazioni, consulta [Supporto nativo dei blocchi di codice di Markdown](https://daringfireball.net/projects/markdown/syntax#precode)

Utilizza gli apici retroversi ( \` ) per creare stili di codice in linea all’interno di un paragrafo. Per creare un blocco di codice specifico su più righe, aggiungi tre apici retroversi (\`\`\`) prima e dopo il blocco di codice (denominato “blocco di codice delimitato” in Markdown e semplicemente componente “blocco di codice” in AEM). Per i blocchi di codice delimitati, aggiungi il linguaggio del codice dopo il primo insieme di apici retroversi in modo tale che la sintassi del codice venga evidenziata correttamente da Markdown. Esempio: \`\`\`javascript

Esempi:

```markdown
This is `inline code` within a paragraph of text.
```

Visualizzato:

Questo è `inline code` all’interno di un paragrafo di testo.

Questo è un blocco di codice delimitato:

```markdown
\```javascript
function test() {
 console.log("notice the blank line before this function?");
\```
```

Visualizzato:

```javascript
function test() {
 console.log("notice the blank line before this function?");
```

Puoi specificare le proprietà dei blocchi di codice per disattivare i numeri di riga (attivato per impostazione predefinita) o aggiungere un ritorno a capo automatico (disattivato per impostazione predefinita). Utilizza {line-numbers=&quot;no&quot;} e {line-wrap=&quot;yes&quot;}. Queste proprietà sono estensioni personalizzate Markdown.

\`\`\`javascript {line-numbers=&quot;no&quot;}
function test() {
console.log(&quot;notice the blank line before this function?&quot;);
\`\`\`

### Elenchi di definizioni

Un elenco di definizioni è un’estensione di Markdown che supporta il componente Elenco di definizioni in AEM. Un elenco di definizioni è costituito da un termine e dalla relativa definizione.

<!--

```markdown
Frog
: An amphibious green creature. Likes flies.

Cat
: A less amphibious creature than frogs.
```

Displayed:

Frog
: An amphibious green creature. Likes flies.

Cat
: A less amphibious creature than frogs.
--->

#### Osservazioni e commenti

I commenti (osservazioni) non vengono visualizzati negli articoli della guida rivolti al pubblico. Tuttavia, i commenti vengono visualizzati nei file Markdown rivolti al pubblico che gli utenti possono visualizzare e modificare.

## Estensioni personalizzate Markdown

Gli articoli Adobe utilizzano Markdown standard per la maggior parte della formattazione degli articoli, come paragrafi, collegamenti, elenchi e intestazioni. Per una formattazione più completa, gli articoli possono utilizzare funzioni estese di Markdown quali:

- Blocchi per le note
- Video incorporati
- Do not localize
- Proprietà dei componenti, come ad esempio l’assegnazione di un ID intestazione diverso a un’intestazione

Utilizza il block quote di Markdown ( &gt; ) all’inizio di ogni riga per collegare un componente esteso, come ad esempio una nota. Se devi utilizzare dei sottocomponenti all’interno di componenti, aggiungi un ulteriore livello di block quote (&gt;  &gt;) per la sezione di quel sottocomponente. Ad esempio, una NOTA all’interno di una sezione DONOTLOCALIZE deve iniziare con &gt;    &gt;.

Alcuni elementi comuni di Markdown come le intestazioni e i blocchi di codice includono proprietà estese. Se devi modificare le proprietà predefinite, aggiungi i parametri tra parentesi graffe /{ /} dopo il componente. Le proprietà estese vengono descritte nel contesto.

### Blocchi per le note

Puoi scegliere tra quattro tipi di blocchi per le note per attirare l’attenzione su contenuti specifici:

- `[!NOTE]`
- `[!CAUTION]`
- `[!TIP]`
- `[!IMPORTANT]`

In generale, i blocchi per le note devono essere utilizzati con cautela poiché possono risultare di disturbo. Anche se supportano a loro volta blocchi di codice, immagini, elenchi e collegamenti, prova a mantenere i blocchi per le note semplici e chiari.


```markdown
>[!NOTE]
>This is a standard NOTE block.
```

Visualizzato:

>[!NOTE]
>Questo è un blocco per le NOTE standard.

```markdown
>[!TIP]
>This is a standard tip.
```

Visualizzato:

>[!TIP]
>Questo è un suggerimento standard.

### Video

I video incorporati non vengono renderizzati in modo nativo in Markdown ma puoi utilizzare questa estensione Markdown.

```markdown
>[!VIDEO](https://www.youtube.com/watch?v=A0EcD2AxvJE)
```

Visualizzato:

>[!VIDEO](https://www.youtube.com/watch?v=A0EcD2AxvJE)

### Altri argomenti correlati

Il componente “Altri argomenti correlati” in AEM viene visualizzato alla fine di un articolo. Permette di visualizzare collegamenti correlati. Quando viene eseguito il rendering dell’articolo, questo può essere formattato come intestazione di livello 2 (##) senza essere aggiunto al minisommario.

<!--
```markdown
>[!MORE]
>* [Article 1](https://helpx.adobe.com/support/analytics.html)
>* [Article 2](https://helpx.adobe.com/support/audience-manager.html){target="new-window"}
```

Displayed:

>[!MORE]
>* [Article 1](https://helpx.adobe.com/support/analytics.html)
>* [Article 2](https://helpx.adobe.com/support/audience-manager.html){target="new-window"}
-->

### DNL (Do not localize) e UICONTROL

In alcuni casi, è necessario contrassegnare determinate sezioni del contenuto all’interno di un articolo affinché risultino solo in lingua inglese.
Parole, frasi e altri elementi devono essere dichiarati ai sistemi di traduzione, creando la possibilità di gestire un lessico controllato.

Per parole o frasi che non devono essere localizzate, utilizza l’estensione `[!DNL]` per racchiudere la parola o la sezione.

Per gli elementi nell’interfaccia utente e i menu di una soluzione, si utilizza l’estensione ``.

**Esempio:**

In [!DNL Adobe Target] puoi creare i test direttamente su una pagina abilitata per [!DNL Target].

**Origine:**

```markdown
In [!DNL Adobe Target] you can create your tests directly on a [!DNL Target]-enabled page.
```

**Esempio**

Utilizza [!UICONTROL Visual Experience Composer] in [!DNL Target] per creare il test direttamente su una pagina.

**Origine:**

```markdown
Use the [!UICONTROL Visual Experience Composer] in [!DNL Target] to create your test directly on a page.
```

## Suggerimenti e risoluzione dei problemi

### Testo alternativo

Il testo alternativo che contiene caratteri di sottolineatura non viene visualizzato correttamente. Ad esempio, invece di utilizzare quanto segue:

```markdown
![Settings_Step_2] (/assets/settings_step_2.png)
```

La procedura ottimale prevede l’utilizzo dei trattini (-) invece dei caratteri di sottolineatura (_) nei nomi dei file.

```markdown
![Settings-Step-2] (/assets/settings-step-2.png)
```

### Apostrofi e virgolette

Se copi del testo in un editor di Markdown, il testo potrebbe contenere apostrofi o virgolette “intelligenti” (curvi). Questi devono essere codificati o modificati in apostrofi o virgolette semplici. In caso contrario, quando il file viene pubblicato si ottengono caratteri come questi: Itâ€™s

Queste sono le codifiche per le versioni “intelligenti” di tali segni di punteggiatura:

- Virgolette (aperte) a sinistra: `&#8220;`
- Virgolette (chiuse) a destra: `&#8221;`
- Virgoletta singola (chiusa) a destra o apostrofo: `&#8217;`
- Virgoletta singola (aperta) a sinistra (usata raramente): `&#8216;`

### Parentesi acute

Se utilizzi delle parentesi acute nel testo (non nel codice) del file (ad esempio, per indicare un segnaposto) devi codificare manualmente le parentesi acute. In caso contrario, verranno interpretate da Markdown come un tag HTML.

Ad esempio, codificare `<script name>` come `&lt;script name&gt;`

### E commerciale nei titoli

Le e commerciali (&amp;) non sono consentite nei titoli. Utilizza invece “e” oppure la codifica `&amp;`.

## Vedi anche

### Risorse su Markdown

- [Introduzione a Markdown](https://daringfireball.net/projects/markdown/syntax)
- [Nozioni di base su Markdown di GitHub](https://help.github.com/articles/markdown-basics/)
