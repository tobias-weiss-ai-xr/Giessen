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

  h1 {
    font-size: 58px;
    color: #2c3e50;
    margin-bottom: 34px;
    font-weight: 400;
    letter-spacing: -0.5px;
  }

  h2 {
    font-size: 42px;
    color: #2c3e50;
    margin: 42px 0 21px 0;
    font-weight: 400;
    border-bottom: 1px solid #e0e0e0;
    padding-bottom: 13px;
  }

  h3 {
    font-size: 34px;
    color: #3498db;
    margin: 21px 0 13px 0;
    font-weight: 400;
  }

  .section-title {
    color: #2c3e50;
    font-size: 26px;
    margin-top: 52px;
    margin-bottom: 13px;
    font-weight: 600;
  }

  .content-box {
    background: #f8f9fa;
    border-radius: 0;
    padding: 21px 34px;
    margin: 13px 0;
    border-left: 2px solid #3498db;
  }

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

  .emphasis {
    color: #3498db;
    font-style: italic;
  }

  .metric {
    font-size: 42px;
    font-weight: 600;
    color: #27ae60;
  }

  .potential {
    font-size: 28px;
    font-weight: 400;
    color: #7f8c8d;
    font-style: italic;
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

  .agent-icon {
    font-size: 34px;
    margin-right: 13px;
  }

  .cta {
    background: #1a1a1a;
    color: #ffffff;
    padding: 34px 55px;
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
    text-align: center;
  }

  .slide-number { display: none; }
  .timer { display: none; }

  img {
    max-height: 450px;
    display: block;
    margin: 0 auto;
  }
---

<!-- Slide 1 - 0:00-0:30 -->

# OpenDesk Edu

## Agentic Engineering in der Praxis

**Tobias Weiss**

tobias-weiss.org | opendesk-edu.org

*Im Anschluss an Christian Uhl – "Agentic AI in der Praxis"*

<div class="footer-note">HackyHour Gießen · 26.08.2026 · 12+8 Format</div>

---

<!-- Slide 2 - 0:30-1:30 -->

# Das Konzept

## Einfach. Mächtig. Offen.

<div class="content-box">

**Kubernetes-basierte Agenten-Plattform für Bildung**

- **Einfach:** Jeder Agent hat eine Aufgabe – UNIX-Prinzip
- **Mächtig:** Zusammen lösen sie komplexe Probleme
- **Offen:** 100% Open Source, Self-Hosted, DSGVO-konform

</div>

<div class="quote">
"Do one thing and do it well."
</div>

---

<!-- Slide 3 - 1:30-2:30 -->

# Die Architektur

![w:900 h:450 Architektur](diagrams/architektur.svg)

**Ein System. Vier Agenten. Maximale Flexibilität.**

---

<!-- Slide 4 - 2:30-3:00 -->

# Kubernetes-Infrastruktur

![w:900 h:450 Kubernetes](diagrams/kubernetes.svg)

**Skalierbar. Robust. Self-Hosted.**

---

<!-- Slide 5 - 3:00-4:00 -->

# Die vier Agenten

![w:900 h:300 Agenten](diagrams/agenten.svg)

<div class="content-box">

**Jeder Agent – eine klare Aufgabe:**

- **User Agent:** Fortschritt tracken, Blockaden erkennen, next steps empfehlen
- **Knowledge Agent:** Inhalte strukturieren, Zusammenhänge herstellen, Fragen beantworten
- **Feedback Agent:** Abgaben analysieren, Vorschläge generieren – **Mensch entscheidet final**
- **Collaboration Agent:** Echtzeit-Übersetzung, Projekte organisieren, Mentoren vermitteln

</div>

---

<!-- Slide 6 - 4:00-4:30 -->

# Das Problem

<div class="content-box">

### Dozent
150 Abgaben × 4 Minuten = **10 Stunden pro Woche** manueller Aufwand

### Lernender
3 Stunden Frust bei Konzepten, die in 30 Minuten verständlich sein könnten

### Forschungsteam
4 Monate Koordination statt 2 Wochen Analyse bei internationalen Teams

</div>

<div class="quote emphasis">
Das muss nicht sein.
</div>

---

<!-- Slide 7 - 4:30-6:00 -->

# Use Case 1: Korrektur-Unterstützung

![w:900 h:400 Use Case 1](diagrams/usecase1.svg)

<div class="content-box">

**Ablauf:** Feedback Agent analysiert Abgaben → erkennt Muster → generiert Vorschläge → **Dozent behält finale Kontrolle**

**Potenzial:** Deutliche Zeitersparnis bei der Korrektur – **der Mensch entscheidet immer final.**

</div>

---

<!-- Slide 8 - 6:00-7:30 -->

# Use Case 2: Adaptives Lernen

![w:900 h:400 Use Case 2](diagrams/usecase2.svg)

<div class="content-box">

**Ablauf:** User Agent erkennt Blockade → Knowledge Agent findet alternative Erklärungen → Collaboration Agent vermittelt Mentor → Feedback Agent generiert Übungen

**Potenzial:** Deutlich schnelleres Verständnis durch personalisierte Lernpfade.

</div>

---

<!-- Slide 9 - 7:30-8:30 -->

# Use Case 3: Kollaborative Forschung

![w:900 h:400 Use Case 3](diagrams/usecase3.svg)

<div class="content-box">

**Ablauf:** Knowledge Agent strukturiert Daten → Collaboration Agent übersetzt in Echtzeit → Feedback Agent validiert Qualität

**Potenzial:** Massiv beschleunigte Projektabwicklung – internationale Teams ohne Barrieren.

</div>

---

<!-- Slide 10 - 8:30-9:00 -->

# Technologie-Stack

![w:900 h:450 Tech Stack](diagrams/techstack.svg)

**Small, sharp tools. UNIX-Prinzip.**

---

<!-- Slide 11 - 9:00-10:00 -->

# Kubernetes: Skalierbar & Robust

<div class="content-box">

**Microservices-Architektur:**
- Jeder Agent als separater Service – unabhängig skalierbar
- Auto-Scaling basierend auf Last
- Self-Healing (automatischer Neustart bei Fehlern)
- Rolling Updates ohne Downtime
- Load Balancing über alle Worker Nodes

</div>

<div class="content-box">

**Enterprise-Ready:**
- Helm Charts für Deployment
- Terraform für Infrastructure as Code
- Von 10 bis 10.000 Nutzern skalierbar
- Volle Datenkontrolle durch Self-Hosting

</div>

---

<!-- Slide 12 - 10:00-11:00 -->

# Mitmachen

<div class="cta">

**Schnellstart (5 Minuten):**

`docker compose up -d`

**Oder mit Kubernetes:**

`kubectl apply -f manifests/`

**Ressourcen:**
GitHub: github.com/opendesk-edu
Website: opendesk-edu.org

**Open Source · Self-Hosted · DSGVO-konform**

</div>

---

<!-- Slide 13 - 11:00-12:00 -->

# 🗳️ Jetzt abstimmen

## Open Source Wettbewerb 2026

<div class="cta">

**Jede Stimme zählt.**

[open-source-wettbewerb.de/voting/opendesk-edu](https://open-source-wettbewerb.de/voting/opendesk-edu/)

</div>

![w:200 h:200 QR-Code](https://api.qrserver.com/v1/create-qr-code/?size=200x200&bgcolor=FFFFFF&color=1a1a1a&data=https://open-source-wettbewerb.de/voting/opendesk-edu/)

<div class="footer-note">30 Sekunden Ihrer Zeit – ein großer Unterschied.</div>

---

<!-- Q&A Slide -->

# Fragen & Diskussion

## +8 Minuten

<div class="content-box">

**Technisch:** Kubernetes, Skalierbarkeit, Modell-Integration, API

**Rechtlich:** EU AI Act, DSGVO, assisted vs. automated

**Philosophisch:** UNIX-Prinzip, Agentic Engineering, Minimalismus

**Praktisch:** Installation, Community, Roadmap

</div>

<div class="quote emphasis">
Vielen Dank für Ihre Aufmerksamkeit.
</div>
