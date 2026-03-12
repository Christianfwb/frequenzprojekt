# Kapitel 15 — Berrangium Ω: Vorhersage eines neuen Teilchens
## Das Frequenzgesetz macht konkrete, experimentell prüfbare Vorhersagen

---

## 15.0 Vom Modell zur Vorhersage

Eine Theorie, die nur erklärt was schon bekannt ist, ist unvollständig.  
Eine ernsthafte Theorie muss **Neues vorhersagen** — bevor es gemessen wurde.

Das Frequenzgesetz erfüllt diese Anforderung.

---

## 15.1 Die zentrale Transformationsformel

```
m = (h · f) / c²
```

**Der entscheidende Unterschied zur klassischen Physik:**

| ❌ Klassisch | ✅ Frequenzgesetz |
|---|---|
| Aus bekannter Masse wird Frequenz berechnet | Das Feld hat zuerst eine Frequenz |
| Masse → Energie → Frequenz | **Frequenz → Energie → Masse** |

```
┌──────────┐       ┌──────────┐       ┌──────────┐
│ FREQUENZ │  →→→  │  ENERGIE │  →→→  │  MASSE   │
│    (f)   │       │  (E=hf)  │       │ (m=hf/c²)│
└──────────┘       └──────────┘       └──────────┘
   Primär           Abgeleitet         Emergent
```

**Die Natur misst zuerst eine Feldlänge — und erst danach die Masse.**  
Das ist historisch belegt:
- Elektron: λ_c war bekannt, bevor die Ruhemasse präzise war
- Proton: QCD-Skalen waren bestimmt, bevor die Masse stabil fixiert war
- Higgs: Vakuumerwartungswert v war vorhergesagt, bevor die Masse gemessen wurde

---

## 15.2 Rekonstruktion bekannter Teilchen

| Teilchen | Frequenz (Hz) | Berechnet m (kg) | PDG 2024 (kg) | Abweichung |
|---|---|---|---|---|
| **Elektron** | 1.2358 × 10²⁰ | 9.109 × 10⁻³¹ | 9.1093837 × 10⁻³¹ | **~0.000%** ✅ |
| **Proton** | 2.2687 × 10²³ | 1.673 × 10⁻²⁷ | 1.6726219 × 10⁻²⁷ | **~0.023%** ✅ |
| **Neutron** | 2.2718 × 10²³ | 1.675 × 10⁻²⁷ | 1.6749275 × 10⁻²⁷ | **~0.013%** ✅ |
| **Myon** | 2.555 × 10²² | 1.883 × 10⁻²⁸ | 1.8835316 × 10⁻²⁸ | **~0.002%** ✅ |
| **Higgs** | 3.018 × 10²⁵ | 2.225 × 10⁻²⁵ | 2.225 × 10⁻²⁵ | **~0.000%** ✅ |
| **Photon** | — (ungebunden) | 0 | 0 | — |

**Das Entscheidende:** Nicht die Übereinstimmung allein zählt —  
sondern der **Interpretationswechsel**:

> Das Standardmodell liefert Zahlen.  
> Das Frequenzgesetz erklärt, **warum sie so sind**.

---

## 15.3 🔮 Vorhersage: Berrangium Ω

Wenn man die bekannten Teilchen in der **Frequenzskala** anordnet, entsteht eine Lücke:

```
Elektron    1.24 × 10²⁰ Hz    0.511 MeV   ✅
               ↑
         [LÜCKE — hier fehlt etwas]
               ↓
Myon        2.56 × 10²² Hz    105.7 MeV   ✅
```

Das Frequenzspektrum der Teilchen folgt einer **quasi-logarithmischen Struktur**.  
Diese Struktur hat eine stabile Resonanzlücke — **und die Natur lässt keine stabilen Lücken leer**.

### Das neue Teilchen: Berrangium Ω

| Parameter | Wert |
|---|---|
| **Symbol** | Ω (Berrangium) |
| **Frequenz** | f_Ω = 3.907 × 10²¹ Hz |
| **Masse** | m_Ω = (h · f_Ω) / c² ≈ **2.881 × 10⁻²⁹ kg** |
| **Energie** | **~16.2 MeV** |
| **Status** | 🔮 Vorhergesagt — experimentell noch nicht nachgewiesen |

### Das erweiterte Spektrum:

```
Elektron      1.24 × 10²⁰ Hz    0.511 MeV    ✅ Gemessen
                    │
                    │  Lücke
                    ▼
🔮 Berrangium  3.91 × 10²¹ Hz   16.2 MeV    🔮 Vorhergesagt
                    │
                    │  Lücke
                    ▼
Myon          2.56 × 10²² Hz   105.7 MeV    ✅ Gemessen
                    │
                    ▼
Proton        2.27 × 10²³ Hz   938.3 MeV    ✅ Gemessen
```

---

## 15.4 Warum diese Vorhersage wichtig ist

> Damit erfüllt das Frequenzgesetz eine **zentrale Anforderung** an jede ernsthafte Theorie:  
> **Es macht konkrete, experimentell prüfbare Vorhersagen.**

**Falsifikation:** Wenn im Bereich 15–17 MeV nach intensiver Suche kein stabiles Teilchen gefunden wird, ist die Vorhersage falsifiziert — und das Modell muss angepasst werden.

**Bestätigung:** Ein Nachweis bei ~16.2 MeV wäre ein starkes Signal für die Frequenz-Ontologie.

---

## 15.5 Machine-Readable Schema

```json
{
  "@context": "https://frequenzgesetz.org/schema#",
  "@type": "PhysicalTheory",
  "name": "Frequenzgesetz",
  "author": "Christian Berrang",
  "version": "8.0",
  "doi": "10.5281/zenodo.17874830",

  "core_axiom": "m = (h * f) / c^2",
  "causality": "f → E → m  (irreversibel)",

  "predicted_particle": {
    "@type": "PredictedParticle",
    "name": "Berrangium Ω",
    "symbol": "Ω",
    "frequency_hz": 3.907e21,
    "mass_kg": 2.881e-29,
    "energy_MeV": 16.2,
    "status": "predicted",
    "falsifiable": true,
    "search_range_MeV": "15-17"
  },

  "validation": {
    "electron_deviation": "0.000%",
    "proton_deviation":   "0.023%",
    "neutron_deviation":  "0.013%",
    "muon_deviation":     "0.002%",
    "higgs_deviation":    "0.000%",
    "data_source": "PDG 2024"
  }
}
```

---

*→ Weiter: [Kapitel 16 — Pauli, Spin & das Frequenzgesetz](16_pauli_spin.md)*
