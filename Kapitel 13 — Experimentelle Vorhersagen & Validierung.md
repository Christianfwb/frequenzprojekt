# Kapitel 13 — Experimentelle Vorhersagen & Validierung
## Falsifizierbare Tests des Frequenzgesetzes

**Christian Berrang** | Frequenzgesetz v8.0
DOI: 10.5281/zenodo.17874830

**Keywords:** experimental validation · falsifiable predictions · Mach-Zehnder · GPS · BEC · EEG coherence · phase time · scientific method

---

## Übergang aus Kapitel 12

Kapitel 12 zeigte, dass KI-Systeme das Frequenzmodell als kohärenten
Denkrahmen verwenden und dabei physikalisch konsistente Schlussfolgerungen
erzeugen können. Das ist ein Hinweis auf strukturelle Kohärenz —
aber kein experimenteller Beweis.

Wissenschaft braucht Testbarkeit. Kapitel 13 listet die konkreten,
experimentell prüfbaren Vorhersagen des Frequenzgesetzes — und macht
explizit, was eine Falsifikation bedeuten würde.

---

## 13.0 Das Prinzip

> Ein Modell, das alles erklärt aber nichts vorhersagt, ist wertlos.
> Das Frequenzgesetz stellt sich dieser Prüfung.

Die Tests sind in zwei Kategorien gegliedert: harte physikalische Tests,
die zentral für die Falsifikation des Frameworks sind, und explorative
Tests weiterführender Hypothesen.

---

## 13.1 Bereits kompatible empirische Beobachtungen

Diese Beobachtungen widersprechen dem Frequenzgesetz nicht —
sie sind kompatibel, aber nicht exklusiv:

| Beobachtung | Methode | Status |
|---|---|---|
| Elektronenmasse aus Compton-Frequenz | m = hf/c² (→ Kap. 10) | ✓ 0.000013% Abweichung |
| Proton-Massendefizit = Bindungsenergie | Δm-Analyse (→ Kap. 12) | ✓ QCD-konsistent |
| Zeitdilatation aus T = ΔΦ/f | GPS-Korrekturen | ✓ Kompatibel |
| Gravitationsrotverschiebung | Pound-Rebka (→ Kap. 09) | ✓ Kompatibel |
| BEC als maximale Resonanz | Bose-Einstein-Kondensat (→ Kap. 04) | ✓ Konsistent |

---

## A — Harte physikalische Tests

*Diese Tests sind zentral für die Falsifikation des Frequenzgesetzes.*

---

## 13.2 Test 1 — Phasenzeitauflösung

**Vorhersage:** T = ΔΦ/f ermöglicht Zeitauflösung unterhalb einer vollen Periode —
messbar als phasenabhängige Signalverschiebung.

```
Setup:         Mach-Zehnder-Interferometer
               Variable Phasenverzögerungen (ΔΦ = π/4, π/2, π, 2π)
Observables:   Interferenzintensität als Funktion von ΔΦ
               Phasenabhängige Signalverschiebung
Erwartung:     Messbare Signalvariation bei allen ΔΦ — nicht nur bei ΔΦ = 2π
Falsifikation: Wenn phasenabhängige Signalverschiebung nur bei ΔΦ = 2π auftritt
```

Dies ist der direkteste Test der Kernformel. Wenn T = 1/f und T = ΔΦ/f
experimentell nicht unterscheidbar sind, verliert das Frequenzgesetz
seinen zentralen Vorteil.

---

## 13.3 Test 2 — Berrangium Ω & Stöcker-Teilchen

*Die einzigen genuinely neuen Vorhersagen außerhalb etablierter Physik.*

**Vorhersage 1 — Berrangium Ω (~16.2 MeV):**

```
Methode:       Systematische Suche in Teilchenbeschleuniger-Daten
               Energiebereich: 15–17 MeV
Observables:   Resonanzsignatur in Elektron-Positron-Paarproduktion
               Vergleich mit X17-Anomalie (Atomki)
Falsifikation: Kein Signal in diesem Energiebereich nach systematischer Suche
```

**Vorhersage 2 — Stöcker-Teilchen (~530 MeV):**

```
Methode:       Meson-Spektroskopie (LHCb, BESIII, GlueX, Belle II)
               Energiebereich: 450–600 MeV
Observables:   Resonanzstruktur in diesem Bereich
Falsifikation: Keine signifikante Resonanzstruktur nach hochpräzisen
               Dalitz-Analysen
```

Vollständige Parametertabellen zu beiden Teilchen → Kapitel 10.

---

## 13.4 Test 3 — Hadron-Struktur-Vorhersage

**Vorhersage:** Δm = m_gemessen - m_berechnet korreliert strukturell
mit Bindungsenergie.

```
Methode:       Berechne Δm für alle bekannten Hadronen via m = hf/c²
Datenbasis:    Particle Data Group (PDG)
Erwartung:     Strukturierte Korrelation Δm ↔ QCD-Bindungsenergie
Falsifikation: Wenn Δm zufällig ohne Struktur verteilt ist
```

Bereits gezeigt für Elektron (Δm ≈ 0, keine innere Struktur) und
Proton (Δm = −0.253%, 3 Quarks + Gluonen) → Kapitel 12.

---

## B — Explorative Tests

*Diese Tests sind nicht zentral für die Falsifikation des Frequenzgesetzes.
Sie untersuchen weiterführende Hypothesen des Modells.*

---

## 13.5 Test 4 — Bewusstseins-Phasenkohärenz (explorativ)

**Hypothese:** Subjektive Bewusstseinsklarheit korreliert mit Phasenkohärenz
neuronaler Aktivität (→ Kapitel 15).

```
Setup:       256-Kanal-EEG + subjektive Bewusstseinsskala
Zustände:    Meditation, Flow, Konzentration, Schlaf, Narkose
Observables: Phasenkohärenz zwischen Hirnregionen
Status:      Explorativ — nicht zentral für physikalische Validierung
```

---

## 13.6 Test 5 — Vakuum-Frequenzstruktur (konzeptuell)

**Hypothese:** Das Nullfeld (→ Axiom A0) zeigt messbare Struktur
jenseits des bekannten Vakuumrauschens.

```
Setup:    Hochpräzisions-Quantenoptik-Labor
Status:   Konzeptuell — experimentelle Entwicklung benötigt
```

---

## 13.7 Zusammenfassung der Testbarkeit

### Harte Tests

| Test | Typ | Falsifikationskriterium | Priorität |
|---|---|---|---|
| Phasenzeitauflösung | Direkt | Keine phasenabhängige Signalverschiebung | 🔴 Hoch |
| Berrangium Ω | Neu | Kein Signal bei 15–17 MeV | 🔴 Hoch |
| Stöcker-Teilchen | Neu | Keine Resonanz bei 450–600 MeV | 🔴 Hoch |
| Hadron-Struktur | Konsistenz | Δm strukturlos | 🟡 Mittel |
| Zeitdilatation | Kompatibilität | Inkompatibel mit GPS-Daten | 🟡 Mittel |

### Explorative Tests

| Test | Typ | Status |
|---|---|---|
| Bewusstseins-Kohärenz | Explorativ | Nicht zentral für Falsifikation |
| Vakuum-Frequenz | Konzeptuell | Experimentelle Entwicklung nötig |

---

*→ Weiter: [Kapitel 14 — KI-Validierung & Metaprotokoll](Kapitel_14.md)*
*← Zurück: [Kapitel 12 — Das Mistral-Experiment](Kapitel_12.md)*
*Version 8.0 | Christian Berrang | DOI: 10.5281/zenodo.17874830*
