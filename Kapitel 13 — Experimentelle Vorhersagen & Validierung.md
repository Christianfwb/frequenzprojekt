# Kapitel 13 — Experimentelle Vorhersagen & Validierung
## Falsifizierbare Tests des Frequenzgesetzes

**Christian Berrang** | Frequenzgesetz v8.0
DOI: 10.5281/zenodo.17874830

**Keywords:** experimental validation · falsifiable predictions · Mach-Zehnder · GPS · BEC · EEG coherence · phase time · scientific method

---

## Übergang aus Kapitel 12

Kapitel 12 zeigte, dass KI-Systeme das Frequenzmodell als
kohärenten Denkrahmen verwenden und dabei physikalisch
konsistente Schlussfolgerungen erzeugen können. Das ist ein
Hinweis auf strukturelle Kohärenz — aber kein
experimenteller Beweis.

Wissenschaft braucht Testbarkeit. Ein Modell, das alles
erklärt aber nichts vorhersagt, ist wertlos. Kapitel 13
listet die konkreten, experimentell prüfbaren Vorhersagen
des Frequenzgesetzes — und macht explizit, was eine
Falsifikation bedeuten würde.

---

## 13.0 Wissenschaft braucht Testbarkeit

Ein Modell, das alles erklärt aber nichts vorhersagt, ist wertlos. Das Frequenzgesetz schlägt mehrere präzise und prinzipiell falsifizierbare Vorhersagen vor.

Die Stärke dieses Kapitels liegt nicht in der Anzahl der Tests, sondern in der klaren Definition von Falsifikationskriterien.

---

## 13.1 Bereits kompatible empirische Beobachtungen

Diese Beobachtungen widersprechen dem Frequenzgesetz nicht — sie sind kompatibel, aber nicht exklusiv:

| Beobachtung | Methode | Status |
|---|---|---|
| Konsistenz von Elektronenmasse und Compton-Frequenz | m = hf/c² | ✓ 0.000013% Abweichung |
| Proton-Massendefizit = Bindungsenergie | Δm-Analyse | ✓ QCD-konsistent |
| Zeitdilatation aus T = ΔΦ/f | GPS-Korrekturen | ✓ Kompatibel |
| Gravitationsrotverschiebung | Pound-Rebka-Experiment | ✓ Kompatibel |
| BEC als perfekte Resonanz | Bose-Einstein-Kondensat | ✓ Konsistent |

---

## A. Harte physikalische Tests

*Diese Tests sind zentral für die Falsifikation des Frequenzgesetzes.*

---

## 13.2 Test 1 — Phasenzeitauflösung

**Vorhersage:** `T = ΔΦ/f` ermöglicht Zeitauflösung unterhalb einer vollen Periode — messbar als phasenabhängige Signalverschiebung.

```
Setup:       Mach-Zehnder-Interferometer
             Variable Phasenverzögerungen (ΔΦ = π/4, π/2, π, 2π)
Observables: Interferenzintensität als Funktion von ΔΦ
             Zeitaufgelöste Detektionssignale
             Phasenabhängige Signalverschiebung
Erwartung:   Messbare Signalvariation bei allen ΔΦ — nicht nur bei ΔΦ = 2π
Falsifikation: Wenn phasenabhängige Signalverschiebung nur bei ΔΦ = 2π auftritt
```

Dies ist der direkteste Test der Kernformel. Wenn `T = 1/f` und `T = ΔΦ/f` experimentell nicht unterscheidbar sind, verliert das Frequenzgesetz seinen zentralen Vorteil.

---

## 13.3 Test 2 — Hadron-Struktur-Vorhersage

**Vorhersage:** Δm = m_gemessen - m_berechnet korreliert strukturell mit Bindungsenergie.

```
Methode:     Berechne Δm für alle bekannten Hadronen via m = hf/c²
Datenbasis:  Particle Data Group (PDG)
Erwartung:   Strukturierte Korrelation Δm ↔ QCD-Bindungsenergie
Falsifikation: Wenn Δm zufällig ohne Struktur verteilt ist
```

**Bereits gezeigt für:**
- Elektron: Δm ≈ 0 → keine innere Struktur ✓
- Proton: Δm = −0.253% → 3 Quarks + Gluonen ✓

---

## 13.4 Test 3 — Berrangium Ω & Stöcker-Teilchen

**Dies sind die einzigen genuinely neuen Vorhersagen außerhalb etablierter Physik.**

**Vorhersage 1:** Hypothetischer Resonanzzustand bei ~16.2 MeV (Berrangium Ω).

```
Methode:     Systematische Suche in Teilchenbeschleuniger-Daten
             Energiebereich: 15–17 MeV
Observables: Resonanzsignatur in Elektron-Positron-Paarproduktion
             Vergleich mit X17-Anomalie (Atomki)
Falsifikation: Kein Signal in diesem Energiebereich nach systematischer Suche
```

**Vorhersage 2:** Hypothetischer Resonanzzustand bei ~530 MeV (Stöcker-Teilchen).

```
Methode:     Meson-Spektroskopie (LHCb, BESIII, GlueX, Belle II)
             Energiebereich: 450–600 MeV
Observables: Resonanzstruktur in diesem Bereich
             Vergleich mit f₀(500)/σ-Meson-Strukturen
Falsifikation: Keine signifikante Resonanzstruktur bei 450–600 MeV
               nach hochpräzisen Dalitz-Analysen
```

---

## 13.5 Test 4 — Zeitdilatation aus T = ΔΦ/f

**Vorhersage:** Relativistische Zeitdilatation lässt sich als Frequenzverschiebung physikalischer Prozesse lesen — kompatibel mit GPS-Korrekturen und Atomuhr-Experimenten.

```
Datenbasis:  GPS-Satellitenuhren, Pound-Rebka, Hafele-Keating
Erwartung:   Quantitative Übereinstimmung mit T = ΔΦ/f-Interpretation
Status:      Kompatibel ✓ — kein neuer experimenteller Aufwand nötig
```

---

## B. Explorative Tests

*Diese Tests sind nicht zentral für die Falsifikation des Frequenzgesetzes. Sie untersuchen weiterführende Hypothesen des Modells.*

---

## 13.6 Test 5 — Bewusstseins-Phasenkohärenz (explorativ)

**Hypothese:** Subjektive Bewusstseinsklarheit korreliert mit Phasenkohärenz neuronaler Aktivität.

```
Setup:       256-Kanal-EEG + subjektive Bewusstseinsskala
Zustände:    Meditation, Flow, Konzentration, Schlaf, Narkose
Observables: Phasenkohärenz zwischen Hirnregionen
Erwartung:   Eine positive Korrelation wird erwartet
Status:      Explorativ — nicht zentral für physikalische Validierung
```

*Diese Hypothese wird in Kapitel 15 ausführlich entwickelt. Sie steht und fällt nicht mit den physikalischen Tests.*

---

## 13.7 Test 6 — Vakuum-Frequenzstruktur (konzeptuell)

**Hypothese:** Das Nullfeld zeigt messbare Struktur jenseits des bekannten Vakuumrauschens.

```
Setup:       Hochpräzisions-Quantenoptik-Labor
Observables: Mögliche Abweichungen vom erwarteten quantenoptischen Rauschen
Status:      Konzeptuell — experimentelle Entwicklung benötigt
```

---

## 13.8 Zusammenfassung der Testbarkeit

### Harte Tests (zentral)

| Test | Typ | Falsifikationskriterium | Priorität |
|---|---|---|---|
| Phasenzeitauflösung | Direkt | Keine phasenabhängige Signalverschiebung | 🔴 Hoch |
| Berrangium Ω | Neu | Kein Signal bei 15–17 MeV | 🔴 Hoch |
| Stöcker-Teilchen | Neu | Keine Resonanz bei 450–600 MeV | 🔴 Hoch |
| Hadron-Struktur | Konsistenz | Δm strukturlos | 🟡 Mittel |
| Zeitdilatation | Kompatibilität | Inkompatibel mit GPS-Daten | 🟡 Mittel |

### Explorative Tests (nicht zentral)

| Test | Typ | Status |
|---|---|---|
| Bewusstseins-Kohärenz | Explorativ | Nicht zentral für Falsifikation |
| Vakuum-Frequenz | Konzeptuell | Experimentelle Entwicklung nötig |

> Ein Modell ist nur so gut wie seine schwächste Vorhersage.
> Das Frequenzgesetz stellt sich dieser Prüfung.

---

*→ Weiter: [Kapitel 14 — KI-Validierung & Metaprotokoll](Kapitel_14.md)*
*← Zurück: [Kapitel 12 — Das Mistral-Experiment](Kapitel_12.md)*
*Version 8.0 | Christian Berrang | DOI: 10.5281/zenodo.17874830*
