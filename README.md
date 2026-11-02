<div align="center">

<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=0:070B18,45:123B69,100:06B6D4&height=230&section=header&text=Pradeep%20Kumar&fontSize=58&fontColor=F8FAFC&animation=fadeIn&fontAlignY=38&desc=FULL-STACK%20DEVELOPER%20%7C%20AI%20ENGINEER%20%7C%20BUILDER&descAlignY=61&descSize=16" alt="Pradeep Kumar profile banner" />

[![Typing SVG](https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=19&duration=2600&pause=900&color=38BDF8&center=true&vCenter=true&width=760&lines=I+build+useful+full-stack+products;I+turn+network+packets+into+clear+insights;I+design+RAG+and+multi-agent+workflows;I+love+backend+systems+and+hard+problems)](https://git.io/typing-svg)

<br/>

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/pradeep-kumar-6aa767324)
[![Email](https://img.shields.io/badge/Email-Say%20hello-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:pradeep9887069@gmail.com)
[![GitHub](https://img.shields.io/badge/GitHub-Explore%20my%20work-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Pradeep-Kumar-30)

![Profile views](https://komarev.com/ghpvc/?username=Pradeep-Kumar-30&style=for-the-badge&color=0E7490&label=PROFILE+VIEWS)

</div>

<table>
<tr>
<td width="60%" valign="middle">

## 👨‍💻 About me

**Computer Science and Engineering undergraduate at IIIT Bhagalpur** with experience in full-stack development, AI engineering, backend systems, and competitive programming.

- 🎓 **B.Tech in CSE, IIIT Bhagalpur** ·  · 2024–2028
- 💼 **Full Stack Developer Intern, AMUS SOFT** · Jul–Aug 2026
- 🧠 Focus areas: **AI engineering, RAG and retrieval, backend and full-stack development**
- 🧩 Solved **850+ problems** across Codeforces, CodeChef, and LeetCode

</td>
<td width="40%" align="center" valign="middle">

<img src="https://media.giphy.com/media/SWoSkN6DxTszqIKEqv/giphy.gif" width="330" alt="Developer working at a laptop" />

</td>
</tr>
</table>

## 📡 PacketLens — watch a packet travel

<div align="center">

![Animated PacketLens packet flow](./assets/packetlens-flow.gif)

</div>

### What happens inside the analysis

```mermaid
flowchart LR
    A[PCAP capture] --> B[Read packet records]
    B --> C[Parse Ethernet, IPv4, TCP or UDP]
    C --> D[Identify flow with 5-tuple]
    D --> E{Host data visible?}
    E -->|TLS Client Hello| F[Extract SNI]
    E -->|HTTP request| G[Read Host header]
    E -->|No host data| H[Classify as unknown when needed]
    F --> I[Classify flow]
    G --> I
    H --> I
    I --> J{Matches IP, app, or domain rule?}
    J -->|No| K[Keep packet]
    J -->|Yes| L[Exclude packet]
    K --> M[Summary and filtered PCAP]
    L --> M

    classDef input fill:#10213A,stroke:#38BDF8,color:#E0F2FE,stroke-width:2px
    classDef step fill:#111827,stroke:#64748B,color:#F8FAFC
    classDef choice fill:#422006,stroke:#F59E0B,color:#FEF3C7,stroke-width:2px
    classDef allow fill:#052E16,stroke:#22C55E,color:#DCFCE7,stroke-width:2px
    classDef block fill:#450A0A,stroke:#EF4444,color:#FEE2E2,stroke-width:2px
    class A,M input
    class B,C,D,F,G,H,I step
    class E,J choice
    class K allow
    class L block
```

**Project stack:** `Python` · `TCP/IP` · `TLS` · `HTTP` · `PCAP` · `Pytest` · `Docker`

> PacketLens focuses on classic Ethernet PCAP and IPv4 TCP/UDP. It extracts TLS SNI and HTTP Host when available in a packet; it does not reassemble TCP payloads split across packets, and encrypted traffic may hide host details.

## 🚀 Resume projects — visual flows

### 💬 CampusConnect · Real-Time College Intranet

```mermaid
flowchart LR
    A[Student] --> B[JWT authentication]
    B --> C{RBAC permission}
    C -->|Denied| X[Reject request]
    C -->|Allowed| D[CampusConnect]
    D --> E[Message or event]
    E --> F[Socket.IO / WebSocket]
    F --> G[500+ student community]
    G --> H[Real-time update]
    classDef entry fill:#10213A,stroke:#38BDF8,color:#E0F2FE,stroke-width:2px
    classDef step fill:#111827,stroke:#64748B,color:#F8FAFC
    classDef choice fill:#422006,stroke:#F59E0B,color:#FEF3C7,stroke-width:2px
    classDef deny fill:#450A0A,stroke:#EF4444,color:#FEE2E2
    class A,H entry
    class B,D,E,F,G step
    class C choice
    class X deny
```

`React` · `Node.js` · `Express.js` · `MongoDB` · `Socket.IO` · `JWT` · `RBAC`

### 🛡️ CloudOps Sentinel · Incident Response Self-RAG Copilot

```mermaid
flowchart LR
    U[Incident question] --> R[Retrieve private runbooks and postmortems]
    R --> G{Relevant evidence?}
    G -->|No| Q[Rewrite query and retry]
    Q --> R
    G -->|Yes| A[Draft evidence-based answer]
    R -. if internal evidence is insufficient .-> W[Tavily web-search fallback]
    W --> A
    A --> E[Evaluate support and usefulness]
    E -->|Needs correction| Q
    E -->|Passes checks| O[Return grounded response]
    classDef entry fill:#10213A,stroke:#38BDF8,color:#E0F2FE,stroke-width:2px
    classDef step fill:#111827,stroke:#64748B,color:#F8FAFC
    classDef choice fill:#422006,stroke:#F59E0B,color:#FEF3C7,stroke-width:2px
    classDef result fill:#052E16,stroke:#22C55E,color:#DCFCE7,stroke-width:2px
    class U,O entry
    class R,Q,A,E,W step
    class G choice
```

`LangGraph` · `OpenAI GPT-5-mini` · `Pinecone` · `FastAPI` · `SQLite` · `Tavily` · `IsSUP` · `IsUSE`

### 🚚 Cold-Chain Logistics · Agentic Dispatch Console

```mermaid
flowchart LR
    U[Dispatch question] --> A[LangGraph agent]
    A --> T{Choose tools}
    T -->|Fleet telemetry| SQL[SQL Server]
    T -->|Weather| WX[Open-Meteo]
    T -->|Operating procedures| V[Pinecone SOP search]
    SQL --> C[Combine retrieved context]
    WX --> C
    V --> C
    C --> G{Need another tool call?}
    G -->|Yes| A
    G -->|No| R[Dispatch recommendation]
    R --> UI[Streamlit operations console]
    classDef entry fill:#10213A,stroke:#38BDF8,color:#E0F2FE,stroke-width:2px
    classDef step fill:#111827,stroke:#64748B,color:#F8FAFC
    classDef choice fill:#422006,stroke:#F59E0B,color:#FEF3C7,stroke-width:2px
    classDef result fill:#052E16,stroke:#22C55E,color:#DCFCE7,stroke-width:2px
    class U,UI entry
    class A,SQL,WX,V,C step
    class T,G choice
    class R result
```

`LangGraph` · `Python` · `SQL Server` · `Open-Meteo` · `Pinecone` · `Streamlit` · `AWS EC2` · `GitHub Actions`

## 🧰 Technologies

<details>
<summary><b>AI engineering, retrieval & evaluation</b></summary>
<br/>

`LangGraph` `LangChain` `OpenAI API` `Gemini API` `AI Agents` `Multi-Agent Systems` `Tool Calling` `Function Calling` `MCP` `Prompt Engineering` `Structured Outputs` `Human-in-the-Loop` `RAG` `Self-RAG` `Agentic RAG` `CRAG` `Hybrid Search` `Semantic Search` `BM25` `Embeddings` `Query Rewriting` `Reranking` `Vector Search` `RAGAS` `DeepEval` `LangSmith` `LLM-as-a-Judge` `IsSUP` `IsUSE` `Faithfulness` `Groundedness` `Hallucination Detection`
</details>

<details>
<summary><b>Languages, frontend & backend</b></summary>
<br/>

`C` `C++` `Python` `JavaScript` `SQL` `HTML` `CSS` `React.js` `Redux Toolkit` `Node.js` `Express.js` `FastAPI` `REST APIs` `WebSockets` `Socket.IO` `JWT` `RBAC`
</details>

<details>
<summary><b>Databases, cloud & developer tools</b></summary>
<br/>

`PostgreSQL` `MySQL` `SQL Server` `MongoDB` `Redis` `Pinecone` `SQLite` `Vector Databases` `AWS EC2` `Docker` `GitHub Actions` `CI/CD` `Linux` `Git` `GitHub` `Nginx` `Postman` `Pytest` `Deployment Automation`
</details>

<details>
<summary><b>System design & computer science</b></summary>
<br/>

`HLD` `LLD` `OOP` `SOLID` `Microservices` `Distributed Systems` `API Integration` `Enterprise Integration` `Solution Architecture` `Rapid Prototyping` `Debugging` `Data Structures & Algorithms` `Operating Systems` `DBMS` `Computer Networks` `TCP/IP` `HTTP` `TLS`
</details>

## 🏅 Competitive programming

<div align="center">

| Codeforces | CodeChef | LeetCode |
|:---:|:---:|:---:|
| **Specialist** · peak **1410**, current **1339** | **3-Star** · peak **1653** | Contest rating **1694** |
| 468 problems | 224 problems · 31 contests | Top **14.69%** |

**850+ problems solved** across platforms · DSA, graphs, dynamic programming, and greedy algorithms

</div>

## 💼 Experience & leadership

- **Full Stack Developer Intern**, AMUS SOFT · Remote · Jul–Aug 2026
- **Web Developer**, IIIT Bhagalpur Development Team · 2024–present
- **Class Representative** · 2024–present
- **Hackathon Team Lead** · led a four-member team through architecture, implementation, and debugging

## 📜 Certifications

- Introduction to Cybersecurity · Cisco Networking Academy
- Adobe University Hackathons · Adobe
- Machine Learning and Deep Learning in Agriculture and Biomedical Engineering · IIIT Bhagalpur

<div align="center">

### Contact

[![Email Pradeep](https://img.shields.io/badge/Let's%20collaborate-pradeep9887069%40gmail.com-06B6D4?style=for-the-badge&logo=gmail&logoColor=white)](mailto:pradeep9887069@gmail.com)

<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=0:06B6D4,50:123B69,100:070B18&height=110&section=footer" alt="" />

</div>
