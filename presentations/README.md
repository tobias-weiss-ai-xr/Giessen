# Presentations – HackyHour Gießen

This directory contains presentation slides for HackyHour Gießen events.

---

## 🎤 Current Presentation: OpenDesk Edu (12+8 Format)

**📅 Date:** 26. August 2026  
**👤 Speaker:** Tobias Weiss  
**📍 Event:** HackyHour Gießen at Makerspace Gießen  
**⏱️ Format:** 12 minutes presentation + 8 minutes Q&A  
**🎯 Topic:** OpenDesk Edu – Agentic Engineering in der Praxis  
**🔗 Live Link:** [Slides ✨](/presentations/opendesk_edu_12plus8.html)

---

## 🎨 Design Philosophy

### UNIX Philosophy:
- Do one thing and do it well
- Small, sharp tools
- Compose small programs into larger ones
- Less is more

### Stoic Philosophy:
- Clear, direct, honest
- No unnecessary elements
- Focus on function over form
- Timeless simplicity

### Golden Ratio (φ ≈ 1.618):
- Natural proportions in layout
- Balanced spacing and sizing
- Harmonic visual hierarchy

---

## 📁 Files

| File | Purpose | Size |
|------|---------|------|
| `opendesk_edu_12plus8.md` | Marp source – Edit this! | 8KB |
| `opendesk_edu_12plus8.html` | Browser-ready | 210KB |
| `opendesk_edu_12plus8.pdf` | Printable version | 155KB |
| `SPEAKER_NOTES_12plus8.md` | Minimal speaker script | 8KB |
| `CHEAT_SHEET.md` | Quick reference | 5KB |
| `LEGAL_CONSIDERATIONS.md` | EU AI Act compliance notes | 14KB |
| `diagrams/` | Mermaid SVG diagrams | 7 files |
| `README.md` | This file | 4KB |

---

## 🎯 Presentation Structure: 12+8 Format

### 12 Minutes – Core Content:

| Time | Slide | Topic | Philosophy |
|------|-------|-------|------------|
| 0:00-0:30 | 1 | Title | Minimal |
| 0:30-1:30 | 2 | Konzept & Philosophie | UNIX + Golden Ratio |
| 1:30-2:30 | 3 | Architektur (SVG) | Simple, clear |
| 2:30-3:00 | 4 | Kubernetes-Infrastruktur | Enterprise-ready |
| 3:00-4:00 | 5 | Die vier Agenten | One thing per agent |
| 4:00-4:30 | 6 | Das Problem | Direct, honest |
| 4:30-6:00 | 7 | Use Case 1: Korrektur | Assisted, not automated |
| 6:00-7:30 | 8 | Use Case 2: Lernen | Adaptive support |
| 7:30-8:30 | 9 | Use Case 3: Forschung | Collaboration |
| 8:30-9:00 | 10 | Technologie-Stack | Small, sharp tools |
| 9:00-10:00 | 11 | Kubernetes Features | Enterprise-ready |
| 10:00-11:00 | 12 | Mitmachen | Simple, direct |
| 11:00-12:00 | 13 | Abstimmen | Clear CTA |

### +8 Minutes – Q&A:
- Open discussion
- Legal questions (see LEGAL_CONSIDERATIONS.md)
- Technical deep dives
- Future vision

---

## ⚖️ Legal Compliance Notes

### EU AI Act – Article 6 Abs. 2 i.V.m. Anhang III Nr. 3(b)
- **Assessment of learning outcomes = HIGH RISK**
- **Fully automated grading = Not possible**
- **Assisted grading = Possible with human oversight**

### Presentation Adjustments:
- ✅ "Feedback Agent" replaces "Assessment Agent"
- ✅ "Unterstützung" (support) not "Automatisch" (automatic)
- ✅ "Mensch entscheidet final" (human has final control)
- ✅ Metrics framed as **potential**, not measured results
- ✅ Focus on content creation, learning support, collaboration

### Key Resources:
- [EU AI Act Service Desk – Education](https://ai-act-service-desk.ec.europa.eu/en/education-and-vocational-training)
- [Art. 6 Abs. 2 i.V.m. Anhang III Nr. 3(b) AI Act](https://artificialintelligenceact.eu/)

---

## 🚀 Quick Start

### Viewing:
- 🌐 **HTML:** Open `opendesk_edu_12plus8.html` in any browser
- 📄 **PDF:** Open `opendesk_edu_12plus8.pdf` in any PDF viewer
- 📝 **Source:** Edit `opendesk_edu_12plus8.md` with any text editor

### Editing:
```bash
# Install Marp CLI
npm install -g @marp-team/marp-cli

# Convert to HTML
marp opendesk_edu_12plus8.md -o opendesk_edu_12plus8.html

# Convert to PDF (allow local files for SVG diagrams)
marp opendesk_edu_12plus8.md -o opendesk_edu_12plus8.pdf --pdf --allow-local-files
```

### Regenerating Diagrams:
```bash
# Install Mermaid CLI
npm install -g @mermaid-js/mermaid-cli

# Regenerate SVGs
cd diagrams
for f in *.mmd; do
  mmdc -i "$f" -o "${f%.mmd}.svg" -b transparent -t neutral
done
```

---

## 📊 Key Points (Honest Framing)

**Important:** The following are **projections of potential**, not measured results:

| Use Case | Problem | Potential |
|----------|---------|-----------|
| Korrektur | 10h/Woche manueller Aufwand | Deutliche Zeitersparnis (assistiert) |
| Lernverständnis | 3h Frust bei Konzepten | Schnelleres Verständnis durch personalisierte Pfade |
| Forschung | 4 Monate Koordination | Beschleunigte Abwicklung, internationale Teams |

**No pilot studies have been conducted. No institutional affiliations claimed.**

---

## 🗳️ Voting Information

### The Ask:
Support OpenDesk Edu in the **Open Source Wettbewerb 2026**

### How:
- **QR Code:** Scan with phone camera
- **URL:** [https://open-source-wettbewerb.de/voting/opendesk-edu/](https://open-source-wettbewerb.de/voting/opendesk-edu/)
- **Time:** Takes less than 30 seconds

---

## 🔗 Related Links

### Presentation:
- [Slides (HTML)](/presentations/opendesk_edu_12plus8.html)
- [Slides (PDF)](/presentations/opendesk_edu_12plus8.pdf)
- [Source (MD)](/presentations/opendesk_edu_12plus8.md)

### OpenDesk Edu:
- [Website](https://opendesk-edu.org/)
- [GitHub](https://github.com/opendesk-edu)
- [Discord](https://discord.gg/opendesk)

### Event:
- [HackyHour Gießen GitHub](https://github.com/tobias-weiss-ai-xr/HackyHourGiessen)

---

## 📝 Version History

| Date | Version | Changes |
|------|---------|---------|
| 23.08.2026 | 3.0.0 | Replaced Mermaid text with SVG diagrams (fixes rendering) |
| 23.08.2026 | 2.0.0 | UNIX + Stoic + Golden Ratio philosophy, removed false claims |
| 23.08.2026 | 1.0.0 | Initial 12+8 format presentation |

---

## ✨ Philosophy Statement

> **"Einfach. Mächtig. Offen."**
>
> OpenDesk Edu verkörpert drei zeitlose Prinzipien:
>
> **UNIX:** Do one thing and do it well. Jeder Agent hat eine klare Aufgabe.
>
> **Stoic:** Klarheit und Ehrlichkeit. Kein Marketing-Geschwafel. Nur Fakten und funktionierende Technologie.
>
> **Golden Ratio:** Natürliche Schönheit durch Proportionen. Funktionelles Design, das angenehm für das Auge ist.

---

**🚀 Ready to present. Keep it simple. Keep it honest. Keep it powerful.**
