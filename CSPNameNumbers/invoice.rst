..  Copyright (C)  Mark Guzdial, Barbara Ericson, Briana Morrison
    Permission is granted to copy, distribute and/or modify this document
    under the terms of the GNU Free Documentation License, Version 1.3 or
    any later version published by the Free Software Foundation; with
    Invariant Sections being Forward, Prefaces, and Contributor List,
    no Front-Cover Texts, and no Back-Cover Texts.  A copy of the license
    is included in the section entitled "GNU Free Documentation License".

.. |runbutton| image:: Figures/run-button.png
    :height: 20px
    :align: top
    :alt: run button

.. |audiobutton| image:: Figures/start-audio-tour.png
    :height: 20px
    :align: top
    :alt: audio tour button

.. |codelensfirst| image:: Figures/codelens-first.png
    :height: 20px
    :align: top
    :alt: move to first button

.. |codelensback| image:: Figures/codelens-back.png
    :height: 20px
    :align: top
    :alt: back button

.. |codelensfwd| image:: Figures/codelens-forward.png
    :height: 20px
    :align: top
    :alt: forward (next) button

.. |codelenslast| image:: Figures/codelens-last.png
    :height: 20px
    :align: top
    :alt: move to last button
    
.. 	qnum::
	:start: 1
	:prefix: csp-3-8-

.. highlight:: java
   :linenothreshold: 4

Fatura Hesaplama
====================================

Bir elektronik çizelgede çözebileceğimiz soruları çözmek için **değişkenleri (variables)** kullanabiliriz. Ofis malzemeleri tedarik eden bir şirketin faturasını içeren bir elektronik tablonuz olduğunu düşünün. 

.. figure:: Figures/invoice.png
    :width: 600px
    :align: center
    :alt: a spreadsheet
    :figclass: align-center
    
    Figure 3: A spreadsheet with order information  

şte size, faturanın toplam fiyatını hesaplamak için bir program. Burada neler olduğunu anlamak için |audiobutton| (sesli tur) butonuna tıkladığınızdan emin olun. 

.. activecode:: Invoice1
    :tour_1: "Line by line tour"; 1: inv-line1; 2: inv-line2; 3: inv-line3; 4: inv-line4; 5: inv-line5; 6: inv-line6; 7: inv-line7; 8: inv-line8; 

    miktar1 = 2
    birimFiyati1 = 7.56
    toplam1 = miktar1 * birimFiyati1
    miktar2 = 4
    birimFiyati2 = 4.71
    toplam2 = miktar2 * birimFiyati2
    faturaToplam = toplam1 + toplam2
    print(faturaToplam)

.. mchoice:: 3_8_1_Invoice1_Q1
		   :answer_a: 7
		   :answer_b: 6
		   :answer_c: 5
		   :answer_d: 2
		   :correct: a
		   :feedback_a: Evet, miktar1, birimFiyat1, toplam1, miktar2, birimFiyat2, toplam2, faturaToplam 
		   :feedback_b: Yanlış. Her satır başına üç değişken olduğu baz alınarak; iki satır ve bir toplam vardır.
		   :feedback_c: Yanlış. Her satır başına üç değişken olduğu baz alınarak; iki satır ve bir toplam vardır.
		   :feedback_d: Yanlış. Her satır başına üç değişken olduğu baz alınarak; iki satır ve bir toplam vardır.

		   Bu programda kaç tane değişken vardır?

Aslında ``miktar2``  ve ``birimFiyat2``  adında yeni değişkenler oluşturmamız gerekmiyor. Dolayısıyla ilgili satırdaki toplamı hesaplamak için mevcut değişken (variable) isimlerini tekrar kullanabiliriz.

.. codelens:: Invoice2

  miktar = 2
  birimFiyati = 7.56
  toplam1 = miktar * birimFiyati
  miktar = 4
  birimFiyati = 4.71
  toplam2 = miktar * birimFiyati
  faturaToplam = toplam1 + toplam2
  print(faturaToplam)

.. mchoice:: 3_8_2_Invoice2_Q1
		   :answer_a: 7
		   :answer_b: 6
		   :answer_c: 5
		   :answer_d: 2
		   :correct: c
		   :feedback_a: Yanlış. Şimdi iki tane daha az değişkenimiz var. 
		   :feedback_b: Yanlış. Her satır için bir toplam (iki adet), bir miktar, bir birimFiyat ve bir de faturaToplam bulunmaktadır.
		   :feedback_c: Doğru. Değişkenler; miktar, birimFiyat, toplam1, toplam2 ve faturaToplam’dır.
		   :feedback_d: Yanlış. Her satır için bir toplam (iki adet), bir miktar, bir birimFiyat ve bir de faturaToplam bulunmaktadır. 

		   Bu programda kaç tane değişken vardır?
		   
.. Note::
    ``buDeğişkenBenimArkadaşım`` ve ``Fred`` gibi bir anlam ifade etmeyen isimler yerine; ``faturaToplam`` ve ``miktar`` gibi anlam taşıyan değişken isimleri kullanmak daha iyi bir yoldur. Değişken ismi, değişkenin neyi temsil ettiğini hatırlamanıza yardımcı olmalıdır. 


Elmaların tanesinin 0.40 TL olduğunu ve armutların tanesinin 0.65 TL olduğunu söyleyelim. Toplam maliyeti hesaplamak için aşağıdaki programı uygun şekilde değiştirin.

.. activecode:: Complete_Assignment

   elmalar = 4
   armutlar = 3
   toplamMaaliyet =
   print(toplamMaaliyett)

Aşağıdaki soruyu yanıtlamadan önce; yukarıdaki programa, soruda birbirini takiben verilen cevapları kopyalayıp yapıştırarak sorunun doğru cevabını bulmayı deneyebilirsiniz.

.. mchoice:: 3_8_3_Make_An_Assignment_Q1
  :answer_a: toplamMaaliyet = elmalar + armutlar
  :answer_b: toplamMaaliyet = (0.4 * elmalar) + (0.65 * armutlar)
  :answer_c: toplamMaaliyet = (0.4 * armutlar) + (0.65 * elmalar)
  :answer_d: toplamMaaliyet = (0.4 + elmalar) * (0.65 + armutlar)
  :correct: b
  :feedback_a: Yanlış. Bu elmaların veya armutların toplam maliyetini dikkate almaz.
  :feedback_b: Doğru. Elma başına düşen maliyet ile elma sayısını çarparak elde ettiğimiz değere, armut başına düşen maliyet ile armut sayısını çarparak elde ettiğimiz değeri eklemeliyiz.
  :feedback_c: Yanlış. Bu masrafları ters olarak alır.
  :feedback_d: Yanlış. Bu, toplamMaliyet’i hesaplamak için yanlış bir formüldür.

   Hangi kod satırı, yukarıdaki 3. satıra konulduğunda doğru ``toplamMaliyet``’i hesaplayacaktır?

.. tabbed:: 3_8_4_WSt

        .. tab:: Question

           Her bir ataş 0.05 TL ise ve cebinizde 4.00 TL varsa, kaç tane ataş satın alabileceğinizi hesaplayan ve ekrana bastıran kodu yazın. Ekrana 80 değerini basmalı.
           
           .. activecode::  3_8_4_WSq
               :nocodelens:

        .. tab:: Answer
        
            Değişkenleri tanımlayın, ve değişkenlere değerleri atayın. Sonuca ulaşmak için ``atasSayisi`` = ``butce / atasBirimFiyati`` formülünü kullanın. Sonucu ekrana yazdırdığınızdan emin olun.  
            
            .. activecode::  3_8_4_WSa
                :nocodelens:
                
                # DEĞİŞKENLERİ BİLDİRİN VE DEĞİŞKENLERE DEĞERLERİNİ ATAYIN
                atasBirimFiyatı = .05
                butce = 4.00
                # 2. FORMÜLÜ OLUŞTURUN 
                atasSayisi = butce / atasBirimFiyati 
                # 3. SONUCU EKRANA BASTIRIN
                print(atasSayisi)
                                
        
