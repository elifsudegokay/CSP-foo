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
	:prefix: csp-9-2-
	
.. highlight:: java
   :linenothreshold: 4

Metni Ters Çevirmek
================

Bir sonraki kodu çalıştırın ve koddaki küçük bir değişikliğin ne kadar farklı sonuçlar verdiğini görün. Bu örnekte 4. adımda kelimleri *sona eklemek* ve *başa eklemek* arasındaki farkı ve bunun sonuçlarını göreceğiz.

.. Run this next one, and look at how a simple change to the pattern gives a very different result.    Here we'll combine *before* rather than *afterward*, changing only Step 4 (how values are accumulated).

.. activecode:: Copy_Reverse
    :tour_1: "Lines of code"; 2-3: strR2-line2-3; 5: strR2-line5; 7: strR2-line7; 9: strR2-line9; 10: strR2-line10; 12: strR2-line12; 13: strR2-line13; 14: strR2-line14; 15: strR2-line15;
	
    # 1. ADIM: BİRİKTİRİCİYE BAŞLANGIÇ DEĞERİNİ KOY
    yeniKarakterDizisi1 = ""
    yeniKarakterDizisi2 = ""
    # 2. ADIM: VERİYİ AL
    kelimeler = "İyi ki doğdun!"
    # 3. ADIM: DÖNGÜYÜ KULLAN
    for harf in kelimeler:
    	# 4. ADIM: BİRİKTİR
      	yeniKarakterDizisi1 = harf + yeniKarakterDizisi1
      	yeniKarakterDizisi2 = yeniKarakterDizisi2 + harf
    # 5. ADIM: SONUCU BASTIR
    print("harf + yeniKarakterDizisi1 şeklinde kullanmanın sonucu:")
    print(yeniKarakterDizisi1)
    print("yeniKarakterDizisi2 + harf şeklinde kullanmanın sonucu:")
    print(yeniKarakterDizisi2)

.. mchoice:: 9_2_1_Copy_Reverse_Q1
   :answer_a: Çünkü her harfi <code>yeniKarakterDizisi1</code> değişkeninin başına ekledik.
   :answer_b: Çünkü <code>yeniKarakterDizisi2</code> karakterleri soldan sağa ekliyor.
   :answer_c: Çünkü ters çevirme fonksiyonu çağırdık.
   :answer_d: Çünkü <code>for</code>  döngüsü tersten işliyor.
   :correct: a
   :feedback_a: Doğru. Her harfin başa eklenmesi terse çevirme durumu yaratır
   :feedback_b: Yanlış. yeniKarakterDizisi2’deki değişiklik neden yeniKarakterDizisi1’i etkilesin ki?
   :feedback_c: Yanlış. Bu programda her hangi bir ters çevirme programı yok.
   :feedback_d: Yanlış. Aynı <code>for</code> döngüsü hem tersten hem de düzden bastırmayı aynı anda sağlıyor dolayısıyla döngü iki durum için de aynı, özel bir şey yapmıyor.

   Sizce neden ``yeniKarakterDizisi1`` bütün harflere tersten sahip?

.. tabbed:: 9_2_2_WSt

        .. tab:: Soru

           “şeker” dizgisi ile palindrom yapan bir program yazın. Palindrom baştan ve sondan okunduğunda aynı olan kelimeye denir. Örneğin: *elmaamel*, *ey edip adanada pide ye*, *al yarısını sırayla*

           .. activecode::  9_2_2_WSq
                :nocodelens:

        .. tab:: Cevap
            
          .. activecode::  9_2_2_WSa
              :nocodelens:
              
              # BİRİKTİRİCİYE BAŞLANGIÇ DEĞERİNİ KOY
              yeniKarakterDizisi1= ""
              yeniKarakterDizisi2 = ""
              # KELİMEYİ GİR
              kelime= "şeker"
              #  DÖNGÜYÜ KULLAN
              for harf in kelime:
                # SONUCU BİRİKTİR
                  yeniKarakterDizisi1 = harf + yeniKarakterDizisi1
                  yeniKarakterDizisi2 = yeniKarakterDizisi2 + harf
              # SONUCU BASTIR
              print("Verdiğiniz dizgiden palindrom yapılmış hali:")
              print(yeniKarakterDizisi2 + yeniKarakterDizisi1)
                



..  Copy_Reverse
    :tour_1: "Lines of code"; 2-3: strR2-line2-3; 5: strR2-line5; 7: strR2-line7; 9: strR2-line9; 10: strR2-line10; 12: strR2-line12; 13: strR2-line13; 14: strR2-line14; 15: strR2-line15;
	
..     # STEP 1: INITIALIZE ACCUMULATORS
..     newStringA = ""
..     newStringB = ""
..     # STEP 2: GET DATA
..     phrase = "Happy Birthday!"
..     # STEP 3: LOOP THROUGH THE DATA
..     for letter in phrase:
 ..    	# STEP 4: ACCUMULATE
 ..      	newStringA = letter + newStringA
..       	newStringB = newStringB + letter
..     # STEP 5: PROCESS RESULT
 ..    print("Here's the result of using letter + newStringA:")
 ..    print(newStringA)
..     print("Here's the result of using newStringB + letter:")
 ..    print(newStringB)

.. 9_2_1_Copy_Reverse_Q1
..    :answer_a: Because we add each new letter at the <i>end</i> of <code>newStringB</code>.
 ..   :answer_b: Because <code>newStringA</code> is adding the characters from left to right.
..    :answer_c: Because we called a reverse function.
..    :answer_d: Because the <code>for</code> loop is doing a reversal
..    :correct: a
 ..   :feedback_a: Each new letter gets added at the end, which creates a reversal.
..    :feedback_b: How would that reverse the other string?
..    :feedback_c: There is no reverse function in this program.
..    :feedback_d: The same <code>for</code> loop is creating both an in-order copy of the string and a reversed order of the string.  The <code>for</code> loop is the same in both cases.

..    Why do you think ``newStringB`` has all the letters, but in the reverse order?

.. ..  9_2_2_WSt

        .. 

..            Write the code to make a palindrome with the string "popsicle". Palindromes read the same foward and backwards. Example: appleelppa

           ..  9_2_2_WSq
                :nocodelens:

..         .. Answer
            
          ..  9_2_2_WSa
              :nocodelens:
              
..               # INITIALIZE ACCUMULATORS
 ..              newStringA = ""
..               newStringB = ""
..               # NAME DATA
..               word = "popsicle"
..               # LOOP THROUGH THE DATA
..               for letter in word:
 ..                # ACCUMULATE RESULT
 ..                  newStringA = letter + newStringA
   ..                newStringB = newStringB + letter
    ..           # DISPLAY RESULT
    ..           print("Here's the result of using newStringB + letter:")
     ..          print(newStringB + newStringA)    

