..  Copyright (C)  Mark Guzdial, Barbara Ericson, Briana Morrison
    Permission is granted to copy, distribute and/or modify this document
    under the terms of the GNU Free Documentation License, Version 1.3 or
    any later version published by the Free Software Foundation; with
    Invariant Sections being Forward, Prefaces, and Contributor List,
    no Front-Cover Texts, and no Back-Cover Texts.  A copy of the license
    is included in the section entitled "GNU Free Documentation License".

.. 	qnum::
	:start: 1
	:prefix: csp-6-4-

Parametreleri İsimlendirme
================

Peki tekerleme oyununda bir yerden sonra farklı bir tekerleme söylenmesini isteseydik ne yapmalıydık ? ``cumle`` parametresine girilen değeri kod içinde değiştirmemiz gerekirdi.

.. activecode:: Function_Change_Size
  :tour_1: "Important lines tour"; 1-9: sq50-line1-9; 2,4,6,8: sq50-line2468; 11-13: sq50-line11-13; 14: sq50-line14; 
  :nocodelens:

  def tekerleme(cumle):
    print("Hadi biraz eğlenelim 🕺🕺🕺")
    print(cumle * 2)
    cumle="Bir tas has hoşaf" + "\n"
    print("Hadi ama daha iyisini yaparsın 😉")
    print(cumle * 3)
    cumle = "Şu yoğurdu sarımsaklasak da mı saklasak" + "\n"
    print("Zorlanmaya başladın galiba 😎")
    print(cumle * 4)
    cumle = "Çatalca'da topal çoban çatal yapıp çatal satar" + "\n"
    print("Çok iyi gidiyorsun 🎯")
    print(cumle * 5)
    print("Bravo 👏 🏆 👏")

  tekerlemeCumlesi = "dal sarkar kartal kalkar\n"
  tekerleme(tekerlemeCumlesi)


 
Ama bu ``cumle``'nin değerini değiştireceğimiz yani kaybedeceğimiz anlamına gelir. Yanlışlıkla değeri kaybedersek hata yapabiliriz. Daha iyi bir yol var mı? ``cumle`` parametresini isimlendirmeye ne dersin? 



.. activecode:: Function_Add_Var
  :tour_1: "Important lines tour"; 1-10: sqvar-line1-10; 2: sqvar-line2; 3: sqvar-line3; 4: sqvar-line4; 5-10: sqvar-line5-10; 12-14: sqvar-line12-14; 15: sqvar-line15;
  :nocodelens:

  def tekerleme(cumle):
    Tekerleme = cumle
    print("Hadi biraz eğlenelim 🕺🕺🕺")
    print(Tekerleme * 2)
    Tekerleme = "Bir tas has hoşaf"
    print("Hadi ama daha iyisini yaparsın 😉")
    print(Tekerleme * 3)
    print("Başka bildiğin tekerleme var mı? ")
    Tekerleme = "Şu yoğurdu sarımsaklasak da mı saklasak" + "\n"
    print("Zorlanmaya başladın galiba 😎")
    print(Tekerleme * 4)
    Tekerleme = "Çatalca'da topal çoban çatal yapıp çatal satar" + "\n"
    print("Çok iyi gidiyorsun 🎯")
    print(Tekerleme * 5)
    print("Bravo 👏 🏆 👏")

  tekerlemeCumlesi = "dal sarkar kartal kalkar\n"
  tekerleme(tekerlemeCumlesi)


.. mchoice:: 6_4_1_Function_Var_Q1
   :answer_a: dal sarkar kartal kartar
   :answer_b: Bir tas has hoşaf
   :answer_c: Çatalca'da topal çoban çatal yapıp çatal satar
   :answer_d: Şu yoğurdu sarımsaklasak da mı saklasak
   :correct: a
   :feedback_a: Doğru.Çünkü cumle parametresine girilen argümanın değerini kaybetmedik.
   :feedback_b: Yanlış. Kodu çalıştırıp denemek ister misin? 
   :feedback_c: Yanlış. Kodu çalıştırıp denemek ister misin? 
   :feedback_d: Yanlış. Kodu çalıştırıp denemek ister misin? 

   Aşağıdaki yordamı ``tekerleme("dal sarkar kartal kartar")`` olarak çağırırsaak ekrana ``Bravo 👏 🏆 👏`` 'dan önce ne yazar
   
   :: 
 
     def tekerleme(cumle):
     	Tekerleme = cumle
    	print("Hadi biraz eğlenelim 🕺🕺🕺")
    	print(Tekerleme * 2)
    	Tekerleme = "Bir tas has hoşaf"
    	print("Hadi ama daha iyisini yaparsın 😉")
    	print(Tekerleme * 3)
    	print("Başka bildiğin tekerleme var mı? ")
    	Tekerleme = "Şu yoğurdu sarımsaklasak da mı saklasak" + "\n"
    	print("Zorlanmaya başladın galiba 😎")
    	print(Tekerleme * 4)
    	Tekerleme = "Çatalca'da topal çoban çatal yapıp çatal satar" + "\n"
    	print("Çok iyi gidiyorsun 🎯")
    	print(Tekerleme * 5)
    	Tekerleme = cumle
    	print(Tekerleme)
    	print("Bravo 👏 🏆 👏")

Şimdi programı değiştirmenin daha kolay olduğunu fark ettin mi ? Farklı tekerlemeler için yapman gereken "Tekerleme'nin değerini değiştirmek 

Programmıza birden fazla parametre ekleyebiliriz. Yordam isminden ``(`` ve ``)`` arasına parametre isimlerini virgüllerle ayırarak çok parametreli yordamlar ya da fonksiyonlar yazabiliriz. Örneğin: ``tekerleme(cumle1, cumle2, cumle3)``


.. activecode:: Function_Call2
  :tour_1: "Important lines tour"; 1-9: dsq3-line1-9; 2: dsq3-line2; 11-13: dsq3-line11-13; 14: dsq3-line14; 15: dsq3-line15; 16: dsq3-line16; 17: dsq3-line17;
  :nocodelens:

  def tekerleme(cumle1, cumle2, cumle3, cumle4):
    	print("Hadi biraz eğlenelim 🕺🕺🕺")
    	print(cumle1 * 2)
    	print("Hadi ama daha iyisini yaparsın 😉")
    	print(cumle2 * 3)
    	print("Zorlanmaya başladın galiba 😎")
    	print(cumle3 * 4)
    	print("Çok iyi gidiyorsun 🎯")
    	print(cumle4 * 5)
    	print("Bravo 👏 🏆 👏")

  tek1 = "dal sarkar kartal kalkar" + "\n"
  tek2 = "Bir tas has hoşaf" + "\n"
  tek3 = "takatukaları takatukacıya takatukalatmaya götür" + "\n"
  tek4 = "O pikap, şu pikap, bu pikap" + "\n"
  tekerleme(tek1, tek2, tek3, tek4)

.. index:: 
	single: arguments
.. index:: 
	single: actual parameters
.. index:: 
	single: parameters
.. index:: 
	single: formal parameters
	pair: parameters; formal
	pair: parameters; actual
  
İşlev ve yordamların girdilerine **parametre (parameters)** ya da **biçimsel parametre (formal parameters)** denmektedir. Yani ``cumle1`` , ``cumle2`` , ``cumle3`` ve ``cumle4`` ;   ``tekerleme`` yordamının biçimsel parametreleridir. İşlevi ya da yordamı çağırırken kullandığımız değerlere ``tek1`` , ``tek2`` , ``tek3`` ve ``tek4`` ise **argüman ya da gerçek parametre** denir.

.. mchoice:: 6_4_3_Name_Args_Q1
   :answer_a: isim ve soyisim
   :answer_b: Ara ve Güler
   :answer_c: isim, soyisim, Ara, Güler
   :correct: b
   :feedback_a: Yanlış. Bunlar parametrelerin isimleri. (Bknz: Biçimsel Parametre )
   :feedback_b: Doğru. Bunlar argümanların yani gerçek parametrelerin isimleri
   :feedback_c: Yanlış. Parametre ve argüman isimleri bir arada verilmiş. Biz sadece argüman isimlerini belirtmeliyiz. 

   Aşağıdaki işlevin argümanları  (gerçek parametre) nedir?  
   
   :: 
 
     def selam(isim, soyisim)
         print("Merhaba " + "isim" + " " + soyisim)

     selam("Ara", "Güler")
     
.. parsonsprob:: 6_4_4_Draw_Squares

   Aşağıdaki program 0'dan ona argüman olarak verilen değere kadar olan sayıların toplamını bulmayı amaçlamaktadır.  Kod bloklarını doğru sırada olacak şekilde gerekli kodları sağ tarafa sürükleyin. Yordama ait deyimlerin girintili yazıldığını ve giritili kısımların daha sağda olması gerektiğini unutmayın. 
   -----
   def toplam(sayi)   
   ===== 		
       sonuc = ((sayi * (sayi +1)) / 2) 		
   =====
       return sonuc
   

