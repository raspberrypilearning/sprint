## À vos marques...

Commençons par créer un compte à rebours de la course.

--- task ---

Ouvre le projet de démarrage Scratch « Sprint ! ».

**En ligne** : ouvre le [projet de démarrage](https://scratch.mit.edu/projects/406227716){:target="_blank"}.

Si tu as un compte Scratch, tu peux en créer une copie en cliquant sur **Remix**.

**Hors ligne**: ouvre le [projet de démarrage](https://rpf.io/p/fr-FR/sprint-go){:target="_blank"} dans l'éditeur hors ligne.

Si tu dois télécharger et installer l'éditeur hors ligne Scratch, tu peux le trouver à [rpf.io/scratchoff](https://rpf.io/scratchoff){:target="_blank"}.

Dans le projet de démarrage, tu devrais voir une route et une ligne d'arrivée.

![projets de démarrage](images/sprint-starter.png)

--- /task ---

--- task ---

Pour commencer, mettons la ligne d'arrivée à l'horizon :

![sprite de la ligne d'arrivée](images/finish-line-sprite.png)

```blocks3
when green flag clicked
go to x: (0) y: (30)
set size to (1) %
```

--- /task ---

--- task ---

Si tu cliques sur le drapeau pour tester ton code, tu verras ta ligne d'arrivée au loin.

![ligne d'arrivée au loin](images/sprint-line-start-test-annotated.png)

--- /task ---

--- task ---

Ensuite, utilise les blocs `dire`{:class="block3looks"} pour créer un compte à rebours, puis envoyer à tous un message `start`{:class="block3events"}.

![sprite de la ligne d'arrivée](images/finish-line-sprite.png)

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

Tu peux également ajouter un son à ton compte à rebours.

![sprite de la ligne d'arrivée](images/finish-line-sprite.png)

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
