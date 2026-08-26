---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/interface/the-graph-view/graph-items/comment.html"
breadcrumb-title: ''
description: Aggiungere commenti ai grafici di Substance 3D Designer per documentare il flusso di lavoro e spiegare le connessioni ai nodi.
helpx_creative_field: ""
helpx_description: Designer > Interface > Graph view > Graph items > Comment
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Commento
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '338'
ht-degree: 1%

---


# Commento

<table>
<tr style="border: 0;">
<td width="25.00%" style="border: 0;" valign="top">

![Icona commento](../../../../assets/graphatomic-comment_1.png "Icona commento")

</td>
<td width="100.00%" style="border: 0;" valign="top">

Un commento è semplicemente un testo mobile che può essere inserito ovunque in un grafico.

Questo metodo consente di annotare e spiegare parti di un grafico. La proprietà <b>Description</b> contiene il testo visualizzato.

</td>
</tr>
</table>

>[!NOTE]
>
> I commenti hanno un’interruzione di riga automatica che mira a ridurne al minimo l’impatto in un grafico.

## Creazione di commenti

Il tipo di commento predefinito viene inserito indipendentemente dai nodi nel grafico.

Può essere creato nei modi seguenti:

+++Menu Nodo
Premi <b>Barra spaziatrice</b> nella vista Grafico per aprire il <b>menu Nodo</b> e seleziona la voce &quot;Commento&quot; nell&#39;elenco.

Digita &quot;commento&quot; nel campo di ricerca per posizionare la superficie dell&#39;elemento e trovarlo più rapidamente.

+++

+++Scelta rapida
Se una scelta rapida da tastiera è associata all&#39;elemento &#39;Comment&#39; nelle [Preferenze](../../../../interface/preferences-window/preferences-window.md), premi la scelta rapida quando la visualizzazione Grafico è attiva.

+++

+++Menu contestuale
Nella vista Grafico, premi <b>RMB</b> su qualsiasi oggetto o in uno spazio vuoto e seleziona l&#39;opzione <b>Aggiungi commento</b>.

+++

+++Barra degli strumenti Grafico
Nella barra degli strumenti Visualizzazione grafico fare clic sul pulsante &#39;Commento&#39; nella <b>Palette dei nodi</b>.

+++

+++Libreria
Nella libreria, seleziona la categoria <b>Elementi del grafico</b>, quindi trascina l’elemento &quot;Commento&quot; nella vista del grafico.

+++

>[!TIP]
>
> Quando viene creato un commento, la relativa proprietà &quot;Descrizione&quot; diventa automaticamente attiva in modo da poter modificare immediatamente il testo del commento.

## Commenti associati

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

Un commento dipendente è un commento che è *associato a un nodo specifico* nel grafico in modo che quando il nodo viene spostato, segue il commento e quando il nodo viene eliminato, il commento viene eliminato insieme a esso.

I commenti creati quando è selezionato un nodo *singolo* o tramite il menu di scelta rapida di un singolo nodo sono associati a tale nodo.

</td>
<td width="33.33%" style="border: 0;" valign="top">

![Commenti: commenti principali](../../../../assets/graph-comment_parented.gif "Commenti: commenti principali")

</td>
</tr>
</table>

## Formattazione HTML

Il testo può essere formattato utilizzando i tag HTML. Questa formattazione viene attivata tramite il pulsante ![](../../../../assets/graph-frames_html-markup-button.png) <b>markup HTML</b> nella proprietà <b>Descrizione</b> del commento.

>[!TIP]
>
> Ulteriori informazioni su questa funzione sono disponibili nella sezione <b>Descrizione</b> della documentazione di [Frame](../../../../interface/the-graph-view/graph-items/frame/frame.md).

![Commenti: markup HTML](../../../../assets/graph-comment_html-markup.gif "Commenti: markup HTML")
