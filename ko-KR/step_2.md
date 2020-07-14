## 당신의 마크에...

레이스 카운트다운을 만들어 시작하도록 하겠습니다.

--- task ---

스크래치 스타터 프로젝트 '전력질주'를 여십시오.

**온라인**: [스타터 프로젝트](http://rpf.io/sprint-on){:target="_ blank"}을 엽니다.

스크래치 계정이 있는 경우 ** Remix를 클릭 ** 하여 사본을 만들 수 있습니다.

**오프라인**: [스타터 프로젝트](http://rpf.io/p/en/sprint-go){:target="_blank"} 를 오프라인 에디터에서 여세요.

스크래치 오프라인 에디터를 다운로드 받아야 하는 경우, [rpf.io/scratchoff](http://rpf.io/scratchoff){:target="_blank"} 에서 다운로드 받을 수 있습니다.

스타터 프로젝트에서는 길과 결승선이 있습니다.

![스타터 프로젝트](images/sprint-starter.png)

--- /task ---

--- task ---

우선, 결승선을 수평선에 놓으십시오.

![결승선 스프라이트](images/finish-line-sprite.png)

```blocks3
when green flag clicked
go to x: (0) y: (30)
set size to (1) %
```

--- /task ---

--- task ---

만약 코드를 테스트하기 위해 깃발을 클릭한다면, 거리에 당신의 결승선이 보일겁니다.

![거리에 있는 결승선](images/sprint-line-start-test-annotated.png)

--- /task ---

--- task ---

다음, `말하기`{:class="block3looks"}블럭을 사용하여 카운트다운을 만든 다음 `시작`{:class="block3looks"} 메세지 방송(브로드캐스트)을 사용하여 메시지를 만드세요.

![결승선 스프라이트](images/finish-line-sprite.png)

```blocks3
when green flag clicked
go to x: (0) y: (30)
set size to (1) %
+say [3] for (1) seconds
+say [2] for (1) seconds
+say [1] for (1) seconds
+broadcast (start v)
```

--- /task ---

--- task ---

카운트 다운에 소리를 추가 할 수도 있습니다.

![결승선 스프라이트](images/finish-line-sprite.png)

```blocks3
when green flag clicked
go to x: (0) y: (30)
set size to (1) %
say [3] for (1) seconds
say [2] for (1) seconds
say [1] for (1) seconds
+start sound (Siren Whistle v)
broadcast (start v)
```

--- /task ---
