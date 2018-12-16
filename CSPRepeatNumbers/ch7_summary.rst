..  Copyright (C)  Mark Guzdial, Barbara Ericson, Briana Morrison
    Permission is granted to copy, distribute and/or modify this document
    under the terms of the GNU Free Documentation License, Version 1.3 or
    any later version published by the Free Software Foundation; with
    Invariant Sections being Forward, Prefaces, and Contributor List,
    no Front-Cover Texts, and no Back-Cover Texts.  A copy of the license
    is included in the section entitled "GNU Free Documentation License".

.. setup for automatic question numbering.

.. 	qnum::
	:start: 1
	:prefix: csp-7-7-


Ünite 5 ~ Kavram Özeti 
============================

Bu ünite programlama ile ilgili aşağıdaki kavramları içermektedir.

..	index::
    single: accumulator pattern
	single: body of a loop
	single: for loop
	single: indention
	single: iteration
	single: list
	single: loop
	single: print
	single: range
	

- **Biriktirici Örüntü ~ Accumulator Pattern** - TBiriktirici örüntü, bir listenin içindeki değerler üzerinde bir dizi işlem yapılmasına denir. Buna, bir listedeki tüm sayıların toplamını bulan kodu örnek verebiliriz.
- **Döngü Gövdesi ~ Body of a Loop** - TBir döngüde tekrarlanan işlem ya da işlemler kümesine döngünün gövdesi ismi verilir. Python'da döngü gövdeleri girintilerle belirtilir.   
- **Girintili yazma ~ Indention** - Girintili yazma, bir metnin satırın hemen başından değil de boşluk bırakarak daha içeriden başlamasına denir. Python’da ise girintili yazma, hangi deyimlerin aynı blok içerisinde olduğunu belirtmek için kullanılır. Örneğin bir döngünün gövdesi, döngüyü başlatan deyimden dört boşluk içeriden başlar.
- **Yineleme ~ Iteration** - Yineleme, programlamada, bir ya da birden fazla adımın tekrarlanabilmesine verilen addır. **Looping** diye de adlandırılır. 
- **Liste ~ liste** -  Bir liste, bir dizi elemanı verilen sıra ile tutar. Python dilinde kullanılan listeye ``[1, 2, 3]`` örnek verilebilir. 
- **Döngü ~ Loop** - Döngü bilgisayara bir ya da birden fazla deyimi tekrar etmesini söyler.


Python Anahtar Sözcüklerinin ve İşlevlerinin Özeti
-------------------------------------------- 

- **for** -  Bir ``for`` döngüsü, bilgisayara bir ya da birden fazla deyimin tekrar etmesini söyleyen deyimdir. Döngü çeşitlerinden bir tanesidir.
- **print** - Python’da kullanılan ``print`` deyimi, bir elemanın değerini ekrana basmaya yarar.
- **range** - Python’da kullanılan ``range`` fonksiyonu, ardışık değerleri içeren bir liste döndürür. Eğer ``range`` fonksiyonuna girdi olarak sadece ``bir değer`` parametre olarak verilirse, 0’dan verilen o sayıya kadar olan değerleri (o sayı hariç) içeren bir liste döndürür. Örneğin,``[0,1,2,3,4]`` böyle bir liste döndürmek istiyorsak range fonksiyonunu  ``range(5)`` şeklinde kullanmalıyız. Eğer range fonksiyonuna girdi olarak ``iki değer`` verilirse, ilk sayıdan başlayıp ikinci sayıya kadar olan değerleri içeren bir liste döndürür. Bu liste ilk sayıyı içerirken, ikinci sayıyı içermez. Örneğin ``range(1,4)`` kullanımı ``[1, 2, 3]``listesini döndürecektir. Eğer üç değer girdi olarak kullanılırsa range(başlangıç,son,adım), ll başlangıçtan sona kadar adım kadar atlayarak bir liste oluşturur. Örneğin ``range(0,10,2)`` kullanımı ``[0,2,4,6,8]``. listesini döndürecektir.



.. - **Accumulator Pattern** - The accumulator pattern is a set of steps that processes a list of values.  One example of an accumulator pattern is the code to sum a list of numbers.  
.. - **Body of a Loop** - The body of a loop is a statement or set of statements to be repeated in a loop.  Python uses indention to indicate the body of a loop.  
.. - **Indention** - Indention means that the text on the line has spaces at the beginning of the line so that the text doesn't start right at the left boundary of the line.  In Python indention is used to specify which statements are in the same block.  For example the body of a loop is indented 4 more spaces than the statement starting the loop.   
.. - **Iteration** - Iteration is the ability to repeat a step or set of steps in a computer program.   This is also called **looping**.  
.. - **List** - A list holds a sequence of items in order.  An example of a list in Python is ``[1, 2, 3]``.
.. - **Loop** - A loop tells the computer to repeat a statement or set of statements. 


.. Summary of Python Keywords and Functions
-------------------------------------------- 

.. - **def** - The ``def`` keyword is used to define a procedure or function in Python.  The line must also end with a ``:`` and the body of the procedure or function must be indented 4 spaces.
.. - **for** - A ``for`` loop is a programming statement that tells the computer to repeat a statement or a set of statements. It is one type of loop. 
.. - **print** - The ``print`` statement in Python will print the value of the items passed to it.  
.. - **range** - The ``range`` function in Python returns a list of consecutive values.  If the range function is passed one value it returns a list with the numbers from 0 up to and not including the passed number.  For example, ``range(5)`` returns a list of ``[0,1,2,3,4]``.  If the range function is passed two numbers separated by a comma it returns a list including the first number and then up to but not including the second number.  For example, ``range(1,4)`` returns the list ``[1, 2, 3]``.  If it is passed three values ``range(start,end,step)`` it returns all the numbers from start to one less than end changing by step.  For example, ``range(0,10,2)`` returns ``[0,2,4,6,8]``.

