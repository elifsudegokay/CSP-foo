..  Copyright (C)  Mark Guzdial, Barbara Ericson, Briana Morrison
    Permission is granted to copy, distribute and/or modify this document
    under the terms of the GNU Free Documentation License, Version 1.3 or
    any later version published by the Free Software Foundation; with
    Invariant Sections being Forward, Prefaces, and Contributor List,
    no Front-Cover Texts, and no Back-Cover Texts.  A copy of the license
    is included in the section entitled "GNU Free Documentation License".

.. |runbutton| image:: Figures/run-button.png
    :height: 20px
    :align: top
    :alt: run button

.. |audiobutton| image:: Figures/start-audio-tour.png
    :height: 20px
    :align: top
    :alt: audio tour button

.. |codelensfirst| image:: Figures/codelens-first.png
    :height: 20px
    :align: top
    :alt: move to first button

.. |codelensback| image:: Figures/codelens-back.png
    :height: 20px
    :align: top
    :alt: back button

.. |codelensfwd| image:: Figures/codelens-forward.png
    :height: 20px
    :align: top
    :alt: forward (next) button

.. |codelenslast| image:: Figures/codelens-last.png
    :height: 20px
    :align: top
    :alt: move to last button
    
.. 	qnum::
	:start: 1
	:prefix: csp-3-5-

.. highlight:: java
   :linenothreshold: 4

İstanbuldan İzmir’e Araç ile Gitmek
====================================

..	index::
	single: CodeLens
	
Örnek olarak İstanbuldan İzmire araç ile gitmeyi planladığınızı düşünün. Eğer aracınızın kilometre başına kullandığı benzin miktarını ve gideceğiniz mesafeyi biliyorsanız, harcayacağınız benzin miktarını tahmin edebilirsiniz.

*CodeLens*  kullanarak aşağıdaki kodun bilgisayarınızın nasıl çalıştırğını adım adım izleyebilirsiniz:

- |codelensfwd| butonuna tıklayarak programın sonraki satırını çalıştırabilirsiniz.
- |codelenslast| butonuna tıklayarak programın bütün satırlarını çalıştırabilirsiniz

.. codelens:: Chicago_2_Dallas

   mesafe = 477
   kmBasinaKullanim = 0.055	#100 Km'de 5.5 Lt
   harcanacakBenzin = mesafe * kmBasinaKullanim
   
..	index::
	single: camel case

İstanbuldan İzmir’e giderken harcayacağımız benzin miktarını biliyoruz. Artık İstanbuldan İzmir’e araçla gitmenin maliyetini hesaplayabiliriz.  

.. Note::

   Aşağıda bulunan kod bloğunda ``benzinFiyati`` ve ``seyahatMaliyeti`` değişkenlerimiz bulunuyor. Değişken isimleri boşluk bırakılmadan birleşik olarak yazılmalıdır. Değişkenlerin daha rahat okunabilmesi için birden çok kelime içeren değişken isimleri kullanabilir bu durumda değişken isminin ilk harf küçük sonraki kelimelerin ilk harfleri büyük olarak yazabiliriz, Bu tarz yazım şekline camel case denmektedir. Python dilinde büyük küçük harf hassasiyeti bulunmaktadır yani ``benzinFiyati`` ve ``benzinfiyati`` bir birinden farklıdır.   

.. codelens:: Chicago_2_Dallas_Cost

   mesafe = 477
   kmBasinaKullanim = 0.055	#100 Km'de 5.5 Lt
   harcanacakBenzin = mesafe * kmBasinaKullanim
   benzinFiyati = 6.93
   seyahatMaaliyeti = harcanacakBenzin * benzinFiyati
   
..	index::
	single: tracing
	single: string
	single: print
	pair: programming; tracing
	
Yaptığımız işlem programın işlenen bütün satırlarının  incelenmesidir(**tracing**). Normal olarak programı çalıştırdığımızda (**run butonuna bastığımızda**) bilgisayara bütün satırları olabildiğinde hızlı olarak çalıştırmasını söyleriz. Bunu yaptığımızda  Programı çalıştırdığı süreçleri göremeyiz. Yaptığımız işlemi görebilmek için ``print`` komutu ile ekrana çıktı vermesini sağlayabiliriz. Aynı zamanda değişken değerlerini kontrol için de kullanabiliriz. print fonksiyonu parantezlerin içine *veri girdileri (input)* yaparak kullanılır. Programımızda kullanmakta olduğumuz değişkenleri aynı şekilde print fonksiyonun içine parantezler içinde yazabiliriz. Print fonksiyonuna **string** (karakter dizisi) ekleyerek kullanıcılara daha anlaşılır ekran *çıktıları(output)* verebiliriz.

|runbutton| butonuna tıklayarak programın en hızlı şekilde çalıştırabilirsiniz.

.. activecode:: Trip_Calculator
   :tour_1: "Line by line tour"; 1: trp-line1; 2: trp-line2; 3: trp-line3; 4: trp-line4; 5: trp-line5; 6: trp-line6; 7: trp-line7; 

   mesafe = 477
   kmBasinaKullanim = 0.055	#100 Km'de 5.5 Lt
   harcanacakBenzin = mesafe * kmBasinaKullanim
   benzinFiyati = 6.93
   seyahatMaaliyeti = harcanacakBenzin * benzinFiyati
   print("İstanbul'dan İzmir'e Yolculuk Maaliyeti:")
   print(seyahatMaaliyeti)

Bu programın nasıl çalıştığını |audiobutton| butonuna basarak sesli olarak dinleyebilirsiniz. (İngilizce)

Programı değiştirerek aşağıdaki soruları cevaplayın.

.. mchoice:: 3_5_1_Chicago_2_Dallas_Q1
   :answer_a: Evet
   :answer_b: Hayır
   :answer_c: Uçmayı deneyebiliriz.
   :correct: a
   :feedback_a: Evet,yeni ulaşım maliyetiniz 170.52 TL olacaktır. (Programı değiştirip çalıştıra tıklayıp aldığınız sonuç)
   :feedback_b: Tekrar dene – 6.50 6.93 den küçüktür..
   :feedback_c: Haklı olabilirsin ama programı değiştirip maliyeti bulmayı dene

   Eğer benzin fiyatını 6.50 TL ye düşürürsek, İstanbuldan İzmire ulaşım maliyetini 180 TL’nin altına indirebilirmiyiz?
   
.. mchoice:: 3_5_2_Chicago_2_Dallas_Q2
   :answer_a: 6.50
   :answer_b: 6.93
   :answer_c: benzinFiyati
   :correct: c
   :feedback_a: Eğer print fonksiyonuna değişken doğru biçimde yazılsaydı doğru olabilirdi.
   :feedback_b: Eğer önceki soru için değişken değerini değiştirdiysen ve print fonksiyonunu düzelttiysen doğru olabilir.
   :feedback_c: Doğru. print fonksiyonunda değişken adının başına ve sonuna “ eklendiği için ekran çıktısı böyle görenecektir. Değişkenin değerini alabilmek için tırnakları kaldırmalısın.

   Eğer kod bloğunun en sonuna ``print("benzinFiyati")`` kodunu eklersek ekran çıktısı ne olur ?


