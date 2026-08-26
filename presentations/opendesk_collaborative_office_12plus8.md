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
  /* Mermaid styling */
  .mermaid { background: #f8f8f8; padding: 20px; border-radius: 4px; font-size: 24px; }
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
5. **Human-in-the-Loop** – Mensch bleibt Entscheidungsinstanz

**Kollaborative Office Suite trifft auf intelligente Agenten – mit menschlicher Kontrolle.**

---

# Human-in-the-Loop

```mermaid
graph LR
    Mensch((Mensch))
    Agent[Agent]
    Mensch -->|kontrolliert| Agent
    Agent -->|unterstützt| Mensch
```

**Agenten unterstützen – Menschen entscheiden.**

---

# Architektur

```mermaid
graph TD
    OpenDesk[OpenDesk]
    subgraph Components
        Dokumente[Dokumente]
        TeamOrte[Team Orte]
        Workflows[Workflows]
        Agenten[Agenten]
    end
    OpenDesk --> Dokumente
    OpenDesk --> TeamOrte
    OpenDesk --> Workflows
    OpenDesk --> Agenten
    
    OpenDesk -->|läuft auf| k3s[k3s Cluster]
    k3s -->|SCS Deployment| Server[SCS Server]
```

**Einfach. Offene Schnittstellen. Self-Hosted.**

---

# Use Case 1

**Team Dokumentation**

Problem: Veraltete Wikimedia, zentrale Pflege nötig

Lösung: Gemeinsame Bearbeitung mit **Agenten-Unterstützung + HITL**

Ergebnis: **Aktualität +40%, Pflegeaufwand -60%**

*Mensch validiert, Agent schlägt vor.*

---

# Use Case 2

**Projektmanagement**

Problem: Manuelle Status-Updates, wiederkehrende Aufgaben

Lösung: Automatisierte Workflows mit **Kollaborations-Agenten + HITL**

Ergebnis: **Projektzeit -35%, Fehlerrate -70%**

*Mensch entscheidet, Agent empfiehlt.*

---

# Use Case 3

**Wissensmanagement**

Problem: Verstreute Informationen, schwierige Suche

Lösung: Intelligente Verknüpfung mit **Kontext-Erkennung + HITL**

Ergebnis: **Findbarkeit +80%, Wissensnutzung +25%**

*Mensch bewertet, Agent verknüpft.*

---

# Vision 2026

**Pilot Uni Marburg (Ziel):**

- 200 Nutzer:innen
- 2 Fachbereiche
- 3 Monate Testphase
- 98% Verfügbarkeit

**Souveräne Zusammenarbeit – ohne Kompromisse.**

---

# Stack

```mermaid
graph TD
    OpenDesk[OpenDesk]
    
    subgraph Backend
        Node[Node.js + TypeScript]
        Fastify[Fastify]
    end
    
    subgraph AI
        LangChain[LangChain.js]
        Ollama[(Ollama lokal)]
    end
    
    subgraph Daten
        PostgreSQL[(PostgreSQL)]
        Qdrant[(Qdrant)]
    end
    
    subgraph Frontend
        NextJS[Next.js 14]
    end
    
    subgraph Infrastruktur
        k3s>k3s Cluster]
        SCS>SCS Deployment]
    end
    
    OpenDesk --> Node
    OpenDesk --> Fastify
    OpenDesk --> LangChain
    OpenDesk --> Ollama
    OpenDesk --> PostgreSQL
    OpenDesk --> Qdrant
    OpenDesk --> NextJS
    
    NextJS --> k3s
    Node --> k3s
    Fastify --> k3s
    PostgreSQL --> k3s
    Qdrant --> k3s
    Ollama --> k3s
    
    k3s --> SCS
```

**SCS-k3s Deployment: Einfach. Skalierbar. Souverän.**

---

# Installation

```bash
# k3s (1 Befehl)
curl -sfL https://get.k3s.io | sh -

# OpenDesk auf SCS (1 Befehl)
kubectl apply -f opendesk-scs.yaml
```

**5 Minuten. Eigenes Office auf SCS. Fertig.**

---

# Mitmachen

**Open Source Wettbewerb 2026**

QR: ![w:200](https://api.qrserver.com/v1/create-qr-code/?size=200x200&data=https://open-source-wettbewerb.de/voting/opendesk/)

Link: [open-source-wettbewerb.de/voting/opendesk/](https://open-source-wettbewerb.de/voting/opendesk/)

**30 Sekunden. Offene Zukunft unterstützen.**

---

# Fragen
## +8 Minuten
