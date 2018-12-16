..  Copyright (C)  Mark Guzdial, Barbara Ericson, Briana Morrison
    Permission is granted to copy, distribute and/or modify this document
    under the terms of the GNU Free Documentation License, Version 1.3 or
    any later version published by the Free Software Foundation; with
    Invariant Sections being Forward, Prefaces, and Contributor List,
    no Front-Cover Texts, and no Back-Cover Texts.  A copy of the license
    is included in the section entitled "GNU Free Documentation License".

.. 	qnum::
	:start: 1
	:prefix: csp-12-4-
	
.. highlight:: python
   :linenothreshold: 3
 
Mantıksal İfadeler ~ Logical Expressions
====================

Bir ``if`` deyiminin temel formu, ``if`` deyimi ardından mantıksal bir ifade ve bir kolon (:) ile sonlanma şeklindedir. ``if`` teriminin altına girintilenilen (indented) tüm ifadeler (**koşul gövdesi** olarak adlandırılır), *SADECE VE SADECE* verilen mantıksal ifade ``true (doğru)`` olduğunda, çalıştırılır.

.. The basic form of an ``if`` statement is the word **if** followed by a logical expression, and then a colon.  All the statements that are indented beneath the ``if`` (called the body of condition) are executed *IF AND ONLY IF* the logical expression is ``true``.

Aşağıdakiler mantıksal ifadelerin birer örneğidir

+------------+---------------------------------------------------------+
| İfade      | Mantıksal Anlam                                         |
+------------+---------------------------------------------------------+
| a < b      | Eğer a, b’den küçükse, Doğru.                           |
+------------+---------------------------------------------------------+
| a <= b     | Eğer a, b’den küçük veya b'ye eşitse, Doğru.            |
+------------+---------------------------------------------------------+
| a > b      | Eğer a, b ‘den büyükse, Doğru.                          |
+------------+---------------------------------------------------------+
| a >= b     | Eğer a, b’den b büyük veya b'ye eşitse, Doğru.          |
+------------+---------------------------------------------------------+
| a == b     | Eğer a, b’ye eşitse, Doğru.                             | 
|            | (İki eşit, atama işlecinden farklı olması içindir.)     |
+------------+---------------------------------------------------------+
| a != b     | Eğer a, b’ye eşit değilse, Doğru.                       | 
+------------+---------------------------------------------------------+


