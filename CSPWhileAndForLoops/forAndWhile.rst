..  Copyright (C)  Mark Guzdial, Barbara Ericson, Briana Morrison
    Permission is granted to copy, distribute and/or modify this document
    under the terms of the GNU Free Documentation License, Version 1.3 or
    any later version published by the Free Software Foundation; with
    Invariant Sections being Forward, Prefaces, and Contributor List,
    no Front-Cover Texts, and no Back-Cover Texts.  A copy of the license
    is included in the section entitled "GNU Free Documentation License".

.. 	qnum::
	:start: 1
	:prefix: csp-8-1-
	
.. highlight:: java
   :linenothreshold: 4
   
	
Döngüler ~ for ve while
=======================


*Öğrenme Hedefleri:*

- Mantıksal bir ifade doğru iken bir döngünün gövdesini tekrarlayan, while döngüsü kavramını tanıtmak,
- Doğru veya yanlış olan mantıksal ifade kavramını tanıtmak,
- Hiçbir zaman sonlanmayan, sonsuz döngü kavramını tanıtmak, 
- for ve while döngü yapılarını karşılaştırmak ve kıyas etmek.



.. *Learning Objectives:*

.. - Introduce the concept of a ``while`` loop, which will repeat the body of a loop while a logical  expression is true.
.. - Introduce the concept of a *logical expression*, which is either true or false.
.. - Introduce the concept of an *infinite loop*, which is a loop that never ends.
.. - Compare and contrast ``while`` and ``for`` loops

..	index:
	single: while
	single: body of a loop
	single: logical expression
	pair: statements; while
	pair: statements; for
	pair: loop: while
	pair: loop: for
	
.. Example For Loop
For Döngüsü Örneği
-----------------

Biz ``for`` döngüsünü, **döngünün gövdesinin** ne kadar süre tekrar edeceğini bildiğimiz durumlarda kullanıyoruz. **Döngünün gövdesi (body of loop)** , ``for`` deyimini izleyen ve sağına doğru girintilenmiş tüm ifadelerdir. **Döngünün gövdesinin** bir parçası olan deyimleri belirtmek için 4 boşluk girdiğinizden emin olun.



.. We have been using a ``for`` loop to repeat the **body of a loop** a known number of times.  The **body of a loop** is all the statements that follow the ``for`` statement and are indented to the right of it.  Be sure to indent 4 spaces to indicate the statements that are part of the body of the loop.

Aşağıdaki for_sayaci 'da kodun içine girmeden önce, basacağı son değeri tahmin etmeye çalışın ve sonra aşağıdaki soruyu yanıtlayın.


.. Before you step through the code in for_counter below, try to predict the last value it will print and then answer the question below.


.. mchoice:: 8_1_1_For_Counter_Q1
		  :answer_a: 9
		  :answer_b: 10
		  :answer_c: 11
		  :correct: a
		  :feedback_a: Doğru. Bir aralık, başlangıç noktasından bitiş noktasından 1 daha azına gider. Eğer 10'a kadar saymak istiyorsak, range(1,11) kullanın.
		  :feedback_b: Yanlış. Aralık, son değeri içermiyor. Son değerden önce durur.
		  :feedback_c: Yanlış. Aslında, 10'a bile ulaşmıyor! Dene.

	   	  Aşağıdaki kod çalıştırıldığında yazdırılacak son değer nedir?






..		  :answer_a: 9
..		  :answer_b: 10
..		  :answer_c: 11
..		  :correct: a
..		  :feedback_a: A range goes from a starting point to one <i>less</i> than the ending point. If we want to count to 10, use range(1,11).
..		  :feedback_b: The range doesn't include the end value.  It stops at one before the last value.
..		  :feedback_c: In fact, it doesn't even get to 10! Try it.

..	   	  What is the last value that will be printed when the code below executes?
	   	  

1'de başlayan ve her defasında 1'er artan bir sayı yazdırmak istiyorsak, bunu bir ``for`` döngüsü ile kolayca yapabiliriz.
Sayacın her zaman döngüde nasıl yeni bir değer aldığını görmek için *Forward (İleri)* düğmesini kullanın.


.. If we want to print out a count that starts at 1 and increases by 1 each time, we can do easily do that with a ``for`` loop.  Use the *Forward* button to see how counter takes on a new value each time through the loop.


.. codelens:: for_counter

	for sayac in range(1,10):
	    print("sayac= ", sayac)

.. codelens: for_counter

	.. for counter in range(1,10):
	    print(counter)


.. Introducing the While Loop	   	  
while Döngüsüne Giriş
----------------------------


İfadeleri tekrar etmenin diğer bir yolu da ``while`` döngüsüdür. Mantıksal ifade doğru olduğu sürece **döngünün gövdesini (body of loop)** tekrar eder. Döngünün gövdesi, ``while`` deyiminin sağında 4 veya daha fazla boşluk girintili deyim veya deyimlerdir. **Mantıksal ifade (logical expression)**, cevabı doğru ya da yanlış olan, ``x > 3`` gibi bir ifadedir.

.. Another way to repeat statements is the ``while`` loop.  It will repeat the **body of loop** as long as a **logical expression** is true.  The **body of the loop** is the statement or statements that are indented 4 or more spaces to the right of the ``while`` statement.   A **logical expression** is one that is either true or false like ``x > 3``.  

``While`` döngüleri genellikle döngüyü kaç defa çalıştıracağımızı bilmediğimiz durumlarda kullanılır. Örneğin, bir oyun oynarken oyunu kazanan olmadığı *sürece(while)* tekrar edersin. Eğer sandalye kapmaca oyunu oynadıysanız bilirsiniz ki müzik çaldığı *sürece(while)* sandalyeler çevresinde dolanırsınız.



.. ``While`` loops are typically used when you don't know how many times to execute the loop.  For example, when you play a game you will repeat the game *while* there isn't a winner.  If you ever played musical chairs you walked around the circle of chairs *while* the music was playing.


Girdiğiniz numara negatif olmadığı sürece aşağıdaki kod dönecektir. Negatif olmayan her sayıyı geçerli toplama ekler. Girdiğiniz tüm sayıların toplamını ve ortalamasını yazdıracaktır.

.. The code below will loop as long as the number that you enter isn't negative.  It will add each non negative number to the current sum.  It will print out the sum and average of all of the numbers you have entered.



.. activecode:: while_ile_girdi_alma
	
    toplam = 0
    sayac = 0
    mesaj = "Toplamı ve ortalaması hesaplanacak tam sayıları girin veya hesaplamadan çıkmak için negatif bir sayi girin. "
    deger = input(mesaj)
    while int(deger) > 0:
        print("Girdiğiniz sayı:  " + deger)
        toplam = toplam + int(deger)
        sayac = sayac + 1
        deger = input(mesaj)
    print("Toplam: " + str(ortalama) + 
          " ortalama: " + str(toplam / sayac))


.. activecode: while_input
	
..   sum = 0
..   count = 0
..    message = "Enter an integer or a negative number to stop"
..    value = input(message)
..    while int(value) > 0:
..        print("You entered " + value)
..        sum = sum + int(value)
..        count = count + 1
..        value = input(message)
..    print("The sum is: " + str(sum) + 
          " the average is: " + str(sum / count))
    
.. mchoice:: 8_1_2_While_Input1
		  :answer_a: 3
		  :answer_b: 4
		  :answer_c: 5
		  :answer_d: 6
		  :correct: b
		  :feedback_a: Yanlış. While döngü deyiminin sağında 4 boşluk ile girintilenmiş tüm deyimler döngü gövdesinin parçasıdır.
		  :feedback_b: Doğru. While deyiminin sağında 4 boşluk girintili dört deyim vardır, dolayısıyla bu döngüde dört deyim vardır.
		  :feedback_c: Yanlış. print(mesaj) deyimi, while deyimi sağına 4boşluk ile girintilenmiş mi? Değilse döngünün gövdesinin bir parçası değildir.
		  :feedback_d: Yanlış. 11. satır girintili iken, bu yalnızca baskı deyiminin bir satırdan fazlasını almasına izin vermek içindir. Baskı deyimi girintili değildir, böylece döngü gövdesi sadece 4 satır içerir.

	   	  Yukarıda *while_ile_girdi_alma* kod bloğunda ``while`` döngüsünün gövdesinde kaç satır vardır?




..  8_1_2_While_Input1
..		  :answer_a: 3
..		  :answer_b: 4
..		  :answer_c: 5
..		  :answer_d: 6
..		  :correct: b
..		  :feedback_a: All the statements that are indented 4 spaces to the right of the <code>while</code> are part of the body of the loop.
..		  :feedback_b: There are four statements that are indented 4 spaces to the right of the <code>while</code> statement, so there are four statements in the body of this loop.
..		  :feedback_c: Is the <code>print(message)</code> line indented 4 spaces to the right of the <code>while</code>? If not it is not part of the body of the loop.
..		  :feedback_d: While line 11 is indented this is just to allow the print statement to take up more than one line.  The print statement is not indented so the body of the loop contains just 4 lines.

..	   	  How many lines are in the body of the ``while`` loop in while_input above?




	   	  
.. mchoice:: 8_1_2_While_InputError
		  :answer_a: Ortalama ve toplam için sıfır yazdırır.
		  :answer_b: Bu 0’a bölemeyeceğine dair bir mesaj yazdırır. 
		  :answer_c: Hata olmaz.
		  :correct: c
		  :feedback_a: Yanlış. Programda bunu yapacak kod görüyor musunuz?
		  :feedback_b: Yanlış. Bu hoş olabilir, ama bu ne olur?
		  :feedback_c: Doğru. ZeroDivisionError hata mesajı alırsın, çünkü sıfıra (sayac = 0) bölemezsin.
		  
	   	  Yukarıdaki kodun ilk girdisi olarak negatif bir sayı girerseniz ne olur?




	   	  
.. 8_1_2_While_InputError
..		  :answer_a: It prints the sum is 0 and the average is 0.
..		  :answer_b: It prints a message that it can't divide by 0.  
..		  :answer_c: There is an error.
..		  :correct: c
..		  :feedback_a: Do you see code to do this in the program?
..		  :feedback_b: This might be nice, but is that what happens?
..		  :feedback_c: You will get a ZeroDivisionError since you can't divide by zero.
..		  
..	   	  What happens if you enter a negative number as the first input to the code above?


