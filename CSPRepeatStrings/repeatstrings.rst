..  Copyright (C)  Mark Guzdial, Barbara Ericson, Briana Morrison
    Permission is granted to copy, distribute and/or modify this document
    under the terms of the GNU Free Documentation License, Version 1.3 or
    any later version published by the Free Software Foundation; with
    Invariant Sections being Forward, Prefaces, and Contributor List,
    no Front-Cover Texts, and no Back-Cover Texts.  A copy of the license
    is included in the section entitled "GNU Free Documentation License".
    
.. |audiobutton| image:: Figures/start-audio-tour.png
    :height: 20px
    :align: top
    :alt: audio tour button

.. 	qnum::
	:start: 1
	:prefix: csp-9-1-
	
.. highlight:: java
   :linenothreshold: 4

Karakter Dizileri (String) İle Tekrarlama (Repetition) Kullanımı
==============================

*Öğrenme hedefleri:*

- Biriktirici *(accumulator)* modelinin, karakter dizileri için nasıl çalıştığını göstermek,
- Bir karakter dizisinin nasıl ters çevrileceğini (reverse – tersten yazmak) göstermek,
- Bir karakter dizisinin nasıl yansıtılacağını (mirror) göstermek,
- Bir karakter dizisini değiştirmek için (modify); while döngüsünün nasıl kullanılacağını göstermek. 

..	index::
	single: assignment
	pair: strings; assignment

.. index::
    single: words
    single: strings
	single: for loop

Python; bir önceki bölümde sayılar üzerinde oynama yapabilmemizi sağladığı gibi, kelimeler yani **karakter dizileri(string)** üzerinde oynama yeteneğine sahip yerleşik komutların kullanımını da sağlar. **Karakter dizisi (string)** ; harfleri, sayıları ve de diğer karakterleri içerebilir. Python’da ``for`` döngüsü; harflerin geçişinin nasıl olacağını ve karakter dizilerini birbirine nasıl ekleyeceğini (addition ( ``+`` )) bilir. Burada harika olan, aynı biriktirici (accumulator) modelinin çalışmasıdır. 

.. Python already has built in the ability to play with words or **strings**, just like how we played with numbers in the last chapter.  A **string** is a collection of letters, numbers, and other characters. A Python ``for`` loop knows how to step through letters, and addition (``+``) appends strings together. What's cool is that the same accumulator pattern works.

Bir hatırlatma olarak, biriktirici modelindeki 5 adım şu şekilde özetlenebilir:

.. As a reminder, here are the five steps in the accumulator pattern.

1. Biriktirici değişkenine kendi başlangıç değerini atayın. Eğer işlenecek veri-(ler) yoksa, istediğimiz değer bu olur.
2. İşlenecek tüm veri-yi-(leri) alın.
3. Bir ``for`` döngüsü kullanarak bütün veri-(ler) arasında bir geçiş yapın; bu sayede değişken, veri-(ler)-de bulunan her  bir değeri almış olur.
4. Veri-nin-(lerin) her bir parçasını biriktiriciye birleştirin (üzerine toplayın veya birleyin).
5. Elde ettiğiniz sonucu kullanarak yapmak istediğiniz işlemi gerçekleştirin.


.. 1. Set the accumulator variable to its initial value.  This is the value we want if there is no data to be processed.
.. 2. Get all the data to be processed.
.. 3. Step through all the data using a ``for`` loop so that the variable takes on each value in the data.
.. 4. Combine each *piece* of the data into the accumulator.
.. 5. Do something with the result.


Aşağıdaki programın nasıl çalıştığını görmek için |audiobutton| butonuna tıklayabilirsiniz.

.. activecode:: Copy_Words
    :tour_1: "Lines of code"; 2: strR1-line2; 4: strR1-line4; 6: strR1-line6; 8: strR1-line8; 10: strR1-line10;

    # ADIM 1: BİRİKTİRİCİYİ BAŞLATIN (BAŞLANGIÇ DEĞERİNE ATAYIN) 
    karakterDizisi = ""
    # ADIM 2: VERİ-Yİ-(LERİ) ALIN
    deyim = "Ağaç yaş iken eğilir."
    # ADIM 3: VERİ-(LER) ARASINDA GEÇİŞ
    for harf in deyim:
    	# ADIM 4: BİRİKTİRME İŞLEMİ
    	karakterDizisi = karakterDizisi + harf
    # ADIM 5: İŞLEMİN SONUCU
    print(karakterDizisi)

Programı çalıştırın. Bu pek de ilginç sayılmaz, öyle değil mi? Program sadece; ``deyim`` içinde yer alan bütün harfleri, ``karakterDizisi`` içerisine kopyalar.


.. Be sure to press the |audiobutton| to get an explanation for how this program works.

.. Copy_Words
..    :tour_1: "Lines of code"; 2: strR1-line2; 4: strR1-line4; 6: strR1-line6; 8: strR1-line8; 10: strR1-line10;

 ..  # STEP 1: INITIALIZE ACCUMULATOR 
  ..  newString = ""
 ..   # STEP 2: GET DATA
 ..   phrase = "Rubber baby buggy bumpers."
 ..   # STEP 3: LOOP THROUGH THE DATA
 ..   for letter in phrase:
 ..   	# STEP 4: ACCUMULATE
 ..   	newString = newString + letter
 ..   # STEP 5: PROCESS RESULT
 ..   print(newString)

.. Run this program.  Enh, not that interesting, eh?  It just copies all the letters from ``phrase`` to ``newString``.


