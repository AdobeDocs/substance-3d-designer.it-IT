---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-uncombine.html"
breadcrumb-title: ''
description: Utilizzare il nodo Normale non combinati per separare i dati della mappa normale combinata nei singoli componenti X, Y e Z.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal map > Normal uncombine
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Normale non combinato
user-guide-description: ''
user-guide-title: ''
source-git-commit: 03373417b3d82a278c159aa83baf282b67c9cbe3
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 2%

---


# Normale non combinato

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Icona di separazione normale](../../../../../../assets/NormalUncombine.png "Icona di separazione normale"){width="200px"}

<b>In:</b> Filtri > Mappa normale

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Rimuove da una mappa normale i dettagli della superficie descritti da una mappa di height.

</td>
</tr>
</table>

<a name="inputs"></a>

## Input

|  |  |
|:---|:---|
| <b>Normale combinato</b> <i>Colore</i> PRIMARIO | La mappa normale da cui rimuovere i dettagli. |
| <b>Height</b> <i>Scala di grigi</i> | La mappa del height che rappresenta i dettagli della superficie da rimuovere dalla mappa normale combinata. |

<a name="outputs"></a>

## Output

|  |  |
|:---|:---|
| <b>Normale non combinato</b> <i>Colore</i> | La mappa normale in cui sono stati rimossi i dettagli della superficie descritti dalla mappa del height di input. |
| <b>Intensità presunta</b> <i>Mobile</i> | Stima dell&#39;intensità che deve essere impostata su un nodo [Normale](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md) connesso alla mappa del height di input, in modo che corrisponda all&#39;intensità della mappa normale di input. |

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Formato normale</b> *Numero intero* | Formato della mappa normale di input. Inverte efficacemente il canale del verde.<ul data-preserve-html="true"> <li data-preserve-html="true"><b>DirectX:</b> l&#39;asse Y punta in alto</li> <li data-preserve-html="true"><b>OpenGL:</b> l&#39;asse Y punta in basso</li> </ul> |

## Esempi

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/normal_uncombine_example_3_before.jpg" alt="normal_uncombine_example_3_before">
      <br><i>Prima</i>
    </td>
    <td>
      <img src="../../../../../../assets/normal_uncombine_example_3_after.jpg" alt="normal_uncombine_example_3_after">
      <br><i>Dopo</i>
    </td>
  </tr>
</table>

![Separazione normale: esempio 2](../../../../../../assets/normal_uncombine_example_4.png "Separazione normale: esempio 2"){zoomable="yes"}

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/normal_uncombine_example_1_before.jpg" alt="normal_uncombine_example_1_before">
      <br><i>Prima</i>
    </td>
    <td>
      <img src="../../../../../../assets/normal_uncombine_example_1_after.jpg" alt="normal_uncombine_example_1_after">
      <br><i>Dopo</i>
    </td>
  </tr>
</table>

![Separazione normale: esempio 4](../../../../../../assets/normal_uncombine_example_6.png "Separazione normale: esempio 4"){zoomable="yes"}

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/normal_uncombine_example_2_before.jpg" alt="normal_uncombine_example_2_before">
      <br><i>Prima</i>
    </td>
    <td>
      <img src="../../../../../../assets/normal_uncombine_example_2_after.jpg" alt="normal_uncombine_example_2_after">
      <br><i>Dopo</i>
    </td>
  </tr>
</table>

![Separazione normale: esempio 6](../../../../../../assets/normal_uncombine_example_5.png "Separazione normale: esempio 6"){zoomable="yes"}
