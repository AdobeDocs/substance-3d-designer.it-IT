---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blurs/mlv-grayscale.html"
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
source-git-commit: 27326c60e0247617a8f57554a68c9663934cd2bc
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 0%

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

## Connettori di ingresso

<b>Immettere </b>*Scala di grigio* L&#39;immagine in scala di grigio che deve essere elaborata.

## Connettori di uscita

<b>Output </b>*Scala di grigi* Immagine filtrata in scala di grigi.

## Parametri

<b>Intensità</b> *Mobile* Intensità del filtro applicato all&#39;immagine.\
Più alti sono i valori, maggiore sarà l’uniformità dei dettagli e del disturbo nelle aree più piatte.

<b>Smoothness</b> *Fluttuazione* L’intensità della smussatura applicata alle aree di strutturazione, che risulta in aree più rotonde e riduce l’effetto di gradazione che può verificarsi con intensità di filtraggio più elevate.

<b>Criterio</b> *Intero* Criterio utilizzato per selezionare i valori che definiranno le aree di strutturazione nell&#39;immagine.\
In altre parole, come devono essere *raggruppati* i pixel in aree da smussare.\
*- Varianza:* Selezionare i valori con la dispersione più bassa attorno alla media, che determina gruppi di pixel simili tra loro\
*- Coefficiente di variazione:* Selezionare i valori tenendo conto della media, il che comporta una minore variazione nelle aree più luminose

<b>Gaussiano</b> *Booleano* Utilizza una distribuzione gaussiana per raggruppare i pixel in aree strutturanti.\
Se è impostato su &quot;True&quot;, l’operazione determina aree più uniformi e un effetto di conversione della trasparenza ridotto.

<b>Iterazioni</b> *Numero intero* Numero di volte in cui il filtro viene eseguito, in cui ogni iterazione viene applicata sul risultato di quella precedente.\
Più iterazioni producono aree strutturanti più piatte e nitide.

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
