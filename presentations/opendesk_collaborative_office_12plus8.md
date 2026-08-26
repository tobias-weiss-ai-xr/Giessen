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
  img { background: transparent !important; max-width: 100%; height: auto; }
  .diagram { text-align: center; margin: 20px 0; }
  .diagram svg { max-width: 100%; height: auto; }
  /* Hide all footers */
  section::after { display: none !important; }
  footer { display: none !important; }
  [class*="footer"] { display: none !important; }
---

# OpenDesk Edu
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

**OpenDesk Edu bietet all das – offen und self-hosted.**

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

<div class="diagram">
<svg viewBox="0 0 400 150" width="400" height="150" xmlns="http://www.w3.org/2000/svg">
<defs>
<marker id="arrow" viewBox="0 0 10 10" refX="9" refY="5" markerWidth="10" markerHeight="10" orient="auto">
<polygon points="0 0, 10 5, 0 10" fill="#333"/>
</marker>
</defs>
<circle cx="100" cy="75" r="35" fill="#ECECFF" stroke="#571EFA" stroke-width="2">
<text x="100" y="70" text-anchor="middle" font-family="Arial" font-size="14" fill="#333">Mensch</text>
<text x="100" y="85" text-anchor="middle" font-family="Arial" font-size="10" fill="#666">(Entscheidet)</text>
</circle>
<rect x="250" y="60" width="100" height="35" fill="#ECECFF" stroke="#333" stroke-width="2" rx="6">
<text x="300" y="78" text-anchor="middle" font-family="Arial" font-size="14" fill="#333">Agent</text>
<text x="300" y="93" text-anchor="middle" font-family="Arial" font-size="10" fill="#666">(Schlägt vor)</text>
</rect>
<path d="M135 75 L250 75" stroke="#333" stroke-width="2" marker-end="url(#arrow)"/>
<text x="192" y="60" text-anchor="middle" font-family="Arial" font-size="12" fill="#666">kontrolliert</text>
<path d="M300 75 L135 75" stroke="#333" stroke-width="2" marker-end="url(#arrow)"/>
<text x="192" y="90" text-anchor="middle" font-family="Arial" font-size="12" fill="#666">unterstützt</text>
</svg>
</div>

**Agenten unterstützen – Menschen entscheiden.**

---

# Architektur

<div class="diagram">
<svg viewBox="0 0 600 300" width="600" height="300" xmlns="http://www.w3.org/2000/svg">
<defs>
<marker id="arrow" viewBox="0 0 10 10" refX="9" refY="5" markerWidth="10" markerHeight="10" orient="auto">
<polygon points="0 0, 10 5, 0 10" fill="#333"/>
</marker>
</defs>
<rect x="250" y="20" width="120" height="40" fill="#ECECFF" stroke="#333" stroke-width="2" rx="6">
<text x="310" y="42" text-anchor="middle" font-family="Arial" font-size="14" fill="#333">OpenDesk Edu</text>
</rect>
<rect x="50" y="100" width="100" height="35" fill="#ECECFF" stroke="#333" stroke-width="2" rx="6">
<text x="100" y="120" text-anchor="middle" font-family="Arial" font-size="13" fill="#333">Dokumente</text>
</rect>
<rect x="180" y="100" width="100" height="35" fill="#ECECFF" stroke="#333" stroke-width="2" rx="6">
<text x="230" y="120" text-anchor="middle" font-family="Arial" font-size="13" fill="#333">Team Orte</text>
</rect>
<rect x="310" y="100" width="100" height="35" fill="#ECECFF" stroke="#333" stroke-width="2" rx="6">
<text x="360" y="120" text-anchor="middle" font-family="Arial" font-size="13" fill="#333">Workflows</text>
</rect>
<rect x="440" y="100" width="100" height="35" fill="#ECECFF" stroke="#333" stroke-width="2" rx="6">
<text x="490" y="120" text-anchor="middle" font-family="Arial" font-size="13" fill="#333">Agenten</text>
</rect>
<rect x="280" y="180" width="100" height="35" fill="#ECECFF" stroke="#333" stroke-width="2" rx="6">
<text x="330" y="200" text-anchor="middle" font-family="Arial" font-size="13" fill="#333">k3s Cluster</text>
</rect>
<rect x="280" y="230" width="100" height="35" fill="#ECECFF" stroke="#333" stroke-width="2" rx="6">
<text x="330" y="250" text-anchor="middle" font-family="Arial" font-size="13" fill="#333">SCS Server</text>
</rect>
<path d="M310 60 L310 100" stroke="#333" stroke-width="1.5" marker-end="url(#arrow)"/>
<path d="M150 100 L100 120" stroke="#333" stroke-width="1.5" marker-end="url(#arrow)"/>
<path d="M230 100 L230 120" stroke="#333" stroke-width="1.5" marker-end="url(#arrow)"/>
<path d="M360 100 L360 120" stroke="#333" stroke-width="1.5" marker-end="url(#arrow)"/>
<path d="M490 100 L490 120" stroke="#333" stroke-width="1.5" marker-end="url(#arrow)"/>
<path d="M230 135 L280 180" stroke="#333" stroke-width="1.5" marker-end="url(#arrow)"/>
<path d="M150 135 L280 180" stroke="#333" stroke-width="1.5" marker-end="url(#arrow)"/>
<path d="M360 135 L380 180" stroke="#333" stroke-width="1.5" marker-end="url(#arrow)"/>
<path d="M490 135 L380 180" stroke="#333" stroke-width="1.5" marker-end="url(#arrow)"/>
<path d="M330 215 L330 230" stroke="#333" stroke-width="1.5" marker-end="url(#arrow)"/>
<text x="330" y="210" text-anchor="middle" font-family="Arial" font-size="11" fill="#666">läuft auf</text>
<text x="330" y="225" text-anchor="middle" font-family="Arial" font-size="11" fill="#666">SCS Deployment</text>
</svg>
</div>

**Einfach. Offene Schnittstellen. Self-Hosted.**

---

# Use Case 1

**Team Dokumentation**

Problem: Veraltete Wikimedia, zentrale Pflege nötig

Lösung: Gemeinsame Bearbeitung mit **Agenten-Unterstützung + HITL**

*Mensch validiert, Agent schlägt vor.*

---

# Use Case 2

**Projektmanagement**

Problem: Manuelle Status-Updates, wiederkehrende Aufgaben

Lösung: Automatisierte Workflows mit **Kollaborations-Agenten + HITL**

*Mensch entscheidet, Agent empfiehlt.*

---

# Use Case 3

**Wissensmanagement**

Problem: Verstreute Informationen, schwierige Suche

Lösung: Intelligente Verknüpfung mit **Kontext-Erkennung + HITL**

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

<div class="diagram">
<svg viewBox="0 0 700 400" width="700" height="400" xmlns="http://www.w3.org/2000/svg">
<defs>
<marker id="arrow" viewBox="0 0 10 10" refX="9" refY="5" markerWidth="10" markerHeight="10" orient="auto">
<polygon points="0 0, 10 5, 0 10" fill="#333"/>
</marker>
</defs>
<rect x="300" y="20" width="120" height="35" fill="#ECECFF" stroke="#333" stroke-width="2" rx="6">
<text x="360" y="40" text-anchor="middle" font-family="Arial" font-size="14" fill="#333">OpenDesk Edu</text>
</rect>
<rect x="100" y="80" width="140" height="35" fill="#ECECFF" stroke="#333" stroke-width="2" rx="6">
<text x="170" y="100" text-anchor="middle" font-family="Arial" font-size="12" fill="#333">OpenCloud</text>
<text x="170" y="112" text-anchor="middle" font-family="Arial" font-size="9" fill="#666">(Dokumente)</text>
</rect>
<rect x="280" y="80" width="140" height="35" fill="#ECECFF" stroke="#333" stroke-width="2" rx="6">
<text x="350" y="100" text-anchor="middle" font-family="Arial" font-size="12" fill="#333">SOGo</text>
<text x="350" y="112" text-anchor="middle" font-family="Arial" font-size="9" fill="#666">(E-Mail & Groupware)</text>
</rect>
<rect x="460" y="80" width="140" height="35" fill="#ECECFF" stroke="#333" stroke-width="2" rx="6">
<text x="530" y="100" text-anchor="middle" font-family="Arial" font-size="12" fill="#333">OpenProject</text>
<text x="530" y="112" text-anchor="middle" font-family="Arial" font-size="9" fill="#666">(Projektmanagement)</text>
</rect>
<rect x="200" y="140" width="140" height="35" fill="#ECECFF" stroke="#333" stroke-width="2" rx="6">
<text x="270" y="160" text-anchor="middle" font-family="Arial" font-size="12" fill="#333">Element</text>
<text x="270" y="172" text-anchor="middle" font-family="Arial" font-size="9" fill="#666">(Matrix Client)</text>
</rect>
<rect x="380" y="140" width="140" height="35" fill="#ECECFF" stroke="#333" stroke-width="2" rx="6">
<text x="450" y="160" text-anchor="middle" font-family="Arial" font-size="12" fill="#333">Synapse</text>
<text x="450" y="172" text-anchor="middle" font-family="Arial" font-size="9" fill="#666">(Matrix Server)</text>
</rect>
<rect x="280" y="220" width="140" height="35" fill="#ECECFF" stroke="#333" stroke-width="2" rx="6">
<text x="350" y="240" text-anchor="middle" font-family="Arial" font-size="12" fill="#333">Keycloak</text>
<text x="350" y="252" text-anchor="middle" font-family="Arial" font-size="9" fill="#666">(Identity & Auth)</text>
</rect>
<rect x="200" y="280" width="140" height="35" fill="#ECECFF" stroke="#333" stroke-width="2" rx="6">
<text x="270" y="300" text-anchor="middle" font-family="Arial" font-size="12" fill="#333">Galera</text>
<text x="270" y="312" text-anchor="middle" font-family="Arial" font-size="9" fill="#666">(MariaDB Cluster)</text>
</rect>
<rect x="380" y="280" width="140" height="35" fill="#ECECFF" stroke="#333" stroke-width="2" rx="6">
<text x="450" y="300" text-anchor="middle" font-family="Arial" font-size="12" fill="#333">PostgreSQL</text>
<text x="450" y="312" text-anchor="middle" font-family="Arial" font-size="9" fill="#666">(OpenProject DB)</text>
</rect>
<rect x="560" y="280" width="80" height="35" fill="#ECECFF" stroke="#333" stroke-width="2" rx="6">
<text x="600" y="300" text-anchor="middle" font-family="Arial" font-size="12" fill="#333">Redis</text>
<text x="600" y="312" text-anchor="middle" font-family="Arial" font-size="9" fill="#666">(Cache)</text>
</rect>
<rect x="300" y="340" width="140" height="35" fill="#ECECFF" stroke="#333" stroke-width="2" rx="6">
<text x="370" y="360" text-anchor="middle" font-family="Arial" font-size="12" fill="#333">k3s Cluster</text>
<text x="370" y="372" text-anchor="middle" font-family="Arial" font-size="9" fill="#666">(Sovereign Cloud Stack)</text>
</rect>
<path d="M360 55 L360 80" stroke="#333" stroke-width="1.5" marker-end="url(#arrow)"/>
<path d="M170 115 L170 140" stroke="#333" stroke-width="1.5" marker-end="url(#arrow)"/>
<path d="M350 115 L350 140" stroke="#333" stroke-width="1.5" marker-end="url(#arrow)"/>
<path d="M530 115 L530 140" stroke="#333" stroke-width="1.5" marker-end="url(#arrow)"/>
<path d="M170 130 L200 160" stroke="#333" stroke-width="1.5" marker-end="url(#arrow)"/>
<path d="M350 130 L380 160" stroke="#333" stroke-width="1.5" marker-end="url(#arrow)"/>
<path d="M270 175 L270 220" stroke="#333" stroke-width="1.5" marker-end="url(#arrow)"/>
<path d="M350 175 L350 220" stroke="#333" stroke-width="1.5" marker-end="url(#arrow)"/>
<path d="M530 175 L350 220" stroke="#333" stroke-width="1.5" marker-end="url(#arrow)"/>
<path d="M200 255 L200 280" stroke="#333" stroke-width="1.5" marker-end="url(#arrow)"/>
<path d="M350 255 L350 280" stroke="#333" stroke-width="1.5" marker-end="url(#arrow)"/>
<path d="M450 255 L450 280" stroke="#333" stroke-width="1.5" marker-end="url(#arrow)"/>
<path d="M600 255 L560 280" stroke="#333" stroke-width="1.5" marker-end="url(#arrow)"/>
<path d="M370 305 L370 340" stroke="#333" stroke-width="1.5" marker-end="url(#arrow)"/>
<path d="M270 315 L300 340" stroke="#333" stroke-width="1.5" marker-end="url(#arrow)"/>
<path d="M450 315 L380 340" stroke="#333" stroke-width="1.5" marker-end="url(#arrow)"/>
<path d="M600 315 L480 340" stroke="#333" stroke-width="1.5" marker-end="url(#arrow)"/>
</svg>
</div>

**OpenCloud, SOGo, OpenProject, Matrix/Element, Keycloak, Galera DB, PostgreSQL, Redis auf k3s.**

---

# Installation

```bash
# k3s (1 Befehl)
curl -sfL https://get.k3s.io | sh -

# OpenDesk Edu auf Sovereign Cloud Stack (1 Befehl)
kubectl apply -f opendesk-scs.yaml
```

**5 Minuten. Eigenes Office auf k3s. Fertig.**

---

# Mitmachen

**Open Source Wettbewerb 2026**

<div class="diagram">
<img src="https://api.qrserver.com/v1/create-qr-code/?size=200x200&data=https://open-source-wettbewerb.de/voting/opendesk-edu/" alt="QR Code" width="200" />
</div>

Link: [open-source-wettbewerb.de/voting/opendesk-edu/](https://open-source-wettbewerb.de/voting/opendesk-edu/)

**30 Sekunden. Offene Zukunft unterstützen.**

---

# Fragen
## +8 Minuten
