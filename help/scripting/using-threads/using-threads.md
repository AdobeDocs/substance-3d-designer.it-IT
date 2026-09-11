---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/scripting/using-threads.html"
breadcrumb-title: ''
description: Scoprite come utilizzare i thread nello scripting Substance 3D Designer Python per l’elaborazione e le prestazioni in parallelo.
helpx_creative_field: ""
helpx_description: Designer > Scripting > Using threads
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Utilizzo dei thread
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 0%

---


# Utilizzo dei thread

È possibile che i plug-in <b>creino thread</b> utilizzando il modulo di threading Python *o* Qt per le classi relative al threading Python.

Questa funzione può essere utile per eseguire elaborazioni in background o operazioni di I/O mentre Designer è in esecuzione.

È importante notare che la maggior parte delle classi e dei metodi nell&#39;API Python di Designer può essere chiamata *solo* dal <b>thread principale dell&#39;applicazione</b>. Di conseguenza, se desiderate apportare modifiche a qualsiasi grafico attualmente aperto in Designer, dovete crearli dal thread dell’applicazione principale.

Una soluzione possibile consiste nell&#39;utilizzare <b>QThread</b> e <b>connessioni in coda</b>, come nell&#39;esempio seguente:

```
import time 

from PySide2 import QtCore 

 

 

## Our thread object.

class TimerThread(QtCore.QThread): 

    tick = QtCore.Signal() 

 

    def run(self): 

        for i in range(0, 7): 

            print("Emitting signal from thread %s" % QtCore.QThread.currentThread()) 

            self.tick.emit() 

            time.sleep(0.5) 

 

 

## Our receiver object, created on the main thread.

class Receiver(QtCore.QObject): 

    def __init__(self, parent=None): 

        super(Receiver, self).__init__(parent) 

 

    def onTick(self): 

## This is called on the main thread. It is safe to use the sd API here.

        print("Tick received in thread %s" % QtCore.QThread.currentThread()) 

 

 

timer = TimerThread() 

receiver = Receiver() 

 

## Use QtCore.Qt.QueuedConnection to make sure that slots are called on the main thread.

## You can also use QtCore.Qt.BlockingQueuedConnection if you need to block while the slot is called.

timer.tick.connect(receiver.onTick, QtCore.Qt.QueuedConnection) 

 

## Start out thread.

timer.start()
```
