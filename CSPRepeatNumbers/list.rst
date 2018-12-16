..  Copyright (C)  Mark Guzdial, Barbara Ericson, Briana Morrison
    Permission is granted to copy, distribute and/or modify this document
    under the terms of the GNU Free Documentation License, Version 1.3 or
    any later version published by the Free Software Foundation; with
    Invariant Sections being Forward, Prefaces, and Contributor List,
    no Front-Cover Texts, and no Back-Cover Texts.  A copy of the license
    is included in the section entitled "GNU Free Documentation License".

.. 	qnum::
	:start: 1
	:prefix: csp-7-3-
	
.. highlight:: java
   :linenothreshold: 4

Liste (list) Nedir ? 
=================

Bir **liste (list)** ; bir dizi elemanı, verilen sıra ile tutar.  Python’da bir liste ``[`` ve ``]`` içerisine (arasına) eklenir ve ``[1,2,3,4,5,6,7,8,9,10]`` gibi virgülle ayrılmış değerlere sahip olabilir. Çoğu zaman **listeleri** kullanırız. Genellikle alışverişe çıkmadan önce bir **liste** hazırlar ya da yapılacak şeylerin bir listesini yaparız. Her listenin belli bir düzeni vardır; dolayısıyla her **liste** elemanı, **listede** belirli bir yere (konuma) sahiptir, örneğin listenin ilk elemanı veya listenin son elamanı gibi.

.. A **list** holds items in order. A **list** in Python is enclosed in ``[`` and ``]`` and can have values separated by commas, like ``[1,2,3,4,5,6,7,8,9,10]``.  You probably use **lists** all the time.  People often make a list before they go shopping or a list of things to do.  A **list** has an order and each list item has a position in the list, like the first item in a list or the last item in a list.

.. figure:: Figures/lists.jpg
    :height: 250px
    :align: center
    :alt: a shopping list
    :figclass: align-center

    Figure 2: A shopping list


Bir önceki bölümde yer alan kodu çalıştırdığınızda, 55 değerini mi elde ettiniz? Bu değer, 1’den 10’a kadar olan sayıların toplamıdır. Aynı programı tekrar ele alalım. Önceden yazdırdığı değeri hatırlamıyorsanız, programı çalıştırın. 


.. When you ran the code in the last section, did you get 55?  That's the sum of all the numbers from 1 to 10.  Here is the program again.  Run it if you don't remember what it printed before.

.. activecode:: Numbers_Repeat2
    :tour_1: "Line by line tour"; 1: for1_line1; 2: for1_line2; 3: for1_line3; 4: for1_line4; 5: for1_line5;
    :tour_2: "High level tour"; 1-2: for1_line1-2; 3-4: for1_line3-4; 5: for1_s_line5;
	 
    toplam = int (input ("Baslangic degerini giriniz: "))	# etkisiz eleman olduğu için 0'dan baslatin
    eklenenDegerler = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
    for sayi in eklenenDegerler :
        toplam = toplam + sayi
    print("toplam: ", toplam)

.. sum = 0  # Start out with nothing
.. thingsToAdd = [1,2,3,4,5,6,7,8,9,10]
.. for number in thingsToAdd:
.. sum = sum + number
.. print(sum)

.. mchoice:: 7_3_1_Numbers_Repeat2_Q1
   :answer_a: 55
   :answer_b: 0
   :answer_c: 3628800
   :answer_d: Hata – Sayı çok büyük 
   :correct: c
   :feedback_a: Yanlış. Bu toplam değerdir.
   :feedback_b: Yanlış. Toplam’ı 0 olarak girdiğinizde elde edeceğiniz değerdir. Herhangi bir değeri 0 ile çarpmak size 0 değerini verecektir
   :feedback_c: Doğru. Bu 1*2*3*4*5*6*7*8*9*10 çarpımının değeridir
   :feedback_d: Yanlış. Program çalışmalıdır. 

   Şimdi, girilen değerlerin toplamı yerine çarpımını elde etmek için yukarıdaki programı değiştirin. (ör. `+` işleci (operator) yerine `*` işlecini kullanın ve `toplam` ’ın başlangıç değeri olan `0` değerini `1` değeri olarak değiştirin.) Programı çalıştırdığınızda ne elde edersiniz?

.. Now, change the program above to get the product instead of the sum (e.g., replace `+` with `*`, and replace the `0` as the initial value of `sum` to `1`).  What do you get now when you run the program?



.. mchoice: 7_3_1_Numbers_Repeat2_Q1
.. :answer_a: 55
.. :answer_b: 0
.. :answer_c: 3628800
.. :answer_d: Error - number is too big
.. :correct: c
.. :feedback_a: That's the sum
.. :feedback_b: That's what you get if you leave the sum as 0.  Multipying everything by 0 gets you 0
.. :feedback_c: That's 1*2*3*4*5*6*7*8*9*10
.. :feedback_d: It should actually work

.. Now, change the program above to get the product instead of the sum (e.g., replace `+` with `*`, and replace the `0` as the initial value of `sum` to `1`).  What do you get now when you run the program?




.. note
    Once you change the program above in order to use ``*`` instead of ``+``, you will see that it is still using the name (*variable*) ``sum`` to represent the `product` of all the numbers in ``thingsToAdd``.  The program would be *better* if we used the right name for the variable: ``product`` instead of ``sum`` once we switched to multiplication (``*``) from addition (``+``).  However, the program still *works*.  In the end, the names for the variables are there for the benefit of the *humans*, not the computer.  The computer doesn't care if we name the program `xyzzy1776`.  It will *work* with a bad variable name.  It's just not as readable.  **You should write your programs so that people can understand them, not just computers.** 

Daha İyi Değişken İsimleri Kullanma
-----------------------------

Bu programı daha iyi bir değişken ismi ile tekrar yazalım. Hesaplama sonucunu tutan değişken ismi için ``toplam`` yerine ``çarpım`` kullanacağız. *İleri (Forward)* butonuna tıklayarak programda adım adım ilerleyin ve ``sayi`` isimli değişkenin, döngü (loop) boyunca her defasında hangi değeri aldığına dikkat edin



.. Let's write that program again with a better variable name.  We will use ``product`` instead of ``sum`` for the variable name that holds the result of the calculation.  Step through the code below by clicking on the *Forward* button and note what value the variable ``number`` is set to each time through the loop.  Also note how the variable ``product`` changes during the loop.




.. codelens:: Numbers_Product
	
    carpim = int (input ("Başlangıç değerini giriniz: "))  # etkisiz elemandan baslatin
    sayilar = [1,2,3,4,5,6,7,8,9,10]
    for sayi in sayilar:
    	carpim = carpim * sayi
    print("Sonuç: ", carpim)
    
.. mchoice:: 7_3_2_Numbers_Product_Q1
   :answer_a: 1
   :answer_b: 2
   :answer_c: 3
   :answer_d: 4
   :answer_e: 10
   :correct: c
   :feedback_a: Yanlış. Bu, döngünün ilk sayi değeridir.
   :feedback_b: Yanlış. Bu, döngünün ikinci sayi değeridir.
   :feedback_c: Doğru. Bu, döngünün üçüncü sayi değeridir.
   :feedback_d: Yanlış. Bu, döngünün dördüncü sayi değeridir.
   :feedback_e: Yanlış. Bu, döngünün son sayi değeridir.

   Döngünün 3. adımındaki “sayi” değişkenin değeri nedir?
   
.. mchoice:: 7_3_3_Numbers_Product_Q2
   :answer_a: 6
   :answer_b: 10
   :answer_c: 24
   :answer_d: 120
   :correct: c
   :feedback_a: Yanlış. Bu, döngünün üçüncü adımdan sonraki carpim değeridir
   :feedback_b: Yanlış. Değerleri çarpmak yerine ekliyor olsaydık bu değeri elde ederdik.
   :feedback_c: Doğru. Bu, döngünün dördüncü adımdan sonraki carpim değeridir.
   :feedback_d: Yanlış. Bu, döngünün üçüncü adımdan sonraki carpim değeridir

   Döngünün 4. adımındaki “carpim” değişkenin değeri nedir?
   
.. parsonsprob:: 7_3_4_Average

   Aşağıdaki program, “numbers” isimli listede bulunan değerlerin ortalamasını hesaplar; ancak program karışık sıra ile verilmiştir. İlk olarak; “toplam” değişkeninin değerini 0’dan başlatın. Ardından “sayilar” listesini oluşturun. Liste elemanlarını kullanarak döngü (loop) yaratın ve her seferinde mevcut “sayi” değişkeninin değerini “toplam” değişkeninin değerine ekleyin. Son olarak; listedeki eleman sayısına bölünmüş olan “toplam” değişkeninin son değerini yazdırın. <b>Döngü içerisindeki satırları girintili yazmanız gerektiğini unutmayın.</b>
   -----
   toplam = 0
   sayilar = [90, 80, 75, 90, 83]
   for sayi in sayilar:
       toplam = toplam + sayi
   print('Ortalama: ' , toplam / 5) 

.. tabbed:: 7_3_5_WSt

        .. tab:: Soru

           Range işlevini (fonksiyonunu) kullanarak; minimum değeri 1 olan maksimum değeri ise kullanıcıdan alınacak değere eşit olan, “sayilar” isimli bir liste oluşturun ve bu listenin bütün elemanlarının toplamını hesaplatan bir program yazın.
           
           .. activecode::  7_3_5_WSq
                :nocodelens:

        .. tab:: Cevap
            
          .. activecode::  7_3_5_WSa
              :nocodelens:
              
              
              
              minimum = int (input('Minimum değeri giriniz: '))
              maksimum =  int (input('Maksimum değeri giriniz: '))
              
              #Veriyi İsimlendirin 

              sayilar = range(minimum, maksimum)

              #Listeyi yazdırın

              print('Listeniz: ', sayilar)	

              toplam = int (input("Toplamın başlangıç değerini giriniz: ")) #etkisiz eleman olduğu için 0'dan başlatın

              #Veri döngüsünü Oluşturun

              for sayi in sayilar:
                  toplam = toplam + sayi

              print("Oluşturduğunuz listedeki sayıların toplamı: ", toplam)
              

                














..

.. codelens:: Numbers_Product
	
    product = 1  # Start out with nothing
    numbers = [1,2,3,4,5,6,7,8,9,10]
    for number in numbers:
    	product = product * number
    print(product)
    
.. mchoice:: 7_3_2_Numbers_Product_Q1
   :answer_a: 1
   :answer_b: 2
   :answer_c: 3
   :answer_d: 4
   :answer_e: 10
   :correct: c
   :feedback_a: That's the value the first time through the loop
   :feedback_b: That's the value the second time through the loop
   :feedback_c: That's the value the third time through the loop
   :feedback_d: That's the value the fourth time through the loop
   :feedback_e: That's the value the last time through the loop

   What is the value of number the 3rd time through the loop?
   
.. mchoice:: 7_3_3_Numbers_Product_Q2
   :answer_a: 6
   :answer_b: 10
   :answer_c: 24
   :answer_d: 120
   :correct: c
   :feedback_a: That's the value after the 3rd time through the loop.
   :feedback_b: That's the value if we were adding up the values rather than multiplying them.
   :feedback_c: That's the value after the 4th time through the loop.
   :feedback_d: That's the value after the 5th time through the loop.

   What is the value of product after the 4th time through the loop?
   
.. parsonsprob:: 7_3_4_Average

   The following program calculates the average of a list of numbers, but the code is mixed up.  First initialize the sum to 0.  Then create the list of numbers.  Loop through the list and each time add the current number to the sum.  Print the sum divided by the number of items in the list.  <b>Don't forget that you must indent the lines that are repeated in the loop</b>.
   -----
   sum = 0
   numbers = [90, 80, 75, 90, 83]
   for number in numbers:
       sum = sum + number
   print(sum / 5) 

.. tabbed: 7_3_5_WSt

        .. tab:: Question

           Define a function to calculate the sum of 1 to the passed number using the range function.  Return the sum from the function.  Call the function and print the result.
           
           .. activecode::  7_3_5_WSq
                :nocodelens:

        .. tab:: Answer
            
          .. activecode::  7_3_5_WSa
              :nocodelens:
              
              # DEFINE THE FUNCTION
              def summation(endvalue):
                # INITIALIZE ACCUMULATOR 
                sum = 0  
                # NAME DATA
                numbers = range(1, endvalue +1)
                # LOOP THROUGH DATA
                for number in numbers:
                  # ACCUMULATE 
                  sum = sum + number
                # RETURN SUM
                return sum

              # PRINT RESULT 
              print(summation(10)) 
                



