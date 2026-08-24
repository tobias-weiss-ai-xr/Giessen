---
marp: true
theme: default
footer: 'Tobias Weiss | openDesk Edu | HackyHour Gießen | 26.08.2026 | 12+8 Format'
style: |
  section {
    font-family: 'Segoe UI', 'Helvetica Neue', Arial, sans-serif;
    font-size: 26px;
    line-height: 1.5;
    color: #2c3e50;
    padding: 55px 72px;
  }
  .lead {
    justify-content: center;
    align-items: center;
    text-align: center;
  }
  h1 {
    font-size: 55px;
    color: #2c3e50;
    line-height: 1.12;
    margin: 4px 0 21px 0;
  }
  h2 {
    font-size: 39px;
    color: #3498db;
    line-height: 1.15;
    margin: 13px 0 13px 0;
  }
  h3 {
    font-size: 30px;
    color: #2c3e50;
    margin: 21px 0 13px 0;
  }
  /* Golden-rule accent under headlines — 61.8 % width */
  h1::after {
    content: '';
    display: block;
    width: 38.2%;
    height: 5px;
    border-radius: 3px;
    background: linear-gradient(90deg, #3498db 0%, #2c3e50 100%);
    margin: 13px 0 0 0;
  }
  .lead h1::after {
    margin: 13px auto 0 auto;
  }
  strong { color: #2c3e50; }
  a { color: #3498db; }
  .tag {
    display: inline-block;
    font-size: 13px;
    letter-spacing: 0.14em;
    text-transform: uppercase;
    color: #3498db;
    font-weight: 600;
    margin-bottom: 13px;
  }
  .timer {
    position: absolute;
    bottom: 13px;
    right: 21px;
    background: rgba(255,255,255,0.92);
    padding: 5px 13px;
    border-radius: 34px;
    font-size: 21px;
    font-weight: bold;
    color: #e74c3c;
    border: 1px solid #fde8e8;
  }
  .slide-number {
    position: absolute;
    bottom: 13px;
    left: 21px;
    font-size: 16px;
    color: #95a5a6;
  }
  /* Golden-section splits: 61.8 / 38.2 */
  .split {
    display: grid;
    grid-template-columns: 61.8fr 38.2fr;
    gap: 34px;
    align-items: center;
  }
  .split-flip {
    display: grid;
    grid-template-columns: 38.2fr 61.8fr;
    gap: 34px;
    align-items: center;
  }
  .card {
    background: linear-gradient(160deg, #f8fafc 0%, #edf2f7 100%);
    border: 1px solid #e2e8f0;
    border-radius: 13px;
    padding: 21px 26px;
  }
  .card strong { color: #2c3e50; }
  .goldline {
    width: 61.8%;
    height: 2px;
    background: #e2e8f0;
    border: none;
    margin: 21px 0;
  }
  .muted { color: #7f8c8d; font-size: 21px; }
  blockquote {
    color: #2c3e50;
    border-left: 5px solid #3498db;
    background: #f2f7fb;
    border-radius: 0 13px 13px 0;
    padding: 13px 21px;
    margin: 21px 0 0 0;
  }
  ul { margin: 13px 0; padding-left: 26px; }
  li { margin: 6px 0; }
  table {
    border-collapse: collapse;
    width: 100%;
    margin: 13px 0;
  }
  th, td {
    border: 1px solid #e2e8f0;
    padding: 10px 16px;
    text-align: left;
  }
  th { background: #f2f7fb; color: #2c3e50; }
  /* QR images: shorn of chrome, sized to the golden column */
  img[alt~="qr"] {
    width: 100%;
    max-width: 330px;
    border-radius: 13px;
    box-shadow: 0 13px 34px -13px rgba(44, 62, 80, 0.35);
    justify-self: center;
  }
  .grid-4 {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 21px;
    margin: 21px 0;
  }
  .grid-3 {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 21px;
    margin: 21px 0;
  }
  .hub {
    display: inline-block;
    padding: 13px 34px;
    margin: 13px 0;
  }
---

<!-- _class: lead -->

# **openDesk Edu**
## Vom eigenen k3s-Cluster in den Pilotbetrieb

**Souveräne Hochschul-IT mit offener KI – aufgebaut auf eigener Hardware**

**Tobias Weiß** · DevOps, Uni Marburg
[opendesk-edu.org](https://opendesk-edu.org)

<div class="slide-number">Folie 1 · Titel</div>

---

<div class="tag">Ausgangslage</div>

# **Die digitale Basis an Hochschulen: Microsoft 365**

- **40.000 Studierende** – die digitale Infrastruktur steht fast überall auf **Microsoft 365**
- US-Cloud, Lizenzen pro Nutzer, **steigende Kosten**
- **Die Datenhoheit liegt nicht bei der Hochschule** 🔒

<div class="card">

**Der Rückenwind wächst:**

- 📄 **HBDI-Risikoanalyse zu M365** – Hessischer Beauftragter für Datenschutz
- 🏛️ **Digitalpakt Hessen 2026–2031** – Förderung offener Hochschul-Infrastrukturen

</div>

**Frage: Wie gewinnt eine Uni digitale Souveränität zurück – ohne alles neu zu erfinden?**

<div class="slide-number">Folie 2 · 0:45</div>
<div class="timer">⏰ 0:45–1:45</div>

---

<div class="tag">Die Idee</div>

# **openDesk Edu – offen statt proprietär**

- **openDesk CE** – der quelloffene Digital Workplace des Bundes: BSI-zertifiziert, vom Bund gefördert
- **openDesk Edu** ergänzt, was Hochschulen brauchen: Lernplattformen, Videokonferenzen, Dateien, kollaboratives Arbeiten
- **Baukasten-Prinzip** – Komponenten austauschbar, nichts für die Ewigkeit festgeschrieben
- **Ein Login für alles** – föderierbar mit dem gewohnten Hochschul-Login
- **Ein Befehl** stellt die komplette Umgebung bereit

> Herzstück: quelloffen, eigenbetrieben, datenschutzkonform.

<div class="slide-number">Folie 3 · 1:45</div>
<div class="timer">⏰ 1:45–3:00</div>

---

<div class="tag">Eigene Hardware</div>

# **Der k3s-Cluster auf bare metal**

<div class="split">

<div>

- **K3s** – schlankes Kubernetes, ideal für eigene Plattformen
- **Bare metal:** eigene Server, volle Kontrolle, keine Cloud-Verträge
- Vom **ersten Test-Setup** zur **produktionsnahen Plattform**
- Betrieb am **eigenen Hochschulrechenzentrum**

<p class="goldline"></p>

<p class="muted">Warum k3s? Klein genug zum Verstehen, robust genug zum Betreiben – und 100 % Kubernetes-kompatibel.</p>

</div>

<div class="card">

**Die Reise von null:**  
🖥️ Cluster aufgebaut → 🔧 Dienste deployed → 🔐 Ein Login → 🚦 in Betrieb

</div>

</div>

<div class="slide-number">Folie 4 · 3:00</div>
<div class="timer">⏰ 3:00–4:15</div>

---

<div class="tag">Wie wir gearbeitet haben</div>

# **Aufgesetzt mit KI-Hilfe**

- **KI-Agenten als Co-Piloten:** Konfigurationen und Skripte entworfen, geprüft, iteriert
- **Fehlersuche im Dialog:** Probleme im Cluster untersuchen – Logs lesen, Ursachen finden, Fixes ableiten
- **Schneller lernen:** „Wie geht X in k3s?“ – direkt umsetzen statt stundenlanges Suchen
- **Die Kontrolle bleibt beim Team:** KI schlägt vor, wir entscheiden und verstehen

> Der Cluster steht. Dass er heute steht, haben wir auch kritischer KI-Unterstützung zu verdanken.

<div class="slide-number">Folie 5 · 4:15</div>
<div class="timer">⏰ 4:15–5:30</div>

---

<div class="tag">Digitale Souveränität konkret</div>

# **openDesk für Unis – und für KI – zugänglich**

- **Von der Verwaltung zur Uni:** Bildungs-Services ergänzt – Lehre, Video, Dateien, Zusammenarbeit
- **KI als Baustein:** datenschutzkonforme, **lokale KI-Assistenten** direkt in der Plattform
- **Keine Daten in fremden Clouds** – eigene Infrastruktur, eigene Regeln
- **Ein Login** für Lehre, Forschung, Kommunikation **und KI**

<div class="card">

**Der Unterschied heute → morgen:**  
Heute: fünf Tools, fünf Logins, Daten überall.  
Morgen: **eine Plattform, ein Login, offene KI.**

</div>

<div class="slide-number">Folie 6 · 5:30</div>
<div class="timer">⏰ 5:30–6:45</div>

---

<div class="tag">Status heute</div>

# **Kein Konzept – es läuft**

- Plattform im Betrieb am **Hochschulrechenzentrum**
- Anmeldung mit dem **gewohnten Hochschul-Login**
- **Kontrollierte Updates** – und wenn nötig, sauberer Rollback
- **Monitoring & Absicherung** gehören von Anfang an dazu

<p class="muted">Vom Testsystem in den regulären Betrieb – Schritt für Schritt, nicht im Alleingang.</p>

<div class="slide-number">Folie 7 · 6:45</div>
<div class="timer">⏰ 6:45–7:45</div>

---

<div class="tag">Zielbild</div>

# **Hybrid: nicht alles oder nichts**

<div class="split">

<div class="card">

**Verwaltung & Backoffice**  
Bleibt bei **Microsoft 365** – Bestand, Stabilität, Formate

</div>

<div class="card">

**Staff & Students**  
Arbeiten auf **openDesk Edu** – souverän, offen, mit KI

</div>

</div>

- **Kein Big Bang** – schrittweise umziehen, dort wo es passt
- Pro Anwendung die Frage: **„Was muss souverän laufen?“**

<div class="slide-number">Folie 8 · 7:45</div>
<div class="timer">⏰ 7:45–8:45</div>

---

<div class="tag">Jetzt</div>

# **Langsam in den Pilotbetrieb**

- Vom Test in die **Praxis** – bewusst **langsam und kontrolliert**
- Erste Piloten: **Startups** aus dem regionalen Startup-Ökosystem
- Ggf. an der Hochschule: ein **Fachbereich als Pilot** (z. B. Mathematik)
- **Kleine Gruppen zuerst** – lernen, messen, dann ausrollen

<div class="card">

**Phasen:** Test ✅ → **Pilot ▶️** → gestaffelter Rollout → Betrieb

</div>

<div class="slide-number">Folie 9 · 8:45</div>
<div class="timer">⏰ 8:45–9:45</div>

---

<div class="tag">Warum</div>

# **Warum sich das lohnt**

- 🛡️ **Souveränität** – Daten bleiben im eigenen Rechenzentrum
- 💶 **Stabile Kosten** – eigene Hardware statt wachsender Lizenzen
- 🧩 **Flexibilität** – Module austauschbar, keine Sackgassen
- 🤝 **Gemeinschaft** – offene Software, von vielen getragen

> Souveränität ist kein Luxus – sie wird zum Standortvorteil.

<div class="slide-number">Folie 10 · 9:45</div>
<div class="timer">⏰ 9:45–10:30</div>

---

<div class="tag">Mitmachen</div>

# **Loslegen & mitmachen**

- 🌐 **Website:** [opendesk-edu.org](https://opendesk-edu.org)
- 🐙 **Quellcode:** [github.com/opendesk-edu](https://github.com/opendesk-edu)
- 🗺️ **Landscape:** [landscape.opendesk-edu.org](https://landscape.opendesk-edu.org)
- 🧪 **Eigene Piloten?** Sprecht mich nach dem Vortrag an!

<div class="card">

**Deploy:** Open Source, ein Befehl, Kubernetes – selbst testen, Feedback geben, Issues melden.

</div>

<div class="slide-number">Folie 11 · 10:30</div>
<div class="timer">⏰ 10:30–11:00</div>

---

<div class="tag">Jetzt zählt jede Stimme</div>

# **🗳️ Voting: Open Source Wettbewerb 2026**

<div class="split">

<div>

**Bis 30. September 2026** für openDesk Edu abstimmen – dauert keine 30 Sekunden:

<div class="card">

🔗 **[open-source-wettbewerb.de/voting/opendesk-edu/](https://open-source-wettbewerb.de/voting/opendesk-edu/)**  
📱 **QR-Code scannen**

</div>

</div>

![qr voting-qr.png](voting-qr.png)

</div>

<div class="slide-number">Folie 12 · 11:00</div>
<div class="timer">⏰ 11:00–12:00</div>

---

<div class="tag">Save the date</div>

# **📺 StartMiUp Preisverleihung – Live auf YouTube**

- **StartMiUp Business Model Wettbewerb 2026** – die Preisverleihung als Livestream
- Wir sind Teil des regionalen Startup-Ökosystems – **schaut zu!**

<div class="split">

<div>

🔗 **[youtube.com/live/wMvwufJSCoY](https://www.youtube.com/live/wMvwufJSCoY)**

<p class="goldline"></p>

<p class="muted">StartMiUp · JLU Gießen · Uni Marburg · THM · kofinanziert durch die EU</p>

</div>

![qr preisverleihung-qr.png](preisverleihung-qr.png)

</div>

<div class="slide-number">Folie 13 · Bonus</div>

---

<div class="tag">+8 Minuten</div>

# **❓ Fragen & Diskussion**

<div class="split">

<div>

**Technik:**  
- Warum k3s statt eines großen Kubernetes?  
- Wie hat KI beim Aufsetzen konkret geholfen?  
- Wie datenschutzkonform ist lokale KI (DSGVO)?

</div>

<div>

**Zukunft:**  
- Wie läuft der Pilotbetrieb konkret ab?  
- Wo endet das Hybrid-Modell, wo beginnt MS365?  
- Rollout an anderen Hochschulen?

</div>

</div>

<div class="slide-number">Folie 14 · Q&A</div>

---

<div class="tag">Backup · Konzept</div>

# **Wie es zusammenhängt**

<div style="text-align:center;">

<div class="card hub">
<strong>Ein Login</strong><br/>
<span class="muted">Hochschul-Identität · SSO</span>
</div>

<p class="muted" style="margin: 13px 0;">↓ verbindet ↓</p>

<div class="grid-4">

<div class="card">🎓 **Lehre**<br/><span class="muted">Lernplattformen · Video</span></div>
<div class="card">💬 **Kommunikation**<br/><span class="muted">Mail · Chat</span></div>
<div class="card">📁 **Dateien & Tools**<br/><span class="muted">Cloud · Dokumente</span></div>
<div class="card">🤖 **KI**<br/><span class="muted">lokal · datenschutzkonform</span></div>

</div>

</div>

---

<div class="tag">Backup · Einordnung</div>

# **Viele Einzellösungen → eine Plattform**

| | Heute | openDesk Edu |
|---|---|---|
| **Logins** | viele, getrennt | **einer (SSO)** |
| **Datenlage** | verstreut in Clouds | **im eigenen Rechenzentrum** |
| **Lizenzmodell** | pro Nutzer, steigend | **Open Source** |
| **KI** | externe Dienste | **lokale, offene KI** |
| **Weiterentwicklung** | Hersteller entscheidet | **Baukasten & Community** |

---

<div class="tag">Backup · Phasen</div>

# **Der Weg in den Betrieb**

<div class="grid-3">

<div class="card">✅ **Test**<br/><span class="muted">Machbarkeit · Setup</span></div>
<div class="card">▶️ **Pilot**<br/><span class="muted">Startups · Fachbereich</span></div>
<div class="card">🚀 **Rollout**<br/><span class="muted">gestaffelt · messbar</span></div>

</div>

<p class="muted" style="text-align:center; margin-top: 13px;">→ Betrieb: Monitoring · Updates · Community</p>

---

<div class="tag">Kontakt & Links</div>

# **Kontakt & Links**

- 🌐 **openDesk Edu:** [opendesk-edu.org](https://opendesk-edu.org)
- 🐙 **Quellcode:** [github.com/opendesk-edu/opendesk-edu](https://github.com/opendesk-edu/opendesk-edu)
- 🗺️ **Landscape:** [landscape.opendesk-edu.org](https://landscape.opendesk-edu.org)
- 🌍 **Tobias:** [tobias-weiss.org](https://tobias-weiss.org) · [@opendesk_edu@mastodon.social](https://mastodon.social/@opendesk_edu) · [linkedin.com/in/tobias-weiss](https://linkedin.com/in/tobias-weiss)
- 📧 **Mail:** [tobias.weiss@opendesk-edu.org](mailto:tobias.weiss@opendesk-edu.org)
