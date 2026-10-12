# MWD-MultiWell — Real Measurement-While-Drilling & Rock-Indentation-Hardness Dataset (4–5 Wells, Multi-Region)

> Real field MWD (Measurement-While-Drilling) logs plus rock indentation hardness and hardness grade, sampled every 2 m, organised as one workbook per well. The full release covers 4–5 wells drilled in different regions; this folder documents what is visible in the supplied screenshots (2 wells) and the shared schema used by every well.

<p align="center">
  <b>Domain:</b> Drilling engineering · Rock mechanics · Formation drillability · MWD petrophysics<br>
  <b>Task types:</b> Regression (hardness), Classification (lithology / hardness grade), Correlation (logging response vs. hardness)<br>
  <b>Contact:</b> lonlonago@foxmail.com
</p>

---

## 1. Overview

This dataset contains **real Measurement-While-Drilling (MWD) records from 4–5 wells**, drilled in **different regions**, together with the **rock indentation hardness** and **hardness grade** of every sampled depth point.

- **Sampling interval:** 2 m along hole depth.
- **Per-well organisation:** each well is one WPS / Excel workbook containing 4 sheets — `Data description` · `MWD records` · `Lithology statistics` · `Hardness distribution chart`.
- **Columns per record:** 18 (see §4), spanning depth, formation, lithology, well trajectory and a standard MWD petrophysical suite (GR / RT / RS / DEN / CNL / AC / CAL) plus drilling-mechanics channels (ROP / drilling time / WOB / RPM / torque).
- **Labels available:** lithology (13 classes observed) and rock-hardness grade (6 classes) — both usable as supervised targets.
- **Visible well section (per well, as titled in the workbooks):** **2600 – 3798 m**, **600 records** (≈1200 m of section).

> **Note on completeness of this folder.** The five images shipped with this folder are screen photographs of per-well workbooks. They allow **2 individual wells to be identified and described in detail** (§3). The remaining wells of the release (a total of **4–5 wells** across different regions) follow exactly the same 18-column schema and the same 4-sheet workbook layout, but are not visible in these particular screenshots.

---

## 2. What is in this folder

| File | Content |
|---|---|
| `123 (1).jpg` | Sheet `Hardness distribution chart`: bar chart **mean indentation hardness per lithology**, with a floating data label (`series "Mean hardness (MPa)" — point "Rhyolite" — value: 2257`). |
| `123 (2).jpg` | Sheet **MWD records** of **Well 1** — formation column reads `…Fm (K1q)`; visible depth window 2600.0 – 2688.0 m (rows index 1–45). |
| `123 (3).jpg` | Sheet **Lithology statistics**: table `Per-lithology statistics (sorted by mean hardness, ascending)` (13 lithologies) + table `Hardness-grade distribution` (6 grades). |
| `123 (4).jpg` | Sheet `Hardness distribution chart`: the same **mean indentation hardness per lithology** chart, photographed with the sheet's `Depth (m)` column (2600, 2632, 2664 … 3784) visible in the background. |
| `123 (5).jpg` | Sheet **MWD records** of **Well 2** — formation column reads `…Fm (J2t)`; workbook title `A1 well — MWD & rock-hardness prediction data (2600 – 3798 m, 600 records)`. |

Common workbook elements visible in every photo (bottom sheet-tab bar): `Data description` · `MWD records` · `Lithology statistics` · `Hardness distribution chart`, i.e. **one workbook per well, identical template across wells**.

---

## 3. Wells identifiable in the screenshots (detailed)

Two wells can be resolved from the two `MWD records` screenshots. Their **well names are partly obscured** by the photo (a blurred patch covers the leading characters of the workbook title), so only the readable tail of each name is reproduced below — no name has been invented.

### 3.1 Well 1 — `…01 well` (formation `…Fm (K1q)`)

| Item | Value (as read from the screenshot) |
|---|---|
| Source image | `123 (2).jpg`, sheet `MWD records` |
| Workbook title | `…01 well — MWD & rock-hardness prediction data (2600 – 3798 m)` — leading characters of the well name are masked by the photo |
| Formation column | `…Fm (K1q)` — the character(s) before `Fm` are cut by the column width |
| Depth interval | **2600 – 3798 m** (from the title) |
| Sampling | **every 2 m** |
| Visible window in the photo | **2600.0 – 2688.0 m**, 45 consecutive rows (index 1–45) |
| Trajectory | near-vertical: **inclination 0.2 – 1.5°**, **azimuth 94 – 131°** |
| Lithology in the window | Sandy mudstone (12) → Siltstone (12) → Mudstone (3) → Siltstone (5) → Sandy mudstone (6) → Mudstone … (counts from visible rows) |

### 3.2 Well 2 — `A1 well` (formation `…Fm (J2t)`)

| Item | Value (as read from the screenshot) |
|---|---|
| Source image | `123 (5).jpg`, sheet `MWD records` |
| Workbook title | `A1 well — MWD & rock-hardness prediction data (2600 – 3798 m, 600 records)` — leading characters of the well name are partly masked |
| Formation column | `…Fm (J2t)` — the character(s) before `Fm` are cut by the column width |
| Depth interval | **2600 – 3798 m** (from the title) |
| Sample count | **600 records** (explicitly stated in the title) |
| Sampling | every 2 m |
| Trajectory | near-vertical: inclination 0.2 – 1.5°, azimuth 94 – 131° |
| Lithology in the window | Sandy mudstone (12) → Siltstone (12) → Mudstone (3) → Siltstone … (same succession as Well 1) |

### 3.3 Cross-well observation (factual, from the images)

The two `MWD records` screenshots show **row-by-row identical readings** — e.g. row 1 = `inclination 0.4 / azimuth 131 / GR 85.2 / RT 4.4 / RS 3.2 / DEN 2.48 / CNL 25.9 / AC 96.0 / CAL 222.8 / ROP 7.94 / drilling time 7.55 / WOB 112 / RPM 74` in **both** images. The only differences between the two screenshots are the **formation code** (`K1q` vs `J2t`) and the **well name** in the title.

This is reported as observed; if the wells are in fact populated with different measurements, the original workbooks govern.

### 3.4 Sample records (first 20 rows of the visible window, transcribed from the screenshots)

Values below are transcribed from the two `MWD records` photographs (both wells show the same values). `—` marks a cell that cannot be resolved because of glare/blur.

| # | Depth (m) | Formation | Lithology | Incl. (°) | Azimuth (°) | GR | RT | RS | DEN | CNL | AC | CAL | ROP | Drill time | WOB | RPM |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| 1 | 2600.0 | …Fm (K1q) | Sandy mudstone | 0.4 | 131 | 85.2 | 4.4 | 3.2 | 2.48 | 25.9 | 96.0 | 222.8 | 7.94 | 7.55 | 112 | 74 |
| 2 | 2602.0 | …Fm (K1q) | Sandy mudstone | 1.3 | 120 | 68.4 | 14.9 | 11.2 | 2.51 | 30.3 | 92.1 | 225.6 | 6.19 | 9.70 | 116 | 59 |
| 3 | 2604.0 | …Fm (K1q) | Sandy mudstone | 0.4 | 108 | 88.9 | 8.2 | 6.0 | 2.41 | 31.7 | 89.7 | 216.7 | 9.71 | 6.18 | 143 | 66 |
| 4 | 2606.0 | …Fm (K1q) | Sandy mudstone | 0.6 | 94 | 106.1 | 5.2 | 3.8 | 2.47 | 33.6 | 88.3 | 220.1 | 7.27 | 8.26 | 93 | 56 |
| 5 | 2608.0 | …Fm (K1q) | Sandy mudstone | 1.2 | 107 | 81.9 | 5.5 | 5.1 | 2.44 | 29.4 | 84.8 | 223.6 | 9.22 | 6.51 | 135 | 56 |
| 6 | 2610.0 | …Fm (K1q) | Sandy mudstone | 0.7 | 102 | 65.1 | 5.3 | 4.6 | 2.52 | 27.3 | 93.5 | 223.6 | 11.08 | 5.42 | 115 | 57 |
| 7 | 2612.0 | …Fm (K1q) | Sandy mudstone | 1.5 | 98 | 79.0 | 5.6 | 4.6 | 2.53 | — | 92.9 | 218.0 | 7.65 | 7.84 | 119 | 59 |
| 8 | 2614.0 | …Fm (K1q) | Sandy mudstone | 0.9 | 99 | 101.8 | 7.1 | 6.7 | 2.41 | 23.8 | 94.9 | 217.8 | 12.22 | 4.91 | 96 | 57 |
| 9 | 2616.0 | …Fm (K1q) | Sandy mudstone | 0.2 | 103 | 78.1 | 3.5 | 3.0 | 2.46 | 23.8 | 98.4 | 223.6 | 10.64 | 5.64 | 91 | 60 |
| 10 | 2618.0 | …Fm (K1q) | Sandy mudstone | 0.5 | 97 | 106.6 | 10.9 | 8.1 | 2.43 | 28.4 | 93.6 | 224.2 | 10.05 | 5.97 | 148 | 69 |
| 11 | 2620.0 | …Fm (K1q) | Sandy mudstone | 0.5 | 99 | 75.7 | 4.3 | 3.4 | 2.45 | 28.6 | 97.7 | 226.4 | 8.72 | 6.88 | 133 | 73 |
| 12 | 2622.0 | …Fm (K1q) | Sandy mudstone | 0.7 | 108 | 66.1 | 7.0 | 5.1 | 2.45 | 25.2 | 103.7 | 221.4 | 5.85 | 10.25 | 122 | 61 |
| 13 | 2624.0 | (K1q) | Siltstone | 1.0 | 116 | 82.4 | 4.5 | 4.1 | 2.49 | 27.2 | 98.1 | 217.1 | 9.20 | 6.52 | 135 | 67 |
| 14 | 2626.0 | (K1q) | Siltstone | 1.1 | 128 | 75.5 | 7.8 | 6.9 | 2.49 | 21.1 | 83.6 | 215.3 | 5.87 | 10.22 | — | 58 |
| 15 | 2628.0 | (K1q) | Siltstone | 0.9 | 106 | 101.0 | 8.8 | 8.2 | 2.42 | 20.0 | 90.3 | 216.5 | 5.63 | 10.67 | 143 | 62 |
| 16 | 2630.0 | (K1q) | Siltstone | 1.5 | 120 | 84.1 | 4.3 | 3.7 | 2.49 | 21.0 | 90.3 | 223.6 | 8.18 | 7.33 | 114 | 61 |
| 17 | 2632.0 | (K1q) | Siltstone | 0.7 | 102 | 86.1 | 8.6 | 7.1 | 2.43 | 27.5 | 93.6 | 222.0 | 4.92 | 12.19 | 132 | 69 |
| 18 | 2634.0 | (K1q) | Siltstone | 1.0 | 114 | 91.8 | 13.3 | 11.2 | 2.51 | 27.4 | 98.5 | 217.1 | 4.65 | 12.91 | 105 | 58 |
| 19 | 2636.0 | (K1q) | Siltstone | 0.7 | 112 | 77.9 | 6.1 | 4.6 | 2.40 | 20.7 | 87.0 | 222.3 | 4.47 | 13.42 | — | 56 |
| 20 | 2638.0 | (K1q) | Siltstone | 0.9 | 111 | 91.7 | 8.1 | 7.1 | 2.41 | 22.5 | 84.9 | 211.3 | 5.10 | 11.78 | 108 | 59 |

*(Units are printed in the workbook headers: Depth (m), Inclination (°), Azimuth (°); `RT/RS` in Ω·m, `DEN` in g/cm³, `AC` in μs/m, `ROP` in m/h, `drilling time` in min/m. A few header unit strings are cut off by the photo — the original workbook is authoritative.)*

---

## 4. Data schema (18 columns, identical for every well)

| # | Column | Meaning | Notes |
|---|---|---|---|
| 1 | Index | Row index | 1 … n within a well |
| 2 | Depth (m) | Measured depth | 2 m step |
| 3 | Formation | Formation code | e.g. `…Fm (K1q)`, `…Fm (J2t)` |
| 4 | Lithology | Lithology | 13 classes observed |
| 5 | Inclination (°) | Inclination | 0.2 – 1.5° → near-vertical wells |
| 6 | Azimuth (°) | Azimuth | 94 – 131° in the visible window |
| 7 | Gamma ray GR | Gamma ray (API) | 65 – 107 in the visible window |
| 8 | Deep resistivity RT (Ω·m) | Deep resistivity | 3.5 – 14.9 |
| 9 | Shallow resistivity RS (Ω·m) | Shallow resistivity | 3.0 – 11.2 |
| 10 | Compensated density DEN (g/cm³) | Compensated density | 2.40 – 2.53 |
| 11 | Compensated neutron CNL | Compensated neutron | 20.0 – 33.6 |
| 12 | Sonic transit time AC (μs/m) | Sonic interval transit time | 83.6 – 103.7 |
| 13 | Caliper CAL | Caliper | ≈ 211 – 226 (unit string cut in the photo; magnitude suggests mm) |
| 14 | Rate of penetration ROP | Rate of penetration | 4.47 – 12.22 (m/h) |
| 15 | Drilling time | Drilling time | 4.91 – 13.42 (min/m) |
| 16 | Weight on bit WOB | Weight on bit | 91 – 155 |
| 17 | Rotary speed RPM | Rotary speed | 55 – 74 |
| 18 | Torque TOR | Torque | Mostly cut off in the photos |

---

## 5. Rock-hardness grade scale (from sheet `Lithology statistics` → `Hardness-grade distribution`)

| Hardness grade | Samples (n) | Share | Indentation hardness (MPa) |
|---|---|---|---|
| Very soft | 154 | 25.7 % | 120 – 500 |
| Soft | 287 | 47.8 % | 500 – 1000 |
| Medium | 64 | 10.7 % | 1000 – 1600 |
| Medium-hard | 28 | 4.7 % | 1600 – 2200 |
| Hard | 58 | 9.7 % | 2200 – 3000 |
| Very hard | 9 | 1.5 % | 3000 – 3300 |
| **Total** | **600** | **100 %** | 120 – 3300 |

---

## 6. Per-lithology statistics (`Per-lithology statistics (sorted by mean hardness, ascending)`, transcribed)

| Lithology | Samples | Thickness (m) | Mean hardness (MPa) | Min hardness | Max hardness | Mean grade value | Mean ROP (m/h) |
|---|---|---|---|---|---|---|---|
| Coal | 15 | 30 | 292 | 156 | 437 | 1.62 | 20.24 |
| Mudstone | 164 | 328 | 478 | 196 | 699 | 2.78 | 9.17 |
| Sandy mudstone | 35 | 70 | 498 | 261 | 833 | 2.82 | 8.95 |
| Siltstone | 109 | 218 | 672 | 261 | 1126 | 3.24 | 6.58 |
| Medium sandstone | 54 | 108 | 677 | 264 | 1148 | 3.27 | 6.58 |
| Fine sandstone | 54 | 108 | 712 | 358 | 1043 | 3.40 | 5.85 |
| Gravelly sandstone | 33 | 66 | 1063 | 659 | 1431 | 3.84 | 4.34 |
| Tuff | 8 | 16 | 1125 | 984 | 1252 | 4.24 | 3.24 |
| Tuffaceous sandstone | 13 | 26 | 1171 | 820 | 1417 | 3.93 | 4.02 |
| Conglomerate | 19 | 38 | 1324 | 1037 | 1595 | 4.46 | 2.78 |
| Rhyolite | 41 | 82 | 2257 | 1369 | 2923 | 5.36 | 1.51 |
| Andesite | 29 | 58 | 2366 | 1808 | 3300 | 5.73 | 1.15 |
| Basalt | 26 | 52 | 2665 | 1993 | 3300 | 6.11 | 0.89 |
| **Total** | **600** | **1200** | — | 156 | 3300 | — | — |

The table adds up to **600 samples / 1200 m**, matching the `600 records` stated in the workbook title of Well 2.

---

## 7. Hardness vs. lithology chart (`Hardness distribution chart`)

Sheet `Hardness distribution chart` carries a bar chart titled **mean indentation hardness per lithology**, category axis = the 13 lithologies above (ordered from coal to basalt), value axis = mean indentation hardness (MPa), 0 – 3000. A floating label in the photo reads `series "Mean hardness (MPa)" — point "Rhyolite" — value: 2257`, confirming the series is the same mean-hardness column as in §6. Images `123 (1).jpg` and `123 (4).jpg` show this chart; `123 (4).jpg` also shows the sheet behind it with a `Depth (m)` column running 2600 → 3784 m in 32 m steps.

---

## 8. Derived baseline statistics (computed from the transcribed table in §6)

Computed here as a modelling baseline; **not printed in the source workbook**.

| Metric | Value |
|---|---|
| Sample-weighted mean indentation hardness | **≈ 939 MPa** |
| Sample-weighted mean ROP | **≈ 6.50 m/h** |
| Sample-weighted mean grade value | **≈ 3.56** |
| Pearson r — mean hardness vs. mean ROP (13 lithologies) | **−0.744** |
| Pearson r — mean hardness vs. mean grade value | **+0.967** |
| Pearson r — ln(hardness) vs. ln(ROP) | **−0.991** |
| Power-law fit | **ROP ≈ 33 870 · H^(−1.312)** |
| Hardness span across lithologies (means) | 292 → 2665 MPa |
| ROP span across lithologies (means) | 20.24 → 0.89 m/h (≈ 23×) |

Interpretation: hardness is an almost sufficient statistic for drillability in this dataset — lithology-mean ROP falls monotonically (log-linearly) with indentation hardness, from coal (20.24 m/h) to basalt (0.89 m/h).

---

## 9. Notes, limitations & open items

1. **Well count.** The release contains **4–5 wells from different regions**; only **2 wells** are identifiable from the screenshots in this folder (Well 1 `…01 well`, formation `K1q`; Well 2 `A1 well`, formation `J2t`).
2. **Masked well names.** The leading characters of both workbook titles are obscured by the photograph; the readable tails (`…01 well`, `A1 well`) are reproduced verbatim and no name has been invented.
3. **Formation-code prefixes.** In both wells the full formation name is wider than its column, so only the tail (`…Fm (K1q)` / `…Fm (J2t)`) is visible. The codes themselves (`K1q`, `J2t`) are legible in every row.
4. **Identical readings across the two visible wells** (§3.3) — reported as observed.
5. **Statistics sheet is not well-attributed.** Sheets `Lithology statistics` and `Hardness distribution chart` carry no well name in the screenshots, so the tables in §5–§7 cannot be assigned to a specific well.
6. **Transcription accuracy.** All numbers in §3.4, §5 and §6 are read from screen photographs (glare, moiré, clipped columns). Values marked `—` were unreadable; otherwise the original workbook is authoritative.
7. **Torque column** is largely cut off in both `MWD records` photos.

### Reference note on the formation codes (interpretation, not data)

`K1q` and `J2t` are standard Chinese stratigraphic codes (Lower Cretaceous and Middle Jurassic respectively). In Chinese petroleum practice `K1q` is the code commonly used for the **Quantou Formation** of the **Songliao Basin** (NE China), while `J2t` is commonly used for the **Toutunhe Formation** of the **Junggar Basin** (NW China) — consistent with the "different regions" character of this multi-well release. This paragraph is **background nomenclature, not content extracted from the dataset**; the actual region of each well should be confirmed by the provider.

---

## 10. Intended use

- **Rock-hardness prediction** from MWD logs (regression; the §8 power-law is a trivial baseline to beat).
- **Lithology classification** from MWD logs (13 classes; note the strong class imbalance — mudstone 164 vs. tuff 8).
- **Hardness-grade classification** (6 ordinal classes).
- **ROP / drillability modelling** and bit-selection studies.
- **Cross-well generalisation benchmarks** — with 4–5 wells from different regions, leave-one-well-out evaluation is the natural protocol.

## 11. Licence & citation

```
Licence: see the accompanying distribution terms.
Citation: MWD-MultiWell — Real Measurement-While-Drilling & Rock-Indentation-Hardness Dataset (4–5 Wells, Multi-Region).
Contact: lonlonago@foxmail.com
```

## 12. Contact

Questions about the data, the per-well workbooks or licensing: **lonlonago@foxmail.com**

---

## 13. Preview images

| Preview | File | Description |
|---|---|---|
| [![123 (1)](123%20(1).jpg)](123%20(1).jpg) | `123 (1).jpg` | Hardness distribution chart — mean indentation hardness per lithology |
| [![123 (2)](123%20(2).jpg)](123%20(2).jpg) | `123 (2).jpg` | Well 1 MWD records (formation K1q) |
| [![123 (3)](123%20(3).jpg)](123%20(3).jpg) | `123 (3).jpg` | Lithology statistics + hardness-grade distribution |
| [![123 (4)](123%20(4).jpg)](123%20(4).jpg) | `123 (4).jpg` | Hardness distribution chart (with depth column in background) |
| [![123 (5)](123%20(5).jpg)](123%20(5).jpg) | `123 (5).jpg` | Well 2 MWD records (formation J2t) |

**Image links (local, relative paths):**

- [123 (1).jpg](123%20(1).jpg) — Hardness distribution chart — mean indentation hardness per lithology
- [123 (2).jpg](123%20(2).jpg) — Well 1 MWD records (formation K1q)
- [123 (3).jpg](123%20(3).jpg) — Lithology statistics + hardness-grade distribution
- [123 (4).jpg](123%20(4).jpg) — Hardness distribution chart (with depth column in background)
- [123 (5).jpg](123%20(5).jpg) — Well 2 MWD records (formation J2t)
- [111.png](111.png) — Payment QR code

---

## 14. Purchase / Payment

Here is a pay link on Stripe ( https://buy.stripe.com/3cs8yP7sY87d0vu9AB ). Please contact me lonlonago@foxmail.com after funding $89, and I will send you a complete data files , thank you!

![Payment QR](111.png)
