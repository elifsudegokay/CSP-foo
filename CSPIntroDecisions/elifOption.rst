..  Copyright (C)  Mark Guzdial, Barbara Ericson, Briana Morrison
    Permission is granted to copy, distribute and/or modify this document
    under the terms of the GNU Free Documentation License, Version 1.3 or
    any later version published by the Free Software Foundation; with
    Invariant Sections being Forward, Prefaces, and Contributor List,
    no Front-Cover Texts, and no Back-Cover Texts.  A copy of the license
    is included in the section entitled "GNU Free Documentation License".

..  qnum::
  :start: 1
  :prefix: csp-13-4-

Daha Fazla Seçenek: "elif" kullanmak
================================
Daha önce iki olası seçenek arasında karar vermek için ``if`` ve ``else`` kullanmıştık ama ya daha fazla seçenek olsaydı ne yapardınız? Peki ya bir değerin negatif, 0 ya da pozitif olup olmadığını kontrol etmek isteseydiniz ne yapardınız? Bunu yapmanın bir yolu aşağıda gösterilen çoklu ``if`` deyimlerini kullanmaktır.  

.. activecode:: sd_three_options_elif
    :tour_1: "Structural Tour"; 1: sd5-line1; 2-3: sd5-line2-3; 4-5: sd5-line4-5; 6-7: sd5-line6-7;

    x = 8
    if x < 0:
        print("x negatiftir")
    if x == 0: 
        print("x'in değeri 0'dır")
    if x > 0: 
        print("x pozitiftir") 
       
Bu kodu farklı x değerleri için tekrar tekrar çalıştırın ve en az bir pozitif, bir negatif ve 0 değeri için doğru çalışıp çalışmadığını kontrol edin. X değerini kullanıcıdan alacak şekilde kodu değiştirin.


..  index::
    single: elif

Üç seçenek arasından seçim yapmanın bir diğer yolu ``if`` kullanmaktır ancak bu sefer ``if`` yapısını ``elif`` takip eder ve en son olarak ``else`` gelir.  

.. activecode:: sd_three_options_elif_elif
    :tour_1: "Structural Tour"; 1: sd6-line1; 2-3: sd6-line2-3; 4-5: sd6-line4-5; 6-7: sd6-line6-7;

    x = 8
    if x < 0:
        print("x negatiftir")
    elif x == 0: 
        print("x'in değeri 0'dır")
    else:
        print("x pozitiftir")
        
Sizce hangisi daha iyi? Başlangıçta 3 tane ``if`` deyimini anlamak daha kolay gelebilir. Ancak deneyimli kişiler  ``if`` , ``elif``, and ``else`` kullanmayı tercih ediyorlar. Çünkü bunu çalıştırmak diğerine nazaran daha hızlı ve arada herhangi bir değeri kaçırma ihtimali daha az.
       
**Karışık Programlar**

.. parsonsprob:: 13_4_1_string_elif_elif

   Aşağıdaki program hangi takımın kazandığını göstermeli, beraberlik varsa da beraberliği bildirmeli. Kod satırları karışık olarak verilmiştir. Doğru sıra ve girintili yazma şekli ile sürükleyip bırak.   
   -----
   takim1 = 20
   takim2 = 20
   =====
   if (takim1 > takim2):
       print("takim1 kazandi")
   =====
   elif (takim2 > takim1):
   =====
       print("takim2 kazandi")
   =====
   else:
   =====
       print("takim1 ve takim2 berabere")
      
Eğer ihtiyacınız varsa birden fazla ``elif``  deyimini kullanabilirsiniz. Ama sadece 1 tane ``else``  deyimi kullanabilirsiniz. Ya eğer elinizde 0-1 arasında bir sayınız varsa ve siz bunun hangi çeyrek dilimde olduğunu merak ediyorsanız?  

.. activecode:: sd_four_options_elif
    :tour_1: "Structural Tour"; 1: sd7-line1; 2-3: sd7-line2-3; 4-5: sd7-line4-5; 6-7: sd7-line6-7; 8-9: sd7-line8-9;

    x = .25
    if x <= .25:
        print("x ilk çeyrek dilimde - x <= .25")
    elif x <= .5: 
        print("x ikinci çeyrek dilimde - .25 < x <= .5")
    elif x <= .75:
        print("x üçüncü çeyrek dilimde  - .5 < x <= .75")
    else:
        print("x dördüncü çeyrek dilimde - .75 < x <= 1")
       
.. mchoice:: 13_4_2_elif1_elif
   :answer_a: x ilk çeyrek dilimde - x <= .25
   :answer_b: x ikinci çeyrek dilimde - .25 < x <= .5
   :answer_c: print("x üçüncü çeyrek dilimde  - .5 < x <= .75")
   :answer_d: print("x dördüncü çeyrek dilimde - .75 < x <= 1")
   :correct: c
   :feedback_a: Yanlış. Bu mesajı ancak  x .25’den küçük olsaydı basardı 
   :feedback_b: Yanlış. 6-7 satırda bulunan satırları ile 4-5. satırdakilerle yer değiştirdiğimiz için bu mesajı asla basmayacak. 
   :feedback_c: Doğru. Bu mesaj eğer ilk if doğru değilse ve x 0.75’den küçükse basılacaktır. Böylece iki satırı yer değiştirmek aslında kodun yapmak istediği işlevi karıştıracak ve kod yanlış bir şekilde 0.5 için 3. Çeyrekte cevabını basacaktır.   
   :feedback_d: Yanlış. Eğer diğer bütün if’ler yanlış olsaydı bu mesajı basardı.  

   Eğer 6. ve 7. satırları 4-5’in öncesine koymuş olsaydık ve x’in değeri 0.5 olsaydı ekrana ne basardı?
   
Aşağıda fala bakan ``elif`` and ``else`` kullanarak yazılmış bir kod örneği görebilirsiniz.
   
.. activecode:: fortune_elif_elif
    :tour_1: "Structural Tour"; 1: elif1-line1; 2-3: elif1-line2-3; 4-5: elif1-line4-5; 6-7: elif1-line6-7; 8-9: elif1-line8-9; 10-11: elif1-line10-11;
    :nocodelens:
    
    sayi = int (input ("1 ve 5 arasında bir sayı giriniz"))
    if sayi == "1": 
        print("Bir tehdit alacaksınız")
    elif sayi == "2"::
        print("Bir şeyinizi kaybedeceksiniz")
    elif sayi == "3":
        print("Yeni birisi ile tanışacaksınız")
    elif sayi == "4":
        print("Grip olacaksınız")
    else:
        print("Sınavdan çok yüksek not alacaksınız")
       
.. mchoice:: 13_4_3_fortune-elif-1_elif
   :answer_a: 1
   :answer_b: 2
   :answer_c: 5
   :answer_d: 6
   :correct: b
   :feedback_a: Yanlış. Önce girilen sayı 1 mi diye kontrol edecek, 1 olmadığı için bu sefer girilen sayı 2 mi diye kontrol etmesi gerekir   
   :feedback_b: Doğru. elif kullanıldığı için doğru olan durumdan sonrakiler kontrol edilmeyecektir.
   :feedback_c: Yanlış. Doğru yanıtı bulana kadar her bir elif  kontrol edilecektir, doğrudan sonrakiler ise göz ardı edilir.
   :feedback_d: Yanlış. Sadece 5 tane mantıksal ifade var o yüzden cevap 5’den daha fazla olamaz. 

   Kaç tane mantıksal ifade (logical expressions) kontrol edilecektir eğer kullanıcı 2 girerse?
   
.. tabbed:: 13_4_4_WSt_elif

        .. tab:: Soru

           Kullanıcıdan bir tam sayı alan ve sonra girilen değere göre uygun mesajı yazan bir program yaz. Kullanıcıya Türkiye’de kaç tane şehri gezdiğini sor ve 3 kategoride cevaplar hazırla. 
           
           .. activecode::  13_4_4_WSq_elif
               :nocodelens:

        .. tab:: Cevap
            
          .. activecode::  13_4_4_WSa_elif
              :nocodelens:
              
              sehirSayisi = int(input ("1 ile 5 arasında bir sayı giriniz"))
              if sehirSayisi <10 : 
                  print("Öğrencisin galiba?")
              elif sehirSayisi < 25:
                  print("Otostop yapmak bence de güzel bir şey")
              elif sehirSayisi < 81:
                  print("Hangi şirkette çalışıyorsunuz?")
              elif sehirSayisi == 81:
                  print("Evliya Çelebi ile bir akrabalığın var mı acaba?")
              else:
                  print("Türkiye’de sadece 81 şehir olduğunu bilmiyor olamazsın?")
                                



