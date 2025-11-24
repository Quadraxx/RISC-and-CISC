# CISC VE RISC MİMARİLERİ KARŞILAŞTIRMALI ANALİZ ÖDEVİ

## Kapak Bilgileri

**Ders Adı:** Bilgisayar Donanımı / Bilgisayar Mimarileri
**Konu:** CISC ve RISC Mimarileri Karşılaştırmalı Analizi
**Hazırlayan:** Hüseyin Akın
**Öğrenci Numarası:** [Kendi Öğrenci Numaranız]
**Okul/Bölüm:** Torul Meslek Yüksekokulu (Torul MYO)
**Tarih:** 24 Kasım 2025

---
## 1. GİRİŞ

Bilgisayar bilimlerinin temelini oluşturan işlemci mimarileri, CPU’nun (Merkezi İşlem Birimi) tasarımını ve komut setini (Instruction Set Architecture - ISA) belirler. Bu mimariler, işlemcinin komutları nasıl yorumlayacağını, belleğe nasıl erişeceğini ve veriyi nasıl işleyeceğini tanımlar. Temelde iki ana felsefe baskındır: **CISC (Complex Instruction Set Computer)** ve **RISC (Reduced Instruction Set Computer)**. Bu araştırma ödevi, karmaşık komut setlerinin kullanıldığı CISC mimarisini derinlemesine inceleyecek, ardından daha yalın yapıdaki RISC mimarisi ile karşılaştırarak modern bilgisayar sistemlerindeki rollerini analiz edecektir.

---
## 2. CISC (COMPLEX INSTRUCTION SET COMPUTER) MİMARİSİ

### 2.1. Tanım ve Tarihçe

CISC, Türkçe karşılığıyla **Karmaşık Komut Setine Sahip Bilgisayar** anlamına gelir. Bu mimarinin temel felsefesi, işlemciye tek bir komutla birden fazla düşük seviyeli görevi (örneğin bellekten veri yükleme, aritmetik işlem yapma ve sonucu kaydetme) gerçekleştirebilme yeteneği vermektir.

* **Motivasyon:** 1970'ler ve 1980'lerin başında geliştirilen CISC, o dönemdeki derleyicilerin basitliği ve belleğin kısıtlı olması nedeniyle programlama dillerindeki yüksek seviyeli yapılara (örneğin bir `STRING COPY` işlemi) doğrudan karşılık gelen komutlar sunmayı amaçlamıştır. Bu, program kodunun boyutunu küçülterek bellekten tasarruf sağlamıştır.
* **Örnekler:** Intel’in **x86** mimarisi (Pentium, Core serileri) CISC’in en bilinen örneğidir.

### 2.2. Komut Yapısı ve Adresleme

CISC komut setleri, yapılarının karmaşıklığı ile öne çıkar:

* **Değişken Komut Uzunluğu:** Komutlar, 1 bayttan 15 bayta kadar değişken uzunlukta olabilir. Bu, komutun çözümlenmesini (decode) zorlaştırır.
* **Bellek Merkezlilik:** Komutlar doğrudan bellek adresleri üzerinde işlem yapabilir (Bellek-Bellek veya Bellek-Yazmaç işlemleri). Örn: `ADD MEM1, REG1`.
* **Karmaşık Adresleme Kipleri:** Doğrudan, dolaylı, baz-endeksli gibi çok sayıda ve karmaşık adresleme kipleri mevcuttur.

### 2.3. Donanımsal Gerçekleştirme (Mikrokod)

CISC işlemcilerde karmaşık komutların yürütülmesi genellikle **Mikrokod (Microcode)** adı verilen bir mekanizma ile gerçekleştirilir.

* **Mikrokod:** Her karmaşık makine komutu, işlemci içindeki özel, küçük ve hızlı bir bellekte (Kontrol Belleği) saklanan daha basit mikro-işlemlerin bir dizisine çevrilir.
* **Kontrol Birimi:** Kontrol birimi, bir donanım devresi (kablolu mantık) yerine, bu mikrokod belleği tarafından yönetilir.

---
## 3. RISC (REDUCED INSTRUCTION SET COMPUTER) MİMARİSİ

### 3.1. Tanım ve Temel Felsefe

RISC, **Azaltılmış Komut Setine Sahip Bilgisayar** anlamına gelir. Bu mimari, CISC’in tam tersi bir felsefeyle, komut setini minimuma indirerek en sık kullanılan, en basit komutlara odaklanır.

* **Motivasyon:** RISC’in temel hedefi, her komutun **tek bir saat döngüsünde (cycle)** yürütülmesini sağlamaktır. Bu, işlemcinin tasarımını basitleştirir ve **Pipelining (Bantlama)** gibi hız artırıcı tekniklerin çok daha verimli kullanılmasına olanak tanır.
* **Örnekler:** ARM (akıllı telefonlar ve tabletler), PowerPC ve MIPS gibi mimariler.

### 3.2. Yapısal Özellikler

* **Sabit Komut Uzunluğu:** Tüm komutlar aynı uzunluktadır (genellikle 4 bayt). Bu, komutların çözümlenmesini basitleştirir ve Pipelining'i kolaylaştırır.
* **Yazmaç Merkezlilik:** İşlemlerin çoğu **yazmaçlar (registers)** arasında yapılır. Bellek erişimi sadece özel **LOAD (yükle)** ve **STORE (kaydet)** komutlarıyla gerçekleştirilir (Load/Store Mimarisi).
* **Çok Sayıda Yazmaç:** İşlemcinin belleğe olan bağımlılığını azaltmak için genellikle 32 veya daha fazla genel amaçlı yazmaç kullanılır.

---
## 4. CISC VE RISC KARŞILAŞTIRMASI

Aşağıdaki tablo, iki mimari arasındaki temel tasarım ve performans farklılıklarını özetlemektedir:

| Özellik | CISC (Complex Instruction Set Computer) | RISC (Reduced Instruction Set Computer) |
| :--- | :--- | :--- |
| **Komut Sayısı** | Çok sayıda karmaşık komut (100'den fazla). | Az sayıda basit komut (genellikle < 100). |
| **Komut Uzunluğu** | Değişken (1-15+ bayt). | Sabit (Genellikle 4 bayt). |
| **Saat Döngüsü** | Her komut için değişken döngü (>1 cycle/komut). | Çoğu komut için tek döngü (1 cycle/komut). |
| **Kontrol Birimi** | Mikrokod tabanlı (daha yavaş). | Tamamen donanım (kablolu mantık) tabanlı (daha hızlı). |
| **Bellek Erişimi** | Komutlar bellek üzerinde doğrudan işlem yapabilir. | Sadece özel LOAD/STORE komutları bellek erişimi yapar. |
| **Yazmaç Sayısı** | Az (genellikle 8-16). | Çok (genellikle 32+). |
| **Derleyici Rolü** | Daha az kritiktir, karmaşıklık donanımdadır. | Çok kritiktir, karmaşıklık derleyiciye yüklenmiştir. |

### 4.1. Avantaj ve Dezavantajlar

| Mimariler | Avantajlar | Dezavantajlar |
| :--- | :--- | :--- |
| **CISC** | **Daha Az Komut:** Program kodu daha kısadır. **Geriye Dönük Uyumluluk:** x86 standart haline gelmiştir. | **Yavaşlık:** Değişken döngü süresi ve Pipelining zorluğu. **Karmaşıklık:** İşlemci tasarımı daha karmaşıktır. |
| **RISC** | **Hız:** Sabit, tek döngülü komutlar sayesinde daha hızlıdır. **Güç Verimliliği:** Daha basit devreler sayesinde daha az güç tüketir (Mobil cihazlar için ideal). | **Daha Uzun Program Kodu:** Aynı işi yapmak için daha fazla komut gerekir. **Derleyici Zorluğu:** Daha karmaşık optimizasyon gerektirir. |

---
## 5. SONUÇ VE GÜNCEL DURUM

CISC ve RISC, ilk ortaya çıktıklarında birbirine zıt iki felsefeyi temsil etse de, günümüz modern işlemcileri bu ayrımı büyük ölçüde ortadan kaldırmıştır.

* **Modern x86 (CISC):** Intel ve AMD işlemcileri, dışarıdan (yani yazılımcı bakış açısıyla) CISC komutlarını kabul etmeye devam ederler (geriye dönük uyumluluk). Ancak bu karmaşık CISC komutları, işlemcinin içinde hızlı bir şekilde basit **mikro-işlemlere (micro-ops)** ayrılır. Bu mikro-işlemler daha sonra RISC mimarisine benzer şekilde, verimli Pipelining ve tek döngülü yürütme mantığıyla işlenir.
* **Sonuç:** Günümüzde en yaygın masaüstü ve sunucu işlemcileri, dışarıdan CISC olsa da, iç yapılarında RISC felsefesinin hız ve verimlilik avantajlarını kullanmaktadır. Mobil cihazlarda ise güç verimliliği nedeniyle saf RISC (ARM) mimarisi liderliğini sürdürmektedir.
