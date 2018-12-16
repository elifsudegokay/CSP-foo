.. qnum::
   :prefix: 2-5-
   :start: 1
   
Değerlendirme Soruları
-------------------------------------

Aşağıdaki sorular, 1. Ve 2. Bölümlerde öğrendiğiniz konuları içermektedir. Test için hazır olduğunuzda “Start” (Başlat) butonuna tıklayınız. Testi durdurmak için “Pause” (Durdur) butonuna tıklayınız (Test durdurulduğunda soruları göremeyeceksiniz). Ne kadar zaman kullandığınızı görebileceksiniz fakat sınırsız zamanınız var. Soruları bitirdiğinizde sayfanın sonundaki “Finish Exam” (Testi Sonlandır)’a tıklayınız. Doğru sayısı, yanlış sayısı ve geçilmiş soru sayısı sayfanın alt bölümünde gösterilmektedir. Yanlış işaretlediğiniz sorularda cevabınız ile birlikte doğru seçenek de gösterilecektir. 

“Finish Exam” (Testi Sonlandır) butonuna tıkladıktan sonra cevaplarınızı değişteremeyeceksiniz. 

.. timed:: ch1a2ex
    
    .. mchoice:: e1a2_1
       :answer_a: köpek
       :answer_b: balık
       :answer_c: kedi
       :answer_d: kuş
       :correct: a
       :feedback_a: Doğru.var3'ün değeri ilk olarak "kuş" olarak ayarlanmıştır, ancak daha sonra var1 değeri olarak değiştirilmiştir. var1'in değeri ilk olarak "kedi" olarak ayarlanır, ancak daha sonra "köpek" olarak ayarlanmış olan var2'nin değerine değiştirilir.
       :feedback_b: Yanlış. Sadece var2 "balık" değerine sahiptir. Bir değişkenin değerini başka bir değişkenin değerine atadığınızdaa, değer yeni değişkene kopyalanır. İki değişken arasında ilişki kurulmamıştır. 
       :feedback_c: Yanlış. var3'ün değeri ilk olarak "kuş" olarak ayarlanmıştır, ancak daha sonra var1 değeri olarak değiştirilmiştir. Bununla birlikte, var1 değeri de orijinal olarak ayarlandıktan sonra değiştiirlir. 
       :feedback_d: Yanlış. var3 orjinal olarak "kuş" olarak ayarlanmışsa da değer olarak daha sonra değiştirilir. 

       Aşağıdaki kod dizinini çalıştırdığınızda var3 değişkinenin değeri ne olacaktır?
       
       ::
       
          var1 = "kedi" 
          var2 = "köpek"
          var3 = "kuş"
          var1 = var2
          var3 = var1
          var2 = "balık"
           
    .. mchoice:: e1a2_2
       :answer_a: variable (değişken)
       :answer_b: turtle (kaplumbağa)
       :answer_c: string (karakter dizisi)
       :answer_d: program
       :correct: a
       :feedback_a: Doğru. Değişken, bir değeri tutan bilgisayar belleği ile ilişkilendirilmiştir.
       :feedback_b:  Yanlış. Bir kaplumbağa ileriye doğru hareket edebilen ve değişebilen bir nesnedir. Hareket ettikçe bir kalemle çizilebilir.
       :feedback_c: Yanlış. String bir karakter dizisidir.
       :feedback_d: Yanlış. Program, bilgisayarın yürütebileceği komutlardır.   

       Aşağıdakilerden hangisine bir değer atanabilir?
           
    .. mchoice:: e1a2_3
       :answer_a: integer
       :answer_b: turtle
       :answer_c: string
       :answer_d: image (resim)
       :correct: c
       :feedback_a: Yanlış. integer bir tam sayıdır.   
       :feedback_b: Yanlış. Bir kaplumbağa ileriye doğru hareket edebilen ve değişebilen bir nesnedir. Hareket ettikçe bir kalemle çizilebilir. 
       :feedback_c: Doğru. String bir karakter dizisidir.
       :feedback_d: Yanlış. Görüntü, dijital resmin bir temsilidir ve görüntüdeki piksellerden renk değerlerini alabilir ve değiştirebilirsiniz. 

       Aşağıdakilerden hangisine tek veya çift tırnak içerisinde harf, sayı ve başka karakterler içerebilen türde bir veri atanabilir?
           
    .. mchoice:: e1a2_4
       :answer_a: 3
       :answer_b: 2
       :answer_c: 5
       :answer_d: 0
       :correct: b
       :feedback_a: Yanlış. Bu var1'in orjinal değeridir. var2'nin değeri nedir? 
       :feedback_b: Doğru. var1, var2 ile aynı değere sahip olduğunda, var2'den gelen değer kopyalanır ve değiştirilmez.
       :feedback_c: Yanlış. Bu var3'ün orjinal değeridir. var2'nin değeri nedir? 
       :feedback_d: Yanlış. Bir değişken (var1) diğerinin (var2) değerine atandığında değeri diğerinden kopyalar (var2). Diğerindeki değeri değiştirmez (var2).

       Aşağıdaki kod dizinini çalıştırdığınızda var2 değişkinenin değeri ne olacaktır?
   
       ::
       
          var1 = 3 
          var2 = 2
          var3 = 5
          var1 = var2
           
    .. mchoice:: e1a2_5
       :answer_a: Kare
       :answer_b: Uzunluğu genişliğinden fazla olan bir dikdörtgen
       :answer_c: Elmas
       :answer_d: Genişliği, uzunluğundan fazla olan bir dikdörtgen 
       :correct: b
       :feedback_a: Yanlış. Ama eğer tüm ilerlemeler (forwardlar) aynı olsaydı doğru olurdu. 
       :feedback_b: Doğru. Zari'nin pozisyonu, onu kuzey yönüne çeviren 90'a ayarlandı. Yani, dikdörtgenin uzunluğu genişliğinden daha fazla. 
       :feedback_c: Yanlış. Tüm ilerlemeler (forward) aynı olsaydı ve 45 derece olsaydı başlansaydı bu doğru olurdu.
       :feedback_d: Yanlış. Kaplumbağalar, varsayılan olarak doğuya doğru yola çıkarlar ve yönlerini 90 derece kuzeye çevirirler. 

       Aşağıdaki kod dizini hangi şekli çizer?
       
       ::
       
         from turtle import *        # turtle (kaplumbağa kütüphanesini kullan)
         space = Screen()            # turtle ekranı (Screen) yarat
         zari = Turtle()             # zari adında bir turtle (kaplumbağa) yarat. 
         zari.setheading(90)         
         zari.forward(100)           # zari'ye 100 birim ilerlemesini söyle
         zari.right(90)              # zari 90 derece sağa dönsün. 
         zari.forward(50)           # zari'ye 50 birim ilerlemesini söyle
         zari.right(90)              # zari 90 derece sağa dönsün.
         zari.forward(100)           # zari'ye 100 birim ilerlemesini söyle
         zari.right(90)              # zari 90 derece sağa dönsün.
         zari.forward(50)           # zari'ye 50 birim ilerlemesini söyle
         zari.right(90)              # zari 90 derece sağa dönsün.
    

   
