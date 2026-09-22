---
name: write-experience-league-markdown
description: |
  Regole di sintassi, estensioni personalizzate e gotchas per la scrittura di contenuto Markdown pubblicato su Adobe Experience League. Questa competenza è utile per la creazione o la modifica di pagine in help/ in questo repository (o in qualsiasi altro repository di contenuto di Experience League): intestazioni, collegamenti, immagini, tabelle, blocchi di note/avvisi, tag UICONTROL/DNL, incorporamenti video, ancoraggi e insiemi di rendering noti. Fonte: https://experienceleague.adobe.com/en/docs/contributor/contributor-guide/writing-essentials/markdown
source-git-commit: ed17c57a1aa9669a602d4523bdef20cd7d82db75
workflow-type: tm+mt
source-wordcount: '1263'
ht-degree: 4%
---

# Commenti Experience League di scrittura

Experience League esegue il rendering di Markdown aromatizzato con GitHub tramite una pipeline personalizzata
con le proprie estensioni e le query di rendering. GFM standard funziona principalmente, ma
gli elementi seguenti sono specifici dell&#39;Experience League: sbagliano e contengono
o non riesce lint/link-check CI o esegue il rendering in modo errato sul sito live.

## Intestazioni

* Da `#` a `#####` (livelli 1-5). L&#39;argomento principale `title` della pagina è
di fatto livello 0; la prima voce Markdown nel corpo dovrebbe essere un
singolo titolo `# Level 1` corrispondente (o molto simile) al titolo della pagina.
* Non saltare i livelli arbitrariamente; il mini-sommario viene generato dai titoli.

## Formattazione testo

* `**bold**`, `*italic*`, `***bold and italic***`.
* Consente di eliminare i caratteri speciali letterali con una barra rovesciata (`\*`, `\_` e così via).
* Le **e commerciali** in intestazioni/titoli devono essere scritte (`and`) o codificate come
  `&amp;`: un `&` non elaborato in un titolo può interrompere l&#39;analisi.
* **Le parentesi angolari** utilizzate come testo letterale (non HTML reale) devono essere codificate:
  `<placeholder>` → `&lt;placeholder&gt;`.
* **Le virgolette tipografiche** incollate da elaboratori testi devono essere codificate, non lasciate come
caratteri ricci letterali: doppio sinistro `&#8220;`, doppio destro `&#8221;`,
apostrofo/singolo destro `&#8217;`.

## Elenchi

* Elenchi numerati: inizia ogni elemento con `1.` (o `1)`) - GitHub/Experience
I numeri automatici della lega indipendentemente dalle cifre letterali digitate.
* Elenchi puntati: utilizzare `*`, `-` o `+`, ma **non combinare i caratteri punto elenco
nello stesso elenco/documento**.
* La nidificazione dell&#39;elenco `TOC.md` utilizza `+` in modo coerente: seguire i file esistenti
stile di punto elenco invece di introdurne uno diverso.

## Collegamenti

* I rimandi interni devono essere **relativi** Collegamenti Markdown al
file di destinazione `.md`: `[Overview](../../overview.md)`.
* I riferimenti esterni devono essere **URL assoluti**.
* Ancoraggi nelle intestazioni/estensioni di un&#39;altra pagina: aggiungi `#anchor-id`, ad esempio
  `[Mesh](../../glossary/glossary.md#mesh)`.
* Gli ancoraggi interni alla pagina vengono dichiarati come intestazione (con indicazioni automatiche) o come
`<span id="anchor-id"></span>` esplicito (HTML) / `{: #anchor-id}` (Markdown) immediatamente prima del termine —
vedere `help/glossary/glossary.md` per il modello utilizzato in questo repository.
* Gli ancoraggi di sezione `TOC.md` utilizzano la sintassi `{#section-id}` dopo un&#39;intestazione o un elenco
etichetta, ad esempio `Getting started{#getting-started}`.

## Immagini

Usa la sintassi dell&#39;immagine Markdown quando possibile:

```markdown
![Alt text](path/to/image.png "Optional hover text")
```

* Il testo `![...]` è un testo alternativo accessibile obbligatorio. Mantieni la concisione e procedi
non utilizzare caratteri di sottolineatura, ma spazi o trattini.
* Il percorso dell&#39;immagine può essere relativo al file Markdown o relativo alla cartella principale, ad esempio
come `/help/assets/shared-image.png`. Le immagini specifiche della pagina appartengono al
cartella `<page-name>.resources/` di pari livello (ad esempio,
  `<page-name>.resources/image.png`). `help/assets/` è una cartella condivisa legacy;
  non aggiungere nuove immagini specifiche della pagina.
* I parametri facoltativi per le query di immagini possono controllare l&#39;elaborazione CDN:
  `?width=750&format=png&optimize=medium`. Mantieni questi parametri nell’immagine
  URL, prima di qualsiasi blocco di proprietà.
* Aggiungere le proprietà dell&#39;immagine subito dopo la chiusura di `)`:
  `![Alt text](image.png "Hover text"){width="300" align="center"}`.
  `width` è un valore in pixel o una percentuale dell&#39;area di visualizzazione; le immagini vengono ridimensionate
proporzionalmente. I valori di allineamento supportati sono `center` e `right`.
  `valign` non è supportato.
* Usa `modal="regular"` o `zoomable="yes"` per fare clic per ingrandire un&#39;immagine:
  `![Alt text](image.png){width="100" zoomable="yes"}`. Non combinare
  click-to-zoom con un collegamento immagine; il collegamento ipertestuale ha la precedenza.
* Per creare un collegamento immagine a un&#39;altra pagina, contornare l&#39;immagine con un collegamento Markdown:
  `[![Alt text](image.png)](../target/target.md)`.
* Per immagini di grandi dimensioni, fornire almeno 640 pixel di larghezza sorgente quando possibile,
non utilizzare più di circa 2000 pixel se non necessario e mantenere i file di immagine sotto
5 MB se possibile. La pipeline accetta file fino a 100 MB, ma oltre
20 MB non superano la convalida e gli articoli non devono contenere più di
100 immagini (alcune guide più vecchie indicano 200; utilizzate il limite più rigido).

Usa HTML solo quando Markdown non è in grado di esprimere il layout richiesto, ad esempio
una tabella speciale o una presentazione in linea personalizzata. Modulo di immagine HTML supportato
è:

```html
<img src="image.png" alt="Alt text" />
```

* Fornisci sempre un attributo `alt` significativo e utilizza un relativo o
`src` relativo alla radice coerente con le immagini Markdown.
* Per le immagini HTML all’interno di HTML in linea conservato, aggiungete
  `data-preserve-html="true"` ai tag che li contengono quando richiesto dal
  markup circostante. Ad esempio:

  ```html
  <div data-preserve-html="true" align="center">
    <img src="my-page.resources/preview.gif" alt="Preview" />
  </div>
  ```

* Per attivare il clic per lo zoom di un’immagine HTML, utilizzare
  `class="modal-image"` sul tag `<img>`.
* Non utilizzare attributi HTML non supportati o affidarsi a `valign`; preferisci Markdown
proprietà per la larghezza e l&#39;allineamento.

## Tabelle

Preferisci tabelle Markdown native per contenuto tabulare ordinario:

```markdown
| Header | Another header | Yet another header |
|--- |--- |--- |
| row 1 | column 2 | column 3 |
| row 2 | row 2 column 2 | row 2 column 3 |
```

* Inserite una riga vuota prima della tabella. Le tabelle di markdown richiedono almeno una
riga di intestazione e riga di corpo; utilizzare una tabella HTML per una riga singola o senza intestazione
tabella.
* Utilizzare almeno tre trattini in ogni cella del separatore di intestazione e mantenere lo stesso
numero di caratteri pipe in ogni riga. Esc di una pipe letterale come `\|` o
  `&vert;`.
* Se necessario, utilizzate i marcatori di allineamento nella riga del separatore:
  `|---|:---:|---:|` per l&#39;allineamento sinistro, centrale e destro.
* Il HTML in linea è supportato nelle celle della tabella Markdown per le interruzioni di paragrafo e
elenchi di base. Utilizzare `<p>` per paragrafi separati, `<br>` per interruzioni di riga e
  `<ul>`/`<ol>` con `<li>` elementi per gli elenchi. Aggiungi
  `data-preserve-html="true"` agli elementi HTML in linea quando richiesto dal
  markup del repository.

  ```markdown
  | Header | Details |
  |---|---|
  | Text | First paragraph.<p>Second paragraph.<br>New line.<ul><li>Item</li></ul> |
  ```

* Evitate tabelle molto larghe e molto alte; sono difficili da navigare.
Prestare attenzione con il codice in linea nelle tabelle perché il codice lungo può forzare
larghezze sproporzionate delle colonne.
* Per scegliere il layout di tabella per una tabella Markdown, aggiungere la proprietà dopo
tabella, separata da una riga vuota:

  ```markdown
  {style="table-layout:fixed"}
  ```

  Usa `table-layout:auto` (impostazione predefinita) quando il testo o il codice lungo richiede flessibilità
  larghezze delle colonne. Utilizzare `fixed` per le colonne bilanciate, ad esempio le tabelle contenenti
  immagini di dimensioni simili.

Utilizzare una tabella HTML quando non è possibile esprimere la struttura richiesta, ad esempio
omissione di intestazioni, combinazione di celle con estensioni, bilanciamento di colonne o allineamento
contenuto nelle celle:

```html
<table style="table-layout:fixed">
  <tr>
    <th>Property</th>
    <th>Value</th>
  </tr>
  <tr>
    <td align="center">Example</td>
    <td>Details</td>
  </tr>
</table>
```

* Gli elementi della tabella supportati includono `<table>`, `<tbody>`, `<thead>`, `<tfoot>`,
  `<tr>`, `<th>`, `<td>`, `<col>` e `<colgroup>`, oltre a supportati
elementi in linea come `<p>`, `<br>`, `<b>`, `<i>`, `<ul>`, `<ol>` e
  `<li>`.
* Non utilizzare la sintassi di Markdown all&#39;interno di una tabella HTML. Ad esempio, Markdown
note, immagini e collegamenti possono essere riprodotti letteralmente; utilizzare la sintassi HTML.
  I tag di localizzazione `UICONTROL` e `DNL` sono eccezioni.
* Usa `align="left"`, `align="center"` o `align="right"` in una cella quando
necessario. Le tabelle HTML non possono contenere tabelle nidificate.
* Impostare il layout della tabella HTML sul tag di apertura:
  `<table style="table-layout:auto">` o
  `<table style="table-layout:fixed">`.
* Per una tabella HTML senza bordi di una riga, utilizzare
  `<tr style="border: 0;">`.

## Codice

* Codice in linea: singoli segni di spunta.
* Blocchi recintati: triplo backtick, con un linguaggio opzionale per la sintassi
evidenziazione (` ```python `, ` ```javascript ` e così via).

## Blocchi note/avvisi

Sintassi delle virgolette di blocco personalizzata, un tipo per blocco, una riga vuota tra
tag e corpo:

```markdown
>[!NOTE]
>
>This is a standard NOTE block.

>[!TIP]
>
>This is a standard TIP.

>[!IMPORTANT]
>
>This is an IMPORTANT note.
```

Tipi supportati: `NOTE`, `TIP`, `IMPORTANT`, `CAUTION`, `WARNING`,
`ADMINISTRATION`, `AVAILABILITY`, `PREREQUISITES`, `ERROR`, `INFO`, `SUCCESS`.

## Incorporamenti video

L&#39;Experience League non supporta incorporazioni dirette di video MP4 o YouTube nei blocchi `[!VIDEO]`. Se è necessaria un&#39;anteprima animata, utilizzare un GIF nella cartella `.resources` di pari livello della pagina e centrarlo con HTML in linea, se necessario.

```markdown
<div data-preserve-html="true" align="center">
  <img src="my-page.resources/my-preview.gif" alt="My preview" />
</div>
```

Non utilizzare `[!VIDEO]` per file MP4 locali, file MP4 remoti o URL YouTube. La pipeline di pubblicazione li rifiuta e l&#39;interfaccia utente non riesce.

## Tag UICONTROL

Inserisce i nomi degli elementi dell&#39;interfaccia utente (etichette di pulsanti, voci di menu, nomi di campi) nella riga in modo da
la pipeline di localizzazione è in grado di verificare la presenza di una stringa tradotta e non
torna all&#39;etichetta inglese se non ne esiste nessuna:

```markdown
Click [!UICONTROL Save] to apply changes.
Go to [!UICONTROL Tools] > [!UICONTROL Settings].
```

Utilizzalo per ogni etichetta letterale dell&#39;interfaccia utente a cui si fa riferimento nel testo informativo (menu
elementi, nomi dei pulsanti, titoli delle finestre di dialogo, nomi dei pannelli).

## Tag DNL (&quot;Non localizzare&quot;)

Contorna con nomi di prodotti, nomi di funzionalità di terze parti o qualsiasi frase che deve
non tradurre mai in automatico:

```markdown
Use [!DNL Adobe Analytics] to track metrics.
The [!DNL Target] implementation requires configuration.
```

In questo repository, utilizzalo per nomi di prodotti come `[!DNL Substance 3D Designer]`,
`[!DNL Substance 3D Sampler]`, ecc., nella prima/principali citazioni per pagina,
coerente con le pagine esistenti.

## HTML agganciato

HTML non elaborato consentito. Il repository `markdownlint_custom.json` disabilita MD033
specifico per questo motivo) ma viene conservato in modo affidabile solo attraverso
pipeline quando i tag contengono `data-preserve-html="true"`. Impegna HTML in linea
per i casi in cui il markdown normale non può esprimere (immagini/elenchi all’interno di celle di tabella,
`<span id="...">`) anziché come sostituto generale di Markdown.

## Fattore anteriore

Vedere la sezione &quot;Page front matter&quot; di AGENTS.md per il blocco esatto utilizzato da
pagine di contenuto regolare in questo repository e `metadata.md` per il livello di repository
campi ereditati.