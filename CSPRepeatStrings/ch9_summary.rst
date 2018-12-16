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
	:prefix: csp-9-5-


Ünite - 7 ~ Kavram Özeti
============================

Bu ünite programlama ile ilgili aşağıdaki kavramları içermektedir.

..	index::
    single: accumulator pattern
    single: for loop
    single: palindrome
    single: range
	single: string




- **Biriktirici Örüntü ~ Accumulator Pattern** - Biriktirici örüntü, bir listenin içindeki değerler üzerinde bir dizi işlem yapılmasına denir. Buna, bir listedeki tüm sayıların toplamını bulan kodu örnek verebiliriz.
- **Palindrom ~ Palindrome** - Bir palndrom baştan ve sondan okunduğunda aynı harflere sahiptir yani baştan ve sondan okunuşu aynıdır. Örneğin: ``"ey edip adanada pide ye"``
- **Karakter Dizisi ~ Dizgi ~ String** - İki çift ya da tek tırnak arasına harf, sayı ve boşluk gibi diğer karakterlerin bir araya gelmesine karakter dizisi denir.

Python Anahtar Sözcüklerinin ve İşlevlerinin Özeti
-------------------------------------------- 


- **for** - Bir ``for``  döngüsü, bilgisayara bir ya da birden fazla deyimin tekrar etmesini söyleyen deyimdir. Döngü çeşitlerinden bir tanesidir.
- **print** - Python’da kullanılan ``print`` deyimi, bir elemanın değerini ekrana basmaya yarar.  
- **range** - Python’da kullanılan ``range`` fonksiyonu, ardışık değerleri içeren bir liste döndürür. Eğer range fonksiyona girdi olarak 1 değer verilirse, 0’dan verilen o sayıya kadar olan değerleri (o sayı hariç) içeren bir liste döndürür. Örneğin, ``[0,1,2,3,4]`` böyle bir liste döndürmek istiyorsak range fonksiyonunu  ``range(5)`` şeklinde kullanmalıyız. Eğer range fonksiyonuna girdi olarak iki değer verilirse, ilk sayıdan başlayıp ikinci sayıya kadar olan değerleri içeren bir liste döndürür. Bu liste ilk sayıyı içerirken, ikinci sayıyı içermez. Örneğin  ``range(1,4)``  kullanımı ``[1, 2, 3]`` listesini döndürecektir. Eğer üç değer girdi olarak kullanılırsa ``range(baslangıç, son, adım)`` ,  başlangıçtan sona kadar adım kadar atlayarak bir liste oluşturur. Örneğin ``range(0,10,2)`` kullanımı ``[0,2,4,6,8]`` listesini döndürecektir.

- **while** -  ``while``  döngüsü, bilgisayara bir ya da birden fazla deyimi tekrar etmesini söyleyen diğer bir deyimdir. **Mantıksal ifadenin (logical expression)** doğru olması durumunda, **döngünün gövdesini (body of the loop)** tekrarlar.


.. - **Accumulator Pattern** - The accumulator pattern is a set of steps that processes a list of values.  One example of an accumulator pattern is the code to reverse the characters in a string.
.. - **Palindrome** - A palindrome has the same letters if you read it from left to right as it does if you read it from right to left.  An example is ``"A but tuba"``.  
.. **String** - A string is a collection of letters, numbers, and other characters like spaces inside of a pair of single or double quotes.

.. Summary of Python Keywords and Functions
-------------------------------------------- 

.. - **def** - The ``def`` keyword is used to define a procedure or function in Python.  The line must also end with a ``:`` and the body of the procedure or function must be indented 4 spaces.
.. - **for** - A ``for`` loop is a programming statement that tells the computer to repeat a statement or a set of statements. It is one type of loop. 
.. - **print** - The ``print`` statement in Python will print the value of the items passed to it.  
.. - **range** - The ``range`` function in Python returns a list of consecutive values.  If the range function is passed one value it returns a list with the numbers from 0 up to and not including the passed number.  For example, ``range(5)`` returns a list of ``[0,1,2,3,4]``.  If the range function is passed two numbers separated by a comma it returns a list including the first number and then up to but not including the second number.  For example, ``range(1,4)`` returns the list ``[1, 2, 3]``.  If it is passed three values ``range(start,end,step)`` it returns all the numbers from start to one less than end changing by step.  For example, ``range(0,10,2)`` returns ``[0,2,4,6,8]``.
.. - **while** - A ``while`` loop is a programming statement that tells the computer to repeat a statement or a set of statements. It repeats the **body of the loop** while a **logical expression** is true.


