# Awesome CPU Design & Architecture 🚀

*Bu belgeyi diğer dillerde okuyun: [English](README.md) | [Türkçe](README-tr.md)*

İşlemci (CPU) tasarımı, mikro mimari ve dijital mantık devreleri öğrenmek isteyenler için telif sorunu olmayan, tamamen ücretsiz ve açık kaynaklı (CC/BSD/Apache/MIT) kaynakların derlendiği bir liste. Bu depo, özellikle **RISC-V** ve **OpenRISC** gibi açık standartlara odaklanarak, kapı seviyesinden işletim sistemi çalıştırabilen çekirdeklere kadar uzanan bir öğrenme serüveni sunar.

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

## İçindekiler
- [Önerilen Öğrenme Yolu](#önerilen-öğrenme-yolu)
- [1. ISA Spesifikasyonları (Açık Standart, Ücretsiz)](#1-isa-spesifikasyonları-açık-standart-ücretsiz)
- [2. Üniversite Ders Materyalleri (Video + Slayt)](#2-üniversite-ders-materyalleri-video--slayt)
- [3. Ücretsiz Kurslar ve Sertifikalı Programlar](#3-ücretsiz-kurslar-ve-sertifikalı-programlar)
- [4. Açık Kaynak İşlemci Çekirdekleri (RTL)](#4-açık-kaynak-işlemci-çekirdekleri-rtl)
- [5. Simülatör ve Araç Zinciri](#5-simülatör-ve-araç-zinciri)
- [6. Ücretsiz / Açık Erişim Kitaplar](#6-ücretsiz--açık-erişim-kitaplar)
- [Katkıda Bulunma](#katkıda-bulunma)

---

## Önerilen Öğrenme Yolu

Aşağıdaki sırayla ilerleyerek sıfırdan tamamen telifsiz/açık kaynaklı bir yol izleyebilirsiniz:

1. **Temelleri Atın:** RISC‑V ve OpenRISC ISA belgelerini okuyarak temel komut seti formatlarını, adresleme modlarını ve mimari ilkeleri öğrenin.
2. **Mimariyi İnceleyin:** OpenRISC OR1200 ve basit RISC‑V çekirdeklerinin HDL (Donanım Tanımlama Dili) kodlarını inceleyerek mikro mimariyi (datapath + control) anlayın.
3. **Kendi Tasarımınızı Yapın:** Tek çevrimli (single-cycle) RISC‑V işlemci tasarımı gibi adım adım rehberlerden yararlanarak kendi küçük çekirdeğinizi tasarlayın ve simüle edin.
4. **Kavramları Pekiştirin:** Eğitim amaçlı işlemci projeleri ve Von Neumann / Logisim dokümanları ile mantık devresi ve veri yolu (bus) kavramlarını pekiştirin.

---

## 1. ISA Spesifikasyonları (Açık Standart, Ücretsiz)

Komut Seti Mimarisi (Instruction Set Architecture - ISA), donanım ve yazılım arasındaki köprüdür. 

- [RISC-V ISA Manual](https://riscv.org/technical/specifications/) / [GitHub Kaynağı](https://github.com/riscv/riscv-isa-manual) - CC BY 4.0 lisanslı, tam spesifikasyon PDF'leri. "Unprivileged ISA" ve "Privileged Spec" olarak ikiye ayrılır.
- [OpenRISC](https://openrisc.io/) - DSP özellikli, ücretsiz ve açık bir RISC ISA'sı; açık kaynak implementasyonları ve yazılım geliştirme araç seti (toolchain) sunar.
- [OpenPOWER ISA](https://openpowerfoundation.org/) - Apache 2.0 lisansıyla yönetilen güçlü mimari standartları.
- [SPARC / OpenSPARC](https://www.oracle.com/servers/technologies/opensparc.html) - Tarihsel bir açık kaynak referansı (GPL lisanslı).

## 2. Üniversite Ders Materyalleri (Video + Slayt)

Dünyanın en iyi üniversitelerinin paylaştığı tamamen ücretsiz akademik ders içerikleri:

- [Onur Mutlu – ETH Zürich / CMU](https://people.inf.ethz.ch/omutlu/) - *Digital Design & Computer Architecture* (Lisans) ve *Computer Architecture* (Lisansüstü) derslerinin uzun yıllara yayılan dev video arşivi (2013-2025). YouTube üzerinde tam oynatma listeleri mevcuttur.
- [UC Berkeley CS61C ("Great Ideas in Computer Architecture")](https://cs61c.org/) - RISC-V mimarisine odaklanan; donanım, mimari, assembly ve yazılım araçlarını kapsayan ikonik ders.
- [MIT 6.004 / 6.191 / 6.175 (Constructive Computer Architecture)](https://ocw.mit.edu/) - Temel RISC-V işlemci tasarımı, çok çevrimli ve 2 aşamalı pipeline laboratuvarları içeren efsanevi MIT materyalleri (CC BY-NC-SA).
- [CMU 18-447 Computer Architecture](https://www.youtube.com/channel/UCR1iaH4WEEHkEMB22kEbbqQ) - Carnegie Mellon'un bilgisayar mimarisi YouTube kanalı.
- [nand2tetris](https://www.nand2tetris.org/) - Mantık kapılarından (NAND) başlayarak işlemci, derleyici, işletim sistemi ve en son Tetris oyununu sıfırdan inşa ettiğiniz muhteşem proje.

## 3. Ücretsiz Kurslar ve Sertifikalı Programlar

- [Linux Foundation LFD111x: Building a RISC-V CPU Core](https://training.linuxfoundation.org/training/building-a-risc-v-cpu-core-lfd111x/) - Makerchip IDE kullanarak dijital mantık kapılarından RISC-V CPU çekirdeğine kadar tasarım yapmayı öğreten, edX üzerinde ücretsiz sunulan harika bir kurs.
- [RISC-V International Training](https://riscv.org/risc-v-training/) - Tarayıcı üzerinden modern araçlarla RISC-V CPU oluşturma kursu.
- [riscv/learn (GitHub)](https://github.com/riscv/learn) - RISC-V mikromimari tasarımı, işletim sistemi geliştirme ve IM mimarisinin temelleri üzerine devasa bir resmi topluluk "awesome list" çalışması.

## 4. Açık Kaynak İşlemci Çekirdekleri (RTL)

İncelemek, simüle etmek ve kendi projelerinizde türetmek (MIT/Apache/BSD) için uygun çekirdek kodları:

- [PicoRV32](https://github.com/YosysHQ/picorv32) - Boyut olarak son derece optimize edilmiş popüler bir RISC-V (RV32IMC) çekirdeği.
- [SERV](https://github.com/olofk/serv) - Dünyanın en küçük RISC-V çekirdeği. İlgi çekici "bit-serial" bir tasarıma sahiptir.
- [Rocket Chip / Chipyard (Berkeley)](https://github.com/ucb-bar/rocket-chip) - Chisel HDL kullanarak SoC ve özel hızlandırıcılar üretmek için kullanılan gelişmiş üretim ortamı.
- [OpenRISC OR1200](https://github.com/openrisc/or1200) - Verilog HDL ile yazılmış, pipeline, ALU ve exception mantığını inceleyebileceğiniz GNU LGPL lisanslı proje.
- [CORE-V CVA6](https://github.com/openhwgroup/cva6) - Endüstri standardında, Linux önyükleyebilen açık kaynak RV64GC işlemci çekirdeği.
- [mikeroyal/RISC-V-Guide](https://github.com/mikeroyal/RISC-V-Guide) - Geniş kapsamlı; Ripes, Renode, Unicorn gibi yüzlerce aracı listeleyen bir başka muazzam rehber.

## 5. Simülatör ve Araç Zinciri

- [Ripes](https://github.com/mortbopet/Ripes) - Harika bir grafiksel (GUI) RISC-V pipeline simülatörü. Komutların işlemci içinde nasıl ilerlediğini görsel olarak görebilirsiniz.
- [Spike (riscv-isa-sim)](https://github.com/riscv-software-src/riscv-isa-sim) - Orijinal ve resmi ISA simülatörü.
- [QEMU](https://www.qemu.org/) - RISC-V, ARM vb. mimarileri destekleyen efsanevi sistem emülatörü.
- **Açık Kaynak EDA Araçları:** Sentez, yerleşim ve simülasyon için [Verilator](https://www.veripool.org/verilator/), [Icarus Verilog](http://iverilog.icarus.com/), [Yosys](https://yosyshq.net/yosys/) ve [nextpnr](https://github.com/YosysHQ/nextpnr).
- [Logisim-Evolution](https://github.com/logisim-evolution/logisim-evolution) - Görsel olarak kapı seviyesinden devrenizi çizip simüle edebileceğiniz harika araç.

## 6. Ücretsiz / Açık Erişim Kitaplar

- **Guide to Computer Processor Architecture: A RISC-V Approach (Goossens):** Springer kaynaklı, bazı açık erişim bölümleri bulunabilen akademik eser.
- **Akademik Arşivler (arXiv vd.):** "RISC-V Education", "RISC-V Software Ecosystem" anahtar kelimeleriyle arama yapıldığında, araç zinciri ve ekosistem hakkında geniş bilgi veren PDF'ler.
- *Referans Notu:* "Computer Organization and Design: RISC-V Edition (Patterson & Hennessy)" kitabı, temel bir yapı taşıdır ancak teliflidir. PDF'leri paylaşılmaz, sadece akademik kütüphaneler aracılığıyla erişim önerilir.

---

## Katkıda Bulunma
Bu listeyi büyütmemize yardımcı olabilirsiniz! Yeni bir kaynak eklemek için:
1. Sadece bağlantı ve 1-2 cümlelik kısa bir açıklama ekleyin.
2. Telifli içerikleri doğrudan kopyalamaktan kaçının.
3. Ekleyeceğiniz deponun/kaynağın açık lisanslı (CC/BSD/Apache/MIT vb.) olduğundan emin olun.
