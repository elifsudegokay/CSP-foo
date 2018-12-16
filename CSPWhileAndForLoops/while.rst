..  Copyright (C)  Mark Guzdial, Barbara Ericson, Briana Morrison
    Permission is granted to copy, distribute and/or modify this document
    under the terms of the GNU Free Documentation License, Version 1.3 or
    any later version published by the Free Software Foundation; with
    Invariant Sections being Forward, Prefaces, and Contributor List,
    no Front-Cover Texts, and no Back-Cover Texts.  A copy of the license
    is included in the section entitled "GNU Free Documentation License".

.. 	qnum::
	:start: 1
	:prefix: csp-8-4-
	
.. highlight:: java
   :linenothreshold: 4


.. Looping When We Don't Know When We'll Stop
Ne Zaman Duracağımızı Bilmediğimizde Döngü
============================================

While döngüleri genellikle, döngünün kaç kez tekrarlanması gerektiğini bilmediğimizde kullanılır. İfade doğru olduğu sürece döngünün gövdesi tekrarlanır. Mantıksal ifade, döngü gövdesi tekrarlamadan hemen önce hesaplanır.



.. While loops are typically used when you don't know how many times the loop needs to repeat.  The body of the loop will repeat while the condition is true.  The logical expression will be evaluated just before the body of the loop is repeated.  


Bir sayının karekökünü bulmak istediğimizi varsayalım. Bazı karekök değerleri için tam net değerler bulamayacaksınız. Kendisiyle çarpılan bir karekök bulmak istediğimizi söyleyelim ki istediğimiz değerin 0.01’lik bir sapmanın içerisinde olsun. Bunu nasıl yaparız? Burada uygulayabileceğimiz çok eski bir süreç var:

.. Let's say that we want to find the square root of a number.  For some square roots, you're never going to be exact.  Let's say that we want to find a square root that, when multiplied by itself, is within `0.01` of the square we want.  How do we do it?  There's a really old process that we can apply here.


1. Tahmin `2` olsun.
2. Tahmininizin karesini alın.
3. Tahmininizin karesi hedefe yakın mı? Eğer bu farkları 0.01’lik sapmanın içindeyse buldunuz. Aşılması durumunda farkın mutlak değerin alacağız .(Python'da mutlak değer hesaplamak için ``abs`` (absolute value function) kullanırız.)
4. Yeterince yakın değilse, hedef sayıyı tahminimize böleriz, o zaman tahminimizle o değeri ortalarız.
5. Bu bizim yeni tahminimiz. Karesini al ve Adım #3 'e geri dön

.. 1. Start by guessing `2`.
.. 2. Compute the guess squared.
.. 3. Is the guess squared close to the target number?  If it's within `0.01`, we're done.  We'll take the absolute value of the difference, in case we overshoot. (In Python, ``abs`` is the absolute value function.)
.. 4. If it's not close enough, we divide the target number by our guess, then average that value with our guess.
.. 5. That's our new guess.  Square it, and go back to Step #3.


İşte tam olarak bunu yapan bir program aşağıda. Farklı hedef değerleri deneyin ve böylece bilgisayarın karekök hesaplamada ne kadar iyi olduğunu görün.

.. Here's a program that does exactly that.  Try different `target` values, and see how good it is at computing square roots.

.. activecode:: Square_Root
  :tour_1: "Line by line tour"; 1: sqR_line1; 2: sqR_line2; 3: sqR_line3; 4: sqR_line4; 5: sqR_line5; 6: sqR_line6; 7: sqR_line7; 8: sqR_line8;

  hedef = 6
  tahmin  = 2
  tahminKare = tahmin * tahmin
  while abs(hedef- tahminKare) > 0.01:
      yakinsa = hedef / tahmin
      tahmin = (tahmin + yakinsa) / 2.0
      tahminKare = tahmin * tahmin
  print(hedef, "’in karekökü: ", tahmin)




.. mchoice:: 8_4_1_Square_Root_Q1
  :answer_a: Döngü içinde hesapladığımızdan hata olmaz. 
  :answer_b: Hata mesajı alırız. 
  :answer_c: While döngüsünden önce buna ihtiyacımız var, ama sonradan değil.
  :correct: b
  :feedback_a: Yanlış. Bunu daha önce hesaplamalıyız ya da abs(hedef- tahminKare) > 0.01 bir hata olur.)
  :feedback_b: Doğru. Değişken kullanılmadan önce tanımlanmalıdır (yaratılmalıdır).
  :feedback_c: Yanlış. İkisine de ihtiyacımız var. Biri testi kuruyor. Döngünün içindeki tahmin  değişkeni tahminKare değişkenini güncellememizi sağlar.

   ``while``  döngüsünden önce ``tahminKare`` hesaplanmazsa ne olur?


.. 8_4_1_Square_Root_Q1
..  :answer_a: No error, since we compute it inside the loop.
..  :answer_b: We would get an error.
..  :answer_c: We need the one before the while loop, but not the one afterward.
..  :correct: b
..  :feedback_a: We have to compute it before, or abs(target-guessSquared) > 0.01 would be an error.
..  :feedback_b: A variable has to be declared (created) before it is used.
..  :feedback_c: We need both.  The one before sets up the test.  The one inside the loop lets us update guessSquared.

..   What would happen if we didn't compute ``guessSquared`` before the ``while`` loop?


Diyelim ki, 6’nın karekökünü bulmak istediniz. ``while`` döngüsünün gövdesi kaç kez çalıştırılacak? Programı takip ederek anlayabiliriz.

.. codelens:: tahmin_while

	hedef = 6
	tahmin = 2
        tahminKare = tahmin * tahmin
        while abs(hedef - tahminKare) > 0.01:
            yakinsa = hedef / tahin
            tahmin = (tahmin + yakinsa) / 2.0
            tahminKare = tahmin * tahmin
        print(hedef, "'in karekökü: ", tahmin)



.. Let's say that you wanted to figure out the square root of 6.  How many times would the body of the ``while`` loop be executed?  We could figure it out by tracing the program.  

.. video: trace-squareroot
   :controls:
   :thumb: ../_static/squareRootTrace.png

   http://ice-web.cc.gatech.edu/ce21/1/static/video/square-root-trace.mov
   http://ice-web.cc.gatech.edu/ce21/1/static/video/square-root-trace.webm



.. mchoice:: 8_4_2_Count_Loops_Q1
  :answer_a: Sadece bir kere.
  :answer_b: İki kere.
  :answer_c: Üç Kere. 
  :answer_d: Dört kere. 
  :correct: c
  :feedback_a: Yanlış. Testi ilk kez yaptığımızda, tahmin 2 ve tahminKare, 2 * 2 = 4 ’tür ve (6 – 4) ise 0.01'den büyüktür.  
  :feedback_b: Yanlış. Testi ikinci kez yaptığımızda tahmin = 2.5 (3 ve 2 nin ortalaması) tahminKare = 2.5 * 2.5 yani 6.25 ki bu değer abs(62.5 - 6) > 0.01 den büyük durumda)
  :feedback_c: Doğru. Üçüncü testi yaptığımızda, tahmin 2.45 olur ve tahminKare de 6.0025. Bu, sayının 6' dan farkı 0,01'den azdır. Yani test 3 kez yürütülür.
  :feedback_d: Yanlış. Dördüncü kez döngüye giremeyiz. Tahmin değişkeni önce 2, sonra 2.5, daha sonra 2.45 olur. Bu noktada test başarısız olur ve döngü durur)

   ``abs(hedef - tahminKare) > 0.01`` durumu ``hedef = 6`` olduğunda kaç kere test edilir?

.. 25'in karekökü nasıl? 2.356'ya ne dersin? Döngünün kaç defa yürütüldüğünü önceden bilmek zor. Sonlandırma durumu (veya daha doğrusu, devam koşulu) belirtebileceğiniz zaman, while döngüsünün gerçekten parladığı yerdir. (EK)

Peki ya 25'in karekökü onu nasıl hesaplarız? 25'in karekökü 2,356 evet ama bu işlem için döngünün kaç defa yürütüldüğünü önceden bilmek zor. Sonlandırma durumu (veya daha doğrusu, *devam koşulu (continue condition)* belirtebileceğiniz zaman, ``while`` döngüsünün gerçekten parladığı yerdir.

.. Yukarıdaki çeviriyi düzellttim (ESG)




.. : 8_4_2_Count_Loops_Q1
..  :answer_a: Just once.
..  :answer_b: Twice.
..  :answer_c: Three times.
..  :answer_d: Four times
..  :correct: c
..  :feedback_a: The first time we do the test, guess is 2, and 2 * 2 is 4, and 6 - 4 is 2 which is greater than 0.01.  
..  :feedback_b: The second time we do the test, guess is 2.5 (average of 3 and 2). But, 2.5 * 2.5 = 6.25 which is still more than 0.01 away from 6.
..  :feedback_c: The third time we do the test, guess is 2.45 which is 6.0025 when squared.  This is less than 0.01 away from 6.  So test executes 3 times.
..  :feedback_d: We don't get to a fourth time.  Guess is 2, then 2.5, then 2.45 at which point the test fails and and the loop stops.

..   How many times do we execute the test ``abs(target-guessSquared) > 0.01`` when ``target = 6`` (in the video)?

.. How about the square root of 25?  How about 2,356?  It's difficult to know ahead of time how many times the loop will execute.  That's where the ``while`` loop really shines, when you can specify an end condition (or rather, a *continue* condition).









..  Bunlar başlangıç değeridir, ancak döngü sırasında değişir
.. mchoice:: 8_4_3_Var1Var2
   :answer_a: sayi1 = -2, sayi2 = 0
   :answer_b: sayi1 = 0, sayi2 = -2
   :answer_c: sayi1 = 0, sayi2 = -1
   :answer_d: Bu sonsuz bir döngüdür, bu yüzden hiçbir şey basmayacaktır.
   :correct: b
   :feedback_a: Yanlış.Bunlar değişkenlerin başlangıç değeridir, ancak  bu değerler döngü sırasında değişir
   :feedback_b: Doğru. Bu döngü iki kez çalışır, böylece sayi1'in değeri 0 olur ve döngü bittikten sonra sayi2'nin değeri -2 olur.
   :feedback_c: Yanlış. Döngü, sayi1 0'a eşit olur olmaz yürütmeyi durdurduysa, bu doğru olur. Döngünün gövdesi, sayi1 değeri tekrar test edilmeden önce çalışmayı bitirir. 
   :feedback_d: Yanlış. sayi1 = sayi1 - 1 olsaydı bu doğru olurdu.

   Aşağıdaki kod yürütüldüğünde yazdırılan sayi1 ve sayi2 değerleri nedir?
   
   :: 
      
      sayi1 = -2
      sayi2 = 0
      while sayi1 != 0:
          sayi1 = sayi1 + 1
          sayi2 = sayi2 - 1
      print("sayi1: " + str(sayi1) + " sayi2 " + str(sayi2))



..  8_4_3_Var1Var2
..   :answer_a: var1 = -2, var2 = 0
..   :answer_b: var1 = 0, var2 = -2
..   :answer_c: var1 = 0, var2 = -1
..   :answer_d: This is an infinite loop so it will never print anything.
..   :correct: b
..   :feedback_a: These are the initial value, but they change during the loop
..   :feedback_b: This loop will execute two times so var1 will be 0 and var2 will be -2 after the loop finishes.
..   :feedback_c: This would be true if the loop stopped executing as soon as var1 was equal to 0, but that isn't what happens.  The body of the loop will finish executing before the value of var1 is tested again.
..   :feedback_d: This would be true if it was <code>var1 = var1 - 1</code>

..   What are the values of var1 and var2 that are printed when the following code executes?
   
 
      
..      var1 = -2
..      var2 = 0
..      while var1 != 0:
..          var1 = var1 + 1
..          var2 = var2 - 1
..      print("var1: " + str(var1) + " var2 " + str(var2))




