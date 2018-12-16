..  Copyright (C)  Mark Guzdial, Barbara Ericson, Briana Morrison
    Permission is granted to copy, distribute and/or modify this document
    under the terms of the GNU Free Documentation License, Version 1.3 or
    any later version published by the Free Software Foundation; with
    Invariant Sections being Forward, Prefaces, and Contributor List,
    no Front-Cover Texts, and no Back-Cover Texts.  A copy of the license
    is included in the section entitled "GNU Free Documentation License".

.. 	qnum::
	:start: 1
	:prefix: csp-12-1-
	
.. highlight:: python
   :linenothreshold: 3


Karar Verme İşlemleri
==================

*Öğrenme Hedefleri:*

- Karar verebilen programlar (uygulamalar) geliştirmek,
- ``if`` deyimi ile koşullu yürütmeleri öğrenmek,
- Mantıksal ifadeler ve ilişkisel işleçlere örnekler vermek,
- ``and``, ``or``, ve ``not`` ile karmaşık koşulları öğrenmek,
- Çoklu ``if`` deyiminin nasıl kullanıldığını ögrenmek,
- ``if`` ve ``else`` deyimlerini öğrenmek,
- Koşullar ile ilgili genel zorlukları incelemek. 


.. !!!!DİKKAT Bu paragraf farklı çevrildi. Biz bu kısmı çeviri yapılırken isimlendirmeden sonra işledik. Dolayısıyla döngülerden önce bu bölümü işlediğimiz için çeviride değişiklik yapıldı. 

Bilgisayarlarımızın önemli yeteneklerinden birini``değer(value)``lere isim verebilme (değişken) özelliğini öğrenmeiştik. Bilgisayarlarımızın bir diğer önemli yeteneği ise **karar verebilme** özelliğidir. Bizler her zaman belli kararlar alırız. Örnek olarak, evden çıkmadan önce, o gün yağmur yağıp yağmayacağını kontrol edip, eğer yağacaksa yanımıza şemşiye almamız.

.. We have discussed two major abilities that computers have.  Computers can name values.  Computers can repeat steps.  The third major ability that a computer has is the ability to make decisions.  We make decisions all the time.  Before we leave the house we may check to see if it will rain that day, and if it will, we bring an umbrella.

.. figure:: Figures/umbrella.jpg
    :height: 200px
    :align: center
    :alt: Picture of an umbrella
    :figclass: align-center

    Figure 1: An umbrella in the rain


Bilgisayar sadece verileri (örn Değişken değerleri) ``True (doğru)`` ise karar verebilir veya başka bir işlem yapabilir. Daha detaylı olarak, (1) bilgisayar bir **veriyi test eder** ve (2) bu test sonucu doğru ise **talimatları uygular**. Veriyi test etme ve sonuca göre işlem yapma yeteneği, bilgisayarın anlayabileceği bir veriyi test etmesi ve bunun üzerine işlemler yapmasıdır. (örn. Eğer kredi kartınız geçerli ile karttan para çekilmesi veya dur işareti gördüğümüzde durmamız gibi.

.. Computers can also make decisions or take action when something is true.  More specifically, (1) a computer can *test data* and (2) a computer can *execute instructions* if that test is true.  The ability to test data and take actions on the result is what allows the computer to deal with input and take action on it (e.g., if the credit card is valid then charge the card), or deal with data from the world around (e.g., if I see a stop sign then stop.).

.. figure:: Figures/stop.jpg
    :height: 200px
    :align: center
    :alt: Picture of a stop sign
    :figclass: align-center

    Figure 2: Picture of a stop sign
    
..	index::
	single: conditional execution
	
Bilgisayar’ın bir işlem sonucu doğru olduğunda harekete geçme (bazı kodları çalıştırarak) yeteneği **koşullu yürütme (conditional execution)** olarak adlandırılır.

.. The computer's ability to take action (execute some code) when something is true is also called **conditional execution**.  


