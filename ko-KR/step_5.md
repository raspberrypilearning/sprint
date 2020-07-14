## 풍경 추가하기

플레이어가 질주 할 때 움직일 나무를 코딩 해 봅시다.

--- task ---

먼저 깃발을 클릭 할 때 나무를 배치하고 작게 만듭니다.

![나무 스프라이트](images/tree-sprite.png)

```blocks3
when green flag clicked
show
go to x: (-50) y: (20)
set size to (1) %
```

--- /task ---


--- task ---

레이스가 시작되면 플레이어가 100 미터를 전력질주 할 때까지 나무가 움직여야합니다.

![나무 스프라이트](images/tree-sprite.png)

```blocks3
when I receive [start v]
repeat until <(distance :: variables) = [100]>
end

```

--- /task ---

--- task ---

왼쪽 키를 눌렀다가 놓으면 결승선처럼 나무가 커지고 움직여야합니다.

![나무 스프라이트](images/tree-sprite.png)

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

나무를 테스트하면 나무가 트랙으로 아래쪽으로 이동하는 것을 볼 수 있습니다.

![나무가 트랙 위로 이동](images/sprint-tree-bug.png)

--- /task ---

--- task ---

이 문제를 해결하려면 코드를 추가하여 나무가 트랙에서 약간 떨어지도록 합니다.

![나무 스프라이트](images/tree-sprite.png)

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

그런 다음 오른쪽 화살표 키에 대해서도 동일하게 수행해야 합니다. 나무 코드는 다음과 같이 쓰여야 합니다:

![나무 스프라이트](images/tree-sprite.png)

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

