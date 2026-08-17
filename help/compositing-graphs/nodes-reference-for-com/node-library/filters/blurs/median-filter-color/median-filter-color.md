---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blurs/median-filter-color.html"
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
source-git-commit: 27326c60e0247617a8f57554a68c9663934cd2bc
workflow-type: tm+mt
source-wordcount: '333'
ht-degree: 0%

---


# Colore filtro mediano

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Colore filtro mediano: icona](../../../../../../assets/MedianFilter_Icon_Color.png "Colore filtro mediano: icona")

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

## Connettori di ingresso

<b>Immettere </b>*Color* L&#39;immagine a cui deve essere applicato il filtro.

## Connettori di uscita

<b>Output</b> *Colore* Immagine a colori calcolata applicando il filtro all&#39;immagine a colori di input.

## Parametri

<b>Dimensioni kernel</b> *Intero* Un kernel è un gruppo specifico di valori utilizzati nei calcoli di un filtro. In questo contesto, sono i valori dei pixel adiacenti.\
Per ogni pixel, il filtro prende tutti i vicini attorno a quel pixel in un kernel quadrato e calcola il valore mediano di tutti i vicini.\
Questo parametro controlla la dimensione del kernel quadrato, in pixel. Un kernel più grande produce un effetto di arrotondamento più forte e di maggiore portata al costo di alcuni dettagli.\
*- 3x3:* un kernel largo 3 pixel e alto 3 pixel, per un totale di 8 pixel adiacenti.\
*- 5x5:* un kernel largo 5 pixel e alto 5 pixel, per un totale di 24 pixel adiacenti.

<b>Tipo di filtro</b> *Numero intero* Calcolo applicato ai vicini campionati nel kernel.\
*- Mediana:* Utilizzare direttamente il valore mediano di tutti i vicini.\
*- MLMAD:* sta per &#39;Mediana della deviazione assoluta meno mediana&#39;. La deviazione tiene conto della differenza tra un valore e la mediana. Invece di utilizzare direttamente il valore mediano che può essere inclinato da un pixel outlier con deviazione alta, il metodo MLMAD utilizza la mediana di tutte le deviazioni. Questo metodo produce un effetto di attenuazione più marcato che può appiattire le aree in base alle dimensioni della forma.

<b>Influenza alfa</b> *Booleano* Controlla se il filtro deve essere applicato al canale alfa dell&#39;immagine. Se *è True*, il canale alfa rimane invariato.

## Esempi

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/MedianFilter_Variant2A.png" alt="MedianFilter_Variant2A">
      <br><i>Prima</i>
    </td>
    <td>
      <img src="../../../../../../assets/MedianFilter_Variant2B.png" alt="MedianFilter_Variant2B">
      <br><i>Dopo</i>
    </td>
  </tr>
</table>

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/MedianFilter_Variant3A.png" alt="MedianFilter_Variant3A">
      <br><i>Prima</i>
    </td>
    <td>
      <img src="../../../../../../assets/MedianFilter_Variant3B.png" alt="MedianFilter_Variant3B">
      <br><i>Dopo</i>
    </td>
  </tr>
</table>
