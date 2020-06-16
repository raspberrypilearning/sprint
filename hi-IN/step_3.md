## दूरी तक जाना

चलिए एरो बटन दबाए जाने पर फिनिश लाइन को हिलाते हैं I

--- task ---

आप खिलाड़ी को एरो बटन दबाने की अनुमति देना चाहते हैं __until they have run 100 meters__। ऐसा करने के लिए, एक नया चर बनाएं `distance`{:class="block3variables"}।

[[[generic-scratch3-add-variable]]]

--- /task ---

--- task ---

आपको अपना नया चर मंच पर देखना चाहिए। इसे ऊपरी-दाएँ कोने में खींचें।

![स्क्रीनशॉट](images/sprint-distance-drag.png)

--- /task ---

--- task ---

झंडा क्लिक किए जाने पर  `distance`{:class="block3variables"} 0 तक निर्धारित करें ।

![फिनिश लाइन स्प्राइट](images/finish-line-sprite.png)

```blocks3
when green flag clicked
+set [distance v] to [0]
go to x: (0) y: (30)
set size to (1) %
```

--- /task ---

--- task ---

एक बार जब आपकी दौड़ शुरू हो जाती है, तो आपके खिलाड़ी को स्प्रिंट करना होगा  __until they have run 100 meters__.

![फिनिश लाइन स्प्राइट](images/finish-line-sprite.png)

```blocks3
when I receive [start v]
repeat until <(distance :: variables) = [100]>
end 
```

--- /task ---

--- task ---

कोड जोड़ें ताकि खिलाड़ी के बाएं एरो बटन को दबाने के बाद आपकी फिनिश लाइन थोड़ी बड़ी हो जाए। दूरी भी बढ़नी चाहिए।

![फिनिश लाइन स्प्राइट](images/finish-line-sprite.png)

```blocks3
when I receive [start v]
repeat until <(distance :: variables) = [100]>
+wait until <key (left arrow v) pressed?>
+ change size by (1)
+ change [distance v] by (1)
end 
```

--- /task ---

--- task ---

अपने खेल का परीक्षण करने के लिए हरे झंडे पर क्लिक करें। आपको देखना चाहिए कि बाएं तीर दबाए जाने पर फिनिश लाइन बड़ी हो जाती है, लेकिन ट्रैक के साथ नहीं चलती है।

![फिनिश लाइन बड़ी है लेकिन एक ही जगह पर है](images/sprint-line-bug.png)

--- /task ---

--- task ---

इसे ठीक करने के लिए, आप प्रत्येक बार एक बटन दबाने पर फिनिश लाइन को थोड़ा नीचे ले जाने के लिए कोड जोड़ सकते हैं।

![फिनिश लाइन स्प्राइट](images/finish-line-sprite.png)

```blocks3
when I receive [start v]
repeat until <(distance :: variables) = [100]>
wait until <key (left arrow v) pressed?>
change size by (1)
+change y by (-1.5)
change [distance v] by (1)
end 
```

--- /task ---

--- task ---

अपनी परियोजना का फिर से परीक्षण करें और आपको यह देखना चाहिए कि फिनिश लाइन आपके चरण को नीचे की ओर ले जाए।

![फिनिश लाइन के सड़क नीचे चला जाता है](images/sprint-line-fix-test.png)

--- /task ---

--- task ---

फिर आपको सही एरो की के लिए ऐसा करना चाहिए।

![फिनिश लाइन स्प्राइट](images/finish-line-sprite.png)

```blocks3
when I receive [start v]
repeat until <(distance :: variables) = [100]>
wait until <key (left arrow v) pressed?>
change size by (1)
change y by (-1.5)
change [distance v] by (1)
+wait until <key (right arrow v) pressed?>
+change size by (1)
+change y by (-1.5)
+change [distance v] by (1)
end 
```

--- /task ---

--- task ---

यदि आप फिनिश लाइन की कास्टूम देखने के लिए क्लिक करते हैं, तो आपको देखना चाहिए कि 2 हैं।

![2 costumes](images/sprint-line-costumes.png)

--- /task ---

--- task ---

आप दौड़ के अंत में 'टूटी' कास्टूम (और खेल के ख़तम होने पर ) पर स्विच कर सकते हैं। दौड़ की शुरुआत में 'normal' कास्टूम पर स्विच करना याद रखें!

![फिनिश लाइन स्प्राइट](images/finish-line-sprite.png)

```blocks3
when I receive [start v]
repeat until <(distance :: variables) = [100]>
wait until <key (left arrow v) pressed?>
change size by (1)
change y by (-1.5)
change [distance v] by (1)
wait until <key (right arrow v) pressed?>
change size by (1)
change y by (-1.5)
change [distance v] by (1)
end 
+switch costume to (broken v)
+stop [all v]
```

```blocks3
when green flag clicked
+switch costume to (normal v)
set [distance v] to [0]
```

--- /task ---

--- task ---

यदि आप अंत में म्युज़िक चलाना चाहते हैं, तो आपको अपना `stop all`{:class="block3control"} ब्लॉक `stop other scripts in sprite`{:class="block3control"} में बदलना होगा I

इसका मतलब है कि आपके द्वारा बनाया गया टाइमर गिनती करना बंद कर देगा, लेकिन म्युज़िक अभी भी बजाएगी।

![फिनिश लाइन स्प्राइट](images/finish-line-sprite.png)

```blocks3
switch costume to (broken v)
+ stop [other scripts in sprite v]
+ start sound (cheer v)
```

--- /task ---

क्या आपने देखा है कि आप केवल बाएँ और दाएँ एरो बटन्स को दबाकर अपने खेल को धोखा दे सकते हैं?

--- task ---

इसे ठीक करने के लिए, आपको यह सुनिश्चित करने की जरुरत है कि फिनिश लाइन ले जाने से पहले प्रत्येक की दबाया जाये __and then released__ ।

यहाँ दिया गया कोड आपको जोड़ना होगा:

![फिनिश लाइन स्प्राइट](images/finish-line-sprite.png)

```blocks3
wait until <key (left arrow v) pressed?>
+wait until <not <key (left arrow v) pressed?>>
change size by (1)
```

फिर आपको सही एरो की के लिए ऐसा करना चाहिए।

![फिनिश लाइन स्प्राइट](images/finish-line-sprite.png)

```blocks3
wait until <not <key (right arrow v) pressed?>>
```

--- /task ---
