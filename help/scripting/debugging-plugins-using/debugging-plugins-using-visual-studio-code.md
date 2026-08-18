---
helpx_url: "https://helpx.adobe.com/it/substance-3d-designer/scripting/debugging-plugins-using-visual-studio-code.html"
breadcrumb-title: ''
description: Scopri come eseguire il debug dei plug-in Substance 3D Designer Python utilizzando Visual Studio Code per uno sviluppo efficiente.
helpx_creative_field: ""
helpx_description: Designer > Scripting > Debugging plugins using Visual Studio Code
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Debug dei plug-in con Visual Studio Code
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 0%

---


# Debug dei plug-in con Visual Studio Code

Come standard del flusso di lavoro per molti sviluppatori, l&#39;**IDE codice Visual Studio** è disponibile per il debug dei plug-in Python.

>[!WARNING]
>
> Il metodo <b>debugpy.Listen()</b> può consentire a chiunque sia in grado di connettersi alla porta specificata di eseguire codice arbitrario all&#39;interno del processo sottoposto a debug.
> 
> Pertanto, il debug deve essere *<b>solo</b>* configurato ed eseguito su *reti sicure*.

Per impostare la sinergia tra Visual Studio Code e Substance 3D Designer, eseguire la procedura seguente:

1. Installare **[Visual Studio Code](https://code.visualstudio.com/)** e **[Python extension](https://marketplace.visualstudio.com/items?itemName=ms-python.python)**.
1. Installare il modulo **[debugpy Python](https://github.com/microsoft/debugpy)**.

   >[!NOTE]
   >
   > Verificare che l&#39;interprete Python in Designer sia in grado di trovare il modulo &#39;*debugpy*&#39;. Il modo più semplice per eseguire questa operazione consiste nell&#39;aggiungere la directory in cui si trova il modulo &#39;*debug*&#39; alla variabile di ambiente **PYTHONPATH**. In alternativa, modificare sys.path nello script per aggiungere il percorso al modulo di debug.
1. Avvia l&#39;applicazione, apri l&#39;editor Python ed **esegui il codice seguente**:

   ```
   import sys 
   
   
   
   debugpy_path = '/path/to/debugpy/module' 
   
   debugpy_port = 5678 
   
   designer_py_interpreter = '/path/to/python/executable/bundled/in/designer' 
   
   
   
   if not debugpy_path in sys.path: 
   
       sys.path.append(debugpy_path) 
   
   
   
   import debugpy 
   
   
   
   debugpy.configure(python=designer_py_interpreter) 
   
   debugpy.listen(debugpy_port)
   ```

1. In Visual Studio Code, apri il progetto e crea un file **launch.json**. Aggiungi quanto segue al file:

   ```
   { 
   
       "name": "Attach to Designer", 
   
       "type": "python", 
   
       "request": "attach", 
   
       "port": <port number used in the script above>, 
   
       "host": "127.0.0.1" 
   
   }
   ```

1. Se necessario, fai clic sull&#39;icona <b>Debug</b> per creare o modificare la configurazione del debugger.
1. Selezionare la configurazione **Python: Attach to Designer** e fare clic su **Start Debugging**.

   È ora possibile impostare i punti di interruzione, scorrere il codice e utilizzare tutte le altre funzionalità del debugger di Visual Studio Code.
