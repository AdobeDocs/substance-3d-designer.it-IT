---
name: generate-node-documentation
description: |
  Come creare una pagina di riferimento a nodo di Substance 3D Designer in modo che corrisponda al layout standard utilizzato in Guida/composizione-grafici/nodi-riferimento-per-com/node-library/. Utilizzare questa abilità ogni volta che si crea o si modifica una pagina nodo (descrizione di un nodo, Input, Output, Parametri o Esempi) sotto la struttura della libreria di nodi o le pagine di riferimento del nodo funzione/nodo atomico equivalenti. Include la convenzione cartella/sommario, l'argomento anteriore minimo, la tabella icona/descrizione, le tabelle Input/Output/Parametri ancorate e la raccolta Esempi. Per le regole generali di Adobe Experience League Markdown (didascalie, collegamenti, UICONTROL/DNL, immagini), utilizza l’abilità write-experience-league-markdown; questa abilità copre solo la struttura a pagina nodo. Esempio canonico: help/compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-v2/shape-splatter-v2.md
source-git-commit: ed17c57a1aa9669a602d4523bdef20cd7d82db75
workflow-type: tm+mt
source-wordcount: '976'
ht-degree: 3%
---

# Generazione della documentazione dei nodi

Ogni pagina di riferimento di nodo foglia in questo repository segue una struttura uniforme. Questa
skill è la specifica della struttura. L&#39;esempio canonico, completamente lavorato è
`.../node-library/texture-generators/patterns/shape-splatter-v2/shape-splatter-v2.md` -
in caso di dubbio, aprilo e rifletterlo.

Questa abilità riguarda solo la *struttura* della pagina nodo. Per Experience League base Markdown
(blocchi note/avvisi, collegamenti relativi rispetto a quelli assoluti, UICONTROL/DNL, parametri query immagine,
lint gotchas) segui l’abilità `write-experience-league-markdown`.

## Posizione di una pagina del nodo (cartella/convenzione di sommario)

* Una cartella per nodo, nel percorso categoria/sottocategoria corrispondente, ad esempio
  `.../node-library/<category>/<subcategory>/<node-name>/<node-name>.md`.
* La cartella è denominata come titolo del nodo kebab-case. Contiene **un** file `.md`
con lo stesso nome.
* Tutti i file multimediali incorporati per la pagina (icona, ad esempio immagini, GIF) sono contenuti in un elemento di pari livello **  `<node-name>.resources/` cartella **accanto a `.md` e a cui viene fatto riferimento con un
  percorso relativo (ad esempio `<node-name>.resources/<file>.png`). Non puntare le pagine del nodo a
  la cartella `help/assets/` condivisa, ovvero un modello legacy in fase di eliminazione; nuovo e
  le pagine modificate utilizzano la propria cartella `.resources`.
* Ogni pagina ha una voce corrispondente in `help/guide/TOC.md`. Quando si aggiunge o si sposta un
pagina, aggiorna `TOC.md` e il layout della cartella (vedere la cartella/sommario di AGENTS.md
convenzione).

## Fattore anteriore

Le pagine del nodo utilizzano il blocco **minimo**, solo `title` e uno stile breadcrumb
`description`. (Questo è diverso dai documenti legacy a 11 campi AGENTS.md per
pagine con contenuto normale.)

```yaml
---
title: "Shape splatter v2"
description: "Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Generator > Pattern > Shape splatter v2"
---
```

## Struttura del corpo

Dall’alto verso il basso, tutto ciò che si trova sotto la parte anteriore:

### &#x200B;1. Titolo H1

Un singolo `# <Node title>`, esattamente un H1 per pagina.

### &#x200B;2. Tabella icone/descrizioni

Una tabella HTML, una riga, due celle. La cella sinistra (`33.33%`) contiene l&#39;icona, quindi la
`In:` breadcrumb; la cella destra (`100.00%`) contiene `## Description` e la prosa.

```html
<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![<Node title> icon](<node-name>.resources/<node-name>.png "<Node title>")

<b>In:</b> <Category> &gt; <Subcategory>

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

<Description prose.>

</td>
</tr>
</table>
```

Convenzioni prosa cella descrizione:
* Separare i paragrafi con `<br><br>` (le righe vuote non elaborate all&#39;interno della cella non sono affidabili).
* Enfasi in linea: `<b>…</b>` / `<i>…</i>`.
* I lead-in secondari utilizzano `<i>Note:</i>` / `<i>Tip:</i>` all&#39;inizio della frase.
* Usa `&gt;` per `>` nella riga `In:` (è all&#39;interno di HTML). Prendi la categoria /
nomi di sottocategorie dal nodo stesso; non inventarli.
* Per nodi con più versioni (ad esempio colore/scala di grigi/valore o varianti numerate)
come Celle 1 / Celle 2), aggiungi un paragrafo di descrizione finale che faccia riferimento all&#39;altro
versioni con collegamenti relativi, separate da un&#39;unica interruzione di riga. Esempio: `See also: [Input
grayscale](../input-grayscale/input-grayscale.md), [Input value](../input-value/input-value.md)`.

### &#x200B;3. Callout facoltativi

`>[!INFO]`, `>[!TIP]`, `>[!NOTE]` ecc. Vai **dopo** la tabella delle icone/descrizioni (non
nella cella). Sintassi per l’abilità `write-experience-league-markdown`.

### &#x200B;4. Input

Includi solo se il nodo dispone di segnaposti di input. Precede l&#39;intestazione con un ancoraggio.

```markdown
<a name="inputs"></a>

## Inputs

|  |  |
|:---|:---|
| <b>Background height</b> <i>Grayscale</i> | The base height map in which shapes are scattered.<br><br>The contribution is controlled by the <b>Background input opacity</b> parameter. |
```

* Due colonne, riga di intestazione vuota, allineamento `|:---|:---|`.
* Una riga per input: cella sinistra `<b>Name</b> <i>Type</i>`, cella destra la descrizione.
* Il marcatore di tipo è corsivo HTML — `<i>Type</i>` — non markdown `*Type*`.

### &#x200B;5. Output

Stessa forma degli input, con `<a name="outputs"></a>` + `## Outputs`. Includi solo se
nodo documenti output distinti (molti nodi hanno un unico output implicito e omettono questo
sezione — non inventarne una).

Per gli output multicanale compressi, interrompere i canali con `<br>` e rientrare
punti secondari con `&nbsp;` (vedere le righe &quot;Splatter UVW&quot; / &quot;Dati splatter&quot; nella
riferimento):

```markdown
| <b>Splatter UVW</b> | <b>R</b> - U component of the shapes' UVs.<br><b>G</b> - V component of the shapes' UVs.<br><b>B</b> - The shapes' height. (W)<br><b>A</b> - Packed data:<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- <i>Integer part:</i> The shapes' unique identifier. |
```

### &#x200B;6. Parametri

Stessa forma tabella, con `<a name="parameters"></a>` + `## Parameters`. Ometti tutto
sezione se il nodo non ha parametri (non emettere mai una tabella vuota o un parametro &quot;No&quot;.
linea).

* **Parametri raggruppati**: emette una riga di etichetta di spanning con una cella destra vuota prima del
righe del gruppo:

  ```markdown
  | <b>Positioning</b> |  |
  | <b>Project Input</b> <i>UV Position, World Space Position</i> | Choose whether the projection position is set in 2D/UV or in 3D/World space. |
  ```

* **Valori Enum / Multi-Option**: elenca le opzioni all&#39;interno della cella di descrizione come
  Elenco trattini `<br>`:

  ```markdown
  | <b>Position distribution mode</b> <i>Integer</i> | The method of distributing the shapes:<br><br>- <b>2D grid:</b> A simple uniform grid.<br>- <b>Poisson disc:</b> Randomly offsets grid cells to prevent overlaps.<br>- <b>Uniform:</b> An even distribution of a set number of shapes. |
  ```

### &#x200B;7. Esempi

Includi solo se sono presenti immagini/GIF di esempio. Usare un HTML senza bordi e a layout fisso
tabella della raccolta; un `<td>` per immagine; eseguire il wrapping in un nuovo `<tr>` dopo 3 immagini. Percorsi dei file multimediali
puntare nella cartella `.resources` della pagina. Utilizza un elemento HTML `<img>` per ogni
ad esempio, con `class="modal-image"` in modo che l&#39;immagine pubblicata si apra nello standard
visualizzatore immagini. Specificare un testo `alt` significativo che identifichi il nodo e l&#39;esempio
numero. Non utilizzare la sintassi dell&#39;immagine Markdown in questa raccolta.

```html
## Examples

<table style="table-layout:fixed">
    <tr style="border: 0;">
        <td style="border: 0;">
            <img src="<node-name>.resources/<file>.gif" class="modal-image" alt="<Node title> - Example 1" />
        </td>
        <td style="border: 0;">
            <img src="<node-name>.resources/<file2>.jpg" class="modal-image" alt="<Node title> - Example 2" />
        </td>
    </tr>
</table>
```

Mantieni `style="table-layout:fixed"` e `style="border: 0;"`
gli attributi esattamente come mostrato; non aggiungere bordi, margini o stili di sfondo.
Lascia vuote le celle finali in una riga finale parzialmente riempita
(`<td style="border: 0;"></td>`) anziché eseguire la ridisposizione. Usa l’immagine esistente
ordine e nomi dei file. Se una pagina contiene sottotitoli, conservali come testo `alt`
di aggiungere markup di sottotitoli visibili. Ometti l’intera sezione quando la pagina non contiene
file multimediali di esempio.

## Valori tipo canonico

Riutilizzare la formulazione del tipo del nodo. Valori tipici: `Grayscale`, `Color`, `Integer`,
`Float`, `Float2`, `Float3`, `Float4`, `Integer2`, `Boolean`, `Grayscale Input`,
`Color Input`, `(Color value)`, `(Grayscale value)`. Non inventare o &quot;normalizzare&quot; un tipo
il nodo non viene effettivamente utilizzato.

## Regole delle celle di tabella

* Nessuna nuova riga non elaborata all&#39;interno di una cella di tabella: unire le righe con `<br>` (e `<br><br>` tra
paragrafi).
* L&#39;enfasi all&#39;interno delle celle è `<b>`/`<i>` e il marcatore del tipo è sempre `<i>Type</i>`.
* Rientro dei punti secondari nidificati con `&nbsp;` sequenze.

## Regole / non

* **Non creare** input, output o parametri non disponibili nel nodo. Omettere il
sezione. Non riformulare, riepilogare o eliminare i contenuti tecnici esistenti, ma solo
riformattarlo.
* **Mantieni i collegamenti relativi** alle altre pagine `.md`; collegamenti esterni assoluti.
* **Elimina la grafica precedente** quando si modifica una pagina precedente in questo formato: tag di difficoltà
(`**Simple**` / `**Intermediate**` / `**Complex**`), il `## <Title>`
sottotitolo all&#39;interno della cella icona, frasi stub come &quot;Non ci sono immagini associate a
questa pagina.&quot; e le eventuali tabelle di wrapper/navigazione vuote rimaste da migrazioni precedenti.
* **Un H1** per pagina; le sezioni utilizzano `##` e gli ancoraggi Input/Output/Parametri
(`inputs` / `outputs` / `parameters`) deve precedere le intestazioni in modo da attraversare la pagina
  `#inputs` collegamenti vengono risolti.
* **Mantieni `TOC.md` sincronizzato** quando aggiungi, ridenomini o sposti una pagina.
