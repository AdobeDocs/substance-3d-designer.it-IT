---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/splatter.html"
breadcrumb-title: ''
description: Usa il nodo Splatter per dispersione le forme tra le texture per creare pattern casuali e dettagli di texture organiche.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Splatter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Schizzo
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 0%

---


# Schizzo

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/splatter.png)

![](../../../../../../assets/splatter-color.png)

## Schizzo (a colori)

**Ingresso:** *Generatori Di Texture**/Pattern*

**Complesso**

</td>
<td style="border: 0;" valign="top">

## Descrizione

Splatter è un generatore di pattern destinato al posizionamento casuale di un input mappa. Dispone di molti controlli per il posizionamento con motivi geometrici ed è più semplice da usare rispetto a [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md). Quest&#39;ultimo può ottenere risultati simili, ma è molto più complesso.

Lo splatter è utile per ottenere rapidamente alcune forme stampate verso il basso, senza bisogno di troppe modifiche.

Tieni presente che i parametri di splatter predefiniti non sembrano affatto casuali: è necessario modificarne alcuni per ottenere la randomizzazione (principalmente i parametri di Disturbo). Tieni inoltre presente che per funzionare è necessario un input mappa.

## Parametri

* **Larghezza dimensione motivo**: *0.0 - 1000.0* Numero di motivi da utilizzare sull&#39;asse X.
* **Height dimensioni pattern**: *0.0 - 1000.0* Numero di pattern da utilizzare sull&#39;asse Y.
* **Rotazione**: *-360,0 - 360,0* Ruota ogni pattern di una quantità impostata.
* **Variazione rotazione**: *0.0 - 360.0* Introduce una rotazione casuale per ogni forma separata.
* **Zoom**: *100.0 - 10000.0* Ridimensiona il risultato finale. Tenete presente che questo rompe la suddivisione in porzioni!
* **Guadagno**: *0.0 - 10.0* Regola il guadagno di fusione di ogni pattern. Le fa risaltare di più.
* **Panning X**: *-100.0 - 100.0* Esegue il panning dell&#39;intero risultato sull&#39;asse X.
* **Panning Y**: *-100.0 - 100.0* Esegue il panning dell&#39;intero risultato sull&#39;asse Y.
* **Disturbo**: *0,0 - 100,0*\
  Sposta le forme a caso.
* **Numero griglia**: *0 - 8* Scorre tra diverse dimensioni della griglia per regolare la scala dei risultati. Mantiene le porzioni.
* **Angolo del disturbo**: *0.0 - 360.0* Controlla l&#39;angolo di spostamento del disturbo.
* **Disturbo casuale**: *Falso/Vero* Rende casuale l&#39;angolo del disturbo, aggiungendo molto più caos.
* **Dimensione motivo**: *5 - 12*
* **Variazione dimensioni**: *0.0 - 100.0* Introduce il ridimensionamento casuale per ogni forma.
* **Filtro input immagine (solo motore > v4)**: *Bilineare + Mipmap, Bilineare, Più vicino* Filtro da applicare all&#39;immagine di input.
* **Livello di output Min**: *0,0 - 1,0* Regolazione del livello minimo in eccesso.
* **Livello di output massimo**: *0,0 - 1,0* Regolazione del livello massimo.
* **Colore sfondo**: *(valore scala di grigio)*Imposta il colore di sfondo in tinta unita.
* **Variazione luminanza**: *0.0 - 1.0 (solo versione in scala di grigi)*Introduce la variazione di luminanza.
* **Variazione colore**: *0.0 - 1.0 (Solo versione a colori)*Introduce la variazione di colore.

## Immagini di esempio

![](../../../../../../assets/splatter-ex.gif)

</td>
</tr>
</table>
