---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-append.html"
breadcrumb-title: ''
description: Utilizzare il nodo Aggiungi spline per aggiungere più spline insieme per creare tracciati continui più lunghi.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Append
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Aggiungi spline
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '518'
ht-degree: 0%

---


# Aggiungi spline

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icona nodo](spline-append.resources/spline-append-01.png "Icona nodo")

<b>In:</b> Strumenti Spline E Tracciati > Strumenti spline

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Le spline sono confezionate come un elenco. Questo nodo aggiunge un elenco di spline di input (set #2) a un elenco esistente (set #1).

L&#39;ordine degli elenchi viene mantenuto, il che significa che l&#39;aggiunta di un elenco D-E-F a un elenco A-B-C dà come risultato un elenco A-B-C-D-E-F.

</td>
</tr>
</table>

>[!TIP]
>
> Prestare attenzione all&#39;ordine in cui vengono aggiunte le spline, in quanto tale ordine viene preso in considerazione in altri nodi, ad esempio [Dispersione sulle spline](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/scatter-on-spline-color/scatter-on-spline-color.md), [Spline Bridge](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-bridge-list/spline-bridge-list.md) e così via.

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Anteprima #1</b> <i>Scala di grigi</i> | Anteprima del primo set di spline di input come immagine in scala di grigio. |
| <b>Spline #1 Coords</b> <i>Colore</i> | Coordinate del primo insieme di punti spline di input codificati nei canali RGBA di un&#39;immagine a colori.<br><b>R</b> - Posizione X<br><b>G</b> - Posizione Y<br><b>B</b> - Height<br><b>A</b> - Dati compressi:<br>- Segno: la spline è chiusa (negativa) o aperta (positiva);<br>- Valore assoluto: Thickness + 1. |
| <b>Dati #1 spline</b> <i>Colore</i> | Dati aggiuntivi del primo set di spline di input codificate nei canali RGBA di un&#39;immagine a colori.<br><b>R</b> - Tangenti X<br><b>G</b> - Tangenti Y<br><b>B</b> - Non utilizzati<br><b>A</b> - Non utilizzati |
| <b>Quantità #1 spline</b> <i>Numero intero</i> | Numero di spline di input nel primo set. |
| <b>Anteprima #2</b> <i>Scala di grigi</i> | Anteprima del secondo set di spline di input come immagine in scala di grigio. |
| <b>Spline #2 Coords</b> <i>Colore</i> | Coordinate del secondo set di punti spline di input codificati nei canali RGBA di un&#39;immagine a colori.<br><b>R</b> - Posizione X<br><b>G</b> - Posizione Y<br><b>B</b> - Height<br><b>A</b> - Dati compressi:<br>- Segno: la spline è chiusa (negativa) o aperta (positiva);<br>- Valore assoluto: Thickness + 1. |
| <b>Dati #2 spline</b> <i>Colore</i> | Dati aggiuntivi del secondo set di spline di input codificati nei canali RGBA di un&#39;immagine a colori.<br><b>R</b> - Tangenti X<br><b>G</b> - Tangenti Y<br><b>B</b> - Non utilizzati<br><b>A</b> - Non utilizzati |
| <b>Quantità #2 spline</b> <i>Numero intero</i> | Numero di spline di input nel secondo set. |

<a name="outputs"></a>

## Output

|  |  |
|:---|:---|
| <b>Anteprima</b> <i>Scala di grigi</i> | Anteprima delle spline di output come immagine in scala di grigio. |
| <b>Spline Coords</b> <i>Colore</i> | Coordinate dei punti delle spline di output codificate nei canali RGBA di un&#39;immagine a colori.<br><b>R</b> - Posizione X<br><b>G</b> - Posizione Y<br><b>B</b> - Height<br><b>A</b> - Dati compressi:<br>- Segno: la spline è chiusa (negativa) o aperta (positiva);<br>- Valore assoluto: Thickness + 1. |
| <b>Dati spline</b> <i>Colore</i> | Dati aggiuntivi delle spline di output codificate nei canali RGBA di un&#39;immagine a colori.<br><b>R</b> - Tangenti X<br><b>G</b> - Tangenti Y<br><b>B</b> - Non usati<br><b>A</b> - Non usati |
| <b>Quantità spline</b> <i>Numero intero</i> | Numero di spline di output. |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Inverti direzione #1 spline</b> <i>Booleano</i> | Inverte la direzione delle spline nel primo insieme. |
| <b>Inverti direzione #2 spline</b> <i>Booleano</i> | Inverte la direzione delle spline nel secondo insieme. |
| <b>Anteprima</b> |  |
| <b>Importo segmenti</b> <i>Numero intero</i> | Regola il numero di segmenti utilizzati per disegnare la visualizzazione della spline nell&#39;output di anteprima. Un valore più alto genera una linea più morbida. |
| <b>Mostra helper direzione</b> <i>Booleano</i> | Visualizza un punto all&#39;inizio della spline e una freccia alla fine nell&#39;output di anteprima. |
| <b>Mostra busta Thickness</b> <i>Booleano</i> | Visualizza le linee aggiuntive ai bordi del thickness della spline. |
| <b>Thickness (px)</b> <i>Mobile</i> | Regola il thickness della visualizzazione della spline in pixel nell&#39;output di anteprima. |

## Esempi

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Esempio di nodo 1](spline-append.resources/spline-append-02.jpg "Esempio di nodo 1")

</td>
<td style="border: 0;" valign="top">

![Esempio di nodo 2](spline-append.resources/spline-append-03.jpg "Esempio di nodo 2")

</td>
</tr>
</table>

![Demo sui nodi](spline-append.resources/spline-append-04.gif "Demo sui nodi")
