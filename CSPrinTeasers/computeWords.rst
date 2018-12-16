..  Copyright (C)  Mark Guzdial, Barbara Ericson, Briana Morrison
    Permission is granted to copy, distribute and/or modify this document
    under the terms of the GNU Free Documentation License, Version 1.3 or
    any later version published by the Free Software Foundation; with
    Invariant Sections being Forward, Prefaces, and Contributor List,
    no Front-Cover Texts, and no Back-Cover Texts.  A copy of the license
    is included in the section entitled "GNU Free Documentation License".

..  shortname:: Chapter: What You Can Do with a Computer
..  description:: Some tidbits of what you can do with a computer

.. setup for automatic question numbering.

.. 	qnum::
	:start: 1
	:prefix: csp-1-4-


.. |runbutton| image:: Figures/run-button.png
    :height: 20px
    :align: top
    :alt: run button

.. |audiobutton| image:: Figures/start-audio-tour.png
    :height: 20px
    :align: top
    :alt: audio tour button


Kelimelerle Hesapla
===================

..	index::
	single: string
	pair: programming; string


Bilgisayar kelimelerle, ya da daha doğru bir tabirle, **karakter dizileri (string)** ile de işlem yapabilir. Tekli (``'Hi'``), ikili (``"Hi"``) veya üçlü (``'Hi'``) tırnak arasında karakterler yazarak bir **karakter dizisi (string)** oluşturabiliriz. Aynı temel aritmetik operatörlerin bazılarını kullanarak dizilerle “işlem yapabiliriz” – yalnız bu operatörler burada farklı bir işlevde kullanılırlar.  Dizileri tekrarlamak için  ``*``  ve iki diziyi birleştirmek **(append – ekleme)** için  ``+``  kullanarak cümle yaratarız. 

.. The computer can also compute with words, or more accurately, with **strings** which are sequences of characters.  We can create a **string** by typing characters between a pair of single (``'Hi'``), double (``"Hi"``), or triple quotes ('''Hi'''). We can "compute" with strings using some of the same basic arithmetic operators -- they just mean something different here.  Here we generate silly song lyrics by using ``+`` to combine (append) two strings and ``*`` to repeat strings.


Aşağıdaki programın üst kısmında, |runbutton| butonunun sağında yer alan, programın sesli turu için olan |audiobutton|  butonunu göreceksiniz. Bu butona tıkladıktan sonra sesli tur için “Line-by-line Tour” ‘a tıklayın. Durdurmak, oynatmak, bir adım öne geçmek ve geri dönmek için konulmuş olan butonları kullanabilirsiniz. 


.. Underneath the program below, to the right of the *Run* button |runbutton|, you'll see the button to open the audio tour for this program: |audiobutton|.  Click on that button and then click on "Line-by-line Tour" to hear the audio tour.  You can use the provided buttons to pause, play, jump ahead, or go back. 


.. activecode:: String_Operators
  :tour_1: "Line-by-line Tour"; 1: str1-line1; 2: str1-line2; 3: str1-line3; 4: str1-line4; 5: str1-line5; 6: str1-line6; 7: str1-line7; 8: str1-line8; 9: str1-line9; 10: str1-line10;
  :nocodelens:
  
  basit = "Ma"
  print(basit)
  uclubasit = basit + basit + basit
  print(uclubasit)
  ileri = "Mow"
  ileri3 = ileri * 3
  print(ileri3)
  birlikte = (basit * 3) + (ileri * 2)
  print(birlikte)
  print(birlikte + "Mmm" + birlikte)



.. basic = "Ma"
..  print(basic)
..  basic3 = basic + basic + basic
..  print(basic3)
..  next = "Mow"
..  next3 = next * 3
..  print(next3)
..  together = (basic * 3) + (next * 2)
..  print(together)
..  print(together + "Mmm" + together)
  
..	index::
	single: dot-notation
	pair: programming; dot-notation

Ayrıca; bir **dizinin (string)**, mevcut diziden aynı yolla değiştirilen yeni bir diziye dönüştürülmesi istenebilir.  Aşağıdaki örnekte, bir diziyi tümü büyük harf olacak şekilde alacağız ve onu büyük harflere çevirilmiş bir cümleye dönüştüreceğiz.  Bu örnek, bir diziyi nasıl değiştirmek istediğimizi bildirmek için  bir yol olan **nokta gösterimini (dot-notation)** (``sentence.lower()``) kullanır.

.. A string can also be asked to return a new string that is changed in some way from the original string.  In the example below, we'll take a string in all-caps and turn it into a nicely capitalized sentence.  This example uses **dot-notation** (``sentence.lower()``) which is the way to tell a string how we want it to change. 

.. activecode:: String_Methods
   :tour_1: "Line-by-line Tour"; 1: str2-line1; 2: str2-line2; 3: str2-line3; 4: str2-line4; 5: str2-line5;
   :nocodelens:
   
   sentence = "THIS IS A TEST"
   better = sentence.lower()
   print(better)
   betterStill = better.capitalize() + "."
   print(betterStill)



 ..  sentence = "THIS IS A TEST"
 ..  better = sentence.lower()
 ..  print(better)
 ..  betterStill = better.capitalize() + "."
 ..  print(betterStill)
 


.. mchoice:: 1_4_1_String_Methods_Q1
   :answer_a: Hi There
   :answer_b: HiThere
   :answer_c: Hi There Hi There
   :answer_d: HiThereHiThere
   :answer_e: HiThere2
   :correct: d
   :feedback_a: Yanlış. Stringleri birbirine eklediğinizde, aslında ilave bir alan eklemeden, ikinci stringi birinci stringin ardına kopyalamış olursunuz
   :feedback_b: Yanlış. "*2" 'nin aynı stringin tekrar eden iki kopyası olduğunu hatırlayalım. 
   :feedback_c: Yanlış. Stringleri birbirine eklerken ya da stringleri tekrar ettirirken stringlerin arasına boşluk koymuş olmayız.
   :feedback_d: Doğru. Stringler birbirine eklenirken ya da tekrar ederken aralarında siz eklemediğiniz sürece boşluk olmaz. 
   :feedback_e: Yanlış. "*2" işleme girdiği stringi iki kez tekrar eder yani aynı stringin kopyasını arada boşluk olmadan ardına ekler. 
   
   Aşağıdaki kodun çıktısı ne olacaktır?
   
   :: 
   
      first = "Hi"
      next = "There"
      print ((first + next) * 2)







  
.. 
   :answer_a: Hi There
   :answer_b: HiThere
   :answer_c: Hi There Hi There
   :answer_d: HiThereHiThere
   :answer_e: HiThere2
   :correct: d
   :feedback_a: When you add strings together you copy the second string right after the first, without any added space
   :feedback_b: Remember that * 2 repeats two copies of the same string
   :feedback_c: Adding strings together and repeating them doesn't add spaces between the strings
   :feedback_d: Strings are added together without adding any space and they are repeated without adding a space
   :feedback_e: The * 2 repeats the string two times
   
   What would the following code print?
   
   :: 
   
      first = "Hi"
      next = "There"
      print ((first + next) * 2)




