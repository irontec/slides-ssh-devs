#### VNC *vs* TeamViewer (Medio)
<div>
Servidor con __x11vnc__:<br><br>
`x11vnc -listen 127.1 -passwd changemeplz -forever -display $DISPLAY -viewonly`
</div> <!-- .element: class="fragment fade-left" -->

<div>
Comprueba el puerto de x11vnc
```
$ netstat -lputan | grep x11vnc
tcp        0      0 127.0.0.1:5900          0.0.0.0:*               LISTEN      PID/x11vnc        
tcp6       0      0 :::5900                 :::*                    LISTEN      PID/x11vnc
```
</div> <!-- .element: class="fragment fade-left" -->

<br>
<div>
Cliente con __xtightvncviewer__:
<p>`ssh -fN -L 9005:127.1:5900 niko@10.10.0.230`</p>
</div> <!-- .element: class="fragment fade-right" -->

<div>
¿Por qué eliges 9005? | La pregunta es... ¿Por qué NO?
<p>`vncviewer 127.1:9005`</p>
</div>  <!-- .element: class="fragment fade-right" -->

<br>
*127.1 = 127.0.0.1 = localhost*
