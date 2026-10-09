# Kore Studio Pilates: AI-Driven Biomechanical Analysis

**Kore Studio** is a B2B SaaS platform designed to optimize biomechanics in Pilates studios. We deploy multimodal LLMs to process user telemetry, assess kinematic alignment in real-time, and generate hyper-personalized, injury-preventive microcycles.

## Core Architecture & AI Stack

*   **Frontend / UI:** React.js dashboard for Pilates instructors.
*   **Backend:** Node.js / Express for API orchestration.
*   **Computer Vision Engine:** Proprietary pose-estimation models pre-processing visual data (reformer/cadillac execution).
*   **Core LLM (Reasoning & Vision):** **Anthropic Claude 3.5 Sonnet**. Selected strictly for its superior multimodal reasoning, eliminating anatomical hallucinations during pose analysis and leveraging its 200k token window for dense clinical histories.
*   **Vector Database (RAG):** Pinecone. Indexing peer-reviewed literature on clinical biomechanics, physiotherapy, and historical client data.

## Key Modules

| Module | Technical Description | Dependency / LLM |
| :--- | :--- | :--- |
| **Kinematic Assessment** | Processes visual frames to detect pelvic retroversion, spinal misalignment, and joint compression risks during exercise. | Claude 3.5 Sonnet (Vision API) |
| **Adaptive RAG Engine** | Cross-references user mobility limitations with indexed academic literature to prescribe progressive overload routines. | Claude 3.5 Sonnet + Pinecone |
| **Predictive Churn Agent** | NLP analysis of post-class feedback and attendance time-series to identify at-risk clients and auto-adjust routines. | Claude 3.5 Sonnet + Python |

## Academic Validation
Our baseline models and injury-prevention protocols are currently in the validation phase, leveraging research methodologies and biomechanical literature indexing stemming from the **Universidad Nacional Mayor de San Marcos (UNMSM)** ecosystem.

## Setup & Deployment
*(Internal use only - Private Alpha)*
1. Clone the repository.
2. Configure `.env` with `ANTHROPIC_API_KEY` and `PINECONE_API_KEY`.
3. Run `npm install` and `npm run dev`.
