## استعداد...

هيا لنبدأ بإنشاء عداد تنازلي للسباق.

--- task ---

قم بفتح مشروع البدء "السباق" في Scratch.

**على الإنترنت**: قم بفتح [المشروع الاولي](https://scratch.mit.edu/projects/406230850){:target="_blank"}.

اذا كنت تملك حساب على Scratch فيمكنك عمل نسخة بالضغط على **Remix**.

**غير متصل بالانترنت**: افتح [المشروع الاولي](http://rpf.io/p/ar-SA/sprint-go){:target="_blank"} عبر المحرر الموجود على جهازك.

اذا كنت بحاجة الى تنزيل وتنصيب محرر Scratch على جهازك الشخصي، ستجده في [rpf.io/scratchoff](http://rpf.io/scratchoff){:target="_blank"}.

في المشروع الاولي، سترى خط بداية و نهاية.

![المشاريع الاولية](images/sprint-starter.png)

--- /task ---

--- task ---

لكي نبدأ، دعنا نضع خط النهاية في الأفق:

![خط النهاية](images/finish-line-sprite.png)

```blocks3
when green flag clicked
go to x: (0) y: (30)
set size to (1) %
```

--- /task ---

--- task ---

إذا قمت بالنقر فوق العلم لاختبار البرنامج الخاص بك ، سترى خط النهاية الخاص بك في الافق.

![خط النهاية من بعيد](images/sprint-line-start-test-annotated.png)

--- /task ---

--- task ---

بعد ذلك، استخدم كتلة `قل`{:class="block3looks"} لإنشاء العداد التنازلي، ثم بث رسالة `ابدأ`{:class="block3events"}.

![خط النهاية](images/finish-line-sprite.png)

```blocks3
when green flag clicked
go to x: (0) y: (30)
set size to (1) %
+say [3] for (1) seconds
+say [2] for (1) seconds
+say [1] for (1) seconds
+broadcast (إبدأ v)
```

--- /task ---

--- task ---

يمكنك أيضًا إضافة صوت إلى العد التنازلي.

![خط النهاية](images/finish-line-sprite.png)

```blocks3
when green flag clicked
go to x: (0) y: (30)
set size to (1) %
say [3] for (1) seconds
say [2] for (1) seconds
say [1] for (1) seconds
+start sound (Siren Whistle v)
broadcast (إبدأ v)
```

--- /task ---
