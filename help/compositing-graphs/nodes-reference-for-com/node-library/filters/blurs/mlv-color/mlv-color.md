---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blurs/mlv-color.html"
breadcrumb-title: ''
description: Usate il filtro Sfocatura colore MLV per applicare effetti di sfocatura movimento alle texture di colore per aspetti visivi dinamici.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blurs > MLV color
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Colore MLV
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '352'
ht-degree: 1%

---


# Colore MLV

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Colore MLV: icona](mlv-color.resources/MLV_Color_Icon.png "Colore MLV: icona")

<b>Ingresso:</b> Filtri > Sfocature

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

MLV sta per <b>&#39;Media della variazione minima&#39;</b>. Questo filtro migliora i bordi e attenua il disturbo in un’immagine.

Il filtro trova le aree strutturanti in un’immagine e le utilizza sia per aumentarne la nitidezza che per appiattirla. In alcuni casi, questo può comportare passaggi lungo sfumature più ampie rispetto alle aree di strutturazione.

</td>
</tr>
</table>

>[!NOTE]
>
> Vedere anche [scala di grigi MLV](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/mlv-grayscale/mlv-grayscale.md).

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Input</b> <i>Colore</i> | Immagine a colori da elaborare. |

<a name="outputs"></a>

## Output

|  |  |
|:---|:---|
| <b>Output</b> <i>Colore</i> | Immagine a colori filtrata. |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Intensità</b> *Mobile* | Intensità del filtro applicato all’immagine.<br><br>Valori più alti determinano una maggiore uniformità dei dettagli e del disturbo nelle aree più piatte. |
| <b>Smoothness</b> *Mobile* | L’intensità della smussatura applicata alle aree strutturanti, che risulta in aree più rotonde e riduce l’effetto di gradino che può verificarsi a intensità di filtrazione più elevate. |
| <b>Criterio</b> *Numero intero* | Criterio utilizzato per selezionare i valori che definiranno le aree di strutturazione nell’immagine.<br><br>In altre parole, come devono essere *raggruppati* i pixel in aree da smussare.<br><br>*- Varianza:* Selezionare i valori con la dispersione più bassa intorno alla media, il che risulta in cluster di pixel simili l&#39;uno all&#39;altro <br>*- Coefficiente di variazione:* Selezionare i valori tenendo conto della media, il che risulta in una minore variazione nelle aree più luminose in modo inverso |
| <b>Gaussiano</b> *Booleano* | Usate una distribuzione Controllo per raggruppare i pixel in aree strutturanti.<br><br>Se è impostato su &quot;True&quot;, l&#39;operazione determina aree più uniformi e un effetto di conversione della trasparenza ridotto. |
| <b>Influenza sul canale alfa</b> *Booleano* | Se è impostato su &#39;True&#39;, il filtro viene applicato anche al canale alfa dell&#39;immagine.<br><br>Se è impostato su &#39;False&#39;, il canale alfa viene ignorato completamente e viene lasciato così com&#39;è nell&#39;output. |
| <b>Iterazioni</b> *Numero intero* | Numero di volte in cui il filtro viene eseguito, in cui ogni iterazione viene applicata al risultato di quella precedente.<br><br>Con più iterazioni le aree strutturate risultano più piatte e nitide. |

## Esempi

<table>
  <tr>
    <td>
      <img src="mlv-color.resources/MLV_Variant4A.png" alt="MLV_Variant4A">
      <br><i>Prima</i>
    </td>
    <td>
      <img src="mlv-color.resources/MLV_Variant4B.png" alt="MLV_Variant4B">
      <br><i>Dopo</i>
    </td>
  </tr>
</table>

<table>
  <tr>
    <td>
      <img src="mlv-color.resources/MLV_Variant5A.png" alt="MLV_Variant5A">
      <br><i>Prima</i>
    </td>
    <td>
      <img src="mlv-color.resources/MLV_Variant5B.png" alt="MLV_Variant5B">
      <br><i>Dopo</i>
    </td>
  </tr>
</table>

<table>
  <tr>
    <td>
      <img src="mlv-color.resources/MLV_Variant3A.png" alt="MLV_Variant3A">
      <br><i>Prima</i>
    </td>
    <td>
      <img src="mlv-color.resources/MLV_Variant3B.png" alt="MLV_Variant3B">
      <br><i>Dopo</i>
    </td>
  </tr>
</table>
