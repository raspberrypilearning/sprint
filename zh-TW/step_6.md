--- challenge ---

## 挑戰：追加一位觀眾

你的專案，可以增添一些觀眾來觀戰 - 點擊“顯示”圖標，以將其顯示在舞台上。

你知道如何在你的比賽裡面，新增一位觀眾嗎？ 你知道如何讓你的觀眾在你抵達終點線時，替你歡呼嗎？

![遊戲中的觀眾](images/sprint-spectator.png)

請記得，你需要的程式和之前所寫的，跑到終點線以及那棵樹的程式非常相似。

這些程式積木可以幫助你：

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

如果你願意，你還可以另外新增一棵樹或是其他你喜歡的東西！


--- /challenge ---