[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/7TXVPuTD)
### 1 – Why we need to use OOP ? Some major OOP languages ?
--- 
OOP(Nesne tabanlı programlama), modüler, ölçeklenebilir ve bakımı kolay yazılımlar geliştirmek için kullanılır. Örneğin Java, C#, C++ ve Python OOP dilleridir.

### Interface vs Abstract class ?
---
Interface bir soyut class'dır ve implemente edilir, birden fazla implementasyonu destekler. Tüm methodlar public'dir. İçerisindeki field'ler final ve static'tir. Abstrack ise methodu veya sınıfı soyutlaştırır, inherit edildiği sınıflardan abstrack methodların body tanımlamasını zorunlu kılar. Değişken tanımlanabilir ve erişim istenildiği gibi belirlenebilir. Interface ve abstrack classlardan object tanımlanamaz yani new ile nesne oluşturulamaz.

### Why wee need equals and hashcode ? When to override ?
---
Hashcode ve equals nesneleri karşılaştırmak ve hızlı aram yapmak için kullanılır. Hashcode içeriğine göre benzersiz bir sayısal numara döner. Map veri yapısında çok daha hızlı arama yapmayı sağlar. Equals ise bellekteki adresleri karşılaştırır. Yani referans adresleri aynı mı diye kontrol eder. 
Override edilmezseler bazı sorunlar yaşanabilir, değerler aynı olsa bile equals bellek adresleri farklı oldukları için false döner, bu durumu kendimiz ele alarak equals methodunu yeniden yapılandırarak çözüme gideriz. Hashcode ise aynı içeriğe sahip farklı hashcode'a sahip olan veriler collections'ları bozabilir. Bu istisnaların önüne geçmek için override ile spesifik durumlara dayanıklı hale getiririz.

### Diamon problem in Java ? How to fix it?
--- 
Bir sınıf birden fazla parent class'ı extends ile inherit ederse ve o parent class'larda aynı isimde field'lar varsa, sub class bu isimde bir çağrı yaptığında hangi parent class içeriğiyle hareket edeceğini belirleyemez. Bu durum diamond problem olarak adlandırılır.
Bu durumu bir sınıfa bir yalnız bir sınıf extends ederek çözeriz, böylelikle inherit edilen içerikler çakışmaz. Java’da diamond problem Interface'lerde default metodlarla, C++’da virtual inheritance ile çözülür.

### Why we need Garbagge Collector ? How does it run ?
---
Kullanılmayan nesneleri temizleyerek memory leak durumlarının önüne geçer. Daha verimli çalışma sağlar.
Javada garbage collector otomatik çalışır, jvm içinde çalışır ve erişilmeyen nesneleri bellekte yer tutmasını engeller.


### Java ‘static’ keyword usage ?
---
Java static, değişmeyen ve o class yapısının sabiti olarak tanımlama yapmamızı sağlar. Class ile içerisindeki static değerlere doğrudan yani nesne oluşturmadan erişebiliriz. Static değişken bellekte yalnızca bir kez oluşturulur.

### 7 – Immutability means ? Where, How and Why to use it ?
---
Immutability oluşturulduktan sonra değiştirilemez anlamında gelir. String Integer gibi sınıflar immutable'dır. 
Hasas veri yapılarında ve eşzamanlı çalışan çok çekirdekli yapılarda kullanılır.
Nesne, final ve private değişkenlerle oluşturulur.

### 8 – Composition and Aggregation means and differences ?
---
Composition ve Aggregation has-a ilişkilerinin türleridir. Composition bağımlılığın daha sıkı olduğu yapıdır, o nesne bulunduğu yapı için olmazsa olmaz anlamında gelir. Aggregation ise daha esnektir, daha zayıf bağımlılık.

### 9 – Cohesion and Coupling means and differences ?
---
Cohesion (Bağlılık), bir modülün tek bir amaca ne kadar odaklandığını ifade eder; yüksek cohesion iyidir çünkü kod daha düzenli ve sürdürülebilir olur. Coupling (Bağımlılık), bir modülün başka bir modüle ne kadar bağımlı olduğunu gösterir; gevşek coupling iyidir çünkü sistem daha esnek ve değiştirilebilir hale gelir. 

### 10 - Heap and Stack means and differences ?
---
Heap, nesnelerin tutulduğu ve kalıcı içeriklerin olduğu yer, Stack geçici değerlerin olduğu bellek bölgesidir.

### 11 – Exception means ? Type of Exceptions ?
---
Exception'lar, program çalışırken oluşabilecek hata durumlarını ele almak için kullanılır. try-catch blokları ile işlenir. Checked (SQLException, IOException) ve Unchecked (RuntimeException) olmak üzere ikiye ayrılır.

### 12 – How to summarize ‘clean code’ as short as possible ?
---
Clean Code, yazılan kodun diğer geliştiriciler tarafından kolaylıkla anlaşılabilir olması, yapıların basit hallerde kurulması, açıklayıcı ve kısa yorum satırlarının bulunması gibi özellikleri taşıyan kodlara denir. Tek cümle ile Basit, anlaşılır, bakımı kolay ve gereksiz karmaşıklıktan arındırılmış koddur.

### 13 - What is the method of hiding in Java ?
---
Method of hiding parent class'ın static methodlarını sub classlarda gizleyebilir ama override edilemez. non-static methodlar override edilebilir ama static methodlar edilemez, oluşabilecek diğer durumlar için hiding kullanılır. Statik methodlar nesnenin referans türünden gelir.

### 14 - What is the difference between abstraction and polymorphism in Java ?
---
Abstraction'ın amacı kullanıcıya karmaşıklığı hissettirmeden bir nesnenin ne yaptığını göstermek, ancak nasıl yaptığını saklamak. Polymorphism'in amacı farklı sınıfların aynı metod ismi ile farklı davranışlar sergilemesini sağlamak. İkisi de bir arada kullanılabilir.
