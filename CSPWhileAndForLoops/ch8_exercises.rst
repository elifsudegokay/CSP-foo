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
	:prefix: 8-8-

Ünite 6 - Değerlendirme Soruları
--------------------

#.

    .. tabbed:: ch8ex1t

        .. tab:: Soru

            Aşağıdaki koddaki 5 yazım hatasını düzeltiniz. Böylece kod ekrana 10’dan 0’akadar sayıları basacaktır.

            .. activecode:: ch8ex1q
                :nocodelens:

                sayac = 10
                while Sayac > 0:
                    Print(sayac)
                    sayac =Sayac +1

        .. tab:: Cevap

            .. activecode:: ch8ex1a
                :nocodelens:

		sayac = 10
		while sayac > 0:
		    print(sayac)
		    sayac = sayac -1	


#.

    .. tabbed:: ch8ex2t

        .. tab:: Soru

            Aşağıdaki kod sonsuz döngüdedir. Tek bir değişiklikle döngüyü sadece 5 kez dönecek hale getirin.

            .. activecode::  ch8ex2q
                :nocodelens:

                x = 5
                while x > 0:
                    print(x)
                    x = x + 1

        .. tab:: Cevap

            .. activecode:: ch8ex2a
                :nocodelens:
		x = 5
		while x > 0:
		    print(x)
		    x = x - 1

#.

    .. tabbed:: ch8ex3t

        .. tab:: Soru

           Aşağıda for döngüsü ile oluşturulmuş kodu while döngüsü ile çalışacak hale dönüştürün.

           .. activecode::  ch8ex3q
                :nocodelens:

                carpim = 1
                sayiListesi = range(10,21,2)
                for sayi in sayiListesi:
                    carpim = carpim * sayi
                print("çarpım: ", carpim)
               


        .. tab:: Cevap

            .. activecode:: ch8ex3a
                :nocodelens:

		carpim = 1 
		sayi = 10
		while sayi < 21:
		    carpim = carpim * sayi
		    sayi = sayi + 2
		print("çarpım: ", carpim)

#.

    .. tabbed:: ch8ex4t


        .. tab:: Soru

            Aşağıdaki kod döngüye girip sürekli “çift” yazıyor. Kodu düzeltin böylece ekrana 0’dan 9’a kadar sayılar için çift veya tek yazsın. 

            .. activecode::  ch8ex4q
                :nocodelens:

                sayi = 0
                while sayi < 10:
                while sayi % 2 == 0:
                    print("Çift")
                while sayi % 2 != 0:
		    print("Tek")
		sayi += 1


        .. tab:: Cevap

            .. activecode:: ch8ex4a
                :nocodelens:

		sayi = 0
		while sayi < 10:
		    if sayi % 2 == 0:
		        print("Çift")
		    if sayi % 2 != 0:
			print("Tek")
		    sayi += 1

#.

    .. tabbed:: ch8ex5t

        .. tab:: Soru

           Aşağıdaki kodda eksik kalan yerleri tamamlayın böylece ekrana -5 ile -1 arasındaki sayıları basın.

           .. activecode::  ch8ex5q
                :nocodelens:

                cikti =
                x = -5
                while x < 0:
                    cikti = cikti + str(x) + " "
                    x =
                print(cikti)


        .. tab:: Cevap

            .. activecode:: ch8ex5a
                :nocodelens:

		cikti = ""
		x = -5
		while x < 0:
		    cikti = cikti + str(x) + " "
		    x = x + 1
		    print(cikti)
#.

    .. tabbed:: ch8ex6t

        .. tab:: Soru

            Kullanıcıdan iki sayı alın, ilk sayının ikinci sayıdan büyük olduğunu varsayıp, ilk sayının ikinci sayıya bölümünden kalanı bulan program yazın. Bu programı mod işlecini kullanmadan yazın.


            .. activecode::  ch8ex6q
                :nocodelens:

                
                
                
                   
                    
                

        .. tab:: Cevap

            .. activecode:: ch8ex6a
                :nocodelens:

		x = int(input("Büyük sayıyı giriniz"))
		y = int(input("küçük sayıyı giriniz"))

		deger = 0
		while deger < x:
		    deger = deger + y
		print("kalan: ", deger - x)

#.

    .. tabbed:: ch8ex7t

        .. tab:: Soru

           While döngüsünü kullanarak kullanıcının girdiği değerin asal sayı olup olmadığını anlayan bir program yazın.

           .. activecode::  ch8ex7q
                :nocodelens:

                
                  

        .. tab:: Cevap

            .. activecode:: ch8ex7a
                :nocodelens:

		sayi = int(input("limit?"))
		bolen = 2
		sonuc = "asal"
		while bolen != sayi:
		    if sayi % bolen == 0:
			sonuc = "asal değil"
		    bolen = bolen + 1
		print("sonuç: ", sonuc)

#.

    .. tabbed:: ch8ex8t

        .. tab:: Soru

            Kullanıcı “exit” yazana kadar kullanıcıdan sürekli kelime alın ve kelimeleri birleştirerek ekrana yazın.

            .. activecode::  ch8ex8q
                :nocodelens:

               


        .. tab:: Cevap

            .. activecode:: ch8ex8a
                :nocodelens:

		girdi = input("kelime giriniz")
		sonuc = ""
		while girdi != "exit":
		    sonuc = sonuc + girdi
		    girdi = input("kelime giriniz")
		print(sonuc)

#.

    .. tabbed:: ch8ex9t

        .. tab:: Soru

           Aşağıdaki kod kullanıcı “exit” yazana kadar sürekli kelime almak ve aldığı kelimelerin arasına “+” sembolü koyarak birleştirerek ekrana bastırmak için yazılmıştır. Örneğin ilk kelime ali, ikinci kelime ata, üçüncü kelime bak ise ekranda “ali+ata+bak“ yazmalıdır. Ancak koddaki bir eksiklikten dolayı ekranda “ali+ata+bak+exit” yazmaktadır. Sizce sorunu nasıl çözmeliyiz?

           .. activecode::  ch8ex9q
                :nocodelens:

                girdi = input("kelime giriniz"):
                sonuc = girdi
                while girdi != "exit":
		    girdi = input("kelime giriniz")
		    sonuc = sonuc + "+" + girdi
		print("sonuc: ", sonuc)

        .. tab:: Cevap

            .. activecode:: ch8ex9a
                :nocodelens:
		
		girdi = input("kelime giriniz")
		sonuc = girdi
		while girdi != "exit":
		    girdi = input("kelime giriniz")
		    if girdi !="exit":
			sonuc = sonuc + "+" + girdi
		print("sonuç: ", sonuc)

#.

    .. tabbed:: ch8ex10t

        .. tab:: Soru

           Kullanıcı negatif değer girene kadar kullanıcıdan değer alın ve girilen sayıların arasından maksimumu bulun

            .. activecode::  ch8ex10q
                :nocodelens:

                


        .. tab:: Cevap

            .. activecode:: ch8ex10a
                :nocodelens:

		x = int(input("bir değer girin?"))
		max = -1

		while x > 0:
		    if x > max:
			max = x
		    x = int(input("bir değer girin?"))
		print("max: ")
		print(max)

#.

    .. tabbed:: ch8ex11t

        .. tab:: Soru

           Kullanıcı negatif değer girene kadar kullanıcıdan değer alın ve kaç çift sayı kaç tek sayı girildi bunu bastırın.

           .. activecode::  ch8ex11q
                :nocodelens:

               

        .. tab:: Cevap

            .. activecode:: ch8ex11a
                :nocodelens:


		x = int(input("bir değer girin?"))
		cift = 0
		tek = 0
		while x > 0:
		    if x % 2 == 0:
			cift = cift + 1
		    else:
			tek = tek + 1
		    x = int(input("bir değer girin?"))
		print("cift: ")
		print(cift)
		print("tek: ")
		print(tek)

#.

    .. tabbed:: ch8ex12t

        .. tab:: Soru

            Kullanıcıdan, kullanıcının girdiği değerlerin toplamı 100 olana kadar sürekli sayı alın ve kaç tane sayı girildiğini bastırın.

            .. activecode::  ch8ex12q
                :nocodelens:

               


        .. tab:: Cevap

            .. activecode:: ch8ex12a
                :nocodelens:

		x = int(input("value?"))
                toplam = x
                sayac = 1
                while toplam != 100: 
                    x = int(input("value?"))
                    toplam = toplam + x
		    sayac = sayac + 1
                print("sayaç: ", sayac)

#.

    .. tabbed:: ch8ex13t

        .. tab:: Soru

           Fibonacci sayı dizisini hesaplayan bir program yazınız. Kaçıncı fibonacci sayısını istediğinizi kullanıcıdan isteyip sonucu ekrana bastırınız. 

           .. activecode::  ch8ex13q
                :nocodelens:

               

        .. tab:: Cevap

            .. activecode:: ch8ex13a
                :nocodelens:

		n = int(input("kaçıncı fibonacci sayısını istiyorsunuz?"))
		first = 0
		second = 1
		sayac = 0
		while sayac != n:
		    sonuc = first + second
		    first = second 
		    second = sonuc
		    sayac = sayac +1
		print(sonuc)

#.

    .. tabbed:: ch8ex14t

        .. tab:: Soru

 	        Yıldızlarla içi dolu bir dik üçgen yapan programı yazınız. Üçgenin ilk satırı 1 yıldızla başlasın ve her bir satırda yıldız sayısı bir artsın. Üçgenin kaç satırdan oluşacağını kullanıcıdan al. Örneğin kullanıcı 4 girerse programın çıktısı aşağıdaki gibi olmalıdır.

		.. figure:: Figures/yildizz.jpg
  	 	 :align: center	

            .. activecode::  ch8ex14q
                :nocodelens:

			

        .. tab:: Cevap

            .. activecode:: ch8ex14a
                :nocodelens:

		x = int(input("limit?"))
		son = 2
		for x in range(1, x+1):
		    for y in range(1, son):
			print("*",end='')
		    son = son + 1
		    print() 	
	  





		
 


#.

    .. tabbed:: ch8ex15t

        .. tab:: Soru

          Yukarıda verilen soruda verilen üçgenin aynısını oluşturun. Sadece bu sefer yıldızlar yerine ardışık sayıları kullan ve her satır 1 ile başlasın. Örneğin kullanıcı 4 girdiyse ekranda şu gözükmesi lazım: 

		.. figure:: Figures/ardisik.jpg
  	 	 :align: center	

           .. activecode::  ch8ex15q
                :nocodelens:

                


        .. tab:: Cevap

            .. activecode:: ch8ex15a
                :nocodelens:

		x = int(input("limit?"))
		son = 2
		for x in range(1,x+1):
		    for y in range(1, son):
			print(y,end='')
		    son = son + 1
		    print()

#.

    .. tabbed:: ch8ex16t

        .. tab:: Soru

            Kullanıcıdan bir değer alın ve alınan değere göre aşağıdaki şekli bastıracak kodu yazın. Aşağıdaki örnek kullanıcının 4 girmesi durumunda ekranda gözükecektir.

		.. figure:: Figures/q16.jpg
  	 	 :align: center	

            .. activecode::  ch8ex16q
                :nocodelens:

                


        .. tab:: Cevap

            .. activecode:: ch8ex16a
                :nocodelens:

		son = int(input("limit?"))
		for x in range(0, son +1):
		    bas = son - x
		    while bas > 0:
			print(str(bas)+" ",end='')
			bas = bas -1
		    print()



#.

    .. tabbed:: ch8ex17t

        .. tab:: Soru

           Kullanıcıdan bir değer alın ve alınan değere göre aşağıdaki çıktıyı bastıracak kodu yazın. Aşağıdaki örnek kullanıcının 5 girmesi durumunda ekranda gözükecektir.

		.. figure:: Figures/q17.jpg
  	 	 :align: center	

           .. activecode::  ch8ex17q
                :nocodelens:

        .. tab:: Cevap

            .. activecode:: ch8ex17a
                :nocodelens:

		limit1 = int(input("limit?"))
		limit2 = limit1
		for x in range(1,limit1+1):
		    deger=1
		    for y in range(0,limit2):
			print(str(deger)+" ",end='')
			deger = deger+ x
		    print()
		    limit2 = limit2 - 1
			
		

#.

    .. tabbed:: ch8ex18t

        .. tab:: Soru

           Kullanıcıdan bir tek sayı  alın ve girilen değere göre yıldızlarla aşağıdaki gibi bir üçgen bastırın. İlk satırda yıldız sayısı kullanıcının girdiği değere eşittir.

		.. figure:: Figures/q18.jpg
  	 	 :align: center	

            .. activecode::  ch8ex18q
                :nocodelens:


        .. tab:: Cevap

            .. activecode:: ch8ex18a
                :nocodelens:

		limit = int(input("limit?"))
		bosluk = 0
		yildiz = limit
		for i in range(limit):
		    for x in range(bosluk):
			print(" ",end='')
		    for x in range(yildiz):
			print("*",end='')
		    for x in range(bosluk):
			print(" ",end='')
		    yildiz = yildiz - 2
		    bosluk = bosluk + 1
		    print()
		
	
		

#.

    .. tabbed:: ch8ex19t

        .. tab:: Soru

           Kullanıcının verilen bir listedeki her hangi bir meyveyi kaç seferde tahmin edeceğini bulan bir program yazınız. Program bir liste ile başlar. Kullanıcıdan listedeki meyvelerden birini tahmin etmesi istenir, listedeki meyvelerden birini tahmin edene kadar bu işlem devam eder ve doğru cevap bulunduğunda kaç seferde tahmin ettiğini ekrana bastırır.


           .. activecode::  ch8ex19q
               :nocodelens:

		liste = ["elma","armut","kiraz"]
		

        .. tab:: Cevap

            .. activecode:: ch8ex19a
                :nocodelens:

		liste = ["elma","armut","kiraz"]
		
		cevapDogruMu=0
		sayac=0
		while cevapDogruMu ==0:
		    meyve = input("bir meyve giriniz")
		    for listedekiMeyve in liste:
			if listedekiMeyve == meyve:
			    cevapDogruMu=1
		    sayac = sayac + 1
		print("doğru cevabı bulma denemesi: ",sayac)

		
		

#.

    .. tabbed:: ch8ex20t

        .. tab:: Soru

            Kullanıcı -1 girene kadar sürekli sayı alın ve kaç tane asal sayı girildiğini hesaplayın.

            .. activecode::  ch8ex20q
                :nocodelens:

        .. tab:: Cevap

            .. activecode:: ch8ex20a
                :nocodelens:

		sayi = int(input("sayi giriniz?"))
		asalSayisi = 0
		while sayi != -1:
		    asal = 1
		    for bolen in range(2,sayi):
			if sayi % bolen == 0:
			    asal = 0
		    asalSayisi = asalSayisi + asal
		    sayi = int(input("sayi giriniz?"))
		print("asal sayı miktarı",asalSayisi)


		
