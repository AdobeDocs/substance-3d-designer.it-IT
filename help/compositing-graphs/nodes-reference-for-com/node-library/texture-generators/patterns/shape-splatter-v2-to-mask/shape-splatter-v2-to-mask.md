---
title: Splatter forma v2 a maschera
description: Designer > Substance grafici composizione > Nodi riferimento per Substance grafici composizione > Libreria nodi > Generatore > Pattern > Splatter forme v2 per maschera
source-git-commit: f688c618b01d3ca8059e67cf0797268e44e94b17
workflow-type: tm+mt
source-wordcount: '621'
ht-degree: 0%

---


# Splatter forma v2 a maschera

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icona Schizzo forma v2 in maschera](shape-splatter-v2-to-mask.png "Schizzo forma v2 in maschera")

<b>Ingresso:</b> Generatore > Pattern

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Calcola una maschera da una selezione di forme generate dal nodo [Splatter forma v2](../shape-splatter-v2/shape-splatter-v2.md) .<br><br>Le opzioni disponibili includono la selezione casuale e la selezione di intervalli di forme tramite identificatore univoco e/o ID materiale/ID motivo*.<br><br>Le forme vengono pre-mascherate dal nodo [Splatter forma v2](../shape-splatter-v2/shape-splatter-v2.md) dalla <i>fusione height</i> con il height di sfondo.<br>Sia lo sfondo che le forme non selezionate sono nero puro. (Ovvero un valore di 0)<br><br><b>*:</b> Uno dei valori recuperati dall&#39;input UVW dello splatter di forma è l&#39;ID materiale o l&#39;ID motivo, a seconda del <b>tipo di forma</b> utilizzato nello splatter di forma v2 nodo:<br>- <i>SDF/primitivo</i>: ID materiale<br>- <i>Input/Atlante griglia motivo:</i> ID motivo, ovvero l&#39;indice del motivo nell&#39;elenco/atlas.

</td>
</tr>
</table>

>[!INFO]
>
> Questo nodo richiede dati di input generati dal nodo [splatter forma v2](../shape-splatter-v2/shape-splatter-v2.md).
> 
> Altri nodi nella famiglia di splatter Shape v2:
> * [Scala di grigi splatter forma v2 mapper](../shape-splatter-v2-mapper-grayscale/shape-splatter-v2-mapper-grayscale.md)
> * [Colore dello splatter di forma v2 mapper](../shape-splatter-v2-mapper-color/shape-splatter-v2-mapper-color.md)

>[!TIP]
> 
> Per iniziare con i nodi Shape splatter v2, è disponibile il materiale [**&#39;Rusty bolts&#39;** sample](../../../../../../function-graphs/nodes-reference-for-fun/function-node-library/function-nodes-sdf-functions/working-with-sdf-functions.md#material-sample).
> 
> Per ulteriori informazioni sui concetti e i flussi di lavoro relativi alla Funzione SDF, consulta la pagina dedicata: [Utilizzo della Funzione SDF](../../../../../../function-graphs/nodes-reference-for-fun/function-node-library/function-nodes-sdf-functions/working-with-sdf-functions.md)

<a name="inputs"></a>

## Input

|                             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|:----------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <b>Splatter UVW</b> *Colore* | <b>R</b> - Componente U degli UV delle forme.<br><b>G</b> - Componente V degli UV delle forme.<br><b>B</b> - height delle forme. (W)<br><b>A</b> - Dati compressi:<br> - <i>Parte intera:</i> Identificatore univoco delle forme. (ID)<br> - <i>Parte frazionale:</i> dipende dal <b>Tipo di forma</b>: ID materiale se SDF/primitivo, ID motivo* se input/atlante griglia motivo.<br><br><b>*:</b> L&#39;ID motivo è l&#39;indice della forma nell&#39;elenco/atlas. |

<a name="outputs"></a>

## Output

|               |                                           |
|:--------------|:------------------------------------------|
| <b>Output</b> | Maschera calcolata delle forme selezionate. |

<a name="parameters"></a>

## Parametri

|                                                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|:--------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <b>Output</b> *Numero intero* | I valori utilizzati per le forme selezionate nella maschera di output.<br><br>- <b>Maschera binaria:</b> Tutte le forme selezionate utilizzano un valore di 1.<br>- <b>ID forma (numero intero):</b> Le forme selezionate utilizzano il relativo identificatore univoco. (ID)<br>- <b>ID materiale (numero intero):</b> Le forme selezionate utilizzano il relativo ID materiale.<br>- <b>ID forma (normalizzato):</b> Le forme selezionate utilizzano il relativo identificatore univoco (ID) mappato sull&#39;intervallo [0, 1] compreso tra l&#39;ID selezionato più basso e quello più alto.<br>- <b>ID materiale (normalizzato):</b> Le forme selezionate utilizzano l&#39;ID materiale mappato sull&#39;intervallo [0, 1] compreso tra l&#39;ID materiale selezionato più basso e quello più alto. |
| <b>Intervallo iniziale ID forma</b> *Numero intero* | Identificatore univoco (ID) della forma utilizzato come inizio dell&#39;intervallo di selezione. (Incluso) |
| <b>Intervallo finale ID forma</b> *Numero intero* | Identificatore univoco (ID) della forma utilizzato come fine dell&#39;intervallo di selezione. (Incluso) |
| <b>Offset ID forma</b> *Numero intero* | Sposta gli identificatori univoci delle forme in base al valore specificato, nel contesto dell&#39;intervallo di selezione.<br><br>In questo modo è più semplice spostare la selezione corrente in base al valore specificato senza dover regolare manualmente i limiti iniziale e finale. |
| <b>Combinazione di materiali/ID pattern</b> *Numero intero* | Specificato l&#39;operatore logico utilizzato per combinare la selezione mediante identificatore univoco (ID) con la selezione in base all&#39;ID materiale/ID modello.<br><br>- <b>Nessuno:</b> Ignorare completamente l&#39;ID materiale/ID modello per la selezione.<br>- <b>AND:</b> Le forme selezionate devono essere incluse sia nell&#39;intervallo ID che nell&#39;intervallo ID materiale/ID modello. (Include meno forme)<br>- <b>OR:</b> Le forme selezionate devono essere incluse negli intervalli ID o ID materiale/ID motivo. (Include più forme) |
| <b>Intervallo di inizio materiale/ID pattern</b> *Numero intero* | ID materiale o ID pattern* utilizzato come inizio dell&#39;intervallo di selezione. (Incluso)<br><br><b>*:</b> Per informazioni dettagliate, vedere la descrizione del nodo. |
| <b>Intervallo finale ID materiale/modello</b> *Numero intero* | ID materiale o ID pattern* utilizzato come fine dell&#39;intervallo di selezione. (Incluso)<br><br><b>*:</b> Per informazioni dettagliate, vedere la descrizione del nodo. |
| <b>Forma maschera casuale</b> *Mobile* | Fattore per la maschera casuale delle forme, in cui 1 indica che tutte le forme sono mascherate. |

