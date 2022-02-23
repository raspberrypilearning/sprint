## Op uw plaatsen...

Laten we beginnen met het maken van het aftellen voor een race.

--- task ---

Open het 'Sprint' Scratch-startproject.

**Online**: open het [startproject](https://scratch.mit.edu/projects/406225992){:target="_blank"}.

Als je een Scratch-account hebt, kun je een kopie maken door op **Remix** te klikken.

**Offline**: open het [startproject](https://rpf.io/p/nl-NL/sprint-go){:target="_blank"} in de offline editor.

Als je de Scratch offline editor wilt downloaden en installeren dan kan je die vinden op [rpf.io/scratchoff](https://rpf.io/scratchoff){:target="_blank"}.

In het startproject zou je een weg en eindstreep moeten zien.

![startprojecten](images/sprint-starter.png)

--- /task ---

--- task ---

Laten we om te beginnen de eindstreep aan de horizon plaatsen:

![eindstreep sprite](images/finish-line-sprite.png)

```blocks3
when green flag clicked
go to x: (0) y: (30)
set size to (1) %
```

--- /task ---

--- task ---

Als je op de vlag klikt om je code te testen, zie je de eindstreep in de verte.

![eindstreep in de verte](images/sprint-line-start-test-annotated.png)

--- /task ---

--- task ---

Gebruik vervolgens `zeg`{:class="block3looks"} blokken om een aftelling te maken en zend vervolgens een `start`{:class="block3events"} bericht uit.

![eindstreep sprite](images/finish-line-sprite.png)

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

Je kunt ook een geluid toevoegen aan je aftelling.

![eindstreep sprite](images/finish-line-sprite.png)

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
