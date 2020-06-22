--- challenge ---

## Desafío: agrega un espectador

Tu proyecto incluye un par de objetos de espectadores: haz clic en el icono de 'mostrar' de uno de ellos para que aparezca en el escenario.

¿Puedes añadir un espectador a tu carrera? ¿Puedes animar al espectador cuando llegues a la línea de llegada?

![un espectador en el juego](images/sprint-spectator.png)

Recuerda que el código que necesitarás es muy similar al que ya has añadido a tu línea de llegada y a tu árbol.

Aquí hay algunos bloques de código útiles para ayudarte:

```blocks3
when green flag clicked

set size to (1) %

go to x: (0) y: (0)

when I receive [salida v]

repeat until <(distancia :: variables) = [100]>
end

change x by (10)

change y by (10)

change size by (1)

wait until <key (left arrow v) pressed?>
```

Si lo prefieres, ¡en lugar del espectador puedes añadir otro árbol!


--- /challenge ---