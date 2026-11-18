# Rahi - Full Info Dump (Resume Research)

> Source: Resume (Nov 2026), codebase exploration (~75 projects), memory files  
> Last updated: 2026-11-17

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
2022 — 2026
CGPA: 3.16/4.00

---

## WORK EXPERIENCE

### Resume Summary Direction
- Plain, industry-standard tone; no "I", no self-promotion, no buzzword stacking
- Current summary: "AI Engineer with 2+ years of experience building and deploying LLM applications, including RAG chatbots, AI agents, and recommendation systems serving millions of users in fintech and media. Experienced in optimizing models for on-device inference on mobile and edge devices with llama.cpp, TFLite, and ONNX."
- Rules: max 3 bullets per job on the resume; keep Outlier/Remotasks entry; Sysnova/Dhaka not repeated in the summary

### Sysnova Information Systems | AI Engineer
**October 2026 – Present** | Dhaka, Bangladesh
- Built a RAG chatbot for Prime Bank's MFS Lenden (~700k users)
- Built a recommendation engine for the Deepto Play OTT platform (8.7M total users, ~1M active); code folder: `novasight`
- Built nova-gate, an internal AI coding gateway on LiteLLM + OpenRouter: routes each request to cheap/mid/strong model tiers, per-developer keys and budgets. The JEV decision model (TypeSafe AI, hosted classifier, provider `jev`, model `jev-latest`, key `TYPESAFE_API_KEY`) is wired in as `nova-auto-jev` for A/B testing only; the default router is LiteLLM's heuristic classifier (`nova-auto`)
- Built an AI agent for internal LibreOffice Writer and Calc with an AI helper for spreadsheet and document work; code folder: `cellscribe`
- Resume shows these as 3 bullets (Lenden + Deepto Play merged; gateway; LibreOffice agent)

### Intelsense AI | Backend Engineer
**April 2024 – September 2026** (left in September)
- Owns backend architecture for an AI-powered SaaS platform
- Django + PostgreSQL systems, focus on modularity, reliability, scale
- Architects production RAG services with structured ingestion and retrieval flows, resilient failure handling, and reliable product-facing APIs
- Builds OCR and ASR data-collection pipelines
- Integrates LLM, speech, and document-processing capabilities into the web backend

### Cortex Technologies | ML Engineer
**January 2024 – Present** | Contract / Freelance Collaboration  
Context: Hobby company with friends that takes freelance work occasionally (still active; resume label "Freelance Collaboration"). Collaborative client-project work with Abrar/Cortex Technologies. Abrar sources freelance/client projects; Rahi owns the ML/AI engineering portion. This should not be framed as a funded startup or formal company employment.

- Owns ML engineering for client projects: custom YOLO-based detection pipelines, stereo depth estimation, and real-time vision inference on resource-constrained edge hardware
- Built an automated object-detection dataset generation pipeline using SAM 3: users provide labels, the model generates object bounding boxes, and annotations are exported in COCO dataset format
- Optimizes and deploys models on resource-constrained hardware using TFLite, ONNX, and quantization techniques

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
Python (primary), C/C++, Dart/Flutter, Rust, Swift, Kotlin, SQL
> Removed from resume: Go (not used enough). JS/TypeScript not included — not comfortable coding in JS.

### Frameworks & Libraries
- **Backend:** FastAPI, Django, Flask
- **Mobile:** Flutter (iOS/Android)
- **ML/AI:** PyTorch, TensorFlow, MLX (Apple Silicon), HuggingFace, LangChain, LiteLLM, llama.cpp
- **LLM gateways:** OpenRouter, LiteLLM
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
Docker, Docker Compose, WebRTC, WebSocket, LiveKit

### Audio/Speech Models
Parakeet (NeMo), Whisper, Kokoro, Qwen3-TTS, ElevenLabs, Deepgram, Silero VAD

### LLMs Used
GPT-family APIs, provider-hosted LLM APIs, Groq-hosted models, local models (MLX-based)

---

## PROJECTS

> Current resume order: Kiln → StereoLite → AgriSense → Hishab → Gesprek (ordered by impact; Hishab is a Kiln demo so it sits lower)  
> Diet Engine was removed from Projects because the paper already covers it (see Publications).  
> Perceptron remains a backup/optional project, but is omitted from the resume.

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
- Decouples iterative multi-scale GRU refinement from a frozen DINOv2 backbone to reduce compute and memory costs while preserving depth-refinement quality across scales
- Convex upsampling for sharp edges, 22 iterative refinement steps
- Exported to ONNX

### Kiln — On-Device LLM Runtime
**October 2026 – Present** | https://github.com/RaihanulHaque/kiln  
**Stack:** C/C++, llama.cpp, Flutter, Kotlin, Rust, React Native
- Open-source on-device runtime for Android and desktop (iOS in progress); chat, decision, embedding, speech-to-text (Whisper, Parakeet, Qwen3-ASR) and text-to-speech (Pocket TTS) through one C API
- Bindings: Flutter (`kiln_flutter` on pub.dev), Kotlin, Rust, React Native
- Acceleration detected at runtime, never assumed; plain Armv8 CPU build for phones without dot-product support; reports backend, memory, real tokens/s
- 505 C checks across Android, macOS, Linux; tested on Pixel 8, Galaxy S26 Ultra, M4 Pro MacBook

### AgriSense — Autonomous Agricultural Advisor
**IUT Hackathon** | LangGraph, RAG, FastAPI
- Multi-agent system that plans a farmer's season (costs, weather) and keeps advising; real government soil/weather/crop data by district and upazila; crop leaf-disease classifier; deployed at agrisense.cortextech.dev

### Hishab — Offline AI Expense Tracker
**May 2024 – Present**  
**Stack:** Python, PyTorch, Qwen3.5-0.8B, GGUF, Kiln, Flutter
- Fine-tuned Qwen3.5-0.8B to turn English, Bangla, Banglish and mixed messages into structured income/expense records; offline Android app (`hishab-offline`), model runs on-device through Kiln, no server, no account
- Latest model v13-trim38k-L20 (published 2026-11-17): vocabulary trimmed 248k → 38k tokens, then 4 of 24 layers pruned (8, 9, 12, 13) and healed by distillation from v13. Q4_K_M-imat 288 MB (v13: 343 MB; v10: 529 MB), 94.4% exact-match on test_clean_v2 (v13: 94.2%), 89.9% on spelled-out amounts. Pixel speed not yet measured for L20; v13 runs ~51 tokens/s on a Pixel 8, and the app still ships v13. HF: `ryuma007/hishab-qwen3.5-0.8b-pipe-signed-full-v13-trim38k-L20-GGUF`. Source: `hishab` repo `ml/results/EXPERIMENTS.md`
- Résumé shows: 51 tok/s on Pixel 8 (v13), and 529 MB → 288 MB with no measurable accuracy loss, 94.4% exact-match
- Relabelled training data against a written labelling guideline (two independent labellers in v10)
- Older version: Flutter + FastAPI + Gemini function calling + Supabase (`hishab_app`)

### Diet Engine — AI Nutrition Coach & Calorie Tracker (removed from resume Projects; paper stays)
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

Python, FastAPI, Django, Flutter, Dart, Rust, Swift, Kotlin, LiteLLM, OpenRouter, llama.cpp, GGUF, PostgreSQL, Supabase, Redis, Docker, PyTorch, TensorFlow, MLX, HuggingFace, LangChain, LLM APIs, RAG, AI agents, tool calling, ElevenLabs, Deepgram, Groq, WebRTC, LiveKit, WebSocket, Silero VAD, Whisper, Parakeet, Kokoro TTS, YOLO, OpenCV, TFLite, ONNX, Apple Silicon, Edge AI, Microservices, Git, C++, SQL, Competitive Programming
