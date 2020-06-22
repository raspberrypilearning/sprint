## Die Entfernung überbrücken

Verschieben wir die Ziellinie, wenn die Pfeiltasten gedrückt werden.

--- task ---

Wir möchten dem Spieler erlauben, die Pfeiltasten zu drücken __bis er 100 Meter__ gelaufen ist. Erstelle dazu eine neue Variable mit dem Namen `Distanz`{:class="block3variables"}.

[[[generic-scratch3-add-variable]]]

--- /task ---

--- task ---

Du solltest die neue Variable auf der Bühne sehen. Ziehe sie in die obere rechte Ecke.

![screenshot](images/sprint-distance-drag.png)

--- /task ---

--- task ---

Setze den `Abstand`{:class="block3variables"} auf 0, wenn auf die Flagge geklickt wird.

![finish line sprite](images/finish-line-sprite.png)

```blocks3
Wenn die grüne Flagge angeklickt wird 
+setze [distance v] auf [0]
gehe zu x: (0) y: (30)
setze Größe auf (1) %
```

--- /task ---

--- task ---

Sobald das Rennen beginnt, soll der Spieler __sprinten bis er 100 Meter gelaufen__.

![finish line sprite](images/finish-line-sprite.png)

```blocks3
when I receive [start v]
repeat until <(distance :: variables) = [100]>
end 
```

--- /task ---

--- task ---

Füge einen weiteren Code hinzu, damit deine Ziellinie etwas größer wird, nachdem der Spieler die linke Pfeiltaste gedrückt hat. Der Abstand sollte ebenfalls zunehmen.

![finish line sprite](images/finish-line-sprite.png)

```blocks3
when I receive [start v]
repeat until <(distance :: variables) = [100]>
+wait until <key (left arrow v) pressed?>
+ change size by (1)
+ change [distance v] by (1)
end 
```

--- /task ---

--- task ---

Click the green flag to test your project. You should see that the finish line gets bigger when the left arrow is pressed, but doesn't move along the track.

![finish line is bigger but in the same place](images/sprint-line-bug.png)

--- /task ---

--- task ---

To fix this, you can add code to move the finish line down slightly each time a key is pressed.

![finish line sprite](images/finish-line-sprite.png)

```blocks3
when I receive [start v]
repeat until <(distance :: variables) = [100]>
wait until <key (left arrow v) pressed?>
change size by (1)
+change y by (-1.5)
change [distance v] by (1)
end 
```

--- /task ---

--- task ---

Test your project again and you should see the finish line move down the stage towards you.

![finish lines moves down the road](images/sprint-line-fix-test.png)

--- /task ---

--- task ---

You should then do the same for the right arrow key.

![finish line sprite](images/finish-line-sprite.png)

```blocks3
when I receive [start v]
repeat until <(distance :: variables) = [100]>
wait until <key (left arrow v) pressed?>
change size by (1)
change y by (-1.5)
change [distance v] by (1)
+wait until <key (right arrow v) pressed?>
+change size by (1)
+change y by (-1.5)
+change [distance v] by (1)
end 
```

--- /task ---

--- task ---

If you click to see the finish line's costumes, you should see that there are 2.

![2 costumes](images/sprint-line-costumes.png)

--- /task ---

--- task ---

You can switch to the 'broken' costume (and end the game) at the end of the race. Remember to switch to the 'normal' costume at the start of the race!

![finish line sprite](images/finish-line-sprite.png)

```blocks3
when I receive [start v]
repeat until <(distance :: variables) = [100]>
wait until <key (left arrow v) pressed?>
change size by (1)
change y by (-1.5)
change [distance v] by (1)
wait until <key (right arrow v) pressed?>
change size by (1)
change y by (-1.5)
change [distance v] by (1)
end 
+switch costume to (broken v)
+stop [all v]
```

```blocks3
when green flag clicked
+switch costume to (normal v)
set [distance v] to [0]
```

--- /task ---

--- task ---

If you want to play a sound at the end, you'll have change your `stop all`{:class="block3control"} block to `stop other scripts in sprite`{:class="block3control"}.

This means that the timer you'll create will stop counting, but the sound will still play.

![finish line sprite](images/finish-line-sprite.png)

```blocks3
switch costume to (broken v)
+ stop [other scripts in sprite v]
+ start sound (cheer v)
```

--- /task ---

Have you noticed that you can cheat your game by just holding down the left and right arrow keys?

--- task ---

To fix this, you need to make sure that each key is pressed __and then released__ before moving the finish line.

Here's the code you'll need to add:

![finish line sprite](images/finish-line-sprite.png)

```blocks3
wait until <key (left arrow v) pressed?>
+wait until <not <key (left arrow v) pressed?>>
change size by (1)
```

You'll need to do the same for the right arrow key.

![finish line sprite](images/finish-line-sprite.png)

```blocks3
wait until <not <key (right arrow v) pressed?>>
```

--- /task ---
