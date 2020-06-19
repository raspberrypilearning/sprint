## Προσθήκη σκηνικού

Ας κάνουμε ένα δέντρο να κινείται καθώς ο παίκτης τρέχει.

--- task ---

Αρχικά, τοποθέτησε το δέντρο και κάνε το μικρό όταν κάνεις κλικ στη σημαία.

![αντικείμενο δέντρο](images/tree-sprite.png)

```blocks3
when green flag clicked
show
go to x: (-50) y: (20)
set size to (1) %
```

--- /task ---


--- task ---

Μόλις ξεκινήσει ο αγώνας, το δέντρο θα πρέπει να κινηθεί μέχρι ο παίκτης να τρέξει 100 μέτρα.

![αντικείμενο δέντρο](images/tree-sprite.png)

```blocks3
when I receive [start v]
repeat until <(distance :: variables) = [100]>
end

```

--- /task ---

--- task ---

Μόλις πατηθεί το αριστερό πλήκτρο (και απελευθερωθεί), το δέντρο θα πρέπει να μεγαλώσει και να κινηθεί - όπως και η γραμμή τερματισμού.

![αντικείμενο δέντρο](images/tree-sprite.png)

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

Εάν δοκιμάσεις το δέντρο σου, θα δεις ότι κινείται προς τα κάτω, στο δρόμο.

![το δέντρο μετακινήθηκε στο δρόμο](images/sprint-tree-bug.png)

--- /task ---

--- task ---

Για να το διορθώσεις, προσθέστε κώδικα για να κάνεις το δέντρο να απομακρύνεται ελαφρώς από το δρόμο.

![αντικείμενο δέντρο](images/tree-sprite.png)

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

Στη συνέχεια, πρέπει να κάνεις το ίδιο για το δεξί βελάκι. Έτσι πρέπει να φαίνεται ο κώδικας:

![αντικείμενο δέντρο](images/tree-sprite.png)

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

