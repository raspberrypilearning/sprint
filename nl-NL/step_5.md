## Landschap toevoegen

Laten we een boom coderen om te bewegen terwijl de speler sprint.

--- task ---

Plaats eerst de boom en maak deze klein wanneer op de vlag wordt geklikt.

![boom sprite](images/tree-sprite.png)

```blocks3
when green flag clicked
show
go to x: (-50) y: (20)
set size to (1) %
```

--- /task ---


--- task ---

Zodra de race begint, moet de boom bewegen totdat de speler 100 meter heeft gesprint.

![boom sprite](images/tree-sprite.png)

```blocks3
when I receive [start v]
repeat until <(distance :: variables) = [100]>
end

```

--- /task ---

--- task ---

Zodra de linkertoets is ingedrukt (en losgelaten), moet de boom groter worden en bewegen - net als de eindstreep.

![boom sprite](images/tree-sprite.png)

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

Als je je boom test, zul je zien dat hij naar beneden beweegt, de weg op.

![boom verplaatst naar de weg](images/sprint-tree-bug.png)

--- /task ---

--- task ---

Om dit te verhelpen, voeg je code toe om je boom een beetje van de weg af te laten bewegen.

![boom sprite](images/tree-sprite.png)

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

Je moet dan hetzelfde doen voor de rechterpijltoets. Zo zou de code van je Boom eruit moeten zien:

![boom sprite](images/tree-sprite.png)

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

