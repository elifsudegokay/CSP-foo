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
	:prefix: csp-3-6-

.. highlight:: java
   :linenothreshold: 4

Ketçap’ın Süzülmesini Takip Etmek
====================================

Ketçap’ın bir masaya doğru  süzülmesinin ne kadar süreceğini hesaplayalım. Dört ayaklı bir masayı eğdiğinizi ve üzerine tepeden ketçup döktüğünüzü düşünün. Masanın alt kısmına ketçup’ın ulaşması ne kadar sürer? Fiziği ve masanın eğimini ihmal ediyoruz ve ketçap ortalama saatte 0.028 mil hızla akmaya başlıyor.

.. figure:: Figures/ketchup.jpg
    :width: 200px
    :align: center
    :alt: A picture of ketchup dripping from a bottle
    :figclass: align-center

    Figure 2: Ketchup dripping speed

.. codelens:: Ketchup_Speed

   dripMPH = .028
   FPM = 5280.0
   dripFPH = dripMPH * FPM
   MPH = 60
   dripFPM = dripFPH / MPH
   print("Ketçap hızı (feet/dakika):")
   print(dripFPM)
   print("Dakikada 4 feet hareket etmek için ketçap hızı:")
   print(4 / dripFPM)

   
Bir sonraki sorunun türü yeni bir tane. Sol taraftaki kod blokları doğru kodları gösteriyor ama sıralaması karışık. Blokları sağ tarafa, doğru sırada sürükleyip bırakmanız gerekiyor. Lütfen doğru kullanım için aşağıdaki videoyu izleyin.
   
**Aşağıdaki videoyu oynatmak için aşağıdaki sağ oku tıklayın.**
   
.. video:: parsons
   :controls:
   :thumb: ../_static/MixedUpCodeVideoThumb.png

   http://ice-web.cc.gatech.edu/ce21/1/static/video/MixedUpCode.mov
   http://ice-web.cc.gatech.edu/ce21/1/static/video/MixedUpCode.webm

.. parsonsprob:: 3_6_1_Ketchup_Speed

   Aşağıdaki program, saniyede kaç feet hızla ketçap aktığını göstermektedir. Soldaki blokları sağa doğru doğru sırayla sürükleyip bırakın. Cevabınızı kontrol etmek için “Checck Me” butonuna basınız.
   -----
   dripMPH = .028
   FPM= 5280.0
   dripFPH = dripMPH * FPM
   =====
   MPH = 60
   dripFPM = dripFPH / MPH
   =====
   SPM = 60
   dripFPS = dripFPM / SPM
   =====
   print("Ketchup speed:")
   print(dripFPS)

