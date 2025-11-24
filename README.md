# 🚀 CISC ve RISC Mimarileri: Kapsamlı Analiz ve Karşılaştırma Ödevi

> **Akademik Çalışma:** Bilgisayar Donanımı Dersi Araştırma Ödevi
> **Hazırlayan:** Hüseyin Akın
> **Okul:** Torul Meslek Yüksekokulu (Torul MYO)
> **Tarih:** 24 Kasım 2025

---

## 🎯 Proje Özeti ve Kapsamı

Bu depo, modern işlemci mimarilerinin temelini oluşturan **CISC (Complex Instruction Set Computer)** ve **RISC (Reduced Instruction Set Computer)** felsefelerini derinlemesine inceleyen bir akademik çalışmayı sunmaktadır. Çalışma, iki mimarinin tarihsel gelişimini, donanımsal yapılarını, kritik farklılıklarını ve günümüz teknolojilerindeki rollerini analiz etmektedir.

---

## 1. GİRİŞ: Mimarilere Genel Bakış

İşlemci Mimarisi (**Instruction Set Architecture - ISA**), bir CPU’nun komutları nasıl yorumlayacağını ve yürüteceğini tanımlar. ISA'lar temelde **CISC** ve **RISC** olarak ikiye ayrılır.

* **CISC:** Tek bir komutla karmaşık görevleri (örneğin bellekten veri yükleme ve aritmetik işlem yapma) gerçekleştirme üzerine kuruludur.
* **RISC:** Komut setini minimuma indirerek, her komutun hızlı ve öngörülebilir bir şekilde yürütülmesini hedefler.

---

## 2. CISC (COMPLEX INSTRUCTION SET COMPUTER) MİMARİSİ

CISC, **karmaşık komut setine** odaklanır ve karmaşıklığı donanıma yükler.

### 2.1. Temel Yapı ve Tarihçe

| Özellik | Açıklama |
| :--- | :--- |
| **Felsefe** | Daha az sayıda komutla daha kısa program kodu yazmak. |
| **Donanım** | Komutlar, **Mikrokod (Microcode)** kullanan kontrol birimi tarafından yürütülür. |
| **Komut Yapısı** | **Değişken uzunluklu** komutlar ve bellek merkezli işlemler. |
| **Yaygın Örnek** | Intel **x86** mimarisi (Masaüstü ve Sunucular). |

### 2.2. Dezavantajları

Değişken komut uzunlukları ve karmaşık yürütme adımları nedeniyle, modern hız artırıcı teknikler olan **Pipelining (Bantlama)** ve **paralelizm** zorlaşır.

---

## 3. RISC (REDUCED INSTRUCTION SET COMPUTER) MİMARİSİ

RISC, **azaltılmış komut setine** odaklanır ve karmaşıklığı derleyiciye yükler.

### 3.1. Temel Yapı ve Motivasyon

| Özellik | Açıklama |
| :--- | :--- |
| **Felsefe** | Her komutu **tek bir saat döngüsünde** tamamlama yeteneği. |
| **Donanım** | Kontrol birimi, hızlı **Kablolu Mantık (Hardwired Logic)** kullanır. |
| **Komut Yapısı** | **Sabit uzunluklu** komutlar ve **Load/Store Mimarisi** (Bellek erişimi sadece yükleme/kaydetme komutlarıyla yapılır). |
| **Yaygın Örnek** | **ARM** (Mobil cihazlar, tabletler, Apple M serisi). |

### 3.2. Avantajları

Basit komutlar, işlemci tasarımını basitleştirir, daha az güç tüketimi sağlar ve **Pipelining** tekniğinin maksimum verimle çalışmasına olanak tanır.

---

## 4. CISC VE RISC KARŞILAŞTIRMASI

Aşağıdaki tablo, iki mimari arasındaki temel tasarım ve performans farklılıklarını özetlemektedir:

| Özellik | CISC (Complex Instruction Set Computer) | RISC (Reduced Instruction Set Computer) |
| :--- | :--- | :--- |
| **Komut Uzunluğu** | Değişken (1-15+ bayt). | Sabit (Genellikle 4 bayt). |
| **Yürütme Süresi** | Değişken döngü (>1 cycle/komut). | Çoğu komut için **tek döngü** (1 cycle/komut). |
| **Kontrol Birimi** | Mikrokod tabanlı. | Tamamen donanım (kablolu mantık) tabanlı. |
| **Yazmaç Sayısı** | Az (genellikle 8-16). | Çok (genellikle 32+). |
| **Güç Verimliliği** | Düşük. | Yüksek (Mobil için ideal). |

---

## 5. SONUÇ VE GÜNCEL DURUM

### 5.1. Mimarilerin Yakınsaması

Günümüzdeki modern işlemcilerde bu iki felsefe büyük ölçüde birleşmiştir:

* Modern **x86 (CISC)** işlemcileri, dışarıdan gelen karmaşık CISC komutlarını içeride hızlıca basit **mikro-işlemlere (micro-ops)** ayırır. Bu mikro-işlemler, **RISC** prensiplerine benzer şekilde hızlı bir şekilde yürütülür.
* Bu sayede, CISC **geriye dönük uyumluluk** avantajını korurken, RISC'in **hız ve verimlilik** avantajlarını kullanabilir.

### 5.2. Pazar Hakimiyeti

* **Masaüstü ve Sunucu:** CISC (x86) geriye dönük uyumluluk nedeniyle liderliğini sürdürmektedir.
* **Mobil ve Gömülü Sistemler:** RISC (ARM) üstün güç verimliliği nedeniyle standarttır.

---

## 6. KAYNAKÇA

Bu ödevin hazırlanmasında kullanılan akademik kaynaklar ve referanslar aşağıdadır:

* [Patterson, D. A., & Hennessy, J. L. (2017). *Computer Organization and Design: The Hardware/Software Interface*.]
* [Stalling, W. (2018). *Computer Organization and Architecture: Designing for Performance*.]
* [Kullanılan diğer ders notları ve internet kaynakları buraya eklenmelidir.]

---

Bu README.md dosyası, ödevinizin akademik standartlara uygun, bilgilendirici ve görsel olarak temiz bir tanıtımını sağlar.
