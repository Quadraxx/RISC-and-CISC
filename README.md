# 🚀 CISC ve RISC Mimarileri: Kapsamlı Analiz ve Karşılaştırma Ödevi 💻

> **AKADEMİK ÇALIŞMA:** Bilgisayar Donanımı Dersi Araştırma Ödevi 👨‍🏫
> **Hazırlayan:** Hüseyin Akın 🧑‍💻
> **Okul:** Torul Meslek Yüksekokulu (Torul MYO) 🏫
> **Tarih:** 24 Kasım 2025 🗓️

---

## 🎯 Projenin Amacı ve Kapsamı (Introduction)

Bu çalışma, işlemci mimarilerindeki iki temel felsefeyi, **CISC (Complex Instruction Set Computer)** ve **RISC (Reduced Instruction Set Computer)**'i, tarihsel gelişimden modern yonga tasarımına kadar analiz etmektedir. Amaç, mimarilerin **hız, güç tüketimi ve programlama modeli** üzerindeki etkilerini detaylıca incelemektir.

---

## 1. CISC Mimarisi (COMPLEX INSTRUCTION SET COMPUTER) 🧠

CISC, tek bir komutla karmaşık görevlerin yerine getirilmesini sağlayarak **karmaşıklığı donanıma** yükler.

### 1.1. Temel Yapı ve Çalışma Prensibi

| Özellik | Açıklama |
| :--- | :--- |
| **Felsefe** | Daha az sayıda makine komutuyla daha kısa program kodu yazmak. 💾 |
| **Donanım** | Komutlar, **Mikrokod (Microcode)** kullanan kontrol birimi tarafından yürütülür. |
| **Komut Yapısı** | **Değişken uzunluklu** komutlar ve doğrudan **bellek adresleri üzerinde işlem yapabilme** yeteneği. |
| **Yaygın Örnek** | Intel **x86** mimarisi (Masaüstü ve Sunucu işlemcilerinin temelidir). 🖥️ |

> **Görsel 1: CISC Mimarisi Şeması**
> ![CISC Mimarisi](https://www.watelectronics.com/wp-content/uploads/CISC-Architecture.jpg)

---

## 2. RISC Mimarisi (REDUCED INSTRUCTION SET COMPUTER) 💨

RISC, komut setini azaltarak **yalınlığı ve hızı** önceliklendirir.

### 2.1. Temel Yapı ve Çalışma Prensibi

| Özellik | Açıklama |
| :--- | :--- |
| **Pipelining (Bantlama)** | Tüm komutlar **sabit uzunlukta** olduğu için komut hattı verimli çalışır ve yüksek saat frekanslarına olanak tanır. ⏱️ |
| **Yazmaç Odaklılık** | Bellek erişimi sadece **LOAD** ve **STORE** komutlarıyla yapılır (**Load/Store Mimarisi**). 📥📤 |
| **Donanım** | Kontrol birimi, hızlı **Kablolu Mantık (Hardwired Logic)** kullanır. |
| **Yaygın Örnek** | **ARM** mimarisi (Mobil cihazlar, Apple M serisi çipleri). 📱 |

> **Görsel 2: RISC Mimarisi Bileşenleri**
> ![RISC Mimarisi Bileşenleri](https://www.watelectronics.com/wp-content/uploads/RISC-Architecture.jpg)

### 2.2. RISC Aile Örnekleri ve Gelişimi

RISC mimarisi zaman içinde farklı ihtiyaçlara göre şekillenmiştir. İşte önemli örnekler:

#### A. RISC-V (Açık Kaynak Devrimi)
Açık kaynaklı, özelleştirilebilir bir RISC komut seti mimarisidir. Donanım tasarımında devrim yaratmıştır ve geleceğin teknolojisi olarak görülmektedir.

> **Görsel 3: RISC-V Çip Mimari Şeması**
> ![RISC-V İşlemci CPU Mimarisi](https://www.technopat.net/wp-content/uploads/2024/07/R%C4%B0SC-V-Islemci-CPU-Mimari-ISA.jpg)

#### B. HP PA-RISC (Endüstriyel Güç)
Hewlett-Packard tarafından geliştirilen, RISC felsefesinin kurumsal alandaki ve sunucu dünyasındaki erken başarı örneklerinden biridir.

> **Görsel 4: HP PA-RISC Mimarisi Örneği**
> ![HP PA-RISC 7300LC Çip](https://upload.wikimedia.org/wikipedia/commons/thumb/6/68/HP_PA-RISC_7300LC.jpg/250px-HP_PA-RISC_7300LC.jpg)

---

## 3. KARŞILAŞTIRMALI ANALİZ 🆚

| Özellik | CISC (x86) | RISC (ARM, MIPS) | Sembol |
| :--- | :--- | :--- | :---: |
| **Komut Uzunluğu** | Değişken (Çözümleme zor) | Sabit (Çözümleme kolay) | 📏 |
| **Yürütme Süresi** | Değişken döngü (>1 cycle/komut) | Çoğu komut için **tek döngü** (1 cycle/komut) | ⏱️ |
| **Kontrol Birimi** | Mikrokod tabanlı | Tamamen **donanım** (Kablolu Mantık) tabanlı | ⚙️ |
| **Pipelining** | Zordur / Daha karmaşık devre gerektirir | Kolaydır / Daha verimli çalışır | 📈 |
| **Güç Verimliliği** | Düşük | Yüksek (Mobil için ideal) | ⚡ |

---

## 4. SONUÇ VE GÜNCEL DURUM 🌐

### 4.1. Mimarilerin Yakınsaması 🤝

Modern **x86 (CISC)** işlemcileri, dışarıdan gelen karmaşık CISC komutlarını içeride hızlıca basit **mikro-işlemlere (micro-ops)** ayırarak, **RISC** prensiplerine benzer şekilde yürütür. Bu **hibrit yaklaşım**, hem **uyumluluk** hem de **hız/verimlilik** avantajlarını birleştirir.

### 4.2. Pazar Hakimiyeti 📈

* **Masaüstü ve Sunucu:** **CISC (x86)**, geriye dönük uyumluluk nedeniyle liderliğini sürdürmektedir.
* **Mobil ve Gömülü Sistemler:** **RISC (ARM)**, üstün güç verimliliği sayesinde mutlak standarttır.

---

## 5. KAYNAKÇA 📚

Bu ödevin hazırlanmasında kullanılan akademik kaynaklar ve görsel referanslar aşağıdadır:

* [Patterson, D. A., & Hennessy, J. L. (2017). *Computer Organization and Design: The Hardware/Software Interface*.]
* [Stalling, W. (2018). *Computer Organization and Architecture: Designing for Performance*.]
* [Görsel Kaynak 1: Watelectronics - CISC Architecture]
* [Görsel Kaynak 2: Watelectronics - RISC Architecture]
* [Görsel Kaynak 3: Technopat - RISC-V Architecture]
* [Görsel Kaynak 4: Wikipedia - HP PA-RISC]

---
