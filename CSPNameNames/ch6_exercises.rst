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
	:prefix: 6-10-

Ünite 8 - Değerlendirme Soruları
--------------------

#.

    .. tabbed:: ch6ex1t

        .. tab:: Soru

            carpim_sembolu(sayi1,sayi2) isimli bir python işlevi yazın ki sayi1 den sayi2 ‘ye kadar olan sayıların çarpımını döndürsün.(sayi1 < sayi2  olacak şekilde).

            .. activecode:: ch6ex1q
                :nocodelens:

                def carpim_sembolu(sayi1,sayi2):

        .. tab:: Cevap

	    .. activecode::  ch6ex1a
                :nocodelens:

                def carpim_sembolu(sayi1, sayi2):
		    carpim = 1
		    liste=range(sayi1, sayi2 + 1)
		    for sayi in liste:
			carpim = carpim * sayi
		    return carpim
		sonuc=carpim_sembolu(1,5)
		print(sonuc)

		

#.

    .. tabbed:: ch6ex2t

        .. tab:: Soru

            tekrar(cumle, sayi) isimli bir yordam yazın. Bu yordam kullanıcının girdiği cumle’yi verilen sayi değeri kadar ekranda yazdırsın.

            .. activecode::  ch6ex2q
                :nocodelens:

                

        .. tab:: Cevap

	    .. activecode::  ch6ex2a
                :nocodelens:
		
		def tekrar(cumle,sayi):
                    i = 0
		    while i < sayi:
			print(cumle)
			i=i+1
		cumle="Merhaba Dunya"
		tekrar(cumle,3)

#.

    .. tabbed:: ch6ex3t

        .. tab:: Soru

           Kullanıcının girdiği bir kelime ve bir harf olarak iki argüman alan bir işlev yazın, kelimenin içindeki verilen harfin içinde kaç kez geçtiğini bulsun.

           .. activecode::  ch6ex3q
                :nocodelens:

                def harfsayan(kelime,harf):
                


		cumle="Merhaba"
		sayi=harfsayan(cumle,'e')
		print(sayi)


        .. tab:: Cevap

	    .. activecode::  ch6ex3a
                :nocodelens:

                def harfsayan(kelime,harf):
		    adet=0
		    for c in kelime:
			if harf == c:
			    adet += 1
		    return adet

		cumle="Merhaba"
		sayi=harfsayan(cumle,'e')
		print(sayi)
		
		


#.

    .. tabbed:: ch6ex4t

        .. tab:: Soru

            Verilen bir listedeki en büyük sayıyı bulan bir fonksiyon yazınız.

            .. activecode::  ch6ex4q
                :nocodelens:

                

        .. tab:: Cevap

	    .. activecode::  ch6ex4a
                :nocodelens:
		
		def maksimum(liste):
		    enbuyuk = liste[0]
		    for sayi in liste:
			if enbuyuk < sayi:
			    enbuyuk = sayi
		    return enbuyuk
		liste1=[1,3,5,12,1,-1,15]
		print(maksimum(liste1))
		

#.

    .. tabbed:: ch6ex5t

        .. tab:: Soru

           degistir(cumle, eski, yeni) seklinde bir yordam yazın ki bu yordam verilen cümlede ki eski bir karakteri değiştirmek istediğiniz yeni bir karakterle değiştirip cümleyi ekranda yazdırsın.

           .. activecode::  ch6ex5q
                :nocodelens:

                

		str ="Yemek yemeyi. uyumayı. öğrenmeyi. ve kodlamayı severim!"
		degistir(str,".",",")

		

        .. tab:: Cevap

	    .. activecode::  ch6ex5a
                :nocodelens:

                def degistir(cumle,eski,yeni):
		    pos = cumle.find(eski)
		    while pos >= 0:
			cumle = cumle[0:pos] + yeni  + cumle[pos+1:len(cumle)]
			pos = cumle.find(eski)
		    print(cumle)
		str ="Yemek yemeyi. uyumayı. öğrenmeyi. ve kodlamayı severim!"
		degistir(str,".",",")

		


#.

    .. tabbed:: ch6ex6t

        .. tab:: Soru

            Verilen bir cümlenin palindrom olup olmadığını söyleyen bir yordam yazınız.

            .. activecode::  ch6ex6q
                :nocodelens:

                def palindrom_mu(cumle):






		str ="meyve"
		palindrom_mu(str)
		

        .. tab:: Cevap

	    .. activecode::  ch6ex6a
                :nocodelens:

                def palindrom_mu(cumle):
                    n = len(cumle) -1
		    sonuc = "evet palindrom"
		    for harf in cumle:
			if harf != cumle[n]:
			    sonuc="palindrom degil"
			 n = n - 1
		    print(sonuc)

		str ="meyve"
		palindrom_mu(str)



#.

    .. tabbed:: ch6ex7t

        .. tab:: Soru

           Kişinin yaşına göre ehliyet alıp alamayacağını söyleyen bir yordam yazınız

           .. activecode::  ch6ex7q
                :nocodelens:

                

        .. tab:: Cevap

	    .. activecode::  ch6ex7a
                :nocodelens:

		def ehliyet(yas):
		    if (yas < 18):
			print("Ehliyet alamazsınız")
		    else:
			print("Ehliyet alabilirsiniz")

                
#.

    .. tabbed:: ch6ex8t

        .. tab:: Soru

            Bir listedeki sayıların toplamını veren toplam isimli işlevi yazınız 

            .. activecode::  ch6ex8q
                :nocodelens:

               

	

        .. tab:: Cevap

	    .. activecode::  ch6ex8a
                :nocodelens:

                def toplam(sayiListesi):
		    total = 0
		    for sayi in sayiListesi:
			toplam += sayi
		    return toplam

		print(toplam(range(5))

#.

    .. tabbed:: ch6ex9t

        .. tab:: Soru

           Bir karakter dizisinin tersini döndüren işlevi yazınız

           .. activecode::  ch6ex9q
                :nocodelens:

                

        .. tab:: Cevap

	    .. activecode::  ch6ex9a
                :nocodelens:

                def tersineCevir(str):

		    yeniStr = " "
		    pozisyon = len(str)
		    while(pozisyon > 0):
		        yeniStr += str[pozisyon -1]
		        pozisyon = pozisyon -1
		    return yeniStr

		print(tersineCevir("kaya"))
		print(tersineCevir("ayşe"))

#.

    .. tabbed:: ch6ex10t

        .. tab:: Soru

            Aldığı iki sayıdan en büyük olanı döndüren enBuyuk isimli işlevi yazınız

            .. activecode::  ch6ex10q
                :nocodelens:

                

        .. tab:: Cevap

	    .. activecode::  ch6ex10a
                :nocodelens:

                def enBuyuk(sayi1, sayi2):
		
		    if sayi1 > sayi2:
			return sayi1
		    elif sayi2 > sayi1:
			return sayi2
		    else
			return "Sayılar eşit"

		print(enBuyuk(3, 56))
		print(enBuyuk(72, 40))
		    

#.

    .. tabbed:: ch6ex11t

        .. tab:: Soru

           Sayının kuvvetini hesaplayan işlevi yazınız

           .. activecode::  ch6ex11q
                :nocodelens:

               

		

        .. tab:: Cevap

	    .. activecode::  ch6ex11a
                :nocodelens:

                def usAlma(sayi, us):
		    sonuc = 1
		    for i in range(us):
		        sonuc = sonuc * sayi
		    return sonuc

		print(usAlma(2,3))
		
#.

    .. tabbed:: ch6ex12t

        .. tab:: Soru

            Fahrenheit cinsinden aldığı dereceyi Celsius'a çeviren işlevi yazınız.

            .. activecode::  ch6ex12q
                :nocodelens:



        .. tab:: Cevap

	    .. activecode::  ch6ex12a
                :nocodelens:

                def Fahr_Celsius(derece):
		    return ((derece -32) * ( 5 / 9))



#.

    .. tabbed:: ch6ex13t

        .. tab:: Soru

           Parametreleri bir liste ve bir sayı olan sayının listede olup olmadığını kontrol eden bir yordam yazınız. 

           .. activecode::  ch6ex13q
                :nocodelens:

               


        .. tab:: Cevap

	    .. activecode::  ch6ex13a
                :nocodelens:

                def arama(liste, sayi):
		    sayac = 0
		    for eleman in liste:
			if eleman == sayi:
			    sayac += 1
		    if sayac != 0:
			print("Var")
		    else:
			print("Yok")
		

		listem = [3, 22, 56, 87, 92, 45, 32]
		arama(listem, 92)
		arama(listem, 76)


#.

    .. tabbed:: ch6ex14t

        .. tab:: Soru

            Kullanıcının iki kelime arasında sadece bir boşluk gireceğini varsayarak kullanıcının girdiği cümledeki kelimeleri alt alta bastırın.

            .. activecode::  ch6ex14q
                :nocodelens:

                
        .. tab:: Cevap

	    .. activecode::  ch6ex14a
                :nocodelens:

                cumle = input("cümle girin")
                kelime = ""
		for harf in cumle:
		    if harf != " ":
			kelime = kelime + harf
		    else:
			print(kelime)
			kelime = ""
		print(kelime) 


#.

    .. tabbed:: ch6ex15t

        .. tab:: Soru

           Kullanıcının iki kelime arasına yanlışlıkşa birden fazla boşluk koyduğu cümleyi tek boşluklu hale getirin.

           .. activecode::  ch6ex15q
                :nocodelens:

                

        .. tab:: Cevap

	    .. activecode::  ch6ex15a
                :nocodelens:

                cumle = input("bir cümle giriniz")
                pos = cumle.find(" ")

		while pos >= 0:
		    cumle = cumle[0:pos]+" "+ cumle[pos+2:len(cumle)]
		    pos = cumle.find("  ")

                print(cumle)


#.

    .. tabbed:: ch6ex16t

        .. tab:: Soru

            Kullanıcıdan alınan cümle palindrom mu değil mi ekrana bastırın.

            .. activecode::  ch6ex16q
                :nocodelens:

               

        .. tab:: Cevap

	    .. activecode::  ch6ex16a
                :nocodelens:

                cumle = input("cümle girin")

                n = len(cumle) -1

		sonuc = "evet palindrom"
		for harf in cumle:
		    if harf != cumle[n]:
			sonuc="palindrom değil"
                    n = n - 1
                print(sonuc)

#.

    .. tabbed:: ch6ex17t

        .. tab:: Soru

           Kullanıcıdan bir cümle bir kelime alın, kelimenin içindeki her bir harf cümlenin içinde kaç kez geçiyor bastırın. 

           .. activecode::  ch6ex17q
                :nocodelens:

                

        .. tab:: Cevap

	    .. activecode::  ch6ex17a
                :nocodelens:

                cumle = input("kelime girin")
                kelime = input("kelime girin")
		

		for harfK in kelime:
		    sayac = 0
		    for harfC in cumle:
			if harfC == harfK:
			    sayac = sayac + 1
		    print(harfK + " is in the sentence " + str(sayac) + " times")

#.

    .. tabbed:: ch6ex18t

        .. tab:: Soru

            Kullanıcıdan kucuk harflerden oluşan bir kelime alın ve butun harflerini büyük harfe çevirin.

            .. activecode::  ch9ex18q
                :nocodelens:

                

        .. tab:: Cevap

	    .. activecode::  ch6ex18a
                :nocodelens:

                cumle = input("kelime girin")
                kucuk = "abcdefghijklmnopqrstuvwxyz"
		buyuk = "ABCDEFGHIJKLMNOPQRSTUVWXYZ"
		yeniCumle = ""

                for harf in cumle:
                    pos = kucuk.find(harf)
                    yeniCumle = yeniCumle + buyuk[pos]
                print(yeniCumle)

#.

    .. tabbed:: ch6ex19t

        .. tab:: Soru

           Kullanıcıdan büyük ve küçük harflerden oluşan bir cümle alın ve küçük harfleri büyüğe, büyük harfleri küçüğe çevirin.

           .. activecode::  ch6ex19q
               :nocodelens:

        .. tab:: Cevap

	    .. activecode::  ch6ex19a
                :nocodelens:

                cumle = input("kelime girin")
                kucuk = "abcdefghijklmnopqrstuvwxyz"
		buyuk = "ABCDEFGHIJKLMNOPQRSTUVWXYZ"
		yeniCumle = ""

                for harf in cumle:
                    pos = kucuk.find(harf)
                    yeniCumle = yeniCumle + buyuk[pos]
                print(yeniCumle)


#.

    .. tabbed:: ch6ex20t

        .. tab:: Soru

            Kullanıcının girdiği cümleden ünlü harfleri çıkarın.

            .. activecode::  ch6ex20q
                :nocodelens:

                
	.. tab:: Cevap
	
	    .. activecode::  ch6ex20a
                :nocodelens:

                cumle = input("kelime girin")
                kucuk = "aeiouAEIOU"

                for harf in cumle:
                    pos = kucuk.find(harf)
                    if pos != -1:
                	pos = cumle.find(harf)
                        cumle = cumle[0:pos]+cumle[pos+1:len(cumle)]
                	print(cumle)
		print(cumle)


