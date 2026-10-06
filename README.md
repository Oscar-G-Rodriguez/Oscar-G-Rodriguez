<a name="top"></a>

![Oscar Rodriguez: Machine learning, AI applications, University of Florida](https://capsule-render.vercel.app/api?type=rect&color=0f172a&height=180&text=Oscar%20Rodriguez&fontColor=f8fafc&fontSize=46&fontAlignY=40&desc=Machine%20Learning%20%7C%20AI%20Applications%20%7C%20University%20of%20Florida&descSize=17&descAlignY=66)

<p align="center">
  <a href="#skills">Skills & direction</a> &nbsp;·&nbsp;
  <a href="#projects">Projects</a> &nbsp;·&nbsp;
  <a href="#roles">Current roles</a> &nbsp;·&nbsp;
  <a href="https://www.linkedin.com/in/oscar-g-rodriguez/">LinkedIn</a> &nbsp;·&nbsp;
  <a href="https://github.com/Oscar-G-Rodriguez?tab=repositories">All repositories</a>
</p>

Hi, I'm Oscar. I'm a freshman studying computer science at the University of Florida. I enjoy working with data, and I'm interested in machine learning and AI. Most of my projects bring models and data into apps that people can use and explore.

<a name="skills"></a>

## Skills and direction

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![Java](https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![C++](https://img.shields.io/badge/C%2B%2B-00599C?style=flat-square&logo=cplusplus&logoColor=white)
![CUDA](https://img.shields.io/badge/CUDA-76B900?style=flat-square&logo=nvidia&logoColor=white)

| Area | Tools and experience from my projects |
| :--- | :--- |
| **ML and AI** | PyTorch, Hugging Face Transformers, XGBoost, Gemini, SegFormer; local LLM inference, agent evaluation, and computer vision |
| **Data and storage** | pandas, NumPy, SQLite, Parquet; data cleaning, quality checks, API ingestion, time-series forecasting, and walk-forward evaluation |
| **Web and APIs** | React, Next.js, Node.js, FastAPI, Fastify, Spring Boot, HTML/CSS; REST APIs and WebSockets |
| **Speech and media** | ElevenLabs, faster-whisper, FFmpeg |
| **GPU development** | CUDA kernels, PyTorch C++ extensions, PyTorch Profiler, numerical validation, and NVIDIA Compute Sanitizer |
| **Testing** | pytest, unittest, JUnit, Mockito, Spring MockMvc, and Playwright |
| **Development tools** | Git, uv, Gradle, Vite, Linux, and WSL |

Recently, I've been using PyTorch and Transformers to evaluate a local Qwen agent in [Factorio Agent Evals](https://github.com/Oscar-G-Rodriguez/factorio-agent-evals). I also implemented and tested a C++/CUDA RMSNorm operator for that project. My Java backend work covers request validation, concurrent updates, and HTTP tests. I enjoy working through the whole application, especially the data and ML.

I'd like to work on frontier models in any way I can. I want to keep building useful applications while learning more about how models are trained, evaluated, and improved.

<a name="projects"></a>

## Featured projects

| Project | What you can explore | Start here |
| :--- | :--- | :--- |
| **Factorio Agent Evals** | Local Qwen agent evaluation, factory-maintenance traces, and a C++/CUDA RMSNorm benchmark | [Overview](#factorio-agent-evals) · [Results](https://github.com/Oscar-G-Rodriguez/factorio-agent-evals/blob/main/outputs/A04%20-%20Maintenance%20-%20Results.md) |
| **SeekR** | Phone-camera object finding and voice-guided navigation | [Overview](#seekr) · [Code](https://github.com/Hemanka/Shellhacks-X) |
| **ROMULUS** | Strategy comparisons, ML forecasts, and the evidence behind portfolio decisions | [Overview](#romulus) · [Validation](https://github.com/Oscar-G-Rodriguez/ROMULUS/blob/main/VALIDATION_REPORT.md) |
| **Florida Policy Advisor** | Florida indicators, data quality, and traceable policy comparisons | [Overview](#florida-policy-advisor) · [Evidence](https://github.com/Oscar-G-Rodriguez/florida_policy_advisor/blob/main/portfolio_evidence/README.md) |

<a name="factorio-agent-evals"></a>

### Factorio Agent Evals

**Agent evaluation · PyTorch · Transformers · C++/CUDA**

I built Factorio Agent Evals to test whether a local language model could keep a small Factorio factory producing iron plates. Qwen3-4B-Instruct-2507 runs locally through PyTorch and Hugging Face Transformers. A Python controller gives it the current factory state and allowed tools, validates its chosen JSON action, and records what happens. I use those traces to inspect where the agent misses fuel or storage decisions. A scripted controller sustained production for 20 game minutes; Qwen's episode ended after 11, which gave me a concrete failure to investigate.

I also profiled the model and implemented an RMSNorm operator with a C++ binding and a CUDA kernel. The reviewed implementation passed 25 numerical correctness cases and four NVIDIA Compute Sanitizer checks. In standalone operator benchmarks on captured inputs, it ran 5.21× faster for the prompt-sized operation and 4.80× faster for the single-token operation than the installed eager CUDA reference. The repository includes the methods, timing samples, source hashes, and original agent traces.

[Repository](https://github.com/Oscar-G-Rodriguez/factorio-agent-evals) &nbsp;·&nbsp; [Agent results](https://github.com/Oscar-G-Rodriguez/factorio-agent-evals/blob/main/outputs/A04%20-%20Maintenance%20-%20Results.md) &nbsp;·&nbsp; [CUDA benchmark](https://github.com/Oscar-G-Rodriguez/factorio-agent-evals/blob/main/outputs/K01%20-%20RMSNorm%20-%20Reviewed%20Benchmark.md)

---

<a name="seekr"></a>

### SeekR

**Computer vision · Accessibility · Gemini · SegFormer**

I worked on SeekR with a team to help blind users find objects and navigate a room using a phone camera and voice guidance. It's the project I feel best represents my interests right now. We chose vision models so users could navigate with a phone without carrying or setting up a separate sensor. The phone captures the view and speaks the guidance. A Windows dashboard runs the analysis.

After a user says what they're looking for, Gemini examines the camera view to identify the target and its position. A segmentation model marks likely walkable areas and obstacles. SeekR uses those outputs to choose a short movement instruction, which the phone reads aloud before sending another view for the next step. I tested it in classrooms and living rooms, where I used it to move around obstacles and reach the objects I was looking for.

[Repository](https://github.com/Hemanka/Shellhacks-X)

---

<a name="romulus"></a>

### ROMULUS

**Python · XGBoost · Walk-forward evaluation · Decision audits**

ROMULUS is a local financial research app I built to compare trading strategies over time. Each strategy has its own simulated portfolio and runs on the same point-in-time data, so I can compare their decisions and results side by side. The app uses returns, risk-adjusted performance, and the current market regime to choose a strategy for a separate portfolio to follow. I wanted that selection to account for risk as well as profit.

The app also uses ML to forecast returns and volatility. In the desktop interface, I can inspect those forecasts, strategy rankings, portfolio changes, and the evidence behind each selection. I wanted to be able to follow how each result was reached. The [validation report](https://github.com/Oscar-G-Rodriguez/ROMULUS/blob/main/VALIDATION_REPORT.md) shows how I checked the backtester and its model outputs.

[Repository](https://github.com/Oscar-G-Rodriguez/ROMULUS) &nbsp;·&nbsp; [Validation report](https://github.com/Oscar-G-Rodriguez/ROMULUS/blob/main/VALIDATION_REPORT.md)

---

<a name="florida-policy-advisor"></a>

### Florida Policy Advisor

**Python · FastAPI · BLS / Census / FRED · Data provenance**

I built Florida Policy Advisor to help people explore Florida labor, housing, and fiscal indicators in a local app. It brings data from sources such as BLS, Census, and FRED into one place. Each refresh checks data quality and coverage, and the results retain their source and retrieval date. The app also compares forecasting baselines on historical data and lets users explore policy options with visible weights.

I wanted people to be able to trace a result back to the underlying data and see how the comparison was made. Building it gave me more experience with everything from collecting data to presenting an answer. The project's [evidence and checks](https://github.com/Oscar-G-Rodriguez/florida_policy_advisor/blob/main/portfolio_evidence/README.md) are documented in its repository.

[Repository](https://github.com/Oscar-G-Rodriguez/florida_policy_advisor) &nbsp;·&nbsp; [Evidence and checks](https://github.com/Oscar-G-Rodriguez/florida_policy_advisor/blob/main/portfolio_evidence/README.md)

<a name="roles"></a>

## Current roles at UF

| Organization | Role | Focus |
| :--- | :--- | :--- |
| Data Science & Informatics | Project Team Member — DSI x NVIDIA Basketball Shot Quality Analysis | Team project on estimating shot quality from player spacing and shooter biomechanics |
| ColorStack UF | Machine Learning Engineer — Knowledge Graph | Assigned backend and API work for a graph intended to support AI agents |
| Software Engineering Club | Sponsorship Lead | Company outreach and potential event speakers |
| ColorStack UF | Corporate Outreach Lead | Corporate outreach under the chapter's VP Corporate |

[My roles on LinkedIn](https://www.linkedin.com/in/oscar-g-rodriguez/)

---

[Back to top](#top) &nbsp;·&nbsp; [Browse all repositories](https://github.com/Oscar-G-Rodriguez?tab=repositories) &nbsp;·&nbsp; [Connect on LinkedIn](https://www.linkedin.com/in/oscar-g-rodriguez/)
