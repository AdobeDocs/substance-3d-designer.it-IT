---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/output-size.html"
breadcrumb-title: ''
description: Configura le impostazioni delle dimensioni di output per Substance grafici di composizione per controllare la risoluzione e la qualità delle texture.
helpx_creative_field: ""
helpx_description: Designer > Substance graphs > Output size
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Dimensioni output
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '1006'
ht-degree: 5%

---


# Dimensioni output

Si tratta del primo dei <b>parametri di base</b> di un grafico e, insieme al <b>formato di output</b> (o bitdepth), è fondamentale per la comprensione poiché ha un grande impatto sull&#39;output di un grafico, sia in Designer che in altre applicazioni come file [risorsa Substance 3D pubblicata (SBSAR)](../publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md).

>[!TIP]
>
> Si consiglia vivamente di acquisire una buona conoscenza dell&#39;[ereditarietà nei grafici Substance](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md) come base per l&#39;utilizzo efficiente della proprietà Dimensione output.

>[!NOTE]
>
> Utilizza il pulsante di blocco ![](../../assets/props-output-size-lock.jpg) per fare in modo che il valore Height *corrisponda* al valore della larghezza.

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

## Potenza di 2 valori

Il parametro Dimensione output determina la risoluzione dell&#39;output *texture* da parte di un grafico o di un nodo.

Texture che è un oggetto nel computing grafico vincolato da alcune restrizioni imposte dal modo in cui l&#39;hardware di elaborazione grafica esegue i suoi calcoli. Una di queste restrizioni è che la texture deve rappresentare un&#39;immagine il cui numero di pixel in X e Y è una *potenza di due*.

</td>
<td width="33.33%" style="border: 0;" valign="top">

| Potenza di 2 | Pixel |
| --- | --- |
| 7 | 128 |
| 8 | 256 |
| 9 | 512 |
| 10 | 1024 |
| 11 | 2048 |
| 12 | 4096 |
| 13 | 8192 |

</td>
</tr>
</table>

La proprietà Dimensione output utilizza *passaggi logaritmici* per mappare facilmente gli incrementi di potenza di due (ad esempio, 256, 512, 1024, ...) su una *scala lineare* (ad esempio 8, 9, 10, ...). Ciò significa che l’aumento o la riduzione del valore Dimensione output in X o Y per 1 è simile alla moltiplicazione o divisione della risoluzione corrente per 2.

Questo vale anche quando il valore Dimensione output è controllato da una [funzione](../../function-graphs/function-graphs.md), in cui la funzione deve generare i valori logaritmici di destinazione (relativi o assoluti) invece della risoluzione di destinazione.

>[!IMPORTANT]
>
> Aumentando o diminuendo la risoluzione sia in X che in Y, il numero di pixel viene moltiplicato o diviso per *4*, con un impatto significativo sulle *prestazioni* e sull&#39;*ingombro di memoria* di un grafico.\
> Pertanto, si consiglia vivamente di utilizzare la *risoluzione minima* effettivamente necessaria per ottenere il risultato desiderato. Tenere sotto controllo le risoluzioni è una delle [linee guida per l&#39;ottimizzazione delle prestazioni](../../best-practices/performance-optimization/performance-optimization-guidelines.md).

>[!NOTE]
>
> In [Grafici a funzione](../../function-graphs/function-graphs.md), le `$size` e `$sizelog2` [variabili di sistema](../../function-graphs/variables/system-variables/system-variables.md) restituiscono un valore Float2 corrispondente alla risoluzione corrente del nodo o del grafico, rispettivamente come un numero di pixel non elaborati o una potenza di due.\
> Ad esempio, per un&#39;immagine 1024\*512, `$size` restituisce `(1024,512)` mentre `$sizelog2` restituisce `(10,9)`.

## Dimensioni relative

Quando la proprietà Dimensione output utilizza un *Relativo a...* [metodo di ereditarietà](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md), il relativo valore viene espresso come modificatore *relativamente al valore logaritmico ereditato*.

Modificatori relativi all’intervallo di risoluzione ereditato compreso tra -12 e +12 su una scala logaritmica; il valore predefinito è 0. Questo significa che ogni passaggio sopra o sotto comporta il raddoppio o il dimezzamento della risoluzione. La tabella a destra fornisce un esempio di come la risoluzione relativa cambia in una dimensione per un valore ereditato di 9 (ovvero, 512 = 2^9) e 11 (ovvero, 2048 = 2^11):

Al di sopra di 8196, la dimensione è *limitata*. Questo limite è controllato dall&#39;impostazione <b>Limite dimensione cottura</b> nella sezione <b>Generali</b> delle [Preferenze](../../interface/preferences-window/preferences-window.md). Notate che lavorare con risoluzioni molto elevate comporta un costo delle prestazioni proporzionale e un ingombro di memoria esponenziale. Inoltre, i limiti nell’elaborazione grafica pongono un limite rigido alla dimensione massima di una texture.

| -5 | -4 | -3 | -2 | -1 | 0 | +1 | +2 | +3 | +4 | +5 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 16 | 32 | 64 | 128 | 256 | <b>512</b> | 1024 | 2048 | 4096 | 8196 | 8196 |
| 64 | 128 | 256 | 512 | 1024 | <b>2048</b> | 4096 | 8196 | 8196 | 8196 | 8196 |

>[!NOTE]
>
> Al di sotto di 16 la risoluzione ha un limite di *non*, ma non è consigliabile abbassarla, in quanto non vi sono miglioramenti delle prestazioni al di sotto di tale soglia. Al contrario, le prestazioni in realtà *diminuiscono* a causa dell&#39;implementazione specifica del <b>motore di Substance</b>. Pertanto, utilizzare 16x16 come risoluzione minima generale nei grafici a Substance.

## Modifica del metodo di ereditarietà

Nella maggior parte dei casi, il [metodo di ereditarietà](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md) predefinito per la proprietà Dimensione output è il seguente, a seconda dell&#39;elemento:

* Grafico: *relativo all&#39;elemento padre*
* Nodo: *Rispetto all&#39;input* - In questo caso vengono utilizzati i valori ereditati dall&#39;[input primario](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md) del nodo
* Nodo [Bitmap](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md): *Assoluto*. Per ulteriori informazioni, vedere la pagina [Risorsa bitmap](../../resources/bitmap-resource/bitmap-resource.md) e le [linee guida per l&#39;ottimizzazione delle prestazioni](../../best-practices/performance-optimization/performance-optimization-guidelines.md)

Visualizzare le proprietà di un nodo o di un grafico facendo clic sull&#39;elemento, quindi nel pannello [Proprietà](../../interface/properties/properties.md) individuare la proprietà <b>Dimensione output</b> nella sezione <b>Parametri di base</b>. Fare clic sul menu a discesa del metodo di ereditarietà per selezionare il metodo di ereditarietà desiderato.

![Metodo di ereditarietà delle dimensioni di output](../../assets/change-mode.gif "Metodo di ereditarietà delle dimensioni di output"){width="512px"}

## Problemi di esempio

Se sei un nuovo utente di [Adobe Substance 3D Designer](https://www.adobe.com/it/products/substance3d-designer.html), potresti riscontrare alcuni problemi comuni. Di seguito sono riportati alcuni esempi e alcune soluzioni.

+++Problema 1
**![(errore)](../../assets/error.svg) Problema**

![Esempio di problema 1](../../assets/problem2-bad.png "Esempio di problema 1")



L&#39;impostazione **Dimensione principale** è *disattivata* e il grafico utilizza una risoluzione indesiderata di 256\*256.

Nelle proprietà del grafico, il metodo di ereditarietà della proprietà Dimensione output è stato impostato su *Assoluto*, che interrompe l&#39;ereditarietà a favore di un valore arbitrario.

**![(tick)](../../assets/check.svg) Soluzione**

![Esempio di problema 1 Soluzione](../../assets/problem2-good.png "Esempio di problema 1 Soluzione")



Imposta il metodo di ereditarietà per le dimensioni di output del grafico su *Rispetto all&#39;elemento padre*.

+++

+++Problema 2
**![(errore)](../../assets/error.svg) Problema**

![Esempio di problema 2](../../assets/problem1-bad.png "Esempio di problema 2")



Sopra si vede un caso in cui l&#39;output di un grafico risulta in una risoluzione diversa (512\*512) rispetto a quella impostata nell&#39;elemento padre (1024\* 1024), nonostante il grafico sia impostato su *Rispetto all&#39;elemento padre*.

Il problema deriva dal nodo [Bitmap](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md). Per impostazione predefinita, viene utilizzato il metodo di ereditarietà *Assoluto* e selezionato 512\*512 come risoluzione basata sulla [risorsa Bitmap](../../resources/bitmap-resource/bitmap-resource.md). Il nodo connesso è impostato su *Rispetto all&#39;input*, quindi eredita le dimensioni di output dal nodo Bitmap.

**![(tick)](../../assets/check.svg) Soluzione**

![Esempio di problema 2 Soluzione](../../assets/problem1-good.png "Esempio di problema 2 Soluzione")



Impostate il metodo di ereditarietà delle dimensioni di output del nodo Bitmap su *Rispetto all&#39;elemento padre*, risolvendo il problema più avanti nella catena.

+++

+++Problema 3
**![(errore)](../../assets/error.svg) Problema**

![Esempio di problema 3](../../assets/problem3-bad.png "Esempio di problema 3")



Sopra vedete un problema in cui la risoluzione salta molto più in alto a metà della catena, risultando in una risoluzione di output molto più alta di quella definita dall&#39;elemento principale.

Il problema è causato da un modificatore relativo di 3 sul nodo [Trasformazione 2D](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/transformation-2d/transformation-2d.md), che rende l&#39;output 8 volte più grande.

**![(tick)](../../assets/check.svg) Soluzione**

![Esempio di problema 3 Soluzione](../../assets/problem3-good.png "Esempio di problema 3 Soluzione")



Impostate i modificatori relativi per Larghezza e Height su 0, senza che si verifichi alcun aumento di scala.

+++
