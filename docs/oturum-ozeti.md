# Zihin Kampı – Oturum Özeti (26 Ekim 2026)

Bu dosya, uygulama kodunun bulunduğu çalışmada kaldığımız yerden devam etmek için hazırlandı.

## Uygulama hakkında bilinenler

- **Zihin Kampı: 3-6. Sınıf**, Google Play'de yayında: `com.onursahin.zihinkampi` ([mağaza sayfası](https://play.google.com/store/apps/details?id=com.onursahin.zihinkampi)).
- 8-12 yaş, Google Play Aile Politikaları kapsamında. Reklam, analitik ve izleyici yok, hesap açılmıyor. Veriler cihazda tutuluyor.
- Gelir modeli: Google Play aboneliği. Kişiye özel davet kodları ve grup/öğretmen kodları var.
- 12 karşılıklı oyun: Dört Taş, Renk Yarışı, Kural Düellosu, Sudoku, Şifre Kırıcı, İşlem Avı, Kesir Düellosu, Hazine Avı, Satranç, Kelime Köprüsü, Ortak Görev, Su Kanalı. Karşılıklı oyun için Firebase Realtime Database (Belçika) kullanılıyor ve bu özelliği veli açıyor.
- Diğer özellikler: veli raporu, PIN'li Veli Paneli, İlerlemem ▸ Raporlarım ekranı, rozetler, seri, uyarlanan zorluk.
- Uygulama, Şira'yla iki yıldır uzaktan yürütülen ödev alışkanlığı ve mantık-matematik çalışmasından doğdu.

## Vizyon ve konumlandırma

- **Kurs gibi düşünülmeli.** Çocuklar voleybol kursuna ve İngilizce kursuna gidiyor, ama düşünme becerileri ve matematik vizyonu için bir kurs yok. Zihin Kampı bu boşluğu dolduruyor: okul müfredatını kapsıyor ama onunla sınırlı kalmıyor, geleceğin bilişsel becerilerini geliştiriyor.
- **EBA'yla rekabet değil, tamamlayıcılık.** "EBA konuyu öğretir, Zihin Kampı düşünmeyi ve düzenli çalışmayı alışkanlık hâline getirir." Konu anlatımı ve test eklenmeyecek.
- **Gelir yolu (öneri):** Velilere tek tek abonelik satmak yerine okullara, etüt merkezlerine ve rehberlik servislerine kurum lisansı satmak. Akıllı tahta için bir "Sınıf Modu" eklemek (takım yarışı, öğrenciden veri alınmaz). Önce 3-5 kurumla ücretsiz pilot yapılacak.

## Dört katmanlı beceri altyapısı (karar verildi)

| Katman | İçerik |
| --- | --- |
| 1. Etkinlikler | Oyunlar, sorular, görevler |
| 2. Zihin Kampı beceri haritası (çekirdek) | Müfredattan bağımsız, birbirine bağlı 20-30 beceri ve "önce bu, sonra şu" ilişkileri |
| 3. Çerçeve eşleştirmeleri | Maarif Modeli kodları (KB, MAB, E, SDB), öğrenme çıktıları (MAT.x.y.z), ileride uluslararası çerçeveler |
| 4. Okul uyumu | Sınıf, tema, OYSS senaryoları |

Müfredat değişirse yalnızca 3. ve 4. katmanlar güncellenir. Beceri haritası ve ilerleme cihazda tutulabilir, yani gizlilik tasarımıyla uyumlu.

Maarif Modeli'nde zayıf kalan, öne çıkarılacak gelecek becerileri: algoritmik düşünme, veri ve olasılık sezgisi, öğrenmeyi öğrenme (metabiliş), yapay zekâ okuryazarlığı, iş birliği ve müzakere.

## Hazırlanan çıktılar

- **Beceri eşleştirme dokümanı:** [Zihin Kampı – Maarif Modeli Beceri Eşleştirmesi](https://claude.ai/artifact/3ty6YfE9YgDU9TW1zVoFYL). İçeriği:
  - 12 oyunun KB, MAB, E ve SDB kodlarıyla eşleştirmesi.
  - Alışkanlık özelliklerinin öz düzenleme (SDB1.2) göstergeleriyle eşleştirmesi.
  - OYSS bağlantısı.
  - **Uyarı:** "Oyunda çocuk ne yapıyor" sütunu oyun adlarından tahmin edildi; kodla doğrulanmalı.
- **Bu repo (`onursahin-creator/Yeni1`, dal `ccr-f3297fc9-vj2t7j`):**
  - `veri/maarif/matematik-ogrenme-ciktilari.json`: 3-6. sınıf matematik dersinin 114 öğrenme çıktısı, tymm.meb.gov.tr'den birebir alındı.
  - `veri/maarif/beceri-cercevesi.json`: Maarif Modeli beceri kodları ve adları.

## Önemli bulgular

- **OYSS:** 2026-2027 1. dönemden itibaren 5-6-7. sınıflarda matematik dahil 6 derste uygulanıyor. Sorular beceri temelli ve açık uçlu, analiz öğrenme çıktısı bazında yapılıyor. 3-4. sınıflar kapsam dışı. Zihin Kampı "sınava hazırlık" olarak değil, sınavın ölçtüğü düşünme becerilerine destek olarak tanıtılmalı.
- **Düşünme Eğitimi dersi:** MEB'in ortaokulda seçmeli bir "Düşünme Eğitimi" dersi var. Hem rakip hem doğal ortak olabilir; programı incelenmeli.
- **Algoritmik düşünme müfredatta:** 3. ve 4. sınıf matematikte kodlama stratejileri var (MAT.3.3.8, MAT.4.3.10). Olasılık 4. sınıfta başlıyor.
- **4. sınıf programı:** Maarif Modeli programı yayımlanmış, ama okullarda hangi yıldan itibaren uygulandığı doğrulanmalı.

## Okul süreci (Dilek Hanım, Şira'nın sınıf öğretmeni)

- WhatsApp'tan ücretsiz kullanım önerisi gönderildi.
- Dilek Hanım'ın cevabı: uygulamayı görmek istiyor, ama öğretmenler ek kaynak ya da uygulama öneremiyor. İstekli velilere veli grubundan ulaşılabilir; her veli kabul etmeyebilir.
- Onur Bey'in cevabı: kendi çocuğu için ürettiği bir uygulama olduğunu, ücretsiz sunacağını ve isteyenin yararlanabileceğini yazdı, Play Store linkini gönderdi.
- **Sıradaki adım:** veli grubuna mesaj. Mesajda Dilek Hanım'ın adı geçmeyecek. Taslak:

> Merhaba değerli veliler, ben Şira'nın babası Onur.
>
> Yaklaşık iki yıldır Şira'nın ödev alışkanlığı ve mantık-matematik becerileri için hazırladığım "Zihin Kampı" adında bir uygulama var. Kısa ve düzenli oturumlardan oluşuyor; mantık, dikkat ve işlem becerilerine yönelik oyunlar içeriyor. Reklam yok, çocuklardan kişisel veri alınmıyor, internetsiz de çalışıyor.
>
> Sınıf arkadaşlarından denemek isteyen olursa ücretsiz açabilirim. Tamamen isteğe bağlı. İlgilenen bana özelden yazabilir, kodu ileteyim.
>
> https://play.google.com/store/apps/details?id=com.onursahin.zihinkampi
>
> Onur Şahin

Göndermeden önce:
- Grup kodu mu, kişiye özel kod mu kullanılacağına karar verilecek ve kodla ücretsiz erişimin açıldığı test edilecek.
- Ücretsiz kullanımın süresi belirlenecek.
- 2-3 hafta sonra velilerden kısa geri bildirim toplanacak.

## Uygulama koduyla yapılacaklar

1. Beceri eşleştirme dokümanındaki oyun açıklamalarını gerçek oyun işleyişiyle doğrulamak ve kodları düzeltmek.
2. Çekirdek beceri haritasını (2. katman) hazırlamak: 20-30 beceri, ön koşul ilişkileri ve bir diyagram.
3. Her oyunu ve seviyeyi beceri haritasına, oradan da Maarif öğrenme çıktılarına (`veri/maarif/`) bağlayan veri yapısını uygulamaya eklemek.
4. Tek kişilik alıştırmaları da eşleştirmeye eklemek.
5. Sınıf Modu (akıllı tahta) ve kurum lisansı için teknik plan.
6. Grup kodu akışının sınıf pilotu için uygun olduğunu kontrol etmek.
