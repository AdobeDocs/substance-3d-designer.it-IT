---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/resources/font-resource.html"
breadcrumb-title: ''
description: Importa e utilizza le risorse di font in Substance 3D Designer per aggiungere testo e composizione tipografica ai tuoi materiali.
helpx_creative_field: ""
helpx_description: Designer > Resources > Font resource
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Risorsa font
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 2%

---


# Risorsa font

Le risorse dei font devono essere utilizzate insieme al [nodo di testo atomico](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/text/text.md). Consentono di utilizzare font non installati nel sistema, facendo riferimento a un file di font in qualsiasi punto del disco.

>[!NOTE]
>
> **Font in SBSAR**
> 
> I font sono sempre incorporati in un SBSAR, indipendentemente dal fatto che provengano da una risorsa collegata o utilizzando un font installato nel sistema. Il vantaggio di questo metodo è che non c&#39;è bisogno di installare, e quando si esporta un file SBS con dipendenze, è possibile essere sicuri che i file dei font vengono.

## Utilizzo di risorse per font personalizzati

* Fai clic con il pulsante destro del mouse su un pacchetto e scegli <b>Link > Font</b>
* Selezionate un file .otf o .ttf.
* Inserite un [nodo di testo](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/text/text.md) nel [grafico](../../compositing-graphs/substance-compositing-graphs.md).
* Sotto la proprietà <b>Font </b>, tutte le risorse di font si troveranno nella parte superiore dell&#39;elenco.

Si noti che l&#39;elenco dei font non si aggiorna automaticamente con le proprietà aperte. Per visualizzare i font appena collegati, dovrete passare a un’altra finestra delle proprietà e tornare a un nodo Testo.
