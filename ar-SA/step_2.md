## استعداد...

هيا لنبدأ بإنشاء عداد تنازلي للسباق.

--- task ---

قم بفتح مشروع البدء "السباق" في Scratch.

**Online**: open the [starter project](https://rpf.io/sprint-on){:target="_blank"}.

اذا كنت تملك حساب على Scratch فيمكنك عمل نسخة بالضغط على **Remix**.

**Offline**: open the [starter project](https://rpf.io/p/en/sprint-go){:target="_blank"} in the offline editor.

If you need to download and install the Scratch offline editor, you can find it at [rpf.io/scratchoff](https://rpf.io/scratchoff){:target="_blank"}.

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
+broadcast (start v)
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
broadcast (start v)
```

--- /task ---
