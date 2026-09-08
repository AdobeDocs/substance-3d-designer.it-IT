---
title: Scala di grigi splatter forma v2 mapper
description: Designer > Substance grafici composizione > Nodi riferimento per i grafici composizione Substance > Libreria nodi > Generatore > Pattern > splatter forma v2 mapper scala di grigi
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '1766'
ht-degree: 0%

---


# Scala di grigi splatter forma v2 mapper

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icona splatter forma v2 mapper scala di grigi](./shape-splatter-v2-mapper-grayscale.resources/shape-splatter-v2-mapper-grayscale.png "Icona splatter forma v2 mapper scala di grigi")

<b>Ingresso:</b> Generatore > Pattern

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Esegue il mapping delle immagini in scala di grigio sulle forme generate e distribuite utilizzando il nodo [splatter di forme v2](../shape-splatter-v2/shape-splatter-v2.md) utilizzando i dati aggiuntivi forniti dal nodo.<br><br>Le immagini vengono fornite come input di pattern separati o inserite in un atlante griglia e possono essere applicate alle forme utilizzando la mappatura UV, la proiezione triplanare o la mappatura personalizzata.<br><br>È possibile colorare le forme e regolarne la luminanza in modo uniforme o casuale in base alla forma.

Vedere anche [Colore di mappatura splatter v2](../shape-splatter-v2-mapper-color/shape-splatter-v2-mapper-color.md) della forma.

</td>
</tr>
</table>

>[!INFO]
>
> Questo nodo richiede dati di input generati dal nodo [splatter forma v2](../shape-splatter-v2/shape-splatter-v2.md).
> 
> Altri nodi nella famiglia di splatter Shape v2:
> * [Splatter forma v2 da mascherare](../shape-splatter-v2-to-mask/shape-splatter-v2-to-mask.md)
>
> I nodi [in scala di grigi Atlanti griglia](../grid-atlas-grayscale/grid-atlas-grayscale.md) consentono di raggruppare le immagini in un atlante di dimensioni personalizzate, fino a 16 pattern in 4*4 celle.

>[!TIP]
> 
> Per iniziare con i nodi Shape splatter v2, è disponibile il materiale [**&#39;Rusty bolts&#39;** sample](../../../../../../function-graphs/nodes-reference-for-fun/function-node-library/function-nodes-sdf-functions/working-with-sdf-functions.md#material-sample).
> 
> Per ulteriori informazioni sui concetti e i flussi di lavoro relativi alla Funzione SDF, consulta la pagina dedicata: [Utilizzo della Funzione SDF](../../../../../../function-graphs/nodes-reference-for-fun/function-node-library/function-nodes-sdf-functions/working-with-sdf-functions.md)

<a name="inputs"></a>

## Input

|                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|:------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <b>Input Atlante griglia</b> *Scala di grigi* | Immagine in scala di grigio di pattern compressi in un layout a griglia.<br><br>La dimensione della griglia deve corrispondere a quella utilizzata dal nodo [splatter forma v2](../shape-splatter-v2/shape-splatter-v2.md) .<br><br>Utilizzare il nodo [scala di grigi Atlanti griglia](../grid-atlas-grayscale/grid-atlas-grayscale.md) per comprimere motivi separati in un atlante griglia. |
| <b>Input pattern 1</b> *Scala di grigi* | L&#39;immagine in scala di grigio per il motivo #1 mappato alle forme.<br><br><i>Suggerimento:</i> Utilizzare una risoluzione vicina alle dimensioni massime consentite per il motivo quando è diffuso. |
| <b>Input pattern 2</b> *Scala di grigi* | L&#39;immagine in scala di grigio per il motivo #2 mappato alle forme.<br><br><i>Suggerimento:</i> Utilizzare una risoluzione vicina alle dimensioni massime consentite per il motivo quando è diffuso. |
| <b>Input pattern 3</b> *Scala di grigi* | L&#39;immagine in scala di grigio per il motivo #3 mappato alle forme.<br><br><i>Suggerimento:</i> Utilizzare una risoluzione vicina alle dimensioni massime consentite per il motivo quando è diffuso. |
| <b>Input pattern 4</b> *Scala di grigi* | L&#39;immagine in scala di grigio per il motivo #4 mappato alle forme.<br><br><i>Suggerimento:</i> Utilizzare una risoluzione vicina alle dimensioni massime consentite per il motivo quando è diffuso. |
| <b>Input pattern 5</b> *Scala di grigi* | L&#39;immagine in scala di grigio per il motivo #5 mappato alle forme.<br><br><i>Suggerimento:</i> Utilizzare una risoluzione vicina alle dimensioni massime consentite per il motivo quando è diffuso. |
| <b>Input pattern 6</b> *Scala di grigi* | L&#39;immagine in scala di grigio per il motivo #6 mappato alle forme.<br><br><i>Suggerimento:</i> Utilizzare una risoluzione vicina alle dimensioni massime consentite per il motivo quando è diffuso. |
| <b>Input pattern 7</b> *Scala di grigi* | L&#39;immagine in scala di grigio per il motivo #7 mappato alle forme.<br><br><i>Suggerimento:</i> Utilizzare una risoluzione vicina alle dimensioni massime consentite per il motivo quando è diffuso. |
| <b>Input pattern 8</b> *Scala di grigi* | L&#39;immagine in scala di grigio per il motivo #8 mappato alle forme.<br><br><i>Suggerimento:</i> Utilizzare una risoluzione vicina alle dimensioni massime consentite per il motivo quando è diffuso. |
| <b>Input in background</b> *Scala di grigi* | Immagine in scala di grigio utilizzata come sfondo per le forme mappate. |
| <b>Input colore</b> *Scala di grigi* | Immagine in scala di grigio utilizzata per colorare le forme mappate in base alla relativa posizione dei punti cardini.<br><br>Utilizzare il parametro <b>Opacità input colore</b> per regolare l&#39;intensità del contributo di questi colori al colore delle forme. |
| <b>Normale</b> *Colore* | Normali calcolati per le forme sparse, mascherati in base alla fusione con il height di sfondo.<br><br> Se il <b>tipo di forma</b> è &#39;Atlante griglia&#39;, vengono utilizzate direttamente le normali fornite all&#39;input <b>Atlante griglia normale</b>. |
| <b>Splatter UVW</b> *Colore* | <b>R</b> - Componente U degli UV delle forme.<br><b>G</b> - Componente V degli UV delle forme.<br><b>B</b> - height delle forme. (W)<br><b>A</b> - Dati compressi:<br> - <i>Parte intera:</i> Identificatore univoco delle forme. (ID)<br> - <i>Parte frazionale:</i> dipende dal <b>Tipo di forma</b>: ID materiale se SDF/primitivo, ID motivo* se input/atlante griglia motivo.<br><br><b>*:</b> L&#39;ID motivo è l&#39;indice della forma nell&#39;elenco/atlas. |
| <b>Dati splatter 1</b> *Colore* | <b>R</b> - Componente X della posizione sulla superficie della forma, nello spazio dell&#39;oggetto.<br><b>G</b> - Componente Y della posizione sulla superficie della forma, nello spazio dell&#39;oggetto.<br><b>B</b> - Componente Z della posizione sulla superficie della forma, nello spazio dell&#39;oggetto.<br><b>A</b> - Dati compressi:<br> - <i>Parte intera:</i> Componente U delle coordinate UV per i dati delle forme negli output dei dati 2/3.<br> - <i>Parte frazionale:</i> V componente delle coordinate UV per i dati delle forme negli output dei dati 2/3.<br> - <i>Firma:</i> Maschera binaria per la fusione delle forme con il height di sfondo. |
| <b>Dati splatter 2</b> *Colore* | <b>R</b> - Componente X della rotazione 3D delle forme.<br><b>G</b> - Componente Y della rotazione 3D delle forme.<br><b>B</b> - Componente Z della rotazione 3D delle forme.<br><b>A</b> - Rotazione delle forme attorno alla normale.<br><br>Tutte le rotazioni sono definite in numero di giri. |
| <b>Dati splatter 3</b> *Colore* | <b>R</b> - Componente X della posizione delle forme.<br><b>G</b> - Componente Y della posizione delle forme.<br><b>B</b> - Scostamento delle forme lungo la normale.<br><b>A</b> - Dati compressi:<br> - <i>Parte intera:</i> ID della forma.<br> - <i>Parte frazionaria:</i>Indice del pattern delle forme nel relativo atlas di origine. (Se si utilizza un tipo di pattern atlante griglia) |
| <b>Dati splatter 4</b> *Colore* | <i>Pixel 1</i><br><b>R</b> - Dimensioni X delle immagini di output Data 2/3.<br><b>G</b> - Dimensioni Y delle immagini di output Data 2/3.<br><b>B</b> - Dimensioni X dell&#39;immagine di output Data 4.<br><b>A</b> - Dimensioni Y dell&#39;immagine di output Data 4.<br><br><i>Pixel 2</i><br><b>R</b> - Tipo di forma. (E.g. Cubo, cilindro, ...)<br><b>G</b> - Dati compressi:<br> - <i>Valore assoluto:</i> Numero di input del pattern.<br> - <i>Firma:</i> Formato normale della mappa normale di output. (Positivo: DirectX / Negativo: OpenGL)<br><b>B</b> - Dimensione X dell&#39;atlante griglia. (ovvero la quantità di colonne)<br><b>A</b> - Dimensione Y dell&#39;atlante griglia. (ovvero l&#39;importo delle righe) |

<a name="outputs"></a>

## Output

|               |                     |
|:--------------|:--------------------|
| <b>Output</b> | Le forme colorate. |

<a name="parameters"></a>

## Parametri

|                                            |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|:-------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <b>Modalità proiezione</b> *Numero intero* | Metodo di proiezione delle immagini di input sulle forme:<br><br>- <b>Dagli UV di splatter:</b> Utilizzare gli UV forniti dal nodo [Splatter forma v2](../shape-splatter-v2/shape-splatter-v2.md).<br>- <b>Triplanare:</b> Utilizzare la proiezione triplanare per mappare le immagini sugli assi XYZ locali delle forme.<br>- <b>Funzione personalizzata:</b> Creare un grafico di funzioni per definire la mappatura delle immagini sulle forme. |
| <b>Funzione personalizzata</b> *Mobile* | Specifica la luminanza per pixel delle forme come mobile.<br><br>Sono disponibili le seguenti variabili:<br>- <code>shape.position.os</code> (Float3) Posizione della superficie della forma nello spazio dell&#39;oggetto.<br>- <code>shape.position.ws</code> (Float3) Posizione della superficie della forma nello spazio mondo*.<br>- <code>shape.normal.os</code> (Float3) Normali della superficie della forma nello spazio dell&#39;oggetto.<br> - <code>forma.normale.ws</code> (Float3) Normali della superficie della forma nello spazio mondo*.<br>- <code>shape.id</code> (Mobile) Identificatore univoco della forma.<br>- <code>material.id</code> (Mobile) L&#39;ID materiale della superficie della forma, definito dal nodo [splatter forma v2](../shape-splatter-v2/shape-splatter-v2.md).<br><br>*: Lo spazio globale della forma è centrato sul relativo perno e non tiene conto del height della forma. Ciò significa che l&#39;unica differenza con lo spazio dell&#39;oggetto è l&#39;orientamento.<br><br>Se è necessario campionare gli input del nodo [Shape splatter v2 mapper grayscale](shape-splatter-v2-mapper-grayscale.md), è possibile utilizzare questi [slot di input del nodo &#x200B;](../../../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/sampler-nodes/sampler-nodes.md) per campionamento in scala di grigi:<br>- 0: Atlante griglia<br>- 1-8: input del modello 1-8 |
| <b>Contrasto di fusione</b> *Mobile* | Nitidezza delle transizioni tra proiezioni planari, dove 1 significa nessuna sfumatura di dissolvenza. |
| <b>Proiezione immagine</b> *Numero intero* | Quantità di <b>immagini di input del pattern n. </b> distribuite tra le proiezioni planari che contribuiscono alla mappatura triplanare.<br><br>Per coprire tutti i lati di una forma, viene eseguita una proiezione piana anteriore (+) e posteriore (-) su ciascun asse, per un totale di 6 proiezioni.<br><br>- <b>1 immagine:</b> L&#39;input pattern 1 viene utilizzato per tutte le proiezioni planari.<br>- <b>3 immagini:</b> Per la proiezione +/- di ciascun asse viene utilizzato un input pattern separato.<br>- <b>6 immagini:</b> Ogni proiezione utilizza un input pattern separato.<br>- <b>1 immagine per ID materiale:</b> Utilizza un input pattern separato ID, in cui ogni immagine viene utilizzata per tutte le proiezioni planari. |
| <b>Centro di proiezione</b> *Float3* | Sposta la proiezione triplanare per asse nello spazio dell’oggetto.<br><br>L&#39;offset viene applicato all&#39;<i>intero spazio di proiezione</i>, pertanto un offset su un asse influisce sul posizionamento delle texture proiettate sugli <i>altri due</i> assi. |
| <b>Scala di proiezione</b> *Mobile* | Regola la scala delle texture proiettate su <i>tutti gli assi</i> in base al fattore specificato. |
| <b>Modalità di selezione dell&#39;input</b> *Numero intero* | Metodo di selezione delle immagini di input da associare alle forme.<br><br>Il <b>tipo di forma</b> selezionato nel nodo [splatter di forma v2](../shape-splatter-v2/shape-splatter-v2.md) di origine cambia il modo di assegnare le immagini alle forme:<br><br>- <b>Atlante griglia</b> significa che le immagini vengono recuperate nell&#39;&#39;input Atlante griglia&#39; tramite indici di griglia corrispondenti (entrambi gli atlanti devono utilizzare la stessa dimensione della griglia)<br>- <b>input pattern</b> significa che le immagini vengono recuperate negli input &#39;n. input pattern&#39; tramite indici corrispondenti.<br>- <b>Altri tipi di forma:</b> le immagini vengono assegnate dagli indici corrispondenti ID materiale della forma.<br><br>I metodi disponibili per la selezione degli indici sono:<br>- <b>Dai dati dello splatter:</b> Far corrispondere gli indici delle immagini &#39;Numero input pattern&#39; o &#39;input Atlante griglia&#39; agli indici delle forme assegnate dal nodo [Splatter forma v2](../shape-splatter-v2/shape-splatter-v2.md).<br>- <b>Manuale:</b> Utilizzare l&#39;indice specificato dal parametro &#39;Indice immagine&#39;.<br>- <b>Casuale:</b> Utilizzare un indice casuale specificato nell&#39;intervallo tramite il parametro &#39;Random range&#39;. |
| <b>Numero di input del pattern</b> *Numero intero* | Quantità di <b>immagini di input con pattern n. </b> da mappare sulle forme. |
| <b>Indice immagine</b> *Numero intero* | L&#39;indice del pattern di input dal <b>input n. </b> o <b>input Atlante griglia</b> che deve essere mappato sulle forme. |
| <b>Intervallo casuale</b> *Intero2* | Intervallo di indici dall&#39;<b>input motivo n. </b> o <b>input Atlante griglia</b> in cui deve essere selezionato in modo casuale il motivo da mappare sulle forme. |
| <b>Regolazione luminanza</b> *Mobile* | Offset applicato in modo uniforme alla luminanza di tutte le forme. |
| <b>Luminanza casuale</b> *Mobile* | Uno scostamento casuale positivo o negativo applicato alla luminanza delle forme, fino ai valori specificati. |
| <b>Opacità input colore</b> *Mobile* | Intensità del contributo dell&#39;<b>Input colore</b> ai colori delle forme, in base al <b>Metodo fusione input colore</b> selezionato. |
| <b>Metodo fusione input colore</b> *Numero intero* | Operazione di fusione dei colori utilizzata per combinare le immagini di primo piano e di sfondo.<br><br>Queste operazioni sono identiche alle corrispondenti operazioni nel nodo [Fusione](../../../../atomic-nodes/blend/blend.md).<br><br>Modalità disponibili:<br>- <b>Copia</b><br>- <b>Aggiungi (schiarisci lineare)</b><br>- <b>Sottrai</b><br>- <b>Moltiplica</b><br>- <b>Sovrapposizione</b> |
| <b>Modalità Porzione</b> *Numero intero* | Assi lungo i quali deve essere ripetuta la texture:<br> - <b>Nessuna porzione</b><br> - <b>Porzione orizzontale</b><br> - <b>Porzione verticale</b><br> - <b>Porzione orizzontale e verticale</b>: porzione orizzontale e verticale combinata. |
| <b>Affiancamento UV</b> *Mobile* | Regola l&#39;affiancamento globale delle immagini mappate sulle forme<br><br>Con valori più alti si ottengono più ripetizioni. |
| <b>Scala UV</b> *Float2* | Regola la suddivisione in porzioni delle immagini mappate sulle forme in base al fattore specificato, con controlli separati per il ridimensionamento U e V. Valori più alti generano più ripetizioni. |
| <b>Offset UV</b> *Float2* | Applica uno scostamento alla mappatura delle immagini sulle forme, consentendo di regolare con precisione il posizionamento delle immagini sulle forme.<br><br>L&#39;offset viene aggiunto all&#39;<b>offset casuale</b>, se presente. |
| <b>Scostamento casuale</b> *Mobile* | Applica una quantità casuale di scostamento positivo o negativo <i>per forma</i> alla mappatura delle immagini nelle forme, fino al valore specificato.<br><br>L&#39;offset viene aggiunto all&#39;<b>Offset UV</b>, se presente. |

