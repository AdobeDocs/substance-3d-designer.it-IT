---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/text.html"
breadcrumb-title: ''
description: Utilizza il nodo Testo per generare texture di testo con font e stili personalizzabili per creare pattern basati su testo.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Text
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Testo
user-guide-description: ''
user-guide-title: ''
source-git-commit: 8b6f65bd88f3c83bf6682c7bca91615166389a91
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 1%

---


# Testo

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Nodo atomico: Testo](text.resources/comp_text_1.png "Nodo atomico: Testo"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

Il nodo Testo fornisce un modo per inserire il testo creato dall&#39;utente nei grafici. Gli utenti possono anche selezionare impostazioni come Font, Allineamento e rotazione per personalizzare il posizionamento del testo.

Il nodo Testo è molto potente e l&#39;unico modo per inserire facilmente il testo. Può essere un po’ complicato da usare perché il posizionamento avviene sempre su un’area di lavoro quadrata limitata e i font sono basati su un elenco esterno definito dal sistema.

</td>
</tr>
</table>

Sono supportati solo i font Truetype (.ttf) e alcuni font Opentype. Se nell&#39;elenco mancano dei font, probabilmente questo è il motivo. <b>Impossibile esporre i font come parametro.</b>

Quando un grafico che utilizza il testo viene pubblicato per sbsar, il font viene incorporato nel pacchetto, proprio come con le bitmap e altre risorse, per garantire che funzioni in tutti i sistemi e in tutte le applicazioni.

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

## Connettori di uscita

</td>
<td style="border: 0;" valign="top">

### Esempi

</td>
</tr>
</table>

## Parametri

|  |  |
| --- | --- |
| <b>Metodo colore</b> *Booleano* | Alterna tra un’immagine in scala di grigio e un’immagine a colori in output. |
| <b>Testo</b> *Stringa* | Determina la descrizione del testo. |
| <b>Carattere</b> *Stringa* | Risorsa font utilizzata per il rendering del testo. |
| <b>Dimensione font</b> *Mobile* | Dimensione del carattere per il testo in punti. |
| <b>Allineamento</b> *Numero intero* | Consente di impostare l’allineamento del testo a sinistra, al centro (impostazione predefinita) o a destra. |
| <b>Trasformazione</b> *Float4* | Matrice di trasformazione 2x2 applicata al testo sottoposto a rendering. |
| <b>Posizione</b> *Float2* | Posizione del testo nell’immagine di output. |
| <b>Sfondo</b> *Float/Float4* | Il colore di sfondo dell&#39;immagine di output. |
| <b>Colore carattere</b> *Float/Float4* | Colore del testo. |

## Connettori di ingresso

|  |  |
| --- | --- |
| <b>Sfondo</b> *Scala di grigi/Colore* PRIMARIO | Il colore di sfondo dell&#39;immagine di output. |

## Connettori di uscita

|  |  |
| --- | --- |
| <b>Output</b> *Scala di grigi/Colore* |  |

## Esempi

*Disponibile a breve.*
