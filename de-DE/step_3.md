## Die Entfernung überbrücken

Verschieben wir die Ziellinie, wenn die Pfeiltasten gedrückt werden.

--- task ---

Wir möchten dem Spieler erlauben, die Pfeiltasten zu drücken __bis er 100 Meter__ gelaufen ist. Erstelle dazu eine neue Variable mit dem Namen `Distanz`{:class="block3variables"}.

[[[generic-scratch3-add-variable]]]

--- /task ---

--- task ---

Du solltest die neue Variable auf der Bühne sehen. Ziehe sie in die obere rechte Ecke.

![Screenshot](images/sprint-distance-drag.png)

--- /task ---

--- task ---

Setze den `Distanz`{:class="block3variables"} auf 0, wenn auf die Flagge geklickt wird.

![Ziellinienfigur](images/finish-line-sprite.png)

```blocks3
when green flag clicked
+set [Distanz v] to [0]
go to x: (0) y: (30)
set size to (1) %
```

--- /task ---

--- task ---

Sobald das Rennen beginnt, soll der Spieler __sprinten bis er 100 Meter gelaufen__.

![Ziellinienfigur](images/finish-line-sprite.png)

```blocks3
when I receive [start v]
repeat until <(Distanz :: variables) = [100]>
end 
```

--- /task ---

--- task ---

Füge einen weiteren Code hinzu, damit deine Ziellinie etwas größer wird, nachdem der Spieler die linke Pfeiltaste gedrückt hat. Der Abstand sollte ebenfalls zunehmen.

![Ziellinienfigur](images/finish-line-sprite.png)

```blocks3
when I receive [start v]
repeat until <(Distanz :: variables) = [100]>
+wait until <key (left arrow v) pressed?>
+ change size by (1)
+ change [Distanz v] by (1)
end 
```

--- /task ---

--- task ---

Klick auf die grüne Flagge, um dein Projekt zu testen. Du solltest sehen, dass die Ziellinie größer wird wenn der linke Pfeil gedrückt wird, sich aber nicht entlang der Strecke bewegt.

![Ziellinie ist größer, aber an der gleichen Stelle](images/sprint-line-bug.png)

--- /task ---

--- task ---

Um dies zu beheben, kannst du Code hinzufügen, um die Ziellinie bei jedem Tastendruck leicht nach unten zu verschieben.

![Ziellinienfigur](images/finish-line-sprite.png)

```blocks3
when I receive [start v]
repeat until <(Distanz :: variables) = [100]>
wait until <key (left arrow v) pressed?>
change size by (1)
+change y by (-1.5)
change [Distanz v] by (1)
end 
```

--- /task ---

--- task ---

Teste dein Projekt erneut und du solltest sehen, wie sich die Ziellinie die Bühne hinunter auf dich zu bewegt.

![Ziellinien bewegen sich die Straße hinunter](images/sprint-line-fix-test.png)

--- /task ---

--- task ---

Du solltest das auch für die rechte Pfeiltaste tun.

![Ziellinienfigur](images/finish-line-sprite.png)

```blocks3
when I receive [start v]
repeat until <(Distanz :: variables) = [100]>
wait until <key (left arrow v) pressed?>
change size by (1)
change y by (-1.5)
change [Distanz v] by (1)
+wait until <key (right arrow v) pressed?>
+change size by (1)
+change y by (-1.5)
+change [Distanz v] by (1)
end 
```

--- /task ---

--- task ---

Wenn Du auf den Reiter Kostüme klickst, siehst Du, dass es dort zwei Ziellinien gibt.

![2 Kostüme](images/sprint-line-costumes.png)

--- /task ---

--- task ---

Du kannst am Ende des Rennens zum Kostüm 'gebrochen' wechseln (und das Spiel beenden). Denke daran zu Beginn des Rennens zum Kostüm „normal“ zu wechseln!

![Ziellinienfigur](images/finish-line-sprite.png)

```blocks3
when I receive [start v]
repeat until <(Distanz :: variables) = [100]>
wait until <key (left arrow v) pressed?>
change size by (1)
change y by (-1.5)
change [Distanz v] by (1)
wait until <key (right arrow v) pressed?>
change size by (1)
change y by (-1.5)
change [Distanz v] by (1)
end 
+switch costume to (gebrochen v)
+stop [all v]
```

```blocks3
when green flag clicked
+switch costume to (normal v)
set [Distanz v] to [0]
```

--- /task ---

--- task ---

Wenn du am Ende einen Klang abspielen möchtest, musst du den Block `stoppe alle`{:class="block3control"} in `stoppe andere Skripte der Figur`{:class="block3control"} ändern.

Dies bedeutet, dass der Timer aufhört zu zählen, der Sound jedoch weiterhin abgespielt wird.

![Ziellinienfigur](images/finish-line-sprite.png)

```blocks3
switch costume to (gebrochen v)
+ stop [other scripts in sprite v]
+ start sound (cheer v)
```

--- /task ---

Hast Du bemerkt, dass man beim Spiel betrügen kann, indem man einfach die linke und rechte Pfeiltaste gedrückt hält?

--- task ---

Um das zu beheben, musst du sicherstellen, dass jede Taste gedrückt __und dann losgelassen__ wird, bevor die Ziellinie verschoben wird.

Hier ist der Code, den du hinzufügen musst:

![Ziellinienfigur](images/finish-line-sprite.png)

```blocks3
wait until <key (left arrow v) pressed?>
+wait until <not <key (left arrow v) pressed?>>
change size by (1)
```

Dasselbe musst du für die rechte Pfeiltaste tun.

![Ziellinienfigur](images/finish-line-sprite.png)

```blocks3
wait until <not <key (right arrow v) pressed?>>
```

--- /task ---
