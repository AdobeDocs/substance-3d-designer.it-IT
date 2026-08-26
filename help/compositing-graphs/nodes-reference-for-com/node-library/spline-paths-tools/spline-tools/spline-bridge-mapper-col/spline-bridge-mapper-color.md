---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-bridge-mapper-color.html"
breadcrumb-title: ''
description: Utilizzate il nodo Colore di Mappatura ponti spline per collegare le texture tra due spline con la mappatura dei colori.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Bridge Mapper Color
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Colore mapping spline bridge
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 0%

---


# Colore mapping spline bridge

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icona nodo](../../../../../../assets/spline-bridge-mapper-color-icon.png "Icona nodo")

<b>In:</b> Strumenti Spline E Tracciati > Strumenti spline

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Esegue la mappatura di un&#39;immagine a colori su un elenco di spline di input in modo che l&#39;immagine attraversi le spline in ordine.

</td>
</tr>
</table>

>[!TIP]
>
> La mappatura va dalla prima spline dell&#39;elenco all&#39;ultima e attraversa le spline intermedie seguendo rigorosamente l&#39;ordine di queste spline nell&#39;elenco.
> 
> Pertanto, dovete prestare attenzione all’ordine in cui aggiungete le spline in anticipo.

>[!NOTE]
>
> Vedere anche [Scala di grigi Mappatura ponti spline](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-bridge-mapper-gra/spline-bridge-mapper-grayscale.md).

## Connettori di ingresso

<b>Spline Coords</b> *Colore* Coordinate dei punti delle spline di input codificate nei canali RGBA di un&#39;immagine a colori:\
<b> R</b> - Posizione X\
<b> G</b> - Posizione Y\
<b> B</b> - Height\
<b>A</b> - Dati compressi:\
* Segno: la spline è chiusa (negativa) o aperta (positiva);\
* Valore assoluto: Thickness + 1.

<b>Dati spline</b> *Colore* Dati aggiuntivi delle spline di input codificate nei canali RGBA di un&#39;immagine a colori.\
<b> R</b> - Tangenti X\
<b> G</b> - Tangenti Y\
<b> B</b> - Non in uso\
<b> A</b> - Non in uso

<b>Quantità spline</b> *Numero intero* Numero di spline di input.

<b>Mappa colori </b>*Colore* Immagine a colori di input da mappare sulle spline di input.

## Connettori di uscita

<b>Colore</b> *Scala di grigio* Risultato della mappatura dell&#39;immagine a colori di input sulle spline sullo sfondo, come immagine a colori.

<b>Height</b> *Scala di grigio* Il height delle spline mappato sulle spline, come immagine in scala di grigio.

<b>UV</b> *Colore* UV (coordinate) dell&#39;immagine mappata, codificati nei canali rosso (U) e verde (V) di un&#39;immagine a colori.

<b>Maschera</b> *Scala di grigi* Maschera della mappatura sulle spline.

## Parametri

<b>Importo segmenti</b> *Interi* Le spline vengono semplificate in segmenti prima che le coordinate dell&#39;immagine le attraversino.\
Una maggiore quantità di segmenti determina una mappatura più uniforme lungo le curve.

<b>Riduci dilatazione UV</b> *Booleano* Regola il metodo utilizzato per interpolare le coordinate dell&#39;immagine da una spline all&#39;altra per ridurre al minimo l&#39;allungamento quando la distanza tra le spline è irregolare.

<b>Scala UV</b> *Float2* Regola la scala delle coordinate dell&#39;immagine. Più alti sono i valori, maggiore sarà la densità delle immagini.

<b>Rotazione UV</b> *Mobile* Ruota le coordinate dell&#39;immagine attorno al loro centro.

<b>Colore di sfondo</b> *Float4* Colore dello sfondo nell&#39;immagine di output.

## Esempi

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/SplineBridgeMapperGrayscale-Variant1-Before.jpg" alt="SplineBridgeMapperGrayscale-Variant1-Before">
      <br><i>Prima</i>
    </td>
    <td>
      <img src="../../../../../../assets/SplineBridgeMapperColor-Variant1-After.jpg" alt="SplineBridgeMapperColor-Variant1-After">
      <br><i>Dopo</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

![Esempio di nodo 2](../../../../../../assets/SplineBridgeMapperColor-Demo.gif "Esempio di nodo 2")

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Esempio di nodo 1](../../../../../../assets/SplineBridgeMapperColor-Variant1-After1.jpg "Esempio di nodo 1")

</td>
<td style="border: 0;" valign="top">

![Esempio di nodo 2](../../../../../../assets/SplineBridgeMapperColor-Graph.jpg "Esempio di nodo 2")

</td>
</tr>
</table>
