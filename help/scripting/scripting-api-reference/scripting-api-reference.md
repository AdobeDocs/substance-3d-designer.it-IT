---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/scripting/scripting-api-reference.html"
breadcrumb-title: ''
description: Accedi alla documentazione completa relativa alle API di scripting di Substance 3D Designer Python per lo sviluppo di plug-in.
helpx_creative_field: ""
helpx_description: Designer > Scripting > Scripting API reference
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Riferimento API script
user-guide-description: ''
user-guide-title: ''
source-git-commit: f320cf6842ff56ac24912ceda264f30c28317c05
workflow-type: tm+mt
source-wordcount: '1251'
ht-degree: 0%

---


# Riferimento API script

Questa pagina descrive i concetti principali dell’API.

Per ulteriori informazioni, consulta la documentazione fornita con l’applicazione e accessibile in <b>Guida > Documentazione Python API...</b>. In questa documentazione, esegui una <b>ricerca rapida</b> per i nomi dei moduli (tra parentesi di seguito) per trovarne facilmente la definizione.

## Contesto

L&#39;oggetto contesto (*Context*) è il <b>punto di ingresso principale dell&#39;API</b>. Viene creato la prima volta che l&#39;utente lo ottiene utilizzando il metodo &#39;<b>*getContext()*</b>&#39; dal modulo &#39;*sd*&#39;.

Questo oggetto consente essenzialmente di <b>recuperare l&#39;oggetto applicazione</b> (*SDApplication*).

## Applicazione (SDApplication)

L&#39;applicazione (*SDApplication*) è l&#39;oggetto che consente a <b>l&#39;accesso ai principali gestori API</b>, ad esempio:

* <b>Package </b>Manager (*SDPackageMgr*) che gestisce tutti i <b>pacchetti</b> dell&#39;applicazione;
* <b>Modulo </b>Manager (*SDModuleMgr*) che gestisce tutti i <b>moduli</b> dell&#39;applicazione;
* <b>UI </b>Manager (*SDUIMgr*) che può creare <b>menu e dock</b> nella finestra dell&#39;applicazione.

È possibile registrare <b>callback</b> con l&#39;applicazione che verrà chiamata quando si verificano determinati eventi.

## Gestione pacchetti (SDPackageMgr)

Questo oggetto gestisce tutti i <b>pacchetti</b> dell&#39;applicazione. I pacchetti vengono visualizzati nel componente &#39;<b>*Explorer*</b>&#39;.

Consente di:

* <b>creare</b> un nuovo pacchetto;
* <b>caricare/scaricare</b> un pacchetto;
* <b>salvare</b> un pacchetto;
* <b>trova</b> un pacchetto.

## Pacchetto (SDPackage)

Un pacchetto (*SDPackage*) è una <b>raccolta di risorse</b> (*SDResource*).

Il contenuto di un pacchetto può essere <b>archiviato</b> in un file con estensione <b>.sbs</b> tramite l&#39;oggetto &#39;*SDPackageMgr*&#39;. Questo oggetto consente di <b>recuperare </b>risorse specifiche.

Per <b>creare</b> una risorsa specifica, vedere i metodi statici oggetto correlati (ad esempio: &#39;*SDSBSCompGraph.sNew()*&#39;).

Un pacchetto contiene anche un dizionario dei metadati (SDMetadataDict). Ulteriori informazioni sui metadati [sono disponibili qui](../../package-metadata/package-metadata.md).

## Risorsa (SDResource)

Una risorsa (*SDResource*) è un oggetto a cui un&#39;altra risorsa può fare riferimento <b></b>.

Sono presenti più <b>tipi</b> di risorsa:

* Cartelle (*SDResourceFolder*);
* grafici (*SDGraph*);
* Bitmap (*SDResourceBitmap*);
* Immagini SVG (*SDResourceSVG*);
* Font (*SDResourceFont*);
* Scene (*SDResourceScene*);
* Misurazioni BSDF (*SDResourceBSDFMeasurement*);
* Profili chiari (*SDResourceLightProfile*).

È possibile <b>creare</b> una risorsa dal metodo statico &#39;*sNew()*&#39; in:

* un collo;
* una cartella.

Una risorsa può avere diverse <b>proprietà</b> (*SDProperty*).

## Gestione interfaccia utente (SDUIMgr)

Il gestore dell&#39;interfaccia utente consente di <b>creare elementi dell&#39;interfaccia utente</b> nella finestra principale del Substance Designer, ad esempio <b>menu</b>, <b>docks</b> e di registrare <b>callback</b> da chiamare quando si verificano eventi correlati all&#39;interfaccia utente.

Inoltre, il gestore dell&#39;interfaccia utente ha accesso al <b>grafico attivo corrente</b> e alla <b>selezione</b> del grafico attivo.

## Grafici (SDGraph)

Un grafico (*SDGraph*) è un oggetto che contiene:

* <b>nodi </b>(*SDNode*);
* <b>oggetti grafici</b> (*SDGraphObjects*);
* <b>proprietà </b>(*SDProperty*).

Esistono 4 tipi di grafici diversi:

* Substance grafico (*SDSBSCompGraph*)
* Substance grafico funzioni (*SDSBSFunctionGraph*)
* Substance grafico FXMap (*SDSBSFxMapGraph*)

Un grafico può avere uno o più nodi <b>output</b>. I nodi di output rappresentano i <b>risultati</b> del grafico.

Tutti i nodi disponibili per un grafico possono essere <b>recuperati</b> con il metodo &#39;*getNodeDefinitions()*&#39;.

È possibile <b>creare</b> un nuovo nodo con il metodo &#39;*newNode()*&#39;.

È possibile creare un nuovo nodo <b>istanza</b> da una risorsa (*SDResource*) con il metodo &#39;*newInstanceNode()*&#39;.

## Nodo (SDNode)

Un nodo (*SDNode*) rappresenta una <b>operazione</b> eseguita su un oggetto.

Può essere creato da:

* una <b>definizione</b> (*SDDefinition*) (vedere &#39;*SDGraph.newNode()&#39;*);
* una <b>risorsa</b> (*SDResource*) (vedere &#39;*SDGraph.newInstanceNode()&#39;*).

Un nodo può avere più <b>proprietà</b>.

Sono presenti più <b>tipi</b> di nodo:

* *<b>SDSBSCompNode</b>*: nodo del Grafico Substance (*SDSBSCompGraph*);
* *<b>SDSBSFunctionNode</b>*: nodo del Grafico delle funzioni Substance (*SDSBSFunctionGraph*);
* *<b>SDSBSFxMapNode</b>*: nodo del grafico FXMap di Substance (*SDSBSFxMapGraph*);

## Oggetti grafico (SDGraphObjects)

Un oggetto grafico (*SDGraphObject*) è un oggetto che <b>aggiunge informazioni aggiuntive</b> al grafico, ma che è <b>*non* considerato</b> durante il processo di valutazione del grafico.

Esistono <b>3 tipi</b> di oggetti grafici:

* <b>Pin</b> (*SDGraphObjectPin*)
* <b>Commento</b> (*SDGraphObjectComment*)
* <b>Frame</b> (*SDGraphObjectFrame*)

Per ulteriori informazioni su come <b>crearli</b>, vedere il metodo statico &#39;*sNew()*&#39; su questi oggetti.

## Proprietà (SDProperty)

Una proprietà (*SDProperty*) è un oggetto che <b>descrive</b> una proprietà di <b>un altro oggetto</b> (un grafico, un nodo, una risorsa e così via).

Appartiene a una <b>categoria</b> specifica (*SDPropertyCategory*):

* <b>Input</b>: classifica le proprietà di input di un oggetto, che in genere <b> influiscono sull&#39;operazione</b> eseguita dall&#39;oggetto corrente;
  * Esempio: la proprietà &#39;*color*&#39; di un nodo Uniform Color in un grafico a Substance è una proprietà di input.
* <b>Output</b>: classifica le proprietà di output di un oggetto. Viene utilizzato per identificare un <b>risultato</b> di un oggetto;
* <b>Annotazione</b>: classifica le proprietà che <b>*non* influiscono sull&#39;operazione</b> eseguita da un oggetto;
  * Esempio: &#39;*label*&#39; di un grafico è una proprietà di annotazione, in quanto non influisce sul calcolo del grafico.

Contiene i seguenti <b>membri</b>:

* <b>Id</b>: identificatore della proprietà nel contesto della categoria;
* <b>Tipi</b>: tipi supportati dalla proprietà corrente. Alcune proprietà possono supportare *più* tipi: &#39;*int*&#39;, &#39;*float*&#39; e così via.;
  * Esempio: le proprietà di input di un nodo &#39;*sbs::function::add*&#39; possono supportare tipi diversi: &#39;*int&#39;*, &#39;*int2&#39;*, &#39;*int3&#39;*, &#39;*int4&#39;*, &#39;*float&#39;*, &#39;*float2&#39;*, &#39;*float3&#39;*, &#39;*float4&#39;, ecc.;*
* <b>Categoria</b>: la categoria a cui appartiene la proprietà (input, output, annotazione);
* <b>Etichetta</b>: etichetta della proprietà, utilizzata per visualizzare *solo*;
* <b>Descrizione</b>: descrizione della proprietà;
* <b>Valore predefinito</b>: valore predefinito;
* <b>IsConnectable</b>: indica se è possibile eseguire una connessione (*SDConnection*) *su questa proprietà;*
* <b>isReadyOnly</b>: indica se la proprietà è di sola lettura. Se è true, il valore associato *non* sarà modificabile;
* <b>isVariadic</b>: se è true, questa proprietà verrà rappresentata come proprietà *multiple* nell&#39;oggetto;
* <b>isPrimary</b>: indica se la proprietà specificata è la proprietà *principal* che controlla altre proprietà. *Nota:* specifica della Substance *Composizione* nodi (*SDSBSCompNode*).

Esempi:

* Proprietà del nodo &#39;*sbs::compositing::input*&#39;:

<table data-preserve-html="true"><colgroup><col style="width: 276.0px;"/><col style="width: 129.0px;"/><col style="width: 283.0px;"/></colgroup><tbody><tr><th colspan="3" style="text-align: center;">sbs::compositing::input</th></tr><tr><td style="text-align: left;"><strong>Input</strong></td><td style="text-align: left;"><strong>Annotazione</strong></td><td style="text-align: left;"><strong>Output</strong></td></tr><tr><td>$outputsize</td><td>etichetta</td><td><p>unique_filter_output (CONNETTIBILE)</p></td></tr><tr><td>$format</td><td>descrizione</td><td><br/></td></tr><tr><td>$pixelsize</td><td>identificatore</td><td><br/></td></tr><tr><td>$pixelratio</td><td>userdata</td><td><br/></td></tr><tr><td>$tiling</td><td>gruppo</td><td><br/></td></tr><tr><td>$randomseed</td><td>visibleif</td><td><br/></td></tr><tr><td><p>bitmapresourcepath</p></td><td>utilizzi</td><td><br/></td></tr></tbody></table>

* Proprietà del nodo &#39;*sbs::compositing::blend*&#39;:

<table data-preserve-html="true"><colgroup><col style="width: 278.0px;"/><col style="width: 129.0px;"/><col style="width: 283.0px;"/></colgroup><tbody><tr><th colspan="3" style="text-align: center;">sbs::compositing::blend</th></tr><tr><td style="text-align: left;"><strong>Input</strong></td><td style="text-align: left;"><strong>Annotazione</strong></td><td style="text-align: left;"><strong>Output</strong></td></tr><tr><td>$outputsize</td><td><br/></td><td>unique_filter_output (CONNETTIBILE)</td></tr><tr><td>$format</td><td><br/></td><td><br/></td></tr><tr><td>$pixelsize</td><td><br/></td><td><br/></td></tr><tr><td>$pixelratio</td><td><br/></td><td><br/></td></tr><tr><td>$tiling</td><td><br/></td><td><br/></td></tr><tr><td>$randomseed</td><td><br/></td><td><br/></td></tr><tr><td>source.connector (COLLEGABILE)</td><td><br/></td><td><br/></td></tr><tr><td><p>destination.connector (CONNETTIBILE)</p></td><td><br/></td><td><br/></td></tr><tr><td>opacity.connector (COLLEGABILE)</td><td><br/></td><td><br/></td></tr><tr><td>opacitimulto</td><td><br/></td><td><br/></td></tr><tr><td colspan="1">metodo fusione</td><td colspan="1"><br/></td><td colspan="1"><br/></td></tr><tr><td colspan="1">colorblending</td><td colspan="1"><br/></td><td colspan="1"><br/></td></tr><tr><td colspan="1">maskrectangle</td><td colspan="1"><br/></td><td colspan="1"><br/></td></tr></tbody></table>

## Tipo (SDType)

Un tipo (*SDType*) contiene informazioni di un valore <b>type</b>, ad esempio:

* <b>Id</b>: identificatore del tipo;
* <b>Modificatore</b>: modificatore di tipo che può essere uno dei valori &#39;*SDTypeModifier&#39;* <b>enum</b>:
  * *Automatico*;
  * *Uniforme*: il valore viene valutato *una volta* per operazione;
  * *Variabile*: il valore viene valutato *più volte* per operazione (ad esempio, per ogni testo).

Sono definiti più tipi, ad esempio:

* <b>enum</b> (*SDTypeEnum*): descrive un tipo <b>enumerazione</b> con tutte le relative proprietà;
* <b>strutture</b> (*SDTypeStruct*): descrive un tipo <b>struttura</b> con tutte le relative proprietà;
* <b>matrice</b> (*SDTypeArray*): descrive una <b>matrice</b>.
* ecc.

Per un elenco completo, consulta la *documentazione Python API* del Substance Designer.

## Valori (SDValue)

Un valore (*SDValue*) è un oggetto che <b>incapsula</b> un valore di *tipo base*.

Ad esempio:

* un oggetto &#39;<b>*SDValueInt*</b>&#39; incapsula un valore &#39;*int*&#39;;
* un oggetto &#39;<b>*SDValueFloat4*</b>&#39; incapsula un valore &#39;*float4*&#39;;
* ecc.

Il valore del tipo di base può essere in genere <b>recuperato</b> con il metodo &#39;<b>get()</b>&#39;, ma può dipendere dal *tipo* di &#39;*SDValue&#39;* restituito.

## Connessione (SDConnection)

Una connessione (*SDConnection*) rappresenta un <b>collegamento</b> tra due diverse<b> proprietà</b> di due diversi <b>nodi</b>.

Contiene:

* <b>nodo di destinazione</b>;
* <b>proprietà di destinazione</b> del nodo di destinazione;

Tutte le <b>operazioni di connessione</b> vengono eseguite in un nodo:

* <b>creazione</b> di una nuova connessione. Vedere &#39;*SDNode.newPropertyConnection()*&#39;
* <b>eliminazione</b> di una connessione esistente. Vedere &#39;*SDNode.deletePropertyConnection()*&#39;
* <b>recupero</b> delle connessioni di una proprietà. Vedere &#39;*SDNode.getPropertyConnections()*&#39;

## Modulo (SDModule)

Un modulo è una <b>raccolta di definizioni e tipi</b>.

Consente di recuperare facilmente tutte le informazioni sui nodi che è possibile creare, nonché su enumerazioni e strutture.

Contiene:

* un <b>identificatore</b> (*Id*) univoco nel contesto del gestore del modulo (*SDModuleMgr*);
* un elenco di <b>definizioni</b> (*SDDefinition*);
* un elenco di <b>tipi</b> (*SDType*).

## Definizione (definizione SDD)

Un oggetto definizione (*SDDefinition*) contiene informazioni sulla definizione di un particolare <b>oggetto</b> in base a <b>proprietà</b> (&#39;*SDNode&#39;* e così via).

Contiene:

* <b>Id</b>: identificatore della definizione;
* <b>Etichetta</b>: etichetta della definizione;
* <b>Descrizione</b>: descrizione della definizione;
* <b>Proprietà</b>: proprietà di tutte le proprietà disponibili *categorie* (*SDPropertyCategory*).
