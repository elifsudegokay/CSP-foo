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
	:prefix: csp-3-7-

.. highlight:: java
   :linenothreshold: 4

Daha Genel Olarak Ödev Üzerinden Gitmek
======================================================

Genel olarak ödevi inceleyelim.  Bu örneği takip etmeye çalışalım:

.. codelens:: Assign_Basic

   a = 1
   b = 12.3
   c = "Fred"
   d = b

.. mchoice:: 3_7_1_Assignment_Q1
   :answer_a: 1
   :answer_b: 12.3
   :answer_c: "b"
   :answer_d: "d"
   :correct: b
   :feedback_a: Yanlış.a değişkeni b değişkenini tanımlamada kullanılmıyor.
   :feedback_b: Doğru. d değişkeni b değişkenin değerinin kopyasına eşitlenir. b değişkeni de hala 12.3 değerini tutar. 
   :feedback_c: Yanlış.d değişkeni b değişkenine atanmış değerin aynısını içermektedir.
   :feedback_d: Yanlış.d değişkeni değerini b değişkeninden almaktadır.
   Bu program çalıştırıldığında  ``d`` değişkeninin değeri nedir?

Bir programdaki ifadelerin sırası çok önemlidir. Atama işlemi, isimler arası, matematikte olduğu gibi, bir ilişki oluşturmaz. ``a``  değişkeni, bir noktada ``12`` ve diğerinde ``15``'e eşit olabilir. Bir atama komutu, bir kez gerçekleşen ve sonra biten bir eylemdir.
   

.. codelens:: Assign_Multiple

	    degisken1 = 45
	    degisken1 = 17.3
	    degisken2 = degisken1

.. mchoice:: 3_7_2_Assignment_Multiple_Q1
		   :answer_a: degisken1'in değeri 45, degisken2'in değeri 45
		   :answer_b: degisken1'in değeri 45, degisken2'in değeri degisken1'in degerine eşit
		   :answer_c: degisken1'in değeri 17.3, degisken2'in değeri 45
		   :answer_d: degisken1'in değeri 17.3, degisken2'in değeri 17.3
		   :correct: d
		   :feedback_a: Yanlış. degisken1 degişkeni ilk olarak 45 değerini almıştı, 2. Satırda değeri değiştirldi, degisken2 değişkenine herhangi bir değer atanmamışken.
		   :feedback_b: Yanlış. İki değişkende nümerik değerler içermektedir, çünkü bu değikenler programdaki tek değişkenlerdir.
		   :feedback_c: Yanlış. degisken2 değişkeni bu programdan hiçibr zaman 45 değerini almamıştır.
		   :feedback_d: Doğru. degisken1 değişkeni ilk olarak 45' değerini alır ve daha sonra 17.3'e değiştirilir ve sonra degisken2, degisken1'in değerine eşitlenir.

		   Bu program çalıştıktan sonra ``degisken1`` ve ``degisken2`` değerlerini ne olur?

Değerleri ekranda yazdırarak görebiliriz( adlandırılımış değikenlerin değerleri dahil). Bu ,bir programda neler olduğunu görmek için yararlı bir yoldur. Bu örneği çalıştırmayı deneyerek bilgisayarın 3 haftadaki gün sayısını hesaplayalım:

.. activecode:: Assign_Days
   :tour_1: "Line by line tour"; 1: calcDays-line1; 2: calcDays-line2; 3: calcDays-line3; 4: calcDays-line4; 5: calcDays-line5; 6: calcDays-line6;

   gun_sayisi_haftada = 7
   print(gun_sayisi_haftada)
   gunSayisi = 7 * 3
   print(gunSayisi)
   gunSayisi2 = gun_sayisi_haftada * 3
   print(gunSayisi2)

.. mchoice:: 3_7_3_Assign_Days_Q1
		   :answer_a: 7, 7*3, gun_sayisi_haftada*3
		   :answer_b: gun_sayisi_haftada, gunSayisi, gunSayisi2
		   :answer_c: 7, 21, 21
		   :answer_d: 7, 21, 3
		   :correct: c
		   :feedback_a: Yanlış.Değerler aslında hesaplanacak ve sayılar basılacaktır.
		   :feedback_b: Yanlış.Değişken isimleri basılmayacaktır.
		   :feedback_c: Doğru. İlk olarak gun_sayisi_haftada(7), ikinci olarak gunSayisi(21), ve üçüncü olarak gunSayisi2(21) değişkenlerinin değerleri basılır.
		   :feedback_d: Yanlış. gun_sayisi_haftada değeri hesaplanacak ve atanacaktır.

		   Bu program çalıştırıldığında ekrana hangi üç değer basılacaktır?
   
.. parsonsprob:: 3_7_4_Per_Person_Cost

   Aşağıdaki program, bahşiş dahil bir akşam yemeği için kişi başı maliyeti belirlemelidir. Ama aşağıdaki kod blokları karışık şekilde verilmiştir. . Soldaki blokları sağa doğru doğru sırayla sürükleyip bırakın. Cevabınızı kontrol etmek için <i>Check Me</i> butonuna basınız.</p>
   -----
   bill = 89.23
   =====
   tip = bill * 0.20
   =====
   total = bill + tip
   =====
   numPeople = 3
   perPersonCost = total / numPeople
   =====
   print(perPersonCost)

.. tabbed:: 3_7_5_WSt

        .. tab:: Question

           Akşam yemeğinde 10 kişi restorana gitti. Her konuk 1 meze ve 1 ara sıcak yedik. Bütün parti 1 tatlıyı paylaştı. Her meze $ 2,00, her ara sıcak maliyeti 9,89 $ ve tatlı maliyeti 7,99 $ ise, toplam faturası hesaplamak ve yazdırmak için kodu yazın. Cevap olrak 126.89 yazmalıdır.
           
           .. activecode::  3_7_5_WSq
               :nocodelens:

        .. tab:: Answer
        
            Değişkenleri tanımla ve değişkenlere değerlerini ata. Faturayı  ``toplamFiyat``= ``mezeFiyat + arasicakFiyat + birimTatlı``olacak şekilde hesapla. Ekrana sonucu yazdırdığından emin ol.
            
            .. activecode::  3_7_5_WSa
                :nocodelens:
                
                # DEĞİŞKENLERİ TANIMLA VE DEĞERLERİNİ ATA
                birimMeze = 2.00
                birimAraSicak = 9.89
                birimTatli = 7.99
                # FATURAYI HESAPLAMAK İÇİN FORMÜL YARAT
                mezeFiyat = birimMeze * 10
                arasicakFiyat = birimAraSicak * 10
                toplamFiyat = mezeFiyat + arasicakFiyat + birimTatli
                # SONUCU YAZDIR
                print(toplamFiyat)
                                
        

