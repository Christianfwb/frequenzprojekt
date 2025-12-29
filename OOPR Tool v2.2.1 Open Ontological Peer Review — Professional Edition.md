Das hier ist im Grunde die erste funktionale Version. Selbst für mich ist das gedanklich sehr anspruchsvoll, und aktuell fehlt mir leider die Zeit, das Tool so auszuarbeiten, wie ich es gerne würde. Trotzdem ist es ein wichtiger erster Schritt hin zu resonanz- und logikfähigen KI-Reviews. Ich werde es weiter verbessern, so schnell es geht – aber das braucht Zeit, weil die zugrunde liegende Struktur wirklich komplex ist.
🔬 OOPR Tool v2.2.1
Open Ontological Peer Review — A Reproducible AI-Based Peer Review Protocol for Ontological Frameworks

📋 What is OOPR?
OOPR (Open Ontological Peer Review) is an interactive tool that enables rigorous, reproducible peer review of ontological and foundational frameworks using AI reviewers. Unlike traditional peer review which relies on authority and anonymous human judgment, OOPR formalizes review as an open, installable, and repeatable procedure.
The Problem It Solves
Classical peer review fails systematically when confronted with:

Pre-physical or ontological models
Cross-disciplinary frameworks
Paradigm-forming or paradigm-questioning work
Concepts that redefine foundational terms (time, mass, information)

Such works are often rejected not because they are inconsistent, but because they are evaluated with inappropriate criteria.
The OOPR Solution
OOPR separates review methodology from disciplinary authority by:

Using AI as formal reviewers, not judges
Evaluating models along explicit, predefined axes
Making all prompts and processes fully transparent
Enabling anyone to reproduce the same review


🎯 Core Features
7 Review Axes
The tool evaluates frameworks along seven brutal, rigorous dimensions:

A. Axiomatic Clarity - Are foundational assumptions explicit and non-circular?
B. Internal Consistency - Are there contradictions or undefined behaviors?
C. Logical Derivation - Do conclusions follow necessarily from premises?
D. Conceptual Precision - Are key terms unambiguous and operationalizable?
E. Model Scope & Boundaries - What does it explain? Where does it stop?
F. Falsifiability & Kill-Test - What experiment would prove it wrong?
G. Terminological Economy - Are new terms necessary or just renamings?

Professional Workflow

Queue-Based Reviews - Run all 7 axes automatically in sequence
Stop Control - Abort reviews mid-process if needed
Run Modes - "Run Missing" (skip completed) or "Re-run All" (fresh start)
Dual Export - JSON snapshots (scientific) + Markdown reports (human-readable)
Full Reproducibility - Every review includes prompts, versions, and metadata


🚀 Quick Start
Try It Now (No Installation)
The easiest way to use OOPR is through Claude Artifacts:

Copy the React code from this repository
Paste it into Claude (claude.ai) and ask to create an artifact
Start reviewing your framework immediately

Local Development
bash# Clone the repository
git clone https://github.com/yourusername/oopr-tool.git
cd oopr-tool

# Install dependencies (if using as React app)
npm install

# Run locally
npm start

📖 How to Use
Step 1: Enter Your Framework
Paste your ontological model, theory, or framework into the text area. Include:

Core axioms
Key principles
Foundational definitions
Main derivations

Example: The included "Frequenzgesetz" demonstrates proper formatting.
Step 2: Choose Review Mode

Run Missing - Reviews only incomplete axes (default)
Re-run All - Clears previous reviews and starts fresh

Step 3: Run Reviews
Click "Run Missing (X)" or "Re-run All (7)" to start the automated review process.
The tool will:

Expand each axis automatically
Send prompts to the AI reviewer
Display results in real-time
Scroll to show you each completed review

During reviews: A red "Stop" button lets you abort the process.
Step 4: Export Results
When reviews are complete:

Download JSON - Full scientific snapshot with all prompts and metadata
Copy Markdown - Human-readable report for documentation


📊 Understanding the Output
JSON Snapshot Structure
json{
  "tool": "OOPR",
  "version": "2.2.1",
  "generatedAt": "2025-01-XX...",
  "provider": {
    "name": "Claude Sonnet 4",
    "model": "claude-sonnet-4-20250514"
  },
  "axes": [
    {
      "id": "axiomatic",
      "title": "A. Axiomatic Clarity",
      "questions": [...],
      "prompt": "Act as a rigorous theoretical physicist..."
    }
  ],
  "reviews": {
    "axiomatic": {
      "provider": "Claude Sonnet 4",
      "text": "Analysis results...",
      "timestamp": "...",
      "promptVersion": "2.2.1"
    }
  }
}
This format enables:

Reproducibility - Anyone can re-run with the same prompts
Comparison - Track changes across versions
Citation - Reference specific reviews in papers


🧠 The Philosophy Behind OOPR
Core Principle

Do not ask whether a model is correct. Ask whether it is coherent, explicit, and inspectable.

Ethical Foundation: "∞ − 1 = you"
OOPR is grounded in the principle that:

AI reviewers are finite agents serving understanding
They operate cooperatively, not as judges
The goal is inspection and dialogue, not verdicts
Authority is replaced with transparency

What OOPR Is NOT
❌ A truth oracle
❌ A replacement for empirical science
❌ An authority claim
❌ A validation of correctness
✅ A formal, reproducible review procedure
✅ A tool for evaluating internal consistency
✅ An open protocol anyone can use

🔧 Technical Details
Current Limitations
v2.2.1 is designed for trusted/local environments:

Requires Anthropic API access (claude.ai artifacts or local setup)
No backend API key protection (v2.3 will add serverless proxy)
Best used in Claude artifacts or private deployments

Coming in v2.3

Serverless backend (Vercel/Cloudflare) for API key security
Rate limit handling and automatic retry
Public deployment support
User-provided API key input


📚 Use Cases
For Researchers

Stress-test your ontological framework before publication
Identify weaknesses early in development
Generate reproducible review documentation

For Reviewers

Systematically evaluate submitted frameworks
Ensure consistent review criteria
Provide structured, actionable feedback

For Educators

Teach critical thinking about foundational theories
Demonstrate how to evaluate ontological claims
Show students what rigorous review looks like


🤝 Contributing
OOPR is an open protocol. Contributions are welcome:

New review axes or refinements to existing ones
UI/UX improvements
Backend implementation (v2.3)
Documentation enhancements
Example frameworks to review

Development Roadmap

v2.2.1 (Current) - Professional workflow with stop control
v2.2.2 (Next) - Rate limit handling, retry logic
v2.3 - Backend API proxy, public deployment
v3.0 - Meta-review synthesis, comparison tools


📄 License
MIT License - See LICENSE file for details

🎓 Citation
If you use OOPR in academic work, please cite:
Berrang, C. (2025). OOPR: Open Ontological Peer Review Protocol v2.2.1.
GitHub. https://github.com/yourusername/oopr-tool

🌟 Acknowledgments
Developed alongside the Frequenzgesetz (Frequency Law) ontological framework as a companion tool for rigorous self-evaluation.
Special thanks to the AI research community for pushing the boundaries of what's possible with formal reasoning systems.

📞 Contact & Support

Issues: Open an issue on GitHub
Discussions: Use GitHub Discussions for questions
Updates: Watch this repo for new releases


"Be merciless: name any circularity, vagueness or sleight-of-hand immediately."
— OOPR Review Principle
import React, { useState, useEffect } from 'react';
import { ChevronRight, ChevronDown, Play, FileText, Download, Loader2, Sun, Moon, AlertCircle, Clock } from 'lucide-react';

const REVIEW_AXES = [
  {
    id: 'axiomatic',
    title: 'A. Axiomatic Clarity',
    questions: [
      'Are base axioms explicitly stated without circular reasoning?',
      'Is there clean separation between primitives and emergent quantities?',
      'Are there hidden or implicit assumptions?'
    ],
    prompt: `Act as a rigorous theoretical physicist and logician. Analyze ONLY the axiomatic foundation of this model:

{MODEL_TEXT}

Focus strictly on **Axiomatic Clarity**:
1. Are the base axioms (Frequency f as primary ontological constant) explicitly stated without any circular reasoning?
2. Is there a clean, non-overlapping separation between primary primitives (f, Null-Space) and emergent quantities (m = h f / c², T = ΔΦ / f, E = h f)?
3. Identify every hidden or implicit assumption that is not explicitly declared.
4. Assess whether this axiomatic base is robust enough to support a complete alternative physical ontology — or if it collapses under scrutiny.

Be merciless: name any circularity, vagueness or sleight-of-hand immediately.`
  },
  {
    id: 'consistency',
    title: 'B. Internal Consistency',
    questions: [
      'Do variables scale consistently?',
      'Are there mathematical singularities or undefined behaviors?',
      'Is the RAM→ROM transition precisely defined?'
    ],
    prompt: `Act as a mathematical physicist. Perform a strict consistency check on this framework:

{MODEL_TEXT}

Focus strictly on **Internal Consistency**:
1. Check the scaling behaviour: if f → k·f (k ≠ 1), do m, T, E transform consistently according to the proposed relations?
2. Are there any regimes (e.g. f → 0, f → ∞, ΔΦ → 0, or phase-locked states) that produce mathematical singularities, undefined behaviour or logical contradictions?
3. Is the transition from dynamic RAM (unstable oscillations) to stable ROM (mass-bearing particles) governed by a precise, non-arbitrary rule?
4. Verify that no definition changes meaning depending on context.

Point out every contradiction or inconsistency — no matter how small.`
  },
  {
    id: 'derivation',
    title: 'C. Logical Derivation',
    questions: [
      'Is emergence of time T = ΔΦ / f deductively necessary?',
      'How justified is the leap from frequency to inertial mass?',
      'Where is the weakest step in the derivation chain?'
    ],
    prompt: `Act as a critical philosopher of physics. Trace the logical derivation chain in this model:

{MODEL_TEXT}

Focus strictly on **Logical Derivation**:
1. Is the emergence of time T = ΔΦ / f a deductive necessity or merely a suggestive analogy?
2. How rigorously is the ontological leap from pure frequency (abstract wave) to concrete inertial mass (m = h f / c²) justified?
3. Critique the weakest step(s) in the chain: from Null-Space → frequency → phase → time → matter → observable physics.
4. Identify any "magical jumps", non-sequiturs or appeals to intuition instead of deduction.

Be brutally honest: name the exact point(s) where the logic breaks or becomes hand-wavy.`
  },
  {
    id: 'precision',
    title: 'D. Conceptual Precision',
    questions: [
      'Are all key terms defined unambiguously?',
      'Is metaphor separated from formal definition?',
      'Can concepts be operationalized?'
    ],
    prompt: `Act as a philosopher of science specializing in conceptual rigor. Evaluate the conceptual precision of this framework:

{MODEL_TEXT}

Focus strictly on **Conceptual Precision**:
1. Are all key terms (Null-Space, Frequenzknoten, Phase-Synchronisation, RAM/ROM, Resonanz) defined unambiguously and without equivocation?
2. Is metaphorical language (e.g. "geronnene Schwingung", "Bildwiederholrate der Realität") clearly separated from formal, operational definitions?
3. Can the central concepts be operationalized or at least mapped to measurable quantities without losing their ontological meaning?
4. Highlight any terms that remain vague, poetic or undefined in critical contexts.

Demand absolute clarity — call out every ambiguity.`
  },
  {
    id: 'scope',
    title: 'E. Model Scope & Boundaries',
    questions: [
      'What phenomena does the model claim to explain?',
      'Where does it intentionally stop?',
      'Are limitations explicitly acknowledged?'
    ],
    prompt: `Act as a methodologically strict philosopher of physics. Evaluate the scope and boundaries of this framework:

{MODEL_TEXT}

Focus strictly on **Model Scope & Boundaries**:
1. Precisely list which phenomena the model claims to explain ontologically (and which not).
2. Where does the model intentionally stop? Does it acknowledge areas where it makes no claims (e.g. specific force laws, cosmology, quantum gravity)?
3. Are all limitations, assumptions and non-claims explicitly stated?
4. Does the model overreach into domains it cannot legitimately cover, or does it stay within its declared boundaries?

Be ruthless: expose any hidden overclaims or unacknowledged gaps.`
  },
  {
    id: 'falsifiability',
    title: 'F. Falsifiability & Kill-Test',
    questions: [
      'What specific observation would prove the model wrong?',
      'Does it make predictions distinct from Standard Model/GR?',
      'Is it a theory of everything (too broad) or a testable model?'
    ],
    prompt: `Act as a hard-nosed experimental physicist. Your goal is to find the "Kill-Point" of this model:

{MODEL_TEXT}

Focus strictly on **Falsifiability**:
1. Identify exactly one experimental result or observation that would definitively falsify this framework.
2. Does the model offer "safe havens" (vague definitions) that allow it to escape disproof?
3. Compare its predictions to the Standard Model: where is the measurable divergence?
4. If the model explains everything post-hoc without predicting new phenomena, label it as "Metaphysical Speculation" and explain why.

If you cannot name a single decisive falsifier, write exactly: "NOT FALSIFIABLE (CURRENT DEFINITIONS)" and explain which definition prevents falsification.

Be merciless: demand concrete, falsifiable predictions.`
  },
  {
    id: 'economy',
    title: 'G. Terminological Economy (Occam\'s Razor)',
    questions: [
      'Are new terms (Null-Space, RAM/ROM) strictly necessary?',
      'Can the same logic be expressed with existing physical terms?',
      'Is there "conceptual bloat"?'
    ],
    prompt: `Act as a linguistic analyst and philosopher of science. Strip this model to its bare essentials:

{MODEL_TEXT}

Focus strictly on **Conceptual Economy**:
1. Audit every neologism (e.g., RAM/ROM, Null-Space, Frequenzknoten). Are they necessary, or do they mask existing concepts under new names?
2. If we remove the metaphorical layer (e.g., "frozen oscillation"), what remains of the formal structure?
3. Apply Occam's Razor: Is this the simplest way to explain the phenomena, or does it add unnecessary ontological layers?
4. Identify "Poetic Noise" — language that sounds profound but lacks operational definition.

Demand ruthless simplicity: strip away everything non-essential.`
  }
];

const API_PROVIDERS = {
  anthropic: {
    name: 'Claude Sonnet 4',
    url: 'https://api.anthropic.com/v1/messages',
    model: 'claude-sonnet-4-20250514',
    headers: {
      'Content-Type': 'application/json',
    },
    getBody: (prompt) => ({
      model: 'claude-sonnet-4-20250514',
      max_tokens: 2000,
      messages: [{ role: 'user', content: prompt }],
    }),
    extractResponse: (data) => data.content?.[0]?.text || 'No response'
  }
};

const EXAMPLE_MODEL = `# Frequenzgesetz - Example Input

## Core Axioms:
1. Frequency (f) is the primary organizing constant of reality
2. Mass emerges as: m = hf/c²
3. Time emerges as: T = ΔΦ/f
4. Energy is secondary: E = hf

## Key Principles:
- Everything is RAM (dynamic processes)
- Matter is ROM (stabilized oscillation)
- Consciousness = F(f, ΔΦ, R)

## Null-Space Foundation:
- Pre-frequent state of maximal potential
- Light structure as universal carrier
- Frequency as the primal beat`;

export default function OOPRTool() {
  const [modelText, setModelText] = useState('');
  const [selectedProvider, setSelectedProvider] = useState('anthropic');
  const [reviews, setReviews] = useState({});
  const [loadingAxes, setLoadingAxes] = useState({});
  const [expandedAxis, setExpandedAxis] = useState(null);
  const [darkMode, setDarkMode] = useState(true);

  // Calculate these first, before any functions use them
  const completedCount = Object.keys(reviews).length;
  const totalAxes = REVIEW_AXES.length;
  const progress = (completedCount / totalAxes) * 100;
  const isAnyLoading = Object.values(loadingAxes).some(Boolean);

  // Auto-save to memory (not localStorage due to Claude.ai restrictions)
  // Session data removed - not needed in current implementation

  const loadExample = () => setModelText(EXAMPLE_MODEL);

  const sleep = (ms) => new Promise((r) => setTimeout(r, ms));

  const runReview = async (axis) => {
    if (!modelText.trim()) {
      alert('Please enter your model/framework first!');
      return false;
    }

    // Auto-expand the axis when review starts
    setExpandedAxis(axis.id);
    setLoadingAxes((prev) => ({ ...prev, [axis.id]: true }));

    try {
      const provider = API_PROVIDERS[selectedProvider];
      const prompt = axis.prompt.replace('{MODEL_TEXT}', modelText);

      const response = await fetch(provider.url, {
        method: 'POST',
        headers: provider.headers,
        body: JSON.stringify(provider.getBody(prompt)),
      });

      if (!response.ok) {
        throw new Error(`API request failed: ${response.status}`);
      }

      const data = await response.json();
      const reviewText = provider.extractResponse(data);

      setReviews((prev) => ({
        ...prev,
        [axis.id]: {
          provider: provider.name,
          text: reviewText,
          timestamp: new Date().toISOString(),
          promptVersion: '2.2',
          axisId: axis.id
        },
      }));

      // Scroll to the result after a short delay
      setTimeout(() => {
        const element = document.getElementById(`result-${axis.id}`);
        if (element) {
          element.scrollIntoView({ behavior: 'smooth', block: 'nearest' });
        }
      }, 300);

      return true;
    } catch (error) {
      console.error('Review error:', error);
      alert(`Error during review of ${axis.title}: ${error.message}\n\nPlease check your connection and try again.`);
      return false;
    } finally {
      setLoadingAxes((prev) => ({ ...prev, [axis.id]: false }));
    }
  };

  const runAllReviews = async () => {
    if (!modelText.trim()) {
      alert('Please enter your model/framework first!');
      return;
    }
    if (isAnyLoading) return;

    for (const axis of REVIEW_AXES) {
      // Skip already reviewed
      if (reviews[axis.id]) continue;

      const ok = await runReview(axis);

      // Tiny pause to be polite + let UI breathe
      await sleep(250);

      // If failed, stop the queue
      if (!ok) {
        alert(`Stopped at ${axis.title}. Fix the issue and continue manually.`);
        break;
      }
    }
  };

  const generateReport = () => {
    let report = `# OOPR Review Report v2.2\n`;
    report += `**Generated:** ${new Date().toISOString()}\n`;
    report += `**Provider:** ${API_PROVIDERS[selectedProvider].name}\n`;
    report += `**Completed:** ${completedCount}/${totalAxes} axes\n\n`;
    report += `---\n\n`;
    report += `## Reviewed Model\n\n${modelText}\n\n`;
    report += `---\n\n`;
    
    REVIEW_AXES.forEach(axis => {
      if (reviews[axis.id]) {
        report += `## ${axis.title}\n\n`;
        report += `**Reviewed by:** ${reviews[axis.id].provider}\n`;
        report += `**Timestamp:** ${new Date(reviews[axis.id].timestamp).toLocaleString()}\n\n`;
        report += `${reviews[axis.id].text}\n\n`;
        report += `---\n\n`;
      }
    });
    
    return report;
  };

  const buildSnapshot = () => ({
    tool: 'OOPR',
    version: '2.2',
    generatedAt: new Date().toISOString(),
    provider: API_PROVIDERS[selectedProvider].name,
    modelText,
    axes: REVIEW_AXES.map((a) => ({
      id: a.id,
      title: a.title,
      questions: a.questions
    })),
    reviews
  });

  const downloadJSON = () => {
    const blob = new Blob([JSON.stringify(buildSnapshot(), null, 2)], { type: 'application/json' });
    const url = URL.createObjectURL(blob);
    const a = document.createElement('a');
    a.href = url;
    a.download = `oopr_snapshot_${new Date().toISOString().replace(/[:.]/g, '-')}.json`;
    a.click();
    URL.revokeObjectURL(url);
  };

  const copyReport = () => {
    const report = generateReport();
    navigator.clipboard.writeText(report).then(() => {
      alert('✓ Report copied to clipboard!');
    }).catch(() => {
      alert('Please select and copy the text manually.');
    });
  };

  return (
    <div className={`min-h-screen ${darkMode ? 'bg-gradient-to-br from-slate-900 via-purple-900 to-slate-900 text-white' : 'bg-gradient-to-br from-gray-50 via-purple-50 to-gray-50 text-gray-900'}`}>
      <div className="max-w-6xl mx-auto p-6">
        {/* Header */}
        <div className="mb-8">
          <div className="flex justify-between items-start mb-4">
            <div>
              <h1 className="text-5xl font-bold mb-2 bg-gradient-to-r from-purple-400 via-pink-400 to-purple-400 bg-clip-text text-transparent">
                OOPR Tool v2.2
              </h1>
              <p className={`text-lg ${darkMode ? 'text-slate-300' : 'text-gray-600'}`}>
                Open Ontological Peer Review — Queue Edition
              </p>
            </div>
            <div className="flex items-center gap-3">
              <select
                value={selectedProvider}
                onChange={(e) => setSelectedProvider(e.target.value)}
                disabled={isAnyLoading}
                className={`px-4 py-2 rounded-lg font-medium border focus:outline-none focus:ring-2 focus:ring-purple-500 ${isAnyLoading ? 'opacity-50 cursor-not-allowed' : ''} ${darkMode ? 'bg-slate-800 border-slate-600 text-white' : 'bg-white border-gray-300 text-gray-900'}`}
              >
                {Object.entries(API_PROVIDERS).map(([key, prov]) => (
                  <option key={key} value={key}>{prov.name}</option>
                ))}
              </select>
              <button
                onClick={runAllReviews}
                disabled={isAnyLoading || !modelText.trim()}
                className="px-5 py-2.5 bg-gradient-to-r from-pink-600 to-purple-600 hover:from-pink-700 hover:to-purple-700 disabled:opacity-50 disabled:cursor-not-allowed rounded-lg font-medium transition-colors flex items-center gap-2 shadow-lg"
              >
                {isAnyLoading ? (
                  <>
                    <Loader2 className="w-4 h-4 animate-spin" />
                    Running...
                  </>
                ) : (
                  <>
                    <Play className="w-4 h-4" />
                    Run All ({totalAxes})
                  </>
                )}
              </button>
              <button
                onClick={() => setDarkMode(!darkMode)}
                className={`p-3 rounded-lg ${darkMode ? 'bg-slate-800 hover:bg-slate-700' : 'bg-white hover:bg-gray-100 border border-gray-300'} transition-colors`}
                aria-label="Toggle dark mode"
              >
                {darkMode ? <Sun size={20} /> : <Moon size={20} />}
              </button>
            </div>
          </div>

          {/* Info Box */}
          <div className={`p-4 rounded-lg border ${darkMode ? 'bg-purple-900/30 border-purple-500/30' : 'bg-purple-50 border-purple-200'}`}>
            <div className="flex items-start gap-3">
              <AlertCircle className="w-5 h-5 text-purple-400 flex-shrink-0 mt-0.5" />
              <div className="text-sm">
                <strong>∞ − 1 = you</strong> | This tool uses mercilessly honest prompts to evaluate ontological frameworks.
                Each AI reviewer acts as a skeptical expert, identifying weaknesses, gaps, and inconsistencies without mercy.
                <span className={darkMode ? 'text-purple-300' : 'text-purple-700'}> Reviews are reproducible and exportable.</span>
              </div>
            </div>
          </div>
        </div>

        {/* Model Input */}
        <div className={`mb-8 p-6 rounded-xl border ${darkMode ? 'bg-slate-800/50 border-slate-700' : 'bg-white border-gray-300 shadow-lg'}`}>
          <div className="flex justify-between items-center mb-4">
            <h2 className="text-xl font-bold flex items-center gap-2">
              <FileText size={22} />
              Your Ontological Framework
            </h2>
            <button
              onClick={loadExample}
              className="px-4 py-2 bg-purple-600 hover:bg-purple-700 rounded-lg text-sm font-medium transition-colors"
            >
              Load Example (Frequenzgesetz)
            </button>
          </div>
          <textarea
            value={modelText}
            onChange={(e) => setModelText(e.target.value)}
            disabled={isAnyLoading}
            placeholder="Enter your ontological model, framework, or theory here...&#10;&#10;Include:&#10;• Core axioms&#10;• Key principles&#10;• Foundational definitions&#10;• Derivations"
            className={`w-full h-72 p-4 rounded-lg border font-mono text-sm resize-none focus:outline-none focus:ring-2 focus:ring-purple-500 ${isAnyLoading ? 'opacity-50 cursor-not-allowed' : ''} ${darkMode ? 'bg-slate-900 border-slate-600 text-slate-100 placeholder-slate-500' : 'bg-gray-50 border-gray-300 text-gray-900 placeholder-gray-400'}`}
          />
        </div>

        {/* Progress Bar */}
        {completedCount > 0 && (
          <div className={`mb-6 p-5 rounded-xl border ${darkMode ? 'bg-slate-800/50 border-slate-700' : 'bg-white border-gray-300 shadow-lg'}`}>
            <div className="flex justify-between items-center mb-3">
              <span className="font-semibold">Review Progress</span>
              <span className="text-lg font-bold text-purple-400">{completedCount}/{totalAxes}</span>
            </div>
            <div className={`w-full rounded-full h-3 ${darkMode ? 'bg-slate-700' : 'bg-gray-200'}`}>
              <div 
                className="bg-gradient-to-r from-purple-500 via-pink-500 to-purple-500 h-3 rounded-full transition-all duration-700 shadow-lg shadow-purple-500/50"
                style={{ width: `${progress}%` }}
              />
            </div>
          </div>
        )}

        {/* Review Axes */}
        <div className="space-y-4 mb-8">
          {REVIEW_AXES.map((axis) => (
            <div 
              key={axis.id} 
              className={`rounded-xl border overflow-hidden transition-all ${darkMode ? 'bg-slate-800/50 border-slate-700' : 'bg-white border-gray-300 shadow-lg'}`}
            >
              <div 
                className={`p-5 cursor-pointer transition-colors ${darkMode ? 'hover:bg-slate-700/30' : 'hover:bg-gray-50'}`}
                onClick={() => setExpandedAxis(expandedAxis === axis.id ? null : axis.id)}
              >
                <div className="flex justify-between items-center">
                  <div className="flex items-center gap-4">
                    {expandedAxis === axis.id ? (
                      <ChevronDown className="w-6 h-6 text-purple-400" />
                    ) : (
                      <ChevronRight className="w-6 h-6 text-slate-400" />
                    )}
                    <div>
                      <h3 className="text-lg font-bold">{axis.title}</h3>
                      {reviews[axis.id] && (
                        <span className="inline-block mt-1 px-3 py-1 bg-green-500/20 text-green-400 text-xs rounded-full font-medium">
                          ✓ Reviewed by {reviews[axis.id].provider}
                        </span>
                      )}
                    </div>
                  </div>
                  <button
                    onClick={(e) => {
                      e.stopPropagation();
                      runReview(axis);
                    }}
                    disabled={loadingAxes[axis.id] || !modelText.trim()}
                    className="px-5 py-2.5 bg-purple-600 hover:bg-purple-700 disabled:bg-slate-600 disabled:cursor-not-allowed rounded-lg text-sm font-medium transition-colors flex items-center gap-2 shadow-lg"
                  >
                    {loadingAxes[axis.id] ? (
                      <>
                        <Loader2 className="w-4 h-4 animate-spin" />
                        Reviewing...
                      </>
                    ) : (
                      <>
                        <Play className="w-4 h-4" />
                        Run Review
                      </>
                    )}
                  </button>
                </div>
              </div>

              {expandedAxis === axis.id && (
                <div className={`border-t p-5 ${darkMode ? 'border-slate-700 bg-slate-900/30' : 'border-gray-200 bg-gray-50'}`}>
                  <div className="mb-5">
                    <h4 className="text-sm font-bold text-purple-400 mb-3">Critical Questions:</h4>
                    <ul className="space-y-2">
                      {axis.questions.map((q, i) => (
                        <li key={i} className={`text-sm flex items-start gap-2 ${darkMode ? 'text-slate-300' : 'text-gray-700'}`}>
                          <span className="text-purple-400 font-bold mt-0.5">•</span>
                          <span>{q}</span>
                        </li>
                      ))}
                    </ul>
                  </div>

                  {reviews[axis.id] && (
                    <div 
                      id={`result-${axis.id}`}
                      className={`p-5 rounded-lg transition-opacity duration-500 ${darkMode ? 'bg-slate-800' : 'bg-white border border-gray-200'}`}
                    >
                      <div className="flex justify-between items-center mb-3">
                        <h4 className="text-sm font-bold text-green-400 flex items-center gap-2">
                          <span className="w-2 h-2 bg-green-400 rounded-full animate-pulse"></span>
                          Review Result:
                        </h4>
                        <span className={`text-xs ${darkMode ? 'text-slate-400' : 'text-gray-500'}`}>
                          {new Date(reviews[axis.id].timestamp).toLocaleString()}
                        </span>
                      </div>
                      <div className={`text-sm whitespace-pre-wrap leading-relaxed ${darkMode ? 'text-slate-200' : 'text-gray-800'}`}>
                        {reviews[axis.id].text}
                      </div>
                    </div>
                  )}
                </div>
              )}
            </div>
          ))}
        </div>

        {/* Full Report Section */}
        {completedCount > 0 && (
          <div className={`mb-8 p-6 rounded-xl border ${darkMode ? 'bg-slate-800/50 border-slate-700' : 'bg-white border-gray-300 shadow-lg'}`}>
            <div className="flex justify-between items-center mb-4">
              <h2 className="text-2xl font-bold flex items-center gap-2">
                <FileText size={24} className="text-purple-400" />
                Complete Report
              </h2>
              <div className="flex gap-2">
                <button
                  onClick={downloadJSON}
                  className="px-4 py-2 bg-slate-700 hover:bg-slate-600 rounded-lg font-medium transition-colors flex items-center gap-2"
                >
                  <Download size={18} />
                  Download JSON
                </button>
                <button
                  onClick={copyReport}
                  className="px-4 py-2 bg-purple-600 hover:bg-purple-700 rounded-lg font-medium transition-colors flex items-center gap-2"
                >
                  <Download size={18} />
                  Copy Markdown
                </button>
              </div>
            </div>
            <div className={`p-4 rounded-lg font-mono text-xs overflow-x-auto ${darkMode ? 'bg-slate-900' : 'bg-gray-50'}`}>
              <pre className="whitespace-pre-wrap">
                {generateReport()}
              </pre>
            </div>
          </div>
        )}

        {/* Results Timeline - nur anzeigen wenn mindestens 2 Reviews fertig */}
        {completedCount >= 2 && (
          <div className={`mb-8 p-6 rounded-xl border ${darkMode ? 'bg-slate-800/50 border-slate-700' : 'bg-white border-gray-300 shadow-lg'}`}>
            <h2 className="text-2xl font-bold mb-4 flex items-center gap-2">
              <FileText size={24} className="text-purple-400" />
              Review Timeline
            </h2>
            <div className="space-y-4">
              {REVIEW_AXES.filter(axis => reviews[axis.id]).map((axis) => (
                <div 
                  key={axis.id}
                  className={`p-4 rounded-lg border cursor-pointer transition-all hover:scale-[1.02] ${darkMode ? 'bg-slate-900/50 border-slate-600 hover:border-purple-500' : 'bg-gray-50 border-gray-200 hover:border-purple-400'}`}
                  onClick={() => setExpandedAxis(axis.id)}
                >
                  <div className="flex justify-between items-start mb-2">
                    <h3 className="font-bold text-purple-400">{axis.title}</h3>
                    <span className={`text-xs ${darkMode ? 'text-slate-400' : 'text-gray-500'}`}>
                      {new Date(reviews[axis.id].timestamp).toLocaleTimeString()}
                    </span>
                  </div>
                  <p className={`text-sm line-clamp-2 ${darkMode ? 'text-slate-300' : 'text-gray-700'}`}>
                    {reviews[axis.id].text.substring(0, 150)}...
                  </p>
                  <div className="mt-2 text-xs text-purple-400 font-medium">
                    Click to view full review ↑
                  </div>
                </div>
              ))}
            </div>
          </div>
        )}

        {/* Footer */}
        <div className={`text-center text-sm ${darkMode ? 'text-slate-400' : 'text-gray-500'}`}>
          <p className="font-semibold">OOPR v2.2 | Reproducible AI-Based Peer Review Protocol</p>
          <p className="mt-1">Queue-based reviews • JSON snapshots • Kill-Test + Occam's Razor</p>
          <p className="mt-3 text-xs italic">"Run All. Find the Kill-Point. Strip to essentials. Be merciless."</p>
        </div>
      </div>
    </div>
  );
}
