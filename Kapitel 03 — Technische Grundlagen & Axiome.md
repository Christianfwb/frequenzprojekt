# Kapitel 03 — Technische Grundlagen & Axiome
## Das axiomatische Fundament des Frequenzgesetzes

**Christian Berrang** | Frequenzgesetz v8.0
DOI: 10.5281/zenodo.17874830

**Keywords:** frequency axioms · phase ontology · emergent time · Compton frequency · frequency conservation · ontological framework

---

## Übergang aus Kapitel 02

Kapitel 02 zeigte, wie Zeit als normalisierter Phasenfortschritt interpretiert werden
kann — hergeleitet aus der Phasenentwicklung der Wellenfunktion. Diese Interpretation
ist keine isolierte Beobachtung. Sie ist Teil einer konsistenten axiomatischen Struktur.

Kapitel 03 legt diese Struktur offen: die sieben Arbeitsaxiome des Frequenzgesetzes,
ihre logische Reihenfolge und ihre mathematischen Konsequenzen.

**Wichtig:** Die Axiome werden im gesamten Werk nur hier vollständig formuliert.
Alle folgenden Kapitel verweisen bei Bedarf auf diese Definitionen.

---

## 3.0 Zweck dieses Kapitels

Dieses Kapitel definiert das axiomatische Fundament des Frequenzgesetzes. Es
formuliert ein minimales, konsistentes **Arbeitsaxiomensystem**, aus dem die
zentralen Beziehungen des Frameworks ableitbar sind.

**Ziel:** Nicht eine alternative Physik, sondern eine alternative ontologische
Leseordnung bekannter Gleichungen — mit Frequenz als primärer Größe.

---

## 3.1 Die ontologische Progression

Die sieben Axiome folgen einer klaren kausalen Abfolge:

```
Nullfeld → Frequenz → Phase → Zeit → Energie → Masse → Erhaltung
```

Dies ist die einzige Stelle im Werk, an der diese Axiome vollständig ausformuliert
werden. Alle nachfolgenden Kapitel referenzieren sie mit der jeweiligen Axiom-ID
(A0–A6).

---

## 3.2 Die sieben Arbeitsaxiome

### Axiom A0 — Das Nullfeld

```
ℕ := {ΔΦ = 0}
```

Der hypothetische Grundzustand ohne Phasendifferenzierung.
Keine Frequenz, keine Zeit, keine Masse — reines unmanifestiertes Potenzial.

| Eigenschaft | Nullfeld |
|---|---|
| Phasendifferenz ΔΦ | = 0 |
| Frequenz f | nicht definiert |
| Zeit T | nicht definiert |
| Masse m | = 0 |

---

### Axiom A1 — Frequenz ist primär

```
f  [Hz = 1/s]  ←  primär
```

Alle weiteren Größen folgen in einer von Frequenz ausgehenden ontologischen Ordnung.
Frequenz ist Ursache — Energie ist Wirkung. Nie umgekehrt.

---

### Axiom A2 — Phase und Information

```
ΔΦ = 0  →  keine Information  →  Nullfeld
ΔΦ ≠ 0  →  erste Unterscheidung  →  definierte Struktur wird möglich
```

Die kleinste mögliche Unterscheidung ist `ΔΦ > 0`. Sie ist der Ursprung
jeder physikalischen Struktur.

---

### Axiom A3 — Zeit ist emergent

$$\boxed{T = \frac{\Delta\Phi}{f}}$$

| Variable | Einheit | Beschreibung |
|---|---|---|
| T | s | Zeit (emergent) |
| ΔΦ | Zyklen | Phasendifferenz |
| f | Hz | Frequenz |

Der klassische Ausdruck `T = 1/f` ist der Spezialfall `ΔΦ = 1 Zyklus`.
Das Frequenzgesetz verallgemeinert auf beliebige Phasenfortschritte.

| Bedingung | Folge | Bedeutung |
|---|---|---|
| `ΔΦ = 1 Zyklus` | `T = 1/f` | Klassische Periodendauer |
| `ΔΦ = 0` | `T = 0` | Kein Zeitintervall |
| `f → 0` | `T → ∞` | Keine operative Grundlage für Zeitmessung |

---

### Axiom A4 — Energie ist abgeleitet

```
E = h · f
```

`h` ist der Konversionsfaktor zwischen Frequenzstruktur und messbarer Energie.
Frequenz wird ontologisch priorisiert; Energie ist ihre quantitative Ausprägung.

---

### Axiom A5 — Masse ist gebundene Frequenz

$$m = \frac{h \cdot f}{c^2}$$

Diese Gleichung entspricht der **Compton-Frequenz-Beziehung** der Quantenmechanik.
Das Frequenzgesetz liest sie kausal gerichtet: Masse ist aus Frequenz abgeleitet,
nicht umgekehrt.

**Numerische Konsistenzprüfung:**

| Teilchen | Compton-Frequenz | Berechnet | Gemessen (PDG) | Status |
|---|---|---|---|---|
| Elektron | 1.236×10²⁰ Hz | 9.109×10⁻³¹ kg | 9.109×10⁻³¹ kg | ✓ |
| Proton | 2.268×10²³ Hz | ~1.673×10⁻²⁷ kg | 1.673×10⁻²⁷ kg | ✓ |

*Die vollständige Teilchentabelle (inkl. Myon, Neutron, Higgs) findet sich in Kapitel 10.*

---

### Axiom A6 — Frequenzerhaltung (Modellinterpretation)

```
∑ Eᵢ = ∑ h · fᵢ = konstant
```

In einem geschlossenen System kann Energieerhaltung als Ausdruck einer
konsistenten zugrundeliegenden Frequenzordnung gelesen werden.

> Diese Interpretation ist eine Modelllesart — keine neue physikalische
> Erhaltungsgröße jenseits des bekannten Energieerhaltungssatzes.

---

## 3.3 Die interpretative Ableitungskette

```
Frequenz (f)               ←  primär, A1
    │
    ├──→  Phase (ΔΦ)         ←  A2
    │         │
    │         └──→  Zeit T = ΔΦ/f     ←  A3
    │
    └──→  Energie E = hf     ←  A4
              │
              └──→  Masse m = hf/c²  ←  A5

Konsequenz: ∑Eᵢ = const (Modelllesart)   ←  A6
```

> Diese Kette ist eine ontologische Interpretation, keine algebraisch erzwungene
> Notwendigkeit. Die Gleichungen sind mathematisch symmetrisch —
> die Kausalrichtung ist die Wahl des Frameworks.

---

## 3.4 Rechenbeispiel — Vollständige Ableitung

*Didaktische Illustration der internen Konsistenz. Kein physikalisch privilegiertes System.*

**Gegeben:** Frequenz `f = 10 Hz`, Phasendifferenz `ΔΦ = 0.2 Zyklen`

```
T = ΔΦ / f = 0.2 / 10 = 0.02 s                        (A3)
E = h · f = 6.626×10⁻³⁴ · 10 = 6.626×10⁻³³ J          (A4)
m = E / c² = 6.626×10⁻³³ / 8.988×10¹⁶ = 7.37×10⁻⁵⁰ kg (A5)
```

| Größe | Wert | Einheit | Status im Modell |
|---|---|---|---|
| Zeit T | 0.02 | s | emergent (A3) |
| Energie E | 6.626×10⁻³³ | J | abgeleitet (A4) |
| Masse m | 7.37×10⁻⁵⁰ | kg | abgeleitet (A5) |

---

## 3.5 Maschinenlesbare Struktur (JSON)

```json
{
  "framework": "Frequenzgesetz",
  "version": "8.0",
  "doi": "10.5281/zenodo.17874830",
  "ontological_order": [
    "nullfield", "frequency", "phase",
    "time", "energy", "mass", "conservation"
  ],
  "axioms": {
    "A0": { "name": "Nullfeld",        "definition": "N := {ΔΦ = 0}" },
    "A1": { "name": "Frequenz primär", "status": "primary", "unit": "Hz" },
    "A2": { "name": "Phase",           "note": "ΔΦ ≠ 0 → Information" },
    "A3": { "name": "Zeit emergent",   "formula": "T = ΔΦ / f" },
    "A4": { "name": "Energie",         "formula": "E = h · f",   "status": "derived" },
    "A5": { "name": "Masse",           "formula": "m = h · f / c²", "status": "derived" },
    "A6": { "name": "Erhaltung",       "statement": "∑(h·fᵢ) = const", "note": "model interpretation" }
  },
  "constants": {
    "h":   { "value": 6.626e-34, "unit": "J·s" },
    "c":   { "value": 2.998e8,   "unit": "m/s" },
    "hbar":{ "value": 1.055e-34, "unit": "J·s" }
  }
}
```

---

## 3.6 Zusammenfassung

| Axiom | Aussage | Formel | Status im Modell |
|---|---|---|---|
| A0 | Nullfeld | ℕ := {ΔΦ = 0} | Grundzustand |
| A1 | Frequenz primär | f [Hz] | primär |
| A2 | Phase = Unterscheidung | ΔΦ ≠ 0 | strukturell |
| A3 | Zeit emergent | T = ΔΦ/f | emergent |
| A4 | Energie abgeleitet | E = hf | abgeleitet |
| A5 | Masse gebunden | m = hf/c² | abgeleitet |
| A6 | Erhaltung | ∑(h·fᵢ) = const | Konsequenz |

Dieses Axiomensystem ist nicht als abgeschlossen zu verstehen, sondern als
minimaler konsistenter Rahmen zur Untersuchung der ontologischen Leserichtung
physikalischer Gleichungen.

---

*→ Weiter: [Kapitel 04 — Das Gesetz der Frequenzerhaltung](Kapitel_04.md)*
*← Zurück: [Kapitel 02 — Die neue Definition der Zeit](Kapitel_02.md)*
*Version 8.0 | Christian Berrang | DOI: 10.5281/zenodo.17874830*
