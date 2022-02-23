## Em suas marcas...

Vamos começar criando uma contagem regressiva para a corrida.

--- task ---

Abra o projeto inicial 'Corrida' do Scratch.

**Online**: abra o [projeto inicial](https://scratch.mit.edu/projects/406798245){:target="_blank"}.

Se você tiver uma conta do Scratch, pode fazer uma cópia clicando em **Remix**.

**Offline**: abra o [projeto inicial](https://rpf.io/p/pt-BR/sprint-go){:target="_blank"} no editor offline.

Se você precisar baixar e instalar o editor offline do Scratch, você pode encontrá-lo em [rpf.io/scratchoff](https://rpf.io/scratchoff){:target="_blank"}.

No projeto inicial, você deve ver a pista e a linha de chegada.

![projetos iniciais](images/sprint-starter.png)

--- /task ---

--- task ---

Para começar, vamos colocar a linha de chegada no horizonte:

![ator linha de chegada](images/finish-line-sprite.png)

```blocks3
when green flag clicked
go to x: (0) y: (30)
set size to (1) %
```

--- /task ---

--- task ---

Se você clicar na bandeira para testar seu código, verá sua linha de chegada à distância.

![linha de chegada à distância](images/sprint-line-start-test-annotated.png)

--- /task ---

--- task ---

Em seguida, use blocos `diga`{:class="block3looks"} para criar uma contagem regressiva, e então transmita uma mensagem `largar`{:class="block3events"}.

![ator linha de chegada](images/finish-line-sprite.png)

```blocks3
when green flag clicked
go to x: (0) y: (30)
set size to (1) %
+say [3] for (1) seconds
+say [2] for (1) seconds
+say [1] for (1) seconds
+broadcast (largar v)
```

--- /task ---

--- task ---

Você também pode adicionar um som à sua contagem regressiva.

![ator linha de chegada](images/finish-line-sprite.png)

```blocks3
when green flag clicked
go to x: (0) y: (30)
set size to (1) %
say [3] for (1) seconds
say [2] for (1) seconds
say [1] for (1) seconds
+start sound (Siren Whistle v)
broadcast (largar v)
```

--- /task ---
