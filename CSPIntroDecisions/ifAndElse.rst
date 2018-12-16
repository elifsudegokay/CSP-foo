..  Copyright (C)  Mark Guzdial, Barbara Ericson, Briana Morrison
    Permission is granted to copy, distribute and/or modify this document
    under the terms of the GNU Free Documentation License, Version 1.3 or
    any later version published by the Free Software Foundation; with
    Invariant Sections being Forward, Prefaces, and Contributor List,
    no Front-Cover Texts, and no Back-Cover Texts.  A copy of the license
    is included in the section entitled "GNU Free Documentation License".

.. 	qnum::
	:start: 1
	:prefix: csp-12-7-
	
.. highlight:: python
   :linenothreshold: 3

if ve else Kullanımı
==========================

..	index::
   	pair: if; else

.. Most professional programmers would write the following code:
Profesyonel programcıların (yazılımcıların) çoğu şu kodu yazacaktır:

.. activeCode:: Coklu_If_2
     :tour_1: "Yapısal Tur"; 1: c1-line1; 2-3: c1-line2-3; 4-5: c1-line4-5; 6: c1-line6; 7-9: c3f-line7-9;

     agirlik = int(input("ağırlığı giriniz"))
     if agirlik < 1:
         fiyat = 1.45
     if agirlik >= 1: 
         fiyat = 1.15
     toplam = agirlik * fiyat
     print("ağırlık: ", agirlik)
     print("fiyat: ", fiyat)
     print("toplam: ", toplam)
     
Ya da aşağıdaki gibi bir kodu yazacaktır. 

.. activeCode:: if_ve_else
     :tour_1: "Yapısal Tur"; 1: c5-line1; 2-3: c5-line2-3; 4-5: c5-line4-5; 6: c5-line6; 7-9: c3f-line7-9;

     agirlik = int(input("ağırlığı giriniz"))
     if agirlik < 1:
         fiyat = 1.45
     else:
         fiyat = 1.15
     toplam = agirlik * fiyat
     print("ağırlık: ", agirlik)
     print("fiyat: ", fiyat)
     print("toplam: ", toplam)


``else``; bir ``if``  deyiminde (statement), isteğe bağlı ek bir tabirdir (phrase). SADECE VE SADECE``if`` deyimindeki (statement) *test*in **yanlış (false)** olması durumunda; ``else`` deyimi (statement) çalıştırılır ve sonrasındaki deyimler (statements) bloğuna geçilir. ``if``  ve ``else`` deyimlerinin beraber kullanımı; *ya* ``if``  bloğunu *ya da* ``else`` bloğunu çalıştırır, **asla** her ikisini de çalıştırmaz. 


.. An ``else`` is an additional optional phrase on an ``if`` statement.  IF AND ONLY IF the *test* in the ``if`` is **false** does the block of statements after the ``else`` get executed.  Using an ``if`` with an ``else`` makes sure that *either* the ``if`` block is executed *or* the ``else`` block is executed, but **never** both.  

.. figure:: Figures/ifAndElseFlow.png
    :height: 350px
    :align: center
    :alt: Flowchart for both an if and else
    :figclass: align-center

    Figure 4: Flow of execution for both an if and else
    
**Karışık programlar**

.. parsonsprob:: 12_7_1_Even_Odd

   Aşağıdaki program, x’in 2’ye bölümünden kalan 0 ise “x, çift bir sayıdır.” ifadesini ve aksi durumu için ise “x, tek bir sayıdır.” ifadesini yazdırmalıdır, ancak kod karışık haldedir. ``%`` sembolü, ilk sayının ikinci sayıya bölündükten sonraki kalanını verir. Soldaki blokları sürükleyin ve sağdaki boşluğa doğru sırada yerleştirin.  Ayrıca doğru girintili olduğundan emin olun! Doğru olup olmadığını görmek için <i> Beni Kontrol Et (Check Me)</i> butonuna tıklayın. Bloklardan herhangi birinin yanlış sırada veya yanlış girintili olup olmadığı size söylenecektir. </p>


   -----
   x = 92
   if x % 2 == 0:
       print("x çift sayıdır")
   else: 
       print("x tek sayıdır")


Bir kod bloğunu tam olarak çalıştırmak istediğinizde ``if`` deyimini (statement) kullanmak kolaydır ancak bunu yaparken yanlışlıkla bir *boşluk* yaratabilirsiniz – her iki kod bloğunun da çalışmadığı bir durum. Bu, ağırlık bir kilograma eşit olduğunda aşağıdaki örnekte olan durumdur.

.. It is easy to write an ``if`` when you want *exactly* one block to execute, but you can accidentally create a "hole" -- a condition where neither block executes.  That's what happened in the example below when the weight is equal to 1 pound.

.. activeCode:: Fiyat_if_2
     :tour_1: "Yapısal Tur"; 1: c1-line1; 2-3: c1-line2-3; 4-5: c3-line4-5; 6: c1-line6; 7-9: c3f-line7-9;

     agirlik = int(input("ağırlığı giriniz"))
     if agirlik < 1:
         fiyat = 1.45
     if agirlik > 1:
         fiyat = 1.15
     toplam = agirlik * fiyat
     print("ağırlık: ", agirlik)
     print("fiyat: ", fiyat)
     print("toplam: ", toplam)

.. tabbed:: 12_7_2_WSt

        .. tab:: Soru

           Yukarıdaki örneği; fincanınıza tam olarak 1 kg döktüğünüz takdirde dondurulmuş yoğurdun maliyeti 0 olacak şekilde düzeltin. 
           
           .. activecode::  12_7_2_WSq
               :nocodelens:

        .. tab:: Cevap
            
          .. activecode::  12_7_2_WSa
              :nocodelens:
              
              agirlik = int(input("ağırlığı giriniz"))
              if agirlik < 1:
                fiyat = 1.45
              if agirlik == 1:
                fiyat = 0
              if agirlik > 1: 
                fiyat = 1.15
              toplam = agirlik * fiyat
              print("ağırlık: ", agirlik)
              print("fiyat: ", fiyat)
              print("toplam: ", toplam)
                                

