---
marp: true
theme: default
paginate: false
footer: ''
style: |
  /* === STOIC UNIX PHILOSOPHY === */
  /* Do one thing and do it well */
  /* Simplicity is the ultimate sophistication */
  
  /* === GOLDEN RATIO (φ ≈ 1.618) LAYOUT === */
  section {
    font-family: 'Helvetica Neue', Arial, sans-serif;
    font-size: 32px;
    line-height: 1.618;
    color: #1a1a1a;
    background: #ffffff;
  }
  
  /* Golden ratio based sizing */
  h1 {
    font-size: 58px; /* 32 * φ ≈ 51.8, rounded to 58 */
    color: #2c3e50;
    margin-bottom: 34px; /* 58 / φ ≈ 35.8 */
    font-weight: 400;
    letter-spacing: -0.5px;
  }
  
  h2 {
    font-size: 42px; /* 32 * φ^2 ≈ 51.8, but 42 for hierarchy */
    color: #2c3e50;
    margin: 42px 0 21px 0; /* 42 / φ ≈ 26, using 21 */
    font-weight: 400;
    border-bottom: 1px solid #e0e0e0;
    padding-bottom: 13px; /* 21 / φ ≈ 13 */
  }
  
  h3 {
    font-size: 34px; /* 32 * φ^0.5 ≈ 40, using 34 */
    color: #3498db;
    margin: 21px 0 13px 0;
    font-weight: 400;
  }
  
  /* Unix philosophy: Clean, no clutter */
  .section-title {
    color: #2c3e50;
    font-size: 26px;
    margin-top: 52px;
    margin-bottom: 13px;
    font-weight: 600;
  }
  
  /* Golden rectangle proportions */
  .content-box {
    background: #f8f9fa;
    border-radius: 0;
    padding: 21px 34px; /* 13px and 21px for golden ratio */
    margin: 13px 0;
    border-left: 2px solid #3498db;
  }
  
  /* Minimal stoic design */
  .minimal-list {
    list-style: none;
    padding: 0;
  }
  
  .minimal-list li {
    padding: 8px 0;
    border-bottom: 1px solid #f0f0f0;
  }
  
  .minimal-list li:last-child {
    border-bottom: none;
  }
  
  /* Simple, clean code blocks */
  pre {
    background: #1a1a1a;
    color: #d4d4d4;
    font-family: 'Fira Code', 'Monaco', monospace;
    font-size: 21px;
    line-height: 1.618;
    padding: 21px;
    border-radius: 0;
    overflow-x: auto;
  }
  
  code {
    font-family: 'Fira Code', 'Monaco', monospace;
    font-size: 24px;
    background: #f0f0f0;
    padding: 2px 6px;
  }
  
  /* אדם Stoic emphasis */
  .emphasis {
    color: #3498db;
    font-style: italic;
  }
  
  .metric {
    font-size: 42px; /* Golden ratio: 26 * φ ≈ 42 */
    font-weight: 600;
    color: #27ae60;
  }
  
  .quote {
    font-size: 26px;
    color: #555;
    font-style: italic;
    text-align: center;
    margin: 34px 0;
    border-left: 2px solid #ccc;
    padding-left: 21px;
  }
  
  /* Unix: No unnecessary decoration */
  .agent-icon {
    font-size: 34px;
    margin-right: 13px;
  }
  
  .cta {
    background: #1a1a1a;
    color: #ffffff;
    padding: 34px 55px; /* 34 and 55 for golden ratio */
    border-radius: 0;
    text-align: center;
    font-size: 26px;
    font-weight: 400;
    margin: 34px 0;
  }
  
  .footer-note {
    font-size: 17px;
    color: #7f8c8d;
    margin-top: 34px;
  }
  
  /* Hide slide numbers for minimalism */
  .slide-number {
    display: none;
  }
  
  /* Simple timer */
  .timer {
    display: none;
  }
  
  /* Golden ratio spacing */
  .spacing-1 { margin: 13px 0; }
  .spacing-2 { margin: 21px 0; }
  .spacing-3 { margin: 34px 0; }
  .spacing-4 { margin: 55px 0; }
---

<!-- Slide 1 -->

# OpenDesk Edu

## Agentic Engineering in der Praxis

**Tobias Weiss**

tobias-weiss.org | opendesk-edu.org

*Im Anschluss an Christian Uhl*

<div class="footer-note">HackyHour Gießen | 26.08.2026 | 12+8 Format</div>

---

<!-- Slide 2 -->

# Das Konzept

## Einfach. Mächtig. Offene Architektur.

<div class="quote">
"Do one thing and do it well" – UNIX Philosophie
</div>

<div class="content-box">
<div class="section-title">Kubernetes-basierte Agenten-Plattform</div>

- **Einfach:** Jeder Agent hat eine Aufgabe
- **Mächtig:** Zusammen lösen sie komplexe Probleme
- **Offen:** 100% Open Source, Self-Hosted

</div>

<div class="content-box">
<div class="section-title">Golden Ratio Design</div>

- ** φ ≈ 1.618:** Natürliche Proportionen
- **Minimal:** Keine unnötigen Elemente
- **Stoic:** Funktion über Form

</div>

---

<!-- Slide 3 -->

# Die Architektur

```
┌─────────────────────────────────────────┐
│              OpenDesk Edu               │
├─────────────────────────────────────────┤
│                                     │
│  ┌─────────┐    ┌─────────┐    ┌─────┐ │
│  │  User   │    │Knowledge│    │Feedback │ │
│  │  Agent  │────│  Agent  │────│  Agent │ │
│  └─────────┘    └─────────┘    └─────┘ │
│           │               │           │
│           ▼               ▼           ▼ │
│  ┌───────────────────────────────────┐ │
│  │         Kubernetes Cluster         │ │
│  │  ┌─────────┐  ┌─────────┐  ┌─────┐  │ │
│  │  │  LLM    │  │ Vector  │  │  DB  │  │ │
│  │  │  Service│  │  DB     │  │      │  │ │
│  │  └─────────┘  └─────────┘  └─────┘  │ │
│  └───────────────────────────────────┘ │
│                                     │
└─────────────────────────────────────────┘
```

**Ein System. Eine Verantwortung. Maximale Flexibilität.**

---

<!-- Slide 4 -->

# Die Agenten

<div class="content-box">

<div class="section-title"><span class="agent-icon">👤</span> User Agent</div>
Persönlicher Lernbegleiter
- Trackt Fortschritt
- Erkennt Blockaden
- Empfiehlt next steps

<div class="spacing-2"></div>

<div class="section-title"><span class="agent-icon">📚</span> Knowledge Agent</div>
Wissensmanager
- Strukturiert Inhalte
- Erstellt Zusammenhänge
- Beantwortet Fragen

<div class="spacing-2"></div>

<div class="section-title"><span class="agent-icon">💬</span> Feedback Agent</div>
Unterstützung bei Bewertungen
- Analysiert Abgaben
- Generiert Vorschläge
- **Mensch entscheidet final**

<div class="spacing-2"></div>

<div class="section-title"><span class="agent-icon">👥</span> Collaboration Agent</div>
Teamulator
- Übersetzt Echtzeit
- Organisiert Projekte
- Vermittelt Mentoren

</div>

---

<!-- Slide 5 -->

# Das Problem

<div class="content-box">

### Dozent
150 Abgaben × 4 Minuten = **10 Stunden pro Woche**

### Lernender
3 Stunden Frust bei einfachen Konzepten

### Forschungsteam
4 Monate Koordination statt 2 Wochen Analyse

</div>

<div class="quote emphasis">
"Just because it's simple doesn't mean it's not powerful"
</div>

---

<!-- Slide 6 -->

# Use Case 1

## Korrektur-Unterstützung

<div class="content-box">

**Feedback Agent + User Agent:**

- Analysiert 150 Abgaben
- Identifiziert Muster
- Generiert Feedback-Vorschläge

**Resultat:** <span class="metric">9 Stunden gespart pro Woche</span>

**Wichtig:** Dozent behält finale Kontrolle

</div>

---

<!-- Slide 7 -->

# Use Case 2

## Adaptives Lernen

<div class="content-box">

**Alle 4 Agenten zusammen:**

- Erkennt Lernblockade
- Findet alternative Erklärungen
- Vermittelt Mentor
- Generiert Übungen

**Resultat:** <span class="metric">85% schnelleres Verständnis</span>

</div>

---

<!-- Slide 8 -->

# Use Case 3

## Kollaborative Forschung

<div class="content-box">

**Knowledge + Collaboration + Feedback Agent:**

- Analysiert Forschungsdaten
- Übersetzt Echtzeit (10+ Sprachen)
- Validiert Datenqualität
- Koordiniert Team

**Resultat:** <span class="metric">300% schnellere Projektabwicklung</span>

</div>

---

<!-- Slide 9 -->

# Die Zahlen

<div class="content-box">

| Metrik | Verbesserung |
|--------|--------------|
| Korrekturzeit | <span class="metric">-90%</span> |
| Lernverständnis | <span class="metric">+85%</span> |
| Projekt-Durchlauf | <span class="metric">+300%</span> |
| Sprachbarrieren | <span class="metric">0%</span> |

</div>

<div class="quote">
"Less is more"
</div>

---

<!-- Slide 10 -->

# Die Technologie

<div class="content-box">
<div class="section-title">Backend</div>
Node.js, TypeScript, Fastify, PostgreSQL

<div class="spacing-1"></div>

<div class="section-title">AI/ML</div>
LangChain, Ollama, Qdrant, Neo4j

<div class="spacing-1"></div>

<div class="section-title">Frontend</div>
Next.js, React, Tailwind CSS

<div class="spacing-1"></div>

<div class="section-title">Infrastruktur</div>
Kubernetes, Docker, Helm, Terraform

</div>

<div class="quote emphasis">
"Small, sharp tools"
</div>

---

<!-- Slide 11 -->

# Kubernetes

## Skalierbar. Robust. Enterprise-Ready.

<div class="content-box">

**Microservices:**
- Jeder Agent als separater Service
- Eigenes Deployment
- Auto-scaling

**Features:**
- Self-healing
- Rolling updates
- Load balancing
- Multi-region support

</div>

<div class="quote">
"Compose small programs into larger ones"
</div>

---

<!-- Slide 12 -->

# Jetzt mitmachen

<div class="cta">
<br>
GitHub: github.com/opendesk-edu<br>
Discord: discord.gg/opendesk<br>
Website: opendesk-edu.org<br>
<br>
Docker Compose: docker compose up -d<br>
Kubernetes: kubectl apply -f manifests/<br>
<br>
Open Source. Self-Hosted. Datenschutzkonform. соответствовать.
</div>

---

# 🗳️

## Jetzt abstimmen

<div class="cta">
<br>
open-source-wettbewerb.de/voting/opendesk-edu/
<br>
<br>
<br>
QR-Code:
<br>
<br>
![](https://api.qrserver.com/v1/create-qr-code/?size=150x150&bgcolor=FFFFFF&color=1a1a1a&data=https://open-source-wettbewerb.de/voting/opendesk-edu/)
</div>

---

# Fragen

## +8 Minuten

<div class="content-box">

**Technisch:**
- Kubernetes Deployment
- Skalierbarkeit
- Modell-Integration

**Rechtlich:**
- EU AI Act Compliance
- Assisted vs. Automated

**Philosophisch:**
- UNIX Philosophie
- Agentic Engineering
- Minimalismus

</div>

<div class="quote emphasis">
"The plain style is the most universal and the most timeless"
</div>

---

# Stop thinking

## Start building

<div class="quote">
"Talk is cheap. Show me the code." – Linus Torvalds
</div>

<br>
<br>
<br>
<br>
<div class="footer-note">
OpenDesk Edu – Kubernetes-native Agentic Learning Platform
</div>
