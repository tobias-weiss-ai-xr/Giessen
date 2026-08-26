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
<svg viewBox="0 0 500 200" width="500" height="200" xmlns="http://www.w3.org/2000/svg">
<defs>
<marker id="arrow-blue" viewBox="0 0 12 12" refX="11" refY="6" markerWidth="12" markerHeight="12" orient="auto">
<polygon points="0,0 12,6 0,12 3,6" fill="#007ACC"/>
</marker>
</defs>

<g font-family="Arial">
<!-- Mensch -->
<circle cx="150" cy="100" r="40" fill="none" stroke="#007ACC" stroke-width="3"/>
<circle cx="150" cy="100" r="25" fill="#007ACC" opacity="0.1"/>
<text x="150" y="95" text-anchor="middle" font-size="16" font-weight="bold" fill="#333">Mensch</text>
<text x="150" y="110" text-anchor="middle" font-size="12" fill="#666">Entscheidet</text>

<!-- Agent -->
<rect x="300" y="80" width="80" height="40" fill="none" stroke="#007ACC" stroke-width="3" rx="6"/>
<rect x="315" y="90" width="10" height="10" fill="#007ACC"/>
<rect x="330" y="90" width="10" height="10" fill="#007ACC"/>
<rect x="345" y="90" width="10" height="10" fill="#007ACC"/>
<text x="340" y="105" text-anchor="middle" font-size="16" font-weight="bold" fill="#333">Agent</text>
<text x="340" y="120" text-anchor="middle" font-size="12" fill="#666">Schlägt vor</text>

<!-- Pfeile -->
<path d="M190 100 L280 100" stroke="#007ACC" stroke-width="3" marker-end="url(#arrow-blue)"/>
<text x="235" y="85" text-anchor="middle" font-size="12" fill="#007ACC">kontrolliert</text>

<path d="M340 80 L190 80 L190 70" stroke="#007ACC" stroke-width="2" marker-end="url(#arrow-blue)" stroke-dasharray="5,3"/>
<path d="M190 120 L340 120 L340 130" stroke="#007ACC" stroke-width="2" marker-end="url(#arrow-blue)" stroke-dasharray="5,3"/>
<text x="235" y="135" text-anchor="middle" font-size="12" fill="#007ACC">unterstützt</text>
</g>
</svg>
</div>

**Agenten unterstützen – Menschen entscheiden.**

---

# Architektur

<div class="diagram">
<svg viewBox="0 0 600 300" width="600" height="300" xmlns="http://www.w3.org/2000/svg">
<defs>
<marker id="arrow-green" viewBox="0 0 12 12" refX="11" refY="6" markerWidth="12" markerHeight="12" orient="auto">
<polygon points="0,0 12,6 0,12 3,6" fill="#2E8B57"/>
</marker>
</defs>

<g font-family="Arial">
<!-- OpenDesk Edu -->
<rect x="250" y="40" width="100" height="40" fill="none" stroke="#2E8B57" stroke-width="3" rx="6"/>
<text x="300" y="65" text-anchor="middle" font-size="16" font-weight="bold" fill="#333">OpenDesk Edu</text>

<!-- Application Layer -->
<rect x="80" y="120" width="90" height="35" fill="none" stroke="#2E8B57" stroke-width="2" rx="4"/>
<text x="125" y="142" text-anchor="middle" font-size="12" fill="#333">Dokumente</text>

<rect x="210" y="120" width="90" height="35" fill="none" stroke="#2E8B57" stroke-width="2" rx="4"/>
<text x="255" y="142" text-anchor="middle" font-size="12" fill="#333">Team Orte</text>

<rect x="340" y="120" width="90" height="35" fill="none" stroke="#2E8B57" stroke-width="2" rx="4"/>
<text x="385" y="142" text-anchor="middle" font-size="12" fill="#333">Workflows</text>

<rect x="470" y="120" width="90" height="35" fill="none" stroke="#2E8B57" stroke-width="2" rx="4"/>
<text x="515" y="142" text-anchor="middle" font-size="12" fill="#333">Agenten</text>

<!-- Infrastructure Layer -->
<rect x="250" y="200" width="100" height="35" fill="none" stroke="#2E8B57" stroke-width="2" rx="4"/>
<text x="300" y="222" text-anchor="middle" font-size="12" fill="#333">k3s Cluster</text>

<rect x="250" y="245" width="100" height="35" fill="none" stroke="#2E8B57" stroke-width="2" rx="4"/>
<text x="300" y="267" text-anchor="middle" font-size="12" fill="#333">Sovereign Cloud Stack</text>

<!-- arrows -->
<path d="M300 80 L300 120" stroke="#2E8B57" stroke-width="2.5" marker-end="url(#arrow-green)"/>

<path d="M125 157 L125 180 L250 180 L250 200" stroke="#2E8B57" stroke-width="2" marker-end="url(#arrow-green)" stroke-dasharray="3,2"/>
<path d="M255 157 L255 180 L250 180" stroke="#2E8B57" stroke-width="2" marker-end="url(#arrow-green)" stroke-dasharray="3,2"/>
<path d="M385 157 L385 180 L250 180" stroke="#2E8B57" stroke-width="2" marker-end="url(#arrow-green)" stroke-dasharray="3,2"/>
<path d="M515 157 L515 180 L250 180" stroke="#2E8B57" stroke-width="2" marker-end="url(#arrow-green)" stroke-dasharray="3,2"/>

<path d="M300 235 L300 245" stroke="#2E8B57" stroke-width="2" marker-end="url(#arrow-green)"/>
<text x="300" y="195" text-anchor="middle" font-size="10" fill="#666">läuft auf</text>
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
<svg viewBox="0 0 700 400" width="700" height="400" xmlns="http://www.w3.org/2000/svg">
<defs>
<marker id="arrow-purple" viewBox="0 0 12 12" refX="11" refY="6" markerWidth="12" markerHeight="12" orient="auto">
<polygon points="0,0 12,6 0,12 3,6" fill="#8E44AD"/>
</marker>
</defs>

<g font-family="Arial">
<!-- Layer 1: OpenDesk Edu -->
<rect x="300" y="30" width="100" height="35" fill="none" stroke="#8E44AD" stroke-width="3" rx="6"/>
<text x="350" y="52" text-anchor="middle" font-size="14" font-weight="bold" fill="#333">OpenDesk Edu</text>

<!-- Layer 2: Services -->
<rect x="120" y="90" width="100" height="30" fill="none" stroke="#8E44AD" stroke-width="2" rx="4"/>
<text x="170" y="108" text-anchor="middle" font-size="11" fill="#333">OpenCloud</text>
<text x="170" y="120" text-anchor="middle" font-size="9" fill="#666">Dokumente</text>

<rect x="250" y="90" width="100" height="30" fill="none" stroke="#8E44AD" stroke-width="2" rx="4"/>
<text x="300" y="108" text-anchor="middle" font-size="11" fill="#333">SOGo</text>
<text x="300" y="120" text-anchor="middle" font-size="9" fill="#666">E-Mail & Groupware</text>

<rect x="380" y="90" width="100" height="30" fill="none" stroke="#8E44AD" stroke-width="2" rx="4"/>
<text x="430" y="108" text-anchor="middle" font-size="11" fill="#333">OpenProject</text>
<text x="430" y="120" text-anchor="middle" font-size="9" fill="#666">Projektmgmt</text>

<rect x="510" y="90" width="100" height="30" fill="none" stroke="#8E44AD" stroke-width="2" rx="4"/>
<text x="560" y="108" text-anchor="middle" font-size="11" fill="#333">Matrix/Element</text>
<text x="560" y="120" text-anchor="middle" font-size="9" fill="#666">Chat & Kollaboration</text>

<!-- Layer 3: Identity & Deployment -->
<rect x="260" y="160" width="100" height="30" fill="none" stroke="#8E44AD" stroke-width="2" rx="4"/>
<text x="310" y="178" text-anchor="middle" font-size="11" fill="#333">Keycloak</text>
<text x="310" y="190" text-anchor="middle" font-size="9" fill="#666">Identity & Auth</text>

<rect x="370" y="160" width="100" height="30" fill="none" stroke="#8E44AD" stroke-width="2" rx="4"/>
<text x="420" y="178" text-anchor="middle" font-size="11" fill="#333">Sovereign Cloud Stack</text>

<!-- Layer 4: Databases -->
<rect x="220" y="230" width="100" height="30" fill="none" stroke="#8E44AD" stroke-width="2" rx="4"/>
<text x="270" y="248" text-anchor="middle" font-size="11" fill="#333">Galera</text>
<text x="270" y="260" text-anchor="middle" font-size="9" fill="#666">MariaDB Cluster</text>

<rect x="340" y="230" width="100" height="30" fill="none" stroke="#8E44AD" stroke-width="2" rx="4"/>
<text x="390" y="248" text-anchor="middle" font-size="11" fill="#333">PostgreSQL</text>
<text x="390" y="260" text-anchor="middle" font-size="9" fill="#666">OpenProject DB</text>

<rect x="460" y="230" width="80" height="30" fill="none" stroke="#8E44AD" stroke-width="2" rx="4"/>
<text x="490" y="248" text-anchor="middle" font-size="11" fill="#333">Redis</text>
<text x="490" y="260" text-anchor="middle" font-size="9" fill="#666">Cache</text>

<!-- Layer 5: Platform -->
<rect x="280" y="300" width="140" height="30" fill="none" stroke="#8E44AD" stroke-width="2" rx="4"/>
<text x="350" y="318" text-anchor="middle" font-size="11" fill="#333">k3s Cluster</text>
<text x="350" y="330" text-anchor="middle" font-size="9" fill="#666">Lightweight Kubernetes</text>

<!-- Arrows Layer 1 -> Layer 2 -->
<path d="M350 65 L170 90" stroke="#8E44AD" stroke-width="2" marker-end="url(#arrow-purple)" stroke-dasharray="4,2"/>
<path d="M350 65 L300 90" stroke="#8E44AD" stroke-width="2" marker-end="url(#arrow-purple)" stroke-dasharray="4,2"/>
<path d="M350 65 L430 90" stroke="#8E44AD" stroke-width="2" marker-end="url(#arrow-purple)" stroke-dasharray="4,2"/>
<path d="M350 65 L560 90" stroke="#8E44AD" stroke-width="2" marker-end="url(#arrow-purple)" stroke-dasharray="4,2"/>

<!-- Arrows Layer 2 -> Layer 3 -->
<path d="M220 120 L260 160" stroke="#8E44AD" stroke-width="1.5" marker-end="url(#arrow-purple)"/>
<path d="M350 120 L370 160" stroke="#8E44AD" stroke-width="1.5" marker-end="url(#arrow-purple)"/>
<path d="M480 120 L370 160" stroke="#8E44AD" stroke-width="1.5" marker-end="url(#arrow-purple)"/>

<!-- Arrows Layer 3 -> Layer 4 -->
<path d="M280 190 L220 230" stroke="#8E44AD" stroke-width="1.5" marker-end="url(#arrow-purple)"/>
<path d="M360 190 L340 230" stroke="#8E44AD" stroke-width="1.5" marker-end="url(#arrow-purple)"/>
<path d="M420 190 L390 230" stroke="#8E44AD" stroke-width="1.5" marker-end="url(#arrow-purple)"/>

<!-- Arrows Layer 4 -> Layer 5 -->
<path d="M270 260 L280 300" stroke="#8E44AD" stroke-width="1.5" marker-end="url(#arrow-purple)"/>
<path d="M390 260 L350 300" stroke="#8E44AD" stroke-width="1.5" marker-end="url(#arrow-purple)"/>
<path d="M490 260 L390 300" stroke="#8E44AD" stroke-width="1.5" marker-end="url(#arrow-purple)"/>
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
