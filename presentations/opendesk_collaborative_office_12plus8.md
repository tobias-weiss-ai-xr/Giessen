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
<svg viewBox="0 0 600 250" width="600" height="250" xmlns="http://www.w3.org/2000/svg">
<defs>
<marker id="arrow-blue" viewBox="0 0 14 14" refX="13" refY="7" markerWidth="14" markerHeight="14" orient="auto">
<polygon points="0,0 14,7 0,14 4,7" fill="#007ACC" />
</marker>
</defs>

<g font-family="Arial">
<!-- Mensch -->
<circle cx="200" cy="125" r="50" fill="none" stroke="#007ACC" stroke-width="4"/>
<circle cx="200" cy="125" r="30" fill="#007ACC" opacity="0.15"/>
<text x="200" y="117" text-anchor="middle" font-size="18" font-weight="bold" fill="#333">Mensch</text>
<text x="200" y="135" text-anchor="middle" font-size="14" fill="#666">Entscheidet &amp; kontrolliert</text>

<!-- Agent -->
<rect x="350" y="100" width="100" height="50" fill="none" stroke="#007ACC" stroke-width="4" rx="8"/>
<rect x="365" y="112" width="12" height="12" fill="#007ACC" rx="2"/>
<rect x="383" y="112" width="12" height="12" fill="#007ACC" rx="2"/>
<rect x="401" y="112" width="12" height="12" fill="#007ACC" rx="2"/>
<text x="400" y="128" text-anchor="middle" font-size="18" font-weight="bold" fill="#333">Agent</text>
<text x="400" y="144" text-anchor="middle" font-size="14" fill="#666">Schlägt vor &amp; unterstützt</text>

<!-- Hauptpfeil: Mensch -> Agent (kontrolliert) -->
<path d="M250 125 L350 125" stroke="#007ACC" stroke-width="4" marker-end="url(#arrow-blue)"/>
<text x="300" y="110" text-anchor="middle" font-size="14" fill="#007ACC">kontrolliert</text>

<!-- Rückpfeile: Agent -> Mensch (unterstützt) -->
<path d="M400 100 L400 80 L250 80 L250 100" stroke="#007ACC" stroke-width="2.5" marker-end="url(#arrow-blue)" stroke-dasharray="6,4" fill="none"/>
<path d="M400 150 L400 170 L250 170 L250 150" stroke="#007ACC" stroke-width="2.5" marker-end="url(#arrow-blue)" stroke-dasharray="6,4" fill="none"/>
<text x="300" y="175" text-anchor="middle" font-size="14" fill="#007ACC">unterstützt</text>
</g>
</svg>
</div>

**Agenten unterstützen – Menschen entscheiden.**

---

# Architektur

<div class="diagram">
<svg viewBox="0 0 600 350" width="600" height="350" xmlns="http://www.w3.org/2000/svg">
<defs>
<marker id="arrow-green" viewBox="0 0 14 14" refX="13" refY="7" markerWidth="14" markerHeight="14" orient="auto">
<polygon points="0,0 14,7 0,14 4,7" fill="#2E8B57" />
</marker>
</defs>

<g font-family="Arial">
<!-- OpenDesk Edu -->
<rect x="230" y="40" width="140" height="50" fill="none" stroke="#2E8B57" stroke-width="4" rx="8"/>
<text x="300" y="70" text-anchor="middle" font-size="18" font-weight="bold" fill="#333">OpenDesk Edu</text>

<!-- Hauptpfeil nach unten -->
<path d="M300 90 L300 120" stroke="#2E8B57" stroke-width="3" marker-end="url(#arrow-green)"/>

<!-- Application Layer -->
<rect x="100" y="120" width="100" height="40" fill="none" stroke="#2E8B57" stroke-width="2.5" rx="6"/>
<text x="150" y="145" text-anchor="middle" font-size="13" fill="#333">Dokumente</text>

<rect x="230" y="120" width="100" height="40" fill="none" stroke="#2E8B57" stroke-width="2.5" rx="6"/>
<text x="280" y="145" text-anchor="middle" font-size="13" fill="#333">Team Orte</text>

<rect x="360" y="120" width="100" height="40" fill="none" stroke="#2E8B57" stroke-width="2.5" rx="6"/>
<text x="410" y="145" text-anchor="middle" font-size="13" fill="#333">Workflows</text>

<rect x="490" y="120" width="100" height="40" fill="none" stroke="#2E8B57" stroke-width="2.5" rx="6"/>
<text x="540" y="145" text-anchor="middle" font-size="13" fill="#333">Agenten</text>

<!-- Pfeile zu Infrastruktur -->
<path d="M150 160 L150 190 L300 190 L300 220" stroke="#2E8B57" stroke-width="2" marker-end="url(#arrow-green)" stroke-dasharray="5,3" fill="none"/>
<path d="M280 160 L280 190" stroke="#2E8B57" stroke-width="2" marker-end="url(#arrow-green)" stroke-dasharray="5,3" fill="none"/>
<path d="M410 160 L410 190" stroke="#2E8B57" stroke-width="2" marker-end="url(#arrow-green)" stroke-dasharray="5,3" fill="none"/>
<path d="M540 160 L540 190" stroke="#2E8B57" stroke-width="2" marker-end="url(#arrow-green)" stroke-dasharray="5,3" fill="none"/>

<!-- Infrastructure Layer -->
<rect x="250" y="220" width="100" height="40" fill="none" stroke="#2E8B57" stroke-width="2.5" rx="6"/>
<text x="300" y="245" text-anchor="middle" font-size="13" fill="#333">k3s Cluster</text>

<path d="M300 260 L300 290" stroke="#2E8B57" stroke-width="2" marker-end="url(#arrow-green)" fill="none"/>

<rect x="250" y="290" width="100" height="40" fill="none" stroke="#2E8B57" stroke-width="2.5" rx="6"/>
<text x="300" y="315" text-anchor="middle" font-size="13" fill="#333">Sovereign Cloud Stack</text>

<text x="300" y="205" text-anchor="middle" font-size="11" fill="#666">läuft auf</text>
</g>
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
<marker id="arrow-purple" viewBox="0 0 14 14" refX="13" refY="7" markerWidth="14" markerHeight="14" orient="auto">
<polygon points="0,0 14,7 0,14 4,7" fill="#8E44AD" />
</marker>
</defs>

<g font-family="Arial">
<!-- Layer 1: OpenDesk Edu -->
<rect x="300" y="40" width="100" height="40" fill="none" stroke="#8E44AD" stroke-width="4" rx="8"/>
<text x="350" y="65" text-anchor="middle" font-size="15" font-weight="bold" fill="#333">OpenDesk Edu</text>

<!-- Layer 2: Services -->
<rect x="120" y="100" width="120" height="40" fill="none" stroke="#8E44AD" stroke-width="2.5" rx="6"/>
<text x="180" y="125" text-anchor="middle" font-size="12" fill="#333">OpenCloud</text>
<text x="180" y="138" text-anchor="middle" font-size="10" fill="#666">Dokumente</text>

<rect x="270" y="100" width="120" height="40" fill="none" stroke="#8E44AD" stroke-width="2.5" rx="6"/>
<text x="330" y="125" text-anchor="middle" font-size="12" fill="#333">SOGo</text>
<text x="330" y="138" text-anchor="middle" font-size="10" fill="#666">E-Mail &amp; Groupware</text>

<rect x="420" y="100" width="120" height="40" fill="none" stroke="#8E44AD" stroke-width="2.5" rx="6"/>
<text x="480" y="125" text-anchor="middle" font-size="12" fill="#333">OpenProject</text>
<text x="480" y="138" text-anchor="middle" font-size="10" fill="#666">Projektmgmt</text>

<rect x="570" y="100" width="120" height="40" fill="none" stroke="#8E44AD" stroke-width="2.5" rx="6"/>
<text x="630" y="125" text-anchor="middle" font-size="12" fill="#333">Matrix/Element</text>
<text x="630" y="138" text-anchor="middle" font-size="10" fill="#666">Chat &amp; Kollaboration</text>

<!-- Layer 3: Identity & Deployment -->
<rect x="260" y="170" width="120" height="40" fill="none" stroke="#8E44AD" stroke-width="2.5" rx="6"/>
<text x="320" y="195" text-anchor="middle" font-size="12" fill="#333">Keycloak</text>
<text x="320" y="208" text-anchor="middle" font-size="10" fill="#666">Identity &amp; Auth</text>

<rect x="390" y="170" width="120" height="40" fill="none" stroke="#8E44AD" stroke-width="2.5" rx="6"/>
<text x="450" y="195" text-anchor="middle" font-size="12" fill="#333">SCS</text>
<text x="450" y="208" text-anchor="middle" font-size="10" fill="#666">Sovereign Cloud Stack</text>

<!-- Layer 4: Databases -->
<rect x="210" y="240" width="120" height="40" fill="none" stroke="#8E44AD" stroke-width="2.5" rx="6"/>
<text x="270" y="265" text-anchor="middle" font-size="12" fill="#333">Galera</text>
<text x="270" y="278" text-anchor="middle" font-size="10" fill="#666">MariaDB Cluster</text>

<rect x="340" y="240" width="120" height="40" fill="none" stroke="#8E44AD" stroke-width="2.5" rx="6"/>
<text x="400" y="265" text-anchor="middle" font-size="12" fill="#333">PostgreSQL</text>
<text x="400" y="278" text-anchor="middle" font-size="10" fill="#666">OpenProject DB</text>

<rect x="470" y="240" width="120" height="40" fill="none" stroke="#8E44AD" stroke-width="2.5" rx="6"/>
<text x="530" y="265" text-anchor="middle" font-size="12" fill="#333">Redis</text>
<text x="530" y="278" text-anchor="middle" font-size="10" fill="#666">Cache</text>

<!-- Layer 5: Platform -->
<rect x="280" y="310" width="140" height="40" fill="none" stroke="#8E44AD" stroke-width="2.5" rx="6"/>
<text x="350" y="335" text-anchor="middle" font-size="12" fill="#333">k3s Cluster</text>
<text x="350" y="348" text-anchor="middle" font-size="10" fill="#666">Lightweight Kubernetes</text>

<!-- Arrows: Ausbauchende Verbindungen -->
<!-- Layer 1 -> Layer 2 -->
<path d="M300 80 L180 100" stroke="#8E44AD" stroke-width="2" marker-end="url(#arrow-purple)" stroke-dasharray="4,2"/>
<path d="M350 80 L330 100" stroke="#8E44AD" stroke-width="2" marker-end="url(#arrow-purple)" stroke-dasharray="4,2"/>
<path d="M400 80 L480 100" stroke="#8E44AD" stroke-width="2" marker-end="url(#arrow-purple)" stroke-dasharray="4,2"/>
<path d="M450 80 L630 100" stroke="#8E44AD" stroke-width="2" marker-end="url(#arrow-purple)" stroke-dasharray="4,2"/>

<!-- Layer 2 -> Layer 3 -->
<path d="M180 140 L180 165 L260 170" stroke="#8E44AD" stroke-width="1.5" marker-end="url(#arrow-purple)"/>
<path d="M330 140 L330 165 L320 170" stroke="#8E44AD" stroke-width="1.5" marker-end="url(#arrow-purple)"/>
<path d="M480 140 L480 165 L390 170" stroke="#8E44AD" stroke-width="1.5" marker-end="url(#arrow-purple)"/>
<path d="M630 140 L630 165 L450 170" stroke="#8E44AD" stroke-width="1.5" marker-end="url(#arrow-purple)"/>

<!-- Layer 3 -> Layer 4 -->
<path d="M260 210 L210 240" stroke="#8E44AD" stroke-width="1.5" marker-end="url(#arrow-purple)"/>
<path d="M320 210 L340 240" stroke="#8E44AD" stroke-width="1.5" marker-end="url(#arrow-purple)"/>
<path d="M450 210 L470 240" stroke="#8E44AD" stroke-width="1.5" marker-end="url(#arrow-purple)"/>

<!-- Layer 4 -> Layer 5 -->
<path d="M270 280 L280 310" stroke="#8E44AD" stroke-width="1.5" marker-end="url(#arrow-purple)"/>
<path d="M400 280 L350 310" stroke="#8E44AD" stroke-width="1.5" marker-end="url(#arrow-purple)"/>
<path d="M530 280 L390 310" stroke="#8E44AD" stroke-width="1.5" marker-end="url(#arrow-purple)"/>
</g>
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
