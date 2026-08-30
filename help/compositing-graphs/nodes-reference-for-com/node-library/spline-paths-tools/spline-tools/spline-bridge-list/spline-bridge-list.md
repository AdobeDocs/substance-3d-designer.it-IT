---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-bridge-list.html"
breadcrumb-title: ''
description: Utilizzare il nodo Elenco ponti spline per creare un ponte tra più spline di un elenco per creare pattern complessi.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Bridge (List)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Spline Bridge (elenco)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '1001'
ht-degree: 0%

---


# Spline Bridge (elenco)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icona nodo](spline-bridge-list.resources/spline-bridge-list-icon.png "Icona nodo")

<b>In:</b> Strumenti Spline E Tracciati > Strumenti spline

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Genera spline che attraversano tutte le spline dell&#39;elenco di input, lungo queste spline.

Le spline generate possono essere lineari (dritte) o quadratiche (curve).

</td>
</tr>
</table>

>[!TIP]
>
> Le spline generate vanno dalla prima spline dell&#39;elenco all&#39;ultima e attraversano le spline intermedie seguendo rigorosamente l&#39;ordine di queste spline nell&#39;elenco.
> 
> Pertanto, dovete prestare attenzione all’ordine in cui aggiungete le spline in anticipo.

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Anteprima</b> <i>Scala di grigi</i> | Anteprima delle spline di input come immagine in scala di grigio. |
| <b>Spline Coords</b> <i>Colore</i> | Coordinate dei punti delle spline di input codificate nei canali RGBA di un&#39;immagine a colori:<br><b>R</b> - Posizione X<br><b>G</b> - Posizione Y<br><b>B</b> - Height<br><b>A</b> - Dati compressi:<br>- Segno: la spline è chiusa (negativa) o aperta (positiva);<br>- Valore assoluto: Thickness + 1. |
| <b>Dati spline</b> <i>Colore</i> | Dati aggiuntivi delle spline di input codificate nei canali RGBA di un&#39;immagine a colori.<br><b>R</b> - Tangenti X<br><b>G</b> - Tangenti Y<br><b>B</b> - Non utilizzati<br><b>A</b> - Non utilizzati |
| <b>Quantità spline</b> <i>Numero intero</i> | Numero di spline di input. |

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
| <b>Quantità spline ponte</b> <i>Numero intero</i> | Numero di spline generate nelle spline di input. |
| <b>Tipo spline bridge</b> <i>Numero intero</i> | Tipo di spline generato:<br><br>- Lineare: una spline nitida che collega spline intermedie con traiettorie rette dall&#39;inizio alla fine;<br>- Bezier quadratico: una spline curva che collega spline intermedie con traiettorie lisce dall&#39;inizio alla fine.<br><br>Nota: per calcolare una spline di Bezier quadratica sono necessarie almeno 3 spline di input. |
| <b>Le spline di input sono chiuse</b> <i>Booleano</i> | Controlla se il primo e l&#39;ultimo punto delle spline di input devono essere elaborati come un singolo punto. Ciò impedisce la duplicazione della prima e dell&#39;ultima spline di attraversamento. |
| <b>Direzione capovolgimento</b> <i>Booleano</i> | Inverte la direzione della spline. |
| <b>Chiudi spline del bridge</b> <i>Booleano</i> | Estende le spline trasversali per riconnetterle alla prima spline dell&#39;elenco di input. |
| <b>Primo scostamento spline ponte</b> <i>Float2</i> | Applica un offset all&#39;inizio di tutte le spline attraversate. Il valore è la lunghezza normalizzata delle spline di input.<br>Le spline generate che soddisfano l&#39;inizio o la fine delle spline attraversate vengono lasciate lì. |
| <b>Ultimo scostamento spline ponte</b> <i>Float2</i> | Applica uno scostamento alla fine di tutte le spline attraversate. Il valore è la lunghezza normalizzata delle spline di input.<br>Le spline generate che soddisfano l&#39;inizio o la fine delle spline attraversate vengono lasciate lì. |
| <b>Intervallo scostamento casuale</b> <i>Numero intero</i> | Distanza massima utilizzata per l&#39;offset casuale applicato alle spline.<br><br>- <i>Spline padre:</i> Viene utilizzata l&#39;intera lunghezza delle spline padre. Può causare sovrapposizioni.<br>- <i>Intervallo:</i> Viene utilizzato l&#39;intervallo tra le spline del bridge. Ciò riduce le sovrapposizioni. Questa distanza diminuisce con l&#39;aumentare della quantità di spline del ponte. |
| <b>Avvia scostamento casuale</b> <i>Mobile</i> | Moltiplicatore per l&#39;offset casuale applicato alla posizione iniziale delle spline del ponte, in cui la distanza massima è specificata dal parametro <b>Intervallo di offset casuale</b>. |
| <b>Fine Scostamento Casuale</b> <i>Mobile</i> | Moltiplicatore per l&#39;offset casuale applicato alla posizione finale delle spline del ponte, in cui la distanza massima è specificata dal parametro <b>Intervallo di offset casuale</b>. |
| <b>Scostamento casuale globale</b> <i>Mobile</i> | Un moltiplicatore per *uguale quantità* di offset casuale applicato su *entrambi* la posizione iniziale e finale delle spline del ponte, in cui la distanza massima è specificata dal parametro <b>Intervallo di offset casuale</b>. |
| <b>Distribuzione uniforme</b> <i>Booleano</i> | Se è impostato su True, i punti delle spline generate vengono distribuiti uniformemente dall&#39;inizio alla fine. |
| <b>Thickness</b> |  |
| <b>Modalità Thickness</b> <i>Numero intero</i> | Metodo di acquisizione del valore thickness per le spline del ponte.<br><br>- <i>Eredita dalle spline padre:</i> Viene utilizzato il thickness delle spline padre nelle posizioni iniziale e finale delle spline del ponte<br>- <i>Ignora:</i> Viene utilizzato il valore arbitrario specificato nel parametro <b>Thickness</b> |
| <b>Thickness</b> <i>Mobile</i> | Valore thickness assoluto applicato alle spline del ponte. |
| <b>Thickness casuale</b> <i>Mobile</i> | Moltiplicatore casuale per il thickness delle spline del bridge, in cui il thickness iniziale a cui viene applicato il moltiplicatore è specificato dal parametro <b>Modalità Thickness</b>. |
| <b>Height</b> |  |
| <b>Modalità Height</b> <i>Numero intero</i> | Metodo di acquisizione del valore height per le spline del ponte.<br><br>- <i>Eredita dalle spline padre:</i> Viene utilizzato il height delle spline padre nelle posizioni iniziale e finale delle spline del ponte<br>- <i>Ignora:</i> Viene utilizzato il valore arbitrario specificato nel parametro <b>Height</b> |
| <b>Scostamento Height</b> <i>Mobile</i> | Quantità di offset applicata al height ereditato dalle spline padre prima che tale height venga applicato alle spline ponte. |
| <b>Height</b> <i>Mobile</i> | Valore height assoluto applicato alle spline del ponte. |
| <b>Height casuale</b> <i>Mobile</i> | Quantità casuale di regolazione al height delle spline del ponte, in cui la regolazione dipende dal parametro selezionato <b>Modalità Height</b>:<br><br>- <i>Eredita dalle spline padre:</i> Il valore è un moltiplicatore per il height ereditato.<br>- <i>Ignora:</i> Il valore è uno scostamento aggiunto al height. |
| <b>Correzione non quadrata</b> <i>Booleano</i> | Regolate le posizioni e il thickness dei punti per mantenere la forma della spline con risoluzioni non quadrate. Questo incide anche sulla distribuzione uniforme. |
| <b>Anteprima</b> |  |
| <b>Mostra helper direzione</b> <i>Booleano</i> | Visualizza un punto all&#39;inizio della spline e una freccia alla fine nell&#39;output di anteprima. |
| <b>Mostra busta Thickness</b> <i>Booleano</i> | Visualizza le linee aggiuntive ai bordi del thickness della spline. |
| <b>Importo segmenti</b> <i>Numero intero</i> | Regola il numero di segmenti utilizzati per disegnare la visualizzazione della spline nell&#39;output di anteprima. Un valore più alto genera una linea più morbida. |
| <b>Thickness (px)</b> <i>Mobile</i> | Regola il thickness della visualizzazione della spline in pixel nell&#39;output di anteprima. |
| <b>Intensità anteprima in background</b> <i>Mobile</i> | Intensità della visualizzazione Anteprima. |

## Esempi

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="spline-bridge-list.resources/SplineBridge-List_Variant1_Before.jpg" alt="SplineBridge-List_Variant1_Before">
      <br><i>Prima</i>
    </td>
    <td>
      <img src="spline-bridge-list.resources/SplineBridge-List_Variant1_After.jpg" alt="SplineBridge-List_Variant1_After">
      <br><i>Dopo</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

![Esempio di nodo 2](spline-bridge-list.resources/SplineBridge-List_Demo.gif "Esempio di nodo 2")

</td>
</tr>
</table>

![Nodo nel grafico](spline-bridge-list.resources/SplineBridge-List_Graph.jpg "Nodo nel grafico")
