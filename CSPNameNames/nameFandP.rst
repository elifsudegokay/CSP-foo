..  Copyright (C)  Mark Guzdial, Barbara Ericson, Briana Morrison
    Permission is granted to copy, distribute and/or modify this document
    under the terms of the GNU Free Documentation License, Version 1.3 or
    any later version published by the Free Software Foundation; with
    Invariant Sections being Forward, Prefaces, and Contributor List,
    no Front-Cover Texts, and no Back-Cover Texts.  A copy of the license
    is included in the section entitled "GNU Free Documentation License".

.. 	qnum::
	:start: 1
	:prefix: csp-6-2-
	
.. highlight:: java
   :linenothreshold: 4

İşlevler ve Yordamlar Nasıl İsimlendirilir ?
========================================

..	index::
	single: procedure
	pair: programming; procedure
	
..	index::
	single: function
	pair: programming; function	
	

İsimleri, sayıları (Örneğin: hem ``3`` ya da  ``-325`` gibi tam sayılar hem de ``2.4`` ve ``-322.9392`` gibi ondalıklı sayılar) ve karakter dizilerini (string)  (Örneğin: ``"Selam olsun dört bir yana merhaba"`` ) temsil etmede nasıl kullanacağımızı öğrenmiştik. İsimleri kullanarak hesaplamalar yapmak istediğimizde, bilgisayar her bir ismin değerini ele alır ve o değer ile hesaplamayı yapar. Değerlerin yanı sıra bir dizi deyimi (statement) de adlandırabilir ve istediğimiz zaman bu deyimleri, verdiğimiz ismi kullanarak çalıştırabiliriz. Bu tıpkı birinden `Macarena <http://en.wikipedia.org/wiki/Macarena_(song)>`_ ya da  `Salsa <http://en.wikipedia.org/wiki/Salsa_(dance)>`_ gibi bildiği bir dansı yapmasını istemeye benzer çünkü eğer dans etmeyi biliyorsa adımları zaten tekrar edebilir.

.. We've already seen how we can use names to represent numbers (both integers like ``3`` and ``-325`` and decimal numbers like ``2.4`` and ``-322.9392``), strings (like ``"Hi There"``), turtles, and images.  When we do calculations using the names, the computer will look up the value for each name, and then use the value in the calculation.  We can also name a sequence of statements and then ask the computer to run that sequence whenever we use that name.  This is similar to asking someone to do a dance that they know, like the `Macarena <http://en.wikipedia.org/wiki/Macarena_(song)>`_ or `Salsa <http://en.wikipedia.org/wiki/Salsa_(dance)>`_. Once you know the dance you can do the steps.    

.. figure:: Figures/salsaDancer.jpg
    :height: 100px
    :align: center
    :alt: a women dancing Salsa
    :figclass: align-center

    Figure 1: A Salsa dancer
    

Programlamada bir dizi deyimi isimlendirebilmemize olanak sağlayan **yordam (procedure)** ve **işlev ~ fonksiyon(function)** olmak üzere iki terim vardır. **Yordam (procedure)** komutları çalıştıran ya da bir komuta yol açan fakat bir değer (value) ile sonuçlanmayan sıralı deyimlerin ismidir. . **İşlev ~ Fonksiyon (function)** ise sonlandığında bir değer üreten ve o değeri döndüren sıralı deyimlerin isimlendirilmiş halidir. Mesela ``abs`` kendisine girdi olarak verilen sayının mutlak değerini döndüren bir *işlev ~ fonksiyondur* , ``int`` *işlevi ~ fonksiyonu* ise ondalıklı olarak aldığı sayının tam sayı kısmını döndürür.

.. activecode:: Functions
  :tour_1: "Line by line tour"; 1: fun-line1; 2: fun-line2; 3: fun-line3; 4: fun-line4;

  print(" -5 sayısının mutlak değeri :")
  print(abs(-5))
  print("34.2 sayısının tam sayı kısmı: ")
  print(int(34.2))

.. mchoice:: 6_2_1_Functionsss_Q1
   :answer_a: -16
   :answer_b: -16.789
   :answer_c: 16.789
   :answer_d: 16
   :correct: d
   :feedback_a: Yanlış. abs işlevi negatifliği değiştirecektir.
   :feedback_b: Yanlış. Orjinal sayı değişecektir.
   :feedback_c: Yanlış. int işlevi ondalık kısmı kaldıracaktır.
   :feedback_d: Doğru. abs işlevi sonucu pozitif yapacak, int işlevi sayıdaki ondalıklı kısmı atarak sayının tam sayı kısmını bırakacaktır.

   Sence ``print(int(abs(-16.789)))`` , deyimi ekrana ne yazar?
