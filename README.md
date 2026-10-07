# Madhur Rishi Sikarwar

*Building systems that survive the real world.*

B.E. Information Science at RVCE, class of 2028. I like owning a system end to end: the firmware, the backend, the model, and the screen it all ends up on.

[Email](mailto:madhurrishis.is24@rvce.edu.in) · [LinkedIn](https://www.linkedin.com/in/madhur-sikarwar-025b87342/) · [GitHub](https://github.com/MadhurSikarwar)

---

```cpp
class Developer : public Engineer {
public:
    Developer() {
        name       = "Madhur Rishi Sikarwar";
        education  = "B.E. Information Science @ RVCE (CGPA: 9.37)";
        focus      = {"Embedded Systems", "Machine Learning", "Distributed Systems"};
        philosophy = "Own the system end to end, from firmware to UI.";
    }

    void execute() {
        while (true) { learn(); build(); optimize(); }
    }
};
```

## Now

- Building self-healing ESP32 mesh networks
- Training domain-adapted NLP models (FinBERT)
- Exploring federated learning and smart-contract security
- Polishing **OrbitWatch**, below

---

## Featured

### OrbitWatch: satellite and space-debris tracking with close-approach alerts

A database-systems project at RVCE, built with [Mayur M Deekshith](https://github.com/MayurDeekshith). It keeps a catalogue of 35,000+ space objects, about 32,000 of them with live orbits, and shows them on a 3D globe. Every few hours it screens a watchlist of satellites for close approaches and works out the probability of collision for each one. For the risky ones, an LLM agent plans an avoidance burn, but only from deterministic physics tools, behind guardrails, and a person has to approve it. It then explains its answer twice: in plain words, and in the original technical wording.

- **Data:** MySQL 8.4 with a separate database account per role (viewer, analyst, admin), and a sharded MongoDB (2 shards, 3 replicas each) for orbit history
- **Backend:** Python, Flask, SGP4 orbit propagation, scheduled jobs, live updates over server-sent events
- **Front end:** vanilla ES modules, CesiumJS globe, a time scrubber, ground tracks, a command palette, a clean accessibility audit
- **Quality:** 170 tests, and a mail guard that stops tests from ever reaching a real inbox

[Repository](https://github.com/MadhurSikarwar/GDGSpaceTech) · [Demo video](https://www.youtube.com/watch?v=Be4tBh7HUjg)

---

## Work

### Systems and IoT

| Project | What it does | Built with |
|---|---|---|
| [ResQMesh](https://github.com/Bhavya-Chawat/ResQMesh) | A disaster network that needs no infrastructure. A self-healing ESP32 mesh with a custom Bellman-Ford routing protocol (poison reverse) and a firmware scheduler that sends SOS packets first. | C++, ESP32, React, FastAPI |
| [AeroSense](https://github.com/MadhurSikarwar/IOT_PBL) | Measures how stagnant a room's air is by fitting how fast VOC gas decays after a pulse. Reports air changes per hour and a stagnation score. | ESP32, MQ135, FastAPI, WebSockets |
| [Algal bloom dashboard](https://github.com/MadhurSikarwar/Algal-Bloom-Prediction) | Water-quality sensors (pH, turbidity, TDS, dissolved oxygen) feed a live dashboard that estimates bloom probability, with alerts and PDF/CSV export. | ESP32, ThingSpeak, JavaScript |
| [ECOSAT](https://github.com/MadhurSikarwar/Algal-Bloom-Satellite) | Algal-bloom risk platform that combines a satellite-based model with an offline sensor-based one. | Web |
| [File Integrity Checker](https://github.com/MadhurSikarwar/File-Integrity-Checker) | A desktop security tool with 18 features: baseline snapshots, change detection and a real-time directory watchdog. | C, GTK3, SQLite, OpenSSL |

### AI and data

| Project | What it does | Built with |
|---|---|---|
| [fIndia-AI](https://github.com/thinbearr/fIndia-AI) | FinBERT adapted to Indian financial text. Runs batch inference over headlines and correlates sentiment with live asset prices. | PyTorch, FinBERT, Pandas |
| [TideLine](https://github.com/MadhurSikarwar/SustainX-Hackathon) | Coastal pollution early warning for UN SDG 14. Five signals become one 0 to 100 risk score per hotspot, and Groq agents explain the score but never override it. | React, FastAPI, PostGIS, Groq |
| [Suraksha Intelligence](https://github.com/MadhurSikarwar/Suraksha-Hackathon) | Hackathon project: a multi-modal AI pipeline that checks property title deeds for forgery, aimed at Indian banks. | Python |
| [Cheating detection](https://github.com/MadhurSikarwar/Emotion-Tracking-Hacknite-Hackathon-) | Flags cheating from emotion and eye-movement tracking (Hacknite hackathon). | Python |
| [IntelliReview](https://github.com/MadhurSikarwar/C---Java-Code-Reviewer) | A static analyzer for C, C++ and Java. Control-flow, pointer-state and taint analysis plus ML models; it returns the risky lines, why, the fix and a risk verdict. | Python, pycparser, javalang |

### Developer tools

| Project | What it does | Built with |
|---|---|---|
| [CodeLens](https://github.com/MadhurSikarwar/CodeDebugger) | Records a run of a Python, JavaScript, TypeScript, Java, C or C++ program and animates the stack, heap and pointers. The debugger steps backwards as easily as forwards. | TypeScript, React, gdb, JDI |
| [SecureGraph](https://github.com/MadhurSikarwar/DAA-PBL) | Simulates enterprise cyber-attacks with Dijkstra, Floyd-Warshall and topological sort, and allocates a defence budget with 0/1 knapsack and branch and bound. | Python, React Flow |
| [Downloader](https://github.com/MadhurSikarwar/Downloader) | A desktop video and audio downloader with a Tkinter interface on yt-dlp. | Python |

### Web, games and sound

| Project | What it does | Built with |
|---|---|---|
| [Swaralaya](https://github.com/MadhurSikarwar/Swarlaya-Music) | A practice studio for Indian classical music: real-time pitch shifting in the browser, a C++ (Drogon) service, and Demucs splitting songs into six stems. | C++, Python, Next.js, Web Audio |
| [TOOL](https://github.com/MadhurSikarwar/TOOL) | An audio-reactive 3D visualizer: 80,000 GPU particles and a kaleidoscopic shader driven by live frequency analysis, in six visual modes. | TypeScript, GPU shaders |
| [KRAKEN: Dead Signal](https://github.com/MadhurSikarwar/PromptArcade) | A 2D cyberpunk survival-horror game. Hacking the facility makes noise that draws the octopus hunting you. [Play it](https://prompt-arcade-gilt.vercel.app) | TypeScript, Phaser 3 |
| [Decentralized Election](https://github.com/MadhurSikarwar/DTL-Student-Election-) | An on-chain student election with MetaMask login, anonymous tamper-proof tallying and gas-optimised contracts on Sepolia. | Solidity, Truffle, Ethereum |

Also on my GitHub: data structures practice in C++, C programming, a logic gate simulator, an expense tracker, and IoT lab work.

---

## Stack

```text
languages   C++ · C · Python · Java · TypeScript · JavaScript · SQL · Solidity
embedded    ESP32 · Arduino · sensors · Linux
ml          PyTorch · TensorFlow · scikit-learn · FinBERT · Demucs
data        MySQL · PostgreSQL · MongoDB
web         React · Next.js · FastAPI · Flask · CesiumJS · Phaser
```

---

<sub>Engineering with purpose. Research over hype.</sub>
