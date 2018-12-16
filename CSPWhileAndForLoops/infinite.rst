..  Copyright (C)  Mark Guzdial, Barbara Ericson, Briana Morrison
    Permission is granted to copy, distribute and/or modify this document
    under the terms of the GNU Free Documentation License, Version 1.3 or
    any later version published by the Free Software Foundation; with
    Invariant Sections being Forward, Prefaces, and Contributor List,
    no Front-Cover Texts, and no Back-Cover Texts.  A copy of the license
    is included in the section entitled "GNU Free Documentation License".

.. 	qnum::
	:start: 1
	:prefix: csp-8-2-
	
.. highlight:: java
   :linenothreshold: 4

.. Infinite Loops
Sonsuz Döngüler
================

Bir dizi ifadeyi tekrarlamak için bilgisayar kullanımı kolaydır. Ama bazen onu (döngüyü) *durdurmak* beceri isteyebilir. Unutmayın, While döngüsü kullandığınız mantıksal ifade doğru olduğu sürece çalışmaya devam edecektir. Peki mantıksal ifade *her zaman* doğruysa ne olur?

.. Getting a computer to repeat a set of statements is simple.  Sometimes it can be tricky to get it to *stop*.  Remember that a while loop will execute as long as the logical expression is true.  What happens if the logical expression is *always* true?

..	index::
	single: infinite loop
	pair: loop; infinite
	
Yani, sonsuza kadar döngü içerisinde kalacak bir program 

.. sourcecode:: python

  	while 1 == 1:
  	    print("Sonsuza dek")
  	    print("Dönüyor")


Yukarıdaki örnekte ``1``  her zaman ``1`` ’e eşit olacağından, ekran çıktısı veren iki ``print`` deyimimiz de devamlı tekrarlanacak ve mantıksal ifademiz (1==1) hiçbir zaman yanlış olmayacaktır. Bu durumu **sonsuz döngü (inifinite loop)** diyoruz. **Sonsuz döngü** sonsuza kadar veya durmaya zorlanana kadar devam eden döngü anlamına gelmektedir.


.. Since ``1`` will always be equal to ``1``, the two ``print`` statements will just be repeated over and over and over again and the logical expression will never be false.  We call that an **infinite loop**, which means a loop that continues forever or until it is forced to stop. 




.. note::
   ``1 == 1`` ifadesi 1 değerinin 1’e eşit olup olmadığını kontrol eder. ``x = 3`` ifadesinin ``x`` değişkenine ``3`` değerini atamak için kullanıldığını hatırlayın. Değer atama işlemlerinde tek ``( = )`` eşittir operatörü kullanılırken karşılaştırma ve kontrol işlemlerinde eşit eşit ``( == )`` operatörünü kullanıyoruz.


.. The expression ``1 == 1`` tests if 1 is equal to 1.  Remember that ``x = 3`` sets the value of x to 3, it doesn't test if x is equal to 3.  To do that use ``x == 3``.  

Aşağıdaki kod bloğumuzu programımızı kolaylıkla durdurabileceğimiz bir python çalışma ortamında çalıştırdık:

.. sourcecode:: python

 	>>> while 1==1:
 	        print ("Dönüyor")
 	        print ("Sonsuza dek")
	Dönüyor
	Sonsuza dek
	Dönüyor
	Sonsuza dek
	Dönüyor
	Sonsuza dek
	Dönüyor
	Sonsuza dek
	
(Kodun çalışmasını bu noktada durdurduk.)

.. mchoice:: 8_2_1_While_Inf_NumLines
   :answer_a: 1
   :answer_b: 2
   :answer_c: 3
   :correct: b
   :feedback_a: Yanlış. Bütün deyimler 4 karakter girinti olarak yazıldığından dolayı while döngüsünün içeriği olarak yorumlanmaktadır.
   :feedback_b: Doğru. while'dan sonraki bütün deyimler 4 karakter girinti olarak yazıldığından while döngüsünün altında bulunan 2 satırlık kod bloğu while döngüsünün gövdesi  olarak yorumlanacaktır.
   :feedback_c: Yanlış. Toplam 3 satır kod bulunuyor, ama bütün satırlar (3 satır) while döngü deyiminin kendisi gövdenin bir parçası değildir.

   Yukarıdaki kodda ``while``  döngüsünün gövdesinde kaç satır kod bulunmaktadır?


.. 8_2_1_While_Inf_NumLines
..   :answer_a: 1
..   :answer_b: 2
..   :answer_c: 3
..   :correct: b
..   :feedback_a: All the statements that are indented 4 spaces to the right of the <code>while</code> are part of the body of the loop.
..   :feedback_b: There are two statements that are indented 4 spaces to the right of the <code>while</code> statement, so there are two statements in the body of this loop.
..   :feedback_c: There are three lines here total, but not all of them are in the body of the loop.

..   How many lines are in the body of the ``while`` loop in shown above?


