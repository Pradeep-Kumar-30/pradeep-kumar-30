<div align="center">

<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=0:070B18,45:123B69,100:06B6D4&height=230&section=header&text=Pradeep%20Kumar&fontSize=58&fontColor=F8FAFC&animation=fadeIn&fontAlignY=38&desc=FULL-STACK%20DEVELOPER%20%7C%20AI%20ENGINEER%20%7C%20BUILDER&descAlignY=61&descSize=16" alt="Pradeep Kumar profile banner" />

[![Typing SVG](https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=19&duration=2600&pause=900&color=38BDF8&center=true&vCenter=true&width=760&lines=I+build+useful+full-stack+products;I+turn+network+packets+into+clear+insights;I+design+RAG+and+multi-agent+workflows;I+love+backend+systems+and+hard+problems)](https://git.io/typing-svg)

<br/>

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/pradeep-kumar-6aa767324)
[![Email](https://img.shields.io/badge/Email-Say%20hello-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:pradeep9887069@gmail.com)
[![Instagram](https://img.shields.io/badge/Instagram-Follow-E4405F?style=for-the-badge&logo=instagram&logoColor=white)](https://instagram.com/praadeep_yadav_)
[![GitHub](https://img.shields.io/badge/GitHub-Explore%20my%20work-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Pradeep-Kumar-30)

![Profile views](https://komarev.com/ghpvc/?username=Pradeep-Kumar-30&style=for-the-badge&color=0E7490&label=PROFILE+VIEWS)

</div>

<table>
<tr>
<td width="60%" valign="middle">

## 👨‍💻 About me

I'm a **Full-Stack Developer and AI Engineer** pursuing Computer Science at **IIIT Bhagalpur**. I like taking a problem from packet parsing or product idea through backend logic and into a usable interface.

- 🎓 **B.Tech in CSE, IIIT Bhagalpur** · CGPA **9.15/10** · 2024–2028
- 💼 **Full Stack Developer Intern, AMUS SOFT** · Jul–Aug 2026
- 🔭 Building **PacketLens** and full-stack applications; exploring **Medisaathi**, a smart appointment and queue management system
- 🌱 Learning **System Design, advanced backend development, Redis, and scalable architecture**
- 🧠 Interested in **AI applications, RAG, multi-agent systems, and real-time products**
- 🧩 Solved **850+ problems** across Codeforces, CodeChef, and LeetCode
- 🤝 Open to collaboration on **MERN, AI-powered apps, open source, and real-time projects**
- 💬 Ask me about **React, Node.js, Express, MongoDB, REST APIs, JWT, Socket.IO, DSA, and competitive programming**

</td>
<td width="40%" align="center" valign="middle">

<img src="https://media.giphy.com/media/SWoSkN6DxTszqIKEqv/giphy.gif" width="330" alt="Developer working at a laptop" />

**Idea → architecture → implementation → ship**

</td>
</tr>
</table>

## 📡 PacketLens — watch a packet travel

An animated walkthrough: a packet travels from the **client**, through a **router**, and reaches the **PacketLens rule engine**. The YouTube example matches a block rule and gets dropped; an allowed packet continues to the server. This is an explanatory visualization of the project’s filtering flow.

<div align="center">

<img src="assets/packetlens-flow.gif" width="100%" alt="Animated PacketLens flow showing a packet moving from client to router, being blocked by PacketLens, and an allowed packet continuing to the server" />

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

## 🚀 Projects I enjoy building

| Project | What it does | Technologies |
|---|---|---|
| **PacketLens** | Deep packet inspection engine that parses PCAP, identifies flows, extracts visible host details, applies rules, and produces a filtered capture. | Python, TCP/IP, TLS, HTTP, PCAP, Docker |
| **Medisaathi** | Smart appointment and queue management system. | MERN stack, full-stack development |
| **CampusConnect** | Real-time college intranet for **500+ students**, with messaging and secure role-based access. | React, Node.js, Express, MongoDB, Socket.IO |
| **AI Notes Generator** | Generates notes with the Gemini API. | AI API integration, web development |
| **Zesto Food Delivery** | Full-stack food ordering platform. | MERN stack |
| **CloudOps Sentinel** | Self-RAG incident response copilot with relevance grading, query rewriting, evidence checks, and private knowledge-base retrieval. | LangGraph, OpenAI, Pinecone, FastAPI, SQLite |
| **Cold-Chain Logistics** | Agentic dispatch console that brings fleet data, weather, and operating procedures into one workflow. | LangGraph, Python, SQL Server, Pinecone, AWS EC2 |

### 🧠 How my RAG projects reason

```mermaid
flowchart LR
    U[Question] --> R[Retrieve internal evidence]
    R --> G{Relevant evidence?}
    G -->|No| Q[Rewrite the query]
    Q --> R
    G -->|Yes| A[Generate grounded response]
    A --> V[Check support and usefulness]
    V -->|Improve| Q
    V -->|Ready| O[Answer with evidence]

    classDef start fill:#10213A,stroke:#38BDF8,color:#E0F2FE,stroke-width:2px
    classDef step fill:#111827,stroke:#64748B,color:#F8FAFC
    classDef gate fill:#422006,stroke:#F59E0B,color:#FEF3C7,stroke-width:2px
    classDef done fill:#052E16,stroke:#22C55E,color:#DCFCE7,stroke-width:2px
    class U,O start
    class R,Q,A,V step
    class G gate
```

## 🧰 Technologies

<details>
<summary><b>AI engineering, RAG & evaluation</b></summary>
<br/>

`LangGraph` `LangChain` `OpenAI API` `Gemini API` `AI Agents` `Multi-Agent Systems` `Tool Calling` `MCP` `Prompt Engineering` `Structured Outputs` `Human-in-the-Loop` `RAG` `Self-RAG` `Agentic RAG` `CRAG` `Hybrid Search` `Semantic Search` `BM25` `Embeddings` `Reranking` `Vector Search` `RAGAS` `DeepEval` `LangSmith` `LLM-as-a-Judge` `Hallucination Detection`
</details>

<details>
<summary><b>Languages, frontend & backend</b></summary>
<br/>

`C` `C++` `Python` `JavaScript` `SQL` `HTML` `CSS` `React` `React Native` `Redux Toolkit` `React Router` `React Hook Form` `Node.js` `Express.js` `FastAPI` `REST APIs` `WebSockets` `Socket.IO` `JWT` `RBAC` `PHP`
</details>

<details>
<summary><b>Databases, cloud & developer tools</b></summary>
<br/>

`PostgreSQL` `MongoDB` `Redis` `MySQL` `SQL Server` `SQLite` `Pinecone` `Firebase` `AWS EC2` `Docker` `Nginx` `Linux` `Git` `GitHub` `GitHub Actions` `CI/CD` `Vercel` `Pytest` `Postman` `Vite` `Tailwind CSS` `Sass` `Bootstrap` `Three.js`
</details>

<details>
<summary><b>Also used</b></summary>
<br/>

`Nodemon` `Canva` `NumPy` `Pandas` `Matplotlib`
</details>

## 🏅 Competitive programming

<div align="center">

| Codeforces | CodeChef | LeetCode |
|:---:|:---:|:---:|
| **Specialist** · peak **1410** | **3-Star** · peak **1653** | Contest rating **1694** |
| 468 problems | 224 problems · 31 contests | Top **14.69%** |

**850+ problems solved** across platforms · DSA, graphs, dynamic programming, and greedy algorithms

</div>

## 📊 GitHub activity

<div align="center">

<img height="170" src="https://github-readme-stats.vercel.app/api?username=Pradeep-Kumar-30&show_icons=true&theme=tokyonight&hide_border=true&rank_icon=github" alt="GitHub contribution statistics" />
<img height="170" src="https://github-readme-stats.vercel.app/api/top-langs/?username=Pradeep-Kumar-30&layout=compact&theme=tokyonight&hide_border=true" alt="Most used languages" />

<br/>

<img src="https://streak-stats.demolab.com?user=Pradeep-Kumar-30&theme=tokyonight&hide_border=true" alt="GitHub contribution streak" />

</div>

## 🌱 Beyond the code

- **Web Developer**, IIIT Bhagalpur Development Team · 2024–present
- **Class Representative** · 2024–present
- **Hackathon Team Lead** · led a four-member team through architecture, implementation, and debugging
- Certifications: **Cisco Introduction to Cybersecurity**, **Adobe University Hackathons**, and **Machine Learning and Deep Learning in Agriculture and Biomedical Engineering** at IIIT Bhagalpur
- I enjoy building scalable applications and solving challenging algorithmic problems.

<div align="center">

### Have an interesting product or open-source idea? Let's build.

[![Email Pradeep](https://img.shields.io/badge/Let's%20collaborate-pradeep9887069%40gmail.com-06B6D4?style=for-the-badge&logo=gmail&logoColor=white)](mailto:pradeep9887069@gmail.com)

<sub>Previously listed email: <a href="mailto:pradeepkumariiitbhagalpur@gmail.com">pradeepkumariiitbhagalpur@gmail.com</a></sub>

<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=0:06B6D4,50:123B69,100:070B18&height=110&section=footer" alt="" />

</div>
