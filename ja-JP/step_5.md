## 風景 (ふうけい) を追加する

プレーヤーが走っているのに合わせて移動する木をコーディングしましょう。

--- task ---

まず、木をおき、緑の旗が押されたときに小さくします。

![木のスプライト](images/tree-sprite.png)

```blocks3
when green flag clicked
show
go to x: (-50) y: (20)
set size to (1) %
```

--- /task ---


--- task ---

レースが始まったら、プレーヤーが100メートル走りきるまで木を動かします。

![木のスプライト](images/tree-sprite.png)

```blocks3
when I receive [スタート v]
repeat until <(距離 :: variables) = [100]>
end

```

--- /task ---

--- task ---

左矢印キーが押され (そしてはなされ) ると、ゴールと同じように木は大きくなり、移動します。

![木のスプライト](images/tree-sprite.png)

```blocks3
when I receive [スタート v]
repeat until <(距離 :: variables) = [100]>
+wait until <key (left arrow v) pressed?>
+wait until <not  <key (left arrow v) pressed?>>
+change size by (1)
+change y by (-1.5)
end
```

--- /task ---

--- task ---

木のコードをテストすると、木は下に移動して行き、コース上に乗っかってしまいます。

![コースに乗っかる木](images/sprint-tree-bug.png)

--- /task ---

--- task ---

これをなおすには、木をコードから少しはなしていくコードを追加します。

![木のスプライト](images/tree-sprite.png)

```blocks3
when I receive [スタート v]
repeat until <(距離 :: variables) = [100]>
wait until <key (left arrow v) pressed?>
wait until <not  <key (left arrow v) pressed?>>
change size by (1)
change y by (-1.5)
+change x by (-2)
end
```

--- /task ---

--- task ---

右矢印キーについても同じようにする必要があります。 木のコードは次のようになります。

![木のスプライト](images/tree-sprite.png)

```blocks3
when green flag clicked
show
go to x: (-50) y: (20)
set size to (1) %

when I receive [スタート v]
repeat until <(距離 :: variables) = [100]>
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

