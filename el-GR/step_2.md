## Στα ίχνη σου...

Ας ξεκινήσουμε δημιουργώντας ένα χρονόμετρο αγώνα.

--- task ---

Άνοιξε το αρχικό πρόγραμμα "Sprint" στο Scratch.

**Σε σύνδεση**: άνοιξε το [αρχικό έργο](https://scratch.mit.edu/projects/406229004){:target="_blank"}.

Αν έχεις λογαριασμό Scratch μπορείς να κάνεις ένα αντίγραφο, κάνοντας κλικ στο κουμπί **Ανάμειξη**.

**Εκτός σύνδεσης**: άνοιξε το [αρχικό έργο](http://rpf.io/p/el-GR/sprint-go){:target="_blank"} στον επεξεργαστή εκτός σύνδεσης.

Αν χρειαστεί να κατεβάσεις και να εγκαταστήσεις τον offline editor για το Scratch, μπορείς να το βρεις στο [rpf.io/scratchoff](http://rpf.io/scratchoff){:target="_blank"}.

Στο αρχικό έργο, θα δεις έναν δρόμο και μια κορδέλα τερματισμού.

![αρχικά έργα](images/sprint-starter.png)

--- /task ---

--- task ---

Αρχικά, ας βάλουμε την κορδέλα τερματισμού στον ορίζοντα:

![αντικείμενο κορδέλας τερματισμού](images/finish-line-sprite.png)

```blocks3
when green flag clicked
go to x: (0) y: (30)
set size to (1) %
```

--- /task ---

--- task ---

Εάν κάνεις κλικ στη σημαία για να ελέγξεις τον κώδικά σου, θα δεις την κορδέλα τερματισμού στο βάθος.

![γραμμή τερματισμού στο βάθος](images/sprint-line-start-test-annotated.png)

--- /task ---

--- task ---

Στη συνέχεια, χρησιμοποίησε μπλοκ `πες`{:class="block3looks"} για να δημιουργήσεις μια αντίστροφη μέτρηση και μετά μετάδωσε το μήνυμα `έναρξη`{:class="block3events"}.

![αντικείμενο κορδέλας τερματισμού](images/finish-line-sprite.png)

```blocks3
when green flag clicked
go to x: (0) y: (30)
set size to (1) %
+say [3] for (1) seconds
+say [2] for (1) seconds
+say [1] for (1) seconds
+broadcast (έναρξη v)
```

--- /task ---

--- task ---

Μπορείς επίσης να προσθέσεις έναν ήχο στην αντίστροφη μέτρηση.

![αντικείμενο κορδέλας τερματισμού](images/finish-line-sprite.png)

```blocks3
when green flag clicked
go to x: (0) y: (30)
set size to (1) %
say [3] for (1) seconds
say [2] for (1) seconds
say [1] for (1) seconds
+start sound (Siren Whistle v)
broadcast (έναρξη v)
```

--- /task ---
