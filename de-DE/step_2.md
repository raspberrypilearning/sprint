## Auf die Plätze...

Beginnen wir mit einem Countdown für das Rennen.

--- task ---

Öffne das Scratch-Basisprojekt 'Sprint'.

**Online**: Öffne das [Basisprojekt](https://scratch.mit.edu/projects/411572918){:target="_blank"}.

Wenn du bereits einen Scratch-Account besitzt, kannst du dir durch Klick auf **Remix** eine Kopie anlegen.

**Offline**: Öffne das [Basisprojekt](http://rpf.io/p/de-DE/sprint-go){:target="_blank"} im Offline-Editor.

Wenn du Scratch herunterladen und auf deinem Rechner installieren möchtest, dann findest du die Datei unter diesem Link: [rpf.io/scratchoff](http://rpf.io/scratchoff){:target="_blank"}.

Im Basisprojekt solltest du eine Straße und eine Ziellinie sehen.

![Basisprojekt](images/sprint-starter.png)

--- /task ---

--- task ---

Lass uns zunächst die Ziellinie am Horizont platzieren:

![Ziellinienfigur](images/finish-line-sprite.png)

```blocks3
when green flag clicked
go to x: (0) y: (30)
set size to (1) %
```

--- /task ---

--- task ---

Wenn du auf die Flagge klickst, um deinen Code zu testen, siehst du deine Ziellinie in der Ferne.

![Ziellinie in der Ferne](images/sprint-line-start-test-annotated.png)

--- /task ---

--- task ---

Verwende als Nächstes `sage`{:class="block3looks"} -Blöcke, um einen Countdown zu erstellen, und sende dann eine `start`{:class="block3events"} -Nachricht.

![Ziellinienfigur](images/finish-line-sprite.png)

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

Du kannst deinem Countdown auch einen Sound hinzufügen.

![Ziellinienfigur](images/finish-line-sprite.png)

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
