..  Copyright (C)  Mark Guzdial, Barbara Ericson, Briana Morrison
    Permission is granted to copy, distribute and/or modify this document
    under the terms of the GNU Free Documentation License, Version 1.3 or
    any later version published by the Free Software Foundation; with
    Invariant Sections being Forward, Prefaces, and Contributor List,
    no Front-Cover Texts, and no Back-Cover Texts.  A copy of the license
    is included in the section entitled "GNU Free Documentation License".

.. 	qnum::
	:start: 1
	:prefix: csp-7-5-
	
.. highlight:: java
   :linenothreshold: 4


Burada Bir Model Var ! 
=====================================

Bu programlarda, veri işlenirken yaygın olan bir model var. Biz bunu **Biriktirici Model (Accumulator Pattern)** olarak adlandırıyoruz. Yukarıdaki ilk programda, ``toplam`` değişkeninde verilerdeki değerleri *biriktiriyoruz*. Son birkaç programda, bir ``carpim`` değişkeninde carpimlari *biriktirdik*.


.. There's a pattern in these programs, a pattern that is common when processing data.  We call this the **Accumulator Pattern**.  In the first program above, we *accumulated* the values into the variable ``sum``.  In the last few programs, we *accumulated* a product into the variable ``product``.



İşte bu modelde ki 5 adım:

1. Biriktirici değişkene başlangıç değeri ata. İşlenecek veri yoksa, istediğimiz değer budur.
2. İşlenecek tüm verileri alın.
3. Bir ``for`` döngüsü kullanarak veriye ulaşın, böylece değişken verilerdeki her bir değeri alır.
4. Verilerin *her bir parçasını* biriktirici’de birleştirin.
5. Veriyi işleyin. 

.. Here are the five steps in this pattern.
.. 1. Set the accumulator variable to its initial value.  This is the value we want if there is no data to be processed.
.. 2. Get all the data to be processed.
.. 3. Step through all the data using a ``for`` loop so that the variable takes on each value in the data.
.. 4. Combine each *piece* of the data into the accumulator.
.. 5. Do something with the result.





Biriktirici Model’i Kullanma ~ Using the Accumulator Model
-----------------------------

1 ile 100 arasındaki tüm sayıların toplamı nedir? Modelimizi kullanarak bunu kolayca yanıtlayabiliriz.

.. activecode:: Numbers_Sum
    :tour_1: "Code tour"; 2: accum_line2; 4: accum_line4; 6: accum_line6; 8: accum_line8; 10: accum_line10;
	
    # ADIM 1: BIRIKTIRICI’YI BASLAT 
    toplam = 0  # hiçbir şey ile basla

    # ADIM 2: VERIYI AL
    sayilar = range(1,101)

    # ADIM 3: VERI UZERINDEN DONGU KUR
    for sayi in sayilar :
    	# ADIM 4: BIRIKTIR
    	toplam = toplam + sayi

    # STEP 5: VERIYI ISLE
    print("Sayilarin toplami: ", toplam)


``range`` fonksiyonunun burada kullanabileceğimiz bir sürümü daha var. Üç adet girdi sayısı sağlayarak, *başlangıç*, *bitiş* (son değerden bir fazla olan) ve *adım* -sayıların arasını ne kadar değiştireceğimiz- değerlerini belirleyebiliriz.

.. The ``range`` function has one more version that we can use here.  By providing *three* input numbers, we can specify the *start* value, the *ending* value (which is one more than the *last* value), and the *step* -- how much to change *between* numbers.

.. activecode:: Range_Examples

  print(range(1,11,1))
  print(range(0,11,2))
  print(range(1,11,3))
  print(range(5,50,5))
  print(range(10,1,-1))

Şimdi biraz daha zor bir soruya cevap verelim: 0 ile 100 arasındaki çift sayıların toplamı nedir? Bizim modelimizle bu kolay.
  
.. activecode:: Numbers_Sum_Even
    :tour_1: "Code tour"; 2: accE_line2; 4: accE_line4; 6: accE_line6; 8: accE_line8; 10: accE_line10;
	
    # ADIM 1: BIRIKTIRICI’YI BASLAT
    toplam = 0  # hicbirseyle basla

    # ADIM 2: VERIYI AL
    sayilar = range(1,101,2)

    # ADIM 3: VERI UZERINDEN DONGU KUR
    for sayi in sayilar :
    	# ADIM 4: BIRIKTIR
    	toplam = toplam + sayi

    # ADIM 5: VERIYI ISLE
    print("Sayıların toplamı: ", toplam)

.. mchoice:: 7_5_1_Numbers_Even_Q1
   :answer_a: Çünkü, 0’dan başlıyoruz.
   :answer_b: Çünkü, 100’ü de dahil etmek istiyoruz.
   :answer_c: Çünkü, bilgisayar sadece 1 ve 0’ları anlıyor. 
   :answer_d: Çünkü, 2’li adımlar kullanıyoruz. 
   :correct: b
   :feedback_a: Yanlış.100’ü dahil etmek istiyoruz.
   :feedback_b: Doğru. 101'den ÖNCE durdurursak, 100'ü dahil ederiz.
   :feedback_c: Yanlış. Dahili olarak, evet, ancak Python'da, tüm ondalık basamaklara izin verilir.
   :feedback_d: Yanlış.Bu gerçekten önemli değil.

   Yukarıdaki programda neden 101'de duruyoruz?

.. mchoice:: 7_5_2_Numbers_Even_Q2
   :answer_a: Çünkü eğer 1 ile başlasaydık, tüm tek sayıları alırdık.
   :answer_b: Çünkü, bütün listeler sıfır ile başlar. 
   :answer_c: Çünkü, 101 ile listeyi bitiriyoruz. 
   :correct: a
   :feedback_a: Doğru. Bu bize [0,2,4,6,...,98,100] listesini verir.
   :feedback_b: Yanlış.0 ile başlamak zorunda değiller.
   :feedback_c: Yanlış. Bu doğru ama burada mantıklı değil.

   Neden SIFIR ile başlıyoruz?


Bu programda gerçekten neler olduğunu nasıl anlarız? *sayi* değişkenin 0’dan 100’e çift değerleri aldığını nasıl bilebiliriz? Bunun bir yolu CodeLens i kullanmak ama 0’dan 20 ‘ye kadar bir problem için. Programda satır satır gidebilir veya programın sonuna *Last (Son)* butonuna basarak gidebilir ve geri geri gidebiliriz.



.. codelens:: Numbers_Sum_Step
	
    # ADIM 1: BIRIKTIRICI’YI BASLAT
    toplam = 0  # hicbirseyle basla

    # ADIM 2: VERIYI AL
    sayilar = range(1,21,2)

    # ADIM 3: VERI UZERINDEN DONGU KUR
    for sayi in sayilar :
    	# ADIM 4: BIRIKTIR
    	toplam = toplam + sayi

    # STEP 5: VERIYI ISLE
    print("Sayıların toplamı: " , toplam)


    
.. parsonsprob:: 7_5_3_Sum_100

   Sıradaki program, 1’den 100 kadar olan tek sayıları ekranda yazdırmamızı sağlayan doğru kodları içeriyor ama karışık sıradalar. Soldaki kod bloklarını sağa doğru doğru sırada sürükleyip bırakın. <b> Unutmayın, döngünün gövdesindeki ifadeler girintilenmelidir! </b> Girintilemek için sağa biraz daha doğru iterek bırakın. <i>Check Me</i> butonuna basıp cevabınızı kontrol edin.


   -----
   toplam = 0  
   =====
   sayilar = range(1,101,2)
   =====
   for sayi in sayilar:
   =====
       toplam = toplam + sayi
   =====
   print('Sayilarin toplami: ' , toplam)


.. mchoice:: 7_5_4_Numbers_Add_Odds_Q1
   :answer_a: range fonksiyonunda adımı 2’den 3 ‘e çevirmek
   :answer_b: aralıkta ki son bitiş değerini 101’den 100’e çevirmek
   :answer_c: aralıkta ki son bitiş değerini 101’den 99’a çevirmek
   :answer_d: aralıkta ki başlangıç değerini 0’dan 1’e çevirmek 
   :correct: d
   :feedback_a: Yanlış. Bize vereceği [0,3,6,9,12...99]
   :feedback_b: Yanlış. Bu bize 0’dan 98’e kadar ki çift sayıları verir. 
   :feedback_c: Yanlış. Bu bize 0’dan 98’e kadar ki çift sayıları verir.
   :feedback_d: Doğru. Bu bize [1,3,5,...99] verir.

   99'a kadar olan TEK numaralarını eklemek için yukarıdaki programı değiştirin (Aktif Kod:3(cift_sayilari_toplama)). Toplam sonucu 2500 olmalıdır. Programda ne tür bir değişiklik yaptın?
   
.. parsonsprob:: 7_5_5_Sum_From_50

   Sıradaki program, 50’den 100 kadar olan çift sayıların toplamanı biriktirici model kullanarak ekranda sağlayan doğru kodları içeriyor ama karışık sıradalar ve <b>ekstra bir blok</b> içeriyor. Soldaki gereken kod bloklarını sağa doğru doğru sırada sürükleyip bırakın. Unutmayın, döngünün gövdesindeki ifadeler girintilenmelidir!  Girintilemek için sağa biraz daha doğru iterek bırakın. <i>Check Me</i> butonuna basıp cevabınızı kontrol edin.</p>


   -----
   toplam = 0  
   =====
   sayilar = range(50,101,2)
   =====
   for sayi in sayilar:
   =====
       toplam = toplam + sayi
   =====
   print("Sayıların toplamı: ", toplam)
   =====
   sayilar = range(50,100,2) #distractor




