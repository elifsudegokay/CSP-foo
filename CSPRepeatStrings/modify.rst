..  Copyright (C)  Mark Guzdial, Barbara Ericson, Briana Morrison
    Permission is granted to copy, distribute and/or modify this document
    under the terms of the GNU Free Documentation License, Version 1.3 or
    any later version published by the Free Software Foundation; with
    Invariant Sections being Forward, Prefaces, and Contributor List,
    no Front-Cover Texts, and no Back-Cover Texts.  A copy of the license
    is included in the section entitled "GNU Free Documentation License".
    
.. |audiobutton| image:: Figures/start-audio-tour.png
    :height: 20px
    :align: top
    :alt: audio tour button

.. 	qnum::
	:start: 1
	:prefix: csp-9-4-
	
.. highlight:: java
   :linenothreshold: 4


Metin Değiştirme
===============

Karakter dizileri üzerinde döngü kurup onları ``find`` ve slice ``[:]`` kullanarak değiştirebilir ve bölebiliriz.

.. We can loop through the string and modify it using ``find`` and slice (substring).

Google kitapları dijitalleştiriyor.Ancak, dijitalleştiriciler bazen hata yapar ve ``i`` harfi için ``1`` kullanırlar. Sıradaki program bir karakter dizisi içindeki her ``1`` karakterini ``i`` ile değiştiriyor. Şimdi siz her ``1`` ’i ``i`` ile gerçekten değiştirmek istemeyebilirsiniz ama bu konuyu şu anlık dert etmeyin. Bu program while döngüsü kullanıyor, çünkü döngüyü kaç kere döndürdüğümüzü bilmiyoruz.

.. Google has been digitizing books.  But, sometimes the digitizer makes a mistake and uses 1 for i.  The following program replaces ``1`` with ``i`` everywhere in the string.  Now you might not want to really replace every ``1`` with ``i``, but don't worry about that right now.  It uses a ``while`` loop since we don't know how many times it will need to loop.


.. codelens:: Birleri_Degistir
    :question: What is the value of pos after the line with the red arrow executes?
    :breakline: 5
    :feedback: Remember that find returns the starting index if the target string is found and -1 if not.  
    :correct: globals.pos
	
    cumle = "Bu b1r d1z1"
    pozisyon = cumle.find("1")
    while pozisyon >= 0:
        cumle = cumle[0 : pozisyon] + "i" + cumle[pozisyon + 1 : len(cumle)]
        pozisyon = cumle.find("1")
    print(cumle)
    
Sadece bir karakteri değiştirmek zorunda değilsiniz. Bir kelimenin her karakterini başka karakter(ler) ile değiştirebilirsiniz. Mesela yanlış yazdığınız bir kelimeyi her yerde değiştirmek istiyorsunuz.

.. codelens:: Kelimeleri_Degistir
    :question: What is the value of pos after the line with the red arrow executes?
    :breakline: 6
    :feedback: Remember that find returns the starting index if the target string is found and -1 if not.  
    :correct: globals.pos
	
    cumle = "Dersi laboratuar da yaptık"
    cumle = cumle + " ama laboratuar da bilgisayar bozuktu."
    pozisyon = cumle.find("laboratuar")
    while pozisyon >= 0:
        cumle=cumle[0 : pozisyon] + "laboratuvar" + cumle[pozisyon + len("laboratuar") : len(cumle)]
        pozisyon = cumle.find("laboratuar")
    print(cumle)
    
Can you loop through and encode a string to hide the contents of the message?

.. codelens:: Mesaj_Sifrele
	
    mesaj = "gece yarisi benimle bulus"
    cumle = "abcdefghijklmnopqrstuvwxyz. "
    eCumle = "zyxwvutsrqponmlkjihgfedcba ."
    esifreliMesaj = ""
    for karakter in mesaj:
        pozisyon = cumle.find(karakter)
        sifreliMesaj = sifreliMesaj + eCumle[pozisyon : pozisyon + 1]
    print("şifreli mesaj: " , sifreliMesaj)


.. mchoice:: 9_4_1_replace_m
   :answer_a: a
   :answer_b: d
   :answer_c: w
   :answer_d: v
   :correct: d
   :feedback_a: Yanlış. cumle'deki harf, eCumle'de aynı konumda bulunan harfle değiştirilir.
   :feedback_b: Yanlış. cumle'deki harf, eCumle'de aynı konumda bulunan harfle değiştirilir.
   :feedback_c: Yanlış. eCumle de kac harf olduğunu anlamak için cumle de ki harfleri say.
   :feedback_d: Doğru. e harfi cumle içinde 4 pozisyonundadır ve eCumle'deki pozisyon 4'teki v harfi ile değiştirilecektir.

   Mesaj kodlandığında e harfi hangi karakter ile değiştirilir?

.. mchoice:: 9_4_2_encodeMess1
   :answer_a: ""
   :answer_b: "o"
   :answer_c: "n"
   :answer_d: "m"
   :correct: c
   :feedback_a: Yanlış. Boş dize olarak başlar, ancak döngü boyunca her seferinde bir harf eklenir. 
   :feedback_b: Yanlış. cumle'deki harf, eCumle'de aynı konumda bulunan harfle değiştirilir.
   :feedback_c: Doğru. eCumle deki t harfi ile cumle deki g harfi aynı pozisyondadır.
   :feedback_d: Yanlış. Hatırla, eCumle de belirtilen pozisyon daki hrfi sifreliMesaj’a ekliyoruz cumle deki harfleri değil

   Döngü ilk kez çalıştırıldıktan sonra sifreliMesaj değeri nedir?

.. parsonsprob:: 9_4_3_Sifreyi_Coz

   Aşağıdaki program şifrelenmiş mesajı çözer fakat satırlar karışık verilmiş. Verilen satırları doğru şekilde ve sırada girintileyerek düzeltiniz.
   -----
   mesaj = ""
   cumle = "abcdefghijklmnopqrstuvwxyz. "
   eCumle = "zyxwvutsrqponmlkjihgfedcba ."
   sifreliMesaj = "tvxv.bzirhr.yvmov.yfofh"
   =====
   for karakter in sifreliMesaj:
   =====
       pozisyon = eCumle.find(karakter)
   =====
       mesaj = mesaj + cumle[pozisyon : pozisyon + 1]
   =====
   print(mesaj)

.. tabbed:: 9_4_4_WSt

    .. tab:: Soru

       ‘Bu 0t0bus c0k hizli y0l aliy0r’ karakter dizisinde her “0” karaketerini “o” harfi ile değiştiren bir  kod yazınız

       .. activecode::  9_4_4_WSq
            :nocodelens:

    .. tab:: Cevap

      .. activecode::  9_4_4_WSa
          :nocodelens:
          
          cumle = "Bu 0t0bus c0k hizli y0l aliy0r"
          # Pozisyon degiskeninin değerini 0’a eşit yada 0’dan büyük  olacak şekilde ayarlayın
          pozisyon = 1
          # while döngü sartını belirleyin
          while pozisyon >= 0:
              # Degeri Degistir
              pozisyon = cumle.find("0")
              if pozisyon == -1:
                break
              cumle = cumle[0 : pozisyon] + "o" + cumle[pozisyon + 1 : len(cumle)]
          # Sonucu Yazdir
          print(cumle)
            







.. Change_Ones
..    :question: What is the value of pos after the line with the red arrow executes?
  ..  :breakline: 5
    .. :feedback: Remember that find returns the starting index if the target string is found and -1 if not.  
  ..  :correct: globals.pos
	
..    str = "Th1s is a str1ng"
..    pos = str.find("1")
..    while pos >= 0:
..        str = str[0:pos] + "i" + str[pos+1:len(str)]
..        pos = str.find("1")
..    print(str)
    
.. You don't have to replace just one character.  You could replace every instance of a word with another word.  For example, what if you spelled a word wrong and wanted to change it everywhere?

.. Change_Word
..    :question: What is the value of pos after the line with the red arrow executes?
..    :breakline: 6
..    :feedback: Remember that find returns the starting index if the target string is found and -1 if not.  
..    :correct: globals.pos
	
 ..   str = "He wanted a peice of candy"
  ..  str = str + " so he gave her a peice."
 ..   pos = str.find("peice")
 ..   while pos >= 0:
 ..       str = str[0:pos] + "piece" + str[pos+len("peice"):len(str)]
 ..       pos = str.find("peice")
 ..   print(str)
    
.. Can you loop through and encode a string to hide the contents of the message?

.. Encode_String
	
  ..  message = "meet me at midnight"
  ..  str = "abcdefghijklmnopqrstuvwxyz. "
  ..  eStr = "zyxwvutsrqponmlkjihgfedcba ."
  ..  encodedMessage = ""
  ..  for letter in message:
  ..      pos = str.find(letter)
  ..      encodedMessage = encodedMessage + eStr[pos:pos+1]
  ..  print(encodedMessage)


..  9_4_1_replace_m
..   :answer_a: a
  ..  :answer_b: d
..   :answer_c: w
..   :answer_d: v
..   :correct: d
..   :feedback_a: The letter in str is replaced with the letter at the same position in eStr.
..   :feedback_b: The letter in str is replaced with the letter at the same position in eStr.
..   :feedback_c: Try counting the letters in str to figure out how many letters to count in eStr.
..   :feedback_d: The letter e is at position 4 in str and will be replaced with the letter v at position 4 in eStr.

 ..  What character is e replaced with when the message is encoded?

..  9_4_2_encodeMess1
..   :answer_a: ""
..   :answer_b: "o"
..   :answer_c: "n"
..   :answer_d: "m"
..   :correct: c
..   :feedback_a: It starts out as the empty string, but a letter is added each time through the loop.
..   :feedback_b: The letter in str is replaced with the letter at the same position in eStr.
 ..  :feedback_c: The letter in eStr at the same position as the m in str is n.
 ..  :feedback_d: Notice that we are adding the letter in eStr at pos not the letter in str at pos.

..   What is the value of encodedMessage after the loop executes the first time?  

.. : 9_4_3_Decode_String

..   The program below decodes an encoded message, but the lines are mixed up.  Put the lines in the right order with the right indentation.
..   -----
..   message = ""
..   str = "abcdefghijklmnopqrstuvwxyz. "
 ..  eStr = "zyxwvutsrqponmlkjihgfedcba ."
..   encodedMessage = "nvvg.nv.zg.nrwmrtsg"
..   =====
..   for letter in encodedMessage:
..   =====
..       pos = eStr.find(letter)
..   =====
       message = message + str[pos:pos+1]
..   =====
..   print(message)

..  9_4_4_WSt

.. : Question

..       Write the code to replace every 0 with o in the given string 'The 0wl h00ts l0udly'. 

       ..   9_4_4_WSq
            :nocodelens:

..     Answer

      .. a  9_4_4_WSa
          :nocodelens:
          
          str = "The 0wl h00ts l0udly"
          # SET POS TO A VALUE GREATER THAN OR EQUAL TO 0
          pos = 1
          # SET WHILE CONDITION
          while pos >= 0:
              # REPLACE VALUE
              pos = str.find("0")
              if pos == -1:
                break
              str = str[0:pos] + "o" + str[pos+1:len(str)]
          # PRINT RESULT
          print(str)
            



