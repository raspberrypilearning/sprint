## En sus marcas...

Empecemos por crear una cuenta regresiva de carreras.

--- task ---

Abre el proyecto de iniciación de Scratch '¡Carrera!'.

**En línea**: abre el [proyecto de iniciación](http://rpf.io/sprint-on){:target="_blank"}.

Si tienes una cuenta de Scratch puedes hacer una copia haciendo clic en **Reinventar**.

**Sin conexión**: abre el [proyecto de iniciación](http://rpf.io/p/en/sprint-go){:target=_blank"} en el editor sin conexión.

Si necesitas descargar e instalar el editor sin conexión de Scratch, puedes encontrarlo en [rpf.io/scratchoff](http://rpf.io/scratchoff){:target="_blank"}.

En el proyecto de iniciación, deberías ver una carretera y una línea de meta.

![proyectos de iniciación](images/sprint-starter.png)

--- /task ---

--- task ---

Para empezar, pongamos la línea de meta en el horizonte:

![objeto línea de meta](images/finish-line-sprite.png)

```blocks3
when green flag clicked
go to x: (0) y: (30)
set size to (1) %
```

--- /task ---

--- task ---

Si haces clic en la bandera para probar tu código, verás tu línea de meta en la distancia.

![línea de meta en la distancia](images/sprint-line-start-test-annotated.png)

--- /task ---

--- task ---

A continuación, utiliza bloques `decir`{:class="block3looks"} para crear una cuenta regresiva y luego enviar un mensaje para `iniciar`{:class="block3events"}.

![objeto línea de meta](images/finish-line-sprite.png)

```blocks3
when green flag clicked
go to x: (0) y: (30)
set size to (1) %
+say [3] for (1) seconds
+say [2] for (1) seconds
+say [1] for (1) seconds
+broadcast (start v)
```

--- /task ---

--- task ---

También puedes añadir un sonido a tu cuenta regresiva.

![objeto línea de meta](images/finish-line-sprite.png)

```blocks3
when green flag clicked
go to x: (0) y: (30)
set size to (1) %
say [3] for (1) seconds
say [2] for (1) seconds
say [1] for (1) seconds
+start sound (Siren Whistle v)
broadcast (start v)
```

--- /task ---
