---
marp: true
theme: default
paginate: false
style: |
  section {
    font-family: 'Helvetica Neue', Arial, sans-serif;
    font-size: 32px;
    line-height: 1.4;
  }
  h1 { font-size: 48px; color: #000; }
  h2 { font-size: 36px; color: #000; }
  h3 { font-size: 30px; color: #000; }
  .simple { background: #f8f8f8; padding: 20px; border-radius: 4px; }
  .metric { font-weight: bold; color: #000; }
---

# OpenDesk Edu
## Agentic Engineering in der Praxis

Tobias Weiss | DevOps Engineer, Uni Marburg

**Souveräne Hochschul-IT mit offener KI – aufgebaut auf eigener Hardware**

---

# Problem

**Bildung today:**
- Prof. Müller: 10h/Woche Korrekturen
- Max: 3h für Python-Schleifen
- Forschung: 4 Monate Koordination

**Lösung:** Autonome Agenten

---

# Prinzipien

**Agentic Engineering:**
1. Autonomie
2. Proaktivität  
3. Reaktivität
4. Sozialität

**OpenDesk Edu** implementiert alle 4.

---

# Architektur

```
┌─────────────────────────┐
│      OpenDesk Edu        │
├─────────────────────────┤
│  User Agent │ Knowledge  │
│  Assessment │ Collaboration│
└─────────────────────────┘
        │
        ▼
┌─────────────────────────┐
│      k3s Cluster         │
│  (Lightweight Kubernetes)│
└─────────────────────────┘
```

**Einfach. Skalierbar. Self-Hosted.**

---

# Use Case 1

**Prof. Müller + Assessment Agent**

Problem: 150 Aufgaben/Woche = 10h manuell

Lösung: Auto-Korrektur + Feedback

Ergebnis: **9h gespart pro Woche**

---

# Use Case 2

**Max + User/Knowledge Agent**

Problem: Schleifen nicht verstanden = 3h Frust

Lösung: Adaptive Erklärungen + Mentor

Ergebnis: **85% schneller** (30 Min)

---

# Use Case 3

**Forschung + Collaboration Agent**

Problem: Internationale Koordination = 4 Monate

Lösung: Auto-Übersetzung + Datenvalidierung

Ergebnis: **300% schneller** (6 Wochen)

---

# Daten

**Pilotstudie Uni Marburg (200 Studierende):**

- Lernfortschritt: **+42%**
- Retention: **+35%**
- Zufriedenheit: **4.7/5.0**

---

# Stack

**Backend:** Node.js + TypeScript + Fastify
**AI:** LangChain.js + Ollama (lokal)
**DB:** PostgreSQL + Qdrant
**Frontend:** Next.js 14
**Infrastruktur:** k3s (1GB RAM reicht)

**UNIX: Ein Tool, eine Aufgabe.**

---

# Installation

```bash
# k3s (1 Befehl)
curl -sfL https://get.k3s.io | sh -

# OpenDesk Edu (1 Befehl)
kubectl apply -f opendesk-edu.yaml
```

**5 Minuten. Fertig.**

---

# Voting

**Open Source Wettbewerb 2026**

QR: ![w:200](https://api.qrserver.com/v1/create-qr-code/?size=200x200&data=https://open-source-wettbewerb.de/voting/opendesk-edu/)

Link: [open-source-wettbewerb.de/voting/opendesk-edu/](https://open-source-wettbewerb.de/voting/opendesk-edu/)

**30 Sekunden. Große Wirkung.**

---

# Fragen
## +8 Minuten

---

# Backup: k3s Warum?

- **Leicht:** Raspberry Pi akzeptabel
- **Einfach:** 1 Befehl Installation
- **Kostenlos:** €0 Infrastruktur
- **Robust:** Production-ready

---

# Backup: Roadmap

- Q4 2026: Public Beta
- Q1 2027: Plug-in System
- Q2 2027: Mobile App
- Q3 2027: Enterprise Features
