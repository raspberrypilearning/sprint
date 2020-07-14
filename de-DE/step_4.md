## Wer ist der Schnellste?

Lass uns deinem Spiel einen Timer hinzufügen, um zu sehen, wer am schnellsten Sprinten kann.

--- task ---

Erstelle eine neue `Zeit`{:class="block3variables"} Variable. Die Variable wird auf der Bühne erscheinen. Ziehe sie in die obere linke Ecke.

![Zeitvariable in der Mitte der Bühne](images/sprint-timer-create.png)

--- /task ---

--- task ---

Setze die Zeit zu Beginn deines Spiels auf 0.

![Ziellinienfigur](images/finish-line-sprite.png)

```blocks3
when green flag clicked
switch costume to (normal v)
set [Distanz v] to [0]
+ set [Zeit v] to [0]
go to x: (0) y: (30)
set size to (1) %
```

--- /task ---

--- task ---

Füge diesen Code hinzu, damit der Timer zu Beginn des Spiels hochzählt.

![Ziellinienfigur](images/finish-line-sprite.png)

```blocks3
when I receive [start v]
forever
wait (0.1) seconds
change [Zeit v] by (0.1)
end
```

--- /task ---

--- task ---

Teste Dein Projekt, indem Du auf die grüne Flagge klickst. Du solltest sehen, dass der Timer bis zu 100 Meter zählt.

![Zeit- und Distanzvariablen auf der Bühne](images/sprint-timer-test.png)

--- /task ---

