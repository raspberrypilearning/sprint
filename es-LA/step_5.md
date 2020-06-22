## Añadiendo el paisaje

Vas a programar un árbol para que se mueva a medida que el jugador corre.

--- task ---

Primero, coloca el árbol y hazlo pequeño al hacer clic en la bandera.

![objeto árbol](images/tree-sprite.png)

```blocks3
when green flag clicked
show
go to x: (-50) y: (20)
set size to (1) %
```

--- /task ---


--- task ---

Una vez que comienza la carrera, el árbol debe moverse hasta que el jugador haya corrido 100 metros.

![objeto árbol](images/tree-sprite.png)

```blocks3
when I receive [start v]
repeat until <(distance :: variables) = [100]>
end

```

--- /task ---

--- task ---

Una vez que la tecla izquierda ha sido presionada (y soltada), el árbol debe hacerse más grande y moverse, al igual que la línea de meta.

![objeto árbol](images/tree-sprite.png)

```blocks3
when I receive [start v]
repeat until <(distance :: variables) = [100]>
+wait until <key (left arrow v) pressed?>
+wait until <not  <key (left arrow v) pressed?>>
+change size by (1)
+change y by (-1.5)
end
```

--- /task ---

--- task ---

Si pruebas tu árbol, verás que se mueve hacia abajo, hacia la pista.

![árbol movido a la pista](images/sprint-tree-bug.png)

--- /task ---

--- task ---

Para arreglar esto, añade código para hacer que tu árbol se aleje de la pista ligeramente.

![objeto árbol](images/tree-sprite.png)

```blocks3
when I receive [start v]
repeat until <(distance :: variables) = [100]>
wait until <key (left arrow v) pressed?>
wait until <not  <key (left arrow v) pressed?>>
change size by (1)
change y by (-1.5)
+change x by (-2)
end
```

--- /task ---

--- task ---

También debes hacer lo mismo para la tecla derecha. Así es como debería verse el código de tu árbol:

![objeto árbol](images/tree-sprite.png)

```blocks3
when green flag clicked
show
go to x: (-50) y: (20)
set size to (1) %

when I receive [start v]
repeat until <(distance :: variables) = [100]>
wait until <key (left arrow v) pressed?>
wait until <not  <key (left arrow v) pressed?>>
change size by (1)
change y by (-1.5)
change x by (-2)
wait until <key (right arrow v) pressed?>
wait until <not  <key (right arrow v) pressed?>>
change size by (1)
change y by (-1.5)
change x by (-2)
end
```

--- /task ---

