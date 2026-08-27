---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-mapper-grayscale.html"
breadcrumb-title: ''
description: Utilizzate il nodo Spline Mapper Scala di grigio per mappare le texture in scala di grigio lungo i tracciati spline con parametri personalizzabili.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Mapper Grayscale
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Mappatura spline in scala di grigi
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '1109'
ht-degree: 0%

---


# Mappatura spline in scala di grigi

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icona nodo](../../../../../../assets/spline-mapper-grayscale-icon.png "Icona nodo")

<b>In:</b> Strumenti Spline E Tracciati > Strumenti spline

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Esegue la mappatura di un&#39;immagine in scala di grigio di input su una forma primitiva allungata lungo le spline di input.

La forma primitiva può essere un piano, un semicilindro o un cilindro. I cilindri possono essere ruotati lungo la spline per deformare di conseguenza l&#39;immagine mappata.

</td>
</tr>
</table>

Il nodo genera l&#39;immagine mappata come immagine in scala di grigio, nonché altre informazioni quali height, UV (ad esempio, coordinate dell&#39;immagine) e una maschera ID per selezionare ciascuna spline mappata in modo indipendente.

>[!IMPORTANT]
>
> Il risultato può includere artefatti indesiderati all&#39;esterno dell&#39;inviluppo della spline quando si utilizzano valori di thickness molto bassi. Questo è un problema noto.

>[!NOTE]
>
> Vedere anche [Spline Mapper Color](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-mapper-color/spline-mapper-color.md).

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

<b>Mappa colori</b> *Scala di grigio* Immagine in scala di grigio di input da mappare lungo le spline di input.

<b>Mappa Height</b> *Scala di grigi* Mappa del height in scala di grigi di input da mappare lungo le spline di input.

<b>Twist curve</b> *Scala di grigi* Immagine che descrive una curva utilizzando i valori della prima riga di pixel.\
Quando il parametro <b>Shape</b> è impostato su *Half-Cylinder* o *Cylinder*, questo input viene utilizzato per controllare la torsione degli UV attorno alla forma. Il suo impatto è controllato utilizzando il parametro <b>Moltiplicatore curva UV torsione</b>.\
La curva fornisce un profilo per la quantità di rotazione lungo la spline, dove il primo pixel della riga è la rotazione all&#39;inizio della spline e l&#39;ultimo è la rotazione alla fine. Il valore in scala di grigi rappresenta un numero di giri.\
È possibile utilizzare un nodo [Curva](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/curve/curve.md) per creare la curva.

## Connettori di uscita

<b>Colore</b> *Scala di grigio* Risultato della mappatura dell&#39;immagine a colori di input sulle spline di input, come immagine in scala di grigio.

<b>Height</b> *Scala di grigio* Risultato della mappatura dell&#39;immagine del Height di input sulle spline di input, come immagine in scala di grigio.

<b>UV</b> *Colore* Gli UV (ovvero le coordinate) della mappatura sulle spline di input, codificati in un&#39;immagine a colori.

<b>ID</b> *Scala di grigio* Maschera di immagini mappate lungo le spline di input, in cui i valori del bianco vengono incrementati di 1 da una spline all&#39;altra in modo che ogni forma possa essere selezionata in modo indipendente.

## Parametri

<b>Importo segmenti</b> *Interi* Le spline vengono semplificate in segmenti prima che le coordinate dell&#39;immagine le attraversino.\
Una maggiore quantità di segmenti determina una mappatura più uniforme lungo le curve.

<b>Scala automatica UV</b> *Booleano* Regola automaticamente la scala delle coordinate in modo da mantenere un&#39;immagine quadrata durante la mappatura lungo le spline.<b></b>

<b>Scala UV</b> *Float2* Regola la scala delle coordinate mappate in X (orizzontale) e Y (verticale).\
Valori più elevati generano un&#39;immagine con suddivisione in porzioni più densa.<b></b>

<b>Modalità</b> *Intero* Metodo di selezione delle spline lungo le quali deve essere mappata l&#39;immagine:\
*- Disegna elenco spline*: vengono utilizzate tutte le spline nell&#39;elenco di input;\
*- Disegna spline singola*: viene utilizzata solo la spline con l&#39;indice specificato;\
*- Disegna intervallo spline*: vengono utilizzate solo le spline incluse nell&#39;intervallo specificato.

<b>Disegna indice spline</b> *Intero* (disponibile quando &quot;Metodo&quot; è impostato su &quot;Disegna spline singola&quot;)Indice della spline lungo la quale deve essere mappata l&#39;immagine.

<b>Disegna intervallo spline</b> *Intero2* (disponibile quando &quot;Metodo&quot; è impostato su &quot;Disegna intervallo spline&quot;)Intervallo di indici per le spline lungo le quali deve essere mappata l&#39;immagine.

<b>Inizio</b> *Mobile* Sposta l&#39;inizio della porzione della spline da mappare.\
Il valore rappresenta la lunghezza normalizzata della spline.

<b>Fine</b> *Mobile* Sposta l&#39;estremità della porzione della spline che deve essere mappata.\
Il valore rappresenta la lunghezza normalizzata della spline.

<b>Modalità Thickness</b> *Numero intero* Metodo di impostazione del thickness dell&#39;immagine mappata:\
*- Manuale*: impostare il thickness in modo esplicito con un valore arbitrario;\
*- Da spline*: utilizzare il thickness della spline.

<b>Thickness</b> *Float* (disponibile quando &quot;Modalità Thickness&quot; è impostato su &quot;Manuale&quot;)Valore arbitrario per il thickness dell&#39;immagine mappata lungo le spline.<b></b>

<b>Moltiplicatore Thickness</b> *Float* (disponibile quando &quot;Modalità Thickness&quot; è impostato su &quot;Da spline&quot;)Moltiplicatore globale per il thickness dell&#39;immagine mappata lungo le spline, quando tale thickness è guidato da quello delle spline.

<b>Forma</b> *Intero* Forma di base utilizzata per mappare le coordinate dell&#39;immagine lungo le spline:\
*- Piano*: coordinate mappate su un piano piatto;\
*- Mezzo cilindro*: le coordinate sono mappate su un semicilindro il cui asse del cerchio di base segue la direzione della spline;\
*- Cilindro*: le coordinate sono mappate su un cilindro il cui asse del cerchio di base segue la direzione della spline.<b></b>

<b>Moltiplicatore Height Cilindro</b> *Float* (disponibile quando &quot;Shape&quot; è impostato su &quot;Half Cylinder&quot; o &quot;Cylinder&quot;)Un moltiplicatore per l’intensità del contributo height del cilindro nell’output del Height.\
Gli adeguamenti di height sono cumulativi.

<b>Scostamento Height cilindro</b> *Mobile* (disponibile quando &quot;Shape&quot; è impostato su &quot;Half Cylinder&quot; o &quot;Cylinder&quot;)\
Sposta il centro del profilo forma Cilindro o Cilindro a metà dalla superficie della spline a un diametro al di sotto della superficie.

<b>Intensità UV torsione</b> *Mobile* (disponibile se &quot;Shape&quot; (Forma) è impostato su &quot;Half Cylinder&quot; (Mezzo cilindro) o &quot;Cylinder&quot; (Cilindro)). La torsione delle coordinate dell&#39;immagine attorno al cilindro, in numero di giri.\
La torsione comporta la rotazione del cilindro solo all&#39;estremità della spline. La rotazione viene quindi interpolata lungo la spline.

<b>Moltiplicatore curva UV torsione</b> *Mobile* (disponibile quando &quot;Shape&quot; è impostato su &quot;Half Cylinder&quot; o &quot;Cylinder&quot;)Un moltiplicatore per l’intensità del contributo dell’input del Twist curve alla torsione del cilindro.\
La curva fornisce un profilo per la quantità di rotazione lungo la spline, dove il primo pixel della riga è la rotazione all&#39;inizio della spline e l&#39;ultimo è la rotazione alla fine. Il valore in scala di grigi rappresenta un numero di giri.

<b>Scostamento curva UV torsione</b> *Mobile* (disponibile quando &quot;Shape&quot; è impostato su &quot;Half Cylinder&quot; o &quot;Cylinder&quot;) Applica uno scostamento globale ai valori di rotazione forniti dal Twist curve, in numero di giri.

<b>Moltiplicatore Height spline</b> *Mobile* Regola l’intensità del contributo dell’input del Height spline all’output del Height.\
Le regolazioni di height sono cumulative.<b></b>

<b>Moltiplicatore Height Di Input</b> *Mobile* Regola l’intensità del contributo dell’input Mappa Height all’output del Height.\
Gli adeguamenti di height sono cumulativi.

<b>Correzione non quadrata </b>*Booleano* Regola le posizioni e il thickness dei punti per mantenere la forma della spline con risoluzioni non quadrate.\
Questo incide anche sulla distribuzione uniforme.

## Esempi

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/SplineMapperColor-Variant1-Before.jpg" alt="SplineMapperColor-Variant1-Before">
      <br><i>Prima</i>
    </td>
    <td>
      <img src="../../../../../../assets/SplineMapperGrayscale-Variant1-After.jpg" alt="SplineMapperGrayscale-Variant1-After">
      <br><i>Dopo</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

![Esempio di nodo 2](../../../../../../assets/SplineMapperGrayscale-Demo.gif "Esempio di nodo 2")

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Esempio di nodo 3](../../../../../../assets/SplineMapperGrayscale-Variant1-After1.jpg "Esempio di nodo 3")

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
