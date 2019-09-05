#### MySQL over SSH
Crea el forwarding al servidor:

`ssh -L 8934:127.1:3306 root@iberdrola-prod`

<p>Esto entra en la shell, si solo quieres crear la conexión añade `-fN`</p> <!-- .element: class="fragment fade-left" -->

`ssh -fN -L 8934:127.1:3306 root@iberdrola-prod` <!-- .element: class="fragment fade-left" -->
```
ver man page (manual):
$ man ssh | grep -- -f # Requests ssh to go to background just before command execution...
$ man ssh | grep -- -N # Do not execute a remote command. This is useful for just forwarding ports...
```
<!-- .element: class="fragment fade-right" -->

<br>
<p>Ahora conectate en localhost al __puerto 8934__</p>  <!-- .element: class="fragment fade-left" -->

<div>
¿Por qué 8934? | La pregunta es... ¿Por qué NO?<br><br>
`mysql -uroot -p -P 8934`
</div>  <!-- .element: class="fragment fade-left" -->

<br>
*'Ya eres un acker sin H'*
