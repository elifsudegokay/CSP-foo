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
	:prefix: csp-1-8-


Ünite 1 - Kavram Özeti
============================

Bu bölüm bilgisayar bilimleri ile ilgili aşağıdaki kavramları içermektedir.

..	index::
	single: code
	single: comment
	single: dot-notation
	single: library
	single: pixel
	single: program
	single: screen
	single: variable

- **Kod (Code)** - Kod, bilgisayarın anlayabileceği talimatlar kümesidir. Bu **program** olarak da adlandırılabilir. 
- **Yorum (Comment)** -  Yorumlar program içerisinde yapılanları açıklar ve insanlar tarafından okunulması niyetiyle oluşturulur, bilgisayarlar bunu algılamaz (işleme tabi tutmaz). Python dilinde yorumlar ``#`` ile başlar. 
- **Nokta Gösterimi Dot-Notation** - okta gösterimi, Pyhton da yapılacak olan işlemlerde nesneyi nasıl belirteceğimizi niteler. Nesneden (object) sonra bir nokta (period) kullanırız, sonrasında nesneden yapmasını istediklerimiz ve sayılar bunu takip eder. Örneğin; ``sentence``  adında bir değişkenden küçük harflerden oluşan yeni bir dizi (string) üretmek için ``sentence.lower()`` kullanın.  ``alex`` adında kaplumbağa nesnesini (object) 50 birim ilerletmek için ``alex.forward(50)`` kullanın. 

- **Kütüphane (Library)** Kütüphane bazı işlevleri gerçekleştiren **program**lar topluluğudur. Kaplumbağa ``Turtle``  kütüphanesi bunun için iyi bir örnektir. Kaplumbağa ``Turtle`` kütüphanesi içinde barındırdığı kaplumbağa (``Turtle``) nesnelerini oluşturmamızı ve kullanmamızı sağlar.
``Turtle`` 
  
- **Piksel (Pixel)** -Piksel resmin en küçük parçasıdır (element). Pikseller bir kılavuz (grid) içerisine saklanır,  x (yatay) ve y (dikey) değerlerini de içinde barındırır. Pikselin 0 ve 255 arasında değişen kırmızı, yeşil ve mavi renk değerleri vardır.   
- **Program** - Program sonuçları elde etmek için bilgisayarın anlayabileceği talimatlar kümesidir. **Kod** olarak da adlandırılabilir.  
- **Screen (Ekran)** - ``Screen`` ya ``Ekran`` kaplumbağa (turtle) kütüphanesinin bir parçasıdır. Kaplumbağa nesnesinin üzerinde hareket ettiği ve çizim yaptığı sayfa üzerindeki bir alandır.
- **String (Dizi)** - Dizi tekli (``'Hi'``), ikili (``"Hi"``) veya üçlü (``'''Hi'''``) tırnak arasında karakterler yazabildiğimiz bir nesne (object) türüdür. Aynı zamanda karakterler topluluğudur.

- **Değişken (Variable)** -  Değişken bilgisayar hafızasında tutulan değerin ismidir. Bu değer değiştirilebilir veya çeşitlendirilebilir. Bir değişken örneği olarak bir maçın skoru düşünülebilir.


