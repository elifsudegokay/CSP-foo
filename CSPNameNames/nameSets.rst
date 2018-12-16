..  Copyright (C)  Mark Guzdial, Barbara Ericson, Briana Morrison
    Permission is granted to copy, distribute and/or modify this document
    under the terms of the GNU Free Documentation License, Version 1.3 or
    any later version published by the Free Software Foundation; with
    Invariant Sections being Forward, Prefaces, and Contributor List,
    no Front-Cover Texts, and no Back-Cover Texts.  A copy of the license
    is included in the section entitled "GNU Free Documentation License".

.. |bigteachernote| image:: Figures/apple.jpg
    :width: 50px
    :align: top
    :alt: teacher note

.. 	qnum::
	:start: 1
	:prefix: csp-6-5-
	
.. highlight:: java
   :linenothreshold: 4

Yordam ve Fonksiyonların Adlarını Belirleme
=========================================

So far we've seen names for values, like variables that hold strings and numbers.  Şimdiye kadar, dizeleri ve sayıları tutan değişkenler gibi değerler için isimler gördük. Ayrıca, işlevlerin veya prosedürlerin nasıl adlandırılacağını (tanımlandığını) ve girdileri bu işlevlere veya prosedürlere depolamak için ek adlar kullanabileceğimizi gördük.

Bazen, bir grup fonksiyona ve / veya prosedüre sahip olmak isteyeceksiniz ve bunları bir yerde saklamak ve tüm fonksiyon ve prosedürler dizisini adlandırmak isteyecek ve ihtiyaç duyacaksınız, aslında bunu daha önce yaptınız 

.. index::
	single: import, from import



.. activecode:: Squares_Pattern
  :tour_1: "Important lines tour"; 1-9: sqM-line1-9; 11-13: sqM-line11-13; 14: sqM-line14; 15: sqM-line15; 16: sqM-line16; 17: sqM-line17; 18: sqM-line18; 19: sqM-line19; 20: sqM-line20; 21: sqM-line21; 22: sqM-line22; 23: sqM-line23; 
  :nocodelens:

  from math import *
  def kare_hesapla(sayi):
      print ("Pi sayısının karesi",sayi*sayi);

  kare_hesapla(math.pi);

  #Pi sayısını math namespace’in alıyoruz. Daha sonra kare_hesapla fonksiyonu ile pi sayısının karesini alıyoruz.



.. activecode:: Squares_Patternns
  :tour_1: "Important lines tour"; 1-9: sqM-line1-9; 11-13: sqM-line11-13; 14: sqM-line14; 15: sqM-line15; 16: sqM-line16; 17: sqM-line17; 18: sqM-line18; 19: sqM-line19; 20: sqM-line20; 21: sqM-line21; 22: sqM-line22; 23: sqM-line23; 
  :nocodelens:

  from math import *
  def kare_hesapla(sayi):
      print ("Sayının karesi",sayi*sayi);

  sayi_al =int(input("Bir sayı giriniz"))
  kare_hesapla(sayi_al);


.. tabbed:: 6_5_2_WSt

        .. tab:: Soru

           sqrt fonksiyonunu kullanarak input ile alacağı sayının karekökünü hesaplayan bir fonksiyon yazınız.Tüyo : sqrt fonksiyonunu kullanmak için math namespace (isim uzayını) kullanmanız gerekmektedir.)
           
           .. activecode::  6_5_2_WSq
               :nocodelens:

	       

        .. tab:: Cevap

          .. activecode::  6_5_2_WSa
               :nocodelens:

	       import math #from math import * olarakta kullanabiliriz
	       def karekokHesapla(sayi):
		  print("Sayının karekökü",sqrt(sayi))

	       sayimiz = int(input("Lütfen sayı giriniz"))
	       karekokHesapla(sayimiz)
