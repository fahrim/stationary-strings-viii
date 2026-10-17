# Duran Sicimler Teoremi VIII — Yayın Paketi

> **English:** [README.md](./README.md)

**Duran Sicimler Teoremi VIII: Falsifiye Edilebilir Öngörüler, 511 keV Tayf Bandı ve Belirsizlik Nicelemesi**

Yazar: Fahri Meral · Tarih: 17 Ekim 2026 · Sürüm: v1 (Makale VIII)

> **Durum:** Yayımlanmamış ön baskı (v1). Hakem denetiminden geçmemiştir.

## İçerik

| Dosya | Açıklama |
|---|---|
| `paper/duran_sicimler_teoremi_VIII.tex` | Ana makale, Türkçe (Tablo 1–4, Şekil 1 2×2) |
| `paper/duran_sicimler_teoremi_VIII_EN.tex` | İngilizce sürüm |
| `figs/fig10_falsifiable_predictions_UQ.pdf` | Test T20–T22 + UQ şekli (TR, 2×2) |
| `figs/fig10_falsifiable_predictions_UQ.png` | Test T20–T22 + UQ şekil önizlemesi (TR) |
| `figs/fig10_falsifiable_predictions_UQ_en.pdf` | Test T20–T22 + UQ şekli (EN, 2×2) |
| `figs/fig10_falsifiable_predictions_UQ_en.png` | Test T20–T22 + UQ şekil önizlemesi (EN) |
| `CITATION.cff` | Atıf kaydı |
| `LICENSE` | MIT |

## Sayısal üretim

Test T20–T22 (+ UQ), **V. makale deposundaki** ([`stationary-strings-v`](https://github.com/fahrim/stationary-strings-v)) çözücüyle üretilir:

```bash
git clone https://github.com/fahrim/stationary-strings-v
pip install numpy scipy matplotlib
python duran_sicimler_sim/solver_engine.py   # T1–T22 (22/22 PASS)
python duran_sicimler_sim/mini_check_viii.py  # bağımsız çapraz kontrol (7/7 PASS)
python duran_sicimler_sim/generate_figures.py  # Şekil 1 (+_en)
```

Bağımsız çapraz kontrol çözücüyü import etmez.

## Kilit bulgular

- T20: BASE-STEP 136 mT zayıf-alan falsifikasyon çifti (`r* = 1,1167668231 µm`,
  `1–4 mm` ofsetler geri-çekildi, korunmasız kol kayboldu).
- T21: ALPHA üçüncü-alan öngörüsü (`ḟ(1,05 T) = −74,2301213010 ± 0,0055473080 kHz/saat`,
  `R(1,05/1,03) = 1,0194406565`, `R(1,07/1,05) = 1,0190695066`).
- T22: 511 keV foton-bütçe öngörü bandı (`f_Ps = 0,92` için `R = 3,3387096774`,
  bant `[3,115; 3,585]`, `P_s = 1` bütçesi `2,6900000000`).
- UQ: kilit-çıktı duyarlılıkları + öz-denetim notu (solver proton sabiti bağımsız
  zincirle yakalanıp düzeltildi; türevler yalnızca %0,04 değişti).

## Lisans

MIT — bkz. `LICENSE`. İçerik hakem denetiminden geçmemiştir.
