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
  .icon {
    width: 40px; height: 40px;
    display: inline-block; vertical-align: middle;
    margin-right: 8px;
  }
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
<svg viewBox="0 0 500 200" width="500" height="200" xmlns="http://www.w3.org/2000/svg">
<defs>
<marker id="hitl-arrow" viewBox="0 0 14 14" refX="13" refY="7" markerWidth="14" markerHeight="14" orient="auto">
<polygon points="0 0, 14 7, 0 14" fill="#007ACC" />
</marker>
<style>
  .hitl-box { fill: #fff; stroke: #007ACC; stroke-width: 3; rx: 8; } 
  .hitl-icon { fill: #007ACC; } 
  .hitl-text { font-family: Arial; fill: #333; } 
  .hitl-label { font-family: Arial; font-size: 10; fill: #666; } 
</style>
</defs>

<!-- Mensch -->
<rect x="80" y="70" width="120" height="60" class="hitl-box"/>
<circle cx="140" cy="100" r="18" class="hitl-icon"/>
<text x="140" y="95" text-anchor="middle" class="hitl-text" font-size="12">Mensch</text>
<text x="140" y="110" text-anchor="middle" class="hitl-label">Entscheidet &amp; kontrolliert</text>

<!-- Pfeil -->
<path d="M200 100 L300 100" stroke="#007ACC" stroke-width="3" marker-end="url(#hitl-arrow)"/>

<!-- Agent -->
<rect x="320" y="70" width="120" height="60" class="hitl-box"/>
<rect x="355" y="85" width="20" height="20" class="hitl-icon" rx="3"/>
<rect x="360" y="90" width="10" height="10" class="hitl-icon" rx="2"/>
<text x="380" y="95" text-anchor="middle" class="hitl-text" font-size="12">Agent</text>
<text x="380" y="110" text-anchor="middle" class="hitl-label">Schlägt vor &amp; unterstützt</text>

<!-- bidirektionaler Pfeil -->
<path d="M200 120 L320 120" stroke="#007ACC" stroke-width="2.5" marker-end="url(#hitl-arrow)" marker-start="url(#hitl-arrow)" stroke-dasharray="5,3"/>
<text x="260" y="125" text-anchor="middle" class="hitl-label">Human-in-the-Loop</text>
</svg>
</div>

**Agenten unterstützen – Menschen entscheiden.**

---

# Architektur

<div class="diagram">
<svg viewBox="0 0 600 320" width="600" height="320" xmlns="http://www.w3.org/2000/svg">
<defs>
<marker id="arch-arrow" viewBox="0 0 14 14" refX="13" refY="7" markerWidth="14" markerHeight="14" orient="auto">
<polygon points="0 0, 14 7, 0 14" fill="#2E8B57" />
</marker>
<style>
  .arch-box { fill: #F8F9FA; stroke: #2E8B57; stroke-width: 2.5; rx: 6; }
  .arch-primary { fill: #2E8B57; }
  .arch-text { font-family: Arial; fill: #333; font-size: 12; }
  .arch-label { font-family: Arial; fill: #666; font-size: 10; }
</style>
</defs>

<!-- OpenDesk Edu -->
<rect x="230" y="30" width="140" height="45" class="arch-box"/>
<circle cx="265" cy="52" r="12" class="arch-primary"/>
<circle cx="305" cy="52" r="12" class="arch-primary"/>
<circle cx="345" cy="52" r="12" class="arch-primary"/>
<text x="300" y="70" text-anchor="middle" class="arch-text">OpenDesk Edu</text>

<!-- Application Layer -->
<rect x="60" y="110" width="120" height="40" class="arch-box"/>
<path d="M70 125 L80 135 L100 125 L80 115 Z" class="arch-primary" fill="#2E8B57"/>
<text x="120" y="132" text-anchor="end" class="arch-text">Dokumente</text>

<rect x="210" y="110" width="120" height="40" class="arch-box"/>
<rect x="230" cy="130" width="20" height="20" class="arch-primary" fill="#2E8B57" rx="3"/>
<rect x="242" cy="130" width="20" height="20" class="arch-primary" fill="#2E8B57" rx="3"/>
<text x="270" y="132" text-anchor="end" class="arch-text">Team Orte</text>

<rect x="360" y="110" width="120" height="40" class="arch-box"/>
<polygon points="380,125 388,130 388,138 380,133" class="arch-primary" fill="#2E8B57"/>
<polygon points="392,125 400,130 400,138 392,133" class="arch-primary" fill="#2E8B57"/>
<text x="420" y="132" text-anchor="end" class="arch-text">Workflows</text>

<rect x="510" y="110" width="80" height="40" class="arch-box"/>
<circle cx="550" cy="130" r="8" class="arch-primary"/>
<path d="M545 125 L555 130 L545 135 Z" class="arch-primary"/>
<text x="550" y="150" text-anchor="middle" class="arch-text">Agenten</text>

<!-- Pfeile Layer 1 -->
<path d="M300 75 L300 110" stroke="#2E8B57" stroke-width="2.5" marker-end="url(#arch-arrow)"/>
<path d="M180 110 L180 130" stroke="#2E8B57" stroke-width="2" marker-end="url(#arch-arrow)"/>
<path d="M330 110 L330 130" stroke="#2E8B57" stroke-width="2" marker-end="url(#arch-arrow)"/>
<path d="M480 110 L480 130" stroke="#2E8B57" stroke-width="2" marker-end="url(#arch-arrow)"/>
<path d="M550 110 L550 130" stroke="#2E8B57" stroke-width="2" marker-end="url(#arch-arrow)"/>

<!-- Infrastructure Layer -->
<rect x="240" y="190" width="120" height="35" class="arch-box"/>
<polygon points="260,195 265,205 275,210 295,210 305,205 310,195 285,205 275,200 265,205" class="arch-primary" fill="#2E8B57"/>
<text x="300" y="210" text-anchor="middle" class="arch-text">k3s Cluster</text>

<rect x="240" y="240" width="120" height="35" class="arch-box"/>
<rect x="255" y="252" width="14" height="14" class="arch-primary" rx="2"/>
<rect x="273" y="252" width="14" height="14" class="arch-primary" rx="2"/>
<rect x="291" y="252" width="14" height="14" class="arch-primary" rx="2"/>
<text x="300" y="260" text-anchor="middle" class="arch-text">Sovereign Cloud Stack</text>

<!-- Pfeile Layer 2 -->
<path d="M180 150 L240 190" stroke="#2E8B57" stroke-width="2" marker-end="url(#arch-arrow)"/>
<path d="M330 150 L300 190" stroke="#2E8B57" stroke-width="2" marker-end="url(#arch-arrow)"/>
<path d="M480 150 L300 190" stroke="#2E8B57" stroke-width="2" marker-end="url(#arch-arrow)"/>
<path d="M550 150 L300 190" stroke="#2E8B57" stroke-width="2" marker-end="url(#arch-arrow)"/>
<path d="M300 225 L300 240" stroke="#2E8B57" stroke-width="2" marker-end="url(#arch-arrow)"/>
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
<svg viewBox="0 0 700 450" width="700" height="450" xmlns="http://www.w3.org/2000/svg">
<defs>
<marker id="stack-arrow" viewBox="0 0 14 14" refX="13" refY="7" markerWidth="14" markerHeight="14" orient="auto">
<polygon points="0 0, 14 7, 0 14" fill="#8E44AD" />
</marker>
<style>
  .stack-box { fill: #fff; stroke: #8E44AD; stroke-width: 2.5; rx: 8; }
  .stack-icon { fill: #8E44AD; } 
  .stack-text { font-family: Arial; fill: #333; font-size: 11; }
  .stack-label { font-family: Arial; fill: #8E44AD; font-size: 9; }
</style>
</defs>

<!-- Layer 1: Applications -->
<rect x="300" y="40" width="100" height="35" class="stack-box"/>
<circle cx="325" cy="57" r="10" class="stack-icon"/>
<circle cx="345" cy="57" r="10" class="stack-icon"/>
<circle cx="365" cy="57" r="10" class="stack-icon"/>
<text x="350" y="72" text-anchor="middle" class="stack-text">OpenDesk Edu</text>

<!-- Layer 2: Services -->
<g id="Layer2">
<rect x="100" y="110" width="100" height="30" class="stack-box"/>
<path d="M110 125 L120 130 L130 125 L120 120 Z" class="stack-icon"/>
<text x="150" y="132" text-anchor="middle" class="stack-text">OpenCloud</text>
<text x="150" y="140" text-anchor="middle" class="stack-label">Dokumente</text>

<rect x="220" y="110" width="100" height="30" class="stack-box"/>
<rect x="230" y="123" width="12" height="12" class="stack-icon" rx="2"/>
<rect x="246" y="123" width="12" height="12" class="stack-icon" rx="2"/>
<text x="270" y="132" text-anchor="middle" class="stack-text">SOGo</text>
<text x="270" y="140" text-anchor="middle" class="stack-label">E-Mail &amp; Groupware</text>

<rect x="340" y="110" width="100" height="30" class="stack-box"/>
<polygon points="350,125 356,130 356,136 350,131" class="stack-icon"/>
<polygon points="360,125 366,130 366,136 360,131" class="stack-icon"/>
<rect x="370" y="125" width="12" height="12" class="stack-icon" rx="2"/>
<text x="390" y="132" text-anchor="middle" class="stack-text">OpenProject</text>
<text x="390" y="140" text-anchor="middle" class="stack-label">Projektmanagement</text>

<rect x="460" y="110" width="100" height="30" class="stack-box"/>
<circle cx="470" cy="125" r="5" class="stack-icon"/>
<circle cx="490" cy="125" r="5" class="stack-icon"/>
<circle cx="510" cy="125" r="5" class="stack-icon"/>
<text x="510" y="132" text-anchor="middle" class="stack-text">Matrix/Element</text>
<text x="510" y="140" text-anchor="middle" class="stack-label">Chat &amp; Kollaboration</text>
</g>

<!-- Layer 3: Infrastructure -->
<g id="Layer3">
<rect x="200" y="180" width="100" height="30" class="stack-box"/>
<rect x="210" y="193" width="10" height="10" class="stack-icon"/>
<circle cx="225" cy="198" r="4" class="stack-icon"/>
<rect x="240" y="193" width="10" height="10" class="stack-icon"/>
<text x="250" y="201" text-anchor="middle" class="stack-text">Keycloak</text>
<text x="250" y="209" text-anchor="middle" class="stack-label">Identity &amp; Auth</text>

<rect x="320" y="180" width="100" height="30" class="stack-box"/>
<circle cx="335" cy="195" r="6" class="stack-icon"/>
<circle cx="365" cy="195" r="6" class="stack-icon"/>
<circle cx="350" cy="195" r="6" class="stack-icon"/>
<text x="370" y="201" text-anchor="middle" class="stack-text">Sovereign Cloud Stack</text>
<text x="370" y="209" text-anchor="middle" class="stack-label">Deployment Framework</text>
</g>

<!-- Layer 4: Databases -->
<g id="Layer4">
<rect x="150" y="250" width="100" height="30" class="stack-box"/>
<rect x="160" y="260" width="20" height="20" class="stack-icon">
<rect x="162" y="262" width="16" height="16" fill="#fff"/>
</rect>
<text x="200" y="271" text-anchor="middle" class="stack-text">Galera Cluster</text>
<text x="200" y="279" text-anchor="middle" class="stack-label">MariaDB</text>

<rect x="270" y="250" width="100" height="30" class="stack-box"/>
<path d="M280 260 L288 265 L288 275 L280 270 Z" class="stack-icon"/>
<path d="M290 260 L298 265 L298 275 L290 270 Z" class="stack-icon"/>
<text x="320" y="271" text-anchor="middle" class="stack-text">PostgreSQL</text>
<text x="320" y="279" text-anchor="middle" class="stack-label">OpenProject DB</text>

<rect x="390" y="250" width="80" height="30" class="stack-box"/>
<rect x="400" y="260" width="16" height="16" class="stack-icon" rx="2"/>
<text x="430" y="271" text-anchor="middle" class="stack-text">Redis</text>
<text x="430" y="279" text-anchor="middle" class="stack-label">Cache</text>
</g>

<!-- Layer 5: Platform -->
<rect x="280" y="320" width="140" height="30" class="stack-box"/>
<polygon points="300,325 308,335 316,325 308,330" class="stack-icon"/>
<polygon points="320,325 328,335 336,325 328,330" class="stack-icon"/>
<rect x="342" y="326" width="16" height="16" class="stack-icon" rx="2"/>
<text x="350" y="341" text-anchor="middle" class="stack-text">k3s Cluster</text>
<text x="350" y="349" text-anchor="middle" class="stack-label">Lightweight Kubernetes</text>

<!-- Arrows between layers -->
<path d="M350 75 L250 110" stroke="#8E44AD" stroke-width="2" marker-end="url(#stack-arrow)" stroke-dasharray="4,2"/>
<path d="M350 75 L350 110" stroke="#8E44AD" stroke-width="2" marker-end="url(#stack-arrow)" stroke-dasharray="4,2"/>
<path d="M350 75 L450 110" stroke="#8E44AD" stroke-width="2" marker-end="url(#stack-arrow)" stroke-dasharray="4,2"/>

<path d="M100 140 L200 180" stroke="#8E44AD" stroke-width="1.5" marker-end="url(#stack-arrow)"/>
<path d="M220 140 L250 180" stroke="#8E44AD" stroke-width="1.5" marker-end="url(#stack-arrow)"/>
<path d="M340 140 L320 180" stroke="#8E44AD" stroke-width="1.5" marker-end="url(#stack-arrow)"/>
<path d="M460 140 L320 180" stroke="#8E44AD" stroke-width="1.5" marker-end="url(#stack-arrow)"/>

<path d="M200 210 L150 250" stroke="#8E44AD" stroke-width="1.5" marker-end="url(#stack-arrow)"/>
<path d="M320 210 L270 250" stroke="#8E44AD" stroke-width="1.5" marker-end="url(#stack-arrow)"/>
<path d="M320 210 L390 250" stroke="#8E44AD" stroke-width="1.5" marker-end="url(#stack-arrow)"/>

<path d="M150 280 L280 320" stroke="#8E44AD" stroke-width="1.5" marker-end="url(#stack-arrow)"/>
<path d="M270 280 L280 320" stroke="#8E44AD" stroke-width="1.5" marker-end="url(#stack-arrow)"/>
<path d="M390 280 L350 320" stroke="#8E44AD" stroke-width="1.5" marker-end="url(#stack-arrow)"/>
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
