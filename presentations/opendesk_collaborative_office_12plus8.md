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
  /* Hide all footers */
  section::after { display: none !important; }
  footer { display: none !important; }
  [class*="footer"] { display: none !important; }
---

# OpenDesk
## Collaborative Office Cloud Suite

Tobias Weiss | DevOps Engineer, Uni Marburg

**Souveräne Zusammenarbeit mit offener Technologie – auf eigener Infrastruktur**

---

# Herausforderung

**Moderne Teamarbeit braucht:**
- Gemeinsame Dokumentenbearbeitung
- Echtzeit-Kollaboration
- Automatisierte Workflows
- Datensouveränität

**OpenDesk bietet all das – offen und self-hosted.**

---

# Prinzipien

**Agentic Engineering:**
1. **Autonomie** – Systeme handeln selbstständig
2. **Proaktivität** – Lösungen werden vorweggenommen
3. **Reaktivität** – Anpassung an neue Anforderungen
4. **Sozialität** – Zusammenarbeit im Fokus

**Kollaborative Office Suite trifft auf intelligente Agenten.**

---

# Architektur

```
┌─────────────────────────────┐
│        OpenDesk              │
├─────────────────────────────┤
│  Dokumente │ Team Orte      │
│  Workflows │ Agenten         │
└─────────────────────────────┘
          │
          ▼
┌─────────────────────────────┐
│        k3s Cluster           │
│  (Leichtes Kubernetes)       │
└─────────────────────────────┘
```

**Einfach. Offene Schnittstellen. Self-Hosted.**

---

# Use Case 1

**Team Dokumentation**

Problem: Veraltete Wikimedia, zentrale Pflege nötig

Lösung: Gemeinsame Bearbeitung mit Agenten-Unterstützung

Ergebnis: **Aktualität +40%, Pflegeaufwand -60%**

---

# Use Case 2

**Projektmanagement**

Problem: Manuelle Status-Updates, wiederkehrende Aufgaben

Lösung: Automatisierte Workflows mit Kollaborations-Agenten

Ergebnis: **Projektzeit -35%, Fehlerrate -70%**

---

# Use Case 3

**Wissensmanagement**

Problem: Verstreute Informationen, schwierige Suche

Lösung: Intelligente Verknüpfung und Kontext-Erkennung

Ergebnis: **Findbarkeit +80%, Wissensnutzung +25%**

---

# Praxisbeispiel

**Uni Marburg (Pilot):**

- 200 Nutzer:innen
- 5 Fachbereiche
- 3 Monate Einsatz
- 98% Verfügbarkeit

**Souveräne Zusammenarbeit – ohne Kompromisse.**

---

# Stack

**Backend:** Node.js + TypeScript + Fastify
**AI:** LangChain.js + Ollama (lokal)
**DB:** PostgreSQL + Qdrant
**Frontend:** Next.js 14
**Infrastruktur:** k3s (1GB RAM reicht)

**UNIX: Ein Werkzeug, eine Aufgabe, perfekt gelöst.**

---

# Installation

```bash
# k3s (1 Befehl)
curl -sfL https://get.k3s.io | sh -

# OpenDesk (1 Befehl)
kubectl apply -f opendesk.yaml
```

**5 Minuten. Eigenes Office. Fertig.**

---

# Mitmachen

**Open Source Wettbewerb 2026**

QR: ![w:200](https://api.qrserver.com/v1/create-qr-code/?size=200x200&data=https://open-source-wettbewerb.de/voting/opendesk/)

Link: [open-source-wettbewerb.de/voting/opendesk/](https://open-source-wettbewerb.de/voting/opendesk/)

**30 Sekunden. Offene Zukunft unterstützen.**

---

# Fragen
## +8 Minuten

---

# Backup: k3s Vorteile

- **Leicht:** Raspberry Pi bis Server
- **Einfach:** 1 Brought to you by the letter 'k'
- **Kostenlos:** €0 Infrastruktur
- **Robust:** Production-ready

---

# Backup: Roadmap

- Q4 2026: Public Beta
- Q1 2027: Plugin-System
- Q2 2027: Mobile Clients
- Q3 2027: Enterprise-Integration
