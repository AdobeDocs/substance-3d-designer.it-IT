---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/shadows-filter-node.html"
breadcrumb-title: ''
description: Utilizza il nodo del filtro Ombre per generare effetti di ombra dalle texture di input per aggiungere profondità e realismo ai materiali.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Shadows (Filter Node)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Ombre (Nodo filtro)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2ea5b90ca7a4cbcd0b0049b156e8ded334aa0ceb
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 8%

---


# Ombre (Nodo filtro)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](shadows-filter-node.resources/shadows-1.png){width="128px"}

<b>Ingresso:</b> Filtri > Effetti

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Versione non elaborata in scala di grigio del nodo [Ombra esterna forma](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/shape-drop-shadow/shape-drop-shadow.md). Prende solo forme binarie in bianco e nero come input e restituisce solo l&#39;ombra.

Può essere utile se siete appena dopo l&#39;ombra e non volete lavorare con un nodo più completo, ad esempio quando si costruisce il proprio materiale o l&#39;illuminazione al forno.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parametri

|  |  |
|:---|:---|
| <b>Distanza ombra</b> <i>0.0 - 1.0</i> | Controlla la distanza dell’ombra. |
| <b>Angolo luce</b> <i>0.0 - 1.0</i> | Controlla l’angolo di incidenza della luce. |
| <b>Morbidezza bordi</b> <i>0.0 - 1.0</i> | Determina la durezza o la morbidezza dei bordi delle ombre. |
| <b>Esempi</b> <i>1 - 16</i> | Imposta la qualità per l’impostazione Sfumatura bordi. |

## Esempi

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="shadows-filter-node.resources/shadow-ex.png" />
        </td>
    </tr>
</table>
