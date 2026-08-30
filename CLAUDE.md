---
source-git-commit: e44437dcecf30714ffe5274c91135d84a0360aa7
workflow-type: tm+mt
source-wordcount: '633'
ht-degree: 0%

---
# CLAUDE.md

Questo file fornisce indicazioni su Claude Code (claude.ai/code) quando si lavora con il codice in questo repository.

# Documentazione di Substance 3D Designer

Questo repository contiene la documentazione di Substance 3D Designer. Nessun codice applicazione, passaggio di compilazione o gruppo di test. Il repository *è* il contenuto, scritto in Markdown e pubblicato in [Adobe Experience League](https://experienceleague.adobe.com/docs/substance3d-designer.html?lang=en).

# Struttura del repository

* `help/` - tutto il contenuto della documentazione, organizzato in modo da rispecchiare il sommario.
* `help/guide/TOC.md`: il sommario. Ogni voce è un collegamento relativo (basato su `/help/...`) al file Markdown di una pagina. `TOC.md` contiene anche metadati dell&#39;albero della pagina (`user-guide-title`, `breadcrumb-title`, `nudge`, ancoraggi di sezione come `{#section-id}`).
* `help/assets/`: cartella di immagini condivise legacy. I file multimediali specifici della pagina sono ora contenuti in una cartella di pari livello per pagina `<md-file-name>.resources/` (vedere la convenzione Cartella/Sommario di seguito). Solo alcune immagini rimanenti non referenziate da alcuna pagina sono ancora presenti. Inserire nuove immagini nella cartella `.resources` della pagina di utilizzo, non qui.
* `help/glossary/glossary.md`: una singola grande pagina di glossario, organizzata alfabeticamente con estensioni di ancoraggio (`<span id="term"></span>`) utilizzata per il collegamento incrociato tramite `#term` frammenti.
* `metadata.md` - argomento principale a livello di repository (ID cloud/soluzione/prodotto, `git-repo` e così via) ereditato da ogni `TOC.md`. Modificate questa impostazione solo per le modifiche dei metadati a livello di repository; i metadati specifici della pagina appartengono all’ambito della pagina.
* `redirects.csv`, `linkcheckexclude.json`, `markdownlint_custom.json`, `pipeline.opts` — configurazione della pipeline di pubblicazione (reindirizzamenti, eccezioni di controllo dei collegamenti, sostituzioni delle regole lint, opzioni pipeline).
* `fix-image-names.py`: utilità singola che rinomina `help/assets` immagini con suffissi tra parentesi (ad esempio `foo(1).png` → `foo_1.png`) e riscrive ogni riferimento di Markdown in modo che corrisponda. Non fa parte di alcun flusso di lavoro regolare; esegui manualmente solo quando tali nomi file vengono nuovamente visualizzati.

## Convenzione cartella/sommario

Per ogni voce in `help/guide/TOC.md`:
* Esiste una cartella corrispondente in `help/`, che segue la stessa nidificazione del sommario.
* Tale cartella contiene un file Markdown, denominato come versione del titolo della pagina con caratteri kebab.
* Se la pagina contiene file multimediali personalizzati (immagini, GIF, video), si trova in una sottocartella di pari livello denominata `<md-file-name>.resources`.

Quando si aggiunge o si sposta una pagina, aggiornare `TOC.md` e il layout della cartella insieme, in quanto devono rimanere sincronizzati.

## Pagine di riferimento dei nodi

Gli alberi della libreria di nodi (ad esempio `help/compositing-graphs/nodes-reference-for-com/node-library/<category>/<node>/<node>.md`) sono un tipo di pagina distinto con layout coerente: una tabella di HTML icon/description, seguita da `## Inputs` / `## Outputs` / `## Parameters` tabelle ancorate (`#inputs`/`#outputs`/`#parameters`) e una raccolta `## Examples`. Utilizzano il **minimo** argomento (solo `title` + `description`), non il normale blocco di pagina contenuto sottostante, modellato su `.../texture-generators/patterns/shape-splatter-v2/shape-splatter-v2.md`. I file multimediali incorporati (icona, immagini/GIF di esempio) si trovano in una cartella di pari livello `<node-name>.resources/` accanto alla pagina, a cui viene fatto riferimento in modo relativo. Utilizza l’abilità `generate-node-documentation` (se presente) per il modello di authoring completo.

## Frontespizio pagina

Le pagine di contenuto normale utilizzano un blocco di argomento principale come:

```yaml
---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/<section>/<page>.html"
breadcrumb-title: ""
description: <one/two sentence SEO description>
helpx_creative_field: ""
helpx_description: Designer > <Section> > <Page>
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: <Page title>
user-guide-description: ""
user-guide-title: ""
---
```

Mantieni `description` preciso e conciso: viene utilizzato per frammenti di ricerca SEO/Search.

# Regole di authoring del contenuto

* L&#39;inglese è la fonte della verità; tutte le altre lingue sono tradotte da esso.
* Tutti i collegamenti ad altre pagine della documentazione devono essere collegamenti **relativi**; tutti i collegamenti a risorse esterne devono essere collegamenti **assoluti**.
* Il contenuto è scritto in Markdown aromatizzato con GitHub con estensioni/gotcha personalizzate di Experience League, documentate [qui](https://experienceleague.adobe.com/en/docs/contributor/contributor-guide/writing-essentials/markdown). Utilizza l&#39;abilità `write-experience-league-markdown` (se presente) per le specifiche.
* Ogni modifica inviata viene sottoposta a controlli lint automatici e convalida dei collegamenti in CI (vedere di seguito). Controllare `markdownlint_custom.json` e `linkcheckexclude.json` prima di presumere che si applichi una regola o che un collegamento debba essere corretto.

# Convalida/CI

* `.github/workflows/validate-articles.yml` viene eseguito su PR e viene inviato a `main` (e tramite un commento PR di `retest`), chiamando il flusso di lavoro condiviso `Adobe-Enterprise-Docs/workflows` riutilizzabile per collegare Markdown e convalidare i collegamenti. Non esiste uno script locale equivalente in questo repo — CI è la fonte di verità per pass/fail.
* `.github/workflows/mirror.yml` esegue il mirroring di `main` nel repository pubblico al push. Si tratta di un&#39;infrastruttura, non di un elemento che deve essere modificato dal contenuto.
* `markdownlint_custom.json` estende il set di regole `markdownlint.json` condiviso e disabilita diverse regole (MD005, MD007, MD018, MD032, MD033, MD034, MD037, MD040) che sono in conflitto con le estensioni Markdown personalizzate di Experience League (ad esempio HTML in linea, enfasi non standard). Non &quot;correggere&quot; il contenuto in base a queste regole disabilitate.
* `linkcheckexclude.json` whitelist i pattern di collegamento (attualmente `example.com`/`example-end.com`) che il controllo collegamenti dovrebbe ignorare.

# Convenzioni di lavoro

* Documentazione pesante per le note sulla versione: le note sulla versione sono disponibili in `help/release-notes/`, una cartella per versione (ad esempio `version-16-0`), più `all-changes` e `old-versions` pagine di aggregazione. Quando aggiungi una nuova versione, segui la cartella delle versioni esistente come modello.
