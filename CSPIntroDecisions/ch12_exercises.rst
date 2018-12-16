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
	:prefix: 12-10-

Ünite 4 - Değerlendirme Soruları
---------------------

#.

    .. tabbed:: ch12ex1t

        .. tab:: Soru

            Aşağıda kod bloğunda bulunan 3 yazım hatasını düzeltin ve eğer x değişkeni 3 den küçük ise ekrana “x değişken değeri 3 den küçüktür” yazdırıp sonrasında yine ekrana “İşlem Tamamlandı :)” yazılmasını sağlayın.

            .. activecode:: ch12ex1q
                :nocodelens:

                x = 0
                if x < 3:
                print ("x değişken değeri 3 den küçüktür.")
                print ("İşlem tamamlandı")
        .. tab:: Cevap
            
          .. activecode::  ch12ex1a
              :nocodelens:
              
              x = 0
	      if x < 3:
              	print ("x değişken değeri 3 den küçüktür.")
              print ("İşlem tamamlandı")



#.

    .. tabbed:: ch12ex2t

        .. tab:: Soru

            Aşağıdaki kod bloğu x değişken değeri 3 den küçük ise ekrana “Merhaba” yazmaktadır. Bu kod bloğunu x değişken değeri 3 e eşit olduğunda ekrana “ Merhaba”  yazacak şekilde düzenleyiniz.

            .. activecode::  ch12ex2q
                :nocodelens:

                x = 3
                if x < 3:
                    print("Merhaba")

        .. tab:: Cevap
            
          .. activecode::  ch12ex2a
              :nocodelens:
              
              x = 3
              if x == 3:
              	print("Merhaba")

#.

    .. tabbed:: ch12ex3t

        .. tab:: Soru

           Aşağıdaki kod bloğunda agirlik 1 kg’ın altında ise fiyat=1.45, 1 kg’ın üzerinde ise fiyat=1.15 olabilmesi için gerekli girintili (indented) yazılması bölümleri ve yazım hatalarını düzeltin.  

           .. activecode::  ch12ex3q
                :nocodelens:

                agirlik = 0.5
                if agirlik < 1:
                fiyat = 1.45
                if agirlik >= 1
                fiyat = 1.15
                toplam = agirlik * fiyat
                print("ağırlık: ", agirlik)
                print("fiyat: ", fiyat)
                print("toplam: ", toplam)

        .. tab:: Cevap
            
          .. activecode::  ch12ex3a
              :nocodelens:
              
              agirlik = 0.5
              if agirlik < 1:
              	fiyat = 1.45
	      if agirlik >= 1:
              	fiyat = 1.15
              toplam = agirlik * fiyat
	      print("ağırlık: ", agirlik)
              print("fiyat: ", fiyat)
              print("toplam: ", toplam)

#.

    .. tabbed:: ch12ex4t

        .. tab:: Soru

            İlk Satırda bulunan agirlik değişken değerini toplam değişkeni 1'e eşit olacak şekilde düzenleyiniz ve girintili (indented) yazım hatalarını düzeltiniz.Fill in line 1 with a weight that will make the total equal 1, and fix the indentation errors.

            .. activecode::  ch12ex4q
                :nocodelens:

                agirlik =

                if agirlik >= .5:
                fiyat = 2
                if agirlik < .5:
                fiyat = 1
                    toplam = agirlik * fiyat
                    print("toplam: ", toplam)

        .. tab:: Cevap
            
          .. activecode::  ch12ex4a
              :nocodelens:
              
              agirlik = .5

              if agirlik >= .5:
                	fiyat = 2
              if agirlik < .5:
              	fiyat = 1
              toplam = agirlik * fiyat
              print("toplam: ", toplam)

#.

    .. tabbed:: ch12ex5t

        .. tab:: Soru

           Aşağıdaki kod bloğunda bulunan 3 hatayı ve girintili (indented) yazım hatasını agirlik 2 kg.dan küçükse fiyat 1.5 TL olacak şekilde düzeltiniz.

           .. activecode::  ch12ex5q
                :nocodelens:

                agirlik = 0.5
                adet = 5
                if agirlik < 2:
                fiyat = 1.50
                if agirlik >= 2:
                fiyat = 1.30
                toplam = agirlik * fiyat
                print(agirlik)
                    print("fiyat: ", fiyat)
                print(toplam)

        .. tab:: Cevap
            
          .. activecode::  ch12ex5a
              :nocodelens:
              
              agirlik = 0.5
              adet = 5
              if agirlik < 2:
              	fiyat = 1.50
              if agirlik >= 2:
              	fiyat = 1.30
              toplam = agirlik * fiyat
              print("agirlik: ", agirlik)
              print("fiyat: ", fiyat)
              print("toplam: ", toplam)

#.

    .. tabbed:: ch12ex6t

        .. tab:: Soru

            Ağaıdaki programda, sayı 2'ye eşitse, şu anda kod hiçbir şey yapmaz. Sayı 2 olduğunda ekranda “Selam” yazdıracak şekilde kodu onar:

            .. activecode::  ch12ex6q
                :nocodelens:

                x = 2
                if x < 2:
                    print("Merhaba")
                if x > 2:
                    print("Selam")

        .. tab:: Cevap
            
          .. activecode::  ch12ex6a
              :nocodelens:
              
              x = 2
              if x < 2:
               print("Merhaba")
              if x >= 2:
               print("Selam")
#.

    .. tabbed:: ch12ex7t

        .. tab:: Soru

           x’in 1'e eşit veya 1'den büyük ve x'in 10’a eşit veya 10'dan daha küçük olduğu durumda ekranda  “x 1'den 10'a bir sayıdır” yazdırmak için aşağıdaki kodda 4 hatayı düzeltin.

           .. activecode::  ch12ex7q
                :nocodelens:

                x = 3
                if x > 1 and x <= 10
                print ("x 1'den 10'a bir sayidir ")
                    print ("İşlem tamamlandı")

        .. tab:: Cevap
            
          .. activecode::  ch12ex7a
              :nocodelens:
              
              x = 3
              if x > 1 and x <= 10:
                print ("x 1'den 10'a bir sayidir ")
              print ("İşlem tamamlandı")

#.

    .. tabbed:: ch12ex8t

        .. tab:: Soru

            Aşağıdaki kod, sayı 8 değilse “Bu 8 değil” yazdırır. If deyiminde tek bir ifade olacak şekilde değişiklik yaparak aynı sonucu elde et.

            .. activecode::  ch12ex8q
                :nocodelens:

                x = 8
                if x < 8 or x > 8:
                    print("Bu 8 değil")
                else:
                    print("Bu 8")

        .. tab:: Cevap
            
          .. activecode::  ch12ex8a
              :nocodelens:
              
              x = 8
              if x != 8:
		print("Bu 8 değil")
	      else:
	       print("Bu 8")

#.

    .. tabbed:: ch12ex9t

        .. tab:: Soru

           3’üncü satırdaki durum ifadesini odaTemizlendi veya odevBitti ifadesinin herhangi biri doğruysa (0 değil 1) ekranda “Çıkabilirsin!” yazacak şekilde değiştir. Programda her zaman “İşlem tamamlandı” yazmalıdır.

           .. activecode::  ch12ex9q
                :nocodelens:

                odaTemizlendi = 1
                odevBitti = 0
                if
                    print ("Çıkabilirsin!")
                print ("İşlem tamamlandı")

        .. tab:: Cevap
            
          .. activecode::  ch12ex9a
              :nocodelens:
              
              odaTemizlendi = 1
              odevBitti = 0
              if odaTemizlendi or odevBitti:
              	print ("Çıkabilirsin!")
              print ("İşlem tamamlandı")

#.

    .. tabbed:: ch12ex10t

        .. tab:: Soru

            Koşulları tamamlayın ve hataları düzeltin, sayı 1 ile 10 (dahil) arasında ya da  15   olduğunda “İyi is” aksi takdirde “Basarisiz”  yazdıracak şekilde düzeltin.

            .. activecode::  ch12ex10q
                :nocodelens:

                x = 8
                    if
                print("Good job")

        .. tab:: Cevap
            
          .. activecode::  ch12ex10a
              :nocodelens:
              
              x = 8
              if (x > 0 and x <= 10) or x == 15:
                print("İyi iş")
	      else :
		print("Basarısız")

#.

    .. tabbed:: ch12ex11t

        .. tab:: Soru

           Aşağıdaki koddaki 5 hatayı, eğer agirlik 1’e küçük eşitse fiyatı 1.45 yapacak, değilse 1.15 yapacak şekilde düzeltin.

           .. activecode::  ch12ex11q
                :nocodelens:

                agirlik = 0.5
                if agirlik < 1:
                fiyat = 1.45
                if agirlik > 1:
                fiyat = 1.15
                toplam = agirlik * fiyat
                print("agirlik: ", agirlik)
                print("fiyat: ", fiyat)
                print("toplam: ", toplam)

        .. tab:: Cevap
            
          .. activecode::  ch12ex11a
              :nocodelens:
              
              agirlik = 0.5
              agirlik = 0.5
              if agirlik <= 1:
              	fiyat = 1.45
              if agirlik > 1:
              	fiyat = 1.15
              toplam = agirlik * fiyat
              print("agirlik: ", agirlik)
              print("fiyat: ", fiyat)
              print("toplam: ", toplam)

#.

    .. tabbed:: ch12ex12t

        .. tab:: Soru

            Aşağıdaki girintili yazma hatalarını düzelt, böylece kod fiyat değişkenini agirlik değişkene bağlı olarak değiştirsin. Sonrasında ise kod total değişkenindeki değer cüzdanındaki değerden büyük mü bunu kontrol etsin.

            .. activecode::  ch12ex12q
                :nocodelens:

                weight = 0.5
                numItems = 5
                wallet = 2

                if weight < 1:
                    price = 1.45
                    if weight >= 1:
                    price = 1.15
                    total = numItems * price
                    if total > wallet:
                    print("You have no money")

        .. tab:: Cevap
            
          .. activecode::  ch12ex12a
              :nocodelens:
              
              agirlik = 0.5
              if agirlik < 1:
              	fiyat = 1.45
	      if agirlik >= 1:
              	fiyat = 1.15
              toplam = agirlik * fiyat
	      print("ağırlık: ", agirlik)
              print("fiyat: ", fiyat)
              print("toplam: ", toplam)

#.

    .. tabbed:: ch12ex13t

        .. tab:: Soru

            Aşağıdaki kodda 3 satırı değiştirin böylece not değişkenini skor 90 ve üzeri ise A, 80-89 arasında ise B, 70-79 arasında ise C, 60-69 arasında ise D ve 60’dan aşağısı için E yapsın.

           .. activecode::  ch12ex13q
                :nocodelens:

                skor = 93
                if skor >= 90:
                    alinanNot = "A"
                if skor >= 80:
                    alinanNot = "B"
                if skor >= 70:
                    alinanNot = "C"
                if skor >= 60:
                    alinanNot = "D"
                if skor < 60:
                   alinanNot = "E"
                print("not: ", alinanNot)

        .. tab:: Cevap
            
          .. activecode::  ch12ex13a
              :nocodelens:
              
              skor = 93
              if skor >= 90:
                  alinanNot = "A"
              elif skor >= 80:
                  alinanNot = "B"
              elif skor >= 70:
                  alinanNot = "C"
              elif skor >= 60:
                  alinanNot = "D"
              elif skor < 60:
                 alinanNot = "E"
              print("not: ", alinanNot)

#.

    .. tabbed:: ch12ex14t

        .. tab:: Soru

            Aşağıdaki koddaki hataları düzelt ve gerekirse kodu değiştir böylece sadece 1 tane if deyimi (statement) olsun. Kod eğer x değeri 5 ise ekrana “x, 5’e eşittir” bassın. Diğer koşullarda ise“x, 5’e eşit değildir” bassın.

            .. activecode::  ch12ex14q
                :nocodelens:

                x = int( input("Bir sayi girin"))
                if x == 5:
                print("Girdiğiniz sayi 5'e eşit")
                if x != 5:
                print("Girdiğiniz sayi 5'ten farklı")


        .. tab:: Cevap
            
          .. activecode::  ch12ex14a
              :nocodelens:
              
              x = int( input("Bir sayi girin"))
              if x == 5:
               print("Girdiğiniz sayi 5'e eşit")
              else:
               print("Girdiğiniz sayi 5'ten farklı")

#.

    .. tabbed:: ch12ex15t

        .. tab:: Soru

           Aşağıdaki kodda var olan 5 hatayı düzeltin böylece eğer agirlik 1’in altında ise fiyat 1.45 olsun değilse 1.15 olsun. 

           .. activecode::  ch12ex15q
                :nocodelens:

                agirlik = 0.5
                if agirlik < 1
                fiyat = 1.45
                else
                fiyat = 1.15
                toplam = agirlik * fiyat
                print("ağırlık: ", agirlik)
                print("fiyat: ", fiyat)
                print("toplam: ", toplam)

        .. tab:: Cevap
            
          .. activecode::  ch12ex15a
              :nocodelens:
              
              agirlik = 0.5
              if agirlik < 1:
               fiyat = 1.45
              else:
               fiyat = 1.15
              toplam = agirlik * fiyat
              print("ağırlık: ", agirlik)
              print("fiyat: ", fiyat)
              print("toplam: ", toplam)

#.

    .. tabbed:: ch12ex16t

        .. tab:: Soru

            Aşağıdaki kod dizininin “Selam” yazdırması için kod dizininde bulunan 1. ve 4. satırlardaki kodu bitirin ve tamamlayın. 

            .. activecode::  ch12ex16q
                :nocodelens:

                x =
                if not x != 3:
                    print("Selam")

                    print("Merhaba")

        .. tab:: Cevap
            
          .. activecode::  ch12ex16a
              :nocodelens:
              
              x = int(input("bir değer giriniz: "))         # 3 değeri girilir
              if not x != 3:
              	print("Selam")
	      else: 		# veya if x != 3: ya da aynı formatta if not x == 3: yazılır.
              	 print("Merhaba")
              
#.

    .. tabbed:: ch12ex17t

        .. tab:: Soru

           Verilen değer çift ise “çift” ifadesini ve verilen değer tek ise “tek” ifadesini yazdıran bir yordam (procedure) yazın. Her iki olasılığı da test edin.

           .. activecode::  ch12ex17q
                :nocodelens:

        .. tab:: Cevap
            
          .. activecode::  ch12ex17a
              :nocodelens:
              
              x = int(input("bir değer giriniz: "))
              if x % 2 == 0:
              	print("çift")
	      else: 		# veya if x % 2 != 0: ya da if x % 2
              	print("tek")
              

#.

    .. tabbed:: ch12ex18t

        .. tab:: Soru

            2 tamsayı (integer), toplam fiyat ve cüzdandaki miktarı alan bir yordam (procedure) yazın. Program; cüzdandaki miktar ile toplam fiyat arasındaki fark 0 veya 0’dan büyük ise “Yeterli paranız var.” ifadesini, aksi durumu için “Daha fazla para kazan!” ifadesini yazdırsın.

            .. activecode::  ch12ex18q
                :nocodelens:

        .. tab:: Cevap
            
          .. activecode::  ch12ex18a
              :nocodelens:
              
              fiyat1 = int(input("ilk fiyatı giriniz: "))
              fiyat2 = int(input("ikinci fiyatı giriniz: "))
              cuzdandakiMiktar = int(input("mevcut paranızı giriniz: "))
	      toplamFiyat = fiyat1 + fiyat2
              if cuzdandakiMiktar - toplamFiyat == 0 or cuzdandakiMiktar - toplamFiyat > 0: 
              	print("Yeterli paranız var")
              else: 		# veya if cuzdandakiMiktar – toplamFiyat < 0: yazılır.
               print("Daha fazla para kazan!")
             

#.

    .. tabbed:: ch12ex19t

        .. tab:: Soru

           Not (grade) için değer alan ve bu değere göre bir dizi (string) notu döndüren bir işlev (function) yazın. Program; 60 ve 60’dan küçük herhangi bir değer için E notunu, 61’den 69’a kadar olan bir değer için D notunu, 70’den 79’a kadar olan bir değer için C notunu, 80’den 89’a kadar olan bir değer için B notunu, 90 ve üzeri bir değer için A notunu yazdırmalıdır. Her not aralığını test eden kodu yazın.

           .. activecode::  ch12ex19q
               :nocodelens:

        .. tab:: Cevap
            
          .. activecode::  ch12ex19a
              :nocodelens:
              
              notDegeri = int(input("Notu giriniz: "))
              if notDegeri >= 90:
              	harfNotu = "A"
	      if notDegeri >= 80 and notDegeri < 90:
              	harfNotu = "B"
              if notDegeri >= 70 and notDegeri < 80:
              	harfNotu = "C"
              if notDegeri >= 60 and notDegeri < 70:
              	harfNotu = "D"
              if notDegeri <= 60:
	       harfNotu = "E"
              print("HARF NOTU: ", harfNotu)
              

#.

    .. tabbed:: ch12ex20t

        .. tab:: Soru

            Girilen sayı 3’e bölünebilir olduğunda “Gerçekten” ifadesini, 5’e bölünebilir olduğunda “Evet” ifadesini ve hem 3’e hem de 5’e bölünebilir olduğunda “GerçektenEvet” ifadesini yazdıran bir kod yazın. (Program, eğer sayı hem 3’e hem de 5’e bölünebiliyor ise  “Gerçekten” ve “Evet” ifadelerini de yazdırmalıdır.)

            .. activecode::  ch12ex20q
                :nocodelens:


        .. tab:: Cevap
            
          .. activecode::  ch12ex20a
              :nocodelens:
              
              sayi = int(input("Bir sayı giriniz: "))
              dizi1 = "Gerçekten"
              dizi2 = "Evet"
	      if sayi % 3 == 0:
              	print(dizi1)   
              if sayi % 5 == 0:
	      	print(dizi2) 
              if sayi % 3 == 0 and sayi % 5 == 0:
                print(dizi1+dizi2)   
