--- challenge ---

## チャレンジ: 観客 (かんきゃく) を追加する

プロジェクトには2人の観客のスプライトがふくまれています。「表示する」アイコンをクリックして、ステージに表示します。

レースに観客を追加できますか？ あなたがゴールした時に観客が声援 (せいえん) を送るようにできますか?

![ゲームの観客](images/sprint-spectator.png)

必要なコードは、ゴールと木のスプライトにすでに追加したコードにとてもにていることに注意してください。

役に立つコードブロックをいくつかしょうかいします。

```blocks3
when green flag clicked

set size to (1) %

go to x: (0) y: (0)

when I receive [スタート v]

repeat until <(距離 :: variables) = [100]>
end

change x by (10)

change y by (10)

change size by (1)

wait until <key (left arrow v) pressed?>
```

かわりにべつの木を追加したり、他の好きなものを追加したりできます。


--- /challenge ---