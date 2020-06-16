## तुम्हारे प्राप्तांक पर (on your marks)...

एक दौड़ उलटी गिनती बनाने के द्वारा शुरू करते हैं।

--- task ---

'स्प्रिंट' Scratch स्टार्टर प्रोजेक्ट खोलें।

**ऑनलाइन**: [starter project](http://rpf.io/sprint-on){:target="_blank"} खोलें |

यदि आपके पास एक Scratch खाता (account) है तो आप **Remix** पर क्लिक करके कॉपी बना सकते हैं |

** ऑफ़लाइन ** : [starter project](http://rpf.io/p/en/sprint-go){:target="_blank"} ऑफ़लाइन संपादक में खोलें ।

यदि आपको Scratch ऑफ़लाइन संपादक को डाउनलोड और इंस्टॉल करने की जरूरत है, तो आप इसे [ rpf.io/scratchoff ](http://rpf.io/scratchoff) {: target= "_ blank"} पर ढूंढ सकते हैं I

स्टार्टर प्रोजेक्ट में, आपको एक सड़क और फिनिश लाइन दिखनी चाहिए।

![प्रारंभक प्रोजैक्ट](images/sprint-starter.png)

--- /task ---

--- task ---

शुरू करने के लिए, आइए क्षेत्र पर फिनिश लाइन डालें:

![फिनिश लाइन स्प्राइट](images/finish-line-sprite.png)

```blocks3
when green flag clicked
go to x: (0) y: (30)
set size to (1) %
```

--- /task ---

--- task ---

यदि आप अपने कोड का परीक्षण करने के लिए ध्वज (flag) पर क्लिक करते हैं, तो आप दूरी में अपनी फिनिश लाइन देखेंगे।

![दूरी में फिनिश लाइन](images/sprint-line-start-test-annotated.png)

--- /task ---

--- task ---

अगला, `say`{:class="block3looks"} ब्लॉक का उपयोग करें एक उलटी गिनती बनाने के लिए ब्लॉक करता है, और फिर एक `start`{:class="block3events"} संदेश प्रसारित करता है I

![फिनिश लाइन स्प्राइट](images/finish-line-sprite.png)

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

आप अपनी उलटी गिनती में एक ध्वनि भी जोड़ सकते हैं।

![फिनिश लाइन स्प्राइट](images/finish-line-sprite.png)

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
