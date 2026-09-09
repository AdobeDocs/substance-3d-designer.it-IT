---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/working-with-3d-scenes/exporting-scenes.html"
breadcrumb-title: ''
description: Esporta scene 3D con tutte le modifiche apportate in Designer utilizzando l’azione Esporta scena nel menu Scena vista 3D.
helpx_creative_field: ""
helpx_description: Designer > Working with 3D scenes > Exporting scenes
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Esportazione di scene
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 0%

---


# Esportazione di scene

Quando devi esportare la scena con tutte le modifiche apportate in Designer, utilizza le azioni &quot;Esporta scena...&quot; nel menu &quot;Scena&quot; di [Vista 3D](../../interface/3d-view/3d-view.md).

Per le esportazioni nei formati USD, il contenuto della scena corrisponderà all&#39;albero visualizzato nel [Visualizzatore scene](../../interface/3d-view/scene-browser/scene-browser.md).

Per gli altri formati, il contenuto della scena e la sua struttura interna dipenderanno dalle caratteristiche supportate dal formato di file selezionato.

>[!NOTE]
>
> Tutti gli elementi aggiunti alla scena da Designer verranno inclusi nella scena esportata: la videocamera predefinita, l’ambiente predefinito, tutto il materiale copia eventuali luci aggiuntive.

![Azioni di esportazione scene](../../assets/exportActions.png "Azioni di esportazione scene"){zoomable="yes"}

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Esporta scena

</td>
<td style="border: 0;" valign="top">

### Esportare una scena come livelli

</td>
<td style="border: 0;" valign="top">

### Texture

</td>
</tr>
</table>

## Esporta scena

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

L’azione &quot;Esporta scena...&quot; nel menu &quot;Scena&quot; esporta scene 3D modificate in modo distruttivo: la scena è *appiattita* e qualsiasi riferimento all’originale viene perso.

Ciò significa che le modifiche apportate alla scena originale non influiscono affatto sulla scena esportata.

</td>
<td style="border: 0;" valign="top">

![File di scena esportati - Con unico livello](../../assets/exportFlattened.png "File di scena esportati - Con unico livello"){zoomable="yes"}

</td>
</tr>
</table>

## Esportare una scena come livelli

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

L&#39;azione &quot;Esporta scena come livelli...&quot; viene esportata nei formati <b>USD</b> (.usd, .usda, .usdc, .usdz) ed è *non distruttiva*: il file esportato principale elabora una *catena di riferimenti* in cui tutti gli aspetti modificati della nuova scena vengono memorizzati in file USD separati.

Questo significa che le modifiche apportate alla scena originale vengono trasferite alla scena esportata.

</td>
<td style="border: 0;" valign="top">

![File di scena esportati - Con livelli](../../assets/exportLayered.png "File di scena esportati - Con livelli"){zoomable="yes"}

</td>
</tr>
</table>

I file esportati seguono questa struttura:

* <b>File principale</b>
  * <b>.layers</b>: fa riferimento ai sottolivelli sottostanti e dichiara le modifiche locali del materiale, che associano la geometria alle copie del materiale create da Designer.
    * <b>.assembly</b>: fa riferimento al file .scene# e dichiara le modifiche locali alla geometria, che apportano i dati ricalcolati da Designer della geometria interessata dai materiali sottoposti a modifiche locali.
      * <b>.scene#</b>: fa riferimento alla scena originale.
    * <b>.camera</b>: dichiara la fotocamera aggiunta da Designer alla scena.
    * <b>.light</b>: dichiara le luci aggiunte da Designer alla scena.
    * <b>.material</b>: dichiara le copie dei materiali aggiunte da Designer alla scena, che utilizzano le texture esportate.

## Texture

Le texture vengono esportate in una directory accanto al file esportato e prendono il nome da esso, con il suffisso ‘<b>\_textures</b>’.

Utilizzano il formato <b>PNG</b>, ad eccezione delle texture HDR (a virgola mobile) che utilizzano il formato <b>EXR</b>.
