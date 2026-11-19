# Kasa Bekçisi — görev kartı

> `07 Ekip/Ajanlar/Kasa Bekcisi/Kimlik.md` sayfasından kısaltılmış örnek.
> Makineye ve projelere özgü ayrıntılar çıkarıldı. Kodun kendisi bu
> repoda yok; burada yalnız tasarım anlatılıyor.

| | |
|---|---|
| **Tür** | Ajan (kendi tetiğiyle çalışır) |
| **Motor** | Python betiği, yalnız standart kütüphane. **Yapay zekâ çağırmaz.** |
| **Makine** | Yalnız ana Mac. Veri makineden çıkmaz. |
| **Durum** | Gölge kipi: ne yapacağını raporlar, onarımları henüz kendisi yapmaz. |

## Neden doğdu

Kasadaki iki durum kartı bayat çıktı: biri ana dala alınmış bir işi
"commit'siz" gösteriyordu, öbürü üç commit'i olan bir işi "kod yok" diye
anlatıyordu. Kural yazılıydı, ama işi bitiren oturumlar kaydı güncellemeyi
atladı. Kurallar yazılı olunca uygulanmıyor; birinin her gün bakması
gerekiyor.

## Görev

Kasanın düzenini her gün denetler ve kurala dayalı, güvenli onarımları
kendisi yapar. Yorum gerektiren her şeyi onu çözecek olana bırakır:
ilgili projenin oturumuna, asistana ya da Hakan'a.

## Tetik

- Her saat ve Mac açılışında uyanır.
- Her gece 23:00'ten sonraki ilk uyanışta tur atar; Mac kapalı kaldıysa
  ilk açılışta telafi eder.
- Elle: `--simdi` (hemen tur), `--kuru` (hiçbir şey değişmez, rapor ekrana).

## Ne kontrol eder

- Kopuk bağlantılar, `index.md`'den ulaşılamayan sayfalar
- Durum kartları ile Git gerçeğinin çelişmesi
  (kart "açık" diyor, ama dal çoktan ana dala girmiş)
- İki Mac arasındaki eşitleme sorunları

## Yazdığı yerler

- Kendi raporu (`rapor.md`) ve `durum.md`'nin en üst satırı
- Kasanın GitHub yedeği: yalnız gece turundan sonra, yalnız ileri
  sararak, **asla zorlamadan**

## Asla dokunmadığı yerler

- Kişisel alan (sağlık, finans). Yalnız dosya adlarını görür, içeriği
  okumaz. **Testle kanıtlanır.**
- Başka bir oturumun henüz commit'lenmemiş değişikliği olan dosyalar.
- Kartların `durum` ve `sira` alanları. **Bekçi hiçbir kaydı kapatmaz;**
  "bu iş bitmiş görünüyor" der, kararı bir insan ya da oturum verir.
- Proje depolarına yazmaz; PR açmaz, yayın yapmaz.
- Kişisel alana dokunan bir commit varsa GitHub'a **hiçbir şey** gönderilmez.

## Bir gece raporundan kesit

```markdown
Tur: 19.11.2026 04:22 · kip: gölge (onarımlar kapalı)

## Bekçi yapacaktı
- yok

## Oturumlara bırakıldı
### Proje oturumu
- “…” kaydının dalı ana dala girmiş; kayıt hâlâ açık (kapanış adayı).

### Asistan (kasa oturumu)
- Yazilim Ogrenme/Günlük.md index.md'den 2 adımda ulaşılamıyor.
```

## Neden yapay zekâ değil

Bu işin çoğu kural: "bağlantı hedefi var mı", "dal ana dala girmiş mi".
Kuralı betik yapar; ucuz, hızlı ve yanıldığında nedeni okunabilir.
Yorum gereken yerde bekçi karar vermez, soruyu doğru kişiye bırakır.
