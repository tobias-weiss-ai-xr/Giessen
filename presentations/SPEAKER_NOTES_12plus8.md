# 🎤 Speaker Notes: openDesk Edu – Vom k3s-Cluster in den Pilotbetrieb

**Event:** HackyHour Gießen  
**Date:** 26. August 2026  
**Speaker:** Tobias Weiss · DevOps, Uni Marburg  
**Format:** 12 Minuten Vortrag + 8 Minuten Q&A  
**Topic:** Souveräne Hochschul-IT mit offener KI – aufgebaut auf eigenem k3s-Cluster (bare metal), jetzt im Übergang in den Pilotbetrieb

---

## 🎯 **Framing & Ground Rules (wichtig!)**

- **Ehrlich und auf Augenhöhe:** Es geht um die echte Geschichte – eigenes Setup, eigene Erfahrungen. Keine erfundenen Zahlen, keine Werbeclaims.
- **Keine Interna:** Keine Knotenzahlen, keine Pod-Zahlen, keine internen Werkzeuge/Prozesse, keine internen Betriebsdetails. Hohes Niveau halten.
- **Erzählbogen:** Warum (Souveränität) → Idee (openDesk Edu) → Wie (eigene Hardware + KI-Hilfe) → Was heute (läuft am RZ) → Ziel (Hybrid MS365 + openDesk Edu) → Jetzt (Pilotbetrieb) → CTA (Voting).
- **CTA-Hierarchie:** 1 = Voting (bis 30.09.), 2 = Mitmachen/Piloten.

---

## ⏱️ **Timing-Übersicht**

| Folie | Zeit | Inhalt |
|-------|------|--------|
| 1 | 0:00–0:45 | Titel & Einstieg |
| 2 | 0:45–1:45 | Ausgangslage: MS365 & Datenhoheit |
| 3 | 1:45–3:00 | Die Idee: openDesk Edu |
| 4 | 3:00–4:15 | Der k3s-Cluster auf bare metal |
| 5 | 4:15–5:30 | Aufgesetzt mit KI-Hilfe |
| 6 | 5:30–6:45 | openDesk für Unis + KI zugänglich |
| 7 | 6:45–7:45 | Kein Konzept – es läuft |
| 8 | 7:45–8:45 | Zielbild: Hybrid |
| 9 | 8:45–9:45 | Langsam in den Pilotbetrieb |
| 10 | 9:45–10:30 | Warum sich das lohnt |
| 11 | 10:30–11:00 | Mitmachen |
| 12 | 11:00–12:00 | CTA Voting |
| 13–17 | Q&A + Backups | +8 Minuten |

---

# ✅ Detaillierte Notizen pro Folie

---

### Folie 1 · Titel (0:00–0:45)

**Wichtigste Botschaft:** Wer ich bin, worum es geht – in 30 Sekunden.

**Script-Idee:**
> „Hallo! Ich bin Tobias, DevOps an der Uni Marburg. Heute zeige ich euch, wie wir **openDesk Edu** aufgebaut haben – eine souveräne Hochschul-Plattform auf **eigener Hardware (k3s)**, aufgesetzt mit **KI-Hilfe**, und warum wir jetzt langsam in den **Pilotbetrieb** gehen. Zwölf Minuten, danach Fragen. Und am Ende hab ich eine Bitte an euch – mehr dazu später.“

**Delivery:** Ruhig starten, lächeln, Blickkontakt. Kein Fachjargon-Wall.

---

### Folie 2 · Ausgangslage: MS365 & Datenhoheit (0:45–1:45)

**Wichtigste Botschaft:** Hochschulen stehen auf MS365 – mit Preis und Problem: die Datenhoheit liegt nicht bei der Hochschule.

**Script-Idee:**
> „Nehmt eine deutsche Uni: **40.000 Studierende**, tausende Mitarbeitende. Die digitale Basis? Fast überall **Microsoft 365** – Cloud in den USA, Lizenzen pro Nutzer, steigende Kosten. Die **Datenhoheit liegt nicht bei der Hochschule**. Das ist kein Geheimnis – der hessische Datenschutzbeauftragte hat genau dafür eine Risikoanalyse zu M365 veröffentlicht, und der Digitalpakt Hessen fördert ab 2026 offene Hochschul-Infrastrukturen. Die Frage ist also nicht ob, sondern wie. – Wie gewinnt man Souveränität zurück, ohne alles neu zu erfinden?“

**Delivery:** Die Zahlen sind öffentlich (HBDI-Bericht, Digitalpakt Hessen). Keine internen Lizenzdetails.

---

### Folie 3 · Die Idee: openDesk Edu (1:45–3:00)

**Wichtigste Botschaft:** Es gibt schon einen souveränen Digital Workplace vom Bund – wir erweitern ihn für Hochschulen.

**Script-Idee:**
> „Die gute Nachricht: Es gibt bereits **openDesk CE** – den quelloffenen Digital Workplace des Bundes, BSI-zertifiziert, vom Bund gefördert. **openDesk Edu** ergänzt das um das, was Hochschulen brauchen: **Lernplattformen, Videokonferenzen, Dateien, kollaboratives Arbeiten**. Das Ganze als **Baukasten** – Komponenten sind austauschbar. Alles läuft hinter **einem Login**, anbindbar an die gewohnte Hochschul-Welt. Und: **ein Befehl** stellt die komplette Umgebung bereit. Kein Raketenbau – Standard-Werkzeuge, offen zusammengesetzt.“

**Delivery:** „Ein Befehl“ kurz wirken lassen. Keine Liste aller Services abspulen (Detail!).

---

### Folie 4 · Der k3s-Cluster auf bare metal (3:00–4:15)

**Wichtigste Botschaft:** Eigene Hardware, volle Kontrolle – k3s als schlankes Kubernetes.

**Script-Idee:**
> „Basis ist unser **eigener Cluster** – k3s, das schlanke Kubernetes, auf **eigener Hardware (bare metal)**. Keine Cloud-Verträge, keine fremden Rechenzentren: Wir bestimmen, wo die Daten liegen. Gestartet als **kleines Test-Setup**, gewachsen zu einer **produktionsnahen Plattform**, betrieben am **eigenen Hochschulrechenzentrum**. Warum k3s? Klein genug zum Verstehen, robust genug zum Betreiben – und 100 % Kubernetes-kompatibel. Wer selbst einsteigen will: exakt das machen wir auch – ein Cluster, Dienste drauf, ein Login davor.“

**Delivery:** Kurz halten, Begeisterung für das Thema „eigene Infrastruktur“. Keine Zahlen zu Knoten/Hardware (Interna).

---

### Folie 5 · Aufgesetzt mit KI-Hilfe (4:15–5:30)

**Wichtigste Botschaft:** KI-Agenten waren Co-Piloten beim Aufbau – die Kontrolle blieb beim Team. (Ehrliche, echte Geschichte – warum wir das gemacht haben.)

**Script-Idee:**
> „Ehrlich: So ein Cluster ist viel Arbeit. Was uns geholfen hat: **KI-Agenten als Co-Piloten**. Sie haben Konfigurationen und Skripte mitentworfen, geprüft und iteriert. Wenn im Betrieb etwas hakte, haben wir **im Dialog mit KI** die Logs untersucht, Ursachen gefunden, Fixes abgeleitet. Und ganz praktisch: ‚Wie geht X in k3s?‘ – statt stundenlang zu suchen, direkt umsetzen. **Wichtig:** Die KI schlägt vor, **wir entscheiden und verstehen**. Der Cluster steht – und dass er heute steht, haben wir auch kritischer KI-Unterstützung zu verdanken.“

**Delivery:** Hier geht es um echte Erfahrung – gern persönlich erzählen. Nicht behaupten, dass KI „alles allein“ gemacht hätte.

---

### Folie 6 · openDesk für Unis + KI zugänglich (5:30–6:45)

**Wichtigste Botschaft:** openDesk war für Verwaltung gebaut – wir machen ihn für Unis nutzbar, inklusive datenschutzkonformer KI.

**Script-Idee:**
> „openDesk kommt aus der **Verwaltung**. Für Hochschulen fehlte was: **Bildungs-Services** – Lehre, Video, Dateien, Zusammenarbeit – die haben wir ergänzt. Und der Clou: **KI als Baustein**. Datenschutzkonforme, **lokale KI-Assistenten** – direkt in der Plattform, nicht in irgendeiner Cloud. Keine Daten bei Drittanbietern, eigene Infrastruktur, eigene Regeln. **Ein Login** für Lehre, Forschung, Kommunikation **und KI**. Heute: fünf Tools, fünf Logins, Daten überall. Morgen: eine Plattform, ein Login, offene KI.“

**Delivery:** Den Kontrast „heute/morgen“ betonen. Keine internen KI-Dienst-Namen nennen (Detail/Interna).

---

### Folie 7 · Kein Konzept – es läuft (6:45–7:45)

**Wichtigste Botschaft:** Live im Betrieb am Hochschulrechenzentrum – mit gewohntem Login.

**Script-Idee:**
> „Und wichtig: Das ist **kein Konzept – das läuft**. Die Plattform läuft am **Hochschulrechenzentrum**, man meldet sich mit dem **gewohnten Hochschul-Login** an. Updates sind **kontrolliert** – und wenn etwas schiefgeht, gibt es einen sauberen Rollback. Monitoring und Absicherung gehören von Anfang an dazu. Vom Testsystem in den regulären Betrieb – Schritt für Schritt, nicht im Alleingang.“

**Delivery:** „Kein Konzept – es läuft“ ist die Punch-Line der Folie. Kurz und sicher vortragen.

---

### Folie 8 · Zielbild: Hybrid (7:45–8:45)

**Wichtigste Botschaft:** Nicht alles oder nichts – Verwaltung bleibt MS365, Staff & Students wechseln auf openDesk Edu.

**Script-Idee:**
> „Unser Ziel ist **Hybrid** – kein Dogma: Die **Verwaltung und das Backoffice bleiben auf Microsoft 365** – Bestand, Stabilität, gewohnte Formate. **Staff und Students** arbeiten auf **openDesk Edu** – souverän, offen, mit KI. Kein Big Bang, sondern **schrittweise**, dort wo es passt. Pro Anwendung die Frage: **‚Was muss souverän laufen?‘** – und genau die Anwendungen wandern nach und nach um.“

**Delivery:** Hybrid ist die pragmatische Botschaft – kommt bei Administratoren gut an. Klar trennen: „MS365 bleibt“ ist kein Widerspruch.

---

### Folie 9 · Langsam in den Pilotbetrieb (8:45–9:45)

**Wichtigste Botschaft:** Übergang vom Test in die Praxis – bewusst langsam, mit Startups und ggf. einem Fachbereich als Pilot.

**Script-Idee:**
> „Jetzt wird es konkret: Wir gehen **in den Pilotbetrieb**. Bewusst **langsam und kontrolliert** – erst lernen, dann ausrollen. Erste Piloten sind **Startups** aus dem regionalen Startup-Ökosystem. Und ggf. an der Hochschule: ein **Fachbereich als Pilot** – denken wir an Mathematik. **Kleine Gruppen zuerst**, messen, dann Schritt für Schritt mehr Nutzer: Test ✅ → Pilot ▶️ → gestaffelter Rollout → Betrieb.“

**Delivery:** Ehrlich bleiben – „ggf.“ Fachbereich nicht überzeichnen. Konkrete Namen nur nennen, wenn sicher.

---

### Folie 10 · Warum sich das lohnt (9:45–10:30)

**Wichtigste Botschaft:** Souveränität, stabile Kosten, Flexibilität, Gemeinschaft.

**Script-Idee:**
> „Warum machen wir das? **Souveränität**: Daten bleiben im eigenen Rechenzentrum. **Stabile Kosten**: eigene Hardware statt wachsender Lizenzen pro Nutzer. **Flexibilität**: Module austauschbar, keine Sackgassen. Und **Gemeinschaft**: offene Software, von vielen getragen – wir profitieren alle. Souveränität ist kein Luxus – sie wird zum Standortvorteil.“

**Delivery:** Nur echte, öffentlich belegbare Argumente. Keine konkreten Ersparnis-Zahlen nennen (nicht belastbar).

---

### Folie 11 · Mitmachen (10:30–11:00)

**Wichtigste Botschaft:** Quellen sind öffentlich – und wir suchen Piloten.

**Script-Idee:**
> „Alles ist offen: **opendesk-edu.org**, der **Quellcode** auf GitHub, und die **Landscape**-Seite zeigt das ganze Ökosystem. Wer eigene **Piloten** starten will: sprecht mich nach dem Vortrag an. Deploy ist Open Source, ein Befehl, Kubernetes – selbst testen, Feedback geben, Issues melden.“

**Delivery:** Kurz halten – die Folie ist Selbstläufer.

---

### Folie 12 · CTA Voting (11:00–12:00)

**Wichtigste Botschaft:** Bis 30.09. abstimmen – 30 Sekunden, großer Unterschied.

**Script-Idee:**
> „Und jetzt meine Bitte: openDesk Edu ist im **Open Source Wettbewerb 2026** – Community-Voting bis **30. September**. Dauert keine 30 Sekunden: **QR-Code scannen** oder open-source-wettbewerb.de/voting/opendesk-edu/. **Jede Stimme zählt – macht die offene Hochschul-IT sichtbar. Danke!**“

**Delivery:** Das ist der emotionale Höhepunkt. QR zeigen, Zeit geben, ehrlich danken.

---

# ❓ Q&A-Vorbereitung (+8 Minuten)

**Typische Fragen & ehrliche Antwort-Linien:**

- **Warum k3s statt großem Kubernetes?** → Leichtgewichtig, wartbar, kompatibel; für unsere Größenordnung perfekt; bewusst einfach gestartet.
- **Wie hat KI konkret geholfen?** → Konfigurationen/Skripte als Entwürfe, Fehlersuche im Dialog, schnelleres Lernen; Kontrolle blieb beim Team.
- **Datenschutzkonform – wie?** → Eigene Infrastruktur, lokale KI, Daten bleiben im eigenen Rechenzentrum; DSGVO-konform ausgelegt.
- **Wo endet das Hybrid-Modell?** → Verwaltung bleibt MS365; Kriterium pro Anwendung: „Was muss souverän laufen?“ – danach Staffeln.
- **Wie läuft der Pilotbetrieb ab?** → Kleine Gruppen zuerst, messen, dann ausrollen; Startups + ggf. Fachbereich; bewusst langsam.
- **Kosten?** → Eigene Hardware statt Lizenzen; Open Source; keine pauschalen Zahlen versprechen.

**Falls nötig:** Laptop mit laufender Instanz zeigen (wenn verfügbar), sonst ehrlich: „Demo gerne nachher im direkten Gespräch.“

---

# 📋 Checkliste

### 1 Woche vorher
- [ ] Folien + Notizen durchgehen, Timing üben
- [ ] QR-Codes auf Folien 12/13 testen (funktionieren offline-fähig als PNG)
- [ ] Voting-Link einmal selbst durchklicken (open-source-wettbewerb.de/voting/opendesk-edu/)

### 1 Tag vorher
- [ ] HTML + PDF final gebaut (marp), beide auf Laptop + USB-Stick
- [ ] Laptop/Clicker laden, Beamer/HDMI prüfen
- [ ] Faktencheck: nur belegbare Aussagen im Vortrag, keine Interna

### 5 Minuten vorher
- [ ] Folien im Browser geöffnet (HTML offline-fähig)
- [ ] PDF als Backup griffbereit
- [ ] Handy stumm, Timer bereit

### Nach dem Talk
- [ ] Fragen nachgehen, Kontakte einsammeln
- [ ] Links (Folien, Quellen) teilen
- [ ] Feedback für nächste Runde notieren

---

## 💬 **Mindset**
Du erzählst eine echte Geschichte – eigene Hardware, KI als Co-Pilot, der Weg in den Pilotbetrieb. Das Publikum will lernen, wie ihr es gemacht habt. Trau deiner Erfahrung, bleib auf Augenhöhe, und mach am Ende eine klare Bitte: **abstimmen!**
