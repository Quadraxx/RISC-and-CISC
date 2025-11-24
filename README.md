# 🚀 CISC ve RISC Mimarileri: Kapsamlı Analiz ve Karşılaştırma Ödevi 💻

> **Akademik Çalışma:** Bilgisayar Donanımı Dersi Araştırma Ödevi 👨‍🏫
> **Hazırlayan:** Hüseyin Akın 🧑‍💻
> **Okul:** Torul Meslek Yüksekokulu (Torul MYO) 🏫
> **Tarih:** 24 Kasım 2025 🗓️

---

## 🎯 Projenin Amacı ve Kapsamı

Bu depo, modern işlemci mimarilerinin temelini oluşturan iki ana komut seti felsefesini, **CISC (Complex Instruction Set Computer)** ve **RISC (Reduced Instruction Set Computer)**'i, tarihsel gelişimden güncel uygulamalara kadar derinlemesine inceleyen kapsamlı bir akademik çalışmayı sunmaktadır. Çalışma, bu iki mimarinin teknik farklarını, performans etkilerini ve günümüz teknolojisindeki rollerini analiz etmeyi amaçlamaktadır. 🌍

---

## 1. GİRİŞ: Mimarilere Genel Bakış

İşlemci Mimarisi (**Instruction Set Architecture - ISA**), bir CPU’nun komutları nasıl yorumlayacağını ve yürüteceğini tanımlayan temel bir kavramdır. ISA'lar temelde **CISC** ve **RISC** olarak ikiye ayrılır.

* **CISC:** Tek bir komutla karmaşık görevleri (örneğin bellekten veri yükleme ve aritmetik işlem yapma) gerçekleştirme üzerine kuruludur.
* **RISC:** Komut setini minimuma indirerek, her komutun hızlı ve öngörülebilir bir şekilde yürütülmesini hedefler.

---

## 2. CISC (COMPLEX INSTRUCTION SET COMPUTER) MİMARİSİ 🧠

CISC, işlemciye tek bir komutla karmaşık görevler yükleyerek, karmaşıklığı donanıma devreden bir yaklaşımdır.

### 2.1. Temel Yapı ve Tarihçe ⏳

| Özellik | Açıklama |
| :--- | :--- |
| **Felsefe** | Daha az sayıda makine komutuyla daha kısa program kodu yazmak, bellek kullanımını optimize etmek. 💾 |
| **Donanım** | Komutlar, **Mikrokod (Microcode)** kullanan karmaşık bir kontrol birimi tarafından yürütülür. |
| **Komut Yapısı** | **Değişken uzunluklu** komutlar ve doğrudan **bellek adresleri üzerinde işlem yapabilme** yeteneği. |
| **Yaygın Örnek** | Intel **x86** mimarisi (Masaüstü ve Sunucu işlemcilerinin temelidir). 🖥️ |

### 2.2. Dezavantajları ❌

* Değişken komut uzunlukları ve karmaşık yürütme adımları nedeniyle, modern hız artırıcı teknikler olan **Pipelining (Bantlama)** ve **paralelizm** zorlaşır.
* Daha karmaşık donanım gerektirir ve bu da güç tüketimini artırabilir. 🔋

> **Görsel: CISC İşlemci Mimarisi Şeması**
> *(Buraya bir CISC işlemcinin temel bileşenlerini (kontrol ünitesi, ALU, yazmaçlar, mikrokod ROM) gösteren bir şema eklenebilir.)*
> 

---

## 3. RISC (REDUCED INSTRUCTION SET COMPUTER) MİMARİSİ 💨

RISC, basit ve optimize edilmiş komut setlerine odaklanarak, karmaşıklığı derleyiciye yükler.

### 3.1. Temel Yapı ve Motivasyon ✨

| Özellik | Açıklama |
| :--- | :--- |
| **Felsefe** | Her komutu mümkün olduğunca **tek bir saat döngüsünde** tamamlayarak hızı ve verimliliği artırmak. ⏱️ |
| **Donanım** | Kontrol birimi, hızlı **Kablolu Mantık (Hardwired Logic)** kullanır. |
| **Komut Yapısı** | Tüm komutlar **sabit uzunluktadır** ve bellek erişimi sadece **LOAD (yükle)** ve **STORE (kaydet)** komutlarıyla yapılır (**Load/Store Mimarisi**). 📥📤 |
| **Yaygın Örnek** | **ARM** mimarisi (Mobil cihazlar, tabletler, Apple M serisi çipleri). 📱 |

### 3.2. Avantajları ✅

* Basit komutlar, işlemci tasarımını basitleştirir ve daha az güç tüketimi sağlar.
* **Pipelining** tekniğinin maksimum verimle çalışmasına olanak tanıyarak yüksek performans sağlar.

> **Görsel: RISC İşlemci Mimarisi Şeması**
> *(Buraya bir RISC işlemcinin temel bileşenlerini (daha fazla yazmaç, basit kontrol ünitesi, LOAD/STORE birimleri) gösteren bir şema eklenebilir.)*
> 

---

## 4. CISC VE RISC KARŞILAŞTIRMASI 🆚

İki mimari arasındaki temel tasarım ve performans farklılıkları aşağıdaki tabloda özetlenmektedir:

| Özellik | CISC (Complex Instruction Set Computer) | RISC (Reduced Instruction Set Computer) | Sembol |
| :--- | :--- | :--- | :---: |
| **Komut Uzunluğu** | Değişken (1-15+ bayt) | Sabit (Genellikle 4 bayt) | 📏 |
| **Yürütme Süresi** | Her komut için değişken döngü (>1 cycle/komut) | Çoğu komut için tek döngü (1 cycle/komut) | ⏱️ |
| **Kontrol Birimi** | Mikrokod tabanlı (daha yavaş) | Tamamen donanım (kablolu mantık) tabanlı (daha hızlı) | ⚙️ |
| **Bellek Erişimi** | Komutlar bellek üzerinde doğrudan işlem yapabilir | Sadece özel LOAD/STORE komutları bellek erişimi yapar | 💾 |
| **Yazmaç Sayısı** | Az (genellikle 8-16) | Çok (genellikle 32+) | #️⃣ |
| **Güç Verimliliği** | Düşük | Yüksek (Mobil için ideal) | ⚡ |

---

## 5. SONUÇ VE GÜNCEL DURUM 🌐

### 5.1. Mimarilerin Yakınsaması 🤝

Günümüzdeki modern işlemcilerde bu iki felsefe büyük ölçüde birleşmiştir:

* Modern **x86 (CISC)** işlemcileri, dışarıdan gelen karmaşık CISC komutlarını içeride hızlıca basit **mikro-işlemlere (micro-ops)** ayırır.
* Bu mikro-işlemler, **RISC** prensiplerine benzer şekilde verimli **Pipelining** ve tek döngülü yürütme mantığıyla işlenir.
* Bu sayede, CISC **geriye dönük uyumluluk** avantajını korurken, RISC'in **hız ve verimlilik** avantajlarını kullanabilir.

### 5.2. Pazar Hakimiyeti 📈

* **Masaüstü ve Sunucu:** CISC (x86) geriye dönük uyumluluk nedeniyle liderliğini sürdürmektedir.
* **Mobil ve Gömülü Sistemler:** RISC (ARM) üstün güç verimliliği nedeniyle standarttır.

> **Görsel: Modern İşlemcilerin Hibrit Mimarisi**
> *(Buraya, CISC komutlarının nasıl mikro-ops'lara dönüştürüldüğünü ve bir RISC çekirdeğinde işlendiğini gösteren bir şema eklenebilir.)*
> 

---

## 6. KAYNAKÇA 📚

Bu ödevin hazırlanmasında kullanılan akademik kaynaklar ve referanslar aşağıdadır:

* [Patterson, D. A., & Hennessy, J. L. (2017). *Computer Organization and Design: The Hardware/Software Interface*. Morgan Kaufmann.]
* [Stalling, W. (2018). *Computer Organization and Architecture: Designing for Performance*. Pearson.]
* [Kullanılan diğer ders notları ve internet kaynakları buraya eklenmelidir. Lütfen bu bölümü kendi kaynaklarınızla güncelleyin.]

---
