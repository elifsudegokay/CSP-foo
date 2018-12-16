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
	:prefix: csp-3-3-

.. highlight:: java
   :linenothreshold: 4



İfade Tiplerinin Özeti
============================

+--------------------+-------------------------------------------------------------------------------------------------------------------------------+
| İfade (expression) | Aritmetik anlam taşır                               					                                     |
+--------------------+-------------------------------------------------------------------------------------------------------------------------------+
| 1 + 2      	     | Toplama işlemini ifade eder, sonuç 3.                            				                             |
+--------------------+-------------------------------------------------------------------------------------------------------------------------------+
| 3 * 4     	     | Çarpma işlemini ifade eder, sonuç 12.                                       					             |
+--------------------+-------------------------------------------------------------------------------------------------------------------------------+
| 1 / 3     	     | Tam sayı bölme işlemini ifade eder, sonuç eski Python versiyonlarında 0 ancak aynı işlemin sonucu Python 3’de 0.333333333333. |
+--------------------+-------------------------------------------------------------------------------------------------------------------------------+
| 2.0 / 4.0 	     | Bölme işlemini ifade eder, sonuç hesaplama işleminde ondalık sayı kullandığınız için 0.5.				     |
+--------------------+-------------------------------------------------------------------------------------------------------------------------------+
| 2 % 3              | Mod işlemini ifade eder, sonuç 2.                      						                             |
+--------------------+-------------------------------------------------------------------------------------------------------------------------------+
| -1       	     | Negatif sayıyı ifade eder.                                                     					             |
+--------------------+-------------------------------------------------------------------------------------------------------------------------------+

.. mchoice:: 3_3_1_intDiv_Q1
   :answer_a: 0
   :answer_b: 1
   :answer_c: 0.75
   :answer_d: 0.25
   :correct: c
   :feedback_a: Eski Python versiyonlarında eğer iki değerin ikisi de tam sayı ise, sonuç tam sayı çıkar. Ancak bu kitapta Python 3 versiyonu kullanılıyor dolayısıyla sonuç ondalık bir sayı olacaktır.
   :feedback_b: Eğer noktadan sonraki kısımlar atılmadan önce yuvarlanmış olsaydı bu sonuç doğru olurdu ancak böyle bir şey bu işlemde geçerli değil.  
   :feedback_c: Doğru. Eski Ptyhon versiyonu olmadığı için,  sonucun ondalık çıkması gerekiyor.
   :feedback_d: Eğer işlem bunlardan birisi olsaydı cevap 0.25 olurdu <code>1 / 4</code>, <code>1.0 / 4</code>, or <code>1 / 4.0</code>

   ``3 / 4`` işleminin sonucu nedir?
    
.. mchoice:: 3_3_2_mod_Q1
   :answer_a: 0
   :answer_b: 1
   :answer_c: 2
   :answer_d: 3
   :correct: d
   :feedback_a: Eğer işlem 18 % 2 olsaydı cevabın doğru olurdu. 
   :feedback_b: Eğer işlem 18 % 17 olsaydı cevabın doğru olurdu.  
   :feedback_c: 18’e en yakın 5’in katı olan sayı nedir? Kalan, 18 eksi o sayı olacaktır.
   :feedback_d: Doğru. 5, 18’in içinde 3 kez olduğundan (5x3 = 15) ve 18 - 15 = 3’e eşit olduğundan,  kalan 3 olacaktır. 

   ``18 % 5`` işleminin sonucu nedir?
   
.. mchoice:: 3_3_3_mod_Q2
   :answer_a: 0
   :answer_b: 1
   :answer_c: 2
   :answer_d: 6
   :correct: c
   :feedback_a: Eğer soru <code>6 % 2</code> olsaydı, bu cevap doğru olurdu  
   :feedback_b: Bu cevabın doğru olması için her hangi bir tek sayının 2’ye göre modunun alınması gerekirdi.
   :feedback_c: Doğru. 6, 2’nin içinde 0 defa vardır ve geriye 2 kalır 
   :feedback_d: Eğer küçük sayıyı büyük sayıya bölüyorsa kalan her zaman küçük sayıdır

   ``2 % 6`` işleminin sonucu nedir?


