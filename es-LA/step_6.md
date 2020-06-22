--- challenge ---

## Desafío: Añadir un espectador

Tu proyecto incluye un par de objetos espectadores – haz clic en el icono 'mostrar' de alguno de ellos para mostrarlo en el escenario.

¿Puedes añadir un espectador a tu carrera? ¿Puedes hacer que el espectador te anime cuando llegues a la línea de meta?

![un espectador en el juego](images/sprint-spectator.png)

Recuerda que el código que necesitarás es muy similar al que ya has añadido a tu línea de meta y a tu árbol.

Aquí hay algunos bloques de código útiles para ayudarte:

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

Si prefieres, puedes añadir otro árbol en su lugar, ¡o cualquier otra cosa que desees!


--- /challenge ---