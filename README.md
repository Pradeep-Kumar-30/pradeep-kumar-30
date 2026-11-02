<div align="center">

<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=0:08111F,50:123B69,100:06B6D4&height=190&section=header&text=Pradeep%20Kumar&fontSize=52&fontColor=FFFFFF&animation=fadeIn&fontAlignY=38&desc=FULL-STACK%20DEVELOPER%20%7C%20AI%20ENGINEERING&descAlignY=61&descSize=15" alt="Pradeep Kumar" />

[![Typing SVG](https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=18&duration=2600&pause=900&color=38BDF8&center=true&vCenter=true&width=720&lines=Building+full-stack+and+AI-powered+systems;Exploring+RAG%2C+agents%2C+and+network+traffic;850%2B+problems+solved)](https://git.io/typing-svg)

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/pradeep-kumar-6aa767324)
[![Email](https://img.shields.io/badge/Email-Contact-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:pradeep9887069@gmail.com)
[![GitHub](https://img.shields.io/badge/GitHub-Projects-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Pradeep-Kumar-30)

</div>

<table>
<tr>
<td width="60%" valign="middle">

## About me

Computer Science and Engineering student at **IIIT Bhagalpur** with experience in full-stack development, AI engineering, and backend systems.

- **Full Stack Developer Intern**, AMUS SOFT · Jul–Aug 2026
- **850+** problems solved across Codeforces, CodeChef, and LeetCode
- Focus: **RAG, AI agents, backend development, and system design**

</td>
<td width="40%" align="center" valign="middle">

<img src="./assets/developer-with-hair.svg" width="330" alt="Developer with wavy hair coding at a laptop" />

</td>
</tr>
</table>

## Projects · visual flows

### PacketLens · Deep Packet Inspection

<div align="center">

![Animated packet traveling through a router to PacketLens, where a matching rule blocks it](./assets/packetlens-flow.gif)

</div>

```mermaid
flowchart LR
    A[PCAP] --> B[Ethernet / IPv4 / TCP / UDP]
    B --> C[5-tuple flow]
    C --> D{Visible host data?}
    D -->|TLS| E[Extract SNI]
    D -->|HTTP| F[Read Host]
    D -->|Unavailable| G[Unknown host]
    E --> H[Classify application / domain]
    F --> H
    G --> H
    H --> I{IP / app / domain rule?}
    I -->|Match| J[Block packet]
    I -->|No match| K[Keep packet]
    J --> L[Filtered PCAP + report]
    K --> L
    classDef input fill:#10213A,stroke:#38BDF8,color:#E0F2FE,stroke-width:2px
    classDef step fill:#111827,stroke:#64748B,color:#F8FAFC
    classDef gate fill:#422006,stroke:#F59E0B,color:#FEF3C7,stroke-width:2px
    classDef block fill:#450A0A,stroke:#EF4444,color:#FEE2E2
    classDef allow fill:#052E16,stroke:#22C55E,color:#DCFCE7
    class A,L input
    class B,C,E,F,G,H step
    class D,I gate
    class J block
    class K allow
```

`Python` · `TCP/IP` · `TLS` · `HTTP` · `PCAP` · `Pytest` · `Docker`

### CampusConnect · Real-Time College Intranet

```mermaid
flowchart LR
    A[Student] --> B[JWT authentication]
    B --> C{RBAC check}
    C -->|Denied| X[Reject]
    C -->|Allowed| D[CampusConnect]
    D --> E[Message / event]
    E --> F[Socket.IO]
    F --> G[500+ student community]
    G --> H[Real-time update]
    classDef input fill:#10213A,stroke:#38BDF8,color:#E0F2FE,stroke-width:2px
    classDef step fill:#111827,stroke:#64748B,color:#F8FAFC
    classDef gate fill:#422006,stroke:#F59E0B,color:#FEF3C7,stroke-width:2px
    classDef block fill:#450A0A,stroke:#EF4444,color:#FEE2E2
    classDef done fill:#052E16,stroke:#22C55E,color:#DCFCE7
    class A,H input
    class B,D,E,F,G step
    class C gate
    class X block
```

`React` · `Node.js` · `Express.js` · `MongoDB` · `Socket.IO` · `JWT` · `RBAC`

### CloudOps Sentinel · Incident Response Self-RAG Copilot

```mermaid
flowchart LR
    A[Incident question] --> B[Retrieve private runbooks]
    B --> C{Relevant evidence?}
    C -->|No| D[Rewrite query / retry]
    D --> B
    B -. Internal evidence insufficient .-> E[Tavily web-search fallback]
    C -->|Yes| F[Generate grounded answer]
    E --> F
    F --> G[IsSUP + IsUSE evaluation]
    G -->|Needs correction| D
    G -->|Pass| H[Evidence-based response]
    classDef input fill:#10213A,stroke:#38BDF8,color:#E0F2FE,stroke-width:2px
    classDef step fill:#111827,stroke:#64748B,color:#F8FAFC
    classDef gate fill:#422006,stroke:#F59E0B,color:#FEF3C7,stroke-width:2px
    classDef done fill:#052E16,stroke:#22C55E,color:#DCFCE7
    class A,H input
    class B,D,E,F,G step
    class C gate
```

`LangGraph` · `OpenAI GPT-5-mini` · `Pinecone` · `FastAPI` · `SQLite` · `Tavily`

### Cold-Chain Logistics · Agentic Dispatch Console

```mermaid
flowchart LR
    A[Dispatch question] --> B[LangGraph agent]
    B --> C{Call data tools}
    C --> D[SQL Server fleet telemetry]
    C --> E[Open-Meteo weather]
    C --> F[Pinecone SOP retrieval]
    D --> G[Combine context]
    E --> G
    F --> G
    G --> H{More information needed?}
    H -->|Yes| B
    H -->|No| I[Dispatch recommendation]
    I --> J[Streamlit console]
    classDef input fill:#10213A,stroke:#38BDF8,color:#E0F2FE,stroke-width:2px
    classDef step fill:#111827,stroke:#64748B,color:#F8FAFC
    classDef gate fill:#422006,stroke:#F59E0B,color:#FEF3C7,stroke-width:2px
    classDef done fill:#052E16,stroke:#22C55E,color:#DCFCE7
    class A,J input
    class B,D,E,F,G step
    class C,H gate
    class I done
```

`LangGraph` · `Python` · `SQL Server` · `Pinecone` · `AWS EC2` · `GitHub Actions`

## Core stack

`Python` `C++` `JavaScript` `React` `Node.js` `Express.js` `FastAPI` `LangGraph` `LangChain` `RAG` `OpenAI API` `Gemini API` `PostgreSQL` `MongoDB` `Redis` `Pinecone` `Docker` `AWS EC2` `GitHub Actions`

## Highlights

| Codeforces | CodeChef | LeetCode |
|:---:|:---:|:---:|
| Specialist · peak **1410** | 3-Star · peak **1653** | Rating **1694** · top **14.69%** |
| 468 problems | 224 problems · 31 contests |  |

**Education:** B.Tech CSE · IIIT Bhagalpur · 2024–2028

**Leadership:** Web Developer, IIIT Bhagalpur Development Team · Class Representative · Hackathon Team Lead

**Certifications:** Cisco Introduction to Cybersecurity · Adobe University Hackathons · Machine Learning and Deep Learning in Agriculture and Biomedical Engineering, IIIT Bhagalpur

<div align="center">

[![Contact](https://img.shields.io/badge/Contact-pradeep9887069%40gmail.com-06B6D4?style=for-the-badge&logo=gmail&logoColor=white)](mailto:pradeep9887069@gmail.com)

<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=0:06B6D4,50:123B69,100:08111F&height=90&section=footer" alt="" />

</div>
