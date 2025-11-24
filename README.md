# 🚀 CISC ve RISC Mimarileri: Kapsamlı Analiz ve Karşılaştırma Ödevi 💻

> **Akademik Çalışma:** Bilgisayar Donanımı Dersi Araştırma Ödevi 👨‍🏫
> **Hazırlayan:** Hüseyin Akın 🧑‍💻
> **Okul:** Torul Meslek Yüksekokulu (Torul MYO) 🏫
> **Tarih:** 24 Kasım 2025 🗓️

---

## 🎯 Projenin Amacı ve Kapsamı

Bu depo, modern işlemci mimarilerinin temelini oluşturan iki ana komut seti felsefesini, **CISC (Complex Instruction Set Computer)** ve **RISC (Reduced Instruction Set Computer)**'i, tarihsel gelişimden güncel uygulamalara kadar derinlemesine inceleyen kapsamlı bir akademik çalışmayı sunmaktadır.

---

## 1. GİRİŞ: Mimarilere Genel Bakış

İşlemci Mimarisi (**Instruction Set Architecture - ISA**), bir CPU’nun komutları nasıl yorumlayacağını ve yürüteceğini tanımlar. ISA'lar temelde **CISC** ve **RISC** olarak ikiye ayrılır.

---

## 2. CISC (COMPLEX INSTRUCTION SET COMPUTER) MİMARİSİ 🧠

CISC, tek bir komutla karmaşık görevler yükleyerek, karmaşıklığı donanıma devreden bir yaklaşımdır.

### 2.1. Temel Yapı ve Tarihçe ⏳

| Özellik | Açıklama |
| :--- | :--- |
| **Felsefe** | Daha az sayıda makine komutuyla daha kısa program kodu yazmak, bellek kullanımını optimize etmek. 💾 |
| **Donanım** | Komutlar, **Mikrokod (Microcode)** kullanan karmaşık bir kontrol birimi tarafından yürütülür. |
| **Komut Yapısı** | **Değişken uzunluklu** komutlar ve doğrudan **bellek adresleri üzerinde işlem yapabilme** yeteneği. |
| **Yaygın Örnek** | Intel **x86** mimarisi (Masaüstü ve Sunucu işlemcilerinin temelidir). 🖥️ |

> **Görsel: CISC İşlemci Mimarisi Şeması**
> ![CISC Mimarisi](https://www.watelectronics.com/wp-content/uploads/CISC-Architecture.jpg)
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

---

## 4. CISC VE RISC KARŞILAŞTIRMASI 🆚

| Özellik | CISC (Complex Instruction Set Computer) | RISC (Reduced Instruction Set Computer) | Sembol |
| :--- | :--- | :--- | :---: |
| **Komut Uzunluğu** | Değişken (1-15+ bayt) | Sabit (Genellikle 4 bayt) | 📏 |
| **Yürütme Süresi** | Değişken döngü (>1 cycle/komut) | Çoğu komut için **tek döngü** (1 cycle/komut) | ⏱️ |
| **Kontrol Birimi** | Mikrokod tabanlı. | Tamamen donanım (kablolu mantık) tabanlı. | ⚙️ |
| **Bellek Erişimi** | Komutlar bellek üzerinde doğrudan işlem yapabilir. | Sadece özel LOAD/STORE komutları bellek erişimi yapar. | 💾 |
| **Yazmaç Sayısı** | Az (genellikle 8-16) | Çok (genellikle 32+) | #️⃣ |
| **Güç Verimliliği** | Düşük. | Yüksek (Mobil için ideal). | ⚡ |

---

## 5. SONUÇ VE GÜNCEL DURUM 🌐

### 5.1. Mimarilerin Yakınsaması 🤝

Modern **x86 (CISC)** işlemcileri, dışarıdan gelen karmaşık CISC komutlarını içeride hızlıca basit **mikro-işlemlere (micro-ops)** ayırarak, **RISC** prensiplerine benzer şekilde yürütür. Bu, CISC'in **uyumluluk** avantajını korurken, RISC'in **hız ve verimlilik** avantajlarını kullanmasını sağlar.

### 5.2. Pazar Hakimiyeti 📈

* **Masaüstü ve Sunucu:** CISC (x86) liderliğini sürdürmektedir.
* **Mobil ve Gömülü Sistemler:** RISC (ARM) üstün güç verimliliği nedeniyle standarttır.

---

## 6. KAYNAKÇA 📚

Bu ödevin hazırlanmasında kullanılan akademik kaynaklar ve referanslar aşağıdadır:

* [Patterson, D. A., & Hennessy, J. L. (2017). *Computer Organization and Design: The Hardware/Software Interface*.]
* [Stalling, W. (2018). *Computer Organization and Architecture: Designing for Performance*.]
* [Kullanılan diğer ders notları ve internet kaynakları buraya eklenmelidir.]

---
