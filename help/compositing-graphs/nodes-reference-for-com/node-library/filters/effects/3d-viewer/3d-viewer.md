---
title: Visualizzatore 3D
description: Designer > Substance grafici composizione > Nodi di riferimento per i grafici composizione Substance > Libreria nodi > Filtro > Effetto > Visualizzatore 3D
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '1989'
ht-degree: 0%
---

# Visualizzatore 3D

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![icona del visualizzatore 3D](./3d-viewer.resources/3d-viewer.png "visualizzatore 3D")

<b>Ingresso:</b> Filtro > Effetto

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrizione

Calcola un rendering 3D per una scena SDF o di intersezione specificata definita da un grafico a funzioni, con una videocamera e una luce ambientale personalizzate.<br><br>Questo nodo è utile per la creazione e la visualizzazione di [Funzioni SDF](../../../../../../function-graphs/nodes-reference-for-fun/function-node-library/function-node-library.md#sdf-functions) da utilizzare nel nodo [splatter forma v2](../../../texture-generators/patterns/shape-splatter-v2/shape-splatter-v2.md) .<br><br>Sono disponibili helper per la visualizzazione degli attributi chiave delle forme nello spazio.<br><br>Per gli utenti esperti, è possibile creare funzioni personalizzate per impostare la videocamera e/o il rendering 3D per pixel.

</td>
</tr>
</table>

>[!INFO]
> 
> Per ulteriori informazioni sui concetti e i flussi di lavoro relativi alla Funzione SDF, consulta la pagina dedicata: [Utilizzo della Funzione SDF](../../../../../../function-graphs/nodes-reference-for-fun/function-node-library/function-nodes-sdf-functions/working-with-sdf-functions.md)

<a name="inputs"></a>

## Input

|                            |                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|:---------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <b>Ambiente</b> *Colore* | L&#39;immagine che deve essere proiettata sulla sfera infinita utilizzata come ambiente della scena e utilizzata per l&#39;illuminazione ambientale.<br><br>La proiezione è <i>equirettangolare</i>, lo stesso utilizzato dalle mappe di ambiente predefinite di Designer disponibili nella categoria <b>vista 3D HDRI</b> della libreria.<br><br>Se non si è connessi, viene utilizzato un ambiente predefinito.<br><br><i>Suggerimento:</i> Utilizzare un&#39;immagine HDR (32 bit) per un&#39;illuminazione precisa. |
| <b>Input 1</b> *Colore* | Un&#39;immagine che può essere campionata nel grafico della funzione <b>Output personalizzato</b> quando il parametro <b>Output</b> è impostato su &#39;Personalizzato&#39;.<br><br>Utilizzare un nodo [Colore campione](../../../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/sampler-nodes/sampler-nodes.md) impostato su &#39;Input immagine 0&#39; per campionare da questa immagine. |
| <b>Input 2</b> *Colore* | Un&#39;immagine che può essere campionata nel grafico della funzione <b>Output personalizzato</b> quando il parametro <b>Output</b> è impostato su &#39;Personalizzato&#39;.<br><br>Utilizzare un nodo [Colore campione](../../../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/sampler-nodes/sampler-nodes.md) impostato su &#39;Input immagine 1&#39; per campionare da questa immagine. |

<a name="outputs"></a>

## Output

|               |                                                                                                                                                                                                                                    |
|:--------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <b>Output</b> | Scena di cui è stato eseguito il rendering, utilizzando il metodo AOV selezionato nel parametro <b>Output</b>.<br><br><i>Nota:</i> per la precisione delle letture in alcuni file AOV, assicurarsi che il vista 2D utilizzi uno spazio colore lineare e che il nodo utilizzi un formato di output HDR a 32 bit. |

<a name="parameters"></a>

## Parametri

|                                               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|:----------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <b>Tipo di scena</b> *Numero intero* | Tipo di funzione utilizzato per descrivere le superfici e le forme di cui eseguire il rendering:<br>- <b>SDF:</b> Utilizzare una funzione campo distanza con segno (SDF, signed distance field) che può descrivere forme complesse.<br>- <b>Intersezione:</b> Utilizzare funzioni di intersezione, che sono più veloci quando sono necessarie solo forme primitive semplici. |
| <b>Scena SDF</b> *Virgola mobile* | Funzione SDF (Sign Distance Field) che descrive le superfici e le forme nella scena.<br><br>Utilizzare i nodi nella categoria [Funzioni SDF](../../../../../../function-graphs/nodes-reference-for-fun/function-node-library/function-node-library.md#sdf-functions) della libreria per creare la funzione. |
| <b>Interseca scena</b> *Virgola mobile* | Funzione di intersezione che descrive le superfici e le forme nella scena.<br><br>Le funzioni di intersezione per semplici primitive e operatori sono disponibili nelle cartelle <b>3d_intersection</b> del pacchetto della libreria <b>3d_functions.sbs</b>.<br><br><i>Suggerimento:</i> Per accedere al pacchetto, trascinare qualsiasi nodo SDF dalla libreria in Esplora risorse. |
| <b>Output</b> *Numero intero* | Il tipo di rendering 3D che deve essere generato dal nodo, comunemente definito come AOV (variabili di output arbitrarie).<br><br>Gli AOV disponibili sono:<br>- <b>Bellezza:</b> Il risultato finale del rendering 3D, con colori ed effetti orientati all&#39;arte.<br>- <b>Normale WS:</b> Le normali dello spazio mondiale delle forme nella scena.<br>- <b>Normale TS:</b> Le normali dello spazio tangente delle forme nella scena.<br>- <b>Posizione:</b> La posizione dello spazio mondiale delle superfici le forme nella scena.<br>- <b>Distanza:</b> La distanza raw dalla fotocamera alle forme nella scena<br>- <b>Profondità:</b> La distanza firmata delle forme dal piano di destinazione della fotocamera, in cui il piano è sempre rivolto verso la fotocamera.<br>- <b>Colore:</b> Il colore di base delle forme (utilizzare il nodo &#39;Imposta colore&#39; per assegnare i colori alle forme nella funzione scena)<br>- <b>ID materiale:</b> Gli ID materiale applicati alle superfici della forma (utilizzare Nodo &#39;Imposta ID materiale&#39; per assegnare ID materiale alle forme nella funzione scena)<br>- <b>Passaggi di traccia Sphere:</b> Visualizzazione della quantità di passaggi necessari per definire la superficie di una forma. Valori più chiari indicano che erano necessari più passaggi.<br>- <b>Personalizzato:</b> Creare una funzione personalizzata per calcolare il colore del rendering per pixel.<br><br><i>Nota:</i> Per letture accurate in alcuni file AOV, assicurarsi che il vista 2D utilizzi uno spazio colore lineare e che il nodo utilizzi un formato di output HDR a 32 bit. |
| <b>Output personalizzato</b> *Virgola mobile 4* | Grafico a funzioni che definisce i colori RGBA per pixel della scena renderizzata come valore Virgola mobile 4.<br><br>Variabili disponibili:<br>- <code>scene.position</code> (Virgola mobile 3) La posizione dello spazio globale delle superfici della scena.<br>- <code>scene.normal</code> (Virgola mobile 3) Normali dello spazio globale delle superfici della scena.<br>- <code>scene.hit</code> (Booleano) Restituisce &#39;True&#39; quando una superficie viene colpita da un raggio della fotocamera.<br>- <code>view.origin</code> (Virgola mobile 3) La posizione dello spazio mondo per pixel della vista fotocamera.<br>- <code>vista.direzione</code> (Virgola mobile 3) Il vettore in avanti per pixel della vista della videocamera, in base alla modalità di proiezione. (E.g. Prospettiva o ortografica)<br>- <code>material.color</code> (Virgola mobile 3) Il colore di base delle superfici della scena.<br>- <code>material.metalness</code> (Virgola mobile) Metallicità delle superfici della scena.<br>- <code>materiale.rugosità</code> (Virgola mobile) Rugosità delle superfici della scena.<br>- <code>material.id</code> (Intero) Gli ID materiale delle superfici della scena.<br><br>È possibile campionare gli input dell&#39;immagine del nodo selezionando i seguenti [Sample color](../../../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/sampler-nodes/sampler-nodes.md) slot del nodo:<br>- <b>Image input 0</b> samples Input 1.<br>- <b>Image input 1</b> samples Input 2. |
| <b>Rotazione dell&#39;ambiente</b> *Mobile* | Rotazione dell&#39;<b>ambiente</b>, in numero di giri. |
| <b>Modalità sfondo</b> *Numero intero* | Specifica l&#39;origine dello sfondo della scena, disegnata in cui non sono visibili superfici di forma.<br><br>- <b>Colore:</b> Il &#39;Colore di sfondo&#39; piatto.<br>- <b>Ambiente:</b> L&#39;immagine fornita all&#39;input &#39;Ambiente&#39;, applicata a una sfera infinita utilizzando la proiezione equirettangolare.  Quando l&#39;input non è connesso, viene utilizzato un ambiente predefinito. |
| <b>Colore di sfondo</b> *Float4* | Colore piatto utilizzato come sfondo della scena. |
| <b>Esempi IBL</b> *Numero intero* | Quantità di campioni di luce eseguita per campione di fotocamera.<br><br>Un valore più elevato determina un&#39;illuminazione più fluida e precisa a costo di prestazioni. |
| <b>Campioni videocamera</b> *Numero intero* | Quantità di campioni di videocamera eseguiti per pixel.<br><br>Questo parametro influisce sulla qualità dell&#39;antialiasing e sulla profondità dell&#39;effetto campo.<br><br>Un valore più elevato produce un&#39;immagine più chiara e meno rumorosa a scapito delle prestazioni. |
| <b>Passaggi di marcia dei raggi</b> *Numero intero* | Quantità di passaggi eseguiti nel processo di traccia della sfera, la tecnica di ray marching utilizzata per rilevare e disegnare le superfici delle forme.<br><br>Un valore più elevato determina superfici accurate e coerenti (in particolare per le forme complesse), a scapito delle prestazioni.<br><br><i>Suggerimento:</i> Impostare il parametro <b>Output</b> sull&#39;AOV &#39;Passaggi di traccia della sfera&#39; per visualizzare le aree delle forme che richiedono ulteriori passaggi. Queste aree saranno interessate per prime riducendo il numero di passaggi. |
| <b>Passaggi secondari per marciare i raggi</b> *Numero intero* | Quantità di passaggi eseguiti nel processo di traccia della sfera per calcolare la diffusione e l&#39;occlusione degli specular al fine di disegnare ombre proiettate.<br><br>Un valore più elevato determina ombre più precise a scapito delle prestazioni. |
| <b>Modalità fotocamera</b> *Numero intero* | Metodo di proiezione della scena sull&#39;immagine di rendering:<br><br>- <b>Prospettiva:</b> Questa proiezione trasmette profondità e consente effetti obiettivo come la profondità di campo.<br>- <b>Ortografica:</b> Questa proiezione appiattisce la scena, annullando la profondità.<br>- <b>Funzione personalizzata:</b> Creare un grafico delle funzioni per impostare una fotocamera personalizzata. |
| <b>Funzione videocamera</b> *Virgola mobile 3* | Grafico a funzioni che definisce la Trasforma della videocamera. Questa opzione può essere utilizzata per configurare una videocamera personalizzata.<br><br>La funzione deve <b>impostare</b> le seguenti variabili:<br>- <code>view.origin</code> (Virgola mobile 3) La posizione dello spazio mondo per pixel della vista fotocamera.<br>- <code>vista.direzione</code> (Virgola mobile 3) Il vettore in avanti per pixel della vista della videocamera, in base alla modalità di proiezione. (E.g. Prospettiva o ortografica)<br><br>Le seguenti variabili sono disponibili per <b>get</b>:<br>- <code>camera.origin</code> (Virgola mobile 3) La posizione spaziale mondiale della videocamera. (camera.direction * camera_distance + camera.target)<br>- <code>camera.direction</code> (Virgola mobile 3) La direzione dello spazio globale della fotocamera, ovvero il vettore Y-forward della fotocamera.<br>- <code>fotocamera.right</code> (Virgola mobile 3) Vettore X-right della fotocamera.<br>- <code>camera.up</code> (Virgola mobile 3) Vettore Z-up della fotocamera.<br>- <code>fotocamera.target</code> (Virgola mobile 3) La posizione spaziale mondiale della fotocamera di destinazione. |
| <b>Posizione UV</b> *Virgola mobile 2* | La posizione nello spazio dell&#39;immagine 2D utilizzata per dedurre la posizione e la direzione della fotocamera in orbita attorno alla <b>posizione di destinazione</b>.<br><br><i>Suggerimento:</i> Questo parametro può essere regolato in modo intuitivo utilizzando il <i>gizmo posizione</i> disponibile nel vista 2D quando viene selezionato il nodo. |
| <b>FOV</b> *Virgola mobile* | Il campo visivo della telecamera ortografica (FOV), che influisce sul fattore di zoom. |
| <b>Lunghezza focale</b> *Virgola mobile* | La lunghezza focale della telecamera, che influisce sul fattore di zoom e sulla profondità dell&#39;effetto campo. |
| <b>Distanza dalla destinazione</b> *Mobile* | La distanza di riposo della fotocamera rispetto alla <b>posizione di destinazione</b>.<br><br>Con questa regolazione, la fotocamera si sposta lungo la direzione da fotocamera a destinazione. |
| <b>Posizione di destinazione</b> *Float3* | La posizione della fotocamera di destinazione, verso cui la fotocamera è sempre orientata. |
| <b>Tonemapper</b> *Numero intero* | Algoritmo di mappatura tonale da applicare al rendering della scena.<br><br>- <b>Nessuno (Raw)<br>- <b>sRGB</b><br>- <b>AgX</b><br>- <b>ACE</b> |
| <b>Abilita profondità campo</b> *Booleano* | Simula l’effetto &quot;profondità di campo&quot; dell’obiettivo della fotocamera per la Prospettiva.<br><br>Utilizzate i parametri <b>Numero F</b> e <b>Distanza focale</b> per regolare rispettivamente l&#39;apertura e il punto focale dell&#39;effetto.<br><br>Anche il risultato è interessato dalla <b>Lunghezza focale</b>. |
| <b>Numero F</b> *Mobile* | L&#39;<i>apertura</i> della fotocamera.<br><br>Con un valore inferiore si ottiene una <i>profondità di campo</i> più breve, ovvero un intervallo di distanza inferiore per gli oggetti più nitidi e un effetto di sfocatura più forte con l&#39;aumentare della distanza da tale intervallo. |
| <b>Distanza focale</b> *Mobile* | Imposta la distanza del punto focale come distanza dalla videocamera lungo il suo vettore in avanti.<br><br>Le superfici all&#39;interno di un intervallo di tale distanza appariranno nitide. Tale intervallo, ovvero la <i>profondità di campo </i>, è definito dal <b>numero F</b>. |
| <b>Esposizione (EV)</b> *Mobile* | Quantità di luce che raggiunge il sensore della fotocamera, ovvero l&#39;intensità della luce nel rendering.<br><br>Con un valore inferiore si ottiene una scena renderizzata più scura.<br><br>Il &#39;valore di esposizione&#39; (EV) si riferisce specificamente alla quantità di luce a cui il sensore della fotocamera è <i>esposto</i>. |
| <b>Colore di base</b> *Float3* | Colore di base di default per le superfici in cui tale colore non è definito dalla relativa funzione SDF o di intersezione. |
| <b>Rugosità</b> *Mobile* | Valore di default della rugosità per le superfici in cui tale valore non è definito dalla relativa funzione SDF o intersezione. |
| <b>Metallicità</b> *Mobile* | Valore di default della metalness per le superfici in cui tale valore non è definito dalla relativa funzione SDF o di intersezione. |
| <b>Opacità helpers</b> *Mobile* | Opacità degli helper 3D, dove un valore inferiore genera helper sfocati. |
| <b>Fotogramma di delimitazione</b> *Booleano* | Visualizzazione di una gabbia a sei lati che definisce i limiti dell&#39;intera scena. Dovrebbe idealmente essere della dimensione più piccola possibile che includa completamente la scena.<br><br>Utilizzare il parametro <b>Dimensioni fotogramma limite</b> per regolare le dimensioni della gabbia.<br><br>Il parametro <b>Colora fuori cornice</b> consente di visualizzare facilmente le superfici esterne a quella gabbia, il che influisce sul risultato dell&#39;utilizzo di quella scena nel nodo [Splatter forma v2](../../../texture-generators/patterns/shape-splatter-v2/shape-splatter-v2.md). (Consulta la descrizione &quot;Dimensione fotogramma limite&quot;) |
| <b>Dimensioni fotogramma di delimitazione</b> *Float3* | Imposta le dimensioni XYZ del riquadro di delimitazione.<br><br>Regolate l&#39;inquadratura sulla scena, quindi applicate gli stessi valori al parametro <b>Dimensione fotogramma associata SDF</b> del nodo [splatter forma v2](../../../texture-generators/patterns/shape-splatter-v2/shape-splatter-v2.md) per garantire che tutte le forme nella scena siano correttamente incluse e disegnate da tale nodo. |
| <b>Colorazione fuori cornice</b> *Booleano* | Applica un colore rosso alle superfici esterne al riquadro di delimitazione.<br><br>In questo modo è possibile verificare che la scena sia completamente inclusa nel riquadro di delimitazione. |
| <b>Asse</b> *Booleano* | Visualizzazione degli assi XYZ della scena come linee colorate a partire dall&#39;origine della scena. |
| <b>Griglia</b> *Booleano* | Visualizzazione di una griglia posizionata sugli assi XY, in cui la dimensione di una cella in X e Y è un&#39;unità di scena. |
| <b>Assistenti trasformazione</b> *Booleano* | Visualizzazione dell&#39;ultima rotazione applicata.<br><br>La visualizzazione include<br>- <b>Una freccia</b> che rappresenta il vettore di direzione dell&#39;asse di rotazione e colorata dopo gli spessori di ciascun asse dello spazio mondo.<br>- <b>Un arco</b> che rappresenta l&#39;angolo di rotazione, ortogonale alla freccia che corrisponde al suo colore. |
| <b>Isoline SDF</b> *Booleano* | Una visualizzazione colorata delle isolinee della funzione SDF (signed distance field).<br><br>Le isolinee sono linee ripetute regolarmente che rappresentano il <i>campo distanza</i> della forma sul piano XY in un determinato height.<br><br>Queste impostazioni sono utili per controllare l&#39;<i>uniformità dello spazio</i> definito dalla Funzione SDF.<br><br>Utilizzare i parametri <b>Frequenza delle isolinee SDF</b> e <b>Posizione delle isolinee SDF</b> per regolare la densità e il height delle isolinee. |
| <b>Frequenza isolinee SDF</b> *Mobile* | Quantità di ripetizioni isolinea entro una determinata distanza.<br><br>Un valore più elevato determina linee più dense e sottili. |
| <b>Posizione isolinee SDF</b> *Mobile* | Il height spaziale mondiale del piano XY utilizzato per disegnare le isolinee.<br><br>Utilizzare questa opzione per controllare il campo distanza della forma a varie quote altimetriche. |
| <b>Min. distanza di accesso</b> *Virgola mobile* | Definisce la distanza minima che si traduce in un hit per il processo di marching dei raggi SDF.<br><br>Un valore basso aumenterà il numero di passaggi di marching dei raggi. |

## Esempi

<table style="border: none;">
    <tr style="width: 50%;">
        <td style="text-align: center">
            <img src="3d-viewer.resources/3d-viewer-example-01.jpg" alt="Esempio 1" />
        </td>
        <td style="width: 50%;">
            <table style="border: none;">
                <tr style="vertical-align: top;">
                    <td style="text-align: center">
                        <img src="3d-viewer.resources/3d-viewer-example-02a.jpg" alt="Esempio 1" />
                    </td>
                    <td style="text-align: center">
                        <img src="3d-viewer.resources/3d-viewer-example-02b.jpg" alt="Esempio 2" />
                    </td>
                </tr>
                <tr style="vertical-align: top;">
                    <td style="text-align: center">
                        <img src="3d-viewer.resources/3d-viewer-example-02c.jpg" alt="Esempio 3" />
                    </td>
                    <td style="text-align: center">
                        <img src="3d-viewer.resources/3d-viewer-example-02d.jpg" alt="Esempio 4" />
                    </td>
                </tr>
            </table>
    </tr>
</table>
