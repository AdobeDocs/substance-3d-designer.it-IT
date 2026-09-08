---
helpx_url: ""
breadcrumb-title: ''
description: Utilizzate la finestra a comparsa Spostamento per regolare rapidamente lo spostamento e la tassellatura applicati alle trame in una scena 3D.
helpx_creative_field: ""
helpx_description: ""
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Popup vista 3D - Spostamento
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '437'
ht-degree: 2%

---


# finestra a comparsa Spostamento

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="vertical-align: top; border: 0">
        <td style="border: 0">
            <p>La finestra a comparsa Spostamento disponibile nella barra degli strumenti vista 3D offre controlli diretti per lo spostamento e la tassellatura delle trame.</p>
            <p>Sono disponibili tre parametri:<ul>
                <li>Scala altezza</li>
                <li>Livello di altezza</li>
                <li>Tassellatura</li></ul>
        </td>
        <td style="width: 60%; margin-left: 32px; border: 0">
            <img src="./displacement.resources/3d-view-displacement-popup-mograph.gif" alt="Finestra a comparsa Spostamento nella vista 3D" />
        </td>
    </tr>
</table>

## Scala altezza

La distanza massima di spostamento per i vertici della trama lungo il normale, espressa in unità di scena.<br>
Questa è la distanza percorsa per un valore di 1,0 nella mappa dell&#39;altezza.

Quando un grafico a Substance è collegato a un materiale e tale grafico include un [nodo di output](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) con
<code>heightScale</code> , il parametro di scala Height nel pop-up è *disabled* per tale materiale
poiché è attualmente guidato dal grafico.

>[!TIP]
> 
>Utilizzare il nodo [Height alle normali unità di misura](../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/height-normal-world-units/height-to-normal-world-units.md) e fare in modo che il parametro &#39;profondità Height&#39; corrisponda al valore &#39;Scala Height&#39;
>per garantire la corretta ombreggiatura quando si utilizza lo spostamento.

## Livello di altezza

Valore in scala di grigio nella mappa dell&#39;altezza utilizzato come *punto intermedio* per il height di spostamento.
Ossia il valore di soglia utilizzato come elevazione 0,0.

I valori inferiori a tale soglia determinano lo spostamento dei vertici all’indietro, mentre i valori superiori a tale soglia determinano
vertici spostati in avanti.

## Tassellatura

La tassellatura comporta la suddivisione di singole facce mesh mediante l&#39;aggiunta di un vertice sui rispettivi segmenti e quindi la connessione
tutti i vertici a un nuovo vertice al centro, in modo che 1 faccia diventi **6**.

Il parametro definisce il numero di volte in cui le facce devono essere suddivise ricorsivamente.

L&#39;*ambito* del parametro di tassellatura varia in base al *renderer* attualmente in uso: può essere applicato
per trama o per materiale.

### Per trama

Quando si utilizza il modulo di rendering [Rasterizzatore](../3d-renderers/3d-renderers.md#rasterizer) o [Pathtracer GPU](../3d-renderers/3d-renderers.md#gpu-pathtracer), ogni oggetto Trama nella scena ha un *oggetto separato*
valore di suddivisione.

La suddivisione è contestuale: è ottimizzata in modo che solo le superfici con un *valore height non uniforme* o
una *mappa di height non piatta* verrà suddivisa, indipendentemente dal valore del parametro.

### Per materiale

Quando si utilizza il modulo di rendering [OpenGL](../3d-renderers/3d-renderers.md#opengl), ogni materiale nella scena ha un valore di suddivisione *separato*, che
viene applicato a *tutte le facce che utilizzano tale materiale*.

La suddivisione non è contestuale: le superfici vengono suddivise nella quantità di volte specificata indipendentemente dalla loro corrente
Valore height o texture.

## Visualizzazione della tassellatura

È possibile visualizzare il risultato della tassellatura controllando il **wireframe** della trama.<br>
Di seguito sono descritti i passaggi per visualizzare il wireframe per ogni renderer:

### Rasterizzatore/Pathtracer GPU

Utilizzare la <img src="../3d-view.resources/3d-view-scene-toolbar-render-settings.png" width="22" /> **Impostazioni rendering**
 quindi, nel Dock proprietà, passa a **Impostazioni rendering > Modalità diagnostica** e seleziona **Wireframe
 (spazio mondo)**.

### OpenGL

Utilizzare la <img src="../3d-view.resources/3d-view-scene-toolbar-wireframe.png" width="22" /> **Wireframe**
 pulsante.
