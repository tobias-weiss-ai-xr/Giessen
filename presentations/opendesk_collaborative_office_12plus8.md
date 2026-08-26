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

<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 400 150" width="400" height="150">
  <style>
    .node { stroke: #333; stroke-width: 2; fill: #f8f8f8; font-family: Arial, sans-serif; font-size: 14px; text-anchor: middle; }
    .node circle { stroke: #571EFA; stroke-width: 2; fill: #ECECFF; }
    .arrow { stroke: #333; stroke-width: 2; fill: none; marker-end: url(#arrowhead); }
    .label { font-family: Arial, sans-serif; font-size: 12px; fill: #333; text-anchor: middle; }
  </style>
  <defs>
    <marker id="arrowhead" markerWidth="10" markerHeight="7" refX="9" refY="3.5" orient="auto">
      <polygon points="0 0, 10 3.5, 0 7" fill="#333"/>
    </marker>
  </defs>
  <circle cx="100" cy="75" r="35" class="node">
    <text x="100" y="70">Mensch</text>
    <text x="100" y="85" font-size="10">(Entscheidet)</text>
  </circle>
  <rect x="250" y="60" width="100" height="35" class="node">
    <text x="300" y="78">Agent</text>
    <text x="300" y="93" font-size="10">(Schlägt vor)</text>
  </rect>
  <path d="M135 75 L250 75" class="arrow"/>
  <text x="192" y="60" class="label">kontrolliert</text>
  <path d="M300 75 L135 75" class="arrow"/>
  <text x="192" y="90" class="label">unterstützt</text>
</svg>

</div>

**Agenten unterstützen – Menschen entscheiden.**

---

# Architektur

<div class="diagram">

<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 600 300" width="600" height="300">
  <style>
    .node { stroke: #333; stroke-width: 1.5; fill: #f8f8f8; font-family: Arial, sans-serif; font-size: 13px; text-anchor: middle; }
    .node rect { rx: 6; ry: 6; }
    .arrow { stroke: #333; stroke-width: 1.5; fill: none; marker-end: url(#arrowhead); }
    .label { font-family: Arial, sans-serif; font-size: 11px; fill: #666; text-anchor: middle; }
    .title { font-family: Arial, sans-serif; font-size: 14px; font-weight: bold; fill: #333; }
  </style>
  <defs>
    <marker id="arrowhead" markerWidth="8" markerHeight="5" refX="7" refY="2.5" orient="auto">
      <polygon points="0 0, 8 2.5, 0 5" fill="#333"/>
    </marker>
  </defs>
  
  <rect x="250" y="20" width="120" height="40" class="node">
    <text x="310" y="42">OpenDesk Edu</text>
  </rect>
  
  <rect x="50" y="100" width="100" height="35" class="node">
    <text x="100" y="120">Dokumente</text>
  </rect>
  <rect x="180" y="100" width="100" height="35" class="node">
    <text x="230" y="120">Team Orte</text>
  </rect>
  <rect x="310" y="100" width="100" height="35" class="node">
    <text x="360" y="120">Workflows</text>
  </rect>
  <rect x="440" y="100" width="100" height="35" class="node">
    <text x="490" y="120">Agenten</text>
  </rect>
  
  <rect x="280" y="180" width="100" height="35" class="node">
    <text x="330" y="200">k3s Cluster</text>
  </rect>
  <rect x="280" y="230" width="100" height="35" class="node">
    <text x="330" y="250">SCS Server</text>
  </rect>
  
  <path d="M310 60 L310 100" class="arrow"/>
  <path d="M150 100 L100 120" class="arrow"/>
  <path d="M230 100 L230 120" class="arrow"/>
  <path d="M360 100 L360 120" class="arrow"/>
  <path d="M490 100 L490 120" class="arrow"/>
  <path d="M230 135 L280 180" class="arrow"/>
  <path d="M150 135 L280 180" class="arrow"/>
  <path d="M360 135 L380 180" class="arrow"/>
  <path d="M490 135 L380 180" class="arrow"/>
  <path d="M330 215 L330 230" class="arrow"/>
  <text x="330" y="210" class="label">läuft auf</text>
  <text x="330" y="225" class="label">SCS Deployment</text>
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

<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 700 400" width="700" height="400">
  <style>
    .node { stroke: #333; stroke-width: 1.5; fill: #f8f8f8; font-family: Arial, sans-serif; font-size: 12px; text-anchor: middle; }
    .node rect { rx: 6; ry: 6; }
    .cluster { fill: none; stroke: #aaa; stroke-width: 1; stroke-dasharray: 5,5; }
    .arrow { stroke: #333; stroke-width: 1.5; fill: none; marker-end: url(#arrowhead); }
    .label { font-family: Arial, sans-serif; font-size: 11px; fill: #666; text-anchor: middle; }
    .title { font-family: Arial, sans-serif; font-size: 14px; font-weight: bold; fill: #333; }
  </style>
  <defs>
    <marker id="arrowhead" markerWidth="8" markerHeight="5" refX="7" refY="2.5" orient="auto">
      <polygon points="0 0, 8 2.5, 0 5" fill="#333"/>
    </marker>
  </defs>
  
  <rect x="300" y="20" width="120" height="35" class="node">
    <text x="360" y="40">OpenDesk Edu</text>
  </rect>
  
  <!-- Applications -->
  <rect x="100" y="80" width="140" height="35" class="node">
    <text x="170" y="100">OpenCloud</text>
    <text x="170" y="112" font-size="9">(Dokumente)</text>
  </rect>
  <rect x="280" y="80" width="140" height="35" class="node">
    <text x="350" y="100">SOGo</text>
    <text x="350" y="112" font-size="9">(E-Mail & Groupware)</text>
  </rect>
  <rect x="460" y="80" width="140" height="35" class="node">
    <text x="530" y="100">OpenProject</text>
    <text x="530" y="112" font-size="9">(Projektmanagement)</text>
  </rect>
  
  <!-- Chat -->
  <rect x="200" y="140" width="140" height="35" class="node">
    <text x="270" y="160">Element</text>
    <text x="270" y="172" font-size="9">(Matrix Client)</text>
  </rect>
  <rect x="380" y="140" width="140" height="35" class="node">
    <text x="450" y="160">Synapse</text>
    <text x="450" y="172" font-size="9">(Matrix Server)</text>
  </rect>
  
  <!-- Infrastructure -->
  <rect x="280" y="220" width="140" height="35" class="node">
    <text x="350" y="240">Keycloak</text>
    <text x="350" y="252" font-size="9">(Identity & Auth)</text>
  </rect>
  <rect x="200" y="280" width="140" height="35" class="node">
    <text x="270" y="300">Galera</text>
    <text x="270" y="312" font-size="9">(MariaDB Cluster)</text>
  </rect>
  <rect x="380" y="280" width="140" height="35" class="node">
    <text x="450" y="300">PostgreSQL</text>
    <text x="450" y="312" font-size="9">(OpenProject DB)</text>
  </rect>
  <rect x="560" y="280" width="80" height="35" class="node">
    <text x="600" y="300">Redis</text>
    <text x="600" y="312" font-size="9">(Cache)</text>
  </rect>
  
  <!-- k3s -->
  <rect x="300" y="340" width="140" height="35" class="node">
    <text x="370" y="360">k3s Cluster</text>
    <text x="370" y="372" font-size="9">(Sovereign Cloud Stack)</text>
  </rect>
  
  <!-- Arrows -->
  <path d="M360 55 L360 80" class="arrow"/>
  <path d="M170 115 L170 140" class="arrow"/>
  <path d="M350 115 L350 140" class="arrow"/>
  <path d="M530 115 L530 140" class="arrow"/>
  <path d="M170 130 L200 160" class="arrow"/>
  <path d="M350 130 L380 160" class="arrow"/>
  <path d="M270 175 L270 220" class="arrow"/>
  <path d="350 175 L350 220" class="arrow"/>
  <path d="530 175 L350 220" class="arrow"/>
  <path d="200 255 L200 280" class="arrow"/>
  <path d="350 255 L350 280" class="arrow"/>
  <path d="450 255 L450 280" class="arrow"/>
  <path d="600 255 L560 280" class="arrow"/>
  <path d="370 305 L370 340" class="arrow"/>
  <path d="270 315 L300 340" class="arrow"/>
  <path d="450 315 L380 340" class="arrow"/>
  <path d="600 315 L480 340" class="arrow"/>
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

QR: ![w:200](https://api.qrserver.com/v1/create-qr-code/?size=200x200&data=https://open-source-wettbewerb.de/voting/opendesk-edu/)

Link: [open-source-wettbewerb.de/voting/opendesk-edu/](https://open-source-wettbewerb.de/voting/opendesk-edu/)

**30 Sekunden. Offene Zukunft unterstützen.**

---

# Fragen
## +8 Minuten
