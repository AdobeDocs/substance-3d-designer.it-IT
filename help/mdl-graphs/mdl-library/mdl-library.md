---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/mdl-graphs/mdl-library.html"
breadcrumb-title: ''
description: Accedere alla libreria Material Definition Language in Substance 3D Designer per creare materiali personalizzati.
helpx_creative_field: ""
helpx_description: Designer > MDL graphs > MDL library
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Libreria MDL
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 0%

---


# Libreria MDL

Questa pagina presenta la libreria di contenuti relativi a [grafici MDL](../../mdl-graphs/mdl-graphs.md) e materiali inclusi in Substance 3D Designer. Viene inoltre illustrato come installare e gestire contenuto personalizzato nella [libreria](../../interface/the-library/the-library.md).

## Contenuto MDL nella libreria

I nodi utilizzabili nei grafici MDL sono disponibili nella sezione <b>mdl</b> della [libreria](../../interface/the-library/the-library.md). I nodi vengono disposti in filtri in base al modulo MDL in cui sono definiti.\
Se i moduli vengono archiviati in sottocartelle, questa gerarchia verrà *specchiata* nella libreria come *categorie*.

Questa sezione include il contenuto delle seguenti origini:

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### Contenuto incorporato

Designer include moduli MDL che contengono elementi di base per la creazione di grafici MDL, nonché definizioni complete dei materiali pronte per l&#39;uso.

Il contenuto è archiviato in questo percorso nella directory di installazione: `./resources/view3d/iray/`

### Contenuto personalizzato

Oltre al contenuto incorporato, puoi aggiungere *i tuoi* moduli MDL alla libreria.

In effetti, qualsiasi modulo MDL trovato nelle directory elencate nella sezione <b>MDL</b> delle [impostazioni del progetto](../../interface/preferences-window/project-settings/project-settings.md) viene aggiunto a questa sezione *cumulativamente* nei file del progetto.

### NVIDIA vMaterials

Se la libreria [vMaterials](https://developer.nvidia.com/vmaterials) di NVIDIA è installata, viene *aggiunta automaticamente* nella libreria nella relativa *categoria*.

</td>
<td style="border: 0;" valign="top">

![Risorse MDL nella libreria](mdl-library.resources/mdl-library.png "Risorse MDL nella libreria")

La sezione *&quot;mdl&quot; nella libreria, nella libreria vMaterials e nel contenuto personalizzato sono incorniciati*

</td>
</tr>
</table>

## Contenuto MDL nella vista 3D

Tutti i moduli MDL disponibili nella libreria possono essere utilizzati nella [vista 3D](../../interface/3d-view/3d-view.md) quando viene utilizzato il modulo di rendering Iray.

Aprite il menu <b>Materiali</b> e aprite un sottomenu *del materiale della scena* per sfogliare i moduli MDL disponibili. Gli elenchi includono:

* Contenuto incorporato
* Contenuto personalizzato
* NVIDIA [vMaterials](https://developer.nvidia.com/vmaterials)
* Caricati [grafici MDL](../../mdl-graphs/mdl-graphs.md)

![Materiali MDL in materiali vista 3D](mdl-library.resources/mdl-apply-in-3dview-material-list.png "MDL in vista 3D")

*Materiali MDL nel vista 3D*
