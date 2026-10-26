# Zihin Kampı – Beceri Altyapısı

Çocuklar spor için voleybol kursuna, dil için İngilizce kursuna gidiyor. Düşünme becerileri ve matematiksel akıl yürütme için ise böyle bir kurs yok. Zihin Kampı bu boşluğu doldurmayı hedefliyor: okul müfredatını kapsayan ama onunla sınırlı kalmayan, geleceğin ihtiyaç duyacağı bilişsel becerileri çocukta oluşturan bir yapı.

Bu repo, uygulamanın arkasındaki beceri altyapısını tutuyor.

## Yapı: dört katman

| Katman | Ne içerir | Durum |
| --- | --- | --- |
| 1. Etkinlikler | Oyunlar, sorular, görevler | Uygulama kodunda |
| 2. Zihin Kampı beceri haritası (çekirdek) | Kendi tanımladığımız, birbirine bağlı beceriler | Sırada |
| 3. Çerçeve eşleştirmeleri | Çekirdek becerilerin Maarif Modeli ve diğer çerçevelerdeki karşılıkları | Maarif verisi hazır |
| 4. Okul uyumu | Sınıf, tema ve sınav (OYSS) uyumu | Maarif verisi hazır |

Çekirdek beceri haritası hiçbir müfredata bağlı değil. Müfredat değiştiğinde yalnızca 3. ve 4. katmanlardaki eşleştirmeler güncellenir.

## Veriler

`veri/maarif/` klasöründe MEB'in resmî sitesinden ([tymm.meb.gov.tr](https://tymm.meb.gov.tr)) alınmış veriler var:

- `matematik-ogrenme-ciktilari.json`: 3-6. sınıf matematik dersinin 114 öğrenme çıktısı. Her çıktı için sınıf, tema, çıktı metni (birebir), MEB'in o çıktı için andığı beceri kodları ve kaynak sayfa bağlantısı yer alıyor.
- `beceri-cercevesi.json`: Maarif Modeli beceri çerçevesinin kodları ve adları (kavramsal beceriler, matematik alan becerileri, eğilimler, sosyal-duygusal öğrenme becerileri).

| Sınıf | Öğrenme çıktısı |
| --- | --- |
| 3 | 33 |
| 4 | 34 |
| 5 | 23 |
| 6 | 24 |

Veri hakkındaki notlar (kodlardaki yazım hataları, 4. sınıf programının yürürlük tarihi gibi) JSON dosyalarının `notlar` alanında.
