---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/modify-color-palette.html"
breadcrumb-title: ''
description: Utilizzare il nodo Modifica tavolozza colori per regolare e Trasforma tavolozze di colori estratte dalla texture.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Modify Color Palette
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Modifica tavolozza colori
user-guide-description: ''
user-guide-title: ''
source-git-commit: 029f702d9b6a4d0dfaa83a4ae8447c02f70be355
workflow-type: tm+mt
source-wordcount: '852'
ht-degree: 0%

---


# Modifica tavolozza colori

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icona Quantizza colore](../../../../../../assets/ModifyColorPalette.png "Icona Quantizza colore"){width="200px"}

<b>Ingresso:</b> Filtri > Regolazioni

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Modifica i colori di una tavolozza ordinata e li applica a un&#39;immagine utilizzando una mappa ID.

È possibile selezionare i colori facendo corrispondere gli indici della mappa ID agli indici dei colori della tavolozza.

Ad esempio, i #2 di colore nella tavolozza verranno applicati a tutti i pixel nella mappa ID con un valore ID pari a 2.

Questo nodo può essere utilizzato in combinazione con i seguenti nodi: [Quantizza colore](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/quantize-color/quantize-color.md), [Crea tavolozza colori](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/create-color-palette-16/create-color-palette-16.md), [Applica tavolozza colori](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/apply-color-palette/apply-color-palette.md), [Visualizza tavolozza colori](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/view-color-palette/view-color-palette.md).

</td>
</tr>
</table>

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>ID</b> <i>Scala di grigi</i> PRIMARIO | La mappa dell’ID di input utilizzata per selezionare i colori, al fine di modificarli e distribuirli nell’output.   Una mappa ID è un’immagine in cui i pixel che fanno parte di un intero (ad esempio, una forma) mantengono tutti lo stesso valore di identificazione univoco. In questo caso, il valore è un numero intero.   È possibile produrre una mappa ID utilizzando un nodo [Quantizza colore](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/quantize-color/quantize-color.md). |
| <b>Tavolozza</b> <i>Colore</i> | Un elenco ordinato di colori RGB codificati come una riga di pixel. La tavolozza può contenere un massimo di 256 colori. Tavolozza modificata dal nodo.   Le tavolozze possono essere prodotte con i nodi [Quantizza colore](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/quantize-color/quantize-color.md) o [Crea tavolozza colori](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/create-color-palette-16/create-color-palette-16.md). |

<a name="outputs"></a>

## Output

|  |  |
|:---|:---|
| <b>Output</b> <i>Colore</i> | Risultato della mappatura dei colori nella tavolozza modificata agli indici della mappa ID. |
| <b>Tavolozza</b> <i>Colore</i> | Tavolozza aggiornata a cui sono state applicate le modifiche di colore specificate.   È possibile applicare la tavolozza a un&#39;altra immagine con il nodo [Applica tavolozza colori](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/apply-color-palette/apply-color-palette.md) o visualizzarla con il nodo [Visualizza tavolozza colori](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/view-color-palette/view-color-palette.md). |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Modalità di selezione colore</b> *Numero intero* | Metodo di selezione del colore di destinazione nella tavolozza che deve essere modificato:<ul data-preserve-html="true"> <li data-preserve-html="true"><b>Indice colore:</b> Indice del colore di destinazione</li> <li data-preserve-html="true"><b>Spazio immagine:</b> la posizione nella mappa ID in cui deve essere campionato l&#39;indice. Quando questa modalità è selezionata, nella vista 2D è disponibile un gizmo di posizione che facilita la selezione</li> </ul> |
| <b>Posizione colore</b> *Float2* *Disponibile quando &#39;Modalità selezione colore&#39; è impostato su &#39;Spazio immagine&#39;* | Posizione nella mappa ID in cui deve essere campionato l’indice.   Utilizzate il gizmo nella vista 2D per selezionare facilmente una posizione nell&#39;immagine.   Suggerimento: puoi visualizzare l&#39;immagine quantizzata da cui è stata estratta la mappa ID, quindi selezionare il nodo Modifica tavolozza colori per visualizzare il gizmo. In questo modo la selezione di un colore da modificare è più intuitiva. |
| <b>Indice colore</b> *Numero intero* *Disponibile quando &#39;Modalità selezione colore&#39; è impostato su &#39;Indice colore&#39;* | Indice del colore di destinazione.   I colori della tavolozza vengono ordinati da sinistra a destra e l&#39;indice del primo colore è 0. |
| <b>Pagine affiancate selezione colore</b> *Mobile* | Consente di controllare l’entità della selezione nei colori adiacenti.   I colori sono disposti in un *cubo* in cui larghezza, height e profondità sono una sfumatura in cui ogni componente di un colore aumenta da 0 a 1 (ad esempio rosso, verde e blu in RGB).   Questo parametro consente di regolare la distanza di modifica del colore selezionato nel cubo anche di altri colori, dove 1 rappresenta la larghezza completa del cubo. |
| <b>Contrasto selezione colore</b> *Mobile* | Controlla la sfumatura di decadimento della selezione sui colori adiacenti.   I colori sono disposti in un *cubo* in cui larghezza, height e profondità sono sfumature in cui un componente di un colore aumenta da 0 a 1 (ad esempio rosso, verde e blu in RGB).   Questo parametro regola il decadimento della selezione sugli altri colori del cubo attorno al colore selezionato, dove 0 rappresenta una sfumatura uniforme dal colore selezionato a quello più lontano e 1 rappresenta un taglio da completamente incluso a non incluso. |
| <b>Spazio colore distanza</b> *Numero intero* | I colori sono disposti in un *cubo* in cui larghezza, height e profondità sono sfumature in cui un componente di un colore aumenta da 0 a 1 (ad esempio rosso, verde e blu in RGB).   Questo parametro consente di selezionare lo spazio cromatico utilizzato per distribuire i colori nel cubo, che cambia i colori adiacenti.   Puoi selezionare lo spazio cromatico che si adatta al tuo caso d&#39;uso:<ul data-preserve-html="true"> <li data-preserve-html="true"><b>Lab (Colore):</b> uno spazio colore percettivo standardizzato, che distribuisce i colori in modo tale che quelli più vicini siano effettivamente vicini nel cubo. Questa opzione è indicata per immagini che possono essere visualizzate su schermi.</li> <li data-preserve-html="true"><b>RGB (dati):</b> il colore viene suddiviso in rosso, verde e blu e distribuito direttamente lungo tali assi, ignorando la percezione umana. Questa opzione è indicata per le immagini contenenti dati non elaborati, ad esempio mappe normali.</li> </ul> |
| <b>Modalità</b> *Numero intero* | Metodo di modifica del colore di destinazione:<ul data-preserve-html="true"> <li data-preserve-html="true"><b>Sostituisci colore:</b> sostituisci il colore con un altro</li> <li data-preserve-html="true"><b>HSL:</b> regolate il colore utilizzando scostamenti di tonalità, saturazione e luminosità</li> </ul> |
| <b>Opacità</b> *Mobile* | Controlla l’interpolazione tra i colori originali e quelli modificati, dove 1 significa che il colore modificato sostituisce completamente il colore originale. |
| <b>Sovrascrivi colore</b> *Float3* *Disponibile quando &#39;Modalità&#39; è impostato su &#39;Sovrascrivi colore&#39;* | Specifica il colore che deve sostituire il colore originale. |
| <b>HSL</b> *Float3* *Disponibile quando &#39;Mode&#39; è impostato su &#39;HSL&#39;* | Controlla gli scostamenti di tonalità, saturazione e luminosità applicati al colore originale. |

## Esempi

![Modificare la tavolozza dei colori: Esempio 1](../../../../../../assets/modify_color_palette_example_1.png "Modificare la tavolozza dei colori: Esempio 1"){zoomable="yes"}

![Modificare la tavolozza dei colori: Esempio 2](../../../../../../assets/modify_color_palette_example_3.png "Modificare la tavolozza dei colori: Esempio 2"){zoomable="yes"}

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/modify_color_example_2_before.jpg" alt="modify_color_example_2_before">
      <br><i>Prima</i>
    </td>
    <td>
      <img src="../../../../../../assets/modify_color_example_2_after.jpg" alt="modify_color_example_2_after">
      <br><i>Dopo</i>
    </td>
  </tr>
</table>
