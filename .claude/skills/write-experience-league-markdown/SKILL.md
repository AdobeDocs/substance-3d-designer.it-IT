---
name: write-experience-league-markdown
description: ""
Source: https://experienceleague.adobe.com/en/docs/contributor/contributor-guide/writing-essentials/markdown
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '628'
ht-degree: 5%

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
`<span id="anchor-id"></span>` esplicito immediatamente prima del termine —
vedere `help/glossary/glossary.md` per il modello utilizzato in questo repository.
* Gli ancoraggi di sezione `TOC.md` utilizzano la sintassi `{#section-id}` dopo un&#39;intestazione o un elenco
etichetta, ad esempio `Getting started{#getting-started}`.

## Immagini

* `![Alt text](path/to/image.png "Optional hover title")`.
* Sono supportati i parametri di query facoltativi di dimensionamento/ottimizzazione:
  `![Adobe logo](assets/logo.png?width=750&format=png&optimize=medium)`.
* **Il testo alternativo non deve contenere caratteri di sottolineatura**. Il rendering non viene eseguito correttamente;
utilizza trattini o spazi.
* Le immagini specifiche della pagina sono disponibili in `<page-name>.resources/`; icone condivise/app
vive in `help/assets/` (vedere CLAUDE.md).

## Tabelle

* Delimitato da pipe, con una riga di separatore dell&#39;intestazione trattino:

  ```markdown
  | Header | Another header | Yet another header |
  |--- |--- |--- |
  | row 1 | column 2 | column 3 |
  | row 2 | row 2 column 2 | row 2 column 3 |
  ```

* Una riga vuota deve precedere la tabella o non verrà visualizzata come tabella.
* Le tabelle non possono contenere in modo pulito contenuto di blocchi complessi o con più paragrafi in un
cella: dove questo repository necessita di immagini/elenchi all&#39;interno di una cella di tabella (ad esempio
tabelle di confronto in `overview.md`), torna a inline HTML
(`<div>`, `<b>`, `<ul>`/`<li>`) con `data-preserve-html="true"` su ciascuno
in modo che la pipeline non lo rimuova. Piuttosto, segui il pattern esistente
che l&#39;invenzione di nuovi HTML in linea, se non necessario.

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

```markdown
>[!VIDEO](https://video.tv.adobe.com/v/29770/?quality=12)
```

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

Vedere la sezione &quot;Page front matter&quot; di CLAUDE.md per il blocco esatto utilizzato da
pagine di contenuto regolare in questo repository e `metadata.md` per il livello di repository
campi ereditati.