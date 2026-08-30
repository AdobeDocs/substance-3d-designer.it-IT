---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/resources/3d-scene-resource.html"
breadcrumb-title: ''
description: Scoprite come importare e utilizzare le risorse per scene 3D in Substance 3D Designer per l’anteprima e il test del materiale.
helpx_creative_field: ""
helpx_description: Designer > Resources > 3D scene resource
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Risorsa scena 3D
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '506'
ht-degree: 1%

---


# Risorsa scena 3D

Questa pagina descrive il tipo di risorsa **scena 3D** in Substance 3D Designer, inclusi i formati di file supportati e il modo in cui può essere utilizzata.

## Panoramica

Le risorse per le scene 3D possono essere utilizzate in vari flussi di lavoro:

* [mappe mesh di cottura](../../bakers/bakers.md)
* visualizza in anteprima *texture* da [Substance grafici](../../compositing-graphs/substance-compositing-graphs.md) nella [vista 3D](../../interface/3d-view/3d-view.md)

Sono supportati i seguenti formati di file di scena 3D:

* [USD](https://graphics.pixar.com/usd/release/index.html) (\*.usd)
* [USDA](https://graphics.pixar.com/usd/release/index.html) (\*.usda)
* [USDZ](https://graphics.pixar.com/usd/release/index.html) (\*.usdz)
* [Autodesk FBX](https://www.autodesk.com/products/fbx/overview) (\*.fbx)
* [OBJ Wavefront](https://www.fileformat.info/format/wavefrontobj/egff.htm) (\*.obj)
* [Trama Studio Autodesk 3D](https://knowledge.autodesk.com/support/3ds-max/learn-explore/caas/CloudHelp/cloudhelp/2022/ENU/3DSMax-Data-Exchange/files/GUID-A16ECF7F-70E5-4F9F-8EAD-35F5CFB485A2-htm.html) (\*.3ds)
* [Collada](https://www.khronos.org/collada/) (\*.dae)
* [Autodesk AutoCAD Drawing](https://knowledge.autodesk.com/support/autocad/learn-explore/caas/CloudHelp/cloudhelp/2019/ENU/AutoCAD-Core/files/GUID-D4242737-58BB-47A5-9B0E-1E3DE7E7D647-htm.html) (\*.dxf)

## Memorizzazione della trama

Le scene 3D possono essere collegate *solo*, il che significa che si trovano nella loro posizione sul disco e vi si fa riferimento nell&#39;applicazione.

Quando un pacchetto con una risorsa scena 3D viene pubblicato come risorsa [Substance 3D](https://www.adobe.com/products/substance3d/3d-augmented-reality.html) (SBSAR), la trama *non è incorporata*, ma viene eliminata.

## Eseguire i baking mappe trama

Il collegamento di una scena 3D nel pacchetto è l&#39;unico modo per [eseguire i baking mappe con trama](../../bakers/bakers.md) al di fuori della geometria della scena. Per iniziare, puoi eseguire i seguenti passaggi:

* Fai clic su *RMB* in un pacchetto e seleziona l&#39;opzione <b>Collegamento > Trama 3D</b> nel menu di scelta rapida
* Scegliere un file di scena 3D supportato
* Se viene visualizzata la finestra di dialogo <b>Collega come trama Udim</b>, fai clic su *No* a meno che non desideri eseguire i baking riquadri UV
* Con la risorsa caricata in [Esplora risorse](../../interface/the-explorer-window/the-explorer-window.md), fare clic su *RMB* e selezionare l&#39;opzione <b>Esegue i baking informazioni modello</b> nel menu di scelta rapida
* Viene visualizzata la finestra di dialogo [Esegue i baking informazioni sul modello](../../bakers/bakers.md) che consente di impostare ed eseguire tutti i esegue i baking delle mappe trama

![Eseguire i baking le mappe trama](3d-scene-resource.resources/bake-model-information.gif "Eseguire i baking le mappe trama"){width="512px"}

## Utilizzo riquadro UDIM/UV

Quando una risorsa trama è collegata e l’applicazione rileva UV al di fuori dell’intervallo 0-1, ti verrà chiesto se questa trama deve essere trattata come una trama UDIM (nota anche come Porzioni UV). Questa impostazione può essere modificata in seguito e, a meno che non si sia certi di utilizzare i riquadri UV, la risposta dovrebbe essere <b>No</b>.

Se è attivo il comportamento Piastrelle UV, la esegue i baking si comporta in modo diverso e eseguirà i baking texture per ogni piastrella UV rilevata.

## Risorsa/Scena e stato

L’applicazione separa i contenuti visualizzati nella vista 3D in due file distinti. Il modello o la trama 3D effettiva è una risorsa visibile in Esplora risorse. La configurazione di luci, fotocamere e altre impostazioni è denominata &quot;<b>Stato</b>&quot;. Gli stati possono essere salvati in file .sbsscn esterni, per essere caricati di nuovo in seguito. I file .sbsscn non sono risorse, ma file di configurazione aggiuntivi che possono essere caricati solo tramite [il menu Scena nel vista 3D.](../../interface/3d-view/3d-view.md)
