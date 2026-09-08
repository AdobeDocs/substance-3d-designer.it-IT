---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blurs/mlv-grayscale.html"
breadcrumb-title: ''
description: Usate il filtro Sfocatura scala di grigi MLV per applicare gli effetti di sfocatura movimento alle texture in scala di grigi per aspetti dinamici.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blurs > MLV grayscale
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Scala di grigi MLV
user-guide-description: ''
user-guide-title: ''
source-git-commit: f25074f2fc4bb66ad781ad2510fdf43ba8aaae69
workflow-type: tm+mt
source-wordcount: '320'
ht-degree: 1%

---


# Scala di grigi MLV

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Scala di grigi MLV: icona](../../../../../../assets/MLV_Grayscale_Icon.png "Scala di grigi MLV: icona")

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
> Vedere anche [Colore MLV](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/mlv-color/mlv-color.md).

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Input</b> <i>Scala di grigi</i> | Immagine in scala di grigio che deve essere elaborata. |

<a name="outputs"></a>

## Output

|  |  |
|:---|:---|
| <b>Output</b> <i>Scala di grigi</i> | Immagine filtrata in scala di grigio. |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Intensità</b> *Mobile* | Intensità del filtro applicato all’immagine.<br><br>Valori più alti determinano una maggiore uniformità dei dettagli e del disturbo nelle aree più piatte. |
| <b>Smoothness</b> *Mobile* | L’intensità della smussatura applicata alle aree strutturanti, che risulta in aree più rotonde e riduce l’effetto di gradino che può verificarsi a intensità di filtrazione più elevate. |
| <b>Criterio</b> *Numero intero* | Criterio utilizzato per selezionare i valori che definiranno le aree di strutturazione nell’immagine.<br><br>In altre parole, come devono essere *raggruppati* i pixel in aree da smussare.<br><br>*- Varianza:* Selezionare i valori con la dispersione più bassa intorno alla media, il che risulta in cluster di pixel simili l&#39;uno all&#39;altro <br>*- Coefficiente di variazione:* Selezionare i valori tenendo conto della media, il che risulta in una minore variazione nelle aree più luminose in modo inverso |
| <b>Gaussiano</b> *Booleano* | Usate una distribuzione Controllo per raggruppare i pixel in aree strutturanti.<br><br>Se è impostato su &quot;True&quot;, l&#39;operazione determina aree più uniformi e un effetto di conversione della trasparenza ridotto. |
| <b>Iterazioni</b> *Numero intero* | Numero di volte in cui il filtro viene eseguito, in cui ogni iterazione viene applicata al risultato di quella precedente.<br><br>Con più iterazioni le aree strutturate risultano più piatte e nitide. |

## Esempi

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/MLV_Variant1A.png" alt="MLV_Variant1A">
      <br><i>Prima</i>
    </td>
    <td>
      <img src="../../../../../../assets/MLV_Variant1B.png" alt="MLV_Variant1B">
      <br><i>Dopo</i>
    </td>
  </tr>
</table>

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/MLV_Variant2A.png" alt="MLV_Variant2A">
      <br><i>Prima</i>
    </td>
    <td>
      <img src="../../../../../../assets/MLV_Variant2B.png" alt="MLV_Variant2B">
      <br><i>Dopo</i>
    </td>
  </tr>
</table>

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/MLV_Variant2A.png" alt="MLV_Variant2A">
      <br><i>Prima</i>
    </td>
    <td>
      <img src="../../../../../../assets/MLV_Variant2C.png" alt="MLV_Variant2C">
      <br><i>Dopo</i>
    </td>
  </tr>
</table>
