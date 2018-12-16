..  Copyright (C)  Mark Guzdial, Barbara Ericson, Briana Morrison
    Permission is granted to copy, distribute and/or modify this document
    under the terms of the GNU Free Documentation License, Version 1.3 or
    any later version published by the Free Software Foundation; with
    Invariant Sections being Forward, Prefaces, and Contributor List,
    no Front-Cover Texts, and no Back-Cover Texts.  A copy of the license
    is included in the section entitled "GNU Free Documentation License".

.. 	qnum::
	:start: 1
	:prefix: csp-7-2-
	
.. highlight:: java
   :linenothreshold: 4

Sayılarla Tekrarlama
=======================

..	index::
	single: list

..	index::
	single: for loop
	pair: loop; for
	pair: loop; body
	pair: loop; indention
	
Bu bölümde ``for`` döngüsü kullanacağız. ``for`` döngüsü bir programdaki bir kod bloğunu veya deyimi tekrarlamak için kullanılan bir döngü deyimidir. ``for`` döngüsü değişkenleri kullanarak çalışır ve değişkenlerin her döngüde birer birer sayı **liste** sindeki değerleri almasını sağlar.  **Liste (list)** içerisindeki değerleri sıra ile tutmaktadır.

.. We are going to use a ``for`` loop.  A ``for`` loop is one type of loop or way to repeat a statement or set of statements in a program.  A ``for`` loop will use a variable and make the variable take on each of the values in a **list** of numbers one at a time.  A **list** holds values in an order.  


Dikkat, aşağıdaki kod bloğunun 3. Satırındaki ``for`` döngüsünün sonunda ``:``  bulunmaktadır. ``for`` döngülerinin satır sonlarında ``:``  ayracının bulunması gerekmektedir. 
döngü içerisinde çalışacak kod bloğu dört karakter içeriden başlamalı yani dört karakter **girintili (indented)** olarak yazılmalıdır. **Girintili (indented)** yazım şeklini daha önce if kullanımını öğrenirken de kullanmıştık. ``for`` döngü deyimi ve if deyimi için de ``:`` ayracının kullanımı ve girintili yazım zorunludur. 


.. note:: 
	Aşağıda bulunan sayiListesi değişkeni bir ``list (liste)`` idir. Listeler birden çok ve farklı türde değeri içlerinde sıralı halde tutabilirler. (Daha sonraki derslerde detaylı olarak öğreneceğiz). Aşağıdaki ``for`` döngüsü sayiListesi değişkeninden sıra ile değerleri alıp her seferinde aldığı değeri toplam değişkeninin değerine ekleme işlemi yapmaktadır.


.. Notice that line 3 in the program below ends with a ``:`` and that line 4 is **indented** four spaces so that it starts under the ``n`` in ``number``.  **Indented** means that text on the line has spaces at the beginning of the line so that the text doesn't start right at the left boundary. Both the ``:`` and the indention are required in a loop.  Line 3 is the start of the ``for`` loop and line 4 is the **body** of the loop.  The **body** of the loop is repeated for each value in the list ``thingsToAdd``.   

1’den 10’a kadar olan sayıların toplam değeri nedir? Öğrenmek için aşağıdaki kod bloğunu çalıştırın.

.. What is the sum of all the numbers between 1 and 10?  Run the program below to calculate the answer.

.. activecode:: Numbers_Repeat1
    :tour_1: "Line by line tour"; 1: for1_line1; 2: for1_line2; 3: for1_line3; 4: for1_line4; 5: for1_line5;
    :tour_2: "High level tour"; 1-2: for1_line1-2; 3-4: for1_line3-4; 5: for1_s_line5;
	
    toplam = 0
    sayiListesi = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
    for sayi in sayiListesi:
        toplam = toplam + sayi
    print('toplam: ', toplam)

.. sum = 0  # Start out with nothing
.. thingsToAdd = [1,2,3,4,5,6,7,8,9,10]
.. for number in thingsToAdd:
..	sum = sum + number
.. print(sum)
    
.. mchoice:: 7_2_1_Numbers_Repeat1_Q1
   :answer_a: Ekran çıktısı aynı kalacaktır
   :answer_b: Toplam değişkeninin değeri 10 kere ekrana yazdırılacaktır ve her seferinde toplam değeri değişecektir. 
   :answer_c: Ekrana toplam değişkenin aynı değerini 10 kere yazacaktır.
   :answer_d: Hata mesajı verecektir.
   :correct: b
   :feedback_a: Yanlış. Gerçekten 5. Satırı girintili yazıp denedin mi? 
   :feedback_b: Doğru.5. Satırda bulunan kod bloğu 4. Satırdaki kod gibi girintili (indented) yazıldığından artık for döngüsü içerisinde çalışacaktır yani her seferinde toplam değişkeninin değeri ekrana yazılacaktır. 
   :feedback_c: Yanlış. Toplam değişkenin değeri her seferinde değişiyor.  
   :feedback_d: Yanlış. Döngü içerisine bir satırdan fazla kod yazabiliyoruz.

   5. Satırdaki kodu 4. Satırdaki gibi girintili (indented) yazarsak ekran çıktısı ne olacaktır? 
   
.. mchoice:: 7_2_2_Numbers_Repeat1_Q2
   :answer_a: Ekran çıktısı aynı kalacaktır
   :answer_b: toplam değişkeninin değerini 10 kere (döngünün her aşamasında) ekrana yazar ve değişken değeri her seferinde değişir.
   :answer_c: toplam değişkeninin değeri 10 kere değer değişmeden ekrana yazar.
   :answer_d: Hata mesajı verecektir.
   :correct: d
   :feedback_a: Yanlış. Gerçekten denedin mi? 
   :feedback_b: Yanlış. 4. ve 5. Satırdaki kodlar artık for döngüsü içerisinde değil
   :feedback_c: Yanlış. print komutu tekrarlanıyor mu? Is the print repeated now? 
   :feedback_d: Doğru. Döngü içerisinde en az 1 satır kod bloğu olması gerekmektedir.

   4. ve 5. satırdaki kodları girintili (indented) olarak yazmaksak ekran çıktısı ne olacaktır? 




.. 
.. mchoice:: 7_2_1_Numbers_Repeat1_Q1
   :answer_a: It prints the same thing it did before.
   :answer_b: It prints the value of sum 10 times and sum is different each time it is printed.
   :answer_c: It prints the same sum 10 times.
   :answer_d: You get an error.
   :correct: b
   :feedback_a: Did you actually try it?
   :feedback_b: Both lines 4 and 5 are now in the body of the loop and are executed each time through the loop. 
   :feedback_c: Sum should be changing.  
   :feedback_d: You can have more than one line in the body of a loop.

   What is printed if you change the program above so that line 5 is also indented the same amount as line 4?
   
.. mchoice:: 7_2_2_Numbers_Repeat1_Q2
   :answer_a: It prints the same thing it did before.
   :answer_b: It prints the value of sum 10 times and sum is different each time it is printed.
   :answer_c: It prints the same sum 10 times.
   :answer_d: You get an error.
   :correct: d
   :feedback_a: Did you actually try it?
   :feedback_b: Both lines 4 and 5 are not in the loop anymore.
   :feedback_c: Is the print repeated now? 
   :feedback_d: You have to have at least one statement in the body of a loop.

   What is printed if you change the program above so that lines 4 and 5 are not indented?
   

