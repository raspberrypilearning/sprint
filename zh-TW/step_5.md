## 添加其他背景

讓我們新增一棵樹，它會隨著玩家衝刺而移動。

--- task ---

首先，將給這棵樹放在一個固定位置，並且在點擊綠色旗子時，那棵樹會變小。

![樹角色](images/tree-sprite.png)

```blocks3
when green flag clicked
show
go to x: (-50) y: (20)
set size to (1) %
```

--- /task ---


--- task ---

比賽開始後，樹會開始移動，直到玩家跑完100米。

![樹角色](images/tree-sprite.png)

```blocks3
when I receive [start v]
repeat until <(distance :: variables) = [100]>
end

```

--- /task ---

--- task ---

按下（釋放）左鍵後，那棵樹應該會越變越大並且像你在移動 - 就跟終點線一樣。

![樹角色](images/tree-sprite.png)

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

如果你測試寫好的程式，應該會看到那棵樹沿著跑道向下移動。

![樹移到跑道上](images/sprint-tree-bug.png)

--- /task ---

--- task ---

解決這個問題方法就是，要增加一些程式邏輯，讓這棵樹可以稍微的偏離跑道。

![樹角色](images/tree-sprite.png)

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

對右方向鍵編輯相同的程式邏輯。 你的程式看起來應該像這樣：

![樹角色](images/tree-sprite.png)

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

