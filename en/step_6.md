--- challenge ---
## Challenge: Add a spectator
Can you add a spectator to your race?

![screenshot](images/sprint-spectator.png)

Remember that the code you'll need is very similar to the code you've already added to your finish line and your tree.

Here are some useful code blocks to help you:

```blocks
when green flag clicked

set size to (1) %

go to x: (0) y: (0)

when I receive [start v]

repeat until <(distance :: variables) = [100]>
end

change x by (10)

change y by (10)

change size by (1)

wait until <key [left arrow v] pressed?>
```

If you prefer, you can add another tree instead, or anything else you like!


--- /challenge ---