..  Copyright (C)  Mark Guzdial, Barbara Ericson, Briana Morrison
    Permission is granted to copy, distribute and/or modify this document
    under the terms of the GNU Free Documentation License, Version 1.3 or
    any later version published by the Free Software Foundation; with
    Invariant Sections being Forward, Prefaces, and Contributor List,
    no Front-Cover Texts, and no Back-Cover Texts.  A copy of the license
    is included in the section entitled "GNU Free Documentation License".

.. 	qnum::
	:start: 1
	:prefix: csp-12-6-
	
.. highlight:: python
   :linenothreshold: 3

if ile Alıştırmalar
======================

Aşağıdaki program küçük birkaç noktadan dolayı hatalıdır.``agirlik`` değişkeninin sahip olacağı bir değer için ``fiyat`` değişkenine herhangi bir değer atanmayacaktır, dolayısıyla ``toplam``’ın hesaplanması başarısız olacaktır ve  program bir şeyler **tanımlı değil (“is not defined”)** şeklinde bir hata mesajı verecektir. İşte tam da bu yüzden profesyonel programcılar programın başında fiyat gibi değişkenlere *bir değer* atarlar, böylece bu tür hatalar oluşmaz. Sizce ``agirlik`` değişkeninin hangi değeri için böyle bir hata ile karşılaşırız? Aşağıdaki kodu farklı ağırlık değerlerini denemek için değiştiriniz.

.. The program below is broken in a subtle way.  For one value of ``weight``, the ``price`` will not be set to any value, so the calculation of ``total`` will fail with an error that something ``is not defined``.  This is why professional programmers will assign *some* value to a variable like ``price`` at the beginning of the program, so that errors like this won't happen.  Can you figure out the value of ``weight`` that will result in an error?  Modify the code below to try different values for weight.  

.. activeCode:: Fiyat_if_deger
  :tour_1: "Yapısal Tur"; 1: c1-line1; 2-3: c1-line2-3; 4-5: c3-line4-5; 6: c1-line6; 7-9: c3f-line7-9;

  agirlik = 0.5
  if agirlik < 1:
      fiyat = 1.45
  if agirlik > 1: 
      fiyat = 1.15
  toplam = agirlik * fiyat
  print("ağırlık: ", agirlik)
  print("fiyat: ", fiyat)
  print("toplam: ", toplam)

Yukarıdaki kodda ``agirlik`` değişkeni için farklı değerler deneyerek aşağıdaki soruyu cevaplamaya çalışın:
        
.. fillintheblank:: 12_6_1_brokenrange_fill

   Hangi ağırlık değeri için program, fiyat tanımlı değildir şeklinde hata mesajı ile sonlanacaktır?

   -    :^1$|1\.[0]*$: Doğru!
        :.*: Hangi değeri denemedin şimdiye kadar?

Birden fazla ``if`` yapısı kullanma imkanına sahipsiniz ve her biri aynı ya da farklı veriler için kullanılabilir. Fiyatların sadece ağırlığa değil, 10 taneden fazla alımda %10 indirimin sağlandığı  daha karmaşık bir sistem düşünelim.

.. It is certainly possible to have multiple ``if`` statements, and each one can match (or not match) the data.  Imagine a more complicated price scheme, where the price is based on the weight, but there is also a 10% discount for buying more then 10 items.

.. activeCode:: Coklu_If
  :tour_1: "Yapısal Tur"; 1: c1-line1; 2: c4-line2; 3-4: c1-line2-3; 5-6: c1-line4-5; 7: c1-line6; 8-9: c4-line8-9; 10-12: c3f-line7-9; 

  agirlik = int(input("ağırlığı giriniz"))
  adet = int(input("adeti giriniz"))
  if agirlik < 1:
      fiyat = 1.45
  if agirlik >= 1: 
       fiyat= 1.15
  toplam = agirlik * fiyat
  if adet >= 10:
      toplam = toplam * 0.9
  print("ağırlık: ", agirlik)
  print("fiyat: ", fiyat)
  print("toplam: ", toplam)

.. mchoice:: 12_6_2_Coklu_If
  :answer_a: $3.45
  :answer_b: $3.11
  :answer_c: $3.105
  :answer_d: $3.10
  :correct: c
  :feedback_a: Yanlış. Eğer %10 indirim olmasaydı cevap bu olacaktı.
  :feedback_b: Yanlış. Python otamatik olarak yuvarlama işlemi yapmaz
  :feedback_c: Doğru cevap bu, ama $3.105 ödemek o kadar da kolay olmazdı ;)
  :feedback_d: Yanlış. Python otamatik olarak $3.105’i  $3.10’e çeviremez.  

   Adet 12, ağırlık 3 ise total ne olacaktır?
   
.. mchoice:: 12_6_3_alinanNot_If
   :answer_a: A
   :answer_b: B
   :answer_c: C
   :answer_d: D
   :answer_e: E
   :correct: d
   :feedback_a: Yanlış. İlk dört deyimin bir if ile başladığına dikkat et.
   :feedback_b: Yanlış. İlk dört if deyiminin hepsinin çalıştırıldığına dikkat et
   :feedback_c: Yanlış. Bu kodu aktif kod penceresine kopyala ve çalıştır. 
   :feedback_d: Doğru.İlk dört if deyiminin hepsi çalıştırılıyor dolayısıyla alinanNot sırayla A, B, C ve en son D olacak 
   :feedback_e: Yanlış. Eğer skor 60’dan küçük olsaydı bu cevap doğru olacaktı   

   Aşağıdaki kod çalıştığında ekranda ne gözükecektir?
   
   :: 
   
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
     print("alınan not: ", alinanNot)
     
.. mchoice:: 12_6_4_Logic_Ifs
   :answer_a: Bu kod herhangi bir x değeri ile çalıştıktan sonra, x her zaman 0’a eşit olacaktır.
   :answer_b: Eğer x, 2’den büyükse, x’in en son değeri, iki katı olacaktır.
   :answer_c: Eğer x, 2’den büyükse, x’in en son değeri 0 olacaktır
   :correct: c
   :feedback_a: Yanlış. Eğer x 1 olsaydı, o zaman hala 1’e eşit olurdu
   :feedback_b: Yanlış. Eğer x 2’den büyükse, kodda neler gerçekleşir? 
   :feedback_c: Doğru. Eğer x 2’den büyükse 0’a eşitlenecektir  

   Verilen koda göre aşağıdakilerden hangisi doğrudur?  
   
   :: 

     x = 3
     if (x > 2): 
         x = x * 2;
     if (x > 4): 
         x = 0;
     print(x)
     

