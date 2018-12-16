..  Copyright (C)  Mark Guzdial, Barbara Ericson, Briana Morrison
    Permission is granted to copy, distribute and/or modify this document
    under the terms of the GNU Free Documentation License, Version 1.3 or
    any later version published by the Free Software Foundation; with
    Invariant Sections being Forward, Prefaces, and Contributor List,
    no Front-Cover Texts, and no Back-Cover Texts.  A copy of the license
    is included in the section entitled "GNU Free Documentation License".

.. 	qnum::
	:start: 1
	:prefix: csp-12-5-
	
.. highlight:: python
   :linenothreshold: 3

Karmaşık Koşullular (and, or, and not) ~ Complex Conditionals 
=========================================

.. 	index::
	single: and
	single: or
	pair: logical operators; and
	pair: logical operators; or
	pair: logical operators; not
	

Birden fazla mantıksal ifadeyi birleştirmek için ``and`` ve ``or`` işleçlerini beraber kullanabiliriz. Birden fazla ifadenin ``or`` işleci kullanarak birleştirildiği bir ifade ancak, *ifadelerden en az bir tanesi* ``true (doğru)``  ise ``true (doğru)`` olarak kabul edilir. Birden fazla ifadenin ``and`` işleci kullanarak birleştirildiği bir karmaşık bir ifade ise, ancak ifadelerden hepsi doğru ise doğru olarak kabul edilir. ``not`` işleci ise kendisini takip eden mantıksal değeri olumsuzlar. Dolayısıyla eğer değer `` doğru (true)``, ise not işleci onu ``yanlış (false)`` yapar. Eğer tam tersi değer yanlış ise, ``not`` işleci onu doğru olarak değiştirir.

We can also use ``and`` and ``or`` to join several logical expressions together as shown in the table below.  An ``or`` joining two expressions means that if *either* of the expressions is true, the whole expression is true.  An ``and`` used to join two expressions is only true if *both* expressions are true.  A ``not`` negates the logical value that follows it.  If it was true, then a ``not`` changes the result to false.  If it was false, the ``not`` changes the result to true.

====================        ================ 
İfade                       Anlamı
====================        ================
(a < b) or (c < d)          Eğer a, b’den küçük ya da c, d’den küçükse bütün ifade doğru olarak kabul edilir. 
--------------------        ----------------
(a < b) and (c < d)         Eğer a, b’den küçük ve aynı zamanda c de d’den küçük, bütün ifade doğru kabul edilir  
--------------------        ----------------
not a < b                   Bu ifade ancak a b’den büyük ya da b’ye eşitse doğru kabul edilir. Bu mantıksal ifade ``not a < b`` aslında ``a >= b`` ile aynıdır.
====================        ================


``and`` işlecinin en genel kullanımı, bir değerin bir aralık arasında olup olmadığını kontrol etmektir. Örneğin bir kişiye 1 ve 10 arasında bir sayı seçmesini istediyseniz, girilen sayıyı aşağıdaki kod ile kontrol edebilirsiniz.

.. A common use of ``and`` is to check that a value is in a range between a minimum value and a maximum value.  For example, if you have asked a person to pick a number between 1 and 10 you can check for this using the following.

.. activecode:: Ornek_Islec_and
  :tour_1: "Yapısal Tur"; 1: and1-line1; 2-3: and1-line2-3; 4: and1-line4;

  x = int(input("Lütfen 1 ve 10 arasında bir sayı giriniz"))
  if x >= 1 and x <= 10:
      print ("Girdiğiniz sayı geçerli")
  print ("İşlem tamamlandı")
  
.. mchoice:: 12_5_1_and1
  :answer_a: 1’den 10’a kadar (10 dahil) 
  :answer_b: 0’dan 9’a kadar (9 dahil)
  :answer_c: 1’den 9’a kadar (9 dahil) 
  :correct: c
  :feedback_a: Eğer ikinci ifade x <= 10 olsaydı, verdiğin cevap doğru olurdu 
  :feedback_b: Eğer ilk mantıksal ifade x >= 0 olsaydı, verdiğin cevap doğru olurdu
  :feedback_c: "Koşul doğru" ifadesi sadece x değeri 0’dan büyük 10’dan küçükse ekrana basılır, dolayısıyla 1 ve 9 aralığındadır

   Aşağıda verilen kodda, x’in hangi değerleri ekrana “koşul doğru” basılmasını sağlıyor?

   
   :: 
   
     if x > 0 and x < 10:
         print ("Koşul doğru")
     print ("İşlem tamamlandı")
    


``or`` işleci ise genel olarak iki ifadeden herhangi birisi doğru mu diye kontrol etmek için kullanılır. Örneğin bir aile çocuğuna, eğer odasını temizlediyse ya da ödevinin bitirdiyse dışarı çıkabileceğini söyledi. Dolayısıyla bunlardan herhangi birisi doğru ise, çocuk dışarıya çıkabilir. Python dilinde, ``0`` değeri yanlışı (false) ifade etmek için kullanılır, 0 dışındaki diğer değerler ise doğruyu (true) ifade eder. Ancak genellikle doğruyu ifade etmek için ``1``  sayısını kullanırız.


.. A common use of ``or`` is to check if either one of two conditions are true.  For example, a parent has told a teen that she can go out if she has cleaned her room or finished her homework.  If either of these is true she can go out.  In Python a value of ``0`` means false and any non-zero value is true, but ``1`` is often used for true.  

.. activecode:: Ornek_Islec_or
  :tour_1: "Yapısal Tur"; 1: and2-line1; 2: and2-line2; 3-4: and2-line3-4; 5: and2-line5;

  odaTemiz = int(input("oda temizse 1 girin, temiz değilse 0"))
  odevBitti = int(input("ödev bittiyse 1 girin, değilse 0"))
  if odaTemiz or odevBitti:
      print ("Dışarı çıkabilirsin!")
  print ("İşlem tamamlandı")
  
.. mchoice:: 12_5_2_or1
  :answer_a: x’in bütün değerleri
  :answer_b: 1’den 9’a kadar (9 dahil) 
  :answer_c: 0’dan 9’a kadar (9 dahil)
  :correct: a
  :feedback_a: Doğru. Bu koşul eğer x 0’dan büyükse ya da 10’dan küçükse doğrudur. Dolayısıyla x’in bütün değerlerini kapsar.)  
  :feedback_b: Yanlış. Eğer or yerine and kullanılsaydı verdiğin cevap doğru olurdu
  :feedback_c: Yanlış. Eğer or yerine and kullanılsaydı ve ilk ifade x >= 0 olsaydı verdiğin cevap doğru olurdu. 

   Aşağıda verilen kodda, x’in hangi değerleri ekrana “koşul doğru” basılmasını sağlıyor?
    
   :: 
   
     if x > 0 or x < 10:
         print ("Koşul doğru")
     print ("İşlem tamamlandı")


