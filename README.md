<div align="center">

# nomu

<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&size=15&duration=3000&pause=900&color=888888&center=true&vCenter=true&width=560&lines=agents+%C2%B7+trust+%C2%B7+local+ai;small+weird+software+that+probably+didn't+need+to+exist;currently%3A+teaching+agents+who+not+to+believe" alt="typing animation" />

<a href="https://create.withdots.studio"><img src="https://img.shields.io/badge/portfolio-111111?style=flat-square&logo=safari&logoColor=white" alt="portfolio"></a>
<a href="https://linkedin.com/in/akumanomu"><img src="https://img.shields.io/badge/linkedin-111111?style=flat-square&logo=linkedin&logoColor=white" alt="linkedin"></a>
<a href="mailto:akumanomu@proton.me"><img src="https://img.shields.io/badge/email-111111?style=flat-square&logo=protonmail&logoColor=white" alt="email"></a>

</div>

<br>

```console
$ whoami
nomu
├─ ai student ............ pavia · unimi · milano-bicocca
├─ software developer
├─ olympiad coach
├─ occasional rust victim
└─ based in algiers
```

I build where **AI, systems, and interfaces** overlap — mostly small, local, slightly strange tools that do one thing and can explain why they did it.

<br>

```console
$ cat ~/now
01  researching   reputation-aware LLM agents
02  designing     MITES — a swarm of tiny event-driven local agents
03  building      software, tools, web things
04  learning      how far Linux bends before I regret it
```

<br>

## research

<details>
<summary><b>reputation-aware agents</b> — agents that remember who lied to them</summary>

<br>

Most agents treat every message as equally trustworthy. In repeated multi-agent settings, that's a bug.

```
   interaction
        │
        ▼
 ┌──────────────┐
 │ observation  │
 └──────┬───────┘
        ▼
  reputation Δ  ──►  persistent model of the other agent
        │
        ▼
 future decisions change
```

The model tracks **trust · deception · reliability · cooperation · contradiction · social history**.

Questions I'm chasing:

- can an agent learn whom to trust from interaction history rather than a system prompt?
- what does deception look like as a signal over time, not in a single turn?
- how should reputation decay, transfer between contexts, or be contested?

</details>

<details>
<summary><b>MITES</b> — Micro Intelligent Task Execution Swarm</summary>

<br>

An experiment in replacing *one giant assistant doing everything* with many small ones that only wake up when something happens.

```
                  events
                    │
      ┌─────────────┼─────────────┐
      ▼             ▼             ▼
    rules       tiny model    tiny model
      │             │             │
      └─────────────┼─────────────┘
                    ▼
               shared state
                    │
               escalate?
               /       \
             no         yes
             │           │
          execute    bigger model
```

Design goals:

| | |
|---|---|
| **cheap** | rules first, tiny models second, big models only on escalation |
| **event-driven** | nothing runs unless something happened |
| **auditable** | every action traces back to an event and a decision |
| **permission-aware** | each agent gets only the access its job needs |
| **modular** | swap any agent without touching the rest |

</details>

<br>

## things I've built

| project | what it is |
|---|---|
| [**Parker**](https://github.com/AkumaNomu/Parker) | <!-- one line: what it does + main tech --> |
| [**Mai**](https://github.com/AkumaNomu/Mai) | <!-- one line --> |
| [**Tina**](https://github.com/AkumaNomu/Tina) | <!-- one line --> |
| [**MemReRust**](https://github.com/AkumaNomu/MemReRust) | <!-- one line --> |

<br>

## toolbox

```yaml
languages:  python · typescript · rust · c++ · javascript
web:        react · next.js · postgresql · supabase
ml/audio:   scikit-learn · librosa · whisper · onnx
systems:    linux · ffmpeg · tesseract · webextensions
```

<br>

<div align="center">
<sub>if you're working on agents, trust, or local-first AI — say hi.</sub>
</div>
