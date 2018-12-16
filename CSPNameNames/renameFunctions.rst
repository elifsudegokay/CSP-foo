..  Copyright (C)  Mark Guzdial, Barbara Ericson, Briana Morrison
    Permission is granted to copy, distribute and/or modify this document
    under the terms of the GNU Free Documentation License, Version 1.3 or
    any later version published by the Free Software Foundation; with
    Invariant Sections being Forward, Prefaces, and Contributor List,
    no Front-Cover Texts, and no Back-Cover Texts.  A copy of the license
    is included in the section entitled "GNU Free Documentation License".

.. |bigteachernote| image:: Figures/apple.jpg
    :width: 50px
    :align: top
    :alt: teacher note

.. 	qnum::
	:start: 1
	:prefix: csp-6-7-
	
.. highlight:: java
   :linenothreshold: 4

Python İşlevlerinin Yeniden İsimlendirilmesi
=============================

``abs`` ve ``int``işlevlere verilen *isimlerdir*.  Onlar, bir sonuca ulaşmak için değerleri deyimler kümesinden oluşan *değişkenlerdir*. Daha sonra, kendi başımıza abs ve int fonksiyonlarını kendi başımıza yazacak kadar kod yazabileceğiz. Buradaki önemli nokta, ``abs`` ve ``int`` isimlerinin işlevlerin ismi olduğudur. Aynı değere sahip birçok isim yaratabilirsiniz. Bunu bir insanın hem gerçek isminin hem de rumuz(takma) isminin olması gibi düşünebilirsiniz. Aşağıdaki programda, Python işlevlerini dahi yeniden isimlendirebileceğimizi gösteriyoruz.


.. The functions ``abs`` and ``int`` are *names*.  They are *variables* whose values are a set of statements that achieve a goal.  Later on, we'll know enough code to write ``abs`` and ``int`` ourselves.  The important point right now is that ``abs`` and ``int`` are *names* for functions.  You can create several names that have the same value.  You can think of this like how a person can have both a name and a nickname.  In the program below we demonstrate that you can even create new names for Python functions.

.. activecode:: Rename_Internal
  :tour_1: "Line-by-line tour"; 1: funName-line1; 2: funName-line2; 3: funName-line3; 4: funName-line4; 5: funName-line5; 6: funName-line6;

  mutlak = abs
  print("-5’in mutlak degeri:")
  print(mutlak(-5))
  tamSayi = int
  print("34.2’nin tam sayi kismi:")
  print(tamSayi(34.2))

.. mchoice:: 6_7_1_Rename_Internal_Q1
   :answer_a: -16
   :answer_b: -16.789
   :answer_c: 16.789
   :answer_d: 16
   :correct: d
   :feedback_a: Hayır, mutlak işlevi negative sayıları pozitif olarak dönüştürür.
   :feedback_b: Hayır, İlk verilen değer değişir.
   :feedback_c: Yanlış. tamSayi işlevi ondalıklı kısmı atar.
   :feedback_d: Evet! Mutlak sayısı poazitif yapar ve tamSayi sadece sayının tam kısmını verir, sonuç olrak sadece elde 16 kalır.)
   
   Yukarıdaki programa print(tamSayi(mutlak(-16.789))) satırını eklersem, ekranda ne görürüm?
   

