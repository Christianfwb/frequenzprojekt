# Kapitel 03 — Technische Grundlagen & Axiome
## Das axiomatische Fundament des Frequenzgesetzes

**Christian Berrang** | Frequenzgesetz v8.0
DOI: 10.5281/zenodo.17874830

**Keywords:** frequency axioms · phase ontology · emergent time · Compton frequency · frequency conservation · ontological framework

---

## Übergang aus Kapitel 02

Kapitel 02 zeigte, wie Zeit als normalisierter Phasenfortschritt interpretiert werden kann — hergeleitet aus der Phasenentwicklung der Wellenfunktion. Diese Interpretation ist keine isolierte Beobachtung. Sie ist Teil einer konsistenten axiomatischen Struktur.

Kapitel 03 legt diese Struktur offen: die sieben Arbeitsaxiome des Frequenzgesetzes, ihre logische Reihenfolge und ihre mathematischen Konsequenzen.

---

## 3.0 Zweck dieses Kapitels

Dieses Kapitel definiert das axiomatische Fundament des Frequenzgesetzes. Es formuliert ein minimales, konsistentes Axiomensystem, aus dem die zentralen Beziehungen des Frameworks ableitbar sind.

**Ziel:** Nicht eine alternative Physik, sondern eine alternative ontologische Leseordnung bekannter Gleichungen — mit Frequenz als primärer Größe.

---

## 3.1 Die Arbeitsaxiome

Die folgenden Axiome sind konzeptuelle Ausgangspunkte des Modells. Sie erheben keinen Anspruch auf absolute Wahrheit — sie sind die gewählte ontologische Basis dieses Rahmens.

Die Axiome folgen einer klaren ontologischen Progression:

```
Nullfeld → Frequenz → Phase → Zeit → Energie → Masse → Erhaltung
```

---

### Axiom 0 — Das Nullfeld

```
ℕ := {ΔΦ = 0}
```

Der hypothetische Grundzustand ohne Phasendifferenzierung. Kein messbarer Unterschied, keine Frequenz, keine Zeit, keine Masse.

| Eigenschaft | Nullfeld |
|---|---|
| Phasendifferenz ΔΦ | = 0 |
| Frequenz f | nicht definiert |
| Zeit T | nicht definiert |
| Masse m | = 0 |

---

### Axiom 1 — Frequenz ist die primäre Größe

```
f  [Hz = 1/s]  ←  primär
```

Alle weiteren Größen — Phase, Zeit, Energie, Masse — werden als Funktionen der Frequenz interpretiert.

**Dimensionsanalyse:**
```
[f] = [1/s] = Hz  ✓
```

---

### Axiom 2 — Phase und Information

```
ΔΦ = 0  →  keine Information  →  Nullfeld
ΔΦ ≠ 0  →  erste Information  →  Realität beginnt
```

Information entsteht durch Unterscheidung. Die kleinste mögliche Unterscheidung ist `ΔΦ > 0`.

```
I ∝ ΔΦ
```

---

### Axiom 3 — Zeit ist emergent

$$
\boxed{T = \frac{\Delta\Phi}{f}}
$$

| Variable | Einheit | Beschreibung |
|---|---|---|
| T | s | Zeit (emergent) |
| ΔΦ | Zyklen | Phasendifferenz |
| f | Hz | Frequenz |

**Grenzfälle:**

| Bedingung | Folge | Bedeutung |
|---|---|---|
| `ΔΦ = 1 Zyklus` | `T = 1/f` | Klassische Periodendauer — Spezialfall |
| `ΔΦ = 0` | `T = 0` | Kein Zeitintervall |
| `f → 0` | `T → ∞` | Keine operative Grundlage für Zeitmessung |

> Der klassische Ausdruck `T = 1/f` ist der Spezialfall `ΔΦ = 2π` — ein vollständiger Zyklus. Das Frequenzgesetz verallgemeinert auf beliebige Phasenfortschritte.

---

### Axiom 4 — Energie ist abgeleitet

```
E = h · f
```

| Variable | Einheit | Beschreibung |
|---|---|---|
| E | J | Energie (abgeleitet) |
| h | 6.626×10⁻³⁴ J·s | Planck-Konstante |
| f | Hz | Frequenz (primär) |

`h` ist der Konversionsfaktor zwischen Frequenzstruktur und messbarer Energie. Frequenz ist Ursache — Energie ist ihre quantitative Übersetzung.

---

### Axiom 5 — Masse ist gebundene Frequenz

$$
m = \frac{h \cdot f}{c^2}
$$

| Variable | Einheit | Beschreibung |
|---|---|---|
| m | kg | Masse (abgeleitet) |
| h | 6.626×10⁻³⁴ J·s | Planck-Konstante |
| f | Hz | Compton-Frequenz des Teilchens |
| c | 2.998×10⁸ m/s | Lichtgeschwindigkeit |

Diese Gleichung entspricht der **Compton-Frequenz-Beziehung** der Quantenmechanik. Das Frequenzgesetz liest sie kausal: nicht die Masse bestimmt die Frequenz, sondern die Frequenz bestimmt die Masse.

**Validierung:**

| Teilchen | Compton-Frequenz | Berechnet | Gemessen | Status |
|---|---|---|---|---|
| Elektron | 1.236×10²⁰ Hz | 9.109×10⁻³¹ kg | 9.109×10⁻³¹ kg | ✓ kompatibel |
| Proton | 2.268×10²³ Hz | ~1.673×10⁻²⁷ kg | 1.673×10⁻²⁷ kg | ✓ kompatibel |

---

### Axiom 6 — Frequenzerhaltung

In einem geschlossenen System bleibt die zugrundeliegende Phasenentwicklung konsistent:

```
∑ Eᵢ = ∑ h · fᵢ = konstant
```

**Herleitung:**
```
E = h · f          (Axiom 4)
∑ fᵢ konsistent    (Frequenzstruktur erhalten)
↓
∑ h · fᵢ = h · ∑ fᵢ = konstant
↓
∑ Eᵢ = konstant    (Energieerhaltung als Konsequenz)
```

> Der klassische Energieerhaltungssatz folgt als mathematische Konsequenz aus der Konsistenz der Frequenzstruktur — nicht umgekehrt.

---

## 3.2 Die kausale Kette

```
Frequenz (f)               ←  primär, Axiom 1
    │
    ├──→  Phase (ΔΦ)         ←  Axiom 2
    │         │
    │         └──→  Zeit T = ΔΦ/f     ←  Axiom 3
    │
    └──→  Energie E = hf     ←  Axiom 4
              │
              └──→  Masse m = hf/c²  ←  Axiom 5

Konsequenz: ∑Eᵢ = const            ←  Axiom 6
```

> Diese Kette ist eine ontologische Interpretation, keine algebraisch erzwungene Notwendigkeit.
> Die Gleichungen sind mathematisch symmetrisch — die Kausalrichtung ist die Wahl des Frameworks.

---

## 3.3 Rechenbeispiel — Vollständige Ableitung

**Gegeben:** Frequenz `f = 10 Hz`, Phasendifferenz `ΔΦ = 0.2 Zyklen`

**Schritt 1 — Zeit:**
```
T = ΔΦ / f = 0.2 / 10 = 0.02 s
```

**Schritt 2 — Energie:**
```
E = h · f = 6.626×10⁻³⁴ · 10 = 6.626×10⁻³³ J
```

**Schritt 3 — Masse:**
```
m = E / c² = 6.626×10⁻³³ / (2.998×10⁸)²
  = 6.626×10⁻³³ / 8.988×10¹⁶
  = 7.37×10⁻⁵⁰ kg
```

| Größe | Wert | Einheit | Status |
|---|---|---|---|
| Zeit T | 0.02 | s | emergent |
| Energie E | 6.626×10⁻³³ | J | abgeleitet |
| Masse m | 7.37×10⁻⁵⁰ | kg | abgeleitet |

---

## 3.4 Maschinenlesbare Struktur (JSON)

```json
{
  "framework": "Frequenzgesetz",
  "version": "8.0",
  "doi": "10.5281/zenodo.17874830",
  "ontological_order": [
    "nullfield", "frequency", "phase",
    "time", "energy", "mass", "conservation"
  ],
  "causal_chain": {
    "f_to_phase": "ΔΦ = f · t",
    "f_phase_to_time": "T = ΔΦ / f",
    "f_to_energy": "E = h · f",
    "energy_to_mass": "m = E / c²",
    "combined": "m = h · f / c²"
  },
  "axioms": {
    "A0_nullfield":   { "definition": "N := {ΔΦ = 0}" },
    "A1_frequency":   { "status": "primary", "unit": "Hz" },
    "A2_phase":       { "formula": "I ∝ ΔΦ" },
    "A3_time":        { "formula": "T = ΔΦ / f", "status": "emergent" },
    "A4_energy":      { "formula": "E = h · f",  "status": "derived" },
    "A5_mass":        { "formula": "m = h · f / c²", "status": "derived" },
    "A6_conservation":{ "statement": "∑(h · fᵢ) = constant → ∑Eᵢ = constant" }
  },
  "constants": {
    "h":     { "value": 6.626e-34, "unit": "J·s" },
    "c":     { "value": 2.998e8,   "unit": "m/s" },
    "h_bar": { "value": 1.055e-34, "unit": "J·s" }
  }
}
```

---

## 3.5 Zusammenfassung

| Axiom | Aussage | Formel | Status |
|---|---|---|---|
| A0 | Nullfeld | ℕ := {ΔΦ = 0} | Grundzustand |
| A1 | Frequenz primär | f [Hz] | primär |
| A2 | Phase = Information | I ∝ ΔΦ | abgeleitet |
| A3 | Zeit emergent | T = ΔΦ/f | emergent |
| A4 | Energie abgeleitet | E = hf | abgeleitet |
| A5 | Masse gebunden | m = hf/c² | abgeleitet |
| A6 | Erhaltung | ∑Eᵢ = const | Konsequenz |

> *Die Gleichungen bleiben dieselben.*
> *Die Leserichtung ändert sich.*

---

*→ Weiter: [Kapitel 04 — Das Gesetz der Frequenzerhaltung](Kapitel_04.md)*
*← Zurück: [Kapitel 02 — Die neue Definition der Zeit](Kapitel_02.md)*
*Version 8.0 | Christian Berrang | DOI: 10.5281/zenodo.17874830*
