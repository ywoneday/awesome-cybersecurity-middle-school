# Teaching Guide

Practical guidance for teaching AP Cybersecurity, based on APSI training materials and educator experience.

## Pacing & Planning

### Default Schedule

The College Board's suggested pacing is based on:
- **45-minute class periods**, 5 days/week
- **Full academic year** (~180 days)

| Unit | Title | Suggested Periods | % of Course |
|---|---|---|---|
| 1 | Introduction to Security | ~10 | 13.3% |
| 2 | Securing Spaces | ~21 | 16.7% |
| 3 | Securing Networks | ~26 | — |
| 4 | Securing Devices | ~23 | — |
| 5 | Securing Applications and Data | ~30 | — |

> **Adjusting for block scheduling:** If you teach 90-minute blocks, the APSI Scope & Sequence template allows you to input your minutes/day and total instructional days to recalculate pacing automatically.

### Planning Tools

| Tool | Description |
|---|---|
| **APSI Scope & Sequence** (xlsx) | Configurable spreadsheet with all units, topics, and learning objectives. Auto-calculates pacing based on your schedule. |
| **2026-2027 APSI Course Planning Suite** (xlsx) | Comprehensive planning suite for the full year. |
| **Unit 1 Calendar/Pacing** (docx) | Day-by-day calendar template for Unit 1. |

---

## Instructional Model

The course uses a consistent **Vulnerability → Protection → Detection** cycle across units 2–5:

1. **Analyze** — Identify vulnerabilities and attack methods (Skill 1)
2. **Mitigate** — Implement protective controls (Skill 2)
3. **Detect** — Monitor systems and analyze evidence (Skill 3)
4. **Collaborate** — Work in teams throughout (Skill 4)

This cycle repeats for each domain (spaces, networks, devices, applications/data), reinforcing the **defense-in-depth** strategy.

---

## Unit Scenarios

Each unit includes authentic **unit scenarios** — real-world cybersecurity situations that connect course content to professional careers. These were developed with AP community teachers.

- **Unit 1 scenarios:** Personal security in everyday life
- **Units 2–5 scenarios:** Common tasks employees perform in cybersecurity jobs

Each scenario is paired with student activities and can be used independently. Teachers can:
- Use one or more scenarios with all students
- Divide scenarios across different student groups

---

## Hands-On Labs

### Lab Sources

| Source | Format | Coverage |
|---|---|---|
| **无锡老师 Labs** | PDF worksheets, 29 lessons across 5 units | All units, multiple lessons per unit |
| **Paradigm Cyber Ventures** | Platform-based labs + facilitation guides | Nmap vulnerability scanning, phone troubleshooting, networking |
| **AP Classroom** | Activity zips with slide decks | Select lessons (1.4, 2.1, 2.3, 3.1, 3.5, 4.1, 4.2, 5.2, 5.4) |
| **Outsmart Cyberthreats** | Interactive collection (NSA/NSF-funded) | Threat actors, defense strategies |

### Lab Distribution by Unit

| Unit | 无锡老师 Labs | AP Classroom Lessons | Paradigm Labs |
|---|---|---|---|
| 1 | 2 lessons | 1.4 Power-Ups | Course Summary |
| 2 | 6 lessons | 2.1, 2.3 | — |
| 3 | 7 lessons | 3.1, 3.5 | Nmap, Phone Troubleshooting |
| 4 | 6 lessons | 4.1, 4.2 | Nmap Vulnerability |
| 5 | 8 lessons | 5.2, 5.4 | CTF Guide |

---

## Assessment Strategy

### Formative Assessment
- **AP Classroom Progress Checks** — topic-level quizzes
- **Unit Reviews** (无锡老师) — 5 review PDFs, one per unit
- **Exit tickets** after each topic

### Summative Assessment
- **Practice Exams** — Student Guide (SG) & Test Bank (TB) versions with MCQ + FRQ
- **AP Exam** — 60 MCQ + 1 FRQ (Device Security Analysis)

### FRQ Preparation

The FRQ is worth 30% of the exam and requires analyzing device security sources. Key preparation strategies:

1. **Practice reading configs** — firewall rules, file permissions, security policies
2. **Practice reading logs** — identify evidence of attacks in log files
3. **Practice citing evidence** — students must reference specific lines/items from sources
4. **Practice the 5 task verbs** — Identify, Explain, Describe, Determine, Write
5. **Use Unit 4 content** as the primary FRQ preparation ground

---

## Recommended Tools Sequence for Middle School

| Phase | Tool | Purpose |
|---|---|---|
| Week 1 | [Have I Been Pwned](https://haveibeenpwned.com/) | Hook: "Are you already compromised?" |
| Unit 1 | [Darknet Diaries](https://darknetdiaries.com/) (selected episodes) | Real-world cybercrime stories |
| Unit 3 | [CyberChef](https://cyberchef.org/) | Network data analysis, encoding/decoding |
| Unit 4 | Paradigm Nmap Lab | Vulnerability scanning hands-on |
| Unit 5 | [Hacksplaining](https://www.hacksplaining.com/lessons) | Web vulnerability demos |
| Unit 5 | [Google Gruyere](https://google-gruyere.appspot.com/) | Hands-on XSS/XSRF exploitation |
| Unit 5 | [Blockchain Hash Demo](https://andersbrownworth.com/blockchain/hash) | Cryptography visualization |
| Ongoing | [picoCTF](https://www.picoctf.org/) | Weekly CTF challenges for engagement |
| Ongoing | [CyberPatriot](https://www.uscyberpatriot.org/) | Team-based OS hardening competition |

---

## AI Integration

The course explicitly addresses AI in both attack and defense contexts (Topics 1.4 and 1.5). Consider:

- Using AI as a **teaching assistant** (Skill 4.C: "Implement AI as a collaboration tool")
- Discussing **AI-powered phishing** and deepfakes (Topic 1.4)
- Exploring **AI-driven threat detection** (Topic 1.5)
- Having students evaluate when AI helps vs. hinders cybersecurity tasks

---

## Tips for Middle School Adaptation

AP Cybersecurity is designed for high school, but many concepts are accessible to motivated middle school students:

1. **Front-load vocabulary** — create a glossary early; cybersecurity has dense terminology
2. **Use stories first** — the AP Cybersecurity Stories PDFs are excellent entry points
3. **Gamify with CTFs** — picoCTF challenges make abstract concepts concrete
4. **Simplify labs** — adapt the 无锡老师 lab worksheets by scaffolding steps more heavily
5. **Focus on the "why"** — before technical details, ensure students understand why security matters
6. **Use comics & media** — xkcd, Darknet Diaries (selected), YouTube videos to maintain engagement
7. **Emphasize personal relevance** — Unit 1 (personal security) is the most relatable for younger students
