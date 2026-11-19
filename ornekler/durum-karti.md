# Durum kartı örneği

> `06 Durum/` klasöründe her açık iş böyle bir kart. Üstteki alanlar
> (frontmatter) makine için, alttaki metin insan için. Bu kart kasadan
> olduğu gibi alındı.

```markdown
---
proje: Kasa
durum: karar bekliyor
sira: Hakan
kaynak: "[[00 Gelen Kutusu/2026-11-08 Karar gündemi]]"
acildi: 2026-11-08
son_hareket: 2026-11-10
---

# Kasanın ham katmanı

Kasada ham katman yok: envanter notları bile asistanın sıkıştırması.
Transkript ve kaynak metin saklamanın telif sınırı da bu kararın içinde.
Durum katmanı bugün çözüldü, bu parça açık kaldı.

**İlerlemesi için gereken:** ham kaynak saklanacak mı, nerede, hangi
sınırla.
```

## Alanlar ne işe yarıyor

| Alan | Anlamı |
|---|---|
| `durum` | açık · bilgi bekliyor · karar bekliyor · duruyor · kapandı |
| `sira` | **Sıra kimde?** Hakan · asistan · bir proje oturumu |
| `kaynak` | Bu iş nereden doğdu (sohbet notu, karar gündemi, proje kaydı) |
| `son_hareket` | En son ne zaman ilerledi; "kaç gündür hareketsiz" buradan hesaplanır |
| **İlerlemesi için gereken** | Tek cümle. İşin önündeki engel. |

## Kartlardan üretilen özet

Bir betik bütün kartları okuyup `durum.md` sayfasını üretiyor. Sabah ilk
bakılan sayfa bu. Kısaltılmış bir görünüm:

```markdown
# Durum

Bekçi 19.11 04:22 · 0 yapacaktı · 8 oturumlara · 56 Hakan'da

Üretilen dosya — elle düzenlenmez.

## Hakan sırasında (13)

- **Kasanın ham katmanı** — Kasa
  - durum: karar bekliyor · hareketsiz: 9 gün
  - gereken: ham kaynak saklanacak mı, nerede, hangi sınırla.
- **Kalibrasyon tablosunun ilk satırı** — Kasa
  - durum: bilgi bekliyor · hareketsiz: 9 gün
  - gereken: o işin gerçekte ne kadar sürdüğü.
  ...

## Asistan sırasında (3)
  ...
```

Neden işe yarıyor: "Ne yapmam gerekiyordu?" sorusu artık hafızaya değil,
dosyaya soruluyor. Ve 9 gündür hareketsiz duran bir iş kendini belli ediyor.
