---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blurs/median-filter-color.html"
breadcrumb-title: ''
description: Usate il nodo Colore filtro medio per ridurre il disturbo e mantenere i bordi nelle texture di colore.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blurs > Median filter color
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Colore filtro mediano
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 1%

---


# Colore filtro mediano

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Colore filtro mediano: icona](median-filter-color.resources/MedianFilter_Icon_Color.png "Colore filtro mediano: icona")

<b>Ingresso:</b> Filtri > Sfocature

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Questo filtro attenua il disturbo in un’immagine preservando i bordi.

Per ogni pixel, il nodo calcola un valore di colore in base al valore mediano dei pixel adiacenti.

</td>
</tr>
</table>

>[!NOTE]
>
> Vedere anche [Scala di grigi filtro mediana](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/median-filter-grayscale/median-filter-grayscale.md).

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Input</b> <i>Colore</i> | Immagine a colori a cui deve essere applicato il filtro. |

<a name="outputs"></a>

## Output

|  |  |
|:---|:---|
| <b>Output</b> <i>Colore</i> | Immagine a colori calcolata applicando il filtro all&#39;immagine a colori di input. |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Dimensioni kernel</b> *Numero intero* | Un kernel è un gruppo specifico di valori usati nei calcoli di un filtro. In questo contesto, sono i valori dei pixel adiacenti.<br><br>Per ogni pixel, il filtro prende tutti i vicini attorno a quel pixel in un kernel quadrato e calcola il valore mediano di tutti i vicini.<br><br>Questo parametro controlla la dimensione del kernel quadrato, in pixel. Un kernel più grande produce un effetto di arrotondamento più forte e di maggiore portata al costo di alcuni dettagli.<br><br>*- 3x3:* un kernel largo 3 pixel e alto 3 pixel, per un totale di 8 pixel adiacenti.<br>*- 5x5:* un kernel largo 5 pixel e alto 5 pixel, per un totale di 24 pixel adiacenti. |
| <b>Tipo filtro</b> *Numero intero* | Calcolo applicato ai vicini campionati nel kernel.<br><br>*- Mediana:* Utilizzare direttamente il valore mediano di tutti i vicini.<br>*- MLMAD:* sta per &#39;Mediana della deviazione assoluta meno mediana&#39;. La deviazione tiene conto della differenza tra un valore e la mediana. Invece di utilizzare direttamente il valore mediano che può essere inclinato da un pixel outlier con deviazione alta, il metodo MLMAD utilizza la mediana di tutte le deviazioni. Questo metodo produce un effetto di attenuazione più marcato che può appiattire le aree in base alle dimensioni della forma. |
| <b>Influenza sul canale alfa</b> *Booleano* | Determina se il filtro deve essere applicato al canale alfa dell&#39;immagine. Se *è True*, il canale alfa rimane invariato. |

## Esempi

<table>
  <tr>
    <td>
      <img src="median-filter-color.resources/MedianFilter_Variant2A.png" alt="MedianFilter_Variant2A">
      <br><i>Prima</i>
    </td>
    <td>
      <img src="median-filter-color.resources/MedianFilter_Variant2B.png" alt="MedianFilter_Variant2B">
      <br><i>Dopo</i>
    </td>
  </tr>
</table>

<table>
  <tr>
    <td>
      <img src="median-filter-color.resources/MedianFilter_Variant3A.png" alt="MedianFilter_Variant3A">
      <br><i>Prima</i>
    </td>
    <td>
      <img src="median-filter-color.resources/MedianFilter_Variant3B.png" alt="MedianFilter_Variant3B">
      <br><i>Dopo</i>
    </td>
  </tr>
</table>
