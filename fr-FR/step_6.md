--- challenge ---

## Défi : Ajouter un spectateur

Ton projet inclut quelques sprites spectateurs – clique sur l’icône « montrer» pour l’afficher sur la scène.

Peux-tu ajouter un spectateur à ta course ? Peux-tu faire encourager le spectateur lorsque tu atteins la ligne d'arrivée ?

![un spectateur dans le jeu](images/sprint-spectator.png)

Rappelle-toi que le code dont tu auras besoin est très similaire au code que tu as déjà ajouté à ta ligne d'arrivée et à ton arbre.

Voici quelques blocs de code utiles pour t'aider :

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

Si tu préféres, tu peux ajouter un autre arbre à la place, ou n'importe quoi d'autre que tu souhaites !


--- /challenge ---