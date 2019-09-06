## ¿Donde configurarlo?
Existen 2 ambitos de configuración:
<div>
__&gt; System Wide__ - Los alias se aplican para todos los usuarios que tengan permiso de lectura en:
```
-rw-r--r-- 1 root root 1580 feb 10  2018 /etc/ssh/ssh_config
```
</div> <!-- .element: class="fragment fade-left" -->
<div>
__&gt; User Defined__ - Solo se aplican a nivel de cada usuario en este archivo:
```
~/.ssh/config = $HOME/.ssh/config = /home/youruser/.ssh/config
```
</div> <!-- .element: class="fragment fade-right" -->
*Dependiendo de la confidencialidad de la configuración es conveniente que el archivo a nivel de usuario tenga los permisos 0600* <!-- .element: class="fragment fade-right" -->
