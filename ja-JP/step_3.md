## ゴールまで走る

矢印キーが押された (おされた) ときにゴールを動かしましょう。

--- task ---

プレーヤーが__100メートル走りきるまで__矢印キーを押せるようにします 。 そのために、`距離`{:class="block3variables"} (きょり) という新しい変数 (へんすう) を作ります。

[[[generic-scratch3-add-variable]]]

--- /task ---

--- task ---

ステージ上に新しい変数が表示されます。 それを右上のすみにドラッグします。

![スクリーンショット](images/sprint-distance-drag.png)

--- /task ---

--- task ---

緑の旗が押されたとき、`距離`{:class="block3variables"}を0にします。

![ゴールのスプライト](images/finish-line-sprite.png)

```blocks3
when green flag clicked
+set [距離 v] to [0]
go to x: (0) y: (30)
set size to (1) %
```

--- /task ---

--- task ---

レースが始まったら、プレーヤーは__100メートルの距離を__全力で走らなければなりません。

![ゴールのスプライト](images/finish-line-sprite.png)

```blocks3
when I receive [スタート v]
repeat until <(距離 :: variables) = [100]>
end 
```

--- /task ---

--- task ---

コードを追加して、プレイヤーが左矢印キーを押したら、ゴールが少し大きくなるようにします。 走った距離もふやします。

![ゴールのスプライト](images/finish-line-sprite.png)

```blocks3
when I receive [スタート v]
repeat until <(距離 :: variables) = [100]>
+wait until <key (left arrow v) pressed?>
+ change size by (1)
+ change [距離 v] by (1)
end 
```

--- /task ---

--- task ---

緑の旗をクリックしてプロジェクトをテストします。 左矢印キーが押されるとゴールは大きくなりますが、コースにそって動いてはくれません。

![ゴールは大きくなるが、同じ場所にある](images/sprint-line-bug.png)

--- /task ---

--- task ---

これをなおすには、キーが押されるたびにゴールを少し下に移動 (いどう) するコードを追加します。

![ゴールのスプライト](images/finish-line-sprite.png)

```blocks3
when I receive [スタート v]
repeat until <(距離 :: variables) = [100]>
wait until <key (left arrow v) pressed?>
change size by (1)
+change y by (-1.5)
change [距離 v] by (1)
end 
```

--- /task ---

--- task ---

もう一度プロジェクトをテストすると、ゴールが自分に向かって、ステージの下に移動するのがわかります。

![コースにそって下るゴール](images/sprint-line-fix-test.png)

--- /task ---

--- task ---

右矢印キーについても同じようにしましょう。

![ゴールのスプライト](images/finish-line-sprite.png)

```blocks3
when I receive [スタート v]
repeat until <(距離 :: variables) = [100]>
wait until <key (left arrow v) pressed?>
change size by (1)
change y by (-1.5)
change [距離 v] by (1)
+wait until <key (right arrow v) pressed?>
+change size by (1)
+change y by (-1.5)
+change [距離 v] by (1)
end 
```

--- /task ---

--- task ---

ゴールのコスチュームをクリックして表示すると、2つのコスチュームがあることがわかります。

![2つのコスチューム](images/sprint-line-costumes.png)

--- /task ---

--- task ---

レースが終わったときに「ゴール時」コスチュームに切りかえ 、そしてゲームを終わらせます。 レースの開始時に「ゴール前」のコスチュームに切りかえることをわすれないでください！

![ゴールのスプライト](images/finish-line-sprite.png)

```blocks3
when I receive [スタート v]
repeat until <(距離 :: variables) = [100]>
wait until <key (left arrow v) pressed?>
change size by (1)
change y by (-1.5)
change [距離 v] by (1)
wait until <key (right arrow v) pressed?>
change size by (1)
change y by (-1.5)
change [距離 v] by (1)
end 
+switch costume to (スタート v)
+stop [all v]
```

```blocks3
when green flag clicked
+switch costume to (ゴール前 v)
set [距離 v] to [0]
```

--- /task ---

--- task ---

さいごに音を再生したい場合は、`すべてを止める`{:class="block3control"}ブロックを`スプライトの他のスクリプトを止める`{:class="block3control"}にかえます。

そうすれば、タイマーはカウントをやめますが、音の再生はつづきます。

![ゴールのスプライト](images/finish-line-sprite.png)

```blocks3
switch costume to (スタート v)
+ stop [other scripts in sprite v]
+ start sound (cheer v)
```

--- /task ---

このコードでは、左右の矢印キーを押しつづければ走っていることになると気づきましたか？

--- task ---

これをなおすには、ゴールを移動させる前に、各キーが押され__そしてはなされる__ようにする必要があります。

追加するコードは次のとおりです。

![ゴールのスプライト](images/finish-line-sprite.png)

```blocks3
wait until <key (left arrow v) pressed?>
+wait until <not <key (left arrow v) pressed?>>
change size by (1)
```

右矢印キーについても同じようにする必要があります。

![ゴールのスプライト](images/finish-line-sprite.png)

```blocks3
wait until <not <key (right arrow v) pressed?>>
```

--- /task ---
