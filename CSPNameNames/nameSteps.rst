..  Copyright (C)  Mark Guzdial, Barbara Ericson, Briana Morrison
    Permission is granted to copy, distribute and/or modify this document
    under the terms of the GNU Free Documentation License, Version 1.3 or
    any later version published by the Free Software Foundation; with
    Invariant Sections being Forward, Prefaces, and Contributor List,
    no Front-Cover Texts, and no Back-Cover Texts.  A copy of the license
    is included in the section entitled "GNU Free Documentation License".

.. 	qnum::
	:start: 1
	:prefix: csp-6-3-
	
.. highlight:: java
   :linenothreshold: 4

Adımlara İsim Verme
=====================

Daha önce kullandığımız ``abs`` and ``int`` nasıl tanımlandı? Yeni prosedür ve fonksiyonları *tanımlayarak*, bir ismi bir dizi adımla ilişkilendirebiliriz. Aşağıdaki programı inceleyin. |runbutton| butonuna bastığınızda ne olmasını beklersiniz ? Hadi programı çalıştıralım ve ne olacağını görelim.


.. activecode:: First_Function
  :tour_1: "Line by line tour"; 1: dsq-line1; 2: dsq-line2; 3: dsq-line3; 4: dsq-line4; 5: dsq-line5; 6: dsq-line6; 7: dsq-line7; 8: dsq-line8; 9: dsq-line9;
  :nocodelens:

  def tekerleme(cumle):
    print("Hadi biraz eğlenelim 🕺🕺🕺")
    print(cumle * 2)
    print("Hadi ama daha iyisini yaparsın 😉")
    print(cumle * 3)
    print("Zorlanmaya başladın galiba 😎")
    print(cumle * 4)
    print("Çok iyi gidiyorsun 🎯")
    print(cumle * 5)
    print("Bravo 👏 🏆 👏")

     

|runbutton| butonu neden hiçbir şey göstermedi ? Çünkü programın tek yaptığı ``tekerleme`` yordamını ``cumle`` girdisi ile tanımlamaktır. Eğer bu programın yürütülmesini (execute) istiyorsak bir sonraki örneğimizde olduğu gibi, ``cumle`` 'yi yaratmalı ve ``yordamı`` çağırmalıyız *(calling procedure)*



..	index::
	single: def
	single: functions
	single: calling functions

.. activecode:: First_Function_Call
  :tour_1: "Important lines tour"; 1-9: dsq2-line1-9; 11-13: dsq2-line11-13; 14: dsq2-line14;
  :nocodelens:

  def tekerleme(cumle):
    print("Hadi biraz eğlenelim 🕺🕺🕺")
    print(cumle * 2)
    print("Hadi ama daha iyisini yaparsın 😉")
    print(cumle * 3)
    print("Zorlanmaya başladın galiba 😎")
    print(cumle * 4)
    print("Çok iyi gidiyorsun 🎯")
    print(cumle * 5)
    print("Bravo 👏 🏆 👏")

    
  tekerlemeCumlesi = "dal sarkar kartal kalkar\n"
  tekerleme(tekerlemeCumlesi)
  
..	index::
	single: parameter
	pair: programming; parameter    

Yukardaki programda, ``tekerleme`` kelimesini tekerleme oyunu adımlarını temsil edecek şekilde *tanımladık (DEFine)* . ``tekerleme`` yordamı ``tekerlemeCumlesi`` girdisi ile bir tekerleme oyunu oynar. 
``tekerleme`` yordamının temsil ettiği adımların yani gövdesindeki deyimlerin  girintili olduğuna dikkat edelim. Python girintileri hangi deyimin yordama ait olduğunu göstermek için kullanır, tıpkı hangi deyimin hangi döngüye ait olduğunu göstermek için kullandığı gibi. 
Girintinin bittiği ``tekerlemeCumlesi = "dal sarkar kartal kalkar\n"`` deyimi ile birlikte yordam tanımı da bitmiş olur.

.. In the above program, we *DEFine* the word ``square`` to represent the Python statements that draw a square with a turtle.  The ``square`` procedure takes as input a ``turtle`` that will be used to draw the square. Notice that the sequence of statements that are part of the ``square`` procedure are indented.  Python uses indention to show what statements belong to the procedure.  When the indention stops with ``from turtle import *`` it means that the new statements are not part of the procedure.  

.. Note::
   Diğer isimlerde olduğu gibi yordamlarda da önce  ``def tekerleme (cumle):`` ile yordamımızı tanımladığımıza daha sonra ``tekerleme(tekerlemeCumlesi)`` ile yordamımızı çağırdığımıza yani kullandığımıza dikkat edelim.
   
İşlev (Fonksiyon) Tanımlama
--------------------

İşlevleri de yordamları tanımladığımız gibi tanımlarız fakat işlevlerin yordamlardan farklı olarak aşağıdaki örnekte de görebileceğiniz gibi ``geri dönüş değerleri (return value)`` vardır. 

.. activecode:: def_function
  :nocodelens:

  def dikdortgenAlan(uzunKenar, kisaKenar):
      return uzunKenar * kisaKenar
      
  print(dikdortgenAlan(12, 5))


.. activecode:: def_function2
  :nocodelens:

  def kup(sayi):
      return sayi * sayi * sayi
      
  print(kup(2))
  print(kup(5)) 
  print(kup(10))



.. activecode:: def_function3
  :nocodelens:

  def enKucuk(sayi1, sayi2):
      if sayi1 < sayi2:
          return sayi1
      elif sayi2 < sayi1:
	  return sayi2
      else:
	  return "Sayilar eşit"
      
  print(enKucuk(60, 2))
  print(enKucuk(20, 25))
  print(enKucuk(20, 20))
  print(enKucuk(17, 651))


  
.. note::
   Python'da bir işlevin değer döndürmesi ``return`` anahtar sözcüğü ile ifade edilir. 
  
**Check Your Understanding**

.. mchoice:: 6_3_1_Functions_Q2
   :answer_a: Yordam ~ Procedure
   :answer_b: İşlev ~ Function
   :correct: b
   :feedback_a: Yanlış. Değer döndüğü için bir işlevdir .
   :feedback_b: Doğru. Değer döndürdüğü için yordam olamaz

   ``abs`` bir yordam mıdır işlev midir ? 
   
.. mchoice:: 6_3_2_Functions_Q3
   :answer_a: Yordam ~ Procedure
   :answer_b: İşlev ~ Function
   :correct: a
   :feedback_a: Doğru. Değer döndürmediği için yordamdır
   :feedback_b: Yanlış. Değer döndürmediği için işlev olamaz.

   ``tekerleme`` bir yordam mıdır işlev midir ? 
   
Aşağıdaki videoyu izleyerek bir sonraki sürükle bırak sorusunu nasıl yapacağını öğrenebilrsin. 

.. video:: indentVideo
		   :controls:
		   :thumb: ../_static/video-mixedUpCodeIndent.png

		   http://ice-web.cc.gatech.edu/ce21/1/static/video/IndentVideo.mov
		   http://ice-web.cc.gatech.edu/ce21/1/static/video/IndentVideo.webm
   
.. parsonsprob:: 6_3_3_Triangle_Procedure

   Aşağıdaki kod öğrenci bilgilerini ekrana yazdıran bir prosedür olmalıdır. Kod bloklarını doğru sırada olacak şekilde gerekli kodları aşağı tarafa sürükleyin. Yordama ait deyimlerin girintili yazıldığını ve giritili kısımların daha sağda olması gerektiğini unutmayın. 

   -----
   def ogrenci(isim, soyisim, ders, not1, not2):
   =====
       print("öğrencinin adı soyadı : " + isim + " " + soyisim)
       print(ders + "dersinden aldığı notlar: ")
       print("İlk Sınav: " + str(not1) + " İkinci Sınav: " + str(not2))
       print(isim + " " + soyisim + " adlı öğrencinin " + ders + " dersi ortalaması: " + str((not1 + not2) / 2))
  
   ===== 
       endDef #distractor


