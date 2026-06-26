# Rahi - Full Info Dump (Resume Research)

> Source: Resume V6, codebase exploration (~75 projects), memory files  
> Last updated: 2026-06-26

---

## PERSONAL INFO

| Field | Value |
|-------|-------|
| **Name** | Md Raihanul Haque Rahi |
| **Email** | raihanulhaque007@gmail.com |
| **Phone** | +8801725737812 |
| **Portfolio** | https://cortextech.dev/engineer/rahi/ |
| **GitHub** | https://github.com/raihanulhaque |
| **LinkedIn** | https://linkedin.com/in/raihanulhaque |
| **Codeforces** | Rating 1280, Pupil |
| **YouTube** | Rahi 404 — tech channel covering Python, ML, AI engineering; focused on Bengali-speaking developers |

---

## EDUCATION

**Bachelor of Science in Mechatronics Engineering**  
Rajshahi University of Engineering & Technology (RUET)  
March 2022 — August 2026 (expected)

---

## WORK EXPERIENCE

### Resume Summary Direction
- AI engineer working across agentic backends, real-time voice systems, and edge/on-device ML
- Avoid "final-year student" framing because graduation is near; education already provides the timeline
- Tone should be modern, focused, and systems-oriented rather than generic student/resume phrasing

### Intelsense AI | Backend Engineer
**April 2024 – Present**
- Owns backend architecture for an AI-powered SaaS platform
- Django + PostgreSQL systems, focus on modularity, reliability, scale
- Integrated production LLM, ASR, and TTS inference pipelines into the web backend
- Enables real-time AI voice and text interaction features at the product layer

### Cortex Technologies | ML Engineer
**January 2024 – Present** | Contract / Freelance Collaboration  
Context: Collaborative client-project work with Abrar/Cortex Technologies. Abrar sources freelance/client projects; Rahi owns the ML/AI engineering portion. This should not be framed as a funded startup or formal company employment.

- Owns ML engineering for client projects: custom YOLO-based detection pipelines, stereo depth estimation, and real-time vision inference on resource-constrained edge hardware
- Builds language-model and automation components for client workflows, including model selection, prompt/tool orchestration, quantization (TFLite/ONNX), and deployment on edge devices

### Outlier | AI Trainer, Quality Reviewer
**September 2024 – December 2024**
- Evaluated and corrected AI-generated solutions across mathematics and code
- Contributed to measurable improvement in model reasoning accuracy

### Remotasks | LLM Dataset Inspector
**July 2023 – January 2024**
- Audited LLM training datasets across multiple programming languages
- Enforced data quality standards for code-generation fine-tuning pipelines

---

## SKILLS

### Languages
Python (primary), C/C++, Dart/Flutter, Rust, Swift, SQL
> Removed from resume: Go (not used enough). JS/TypeScript not included — not comfortable coding in JS.

### Frameworks & Libraries
- **Backend:** FastAPI, Django, Flask
- **Mobile:** Flutter (iOS/Android)
- **ML/AI:** PyTorch, TensorFlow, MLX (Apple Silicon), HuggingFace, LangChain
- **Data:** NumPy, Pandas, SQLModel

### AI/ML Specializations
- Voice AI: VAD, ASR, TTS, real-time speech pipelines
- Computer Vision: YOLO, stereo depth estimation, object detection
- LLM Integration: provider-agnostic LLM APIs, RAG, Groq-hosted inference, function/tool calling, AI agents
- On-device inference: TFLite, MLX, ONNX, quantization (3–8 bit)
- Edge AI: model optimization, deployment on resource-constrained hardware

### Databases
PostgreSQL, Supabase, Redis, Firebase
> MongoDB not included — not a primary tool.

### Infrastructure
Docker, Docker Compose, WebRTC, WebSocket, LiveKit, FastRTC

### Audio/Speech Models
Parakeet (NeMo), Whisper, Kokoro, Qwen3-TTS, ElevenLabs, Deepgram, Silero VAD

### LLMs Used
GPT-family APIs, provider-hosted LLM APIs, Groq-hosted models, local models (MLX-based)

---

## PROJECTS

> Current resume order: Gesprek → StereoLite → Hishab → Diet Engine  
> Perceptron remains a backup/optional project, but is omitted from the compact one-page resume.

### Gesprek — AI Voice Agents Platform
**Status:** Built/deployed as a full product prototype; now archived/shut down after feasibility and market constraints  
**Stack:** FastAPI, Supabase, PostgreSQL, Redis, Docker, ElevenLabs, LiveKit
- Built with a friend as an end-to-end voice-agent product, including domain, deployment, backend, auth, subscriptions, and voice infrastructure
- Project was discontinued after validation due to investment constraints, technical feasibility issues, and local-market fit concerns
- Enables configurable, niche-specific multi-agent voice deployments
- Modular FastAPI backend, Supabase auth, Redis-backed real-time TTS (ElevenLabs)
- Multi-tenant agent orchestration, subscription management
- Containerized with Docker Compose; independently scalable services
> Note: Has a React/TypeScript frontend but Rahi mainly works on the backend/AI side

### StereoLite — Lightweight Stereo Depth Estimation (Thesis)
**Status:** Active research  
**Stack:** PyTorch, ONNX  
- Under-3M-parameter stereo matching model — no foundation model dependency
- More than 10× smaller than DEFOM-Stereo (<3M vs 30M+ params)
- 4× less VRAM: 1.5GB vs 6GB at 720p
- Multi-level GRU hierarchy (3 scales: 1/4, 1/8, 1/16)
- EPE 0.57 in 1,600 training steps
- Decouples DEFOM architectural innovations from frozen DINOv2 backbone
- Convex upsampling for sharp edges, 22 iterative refinement steps
- Exported to ONNX

### Hishab — Agentic Expense Tracking App
**May 2024 – August 2025**  
**Stack:** Flutter, FastAPI, agentic LLM workflows, Supabase, SQLModel
- Tracks income/expenses through natural-language prompts in Banglish (Bengali+English)
- Agent/tool-calling workflow for AI-driven financial parsing, categorization, and record creation
- Full auth, user isolation (row-level security), SMTP integration
- Has both Flutter mobile app and companion web frontend

### Diet Engine — AI Nutrition Coach & Calorie Tracker
**February 2024 – May 2024**  
**Stack:** Flutter, FastAPI, Firebase, PyTorch
- Food recognition with server-side PyTorch models
- Full-stack: Firebase auth, calorie tracking, nutrition analysis
- **Published:** [https://doi.org/10.1016/j.focha.2025.100978](https://doi.org/10.1016/j.focha.2025.100978)  
  Food Chemistry Advances (Elsevier, 2025)

### Perceptron — On-Device Image Classifier App
**November 2025**  
**Stack:** Flutter, tflite_flutter
- Model-agnostic TFLite inference engine
- Error-adaptive backend-swap architecture
- Runs entirely on-device; no server dependency
- Supports YOLO-based detection and class prediction

### Other Notable Projects (not on current resume)

**Voice Agent System** — FastAPI, WebSocket, ElevenLabs (Scribe v2 ASR, Turbo v2.5 TTS), OpenAI  
- Autonomous continuous listening with 1.5s VAD silence detection
- Real-time ASR → LLM → TTS pipeline with function calling and multi-turn context

**LiveKit Voice AI** — LiveKit, Deepgram STT, ElevenLabs TTS, Next.js  
- SIP API for phone number management (Redis, JWT auth)
- Full telephony integration

**Glyph** — Swift, MLX, Parakeet-TDT (0.6b-8bit), Silero VAD  
- Real-time macOS dictation app on Apple Silicon
- Streaming TDT, app-aware text insertion, self-correcting cumulative pipeline

**KIBO25-ML** — YOLOv11, OpenCV, TFLite  
- Object detection for JAXA Kibo Robot Programming Challenge
- yolo11m.pt + TFLite conversion + preprocessing pipeline

**Llama3 From Scratch** — PyTorch  
- Llama3 architecture implemented tensor-by-tensor
- Custom tokenizer (minBPE), model weight loading

**AgentHub** — FastAPI, Docker Compose, PostgreSQL  
- Multi-agent microservices orchestration platform

---

## OPEN SOURCE CONTRIBUTIONS

### Microsoft / VibeVoice (40,000+ stars)
- State-of-the-art voice synthesis model with emotional control
- Contributed: package import support (PR merged, 2024)

---

## PUBLICATIONS

**Diet Engine: A real-time food nutrition assistant system for personalized dietary guidance**  
Published in Food Chemistry Advances (Elsevier, 2025)  
DOI: [https://doi.org/10.1016/j.focha.2025.100978](https://doi.org/10.1016/j.focha.2025.100978)

---

## AWARDS & LEADERSHIP

### Kibo Robot Programming Challenge 2025
- **1st place** in Bangladesh regional (2025)
- **4th place globally** (2025)
- Improved from 2nd place (232.9 points) in 2024
- Programmed Astrobee robots for zero-gravity navigation and AR object recognition on ISS

### Rahi 404 — YouTube Channel
- Technical channel covering Python, ML, AI engineering
- Focused on making programming and ML accessible to Bengali-speaking developers

### Coding Club Leadership
- Led student coding club at RUET
- Taught first-year students C/C++, algorithmic problem-solving, provided mentorship

### Team "Cortex" — National Robotics Competition
- Kambali-RUET Toolkit 2022
- Designed, built, and presented a fully autonomous vision-guided 6-DOF robotic arm

---

## ADDITIONAL CONTEXT

- Competitive programming: Codeforces 1280 (Pupil)
- Comfortable with Banglish NLP (Bengali+English mixed input)
- Experience with Apple Silicon optimization (MLX, on-device inference)
- Background in signal processing (DSP + machine vision coursework at RUET)
- Builds AI agents, voice agent pipelines, real-time telephony integrations
- NeRF/3D reconstruction (NERF_Project, NeuroDepth — exploratory)
- Self-described: curiosity-driven, clean code, ships production systems

---

## TECH TAGS (for ATS/keyword optimization)

Python, FastAPI, Django, Flutter, Dart, Rust, Swift, PostgreSQL, Supabase, Redis, Docker, PyTorch, TensorFlow, MLX, HuggingFace, LangChain, LLM APIs, RAG, AI agents, tool calling, ElevenLabs, Deepgram, Groq, WebRTC, LiveKit, FastRTC, WebSocket, Silero VAD, Whisper, Parakeet, Kokoro TTS, YOLO, OpenCV, TFLite, ONNX, Apple Silicon, Edge AI, Microservices, Git, C++, SQL, Competitive Programming
