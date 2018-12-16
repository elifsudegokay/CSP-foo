..  Copyright (C)  Mark Guzdial, Barbara Ericson, Briana Morrison
    Permission is granted to copy, distribute and/or modify this document
    under the terms of the GNU Free Documentation License, Version 1.3 or
    any later version published by the Free Software Foundation; with
    Invariant Sections being Forward, Prefaces, and Contributor List,
    no Front-Cover Texts, and no Back-Cover Texts.  A copy of the license
    is included in the section entitled "GNU Free Documentation License".

.. 	qnum::
	:start: 1
	:prefix: csp-8-5-
	
.. highlight:: java
   :linenothreshold: 4

	   	  
İç içe For Döngüsü
=================

Herhangi bir döngü gövdesi, başka bir döngüyü de içerebilir.  İşte size; 0’dan 10’a kadar olan bütün sayıların çarpım tablosunu oluşturan oldukça basit bir program. str() işlevi (function), sayısal bir değeri bir diziye – dizgiye dönüştürür

.. The body of any loop, can even include...another loop!  Here is a super-simple program that generates all the times tables from 0 to 10.  The ``str()`` function changes a numeric value into a string.

.. codelens:: Times_Table
	:showoutput: 

	for x in range(0,11):
	    for y in range(0,11):
	        print(str(x) + " * " + str(y) + " = " + str(x*y))
		

Bu programı gözden geçirmenin iki farklı yolu var. İlk yol olarak, programın *yapısına* bakarız – bunu sadece programa bakarak anlayabilirsiniz. 

.. Here are two different ways to look at this program.  In the first one, we look at the *structure* of the program -- what you can understand by just *looking* at the program.

.. video:: timesTableStructure
		   :controls:
		   :thumb: ../_static/timesTableStructure.png

		   http://ice-web.cc.gatech.edu/ce21/1/static/video/nestedLoopStructure.mov
		   http://ice-web.cc.gatech.edu/ce21/1/static/video/nestedLoopStructure.webm


İkinci yol olarak ise programın yürütülme (çalıştırılma) aşamasına bakarız – bilgisayar tarafından çalıştırıldığında, programın gerçekte nasıl işlediğini görebilirsiniz.

.. In this video, we look at the *execution* of the program -- how it actually works when it's being *run* by the computer.

.. video:: timesTableTrace
		   :controls:
		   :thumb: ../_static/timesTableTrace.png

		   http://ice-web.cc.gatech.edu/ce21/1/static/video/nestedLoopTrace.mov
		   http://ice-web.cc.gatech.edu/ce21/1/static/video/nestedLoopTrace.webm
		   
İç Döngü Kaç Kez Çalışır?
--------------------------------------------
		   
Aşağıdaki kodu deneyin. Kaç tane ``*`` yazdırılıyor? Peki sizce program neden bu kadar fazla yazdırıyor? Şimdi de programdaki başlangıç ve bitiş değerlerini değiştirin ve bu değerlere göre çıktının (output) nasıl değiştiğini gözlemleyin. 

.. Try out the following code.  How many ``*``'s are printed?  Why do you think it prints that many?  Try changing the start and end values and see what changing those does to the output.

.. activecode:: Nested_Loops_Stars

    for x in range(0,2):
        for y in range(0,3):
            print('*')
            
Dış döngü 2 kez yürütülür (çalıştırılır - execute) ve her dış döngü iç döngüyü 3 kez yürütür (çalıştırır - execute). Böylece ekrana 2 * 3 = 6 adet yıldız basılacaktır.

.. The outer loop executes 2 times and each time the outer loop executes the inner loop executes 3 times so this will print 2 * 3 = 6 stars.  

.. note::
   İç içe döngünün toplamda kaç kez çalıştırılacağı; dış döngünün tekrar sayısı ile iç döngünün tekrar sayısının çarpım değerine göredir. 


.. The formula for calculating the number of times the inner loop executes is the number of times the outer loop repeats multiplied by the number of times the inner loop repeats.
		   
.. mchoice:: 8_5_1_NumStars
   :answer_a: 6
   :answer_b: 9
   :answer_c: 12
   :answer_d: 16
   :answer_e: 20
   :correct: c
   :feedback_a: Yanlış. Range işlevinin (function); başlangıç değerinden itibaren son değerin bir eksiğine kadar olan sayıları içereceğini unutmayın. Buna göre dış döngü 3 kez ([0,1,2]) çalışacaktır
   :feedback_b: Yanlış. range(0,3) işlevi, her iki döngü için de geçerli olsaydı; bu doğru olurdu.
   :feedback_c: Doğru. İç içe döngünün toplamda kaç kez çalıştırılacağı; dış döngünün tekrar sayısı (3) ile iç döngünün tekrar sayısının (4) çarpım değerine göredir. Dolayısıyla ekrana 3 * 4  = 12 adet yıldız basılacaktır. 
   :feedback_d: Yanlış. range(0,4) işlevi, her iki döngü için de geçerli olsaydı; bu doğru olurdu
   :feedback_e: Yanlış. Range işlevi, başlagıç değerinden son değere kadar olan sayıları döndürdüğünde bu gerçekleşir fakat böyle bir işlem tanımlı değildir.

   Bu döngü kaç kez ``*`` yazdırır?
   
   :: 
      
       for x in range(0,3):
           for y in range(0,4):
               print('*')
               
İç döngüdeki bir diziye - dizgiye (string) öğe (item) ekleyebilir ve sonrasında bir desen oluşturmak için dizileri - dizgileri (string) yazdırabilirsiniz. 

.. You can add items to a string in the inner loop and then print the strings to make a pattern.  
               
.. activecode:: Nested_Loops_Pattern

    for x in range(0,2):
        cizgi = ""
        for y in range(0,3):
            cizgi = cizgi + '*'
        print(cizgi)
        
Yıldızlardan bir kare çizmek için (sadece kenarları dolu olacak şekilde – içi boş), yukarıdaki kodu değiştirin. 

.. Modify the code above to draw a square of stars.  

.. tabbed:: 8_5_2_WSt

        .. tab:: Soru

           Yıldızları, 4’e 4 (4 x 4) boyutunda boş bir kare şeklinde yazdırmak için gereken kodu yazın. 
           
           .. activecode::  8_5_2_WSq
                :nocodelens:

        .. tab:: Cevap
            
          .. activecode::  8_5_2_WSa
              :nocodelens:
              
              # ÜST ÇİZGİ 
              cizgi = ""
              for x in range(0,4):
                cizgi = cizgi + "*"
              print(cizgi)

              # ORTA ÇİZGİLER 
              for x in range(0,2):      # karenin kenarı için dış döngü
                cizgi = "*"
                for y in range(0,2):    # karenin boşluğu için iç döngü
                    cizgi = cizgi + ' '
                 cizgi = cizgi + '*'
                print(cizgi)

              # ALT ÇİZGİ 
              cizgi = ""
              for x in range(0,4):
                cizgi = cizgi + "*"
              print(cizgi)

               
..   :answer_a: 6
  .. :answer_b: 9
 ..  :answer_c: 12
..   :answer_d: 16
..   :answer_e: 20
..   :correct: c
..   :feedback_a: Remember that the range function will include the start value and all the numbers up to one less than the end value.  So the outer loop will execute 3 times ([0,1,2]).
  .. :feedback_b: This would be true if they were both range(0,3).  Is that correct?
..   :feedback_c: The number of times a nested loop executes is the number of times the outer loop executes (3) times the number of the times the inner loop executes (4) so that is 3 * 4 = 12.  
..   :feedback_d: This would be true if both were range(0,4).  Is that right?
..   :feedback_e: This would be true if the range returned all the numbers from start to end, but it does not.
..
   How many times will this loop print a ``*``?
   
   :: 
      
       for x in range(0,3):
           for y in range(0,4):
               print('*')
..               
.. You can add items to a string in the inner loop and then print the strings to make a pattern.  
               
..  Nested_Loops_Pattern

    for x in range(0,2):
        line = ""
        for y in range(0,3):
            line = line + '*'
        print(line)
        
.. Modify the code above to draw a square of stars.  

.. 8_5_2_WSt

        .. tab:: Question

           Write code to print stars in the shape of an empty square of size 4 by 4. 
           
           .. activecode::  8_5_2_WSq
                :nocodelens:

        .. tab:: Answer
            
          .. activecode::  8_5_2_WSa
              :nocodelens:
              
              # TOP LINE 
              line = ""
              for x in range(0,4):
                line = line + "*"
              print(line)

              # MIDDLE LINES 
              for x in range(0,2):      # outer loop for edge of square 
                line = "*"
                for y in range(0,2):    # inner loop for space in square
                    line = line + ' '
                line = line + '*'
                print(line)

              # BOTTOM LINE 
              line = ""
              for x in range(0,4):
                line = line + "*"
              print(line)

               

