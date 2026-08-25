# Presentations – HackyHour Gießen

This directory contains presentation slides for HackyHour Gießen events.

---

## 🎤 **Current Presentation: openDesk Edu (12+8 Format)**

**📅 Date:** 26. August 2026  
**👤 Speaker:** Tobias Weiss (DevOps, Uni Marburg)  
**📍 Event:** HackyHour Gießen at Makerspace Gießen  
**⏱️ Format:** **12 minutes presentation + 8 minutes Q&A**  
**🎯 Topic:** Souveräne Hochschul-IT mit offener KI – aufgebaut auf eigenem k3s-Cluster (bare metal), mit KI-Hilfe aufgesetzt, jetzt im Übergang in den Pilotbetrieb; Zielbild: **Hybrid** (Verwaltung bleibt MS365 · Staff & Students wechseln auf openDesk Edu)  
**🔗 Live Link:** [Slides ✨](/presentations/opendesk_edu_12plus8.html)

---

## 📁 **Files**

| File | Purpose | Size |
|------|---------|------|
| [`opendesk_edu_12plus8.md`](opendesk_edu_12plus8.md) | **Marp source** – Edit this! | 13KB |
| [`opendesk_edu_12plus8.html`](opendesk_edu_12plus8.html) | **Browser-ready** – Open in any browser | ~175KB |
| [`opendesk_edu_12plus8.pdf`](opendesk_edu_12plus8.pdf) | **Printable** – For handouts or offline viewing | ~360KB |
| [`SPEAKER_NOTES_12plus8.md`](SPEAKER_NOTES_12plus8.md) | **Script & Timing** – Story + Delivery-Tipps | 13KB |
| [`CHEAT_SHEET.md`](CHEAT_SHEET.md) | **Quick reference** – On-stage cheat sheet | 5KB |
| [`voting-qr.png`](voting-qr.png) | **Offline QR** – Voting (Folie 12) | 3KB |

---

## 🎯 **12+8 Format Explained**

### **Why 12+8?**
- **12 minutes:** Tight, high-impact, story-driven presentation
- **+8 minutes:** Flexible Q&A, discussion, and audience interaction

### **Structure (Story-Arc, hohes Niveau, keine Interna):**
1. **Ausgangslage (0:00–1:45)** – MS365, US-Cloud, Datenhoheit nicht an der Hochschule
2. **Idee (1:45–3:00)** – openDesk Edu = openDesk CE (quelloffen, BSI-zertifiziert) + Bildungs-Services + offene KI
3. **Wie (3:00–6:45)** – eigener k3s-Cluster auf bare metal, mit KI-Hilfe aufgesetzt; für Unis + KI zugänglich gemacht
4. **Status (6:45–7:45)** – läuft am Hochschulrechenzentrum ("Kein Konzept – es läuft")
5. **Ziel (7:45–8:45)** – Hybrid: Verwaltung MS365 · Staff & Students openDesk Edu
6. **Jetzt (8:45–11:00)** – langsamer Pilotbetrieb (Startups · ggf. Fachbereich), Gründe, Mitmachen
7. **CTA (11:00–12:00)** – **VOTING** (Open Source Wettbewerb, bis 30.09.)

---

## ⚡ **Quick Start**

### **Viewing:**
- 🌐 **HTML:** Open `opendesk_edu_12plus8.html` in any browser
- 📄 **PDF:** Open `opendesk_edu_12plus8.pdf` in any PDF viewer
- 📝 **Source:** Edit `opendesk_edu_12plus8.md` with any text editor

### **Editing:**

```bash
# Install Marp CLI globally
npm install -g @marp-team/marp-cli

# Convert to HTML
marp opendesk_edu_12plus8.md -o opendesk_edu_12plus8.html

# Convert to PDF
marp --pdf --allow-local-files opendesk_edu_12plus8.md -o opendesk_edu_12plus8.pdf

# As slide images (for review):
marp opendesk_edu_12plus8.md --images png -o .preview/preview.png
```

### **Presenting:**
- Use **arrow keys** or **clicker** to navigate
- **Space bar** also advances slides
- **ESC** to exit fullscreen
- **O** to overview all slides

---

## 📊 **Slide Overview (12 Main + Q&A + Backups)**

### **🎯 Core Presentation (12 slides – 12 minutes):**

| # | Slide | Time | Topic | Key Message |
|---|-------|------|-------|-------------|
| 1 | **Title** | 0:00–0:45 | openDesk Edu | Vom k3s-Cluster in den Pilotbetrieb |
| 2 | **Ausgangslage** | 0:45–1:45 | MS365 & Datenhoheit | 40.000 Studierende · US-Cloud · HBDI/Digitalpakt Hessen |
| 3 | **Idee** | 1:45–3:00 | openDesk Edu | openDesk CE (BSI) + Bildungs-Services · Baukasten · ein Login |
| 4 | **Cluster** | 3:00–4:15 | k3s auf bare metal | eigene Hardware, volle Kontrolle |
| 5 | **KI-Hilfe** | 4:15–5:30 | Aufgesetzt mit KI | KI-Agenten als Co-Piloten, Kontrolle beim Team |
| 6 | **Zugänglich** | 5:30–6:45 | Für Unis + KI | Bildungs-Services + lokale, datenschutzkonforme KI |
| 7 | **Status** | 6:45–7:45 | Läuft am RZ | Kein Konzept – es läuft |
| 8 | **Zielbild** | 7:45–8:45 | Hybrid | Verwaltung MS365 · Staff & Students openDesk Edu |
| 9 | **Pilotbetrieb** | 8:45–9:45 | Jetzt | Startups · ggf. Fachbereich (Mathematik) · kleine Gruppen |
| 10 | **Warum** | 9:45–10:30 | Gründe | Souveränität · stabile Kosten · Flexibilität · Community |
| 11 | **Mitmachen** | 10:30–11:00 | Ressourcen | Website · GitHub · Landscape · Piloten |
| 12 | **🎯 VOTING CTA** | 11:00–12:00 | Call to Action | **QR (voting-qr.png) + Link** · bis 30.09. |
| 13 | **❓ Q&A** | +8 Minuten | Fragen & Diskussion – Technik, Datenschutz, Hybrid, Pilotbetrieb |

### **📦 Backup Slides (if time permits):**
- **Slide 14:** Konzeptbild – ein Login verbindet Lehre · Kommunikation · Dateien · KI
- **Slide 15:** Einordnung – viele Einzellösungen → eine Plattform
- **Slide 16:** Phasen – Test → Pilot → Rollout → Betrieb
- **Slide 17:** Kontakt & Links

---

## 🎯 **Content Highlights (die echte Geschichte – keine erfundenen Zahlen)**

### **🔥 Der Erzählbogen:**
1. **Problem:** Hochschulen stehen auf MS365 – US-Cloud, steigende Lizenzen, Datenhoheit nicht an der Hochschule (belegt: HBDI-Risikoanalyse M365, Digitalpakt Hessen 2026–2031)
2. **Idee:** openDesk Edu – der quelloffene, BSI-zertifizierte Digital Workplace des Bundes (openDesk CE) + Bildungs-Services + lokale, datenschutzkonforme KI; Baukasten, ein Login, ein Befehl deployt alles
3. **Wie:** eigener k3s-Cluster auf bare metal, im Betrieb am Hochschulrechenzentrum; aufgesetzt **mit KI-Hilfe** (KI-Agenten als Co-Piloten bei Konfiguration & Fehlersuche – Entscheidungskontrolle beim Team)
4. **Ziel:** Hybrid – Verwaltung/Backoffice bleibt MS365, Staff & Students arbeiten auf openDesk Edu; kein Big Bang
5. **Jetzt:** langsamer, kontrollierter **Pilotbetrieb** – erste Piloten: Startups aus dem regionalen Ökosystem; ggf. ein Fachbereich (z. B. Mathematik); kleine Gruppen → gestaffelter Rollout

**Grundsatz:** Der Vortrag bleibt bewusst auf hohem Niveau – **keine internen Details** (keine Knoten-/Pod-Zahlen, keine internen Werkzeuge, keine internen Prozesse). Alles Gesagte ist öffentlich belegbar.

---

## 🎤 **Presenting Tips**

### **Timing:**
- **Start strong** – Grab attention in the first 30 seconds
- **Watch the clock** – Aim for **Slide 12 (Voting) by minute 11:00**
- **End on time** – respect the audience
- **Leave buffer** – 30 seconds for transitions

### **Delivery:**
- **Make eye contact** – connect with individuals
- **Vary your voice** – avoid monotony
- **Pause after the punch lines** – "Kein Konzept – es läuft", "ein Login für alles"
- **Be honest** – if unsure, say so; never invent numbers

### **Handling Q&A:**
- **Repeat the question** – gives you time to think
- **"Good question!"** – always positive
- **Bridge to your message** – "Daran arbeiten wir aktiv…"
- **Interna-Fragen** – freundlich abgrenzen: "Dazu halten wir Details bewusst privat – gern im Gespräch dazu"

---

## 🗣️ **Key Phrases to Remember**

### **Transitions:**
- "Nehmt eine deutsche Uni – 40.000 Studierende…" → Ausgangslage
- "Die gute Nachricht: Es gibt schon openDesk CE…" → Idee
- "Basis ist unser eigener Cluster…" → Technik
- "Ehrlich: viel Arbeit – KI-Agenten waren Co-Piloten…" → KI-Hilfe
- "Und wichtig: Das ist **kein Konzept – es läuft**." → Status
- "Unser Ziel ist Hybrid – kein Dogma…" → Zielbild
- "Jetzt wird es konkret: in den Pilotbetrieb…" → Pilot
- "Und jetzt meine Bitte…" → Voting

### **Call to Action:**
- "**Bis 30. September abstimmen** – open-source-wettbewerb.de/voting/opendesk-edu/"
- "Jede Stimme macht offene Hochschul-IT sichtbar."
- "Eigene Piloten? Sprecht mich an!"

---

## 🗳️ **Voting Information**

### **The Ask:**
Support OpenDesk Edu in the **Open Source Wettbewerb 2026** (Community-Voting; 65 Projekte)

### **How:**
- **QR Code:** local PNG `voting-qr.png` on Folie 12 (offline-fähig)
- **URL:** [https://open-source-wettbewerb.de/voting/opendesk-edu/](https://open-source-wettbewerb.de/voting/opendesk-edu/)
- **Deadline:** **30. September 2026**
- **Time:** Takes less than 30 seconds

### **Why It Matters:**
- **Visibility** – more recognition for the project
- **Credibility** – validation from the community
- **Community** – strengthens open source in education
## 📋 **Preparation Checklist**

### **📁 Files:**
- [ ] `opendesk_edu_12plus8.html` – Main presentation (browsers)
- [ ] `opendesk_edu_12plus8.pdf` – Backup (print/offline)
- [ ] `opendesk_edu_12plus8.md` – Source (editing)
- [ ] `SPEAKER_NOTES_12plus8.md` – Script & timing
- [ ] `CHEAT_SHEET.md` – Quick reference
- [ ] `voting-qr.png` – Offline QR für Voting (Folie 12)

### **💻 Technology:**
- [ ] Laptop charged (>50%)
- [ ] Presentation tested in browser (offline capable)
- [ ] PDF backup on desktop
- [ ] Clicker tested
- [ ] HDMI adapter (if needed)
- [ ] USB stick with all files (backup)

### **📱 On Your Phone:**
- [ ] QR code for voting ready (slides + phone backup)
- [ ] Timer/stopwatch app
- [ ] Silent mode enabled

### **🧠 Mental Prep:**
- [ ] Review speaker notes
- [ ] Practice timing (aim for Slide 12 by 11:00)
- [ ] Faktencheck: nur belegbare Aussagen, keine Interna
- [ ] Prepare answers for likely questions (see speaker notes)

---

## 🎨 **Aesthetic & Design Features (Golden Ratio)**

- **Color Scheme:** Professionelle Blau-Palette (#2c3e50, #3498db) – konsistent mit QR-Codes
- **Typography:** Fibonacci-basierte Schriftskala (26 / 30 / 39 / 55 px), Segoe UI / Helvetica Neue
- **Layout:** **Goldener Schnitt** – Zwei-Spalten-Splits 61.8 %/38.2 %, Akzentlinie unter Headlines bei 38.2 %, Fokus auf goldenen Punkten (0.382/0.618), Fibonacci-Abstände
- **Icons:** Emoji für visuelle Betonung
- **Diagrams:** HTML/CSS-Boxen (kein Mermaid) – volle Kontrolle über Komposition
- **QR-Codes:** lokale PNGs, weiche Schatten, im goldenen Split platziert

---

## 🔗 **Related Links**

### **Presentation:**
- [Slides (HTML)](/presentations/opendesk_edu_12plus8.html)
- [Slides (PDF)](/presentations/opendesk_edu_12plus8.pdf)
- [Source (MD)](/presentations/opendesk_edu_12plus8.md)

### **OpenDesk Edu:**
- [Website](https://opendesk-edu.org/)
- [GitHub](https://github.com/opendesk-edu/opendesk-edu)
- [Landscape (Ecosystem Map)](https://landscape.opendesk-edu.org/)

### **HackyHour Gießen:**
- [Website](https://hackyhour.github.io/Giessen/)
- [GitLab (Orga & Notes)](https://gitlab.ub.uni-giessen.de/hackyhour-team/hackyhour-giessen-orga)

### **Voting:**
- [Open Source Wettbewerb 2026](https://open-source-wettbewerb.de/voting/opendesk-edu/)

---

## 📝 **Version History**

| Date | Version | Changes |
|------|---------|---------|
| 26.08.2026 | 1.0.0 | Initial 12+8 format presentation |
| 23.08.2026 | **1.1.0** | Offline QR-PNGs (Voting), Bonus-Folie |
| 24.08.2026 | **2.0.0** | **Content-Refactor:** ehrliche, belegbare Story statt erfundener Kennzahlen; neuer Erzählbogen (MS365 → openDesk Edu → k3s-Cluster mit KI-Hilfe → Hybrid-Zielbild → Pilotbetrieb); Golden-Ratio-Design; Notizen & Cheat Sheet komplett überarbeitet |
| 24.08.2026 | **2.0.1** | Bonus-Folie + zugehöriges QR-PNG entfernt (Termin lag vor dem Talk); Deck jetzt 17 Seiten |

---

## 🎉 **You're Ready!**

Your presentation is:
- ✅ **Perfectly timed** for 12+8 minutes
- ✅ **Story-driven** – a real journey, told honestly
- ✅ **No fabricated claims** – everything said is publicly verifiable
- ✅ **High-level** – no internal details, no internals
- ✅ **Aesthetically composed** – golden-ratio layout, consistent palette
- ✅ **Practical** – clear CTA (voting until 30.09.)
- ✅ **Available in 3 formats** (MD, HTML, PDF) with offline QR codes

**🚀 Jetzt den Talk halten – und (bis 30.09.) Stimmen sammeln!**

---

---

*Last updated: 24. August 2026*
