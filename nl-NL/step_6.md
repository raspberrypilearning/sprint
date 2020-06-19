--- challenge ---

## Uitdaging: voeg een toeschouwer toe

Je project bevat een aantal toeschouwerssprites - klik op het 'toon' pictogram om het op het speelveld weer te geven.

Kun je een toeschouwer aan je race toevoegen? Kun je de toeschouwer laten juichen als je de eindstreep bereikt?

![een toeschouwer in het spel](images/sprint-spectator.png)

Onthoud dat de code die je nodig hebt erg lijkt op de code die je al hebt toegevoegd aan je eindstreep en je boom.

Hier zijn enkele nuttige codeblokken om je te helpen:

```blocks3
when green flag clicked

set size to (1) %

go to x: (0) y: (0)

when I receive [start v]

repeat until <(afstand :: variables) = [100]>
end

change x by (10)

change y by (10)

change size by (1)

wait until <key (left arrow v) pressed?>
```

Als je wilt, kun je een andere boom toevoegen, of iets anders dat je leuk vindt!


--- /challenge ---