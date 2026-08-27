---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/curve.html"
breadcrumb-title: ''
description: Utilizza il nodo Curva per regolare i valori della texture utilizzando curve personalizzabili per un controllo preciso del colore e della luminosità.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Curve
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Curva
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '619'
ht-degree: 2%

---


# Curva

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Nodo atomico: curva](../../../../assets/comp_curve_1.png "Nodo atomico: curva"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

Modifica i valori di un’immagine utilizzando una curva personalizzata.

Il nodo fornisce un&#39;interfaccia per la modifica della tonalità dell&#39;immagine, simile ad altre applicazioni di modifica delle immagini 2D. L&#39;utente può posizionare punti e regolare le curve di Bezier per rimappare l&#39;input, che può essere in scala di grigio o a colori.È particolarmente utile quando viene utilizzato con le transizioni di sfumatura per rimapparle a un profilo di height specifico, in quanto consente di modellare con estrema precisione i profili di smusso e simili.

</td>
</tr>
</table>

A differenza della maggior parte degli altri nodi, il nodo Curva non dispone di un&#39;interfaccia standard tipica con cursori e parametri, ma presenta invece un editor di curve completo. Vedere la sezione espandibile riportata di seguito su come utilizzarlo.

[Ciò significa tuttavia che nessuno dei parametri di un nodo Curva può essere esposto a un grafico secondario](../../../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md). L&#39;unica opzione disponibile è quella di utilizzare un [switch multiplo](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blending/multi-switch/multi-switch.md) per passare da un profilo di curva all&#39;altro.

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">



</td>
<td width="83.33%" style="border: 0;" valign="top">



</td>
<td width="100.00%" style="border: 0;" valign="top">



</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Parametri

### Editor curva

</td>
<td style="border: 0;" valign="top">

### Connettori di ingresso

### Connettori di uscita

</td>
<td style="border: 0;" valign="top">

### Esempi

</td>
</tr>
</table>

## Parametri

|  |  |
| --- | --- |
| <b>Applica/Esporta curva</b> *Booleano* | Consente di copiare la curva utente nell&#39;output invece di applicarla all&#39;immagine di input |
| <b>Indirizzamento della curva</b> *Booleano* | Questo parametro determina il modo in cui vengono gestiti i pixel HDR fuori dall’intervallo [0, 1] nell’input: bloccati o piegati fino a [0, 1]. |
| <b>Curva</b> *Matrice di chiavi di curva* | Curva personalizzata utilizzata per mappare i valori in scala di grigio di input.   Può essere modificato utilizzando l&#39;[editor curva](#curve-editor). |

## Editor curva

### Creare e spostare un punto

Per creare un punto, fate doppio clic in un punto qualsiasi della vista Curva:

![](../../../../assets/createmovepoint.gif)

### Controllo dell&#39;influenza di un punto

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

Per ottenere risultati precisi, i nodi della curva offrono diverse modalità per ciascun punto:

</td>
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../assets/image2017-2-17-14-5-36.png)

</td>
</tr>
</table>

![](../../../../assets/image2017-2-17-14-13-27.png) Reimpostare la modalità punto sul valore predefinito.

![](../../../../assets/image2017-2-17-14-12-6.png) Bloccare e sbloccare i due gestori Bezier in modo che l&#39;utente possa spostarli insieme o in modo indipendente.

![](../../../../assets/image2017-2-17-14-14-0.png) Entrambi i lati del punto sono controllati da un gestore di Bezier.

![](../../../../assets/image2017-2-17-14-16-22.png) Il lato destro del punto è controllato da un gestore di Bezier mentre il lato sinistro rimane piatto.

![](../../../../assets/image2017-2-17-14-18-25.png) Il lato sinistro del punto è controllato da un gestore di Bezier mentre il lato destro rimane piatto.

![](../../../../assets/image2017-2-17-14-19-32.png) I lati dei punti rimangono piatti

![](../../../../assets/curvepointsmodes.gif)

### Mostra istogramma di input

Puoi mostrare/nascondere l&#39;istogramma del tuo input semplicemente facendo clic su ![](../../../../assets/image2017-2-17-14-50-13.png)

![](../../../../assets/image2017-2-17-14-48-35.png)

### Controllo individuale di ciascun canale (input colore)

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

Quando immettete è un nodo di colore, potete regolare la curva per ciascun canale:

Seleziona la curva da regolare nell’elenco a discesa in alto a destra:

</td>
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../assets/image2017-2-17-14-52-43.png)

</td>
</tr>
</table>

Nella modalità Curva RGB puoi nascondere/mostrare le singole curve dei canali premendo/depremendo ![](../../../../assets/image2017-2-17-14-55-0.png):

![](../../../../assets/image2017-2-17-14-55-38.png)

### Allineamento, specchiatura e capovolgimento

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

Se fate clic con il pulsante destro del mouse sulla vista curva, verranno visualizzate altre opzioni.

<b>Allinea in alto:</b> Allinea orizzontalmente i punti selezionati a quello più alto.

<b>Allinea al centro:</b> Allinea orizzontalmente i punti selezionati al height medio della selezione.

<b>Allinea in basso:</b> Allinea orizzontalmente i punti selezionati con quello più basso.

</td>
<td width="50.00%" style="border: 0;" valign="top">

![](../../../../assets/image2017-6-27-16-11-9.png)

</td>
</tr>
</table>

<b>Distribuisci orizzontalmente/verticalmente:</b> Distribuisci i punti sull&#39;asse selezionato

<b>Capovolgi in orizzontale/verticale:</b> capovolgi i punti selezionati in base all&#39;asse selezionato.

<b>Specchiatura orizzontale/verticale:</b> Specchiatura dell&#39;intera curva, in base all&#39;asse selezionato

### Scelte rapide da tastiera

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<b>LMB + Trascina</b>

Disegnate una casella di selezione.

</td>
<td style="border: 0;" valign="top">

![](../../../../assets/ctrl.gif)

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<b>Maiusc + Trascina</b>

Vincola lo spostamento sull’asse X o Y.

</td>
<td style="border: 0;" valign="top">

![](../../../../assets/shift.gif)

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<b>Alt + LMB + Trascina</b>

Interrompi temporaneamente le maniglie per spostarle in modo indipendente.

</td>
<td style="border: 0;" valign="top">

![](../../../../assets/altclick.gif)

</td>
</tr>
</table>

### Regolare l’inquadratura della curva

Durante l’ottimizzazione dei gestori, potreste trovarvi in un caso in cui un gestore si trova sopra la vista curva.

In tal caso, è possibile utilizzare il pulsante ![](../../../../assets/image2017-2-20-19-11-53.png) per adattare le dimensioni al contenuto.

Il pulsante ![](../../../../assets/image2017-2-20-19-12-45.png) ripristina il livello di zoom su 1

![](../../../../assets/viewzoom.gif)

## Connettori di ingresso

|  |  |
| --- | --- |
| <b>Input</b> *Scala di grigi/Colore* PRIMARIO | Immagine da elaborare. |

## Connettori di uscita

|  |  |
| --- | --- |
| <b>Output</b> *Scala di grigi/Colore* |  |

## Esempi

*Disponibile a breve.*
