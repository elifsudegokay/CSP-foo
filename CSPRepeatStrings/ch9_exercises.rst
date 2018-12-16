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
	:prefix: 9-6-

Ünite 7 ~ Değerlendirme Soruları
--------------------

#.

    .. tabbed:: ch9ex1t

        .. tab:: Soru

            Aşağıdaki kod bloğunu ekran çıktısı “Döngü dönsün yüzler gülsün” olacak şekilde hatalı 5 kodu düzeltin.

            .. activecode:: ch9ex1q
                :nocodelens:

                # 1. Aşama : Değişkeni tanımlayın
                yeniYazimiz = ""
                # 2. Aşama : Veriyi alın
                cumle = "Döngü dönsün yüzler gülsün
                # 3. Aşama : Veriyi her seferinde bir harf alacak şekilde döngüye sokun
                for harf in Cumle
                    # 4. Aşama : Döngü ile yeniYazimiz değişkenimize harfleri atayalım.
                    yeniYazimiz = yeniYazimiz  harf
                # 5. Aşama : Oluşturduğumuz dize (String) değişken içeriğimiz ekrana yazdıralım.
                print(yeniYazimiz

        .. tab:: Cevap

	    .. activecode::  ch9ex1a
                :nocodelens:

                
		# 1. Aşama : Değişkeni tanımlayın
                yeniYazimiz = ""
                # 2. Aşama : Veriyi alın
                cumle = "Döngü dönsün yüzler gülsün"
                # 3. Aşama : Veriyi her seferinde bir harf alacak şekilde döngüye sokun
                for harf in cumle:
                    # 4. Aşama : Döngü ile yeniYazimiz değişkenimize harfleri atayalım.
                    yeniYazimiz = yeniYazimiz + harf
                # 5. Aşama : Oluşturduğumuz dize (String) değişken içeriğimiz ekrana yazdıralım.
                print(yeniYazimiz)

#.

    .. tabbed:: ch9ex2t

        .. tab:: Soru

            Aşağıda bulunan kod bloğu ekran çıktısında dize (String)yi tersten yazdırmaktadır. Dizeyi doğru sırayla ekran çıktısı alacak şekilde düzeltin.

            .. activecode::  ch9ex2q
                :nocodelens:

                # 1. Aşama : Değişkeni tanımlayın
                yeniYazimiz = ""
                # 2. Aşama : Veriyi alın
                cumle = "Bu bir karakter dizisi(String)dir."
                # 3. Aşama : Veriyi her seferinde bir harf alacak şekilde döngüye sokun
                for harf in cumle:
                    # 4. Aşama : Döngü ile yeniYazimiz değişkenimize harfleri atayalım.
                    #yeniYazimiz = yeniYazimiz + harf
                # 5. Aşama : Sonucu yazdıralım
                print(yeniYazimiz)

        .. tab:: Cevap

	    .. activecode::  ch9ex2a
                :nocodelens:

                 # 1. Aşama : Değişkeni tanımlayın
                yeniYazimiz = ""
                # 2. Aşama : Veriyi alın
                cumle = "Bu bir karakter dizisi(String)dir."
                # 3. Aşama : Veriyi her seferinde bir harf alacak şekilde döngüye sokun
                for harf in cumle:
                    # 4. Aşama : Döngü ile yeniYazimiz değişkenimize harfleri atayalım.
                    yeniYazimiz =  yeniYazimiz + harf
                # 5. Aşama : Sonucu yazdıralım
                print(yeniYazimiz)

#.

    .. tabbed:: ch9ex3t

        .. tab:: Soru

           Aşağıdaki kod bloğunda 4. Satırda hatalı olan Girintili ( indented) yazımı düzeltin, Ekran çıktısı “!nuslO uLtuK nünüG muğoD” olmalı.

           .. activecode::  ch9ex3q
                :nocodelens:

                # 1. Aşama : Değişkeni tanımlayın
                yeniYazimiz = ""
                # 2. Aşama : Veriyi alın
                    cumle= "Doğum Günün KutLu Olsun!"
                # 3. Aşama : Veriyi her seferinde bir harf alacak şekilde döngüye sokun
                for harf in cumle :
                # 4. Aşama : Döngü ile yeniYazimiz değişkenimize harfleri atayalım.
                yeniYazimiz =  harf + yeniYazimiz
                # STEP 5: Sonucu yazdıralım
                    #print(yeniYazimiz)


        .. tab:: Cevap

	    .. activecode::  ch9ex3a
                :nocodelens:

                 # 1. Aşama : Değişkeni tanımlayın
                yeniYazimiz = ""
                # 2. Aşama : Veriyi alın
                cumle = "Doğum Günün KutLu Olsun!"
                # 3. Aşama : Veriyi her seferinde bir harf alacak şekilde döngüye sokun
                for harf in cumle :
                # 4. Aşama : Döngü ile yeniYazimiz değişkenimize harfleri atayalım.
                    yeniYazimiz =  harf + yeniYazimiz
                # STEP 5: Sonucu yazdıralım
                print(yeniYazimiz)

#.

    .. tabbed:: ch9ex4t

        .. tab:: Soru

            Aşağıdaki kod bloğunu Dize (String) ifadesi tersten yazacak şekilde düzeltin. Ekran çıktısı “!miyezid rib neB ,yeH” olmalı.

            .. activecode::  ch9ex4q
                :nocodelens:

                # 2. Aşama : Veriyi alın
                cumle = "Hey, Ben bir karakter dizisiyim!"
                # 3. Aşama : Veriyi her seferinde bir harf alacak şekilde döngüye sokun
                for harf in cumle :
                    yeniYazimiz ="" 
                    # 4. Aşama : Döngü ile yeniYazimiz değişkenimize harfleri atayalım.
                    yeniYazimiz = yeniYazimiz + harf
                    # 5. Aşama: Sonucu yazdıralım
                    print(cumle)

        .. tab:: Cevap

	    .. activecode::  ch9ex4a
                :nocodelens:

		# 1. Aşama : Değişinimizi tanımlayalım
		yeniYazimiz =""
                # 2. Aşama : Veriyi alın
                cumle = "Hey, Ben bir karakter dizisiyim!"
                # 3. Aşama : Veriyi her seferinde bir harf alacak şekilde döngüye sokun
                for harf in cumle :
                    # 4. Aşama : Döngü ile yeniYazimiz değişkenimize harfleri atayalım.
                    yeniYazimiz = harf + yeniYazimiz
                    # 5. Aşama: Sonucu yazdıralım
                print(cumle)

#.

    .. tabbed:: ch9ex5t

        .. tab:: Soru

           Aşağıdaki kod bloğundaki metnin yansısı ile birlikte doğru şekilde yazdırmak için hatalı 4 kodu düzeltin. Ekran Çıktısı “.rittset rib uBBu bir testtir.” olmalı."

           .. activecode::  ch9ex5q
                :nocodelens:

                # 1. Aşama : Değişkeni tanımlayın
                yeniYazimiz =
                # 2. Aşama : Veriyi alın
                cumle = "Bu bir testtir."
                # 3. Aşama : Veriyi her seferinde bir harf alacak şekilde döngüye sokun
                for h in cumle:
                    # 4. Aşama : Döngü ile yeniYazimiz değişkenimize harfleri atayalım.
                    yeniYazimiz = harf + yeniYazimiz harf
                # 5. Aşama: Sonucu yazdıralım
                print()


        .. tab:: Cevap

	    .. activecode::  ch9ex5a
                :nocodelens:

                 # 1. Aşama : Değişkeni tanımlayın
                yeniYazimiz =""
                # 2. Aşama : Veriyi alın
                cumle = "Bu bir testtir."
                # 3. Aşama : Veriyi her seferinde bir harf alacak şekilde döngüye sokun
                for harf in cumle:
                    # 4. Aşama : Döngü ile yeniYazimiz değişkenimize harfleri atayalım.
                    yeniYazimiz = harf + yeniYazimiz
                # 5. Aşama: Sonucu yazdıralım
                print(yeniYazimiz + cumle)

#.

    .. tabbed:: ch9ex6t

        .. tab:: Soru

            Aşağıdaki programda bulunan mesajın şifrelenmesi gerekiyor ancak 5 tane hata bulunuyor. Program; “gsrh.rh.hkzigz.” çıktısını yazdıracak şekilde hataları düzeltin.

            .. activecode::  ch9ex6q
                :nocodelens:

                mesaj = "this is sparta"
		str = "abcdefghijklmnopqrstuvwxyz. 
		eStr = zyxwvutsrqponmlkjihgfedcba ."
		sifreliMesaj = mesaj
		for harf in mesaj
		    pos = str.find(harf)
		    sifreliMesaj = sifreliMesaj + eStr[pos:pos+1]
		print(sifreliMesaj)

        .. tab:: Cevap

	    .. activecode::  ch9ex6a
                :nocodelens:

                mesaj = "this is sparta "
                str = "abcdefghijklmnopqrstuvwxyz. "
		eStr = "zyxwvutsrqponmlkjihgfedcba ."
		sifreliMesaj = ""

                for harf in mesaj:
                    pos = str.find(harf)
                    sifreliMesaj = sifreliMesaj + eStr[pos:pos+1]
                print(sifreliMesaj)

#.

    .. tabbed:: ch9ex7t

        .. tab:: Soru

           Aşağıdaki kod, 1’lerin tamamını i’ler ile değiştirmelidir; fakat sonsuz bir döngü içerisindedir. Sonsuz döngüyü durdurmak (kill) için sayfayı yeniden yükleyebilirsiniz. Kodun çalışması için bir satır eklemelisiniz. Kod “Bu bir karakter dizisidir” yazdırmalıdır. 

           .. activecode::  ch9ex7q
                :nocodelens:

                str = "Bu b1r karakter d1z1s1d1r."
                pos = str.find("1")
                while pos >= 0:
                    str = str[0:pos] + "i" + str[pos+1:len(str)]
                print(str)

        .. tab:: Cevap

	    .. activecode::  ch9ex7a
                :nocodelens:

                str = "Bu b1r karakter d1z1s1d1r."
                pos = str.find("1")
                while pos >= 0:
                    str = str[0:pos] + "i" + str[pos+1:len(str)]
		    pos = str.find("1")
                print(str)
#.

    .. tabbed:: ch9ex8t

        .. tab:: Soru

            Aşağıdaki kodda bulunan hataları düzeltin, böylece kod yanlış yazılmış olan “Kızmırı” kelimesini doğru hali olan “Kırmızı” ile değiştirsin. 

            .. activecode::  ch9ex8q
                :nocodelens:

                str = "Benim adım Kızmırı"
		pos = str.find("Kırmızı")
		while pos >= 0:
		    str = str[0:pos+len("Kızmırı")] + "Kırmızı" + str[pos:len(str)]
		    pos = str.find("Kızmırı")
		print(str)

	

        .. tab:: Cevap

	    .. activecode::  ch9ex8a
                :nocodelens:

                str = "Benim adım Kızmırı"
		pos = str.find("Kızmırı")
		while pos >= 0:
		    str = str[0:pos] + "Kırmızı" + str[pos+len("Kızmırı"):len(str)]
		    pos = str.find("Kırmızı")
		print(str)

#.

    .. tabbed:: ch9ex9t

        .. tab:: Soru

           Aşağıdaki kodu; koddaki noktaların yerine virgül gelecek şekilde tamamlayın.

           .. activecode::  ch9ex9q
                :nocodelens:

                str = "Yemek yemeyi. uyumayı. öğrenmeyi. ve kodlamayı severim!"
                pos = str.
                while pos >= :
                    str = str[0:pos] +   + str[  :len(str)]
		    pos =
		print(str)
                

        .. tab:: Cevap

	    .. activecode::  ch9ex9a
                :nocodelens:

                str = "Yemek yemeyi. uyumayı. öğrenmeyi. ve kodlamayı severim!"
                pos = str.find(".")
                while pos >= 0:
                    str = str[0:pos] + ","  + str[pos+1:len(str)]
		    pos = str.find(".")
		print(str)

#.

    .. tabbed:: ch9ex10t

        .. tab:: Soru

            Aşağıdaki kodu; verilen karakter dizisinin, doğru yöndeki ayna görüntüsünü (mirror) ve ardından tersini (reverse) yazdıracak şekilde bitirin. Kodu tamamladığınızda ekranda “Bu bir aynadır!!rıdanya rib uB” çıktısı olmalıdır. 

            .. activecode::  ch9ex10q
                :nocodelens:

                Str1 = ""
                Str2 = ""
                cumle = "Bu bir aynadır!"
                for harf in cumle:   

        .. tab:: Cevap

	    .. activecode::  ch9ex10a
                :nocodelens:

                Str1 = ""
                Str2 = ""
                cumle = "Bu bir aynadır!"

                for harf in cumle:
		    Str1 = Str1 + harf
		    Str2 = harf + Str2
		Str2 = harf + Str2

		print(Str1 + Str2)
		    

#.

    .. tabbed:: ch9ex11t

        .. tab:: Soru

           Aşağıda bir mesajı şifreleyen kod verilmiştir. Şifreli mesajı deşifre eden ve yazdıran kodu aşağıdaki kodun altına yazın. 

           .. activecode::  ch9ex11q
                :nocodelens:

                mesaj = "this is sparta"
		str = "abcdefghijklmnopqrstuvwxyz. "
		eStr = "zyxwvutsrqponmlkjihgfedcba ."
		sifreliMesaj = ""
		for harf in mesaj:
		    pos = str.find(harf)
		    sifreliMesaj = sifreliMesaj + eStr[pos:pos+1]
		print(sifreliMesaj)

		

        .. tab:: Cevap

	    .. activecode::  ch9ex11a
                :nocodelens:

                mesaj = "this is sparta"
		str = "abcdefghijklmnopqrstuvwxyz. "
		eStr = "zyxwvutsrqponmlkjihgfedcba ."
		sifreliMesaj = ""
		for harf in mesaj:
		    pos = str.find(harf)
		    sifreliMesaj = sifreliMesaj + eStr[pos:pos+1]
		print(sifreliMesaj)

		desifreMesaj = ""
		for harf in sifreliMesaj:
		    pos = eStr.find(harf)
		    desifreMesaj = desifreMesaj + str[pos:pos+1]
		print(desifreMesaj)

		
#.

    .. tabbed:: ch9ex12t

        .. tab:: Soru

            Kullanıcının iki kelime arasında sadece bir boşluk gireceğini varsayarak ve find fonksiyonunu kullanarak kullanıcının girdiği cümlede kaç tane kelime var bastırın.

            .. activecode::  ch9ex12q
                :nocodelens:



        .. tab:: Cevap

	    .. activecode::  ch9ex12a
                :nocodelens:

                cumle = input("cümle girin")
                pos = cumle.find(" ")
		sayac = 0
		while pos >= 0:
		    cumle = cumle[pos+1:len(cumle)]
		    pos = cumle.find(" ")
		    sayac = sayac + 1
		print(sayac+1)



#.

    .. tabbed:: ch9ex13t

        .. tab:: Soru

           Kullanıcının iki kelime arasında sadece bir boşluk gireceğini varsayarak ve find fonksiyonunu kullanmadan kullanıcının girdiği cümlede kaç tane kelime var bastırın.

           .. activecode::  ch9ex13q
                :nocodelens:

               


        .. tab:: Cevap

	    .. activecode::  ch9ex13a
                :nocodelens:

                cumle = input("cümle girin")
                sayac = 0
		for harf in cumle:
		    if harf == " ":
			sayac = sayac + 1
		print(sayac + 1)  


#.

    .. tabbed:: ch9ex14t

        .. tab:: Soru

            Kullanıcının iki kelime arasında sadece bir boşluk gireceğini varsayarak kullanıcının girdiği cümledeki kelimeleri alt alta bastırın.

            .. activecode::  ch9ex14q
                :nocodelens:

                
        .. tab:: Cevap

	    .. activecode::  ch9ex14a
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

    .. tabbed:: ch9ex15t

        .. tab:: Soru

           Kullanıcının iki kelime arasına yanlışlıkşa birden fazla boşluk koyduğu cümleyi tek boşluklu hale getirin.

           .. activecode::  ch9ex15q
                :nocodelens:

                

        .. tab:: Cevap

	    .. activecode::  ch9ex15a
                :nocodelens:

                cumle = input("bir cümle giriniz")
                pos = cumle.find(" ")

		while pos >= 0:
		    cumle = cumle[0:pos]+" "+ cumle[pos+2:len(cumle)]
		    pos = cumle.find("  ")

                print(cumle)


#.

    .. tabbed:: ch9ex16t

        .. tab:: Soru

            Kullanıcıdan alınan cümle palindrom mu değil mi ekrana bastırın.

            .. activecode::  ch9ex16q
                :nocodelens:

               

        .. tab:: Cevap

	    .. activecode::  ch9ex16a
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

    .. tabbed:: ch9ex17t

        .. tab:: Soru

           Kullanıcıdan bir cümle bir kelime alın, kelimenin içindeki her bir harf cümlenin içinde kaç kez geçiyor bastırın. 

           .. activecode::  ch9ex17q
                :nocodelens:

                

        .. tab:: Cevap

	    .. activecode::  ch9ex17a
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

    .. tabbed:: ch9ex18t

        .. tab:: Soru

            Kullanıcıdan kucuk harflerden oluşan bir kelime alın ve butun harflerini büyük harfe çevirin.

            .. activecode::  ch9ex18q
                :nocodelens:

                

        .. tab:: Cevap

	    .. activecode::  ch9ex18a
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

    .. tabbed:: ch9ex19t

        .. tab:: Soru

           Kullanıcıdan büyük ve küçük harflerden oluşan bir cümle alın ve küçük harfleri büyüğe, büyük harfleri küçüğe çevirin.

           .. activecode::  ch9ex19q
               :nocodelens:

        .. tab:: Cevap

	    .. activecode::  ch9ex19a
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

    .. tabbed:: ch9ex20t

        .. tab:: Soru

            Kullanıcının girdiği cümleden ünlü harfleri çıkarın.

            .. activecode::  ch9ex20q
                :nocodelens:

                
	.. tab:: Cevap
	
	    .. activecode::  ch9ex20a
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


