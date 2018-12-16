..  Copyright (C)  Mark Guzdial, Barbara Ericson, Briana Morrison
    Permission is granted to copy, distribute and/or modify this document
    under the terms of the GNU Free Documentation License, Version 1.3 or
    any later version published by the Free Software Foundation; with
    Invariant Sections being Forward, Prefaces, and Contributor List,
    no Front-Cover Texts, and no Back-Cover Texts.  A copy of the license
    is included in the section entitled "GNU Free Documentation License".

.. |runbutton| image:: Figures/run-button.png
    :height: 20px
    :align: top
    :alt: run button

.. |audiobutton| image:: Figures/start-audio-tour.png
    :height: 20px
    :align: top
    :alt: audio tour button

.. |codelensfirst| image:: Figures/codelens-first.png
    :height: 20px
    :align: top
    :alt: move to first button

.. |codelensback| image:: Figures/codelens-back.png
    :height: 20px
    :align: top
    :alt: back button

.. |codelensfwd| image:: Figures/codelens-forward.png
    :height: 20px
    :align: top
    :alt: forward (next) button

.. |codelenslast| image:: Figures/codelens-last.png
    :height: 20px
    :align: top
    :alt: move to last button
    
.. 	qnum::
	:start: 1
	:prefix: csp-3-5-

.. highlight:: java
   :linenothreshold: 4


İfadeler (Expressions) Nasıl Çalışır ?
===============================

.. The order that expressions are executed is the same as it is in math and is shown in the table below from highest precedence to lowest. If two symbols have the same precedence they are evaluated from left to right.

İfadelerin çalışma sırası matematiksel işlemler sıralaması ile aynıdır. Aşağıdaki tabloda operatör öncelikleri en yüksek öncelikten en düşük ön düşük önceliğe doğru gösterilmektedir. Eğer iki sembol (matematiksel sembol +, - gibi) aynı önceliğe sahip ise sıralama soldan sağa doğru değerlendirilir.
   

+------------------------+----------------------------------------------------+
|İşleç (Operator)        | Operatörün İsmi                                    |
+------------------------+----------------------------------------------------+
| -x                     | Olumsuzluk, Negatiflik                             |
+------------------------+----------------------------------------------------+
| x * y, x / y, x % y    | Çarpma, Bölme, ve Mod Operatörleri	              |
+------------------------+----------------------------------------------------+
| x + y, x - y           | Toplama ve çıkarma				      |
+------------------------+----------------------------------------------------+

.. fillintheblank:: 3_4_1_Order1_fill

   Aşağıdaki Çalıştır (Run) butonuna tıklandığında kod bloğunun çıktısı ne olur?

   -    :^-2$: Doğru
        :.*: Programı çalıştırdığına emin misin? 

.. activecode:: Expression_Order1
    :nocodelens:
    
    result = 4 + -2 * 3
    print(result)
   
İfadeye parantez ekleyerek işlem öncelik sırasını değiştirebilirsiniz

.. fillintheblank:: 3_4_2_Order2_fill

   Aşağıdaki Çalıştır (Run) butonuna tıklandığında kod bloğunun çıktısı ne olur.

   -    :^6$: Doğru
        :.*: Programı çalıştırdığına emin misin?

.. activecode:: Expression_Order2
    :nocodelens:
    
    result = (4 + -2) * 3
    print(result)


