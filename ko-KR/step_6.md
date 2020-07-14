--- challenge ---

## 과제: 관중을 추가하기

프로젝트에는 두 개의 관중(관전자) 스프라이트가 포함됩니다 - 스테이지에 표시하려면 '표시'아이콘을 클릭하십시오.

게임에 점수를 추가할 수 있나요? 결승선에 도달하면 관중을 응원시킬 수 있습니까?

![게임안의 관중](images/sprint-spectator.png)

기억하세요 필요한 코드는 결승선과 나무에 이미 추가 한 코드와 매우 유사합니다.

다음은 유용한 코드 블록입니다:

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

원하는 경우 다른 트리를 추가하거나 원하는 다른 것을 추가 할 수 있습니다!


--- /challenge ---