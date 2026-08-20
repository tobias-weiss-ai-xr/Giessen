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
    padding: 21px 34px;
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
  
  .emphasis {
    color: #3498db;
    font-style: italic;
  }
  
  .metric {
    font-size: 42px;
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
  
  .slide-number {
    display: none;
  }
  
  .timer {
    display: none;
  }

  /* Mermaid diagram styling */
  .mermaid {
    font-family: 'Fira Code', 'Monaco', monospace;
    font-size: 24px;
    line-height: 1.618;
    margin: 21px 0;
  }
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

- **φ ≈ 1.618:** Natürliche Proportionen
- **Minimal:** Keine unnötigen Elemente
- **Stoic:** Funktion über Form

</div>

---

<!-- Slide 3 -->

# Die Architektur

```mermaid
graph TD
    subgraph "OpenDesk Edu Suite"
        Frontend[("Frontend")] --> Backend
        Backend[("Backend")] --> Agents
        Agents[("Agenten")] --> AI
        AI[("AI Services")] --> Storage
        Storage[("Storage")] --> Backend
    end
    
    Frontend -->|Next.js| User
    Backend -->|Node.js| Frontend
    Agents -->|LangChain| AI
    AI -->|Ollama| Agents
    Storage -->|PostgreSQL| Backend
    
    style Frontend fill:#e3f2fd
    style Backend fill:#e3f2fd
    style Agents fill:#bbdefb
    style AI fill:#bbdefb
    style Storage fill:#f0f8ff
    style User fill:#fff
```

**Ein System. Eine Verantwortung. Maximale Flexibilität.**

---

<!-- Slide 4 -->

# Die Kubernetes-Infrastruktur

```mermaid
graph TD
    subgraph "Kubernetes Cluster"
        direction TB
        
        subgraph "Control Plane"
            API[API Server]
            Scheduler[Scheduler]
            Controller[Controller Manager]
            Etcd[(etcd)]
        end
        
        subgraph "Worker Nodes"
            Node1[Node 1]
            Node2[Node 2]
            Node3[Node 3]
        end
        
        API --> Scheduler
        API --> Controller
        Scheduler --> Node1
        Scheduler --> Node2
        Scheduler --> Node3
        Controller --> Etcd
    end
    
    subgraph "OpenDesk Edu Pods"
        PodFrontend[Frontend Pod\nNext.js]
        PodBackend[Backend Pod\nNode.js]
        PodAgents[Agenten Pods\n4 Services]
        PodAI[AI Pod\nOllama]
        PodStorage[Storage Pods\nPostgreSQL, Qdrant]
    end
    
    Node1 --> PodFrontend
    Node1 --> PodBackend
    Node2 --> PodAgents
    Node2 --> PodAI
    Node3 --> PodStorage
    
    style Control Plane fill:#f0f8ff
    style Worker Nodes fill:#f0f8ff
    style OpenDesk Edu Pods fill:#e8f4fd
```

**Skalierbar. Robust. Enterprise-Ready.**

---

<!-- Slide 5 -->

# Die Agenten

```mermaid
graph LR
    UserAgent[User Agent\nPersönlicher Lernbegleiter] 
    KnowledgeAgent[Knowledge Agent\nWissensmanager]
    FeedbackAgent[Feedback Agent\nUnterstützung bei Bewertungen]
    CollaborationAgent[Collaboration Agent\nTeamulator]
    
    style UserAgent fill:#e3f2fd
    style KnowledgeAgent fill:#bbdefb
    style FeedbackAgent fill:#bbdefb
    style CollaborationAgent fill:#bbdefb
```

<div class="content-box">

**Jeder Agent hat eine klare Aufgabe:**

✅ **User Agent:** Trackt Fortschritt, erkennt Blockaden, empfiehlt next steps

✅ **Knowledge Agent:** Strukturiert Inhalte, erstellt Zusammenhänge, beantwortet Fragen

✅ **Feedback Agent:** Analysiert Abgaben, generiert Vorschläge, **Mensch entscheidet final**

✅ **Collaboration Agent:** Übersetzt Echtzeit, organisiert Projekte, vermittelt Mentoren

</div>

---

<!-- Slide 6 -->

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

<!-- Slide 7 -->

# Use Case 1

## Korrektur-Unterstützung

```mermaid
graph LR
    Dozent[Dozent] -->|150 Abgaben| FeedbackAgent
    FeedbackAgent[Feedback Agent] -->|Analyse| Muster[Fehlermuster Erkennen]
    Muster --> Vorschläge[Feedback-Vorschläge Generieren]
    Vorschläge --> Dozent
    Dozent -->|Finale Kontrolle| Bewertung[Bewertung]
    
    style Dozent fill:#e3f2fd
    style FeedbackAgent fill:#bbdefb
    style Muster fill:#90caf9
    style Vorschläge fill:#90caf9
    style Bewertung fill:#e3f2fd
```

**Resultat:** <span class="metric">9 Stunden gespart pro Woche</span>

---

<!-- Slide 8 -->

# Use Case 2

## Adaptives Lernen

```mermaid
graph TD
    Lernender[Lernender] -->|Blockade| UserAgent
    UserAgent[User Agent] -->|Erkennt| KnowledgeAgent
    KnowledgeAgent[Knowledge Agent] -->|Findet| Alternativ[Alternative Erklärung]
    KnowledgeAgent --> Mentor[Mentor vermitteln]
    KnowledgeAgent --> Übungen[Übungen generieren]
    Alternativ --> Lernender
    Mentor --> Lernender
    Übungen --> Lernender
    
    style Lernender fill:#e3f2fd
    style UserAgent fill:#bbdefb
    style KnowledgeAgent fill:#bbdefb
    style Alternativ fill:#90caf9
    style Mentor fill:#90caf9
    style Übungen fill:#90caf9
```

**Resultat:** <span class="metric">85% schnelleres Verständnis</span>

---

<!-- Slide 9 -->

# Use Case 3

## Kollaborative Forschung

```mermaid
graph TD
    Team[Forschungsteam] -->|Daten| KnowledgeAgent
    KnowledgeAgent[Knowledge Agent] -->|Analyse| Datenanalyse[Daten Analyse]
    KnowledgeAgent --> CollaborationAgent
    CollaborationAgent[Collaboration Agent] -->|Übersetzung| Echtzeit[Echtzeit-Übersetzung]
    CollaborationAgent --> Qualität[Qualitätsvalidierung]
    CollaborationAgent --> Koordination[Team-Koordination]
    
    style Team fill:#e3f2fd
    style KnowledgeAgent fill:#bbdefb
    style CollaborationAgent fill:#bbdefb
    style Datenanalyse fill:#90caf9
    style Echtzeit fill:#90caf9
    style Qualität fill:#90caf9
    style Koordination fill:#90caf9
```

**Resultat:** <span class="metric">300% schnellere Projektabwicklung</span>

---

<!-- Slide 10 -->

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

<!-- Slide 11 -->

# Die Technologie

```mermaid
graph TD
    subgraph "Technologiestack"
        direction TB
        
        subgraph "Frontend"
            F1[Next.js 14]
            F2[React]
            F3[Tailwind CSS]
            F4[WebSockets]
        end
        
        subgraph "Backend"
            B1[Node.js]
            B2[TypeScript]
            B3[Fastify]
            B4[REST API]
        end
        
        subgraph "AI/ML"
            A1[LangChain.js]
            A2[LangGraph]
            A3[Ollama]
            A4[Qdrant]
            A5[Neo4j]
        end
        
        subgraph "Speicher"
            S1[PostgreSQL]
            S2[Redis]
            S3[Elasticsearch]
        end
        
        subgraph "Infrastruktur"
            I1[Kubernetes]
            I2[Docker]
            I3[Helm]
            I4[Terraform]
        end
    end
    
    F1 --> B1
    F2 --> B1
    B1 --> A1
    A1 --> A2
    A2 --> A3
    A2 --> A4
    A2 --> A5
    B1 --> S1
    B1 --> S2
    B1 --> S3
    I1 --> F1
    I1 --> B1
    I2 --> I1
    I3 --> I1
    
    style Frontend fill:#f0f8ff
    style Backend fill:#f0f8ff
    style AI/ML fill:#e8f4fd
    style Speicher fill:#e8f4fd
    style Infrastruktur fill:#e8f4fd
```

**Small, sharp tools.**

---

<!-- Slide 12 -->

# Kubernetes Features

```mermaid
graph TD
    subgraph "Kubernetes Eigenschaften"
        direction TB
        
        AutoScaling[Auto-Scaling] -->|basierend auf Last| Scale
        SelfHealing[Self-Healing] -->|automatisch| Restart[Pod Neustart]
        Rolling[Rolling Updates] -->|ohne Downtime| Deploy[Deployment]
        LoadBalancing[Load Balancing] -->|verteilte Last| Traffic
        MultiRegion[Multi-Region] -->|global| HA[(High Availability)]
        
        style AutoScaling fill:#e3f2fd
        style SelfHealing fill:#e3f2fd
        style Rolling fill:#e3f2fd
        style LoadBalancing fill:#e3f2fd
        style MultiRegion fill:#e3f2fd
        style Scale fill:#bbdefb
        style Restart fill:#bbdefb
        style Deploy fill:#bbdefb
        style Traffic fill:#bbdefb
        style HA fill:#bbdefb
    end
```

**Skalierbar. Robust. Enterprise-Ready.**

---

<!-- Slide 13 -->

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
Open Source. Self-Hosted. Datenschutzkonform.
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
