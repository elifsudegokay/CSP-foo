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
	:prefix: csp-9-3-
	
.. highlight:: java
   :linenothreshold: 4

Metni Yansıtma
===============

Eğer harf'i yeni oluşturduğumuz karakter dizisinin (String) her *hem başına hem sonuna* eklersek ne yapmış oluruz ? 

.. What happens if we add the letter to *both* sides of the new string that we're making?

.. activecode:: Copy_Mirror
    :tour_1: "Lines of code"; 2: strR3-line1; 4: strR3-line2; 6: strR3-line3; 8: strR3-line4; 10: strR3-line5;
	
    # ADIM 1: BİRİKTİRİCİYİ BAŞLATIN (BAŞLANGIÇ DEĞERİNE ATAYIN) 
    karakterDizisi = ""
    # ADIM 2: VERİ-Yİ-(LERİ) ALIN
    cumle = "Bu bir deneme"
    # ADIM 3: VERİ-(LER) ARASINDA GEÇİŞ
    for harf in cumle:
      	# ADIM 4: BİRİKTİRME İŞLEMİ
      	karakterDizisi = harf + karakterDizisi + harf
    # ADIM 5: İŞLEMİN SONUCU
    print(karakterDizisi)


``cumle`` 'yi değiştirmeyi deneyin ve kodun nasıl çalıştığını anlamaya çalışın. 

.. Try changing the phrase and see what effects you can generate.

.. mchoice:: 9_3_1_Copy_Mirror_Q1
   :answer_a: cumle değişkeninin değerini <code>“Panikleme zamanı!”</code> olarak değiştiririz.
   :answer_b: karakterDizisi değişkeninin 1.karakterini <code>“!”</code> olarak değiştiririz.
   :answer_c: 4 karakter girintili “Indent” yazdığımız bölümü <code>harf + “!” + karakterDizisi + harf</code> olarak değiştiririz.
   :answer_d: 4 karakter girintili “Indent” yazdığımız bölümü <code> harf + karakterDizisi + “!” + harf </code> olarak değiştiririz.
   :correct: b
   :feedback_a: Yanlış. Ekran çıktısı : “!ınamaz emelkinaPPanikleme zamanı!” olacaktır.
   :feedback_b: Doğru. Yansıtma için kullanacağımız değişkenimize başlangıçta bir değer atabiliriz.
   :feedback_c: Yanlış. Bu değişiklik bize “ı!n!a!m!a!z! !e!m!e!l!k!i!n!a!P!Panikleme zamanı” ekran çıktısını vermektedir. Yansıma bölümünde bütün harflerin arasında ! işareti eklenecektir.
   :feedback_d: Yanlış. Bu değişiklik bize “ınamaz emelkinaP!P!a!n!i!k!l!e!m!e! !z!a!m!a!n!ı” ekran çıktısını vermektedir, Yansıma doğru olmasına karşın düz metin olan metin bölümünde harflerin arasına ! işareti eklenecektir.

   Yansıtıcı programı değiştirerek  ekran çıktısının ``"Panikleme zamanı"`` cümlesini ortada tek bir ünlem işaretiyle  yansıtmak için yazınız. Yani sonuç ``"ınamaz emelkinaP!Panikleme zamanı"`` şeklinde olmalıdır. Bunu nasıl yaparsın?


Biriktirici değişkenin boş bir karakter dizisi olarak tanımlanması zaruri değildir. Biriktirici değişkene atadığınız herhangi bir değer, yansıyan cümlenin ortasında görüntülenecektir.

.. The accumulator doesn't have to be set to be an empty string.  You can put something in the accumulator, and then it will show up in the middle of the mirrored phrase.

.. codelens:: Char_In_Middle

    yeniKarakterDizisi = "!"
    cumle = "Unutma Red, umut iyidir, belki de en iyisi"
    for harf in cumle :
        yeniKarakterDizisi = harf + yeniKarakterDizisi + harf
    print(yeniKarakterDizisi)

.. mchoice:: 9_3_2_Count_Exclamations_Q1
   :answer_a: Bir
   :answer_b: İki
   :answer_c: Üç
   :answer_d: Dört
   :correct: a
   :feedback_a: Doğru. Sadece başlangıçta 1 tane bulunuyor.
   :feedback_b: Yanlış. Sadece karakter dizisini yansıtsaydık iki tane olurdu, Ama harfleri birleştirdiğimiz değişkenimizle yansıtma işlemi yapıyoruz.
   :feedback_c: Yanlış. Program sonlandığında bu sonuç doğrudur ama ``Red`` kelimesinin ilk harfinden söz ediyoruz.
   :feedback_d: Yanlış. Program sonlandığında yeniKarakterDizisi değişkeninde toplam 3 adet ünlem bulunmaktadır.

    ``harf`` değişkeni ``Red'`` 'deki ``"R"`` değerini aldığında, ``yeniKarakterDizisi`` değişkeninde kaç tane ünlem işareti olur?

.. parsonsprob:: 9_3_3_Palindrome

   <p> ``AÇ RIFAT’A FIRÇA`` cümlesi bir palindromdur. Palindrom cümleler ters veya düz olarak okunduğunda aynı olan cümlelerdir. Aşağıdaki program çıktısını ``AÇRIF A’TAFIR ÇA<=>AÇ RIFAT’A FIRÇA`` olacak şekilde kod satırlarını sıralayın.</p>
   -----
   yeniKarakterDizisi = "<=>"
   cumle = "AÇ RIFAT’A FIRÇA"
   =====
   for harf in cumle:
   =====
       yeniKarakterDizisi = harf + yeniKarakterDizisi + harf
   =====
   print(yeniKarakterDizisi)




..  9_3_1_Copy_Mirror_Q1
..   :answer_a: Make the phrase <code>"Time to panic!"</code>
..   :answer_b: Change the <code>newString</code> in line 1 to <code>"!"</code> instead of <cod>""</code>
..   :answer_c: Change the right hand side of line 4 to <code>letter + "!" + newstring + letter</code>
..   :answer_d: Change the right hand side of line 4 to <code>letter + newstring + "!" + letter</code>
..   :correct: b
..   :feedback_a: That would give us <code>!cinaP ot emiTTime to Panic!</code>.
..   :feedback_b: We can start our accumulator with something in it.
..   :feedback_c: That would give us <code>!!c!i!n!a!P! !o!t! !e!m!i!T!Time to Panic!</code> -- exclamation points between the letters in the first half of the mirror.
..   :feedback_d: That would give us <code>!cinaP ot emiT!T!i!m!e! !t!o! !P!a!n!i!c!!</code> -- exclamation points between the letters in the second half of the mirror.

..   Change the mirroring program to mirror the phrase ``"Time to Panic"`` with a single exclamation point in the middle, to make the printed words look like this: ``cinaP ot emiT!Time to Panic``.  How do you do it?

.. The accumulator doesn't have to be set to be an empty string.  You can put something in the accumulator, and then it will show up in the middle of the mirrored phrase.

.. : Char_In_Middle

 ..   newString = "!"
 ..   phrase = "We're off to see the Wizard!"
..    for letter in phrase:
 ..       newString = letter + newString + letter
 ..   print(newString)

.. 9_3_2_Count_Exclamations_Q1
..   :answer_a: One
..   :answer_b: Two
..   :answer_c: Three
..   :answer_d: Four
..   :correct: a
..   :feedback_a: There is just the one in the accumulator to start.
..   :feedback_b: If we just mirrored the string, there would be only two.  But we are mirroring with something in the accumulator.
 ..  :feedback_c: That is true at the end, but not when letter contains the first letter of <code>"Wizard"</code>
..   :feedback_d: At most, there will be three in <code>newString</code>.

..   When the variable ``letter`` contains the ``"W"`` from ``Wizard``, how many exclamation points are in ``newString``?

.. : 9_3_3_Palindrome

..   <p>The phrase <code>"A but tuba"</code> is a <b>palindrome</b>.  The letters are the same forward and backward.  The below program generates the output: <code>"abut tub a<=>a but tuba"</code>  Put the lines in the right order with the right indentation.</p>
..   -----
..  newStr = "<=>"
..   phrase = "a but tuba"
..   =====
..   for char in phrase:
..   =====
..       newStr = char + newStr + char
..   =====
..   print(newStr)

