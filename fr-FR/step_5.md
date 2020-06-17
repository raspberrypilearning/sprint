## Ajouter des décors

Codons un arbre pour qu'il se déplace pendant que le joueur court.

--- task ---

Tout d'abord, positionne l'arbre et réduis-le lorsque tu cliques sur le drapeau.

![sprite d'arbre](images/tree-sprite.png)

```blocks3
when green flag clicked
show
go to x: (-50) y: (20)
set size to (1) %
```

--- /task ---


--- task ---

Une fois la course commencée, l'arbre doit se déplacer jusqu'à ce que le joueur ait couru 100 mètres.

![sprite d'arbre](images/tree-sprite.png)

```blocks3
when I receive [start v]
repeat until <(distance :: variables) = [100]>
end

```

--- /task ---

--- task ---

Une fois que la touche gauche a été appuyée (et relâchée), l'arbre devrait devenir plus grand et se déplacer, tout comme la ligne d'arrivée.

![sprite d'arbre](images/tree-sprite.png)

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

Si tu testes ton arbre, tu verras qu'il se déplace vers le bas, sur la piste.

![arbre déplacé sur la piste](images/sprint-tree-bug.png)

--- /task ---

--- task ---

Pour corriger ceci, ajoute du code pour que ton arbre s'éloigne légèrement de la piste.

![sprite d'arbre](images/tree-sprite.png)

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

Tu devrais aussi faire la même chose pour la touche fléchée droite. Voici à quoi ton code de l'arbre devrait ressembler :

![sprite d'arbre](images/tree-sprite.png)

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

