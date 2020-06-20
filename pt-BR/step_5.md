## Adicionando cenário

Vamos programar uma árvore para mover conforme o jogador corre.

--- task ---

Primeiro, posicione a árvore e faça com que ela diminua quando a bandeira for clicada.

![ator árvore](images/tree-sprite.png)

```blocks3
when green flag clicked
show
go to x: (-50) y: (20)
set size to (1) %
```

--- /task ---


--- task ---

Uma vez que a corrida tenha começado, a árvore deve se mover até que o jogador tenha percorrido 100 metros.

![ator árvore](images/tree-sprite.png)

```blocks3
when I receive [start v]
repeat until <(distance :: variables) = [100]>
end

```

--- /task ---

--- task ---

Uma vez que a tecla para esquerda tenha sido pressionada (e liberada), a árvore deve ficar maior e se mover - assim como a linha de chegada.

![ator árvore](images/tree-sprite.png)

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

Se você testar sua árvore, verá que ela se move para baixo, se aproximando da pista.

![árvore se aproximando da pista](images/sprint-tree-bug.png)

--- /task ---

--- task ---

Para corrigir isso, adicione código para fazer que sua árvore se afaste aos poucos da pista.

![ator árvore](images/tree-sprite.png)

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

Você deve fazer o mesmo para a seta para a direita. Aqui está como o código da sua Árvore deve ficar:

![ator árvore](images/tree-sprite.png)

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

