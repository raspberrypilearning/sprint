--- challenge ---

## التحدي: إضافة مشجعين

يحتوي مشروعك على مجموعة من كائنات المشجعين - انقر فوق علامة "إظهار" لإظهار واحد على الشاشة.

هل بامكانك إضافة مشجع إلى سباقك؟ و هل بامكانك أن تجعل المشجع يهتف عندما تصل إلى خط النهاية؟

![متفرج في اللعبة](images/sprint-spectator.png)

تذكر أن الكود البرمجي الذي ستحتاجه يشبه إلى حد كبير الكود البرمجي الذي أضفته بالفعل إلى خط النهاية والشجرة خاصتك.

هنا التعليمات البرمجية التي ستحتاج اليها:

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

إذا كنت تفضل ، يمكنك إضافة شجرة أخرى بدلاً من ذلك، أو أي شيء تحب!


--- /challenge ---