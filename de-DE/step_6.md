--- challenge ---

## Herausforderung: Füge einen Zuschauer hinzu

Dein Projekt enthält einige Zuschauer-Figuren. Klicke auf das Symbol "Anzeigen", um sie auf der Bühne anzuzeigen.

Kannst du deinem Rennen einen Zuschauer hinzufügen? Kannst du den Zuschauer zum Jubeln bringen, wenn du die Ziellinie erreicht?

![ein Zuschauer im Spiel](images/sprint-spectator.png)

Der Code den du benötigst, ist dem Code den du bereits zu der Ziellinie und dem Baum hinzugefügt hast, sehr ähnlich.

Hier sind einige nützliche Codeblöcke, die dir helfen sollten:

```blocks3
when green flag clicked

set size to (1) %

go to x: (0) y: (0)

when I receive [start v]

repeat until <(distance :: variables) = [100]>
end

change x by (10)

change y by (10)

change size by (1)

wait until <key (left arrow v) pressed?>
```

Du kannst auch einen weiteren Baum hinzufügen, wenn dir das lieber ist. Oder alles was dir so einfällt!


--- /challenge ---