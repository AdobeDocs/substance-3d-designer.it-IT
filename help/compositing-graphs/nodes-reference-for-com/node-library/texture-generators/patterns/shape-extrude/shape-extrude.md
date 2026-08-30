---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/shape-extrude.html"
breadcrumb-title: ''
description: Usate il nodo Estrusione forma per estrarre le forme e creare effetti di profondità 3D nelle texture di Substance 3D Designer.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Shape Extrude
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Estrusione forma
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '457'
ht-degree: 5%

---


# Estrusione forma

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](shape-extrude.resources/shape-extrude.png){width="128px"}

<b>Ingresso:</b> Generatori Texture > Pattern

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Nodo avanzato che consente il rendering degli input di &quot;forme&quot; binari 2D su mappe di altezza ruotate in 3D. Funziona in modo simile a un&#39;estrusione in un pacchetto 3D in cui una forma viene estrusa lungo il suo asse, creando un volume. In combinazione con la maschera Sfumatura profilo, è possibile creare anche corpi di tipo rivoluzione/tornio. Molto utile per creare forme artistiche complesse per le mappe altezza.

</td>
</tr>
</table>

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Input forma estrusione</b> <i>Input scala di grigi</i> | Se Extrude Shape è impostato su Custom, inserire qui la propria maschera di forma binaria (preferibilmente). |
| <b>Sfumatura profilo</b> <i>Input scala di grigi</i> | Se Tipo profilo è impostato su Sfumatura verticale, può essere utilizzato per definire la scala della forma lungo l&#39;asse, per i corpi di rivoluzione. |
| <b>Maschera profilo</b> <i>Input scala di grigi</i> | Slot maschera utilizzato per nascondere o mostrare la forma estrusa lungo il suo asse. Può essere utilizzato per interrompere la continuità della forma lungo il suo asse. Interpretato solo come binario: i valori put della scala di grigi vengono arrotondati a 0 o 1. |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Estrusione Height</b> <i>0.0 - 1.0</i> | Entità per l&#39;estrusione della forma dal centro verso l&#39;alto. |
| <b>Estrusione Profondità</b> <i>0.0 - 1.0</i> | Entità per l&#39;estrusione della forma in base ai livelli inferiori dal centro. |
| <b>Estrusione forma</b> <i>Cubo, Cilindro, Input personalizzato</i> | Utilizza forme incorporate o inserisci una forma personalizzata esternamente. |
| <b>Dimensioni forma estrusione</b> <i>0.0 - 1.0</i> | Utilizzato solo con Cubo incorporato e Cilindro, determina la dimensione della forma di base, può essere ridimensionato in scala non uniforme. |
| <b>Scala</b> <i>0.0 - 1.0</i> | Impostate la scala globale per l’effetto. Con Forme incorporate si tratta di una scala di forma base uniforme che non influisce sul Height o sulla Profondità.<br><br>Con l&#39;input personalizzato, l&#39;intero risultato finale viene ridimensionato in modo uniforme. |
| <b>Tipo di profilo</b> <i>Sfumatura verticale dritta, maschera</i> | Controllo principale per determinare il comportamento dell&#39;effetto e l&#39;uso di mappe di input aggiuntive opzionali.<br><br>Con il comportamento Estrusione diritto standard, Sfumatura verticale puoi personalizzare i valori di scala lungo l&#39;intero asse e Maschera puoi nascondere le sezioni lungo l&#39;asse in base alla maschera. |
| <b>Height smussato</b> <i>0.0 - 1.0</i> | Impostate la distanza della smussatura lungo l&#39;asse di estrusione. |
| <b>Intensità smusso</b> <i>0.0 - 1.0</i> | Impostate il valore di ritrazione della smussatura rispetto alla forma originale. |
| <b>Curva smussata</b> <i>-1.0 - 1.0</i> | Impostate la curva convessa o concava dell’effetto Smussato. Un valore pari a 0 significa rettilineo, nessuna curva. |
| <b>Smusso speculare</b> <i>Falso/Vero</i> | Attiva/disattiva per applicare Smusso sopra e sotto la forma. |
| <b>Riduci multicolore</b> <i>0 - 2</i> | Comando di downscaling semplice integrato. Può essere utilizzato per aggiungere rapidamente l&#39;antialiasing; assicurarsi di aumentare anche la risoluzione dei nodi. |
| <b>Posizione</b> | Controllo principale per la rotazione dei risultati nello spazio 3D. Correlazione con Gizmo interavtice nel Vista 2D. |
| <b>Intervallo di output</b> <i>[0, 1], [-1, 1]</i> | Impostare i valori di output min e max. Se intervallo è impostato su [-1,1], i valori negativi vengono presentati come nero. |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="shape-extrude.resources/shape-extrude-1.png" />
        </td>
    </tr>
</table>
