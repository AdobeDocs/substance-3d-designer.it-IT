---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/interface/3d-view/camera/post-effects.html"
breadcrumb-title: ''
description: Applicate effetti di post-elaborazione alla videocamera con vista 3D per visualizzare e visualizzare materiale migliorato.
helpx_creative_field: ""
helpx_description: Designer > Interface > 3D view > Camera > Post effects
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Effetti post
user-guide-description: ''
user-guide-title: ''
source-git-commit: 27326c60e0247617a8f57554a68c9663934cd2bc
workflow-type: tm+mt
source-wordcount: '732'
ht-degree: 4%

---


# Effetti post

![Effetti post](../../../../assets/postEffects.png "Effetti post"){zoomable="yes"}

Nelle proprietà della videocamera, potete attivare gli effetti di postproduzione per migliorare i rendering o controllare proprietà specifiche del materiale.

Questi effetti sono sviluppati internamente e sono disponibili solo per il rasterizzatore e i [moduli di rendering](../../../../interface/3d-view/3d-renderers/3d-renderers.md) di Pathtracer GPU.

Qualsiasi effetto post attivato al momento del salvataggio di [risorse scena 3D](../../../../resources/3d-scene-resource/3d-scene-resource.md) o [file di stato scena](../../../../working-with-3d-scenes/working-with-3d-scenes.md) verrà salvato come parte dello stato della scena.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Mappatura toni

</td>
<td style="border: 0;" valign="top">

### Bloom

</td>
<td style="border: 0;" valign="top">

### Profondità di campo

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>

## Mappatura toni

Modifica i colori del rendering in base ad algoritmi e/o tabelle di ricerca (LUT) specifici.

Ciò consente di migliorare la coerenza dei colori tra le applicazioni. Ad esempio, la mappatura toni AgX è disponibile anche in Blender.

+++Reinhard


<table>
  <tr>
    <td>
      <img src="../../../../assets/PostFXDisabled.jpg" alt="PostFXDisabled">
      <br><i>Prima</i>
    </td>
    <td>
      <img src="../../../../assets/PostFXReinhard.jpg" alt="PostFXReinhard">
      <br><i>Dopo</i>
    </td>
  </tr>
</table>



![PostFXDisabled](../../../../assets/PostFXDisabled.jpg "PostFXDisabled")

![PostFXReinhard](../../../../assets/PostFXReinhard.jpg "PostFXReinhard")

+++

+++Atan


<table>
  <tr>
    <td>
      <img src="../../../../assets/PostFXDisabled.jpg" alt="PostFXDisabled">
      <br><i>Prima</i>
    </td>
    <td>
      <img src="../../../../assets/PostFXAtan.jpg" alt="PostFXAtan">
      <br><i>Dopo</i>
    </td>
  </tr>
</table>



![PostFXDisabled](../../../../assets/PostFXDisabled.jpg "PostFXDisabled")

![PostFXAtan](../../../../assets/PostFXAtan.jpg "PostFXAtan")

+++

+++Exp


<table>
  <tr>
    <td>
      <img src="../../../../assets/PostFXDisabled.jpg" alt="PostFXDisabled">
      <br><i>Prima</i>
    </td>
    <td>
      <img src="../../../../assets/PostFXExp.jpg" alt="PostFXExp">
      <br><i>Dopo</i>
    </td>
  </tr>
</table>



![PostFXDisabled](../../../../assets/PostFXDisabled.jpg "PostFXDisabled")

![PostFXExp](../../../../assets/PostFXExp.jpg "PostFXExp")

+++

+++Registro


<table>
  <tr>
    <td>
      <img src="../../../../assets/PostFXDisabled.jpg" alt="PostFXDisabled">
      <br><i>Prima</i>
    </td>
    <td>
      <img src="../../../../assets/PostFXLog.jpg" alt="PostFXLog">
      <br><i>Dopo</i>
    </td>
  </tr>
</table>



![PostFXDisabled](../../../../assets/PostFXDisabled.jpg "PostFXDisabled")

![PostFXLog](../../../../assets/PostFXLog.jpg "PostFXLog")

+++

+++Aces


<table>
  <tr>
    <td>
      <img src="../../../../assets/PostFXDisabled.jpg" alt="PostFXDisabled">
      <br><i>Prima</i>
    </td>
    <td>
      <img src="../../../../assets/PostFXAces.jpg" alt="PostFXAces">
      <br><i>Dopo</i>
    </td>
  </tr>
</table>



![PostFXDisabled](../../../../assets/PostFXDisabled.jpg "PostFXDisabled")

![PostFXAces](../../../../assets/PostFXAces.jpg "PostFXAces")

+++

+++Hejl


<table>
  <tr>
    <td>
      <img src="../../../../assets/PostFXDisabled.jpg" alt="PostFXDisabled">
      <br><i>Prima</i>
    </td>
    <td>
      <img src="../../../../assets/PostFXHejl.jpg" alt="PostFXHejl">
      <br><i>Dopo</i>
    </td>
  </tr>
</table>



![PostFXDisabled](../../../../assets/PostFXDisabled.jpg "PostFXDisabled")

![PostFXHejl](../../../../assets/PostFXHejl.jpg "PostFXHejl")

+++

+++Neutro


<table>
  <tr>
    <td>
      <img src="../../../../assets/PostFXDisabled.jpg" alt="PostFXDisabled">
      <br><i>Prima</i>
    </td>
    <td>
      <img src="../../../../assets/PostFXNeutral.jpg" alt="PostFXNeutrale">
      <br><i>Dopo</i>
    </td>
  </tr>
</table>



![PostFXDisabled](../../../../assets/PostFXDisabled.jpg "PostFXDisabled")

![PostFXNeutral](../../../../assets/PostFXNeutral.jpg "PostFXNeutral")

+++

+++Agx


<table>
  <tr>
    <td>
      <img src="../../../../assets/PostFXDisabled.jpg" alt="PostFXDisabled">
      <br><i>Prima</i>
    </td>
    <td>
      <img src="../../../../assets/PostFXAgx.jpg" alt="PostFXAgx">
      <br><i>Dopo</i>
    </td>
  </tr>
</table>



![PostFXDisabled](../../../../assets/PostFXDisabled.jpg "PostFXDisabled")

![PostFXAgx](../../../../assets/PostFXAgx.jpg "PostFXAgx")

+++

+++Pbr neutro


<table>
  <tr>
    <td>
      <img src="../../../../assets/PostFXDisabled.jpg" alt="PostFXDisabled">
      <br><i>Prima</i>
    </td>
    <td>
      <img src="../../../../assets/PostFXPbrNeutral.jpg" alt="PostFXPbrNeutral">
      <br><i>Dopo</i>
    </td>
  </tr>
</table>



![PostFXDisabled](../../../../assets/PostFXDisabled.jpg "PostFXDisabled")

![PostFXPbrNeutral](../../../../assets/PostFXPbrNeutral.jpg "PostFXPbrNeutral")

+++

## Bloom

Simula l’effetto in-camera di smarginature di luce che si diffondono verso l’esterno da aree molto luminose ad aree che ricevono meno luce.

L&#39;effetto è influenzato dall&#39;illuminazione della scena, dall&#39;esposizione della fotocamera e dai materiali di emissione.

+++Soglia
Valore di luminanza al di sopra del quale deve essere visibile la fioritura.

*A sinistra: 1.0 / A destra: 4.0*



<table>
  <tr>
    <td>
      <img src="../../../../assets/bloomThreshold1.jpg" alt="bloomThreshold1">
      <br><i>Prima</i>
    </td>
    <td>
      <img src="../../../../assets/bloomThreshold4.jpg" alt="bloomThreshold4">
      <br><i>Dopo</i>
    </td>
  </tr>
</table>



![bloomThreshold1](../../../../assets/bloomThreshold1.jpg "bloomThreshold1")

![bloomThreshold4](../../../../assets/bloomThreshold4.jpg "bloomThreshold4")

+++

+++Angolo totale
La rampa di attenuazione della fioritura, in cui un valore più basso determina un raggio di fioritura più breve.

*A sinistra: 1.0 / A destra: 0.6*



<table>
  <tr>
    <td>
      <img src="../../../../assets/bloomFalloff1.jpg" alt="bloomFalloff1">
      <br><i>Prima</i>
    </td>
    <td>
      <img src="../../../../assets/bloomFalloff0-6.jpg" alt="bloomFalloff0-6">
      <br><i>Dopo</i>
    </td>
  </tr>
</table>



![bloomFalloff1](../../../../assets/bloomFalloff1.jpg "bloomFalloff1")

![bloomFalloff0-6](../../../../assets/bloomFalloff0-6.jpg "bloomFalloff0-6")

+++

+++Livello
Intensità della fioritura. Un valore più elevato produce smarginature di luce più luminose e pronunciate.

*Sinistra: 8.0 / Destra: 2.0*



<table>
  <tr>
    <td>
      <img src="../../../../assets/bloomLevel8.jpg" alt="bloomLevel8">
      <br><i>Prima</i>
    </td>
    <td>
      <img src="../../../../assets/bloomLevel2.jpg" alt="bloomLevel2">
      <br><i>Dopo</i>
    </td>
  </tr>
</table>



![bloomLevel8](../../../../assets/bloomLevel8.jpg "bloomLevel8")

![bloomLevel2](../../../../assets/bloomLevel2.jpg "bloomLevel2")

+++

+++Spostamento colore
Sposta la tonalità delle aree interessate dalla fioritura verso i colori più caldi.

*A sinistra: 0,0 / A destra: 0,8*



<table>
  <tr>
    <td>
      <img src="../../../../assets/bloomColorShift0.jpg" alt="bloomColorShift0">
      <br><i>Prima</i>
    </td>
    <td>
      <img src="../../../../assets/bloomColorShift0-8.jpg" alt="bloomColorShift0-8">
      <br><i>Dopo</i>
    </td>
  </tr>
</table>



![bloomColorShift0](../../../../assets/bloomColorShift0.jpg "bloomColorShift0")

![bloomColorShift0-8](../../../../assets/bloomColorShift0-8.jpg "bloomColorShift0-8")

+++

## Profondità di campo

Simula il fenomeno ottico causato dall&#39;uso di ottiche in cui gli oggetti più vicini e più lontani rispetto alla distanza focale risultano sfocati.

L’effetto è influenzato dai parametri &quot;F-Stop&quot; e &quot;Distanza focale&quot; della fotocamera.

>[!TIP]
>
> Per regolare rapidamente la messa a fuoco della fotocamera, posizionate il cursore sulla posizione di una scena che desiderate mettere a fuoco e premete Ctrl+LMB (Windows) o Cmd+LMB (macOS) per impostare automaticamente la distanza di messa a fuoco su tale posizione.

+++Raggio massimo
Raggio massimo dell’effetto di sfocatura.

*A sinistra: 32.0 / A destra: 4.0*



<table>
  <tr>
    <td>
      <img src="../../../../assets/depthOfFieldMaxRadius32.jpg" alt="depthOfFieldMaxRadius32">
      <br><i>Prima</i>
    </td>
    <td>
      <img src="../../../../assets/depthOfFieldMaxRadius4.jpg" alt="depthOfFieldMaxRadius4">
      <br><i>Dopo</i>
    </td>
  </tr>
</table>



![depthOfFieldMaxRadius32](../../../../assets/depthOfFieldMaxRadius32.jpg "depthOfFieldMaxRadius32")

![depthOfFieldMaxRadius4](../../../../assets/depthOfFieldMaxRadius4.jpg "depthOfFieldMaxRadius4")

+++

+++Intensità composita
Entità dell’effetto di sfocatura dalla distanza focale verso l’esterno.

*A sinistra: 0,2 / A destra: 0,05*



<table>
  <tr>
    <td>
      <img src="../../../../assets/depthOfFieldCompositeStrength0-2.jpg" alt="depthOfFieldCompositeStrength0-2">
      <br><i>Prima</i>
    </td>
    <td>
      <img src="../../../../assets/depthOfFieldCompositeStrength0-05.jpg" alt="depthOfFieldCompositeStrength0-05">
      <br><i>Dopo</i>
    </td>
  </tr>
</table>



![depthOfFieldCompositeStrength0-2](../../../../assets/depthOfFieldCompositeStrength0-2.jpg "depthOfFieldCompositeStrength0-2")

![depthOfFieldCompositeStrength0-05](../../../../assets/depthOfFieldCompositeStrength0-05.jpg "depthOfFieldCompositeStrength0-05")

+++

+++Aberrazione longitudinale
Intensità dell’aberrazione che si verifica lontano dalla distanza focale.

Aberration simula come diverse lunghezze d&#39;onda della luce abbiano lunghezze focali leggermente diverse, facendo sì che i colori sembrino essere sfalsati e abbiano sottili differenze nella messa a fuoco.

*A sinistra: 0,0 / A destra: 1,0*



<table>
  <tr>
    <td>
      <img src="../../../../assets/depthOfFieldLongitudinalAberration0.jpg" alt="depthOfFieldLongitudinalAberration0">
      <br><i>Prima</i>
    </td>
    <td>
      <img src="../../../../assets/depthOfFieldLongitudinalAberration1.jpg" alt="depthOfFieldLongitudinalAberration1">
      <br><i>Dopo</i>
    </td>
  </tr>
</table>



![depthOfFieldLongitudinalAberration0](../../../../assets/depthOfFieldLongitudinalAberration0.jpg "depthOfFieldLongitudinalAberration0")

![depthOfFieldLongitudinalAberration1](../../../../assets/depthOfFieldLongitudinalAberration1.jpg "depthOfFieldLongitudinalAberration1")

+++

+++Aberrazione acromatica
Specifica se l’aberrazione deve essere acromatica, ovvero se alcuni o tutti i colori hanno la stessa lunghezza focale.

In questo modo, l’effetto di sfocatura appare distribuito in modo più uniforme.

*Sinistra: True / Destra: False*



<table>
  <tr>
    <td>
      <img src="../../../../assets/depthOfFieldAchromaticAberrationYes.jpg" alt="depthOfFieldAchromaticAberrationYes">
      <br><i>Prima</i>
    </td>
    <td>
      <img src="../../../../assets/depthOfFieldAchromaticAberrationNo.jpg" alt="depthOfFieldAchromaticAberrationNo">
      <br><i>Dopo</i>
    </td>
  </tr>
</table>



![depthOfFieldAchromaticAberrationYes](../../../../assets/depthOfFieldAchromaticAberrationYes.jpg "depthOfFieldAchromaticAberrationYes")

![depthOfFieldAchromaticAberrationNo](../../../../assets/depthOfFieldAchromaticAberrationNo.jpg "depthOfFieldAchromaticAberrationNo")

+++

+++Cat&#39;s eye
Consente di attivare l’effetto occhio gatto nella scena, che simula il modo in cui la luce che entra da un angolo obliquo non entra in un disco, ma in un ovale irregolare, causando distorsioni.

Questo effetto è più pronunciato con aperture più alte, cioè con valori di F-Stop più bassi.

*Sinistra: True / Destra: False*



<table>
  <tr>
    <td>
      <img src="../../../../assets/depthOfFieldAchromaticCatsEyeYes.jpg" alt="depthOfFieldAchromaticCatsEyeYes">
      <br><i>Prima</i>
    </td>
    <td>
      <img src="../../../../assets/depthOfFieldAchromaticCatsEyeNo.jpg" alt="depthOfFieldAchromaticCatsEyeNo">
      <br><i>Dopo</i>
    </td>
  </tr>
</table>



![depthOfFieldAchromaticCatsEyeYes](../../../../assets/depthOfFieldAchromaticCatsEyeYes.jpg "depthOfFieldAchromaticCatsEyeYes")

![depthOfFieldAchromaticCatsEyeNo](../../../../assets/depthOfFieldAchromaticCatsEyeNo.jpg "depthOfFieldAchromaticCatsEyeNo")

+++
