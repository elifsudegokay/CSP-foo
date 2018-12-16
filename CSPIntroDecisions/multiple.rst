..  Copyright (C)  Mark Guzdial, Barbara Ericson, Briana Morrison
    Permission is granted to copy, distribute and/or modify this document
    under the terms of the GNU Free Documentation License, Version 1.3 or
    any later version published by the Free Software Foundation; with
    Invariant Sections being Forward, Prefaces, and Contributor List,
    no Front-Cover Texts, and no Back-Cover Texts.  A copy of the license
    is included in the section entitled "GNU Free Documentation License".

.. 	qnum::
	:start: 1
	:prefix: csp-12-3-
	
.. highlight:: python
   :linenothreshold: 3

Çoklu if Deyimi Kullanımı - Using Multiple if statements
====================================

Kodunuzuda birden çok ``if`` deyimi kullanabilirsiniz. Burada iki ``if`` deyimi kullanan bir hesaplamanın örneği var. Fiyatının ağırlığına dayalı olduğu bir parçanın toplam maaliyetini hesaplayalım. Eğer parçanın ağırlığı 1 pound’tan az ise fiyatı 1.45 pound. Eğer ağırlığı 1 pound ve üstündeyse fiyat 1.15 pound.

.. You can use more than one ``if`` statement in your code.  Here's an example of a calculation that uses two ``if`` statements.  Let's compute the total cost of an item where the price is based on the weight of the item.  If the item weighs less than 1 pound then the price is 1.45 a pound.  If the item weighs 1 pound or more the price is 1.15 a pound.

.. activecode:: Fiyat_If
    :tour_1: "Yapısal Tur"; 1: c1-line1; 2-3: c1-line2-3; 4-5: c1-line4-5; 6: c1-line6; 7-9: c3f-line7-9;
    
    agirlik = 0.5
    if agirlik < 1:
    	fiyat = 1.45
    if agirlik >= 1: 
    	fiyat = 1.15
    toplam = agirlik * fiyat
    print(agirlik)
    print(fiyat)
    print(toplam)

Yukarıdaki kodu düzenleyin ve ilk satırdaki ``agirlik`` değerinin farklı olmasını sağlayarak Tekrar çalıştırıp ve neyin değiştiğini görün. Ayrıca, agirlik için farklı değerlerin yürütülen kod satırlarını nasıl değiştirdiğini görmek için codeLens’te deneyin.
.. Edit the code above and change the first line so that ``weight`` has a different value. Run it again and see what changes.  Try it in the codelens as well to see how the different values for weight changes the lines of code that are executed.   

Bu ikinci versiyonda, *varsayılan (default)* olarak bir ``fiyat`` belirledik, sonra sadece özel bir koşulda değiştirdik. Bu kod yukarıdaki örnekle aynı şekilde çalışır mı?
.. In this second version, we set a ``price`` as a *default*, then change it only on the special condition. Does it work the same as the above example?

.. activecode:: Fiyat_If2
  :tour_1: "Yapısal Tur"; 1: c2-line1; 2: c2-line2; 3-4: c2-line3-4; 5: c2-line5; 6-8: c3f-line7-9;

  agirlik = 0.5
  fiyat = 1.45
  if agirlik >= 1: 
      fiyat = 1.15
  toplam = agirlik * fiyat
  print(agirlik)
  print(fiyat)
  print(toplam)

.. mchoice:: 12_3_1_Price_If_Equivalent
  :answer_a: Hayır, her zaman aynı (Son sonuç aynı).
  :answer_b: Evet, ağırlık tam olarak 1 pound ise farklıdırlar.( Ağırlık tam olarak 1 pound ise, her iki programda fiyat 1,15 olacaktır.)
  :answer_c: Evet, ağırlık 1 poundun altındaysa farklılar. (Ağırlık 1 poundun altında ise, fiyat iki programda da 1.45 olacaktır.)
  :answer_d: Evet, ağırlık 1 poundun üstündeyse farklıdırlar.( Ağırlık 1 pound'un üzerindeyse, her iki programda da fiyat 1,15 olacaktır.)
  :correct: a
  :feedback_a: Doğru. Son sonuç aynı.
  :feedback_b: Yanlış. Eğer agirlik 1 pound olsaydı, fiyat 1.15 olurdu. 
  :feedback_c: Yanlış. Eğer agirlik 1 pound'un altında olsaydı, fiyat iki programda da 1.45  olurdu. 
  :feedback_d: Yanlış. Eğer agirlik 1 pound'un üstünde olsaydı, fiyat iki programda da 1.15  olurdu. 

   Her iki programda aynı ağırlık kullanıldığı zaman, yukarıdaki iki programı farklı çıktılar bastırtan ağırlık değerleri var mı?
   
**Karışık programlar**

.. parsonsprob:: 12_3_2_Price_By_Weight

..   The following program should calculate the total price, but the lines are mixed up.   The price is based on the weight.  Items that weigh less than 2 pounds should cost 1.5.  Items that weigh more than 2 pounds should cost 1.3.   Drag the blocks from the left and place them in the correct order on the right.  Be sure to also indent correctly! Click on <i>Check Me</i> to see if you are right. You will be told if any of the lines are in the wrong order or have the wrong indention.</p>
   Aşağıdaki program toplam fiyatı hesaplamalıdır, ancak satırlar karıştırılmıştır. Fiyat ağırlığa dayalıdır. 2 pounddan hafif ağılıklı parçaların fiyatı 1.5 olmalıdır. 2 poundan ağır parçaların fiyatı 1.3 olmalıdır. Blokları sola doğru sürükleyin ve sağdaki doğru sıraya yerleştirin. Ayrıca doğru girintili olduğundan emin olun! Doğru olup olmadığını görmek için “Check Me” tıklayınız. Hatlardan herhangi birinin yanlış sırada olup olmadığı veya yanlış girintiye sahip olup olmadığı size söylenecektir.</p>

   -----
   agirlik = 0.5
   parcaSayisi = 5
   if agirlik < 2:
   =====
       fiyat = 1.50
   =====
   if agirlik >= 2: 
   =====
       fiyat = 1.30
   =====
   toplam = agirlik * fiyat
   =====
   print(agirlik)
   print(fiyat)
   print(toplam)

.. tabbed:: 12_3_3_WSt

        .. tab:: Soru

           14 km taksi yolculuğu maliyetini hesaplayan ve sonucu ekrana yazdıran kodu yazın. Gidilen mesafe 12 km’den az veya eşit ise, maliyet $ 2.00/km, ve gidilen mesafe 12 km’den fazla ise maliyet $1,50/km’dir.
           
           .. activecode::  12_3_3_WSq
               :nocodelens:

        .. tab:: Cevap
            
          .. activecode::  6_5_2_WSa
              :nocodelens:
              
              mesafe = 14
              # koşulları belirleyelim
              if mesafe <= 12:
                  oran = 2.00
              if mesafe > 12:
                  oran = 1.50
              # SEYAHAT MAALİYETİ HESAPLAMA
              toplam = mesafe * oran
              print("Toplam seyhat maaliyeti: " + str(toplam))
                                

