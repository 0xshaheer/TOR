# TOR
 Dark Web Forensics – Artifact Analysis and Anti-Forensics Investigation   Explores Tor-based dark web activity, RAM acquisition, and forensic artifact analysis. Detects anti-forensic techniques like memory wiping and hidden processes using tools such as FTK Imager, Bulk Extractor, Volatility, and Netstat.

# Dark Web Forensics – Artifact Analysis and Anti-Forensics Investigation

**Name:** Shaheer Ahmad  
**Submission Date:** 30 June 2025  

---

## 📖 Introduction
This project explores dark web activities using the Tor Browser and applies forensic techniques to analyze captured memory artifacts. The goal is to detect anti-forensic behaviors and uncover digital traces left behind by obfuscation methods.

---

## 🛠️ Tools Used & Justification

| Tool              | Purpose |
|-------------------|---------|
| Tor Browser       | Anonymous browsing of dark web websites |
| FTK Imager / Belkasoft | RAM acquisition from live system |
| WinPrefetchView   | Analysis of `.pf` files to detect Tor activity |
| Netstat (CMD)     | Identify live connections linked to Tor sessions |
| Bulk Extractor    | Extract hidden/cached PII and evidence from RAM |
| Volatility (optional) | Deeper memory structure analysis |

---

## 🔍 Tor Browser Setup & Observations
- Installed on a Windows VM (1 GB RAM).
- Visited directories/search engines: **Ahmia**, **Hidden Wiki**, **Torch**, **Excavator**.
- Searched for *“Hacker for Hire”* and browsed illicit-themed onion sites.  
⚠️ No personal data was shared; all interactions were observational only.

---

## 💾 RAM Acquisition Process
- After closing Tor, **FTK Imager** acquired a full memory dump.
- Output file: `tor_session.mem`.

---

## 🧪 Memory Analysis
- **Bulk Extractor** revealed:
  - `.onion` domains
  - Email addresses
  - Strings resembling credit card numbers
- **Volatility** (optional) showed hidden processes linked to obfuscation.

---

## 🚨 Detection of Anti-Forensic Behavior
- No browser history present.
- Zeroed-out memory patterns.
- Hidden/terminated Tor process detected.
- Indicates obfuscation attempts.

---

## ⏱️ Timeline of Events

| Time     | Event |
|----------|-------|
| 4:00 PM  | VM Booted, Tor Installed |
| 4:30 PM  | Browsing dark web |
| 5:00 PM  | Tor closed, RAM acquired |
| 5:15 PM  | Prefetch & netstat analysis |
| 6:00 PM  | RAM analysis via Bulk Extractor |

---

## ⚡ Challenges & Mitigation

| Challenge | Solution |
|-----------|----------|
| Slow VM performance | Increased RAM to 1.5 GB |
| Onion sites not loading | Switched directories |
| FTK Imager freezing | Used Belkasoft RAM Capturer |
| Misleading artifacts | Filtered by time/process |

---

## ✅ Conclusion
This project provided hands-on experience in dark web browsing behavior, forensic acquisition, and evidence extraction. It highlighted how attackers use anti-forensic techniques like memory wiping and browser history obfuscation.

---

## 📚 References
- [Tor Project](https://www.torproject.org/)  
- [FTK Imager](https://accessdata.com)  
- [Bulk Extractor](https://digitalcorpora.org)  
- [Volatility Framework](https://www.volatilityfoundation.org)  
- [WinPrefetchView](https://www.nirsoft.net)  
