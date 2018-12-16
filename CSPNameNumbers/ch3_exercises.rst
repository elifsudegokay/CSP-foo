..  Copyright (C)  Brad Miller, David Ranum, Jeffrey Elkner, Peter Wentworth, Allen B. Downey, Chris
    Meyers, and Dario Mitchell.  Permission is granted to copy, distribute
    and/or modify this document under the terms of the GNU Free Documentation
    License, Version 1.3 or any later version published by the Free Software
    Foundation; with Invariant Sections being Forward, Prefaces, and
    Contributor List, no Front-Cover Texts, and no Back-Cover Texts.  A copy of
    the license is included in the section entitled "GNU Free Documentation
    License".


.. setup for automatic question numbering.

.. 	qnum::
	:start: 1
	:prefix: csp-3-12-

Ünite 3 - Değerlendirme Soruları
----------------------

#.

    .. tabbed:: ch3ex1t

        .. tab:: Question

            Bu ifadelerin her birinin ne yazdıracağını düşündüklerinizi yazın, 
	    ardından sonuçlarınızı kontrol etmek için aktif kod penceresini kullanın:
            

            #. ``9 * 5``
            #. ``2 / 5``
            #. ``5 % 2``
            #. ``9 % 5``
            #. ``6 % 6``
            #. ``2 % 7``
            #. ``3 / 0``

            .. activecode:: ch3ex1
                :nocodelens:

               print(9 * 5)

        

#.

    .. tabbed:: ch3ex2t

        .. tab:: Question

            Her bir satır için Doğru ``True`` ifadesi yazılacak şekilde, doğru işleçleri (operator) ``#`` yerine yerleştirin. ``==`` ifadesinin eşitliği kontrol ettiğini unutmayın.

            .. activecode:: ch3ex2q
                :nocodelens:

                print(16 # 7 == 2)
                print((7 # 2) # 10 == 35)
                print(2 # 4 == 0.5)
                print(5 # 2 # 3 == -1)
                print(3 # 2 # 1 == 7)

        

#.

    .. tabbed:: ch3ex3t

        .. tab:: Question


           Aşağıdaki kodun 4 yerine -6 yazdırması için ``x = 6 * 1 - 2`` ifadesine bir parantez grubu ekleyin.

           .. activecode::  ch3ex3q
               :nocodelens:

               x = 6 * 1 - 2
               print(x)

        

#.

    .. tabbed:: ch3ex4t

        .. tab:: Question


           Aşağıdaki kodun 29 yerine -4 yazdırması için ``x = 12 * 2 - 3 + 4 * 2`` ifadesine parantezler ekleyin.


           .. activecode::  ch3ex4q
               :nocodelens:

               x = 12 * 2 - 3 + 4 * 2
               print(x)

        

#.

    .. tabbed:: ch3ex5t

        .. tab:: Question

           Araba galon başına 26 mil ilerler ve bir galonluk gazın maliyeti 3.45 dolardır. 500 millik bir araba yolculuğunun maliyetini yazdırmak için aşağıdaki kod dizininde yer alan 3. ve 5. satırdaki kodları tamamlayın. Program 66.3461538462 değerini basmalıdır. 

           .. activecode::  ch3ex5q
               :nocodelens:

               mil = 500
               galonBasiMil = 26
               galonSayisi =
               galonBasiFiyat = 3.45
               toplam =
               print(toplam)

        

#.

    .. tabbed:: ch3ex6t

        .. tab:: Question

            Günlerin Pazar 1, Pazartesi 2, Salı 3, vb., olarak temsil edildiğini düşünün. Bugünün de Pazar olduğunu kabul edin. Bugünden itibaren 82 gün sonra hangi gün olacağını göstermek için aşağıdaki kod dizininde yer alan 4. satırdaki kodu (matematiksel bir ifade ile) tamamlayın. (program, Cuma gününü temsil eden 6 değerini basmalıdır)


            .. activecode:: ch3ex6q
                :nocodelens:

                bugun = 1
                gunSayisi = 82
                oGununSayisi = bugun + gunSayisi
                oGun = oGununSayisi ...
                print(oGun)



#.

    .. tabbed:: ch3ex7t

        .. tab:: Question

           Aracınızın galon başına 40 mil gittiğini ve bir galonluk gazın maliyetinin 3.65 dolar olduğunu kabul edin. 25 dolarlık bütçe ile aracınızı kaç mil boyunca sürebileceğinizi yazdırmak için aşağıdaki kod dizininde yer alan 4. ve 5. satırlardaki kodları tamamlayın. Program 273.97260274 değerini yazdırmalıdır.

           .. activecode::  ch3ex7q
               :nocodelens:

               butce = 25
               galonBasiMil = 40
               galonBasiUcret = 3.65
               galonSayisi =
               milSayisi =
               print(milSayisi)

        

#.

    .. tabbed:: ch3ex8t

        .. tab:: Question

            Sözdizimi (syntax) hatalarını düzeltin.


            .. activecode:: ch3ex8q
                :nocodelens:

                a Sayisi = 12
                3 = bSayisi
                a Sayisi * b Sayisi = cSayisi
                print(cSayisi)



#.

    .. tabbed:: ch3ex9t

        .. tab:: Question

           Bir mağazada ürün fiyatlarında % 40 oranında indirim yapılmaktadır. Aynı zamanda bu indirime ek olarak, elinizde o mağazada kullanabileceğiniz % 20 oranında bir indirim kuponunuz da bulunuyor. Bu durumlara uygun olacak şekilde, mağazadaki 68 TL fiyatlı satın almak istediğiniz ürünün son maliyetini yazdırmak için aşağıdaki kod dizininde yer alan 3. ve 7. satırladaki kodları tamamlayın. Program, 32.64 değerini yazdırmalıdır. 

           .. activecode::  ch3ex9q
                :nocodelens:

                fiyat = 68
                indirimOrani = 0.4
                satisAzalimi =
                satisFiyati = fiyat - satisAzalimi
                indirimOrani = 0.2
                kuponAzalimi = satisFiyati * indirimOrani
                kuponFiyati =
                print(kuponFiyati)



#.

    .. tabbed:: ch3ex10t

        .. tab:: Question

            Cevabın 3.5 yerine 1 olması için sözdizimi (syntax) hatalarını ve anlamsal (semantic) hataları düzeltin.

            .. activecode:: ch3ex10q
                :nocodelens:

                7 = a
                b = 2
                a / b = c
                print (c)

#.

    .. tabbed:: ch3ex11t

        .. tab:: Question

           Toplamda 5 kişisiniz ve her biriniz 4 TL harcayabiliyorsunuz. Birim fiyatı 0.50 TL olan kanatlardan satın almak istiyorsunuz. Kaç tane kanat satın alabileceğinizi yazdırmak için aşağıdaki kod dizininde yer alan 4. ve 5. satırlardaki kodları tamamlayın. Program, sonuç olarak 40.0 değerini yazdırmalıdır.

           .. activecode::  ch3ex11q
                :nocodelens:

                kisiSayisi = 5
                kisiBasiMiktar = 4
                fiyat = 0.5
                toplam =
                kanatSayisi =
                print(kanatSayisi)





#.

    .. tabbed:: ch3ex12t

        .. tab:: Question

           Şu an saatin 10:00 olduğunu varsayın. 123 saat sonra zamanın ne olacağını söyleyen aşağıdaki kodu tamamlayın. (24 saat dilimi yerine 12 saat dilimi geçerlidir)(Cevap 1 olmalıdır)

            .. activecode:: ch3ex12q
                :nocodelens:

                guncelSaat = 10
                yeniZaman = 10 + 123
                saatZamani =
                print(saatZamani)





#.

    .. tabbed:: ch3ex13t

        .. tab:: Question

          Bir buluşma için 270 dakika beklediğinizi varsayın. Toplamda kaç saat ve dakika beklediğinizi yazdırmak için aşağıdaki kod dizininde yer alan 2. ve 3. satırdaki kodları tamamlayın. Bir saatte 60 dakika olduğunu unutmayın. Program, 4.0 değerinden sonra 30 değerini de yazdırmalıdır.

           .. activecode::  ch3ex13q
                :nocodelens:

                toplamDakika = 270
                dakikaSayisi =
                saatSayisi =
                print(saatSayisi)
                print(dakikaSayisi)




#.

    .. tabbed:: ch3ex14t

        .. tab:: Question

            Market alışverişi yapıyorsunuz ve alt toplam tutarınız 73 TL tutuyor. Fakat bu tutara ek olarak % 7 oranında vergi ödemek zorundasınız. Toplam fiyatınızı bulmak için aşağıdaki kodu tamamlayın.  Toplam fiyatınız 78.11 değerinde olmalıdır. 


            .. activecode:: ch3ex14q
                :nocodelens:

                altToplam =
                vergi = 0.07
                toplam =
                print (toplam)







#.

    .. tabbed:: ch3ex15t

        .. tab:: Question

           Çalıştığınız iş yerinde bir saatte 8 TL kazandığınızı ve 100 TL kazanmak istediğinizi varsayın. Bu miktarı kazanmanız için çalışmanız gereken saat sayısını hesaplayan ve yazdıran aşağıdaki kod dizininin sözdizimi (syntax) hatalarını düzeltin. Program, işlemin sonunda 12.5 değerini yazdırmalıdır. 

           .. activecode::  ch3ex15q
                :nocodelens:

                8 = saatBasiUcret
                miktar = 100
                miktar / saatBasiUcret = saatSayisi
                print(saatSayisi)




#.

    .. tabbed:: ch3ex16t

        .. tab:: Question

            1.3 gün içinde kaç dakika ve kaç saniye olduğunu göstermek için aşağıdaki kodu tamamlayın. Program, işlemin sonunda 1872.0 ve 112320.0 değerlerini yazdırmalıdır.

            .. activecode:: ch3ex16q
                :nocodelens:

                toplamGun =
                saatSayisi = toplamGun * 24
                dakikaSayisi =
                saniyeSayisi =
                print(dakikaSayisi)
                print(saniyeSayisi)




#.

    .. tabbed:: ch3ex17t

        .. tab:: Question

           Elinizde toplam 8 TL var. Tanesi 1.2 TL olan armutlardan 3 tane satın almak istiyorsunuz. 	Geriye kalan paranızla da kaç tane elma satın alabileceğinizi hesaplamak için aşağıdaki kod 	dizininde yer alan 5. ve 6. satırlardaki kodları tamamlayın.  Program, 7.33333333333 değerini 	yazdırmalıdır. 7.333 tane elma satın alamayacağınız için, programın sadece 7 değerini 	yazdırmasını nasıl bir yolla sağlayabilirsiniz?

           .. activecode::  ch3ex17q
                :nocodelens:

                elmaBirimFiyati = 0.6
                armutSayisi = 3
                armutBirimFiyati = 1.2
                butce = 8
                armutlardanSonrakiButce =
                elmaSayisi =
                print(elmaSayisi)




#.

    .. tabbed:: ch3ex18t

        .. tab:: Question

            Bir araba 23 mpg (galon başı 23 mil – milepergallon) oranında yakıt tüketir. Birisi arabayı 15 galonluk yakıtla doldurur ve 112 mil hareket ettirir. Geriye kaç galonluk yakıt kaldığını belirlemek için aşağıdaki kodu doldurun. Cevap, 10.13043478260869 değeri olmalıdır.


            .. activecode:: ch3ex18q
                :nocodelens:

                yakitOrani = 23
                yakitMiktari = 15
                mesafe =
                tuketilenYakit =
                kalanYakit =
                print(kalanYakit)




#.

    .. tabbed:: ch3ex19t

        .. tab:: Question

           Arabanız 10 galonluk yakıt depo edebilmektedir ve galon başına 32 mil yol katedebilmektedir. Deponuzda ise geriye dörtte birlik yakıt kalmıştır.  Bu miktarda yakıtla kaç mil sürebileceğinizi hesaplamak ve yazdırmak için gereken kodu yazın. Programınız, 80 değerini yazdırmalıdır. 

           .. activecode::  ch3ex19q
               :nocodelens:


#.

    .. tabbed:: ch3ex20t

        .. tab:: Question

            Bir mermi 25 m/s hızla ilerliyor.  Kaç saniyelik sürede 111 m ileriye gideceğini belirleyen kodu yazın. (Programınız sonuç olarak 4.44 saniye değerini yazdırmalıdır)

            .. activecode::  ch3ex20q
                :nocodelens:

        .. tab:: Discussion

