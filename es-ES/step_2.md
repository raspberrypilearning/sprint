## A sus marcas...

Empecemos por crear una cuenta atrás para el comienzo de la carrera.

--- task ---

Abre el proyecto inicial Sprint (Carrera).

**Online**: abre el [poryecto de iniciación](https://scratch.mit.edu/projects/406794421){:target="_blank"}.

Si tienes una cuenta de Scratch puedes hacer una copia haciendo clic en **Reinventar**.

**Offline**: abre el [proyecto de iniciación](https://rpf.io/p/es-ES/sprint-go){:target=_blank"} en el editor offline.

Si necesitas descargar e instalar el editor offline de Scratch, puedes encontrarlo en [rpf.io/scratchoff](https://rpf.io/scratchoff){:target="_blank"}.

En el proyecto inicial deberías ver un camino y una línea de llegada.

![proyectos para comenzar](images/sprint-starter.png)

--- /task ---

--- task ---

Para empezar, pongamos la línea de meta en el horizonte:

![objeto línea de llegada](images/finish-line-sprite.png)

```blocks3
when green flag clicked
go to x: (0) y: (30)
set size to (1) %
```

--- /task ---

--- task ---

Si haces clic en la bandera para probar tu código, verás tu línea de llegada en la distancia.

![línea de llegada en la distancia](images/sprint-line-start-test-annotated.png)

--- /task ---

--- task ---

A continuación, usa bloques `decir`{:class="block3looks"} para crear una cuenta atrás y luego enviar un mensaje `salida`{:class="block3events"}.

![objeto línea de llegada](images/finish-line-sprite.png)

```blocks3
when green flag clicked
go to x: (0) y: (30)
set size to (1) %
+say [3] for (1) seconds
+say [2] for (1) seconds
+say [1] for (1) seconds
+broadcast (salida v)
```

--- /task ---

--- task ---

También puedes añadir un sonido a tu cuenta atrás.

![objeto línea de llegada](images/finish-line-sprite.png)

```blocks3
when green flag clicked
go to x: (0) y: (30)
set size to (1) %
say [3] for (1) seconds
say [2] for (1) seconds
say [1] for (1) seconds
+start sound (Siren Whistle v)
broadcast (salida v)
```

--- /task ---
