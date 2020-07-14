## Landschaft hinzufügen

Lass uns einen Baum codieren, der sich bewegt, wenn der Spieler sprintet.

--- task ---

Positioniere zuerst den Baum und verkleinere ihn, wenn du auf die Flagge klickst.

![Baumfigur](images/tree-sprite.png)

```blocks3
when green flag clicked
show
go to x: (-50) y: (20)
set size to (1) %
```

--- /task ---


--- task ---

Sobald das Rennen beginnt, sollte sich der Baum bewegen, bis der Spieler die 100 Meter gesprintet ist.

![Baumfigur](images/tree-sprite.png)

```blocks3
when I receive [start v]
repeat until <(Distanz :: variables) = [100]>
end

```

--- /task ---

--- task ---

Sobald die linke Taste gedrückt (und losgelassen) wurde, sollte der Baum größer werden und sich bewegen - genau wie die Ziellinie.

![Baumfigur](images/tree-sprite.png)

```blocks3
when I receive [start v]
repeat until <(Distanz :: variables) = [100]>
+wait until <key (left arrow v) pressed?>
+wait until <not  <key (left arrow v) pressed?>>
+change size by (1)
+change y by (-1.5)
end
```

--- /task ---

--- task ---

Wenn Du den Baum testest, wirst Du feststellen, dass er sich auf dem Weg nach unten bewegt.

![Baum bewegte sich auf dem Weg](images/sprint-tree-bug.png)

--- /task ---

--- task ---

Um das zu beheben, füge einwen Code hinzu, damit sich der Baum leicht vom Weg entfernt.

![Baumfigur](images/tree-sprite.png)

```blocks3
when I receive [start v]
repeat until <(Distanz :: variables) = [100]>
wait until <key (left arrow v) pressed?>
wait until <not  <key (left arrow v) pressed?>>
change size by (1)
change y by (-1.5)
+change x by (-2)
end
```

--- /task ---

--- task ---

Mach das gleiche auch für die rechte Pfeiltaste. So sollte der Code deines Baums aussehen:

![Baumfigur](images/tree-sprite.png)

```blocks3
when green flag clicked
show
go to x: (-50) y: (20)
set size to (1) %

when I receive [start v]
repeat until <(Distanz :: variables) = [100]>
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

