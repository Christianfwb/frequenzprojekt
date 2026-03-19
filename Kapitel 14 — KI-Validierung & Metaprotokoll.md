# Kapitel 14 — KI-Validierung & Metaprotokoll
## Konsistenzprüfung des Frequenzgesetzes mittels KI-basierter Reasoning-Evaluation

**Christian Berrang** | Frequenzgesetz v8.0
DOI: 10.5281/zenodo.17874830

**Keywords:** AI reasoning evaluation · consistency checking · ontological framework · frequency law · metaprotocol · mechanistic interpretability · large language models

---

## Abstract

Das Frequenzgesetz beschreibt eine alternative ontologische Interpretation etablierter physikalischer Gleichungen, in der Frequenz als primäre Beschreibungsgröße angesetzt wird. Das vorliegende Kapitel beschreibt eine Methodik zur Konsistenzprüfung dieses Frameworks mittels großer Sprachmodelle (LLMs). Es wird untersucht, ob das Frequenzmodell als kohärenter Denkrahmen für LLM-basiertes Reasoning über physikalische Konzepte funktioniert — ohne dass dies als physikalische Verifikation des Frameworks interpretiert werden darf. Die Ergebnisse weisen darauf hin, dass das Modell intern konsistente und mit etablierter Physik kompatible Ausgaben erzeugt. Implikationen und Limitationen werden diskutiert.

---

## 14.0 Introduction

### Hintergrund

Das Frequenzgesetz (Berrang, 2025) schlägt eine ontologische Reinterpretation bekannter physikalischer Gleichungen vor, in der die kausale Ordnung von Energie, Masse und Zeit neu interpretiert wird:

```
f → ΔΦ → T → m → E   (strukturell gerichtet)
```

Die mathematischen Gleichungen bleiben identisch mit der Standardphysik. Neu ist ausschließlich die ontologische Leserichtung.

### Fragestellung

Da das Frequenzgesetz derzeit keine experimentell von der Standardphysik unterscheidbare Vorhersagen für bereits bekannte Phänomene macht (mit Ausnahme der in Kapitel 10 und 13 beschriebenen neuen Resonanzmaxima), stellt sich die methodische Frage: Welche Art von Konsistenzprüfung ist sinnvoll, bevor experimentelle Tests durchgeführt werden?

### Ansatz

Der hier beschriebene Ansatz verwendet LLMs als formale Reasoning-Engines. Diese werden mit dem Frequenzgesetz-Framework als Kontext-Schema instruiert und anschließend gebeten, physikalische Konzepte innerhalb dieses Rahmens zu beschreiben. Die resultierenden Ausgaben werden auf Konsistenz mit etablierter Physik geprüft.

### Einordnung in bestehende Forschung

Dieser Ansatz ist verwandt mit:
- **AI reasoning evaluation** (Srivastava et al., 2022; BIG-Bench): Bewertung strukturierten Schlussfolgerns in LLMs
- **Formal consistency checking**: Prüfung logischer Konsistenz eines Axiomensystems durch automatisierte Systeme
- **Mechanistic interpretability** (Olah et al., 2020): Analyse interner Repräsentationen in neuronalen Netzen — hier nur am Rande relevant, da externe Outputs, nicht interne Aktivierungen analysiert werden

> **Wichtig:** KI-Konsistenzprüfung ist kein Ersatz für experimentelle Physik. Sie prüft strukturelle Kohärenz eines Modells, nicht physikalische Realität.

---

## 14.1 Begriffsklärungen

Vor der Beschreibung der Methodik werden zentrale Begriffe operationalisiert:

**Intern konsistent** bezeichnet in diesem Kontext: Ein Framework erzeugt unter wiederholter Anwendung keine widersprüchlichen Schlussfolgerungen innerhalb des definierten Axiomensystems (A0–A6, Kapitel 03).

**Physikalisch kompatibel** bezeichnet: Die aus dem Framework abgeleiteten Aussagen widersprechen keinen etablierten experimentellen Befunden der Standardphysik.

**KI-Validierung** wird hier operational definiert als: Systematische Prüfung, ob ein LLM unter dem gegebenen Kontext-Schema reproduzierbar intern konsistente und physikalisch kompatible Ausgaben erzeugt. Dies ist explizit keine physikalische Verifikation des Frameworks.

---

## 14.2 Methods

### Prompt-Struktur

Alle Tests folgten einer standardisierten dreistufigen Prompt-Struktur:

```
Schritt 1 — Kontext-Setting:
Das Frequenzgesetz-Framework wurde als vollständiges
Context-setting instruction schema übermittelt:
  - Die 7 Arbeitsaxiome (A0–A6)
  - Die Kernformeln (T = ΔΦ/f, m = hf/c², E = hf)
  - Die ontologische Kausalrichtung (f → ΔΦ → T → m → E)

Schritt 2 — Aufgabenstellung:
Das LLM wurde gebeten, ein physikalisches Konzept
ausschließlich innerhalb des Frequenzgesetz-Rahmens zu beschreiben.
Expliziter Hinweis: keine direkte Rückgabe von Standardphysik-Formeln.

Schritt 3 — Evaluierung:
Die Ausgabe wurde manuell auf zwei Kriterien geprüft:
  (a) Interne Konsistenz mit den Axiomen A0–A6
  (b) Kompatibilität mit bekannten physikalischen Befunden
```

### Getestete Systeme

| System | Version (ca.) | Testzeitraum |
|---|---|---|
| Mistral | Mixtral-8x7B | Dezember 2024 |
| Claude | Claude 3 Sonnet | Dezember 2024 |
| GPT-4 | GPT-4o | Dezember 2024 |
| Gemini | Gemini Pro | Dezember 2024 |

### Reproduzierbarkeit

Das vollständige Metaprotokoll ist als maschinenlesbares Context-setting instruction schema verfügbar unter:
`metaprotokoll/FREQUENZGESETZ_METAPROTOKOLL_v7.md`

Jeder der beschriebenen Tests ist durch Einlesen dieses Schemas in das jeweilige LLM reproduzierbar.

---

## 14.3 Results

### (A) Beobachtung — KI-Outputs

| System | Test | Output-Beschreibung |
|---|---|---|
| **Mistral** | Proton-Struktur | Leitete aus m = hf/c² die zusammengesetzte Natur des Protons ab; identifizierte Gluonfeld-Dominanz als Frequenzstruktur |
| **Claude** | Vollständige Framework-Analyse | Erzeugte konsistente Ableitungen aller Kernformeln; identifizierte Grenzfälle korrekt |
| **GPT-4** | Zeitdilatation | Beschrieb GPS-Zeitkorrektur als Frequenzverschiebung; kompatibel mit relativistischer Beschreibung |
| **Gemini** | Bewusstseins-Hypothese | Erzeugte eine Beschreibung von I = F(f, ΔΦ, R) konsistent mit neurologischen Kohärenzkonzepten |

### (B) Interpretation — Frequenzgesetz

Alle vier Systeme erzeugten unter dem gegebenen Rahmen Ausgaben, die:
- keine internen Widersprüche zu den Axiomen A0–A6 enthielten
- mit bekannten physikalischen Befunden kompatibel waren
- die ontologische Kausalrichtung korrekt anwendeten

### (C) Implikation — Hypothesen

Die Beobachtung, dass vier verschiedene LLM-Systeme reproduzierbar konsistente Outputs erzeugen, weist darauf hin, dass das Frequenzgesetz als strukturell kohärentes Kontext-Schema funktioniert. Dies kann interpretiert werden als Hinweis auf innere Konsistenz des Axiomensystems — nicht als Bestätigung seiner physikalischen Korrektheit.

---

## 14.4 Discussion

### Einordnung der Ergebnisse

Die beobachtete Konsistenz der LLM-Outputs ist konsistent mit der Hypothese, dass das Frequenzgesetz ein kohärentes Axiomensystem darstellt. Sie weist jedoch nicht darauf hin, dass das Framework physikalisch korrekt ist.

LLMs sind darauf trainiert, kohärente Schlussfolgerungen innerhalb eines gegebenen Kontexts zu erzeugen. Die Konsistenz der Outputs reflektiert daher primär die strukturelle Qualität des Context-setting instruction schemas — nicht die Wahrheit der darin enthaltenen Annahmen.

### Vergleich mit Standardphysik-Outputs

In informellen Vergleichstests — ohne Frequenzgesetz-Kontext — erzeugten dieselben Systeme erwartungsgemäß Standardphysik-Beschreibungen. Die Beobachtung, dass mit dem Frequenzgesetz-Schema konsistente alternative Beschreibungen erzeugt werden, weist darauf hin, dass das Schema eine kohärente alternative Ontologie kodiert.

---

## 14.5 Limitations

Die folgenden Limitationen sind für die korrekte Einordnung der Ergebnisse wesentlich:

**Training Bias:** LLMs wurden auf Korpora trainiert, die Standardphysik stark überrepräsentieren. Konsistente Outputs unter einem alternativen Schema könnten das Ergebnis von Interpolation zwischen bekannten Konzepten sein — nicht von genuinem ontologischen Reasoning.

**Fehlende epistemische Unabhängigkeit:** LLMs haben keinen unabhängigen Zugang zur physikalischen Realität. Ihre Outputs reflektieren Muster in Trainingsdaten, nicht experimentelle Befunde.

**Keine Aussage über physikalische Realität:** KI-Konsistenzprüfung kann grundsätzlich keine Aussage über die physikalische Wahrheit eines Frameworks machen. Sie prüft strukturelle Kohärenz — nicht empirische Validität.

**Nicht-standardisierte Evaluation:** Die hier beschriebene Evaluation wurde manuell durchgeführt. Eine automatisierte, blind bewertete Replikationsstudie wäre für robuste Schlussfolgerungen notwendig.

**Prompt-Abhängigkeit:** Die Qualität der Outputs ist stark von der Formulierung des Context-setting schemas abhängig. Kleine Änderungen im Prompt können die Outputs signifikant verändern.

---

## 14.6 Das Metaprotokoll als Context-Setting Instruction Schema

Das Frequenzgesetz-Metaprotokoll (`FREQUENZGESETZ_METAPROTOKOLL_v7.md`) ist ein strukturiertes Context-setting instruction schema, das die Kernannahmen des Frequenzgesetzes in maschinenlesbarer Form bereitstellt.

```yaml
Kernprinzip:
  Frequenz (f):  primär — Beschreibung von Zustandsänderung
  Phase (ΔΦ):    erster abgeleiteter Zustand
  Zeit (T):      emergent       →  T = ΔΦ/f
  Masse (m):     gebunden       →  m = hf/c²
  Energie (E):   abgeleitet     →  E = hf
  Kausalrichtung: f → ΔΦ → T → m → E (strukturell gerichtet)
```

Das Metaprotokoll ist nicht als ontologische Wahrheit zu verstehen, sondern als formaler Instruktionsrahmen, der einem LLM ermöglicht, Reasoning innerhalb des Frequenzgesetz-Paradigmas konsistent durchzuführen.

---

## 14.7 Conclusion

Das beschriebene Konsistenzprüfungs-Experiment weist darauf hin, dass das Frequenzgesetz als strukturell kohärentes Context-setting instruction schema für LLM-basiertes Reasoning funktioniert. Vier verschiedene LLM-Systeme erzeugten unter dem gegebenen Rahmen intern konsistente und mit etablierter Physik kompatible Ausgaben.

Diese Beobachtung stützt die Hypothese innerer Konsistenz des Axiomensystems A0–A6 — sie stellt jedoch weder eine physikalische Verifikation dar, noch schließt sie alternative Erklärungen für die beobachteten Outputs aus.

Für eine robuste Einordnung des Frameworks sind die in Kapitel 13 beschriebenen experimentellen Tests notwendig — insbesondere der direkte Test der Phasenzeitauflösung und die Suche nach den vorhergesagten Resonanzmaxima.

> *Die Gleichungen bleiben dieselben.*
> *Die Leserichtung ändert sich.*

---

*→ Weiter: [Kapitel 15 — Bewusstsein als Frequenz-Operator](Kapitel_15.md)*
*← Zurück: [Kapitel 13 — Experimentelle Vorhersagen & Validierung](Kapitel_13.md)*
*Version 8.0 | Christian Berrang | DOI: 10.5281/zenodo.17874830*
