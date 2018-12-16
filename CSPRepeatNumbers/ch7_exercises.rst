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
	:prefix: 7-8-

Ünite 5 ~ Değerlendirme Soruları
--------------------

#.

    .. tabbed:: ch7ex1t

        .. tab:: Soru

            1. ve 2. Satırdaki kodları 1 den 5 kadar sayıların toplamlarını yazacak şekilde düzenleyin.

            .. activecode:: ch7ex1q
                :nocodelens:

                toplam =
                sayiListesi =
                for sayi in sayiListesi:
    	            toplam = toplam + sayi
                print(toplam)

        .. tab:: Cevap

            .. activecode:: ch7ex1a
                :nocodelens:
                
                toplam = 0
                sayiListesi = range(1,6)
                for sayi in sayiListesi:
                   toplam = sayi + toplam
                print(toplam)
		    
#.

    .. tabbed:: ch7ex2t

        .. tab:: Soru

            Aşağıdaki kod bloğunu 1 den 10 a kadar bütün sayıların toplamını ekrana yazdıracak şekilde düzeltiniz.

            .. activecode::  ch7ex2q
                :nocodelens:

                toplam = 0
                sayiListesi = range(1,10)
                for sayi in sayiListesi:
                    toplam = sayi
                print(toplam)

        .. tab:: Cevap

            .. activecode:: ch7ex2a
                :nocodelens:

                toplam = 0
		sayiListesi = range(1,10)
		for sayi in sayiListesi:
		    toplam = toplam + sayi
		print(toplam)
#.

    .. tabbed:: ch7ex3t

        .. tab:: Soru

           Aşağıdaki kod bloğunu sayiListesi değişkeninde bulunan değerlerden en küçük değeri yazdıracak şekilde düzenleyiniz.

           .. activecode::  ch7ex3q
                :nocodelens:

                enkucuk = 0  # Start out with nothing
                sayiListesi = [56, 2, 88, 34, 90, 32, 35, 61]
                for sayi in sayiListesi:
                print(enkucuk)


        .. tab:: Cevap

            .. activecode:: ch7ex3a
                :nocodelens:
                
		sayiListesi = [56, 2, 88, 34, 90, 32, 35, 61]
		enkucuk = sayiListesi[0]
		for sayi in sayiListesi:
		    if (enkucuk > sayi):
		        enkucuk = sayi
		print("Listedeki en kucuk sayi: ", enkucuk)
#.

    .. tabbed:: ch7ex4t

        .. tab:: Soru

            Aşağıdaki kod bloğunu 5 – 25 arasındaki (5 ve 25 dahil) sayıları 5 er 5 er sıralayıp her sayıyı sonuc değişkenine ekleyerek ekrana yazdıracak şekilde düzenleyiniz.

            .. activecode::  ch7ex4q
                :nocodelens:

                sonuc = 0
                sayilar = len(4,25,5)
                for sayi in sayilar:
                	sonuc = sonuc + sayi
                print("Sonuc: ", sonuc)

        .. tab:: Cevap

            .. activecode:: ch7ex4a
                :nocodelens:
                
		sonuc = 0
		sayilar = range(5, 30, 5)
		for sayi in sayilar:
		    sonuc = sonuc + sayi
		print("Sonuc: ", sonuc)
#.

    .. tabbed:: ch7ex5t

        .. tab:: Soru

           Aşağıdaki kod bloğunu urun değişkinin değerini sayiListesi değişkenindeki sayıların adedi kadar çarpıp son değerini ekrana yazacak şekilde düzetiniz.

           .. activecode::  ch7ex5q
                :nocodelens:

                sonuc = 1 
                sayiListesi = [1,2,3,4,5]
                for in sayilar:
    	            sonuc = sonuc *


        .. tab:: Cevap

            .. activecode:: ch7ex5a
                :nocodelens:
		
		sonuc = 1  # Start out with nothing
		sayiListesi = [1,2,3,4,5]
		for sayi in sayiListesi:
		    sonuc = sonuc * sayi
		print(sonuc)
    

#.

    .. tabbed:: ch7ex6t

        .. tab:: Soru

            Koddaki hataları düzeltin, böylece 1 ile 20 arasındaki tüm tek sayıların toplamını yazdırın.

            .. activecode::  ch7ex6q
                :nocodelens:

                toplam = 1
                sayilar = range(1,21,1)
                for sayilar in sayi:
                toplam = toplam + sayi
                print(toplam)

        .. tab:: Cevap

            .. activecode:: ch7ex6a
                :nocodelens:
                
		toplam = 0
		sayilar = range(1, 21, 2)
		for sayi in sayilar:
		    toplam = toplam + sayi
		print(toplam)
		
#.

    .. tabbed:: ch7ex7t

        .. tab:: Soru

           Aşağıdaki kodu listedeki çift sayiların çarpımını bulacak şekilde düzeltin:

           .. activecode::  ch7ex7q
                :nocodelens:

                carpim = 1  # 1 degeri ile basla
                sayilar = [1,2,3,4,5]
                for sayi in sayilar:
    	            carpim = carpim * sayi
                print(carpim)

        .. tab:: Cevap

            .. activecode:: ch7ex7a
                :nocodelens:
                
		carpim = 1  # 1 degeri ile basla
		sayilar = [1,2,3,4,5]
		for sayi in sayilar:
		    if sayi % 2 == 0:
		        carpim = carpim * sayi
		print(carpim)

#.

    .. tabbed:: ch7ex8t

        .. tab:: Soru

            Koddaki hatayı düzeltin, böylece listedeki her kelimeyi alın ve “Pizza yemeyi severim” cümlesi yazdırın.

            .. activecode::  ch7ex8q
                :nocodelens:

                cumle = ""
                kListe = ["Pizza", "yemeyi", "severim"]
                for kelime in kListe:
                	cumle=kelimea
                	print(cumle)

        .. tab:: Cevap

            .. activecode:: ch7ex8a
                :nocodelens:
                
		cumle = ""
		kListe = ["Pizza", "yemeyi", "severim"]
		for kelime in kListe:
		    cumle = cumle + " " + kelime
		print(cumle)

#.

    .. tabbed:: ch7ex9t

        .. tab:: Soru

           0 ile 10 (dahil) arasında tüm çift sayıların doğru bir şekilde toplanması ve basılması için 2., 4. ve 6. satırlarda aşağıdaki kodu doldurun.

           .. activecode::  ch7ex9q
                :nocodelens:

                # ADIM 1: BIRIKTIRICIYI BASLAT
                toplam =   # hicbir sey ile baslat

                 # ADIM 2: VERI AL
                sayilar = range()

                # ADIM 3: VERI UZERINDEN DONGU KUR
                for sayi in sayilar:
    	            # ADIM 4: BIRIKTIR
    	          toplam = toplam +
                # ADIM 5: SONUCU ISLE
                print(sum)

        .. tab:: Cevap

            .. activecode:: ch7ex9a
                :nocodelens:
                
		# ADIM 1: BIRIKTIRICIYI BASLAT
		toplam = 0  # hicbir sey ile baslat

		# ADIM 2: VERI AL
		sayilar = range(0,11,2)

		# ADIM 3: VERI UZERINDEN DONGU KUR
		for sayi in sayilar:
		    # STEP 4: BIRIKTIR
		    toplam = toplam + sayi
		# STEP 5: SONUCU ISLE
		print(toplam)

#.

    .. tabbed:: ch7ex10t

        .. tab:: Soru

            1'den 10'a kadar her sayının karesini “1 * 1 = 1” biçiminde yazdıran kod yazın. 

            .. activecode::  ch7ex10q
                :nocodelens:

        .. tab:: Cevap

            .. activecode:: ch7ex10a
                :nocodelens:
                
		Sayilar = range(1,11)
		for sayi in Sayilar:
		    sayiKare = sayi * sayi
		    print(sayi, "*", sayi, "=", sayiKare)

#. 

    .. tabbed:: ch7ex11t

        .. tab:: Soru

           Aşağıda verilen kodu başlangıç ve bitiş(bdahil) değerleri kullanıcıdan okunacak şekle haliyle, bu değerler arasındaki çift sayiların toplamını ekrana bastıracak hale getirin. 

           .. activecode::  ch7ex11q
                :nocodelens:

                # ADIM 1: BIRIKTIRICIYI BASLAT
                toplam = 0  # hicbir sey ile baslat
		baslangic =
		bitis =

                # ADIM 2: VERI AL
                sayilar = range(0,21,2)

                # ADIM 3: VERI UZERINDEN DONGU KUR
                for sayi in sayilar:
    	            # ADIM 4: BIRIKTIR
    	           toplam = toplam +
                # ADIM 5: SONUCU ISLE
                print(toplam)

        .. tab:: Cevap

            .. activecode:: ch7ex11a
                :nocodelens:
                
		# ADIM 1: BIRIKTIRICIYI BASLAT
		toplam = 0  # hicbir sey ile baslat
		baslangic = int (input("Baslangic: "))
		bitis = int (input("Bitis "))

		if baslangic %2 == 1:
		   baslangic = baslangic + 1

		sayilar = range(baslangic, bitis + 1, 2)

		
		for sayi in sayilar:
		    toplam = toplam + sayi
		# ADIM 5: SONUCU ISLE
		print(toplam)
		
#.

    .. tabbed:: ch7ex12t

        .. tab:: Soru

            Kullanıcı tarafından verilen fonksiyonun faktoriyelini hesaplayan bir kod yazınız.

            .. activecode::  ch7ex12q
                :nocodelens:

        .. tab:: Cevap

            .. activecode:: ch7ex12a
                :nocodelens:
                
		faktoriyel = 1
		sayi = int (input("Hangi sayinin faktoriyelini hesaplamak istersiniz? "))
		aralik = range (1, sayi + 1)
		for sayi1 in aralik:
		    faktoriyel = faktoriyel * sayi1 
		print(sayi, "! = ", faktoriyel)

#.

    .. tabbed:: ch7ex13t

        .. tab:: Soru

           10 ile 20 arasındaki çift sayıların çarpımını hesaplayıp, yazdıracak şekilde verilen kodu düzeltiniz.

           .. activecode::  ch7ex13q
                :nocodelens:

                # ADIM 1: BIRIKTIRICIYI BASLAT
                carpim = 0  # carpimi baslat

                # ADIM 2:  VERIYI AL
                sayilar = range(10,20,2)

                # STEP 3:VERI UZERINDEN DONGU KUR
                for sayi in sayilar:
    	            #  ADIM 4: BIRIKTIR
    	           carpim = carpim + sayi

                # ADIM 5: SONUCU ISLE
                print(carpim)

        .. tab:: Cevap

            .. activecode:: ch7ex13a
                :nocodelens:
                
		# ADIM 1: BIRIKTIRICIYI BASLAT
		carpim = 1  # carpimi baslat

		# ADIM 2:  VERIYI AL
		sayilar = range(10,20,2)
		
		# ADIM 3:VERI UZERINDEN DONGU KUR
		for sayi in sayilar:
		    #  ADIM 4: BIRIKTIR
		    carpim = carpim * sayi
		# ADIM 5: SONUCU ISLE
		print(carpim)

#.

    .. tabbed:: ch7ex14t

        .. tab:: Soru

            1 ile 20 arasındaki tüm tek sayıların bir listesini oluşturun ve bu sayıların ortalamasını bulun. Ardından, ortalama sayısını artış olarak kullanarak 1 ile 100 arasında bir sayı listesi oluşturun ve bu sayıların carpımını yazdırın.

            .. activecode::  ch7ex14q
                :nocodelens:

        .. tab:: Cevap

            .. activecode:: ch7ex14a
                :nocodelens:
                
		sayilar = range( 1, 21, 2)
		toplam = 0
		adet = 0
		for sayi in sayilar:
		    toplam = toplam + sayi
		    adet = adet + 1
		ortalama = int ((toplam / adet))
		print("Ortalama : ", ortalama)
		liste2 = range(1, 101, ortalama)
		carpim = 1
		for sayi in liste2:
		    carpim = carpim * sayi2
		print("Carpimlari: ", carpim)
		

#.

    .. tabbed:: ch7ex15t

        .. tab:: Soru

           1 ile son kullanıcıdan okunan bir sayi(dahil) arasındaki tek sayıların toplamını hesaplamak ve döndürmek için bir kod oluşturun.

           .. activecode::  ch7ex15q
                :nocodelens:

        .. tab:: Cevap

            .. activecode:: ch7ex15a
                :nocodelens:
                
		toplam = 0
		bitis = int (input("Bir sayi giriniz: "))
		sayilar = range(1, bitis, 2)
		for sayi in sayilar:
			toplam = toplam + sayi
		print("Toplam: ", toplam)
		
		

#.

    .. tabbed:: ch7ex16t

        .. tab:: Soru

            Pozitif sayılardan oluşan aşağıda yer alan listedeki maximum sayıyı bulan kodu yazın..

            .. activecode::  ch7ex16q
                :nocodelens:

                liste = [3, 7, 1, 33, 15, 27]

        .. tab:: Cevap

            .. activecode:: ch7ex16a
                :nocodelens:
                
		liste = [3, 7, 1, 33, 15, 27]
		max = -1
		for sayi in liste:
			if sayi > max:
				max = sayi
		print("Listedeki en buyuk sayi: ", max)

#.

    .. tabbed:: ch7ex17t

        .. tab:: Soru

           Kullanıcıdan bir sayı alın. 2’den, girilen sayıya kadar (girilen sayı dahil) olan çift sayıların çarpımını hesaplayan bir program yaz. Sonucu bastırmayı unutma.

           .. activecode::  ch7ex17q
                :nocodelens:

        .. tab:: Cevap

            .. activecode:: ch7ex17a
                :nocodelens:
                
		ustDeger = int(input("ust degeri giriniz:"))
		sonuc = 1
		for sayi in range(2, ustDeger + 1, 2) :
		    sonuc = sonuc * sayi
		print(sonuc)

#.

    .. tabbed:: ch7ex18t

        .. tab:: Soru

            Normalizasyon işlemi birçok istatistik işleminde kullanılır. Bu işlem belirli bir aralıkta verilen sayıları 0 ve 1 arasında değerlere eşleştirmek ya da kaydırmak için kullanılır. Eğer aralık alt değeri min, üst değer max ile temsil edilirse, bir değerin normalize karşılığı  normalizeDeğer = (değer - min) / (max - min) formülü ile hesaplanır. Örneğin elimizdeki değerler [3,4,5] ise bunlara karşılık gelen normalize değerler 0, 0.5 ve 1 olacaktır. Bu verilen örnekte min 3, max ise 5’dir. Bu formüle göre 4 için normalize Değer = (4 - 3) / (5-3) yani 0.5 olacaktır. Verilen formülü kullanarak normalizasyon yapan programı yazınız.


            .. activecode::  ch7ex18q
                :nocodelens:

        .. tab:: Cevap

            .. activecode:: ch7ex18a
                :nocodelens:
                
		min = 3
		max = 5
		aList = range( min, max + 1)
		print(aList)
		for i in aList:
			print((i - min) / (max - min))
		
		

#.

    .. tabbed:: ch7ex19t

        .. tab:: Soru

           Alt değeri ve üst değeri kullanıcıdan aldığın bir program yaz. Bu program, alt ve üst değer arasındaki 3 ile bölünüp 5’e bölünemeyen sayıları ekrana bastırsın.

           .. activecode::  ch7ex19q
               :nocodelens:

        .. tab:: Cevap

            .. activecode:: ch7ex19a
                :nocodelens:
                
		altDeger = int (input("Alt degeri giriniz: "))
		ustDeger = int (input("Ust degeri giriniz: "))
		
		print("Belirlenen aralikta kritere uyan sayilar: ")
		for sayi in range(altDeger, ustDeger):
			if sayi % 3 == 0 and sayi % 5 != 0:
				print(sayi)
		

#.

    .. tabbed:: ch7ex20t

        .. tab:: Soru

            Kullanıcıdan bir “n” değeri alın ve 0’dan n’e kadar olan sayının karesinden kendisini çıkarın. Ve bu sayıların toplamını ekrana bastırın

            .. activecode::  ch7ex20q
                :nocodelens:

    	.. tab:: Cevap

            .. activecode:: ch7ex20a
                :nocodelens:
                
		n = int(input(" n degerini giriniz: "))
		
		sonuc = 0
		for sayi in range(n + 1):
			sonuc = sonuc + (sayi * sayi - sayi )
		print("Sonuc: " , sonuc)
