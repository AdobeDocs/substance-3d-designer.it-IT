---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-bridge-list.html"
breadcrumb-title: ''
description: Utilizzare il nodo Elenco ponti spline per collegare le texture tra più spline in un elenco per creare pattern complessi.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Bridge (List)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Spline Bridge (elenco)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '987'
ht-degree: 0%

---


# Spline Bridge (elenco)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icona nodo](../../../../../../assets/spline-bridge-list-icon.png "Icona nodo")

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

## Connettori di ingresso

<b>Anteprima</b> *Scala di grigio* Anteprima delle spline di input come immagine in scala di grigio.

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

## Connettori di uscita

<b>Anteprima</b> *Scala di grigi* Anteprima delle spline di output come immagine in scala di grigi.

<b>Spline Coords</b> *Colore* Coordinate dei punti delle spline di output codificate nei canali RGBA di un&#39;immagine a colori.\
<b>R</b> - Posizione X\
<b>G</b> - Posizione Y\
<b>B</b> - Height\
<b>A</b> - Dati compressi:\
* Segno: la spline è chiusa (negativa) o aperta (positiva);\
* Valore assoluto: Thickness + 1.

<b>Dati spline</b> *Colore* Dati aggiuntivi delle spline di output codificate nei canali RGBA di un&#39;immagine a colori.\
<b>R</b> - Tangenti X\
<b>G</b> - Tangenti Y\
<b>B</b> - Non utilizzato\
<b>A</b> - Non in uso

<b>Quantità spline</b> *Numero intero* Numero di spline di output.

## Parametri

<b>Quantità spline ponte</b> *Numero intero* Numero di spline generate nelle spline di input.

<b>Tipo spline bridge</b> *Intero* Tipo di spline generato:
* Lineare: una spline affilata che collega spline intermedie con traiettorie rette dall&#39;inizio alla fine;
* Bezier quadratico: una spline curva che collega spline intermedie con traiettorie lisce dall&#39;inizio alla fine.\
  Nota: per calcolare una spline di Bezier quadratica sono necessarie almeno 3 spline di input.

<b>Le spline di input sono chiuse</b> *Booleano* Controlla se il primo e l&#39;ultimo punto delle spline di input devono essere elaborati come un singolo punto. Ciò impedisce la duplicazione della prima e dell&#39;ultima spline di attraversamento.

<b>Direzione capovolgimento</b> *Booleano* Inverte la direzione della spline.

<b>Chiudi spline del bridge</b> *Booleano* Estende le spline di attraversamento per riconnettersi alla prima spline dell&#39;elenco di input.

<b>Primo scostamento spline ponte </b>*Float2* Applica uno scostamento all&#39;inizio di tutte le spline attraversate. Il valore è la lunghezza normalizzata delle spline di input.\
Le spline generate che soddisfano l&#39;inizio o la fine delle spline attraversate vengono lasciate lì.

<b>Ultimo scostamento spline ponte </b>*Float2*\
Applica uno scostamento alla fine di tutte le spline attraversate. Il valore è la lunghezza normalizzata delle spline di input.\
Le spline generate che soddisfano l&#39;inizio o la fine delle spline attraversate vengono lasciate lì.

<b>Intervallo scostamento casuale</b> *Intero* La distanza massima utilizzata per l&#39;offset casuale applicato sulle spline.\
*- Spline padre:* Viene utilizzata l&#39;intera lunghezza delle spline padre. Può causare sovrapposizioni.\
*- Intervallo:* Viene utilizzato l&#39;intervallo tra le spline del bridge. Ciò riduce le sovrapposizioni. Questa distanza diminuisce con l&#39;aumentare della quantità di spline del ponte.

<b>Avvia scostamento casuale</b> *Mobile* Moltiplicatore per lo scostamento casuale applicato alla posizione iniziale delle spline del ponte, in cui la distanza massima è specificata dal parametro <b>Intervallo scostamento casuale</b>.

<b>Fine Scostamento Casuale</b> *Mobile* Moltiplicatore per lo scostamento casuale applicato alla posizione finale delle spline del ponte, in cui la distanza massima è specificata dal parametro <b>Intervallo scostamento casuale</b>.

<b>Scostamento casuale globale</b> *Mobile* Un moltiplicatore per *uguale quantità* di offset casuale applicato *sia* la posizione iniziale che finale delle spline del ponte, dove la distanza massima è specificata dal parametro <b>Intervallo di offset casuale</b>.

<b>Distribuzione uniforme</b> *Booleano* Se è True, i punti delle spline generate sono equamente distanziati dall&#39;inizio alla fine.

+++Spessore
<b>Modalità Thickness</b> *Intero* Metodo di acquisizione del valore thickness per le spline del ponte.\
*- Eredita dalle spline padre:* Viene utilizzato il thickness delle spline padre nelle posizioni iniziale e finale delle spline ponte\
*- Override:* Viene utilizzato il valore arbitrario specificato nel parametro <b>Thickness</b>

<b>Thickness</b> *Float* Valore thickness assoluto applicato alle spline del ponte.

<b>Thickness casuale</b> *Float* Un moltiplicatore casuale per il thickness delle spline del ponte, in cui il thickness iniziale a cui viene applicato questo moltiplicatore è specificato dal parametro <b>Modalità Thickness</b>.

+++

+++Altezza
<b>Modalità Height</b> *Intero* Metodo di acquisizione del valore height per le spline del ponte.\
*- Eredita dalle spline padre:* Viene utilizzato il height delle spline padre nelle posizioni iniziale e finale delle spline ponte\
*- Override:* Viene utilizzato il valore arbitrario specificato nel parametro <b>Height</b>

<b>Scostamento Height</b> *Mobile* Quantità di offset applicata al height ereditato dalle spline padre, prima che tale height venga applicato alle spline del ponte.

<b>Height</b> *Float* Valore height assoluto applicato alle spline del ponte.

<b>Height casuale</b> *Mobile* Una quantità casuale di regolazione al height delle spline del ponte, dove tale regolazione dipende dal parametro selezionato per la <b>modalità Height</b>:\
*- Eredita dalle spline padre:* Il valore è un moltiplicatore per il height ereditato.\
*- Sostituzione:* Il valore è un offset aggiunto al height.

+++

<b>Correzione Non Quadrata </b>*Booleano*

Regolate le posizioni e il thickness dei punti per mantenere la forma della spline in risoluzioni non quadrate.\
Questo incide anche sulla distribuzione uniforme.

+++Anteprima
<b>Mostra helper direzione</b> *Booleano* Visualizza un punto all&#39;inizio della spline e una freccia alla fine nell&#39;output di anteprima.

<b>Mostra busta Thickness</b> *Booleano*\
Visualizza le linee aggiuntive ai bordi del thickness della spline.

<b>Importo segmenti</b> *Numero intero* Regola il numero di segmenti utilizzati per disegnare la visualizzazione della spline nell&#39;output di anteprima.\
Un valore più alto genera una linea più morbida.

<b>Thickness (px)</b> *Mobile* Regola il thickness della visualizzazione della spline in pixel nell&#39;output di anteprima.

<b>Intensità anteprima in background</b> *Mobile* L&#39;intensità della visualizzazione dell&#39;anteprima.

+++

## Esempi

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/SplineBridge-List_Variant1_Before.jpg" alt="SplineBridge-List_Variant1_Before">
      <br><i>Prima</i>
    </td>
    <td>
      <img src="../../../../../../assets/SplineBridge-List_Variant1_After.jpg" alt="SplineBridge-List_Variant1_After">
      <br><i>Dopo</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

![Esempio di nodo 2](../../../../../../assets/SplineBridge-List_Demo.gif "Esempio di nodo 2")

</td>
</tr>
</table>

![Nodo nel grafico](../../../../../../assets/SplineBridge-List_Graph.jpg "Nodo nel grafico")
