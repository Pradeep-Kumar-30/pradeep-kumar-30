<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0F172A,50:0EA5E9,100:22D3EE&height=220&section=header&text=Pradeep%20Kumar&fontSize=54&fontColor=ffffff&animation=fadeIn&fontAlignY=38&desc=Full-Stack%20Developer%20%7C%20AI%20Engineer&descAlignY=60&descSize=18" width="100%" alt="Pradeep Kumar profile banner" />

<a href="https://git.io/typing-svg">
  <img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=20&duration=2600&pause=900&color=38BDF8&center=true&vCenter=true&width=720&lines=Building+AI-powered+applications;Turning+PCAP+traffic+into+clear+insights;Creating+RAG+and+multi-agent+workflows;Shipping+reliable+full-stack+software" alt="Animated introduction" />
</a>

<br/>

<a href="mailto:pradeep9887069@gmail.com"><img src="https://img.shields.io/badge/Email-Let's%20connect-0EA5E9?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" /></a>
<a href="https://linkedin.com/in/pradeep-kumar-6aa767324"><img src="https://img.shields.io/badge/LinkedIn-Connect-2563EB?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>
<a href="https://github.com/Pradeep-Kumar-30"><img src="https://img.shields.io/badge/GitHub-Follow-111827?style=for-the-badge&logo=github&logoColor=white" alt="GitHub" /></a>

</div>

---

<table>
<tr>
<td width="58%" valign="middle">

## 👨‍💻 A little about me

I'm a **Computer Science student at IIIT Bhagalpur** who enjoys building useful software across full-stack development, backend systems, and AI engineering.

- 🎓 **B.Tech CSE, IIIT Bhagalpur**
- 💼 **Full Stack Developer Intern** at AMUS SOFT
- 🔭 Building **PacketLens**, a Python Deep Packet Inspection engine
- 🤖 Exploring **RAG, AI agents, and multi-agent systems**
- 🧩 Solved **850+** problems across coding platforms
- 📍 Bhagalpur, India

</td>
<td width="42%" align="center" valign="middle">

<img src="https://media.giphy.com/media/SWoSkN6DxTszqIKEqv/giphy.gif" width="340" alt="Developer coding at a laptop" />

</td>
</tr>
</table>

## 🛰️ PacketLens: follow a packet

**PacketLens** reads a PCAP capture, extracts packet and flow details, identifies available host information, then applies your filtering rules. The diagram shows the analysis path and the allow/block decision.

```mermaid
flowchart LR
    A["📁 PCAP capture"] --> B["📦 Read packet records"]
    B --> C["🔍 Parse Ethernet, IPv4, TCP / UDP"]
    C --> D["🧬 Group packets by 5-tuple flow"]
    D --> E{"🌐 Host info available?"}
    E -->|"TLS Client Hello"| F["Extract SNI"]
    E -->|"HTTP request"| G["Read Host header"]
    E -->|"Unavailable"| H["Keep host unknown"]
    F --> I["🏷️ Classify application / domain"]
    G --> I
    H --> I
    I --> J{"⚙️ Matches a block rule?"}
    J -->|"No"| K["✅ Keep packet"]
    J -->|"Yes"| L["⛔ Exclude packet"]
    K --> M["📊 Traffic summary + filtered PCAP"]
    L --> M

    classDef input fill:#172554,stroke:#38bdf8,color:#e0f2fe,stroke-width:2px
    classDef process fill:#0f172a,stroke:#64748b,color:#f8fafc
    classDef decision fill:#422006,stroke:#f59e0b,color:#fef3c7,stroke-width:2px
    classDef keep fill:#052e16,stroke:#22c55e,color:#dcfce7,stroke-width:2px
    classDef drop fill:#450a0a,stroke:#ef4444,color:#fee2e2,stroke-width:2px
    class A,M input
    class B,C,D,F,G,H,I process
    class E,J decision
    class K keep
    class L drop
