# Inpact: AI-Powered Creator Collaboration & Sponsorship Matchmaking Platform

## Project Overview
**Inpact** : AI-powered platform designed to connect content creators, brands, and agencies through data-driven insights. It enables influencers to discover relevant sponsorship deals, collaborate with like-minded creators, and optimize brand partnerships.

### Key Features:
- **AI-Driven Sponsorship Matchmaking**: Matches creators with brands based on audience demographics and engagement.
- **AI-Powered Creator Collaboration Hub**: Connects creators for joint projects and cross-promotions.
- **AI-Based Pricing & Deal Optimization**: Provides fair sponsorship pricing using market insights.
- **AI-Powered Negotiation & Contract Assistant**: Structures deals and generates contracts via AI.
- **Performance Analytics & ROI Tracking**: Monitors sponsorship effectiveness and audience engagement.

---

## Tech Stack

### Frontend:
- **ReactJS**: UI development framework.
- **Tailwind CSS**: Styling for responsive design.
- **ShadCN/UI**: Modern UI components.
- **Framer Motion**: Animations.

### Backend:
- **FastAPI**: High-performance backend framework.
- **Python**: Core backend language.

### Database & Storage:
- **Supabase**: PostgreSQL-based backend as a service.
- **Redis**: Caching and real-time analytics.

### AI & Analytics:
- **Generative AI (LangChain, OpenAI API, or Local Models)**: AI-driven matchmaking & negotiation.
- **Vector Databases (Weaviate, Pinecone, or ChromaDB)**: Similarity searches for sponsorship recommendations.

### DevOps & Deployment:
- **Docker**: Containerization.

---

## Architecture Diagram
```mermaid
graph TD;
    A[Frontend - ReactJS] -->|API Requests| B[FastAPI Backend]
    B -->|Auth & User Data| C[Supabase]
    B -->|AI Processing| D[GenAI Engine]
    B -->|Sponsorship Matching| E[Vector DB]
    B -->|Campaign Analytics| F[DataStax]
    F -->|Real-time Caching| G[Redis]
    D -->|Pricing & Contract AI| H[LLM API / Local Model]
    subgraph AI Services
        D
        H
        I
    end
    subgraph Backend Services
        B
        C
        E
        F
        G
    end
    subgraph Frontend Services
        A
    end
```

---

## Workflow Diagram
```mermaid
sequenceDiagram
    participant Creator
    participant Frontend
    participant Backend
    participant AI Engine
    participant Database
    participant Brand

    Creator->>Frontend: Request sponsorship opportunities
    Frontend->>Backend: Send user data & preferences
    Backend->>AI Engine: Process matchmaking request
    AI Engine->>Database: Retrieve creator's analytics
    AI Engine->>Database: Retrieve brand sponsorship data
    Database->>AI Engine: Return relevant data
    AI Engine->>Backend: Return best sponsorship matches
    Backend->>Frontend: Send sponsorship opportunities
    Frontend->>Creator: Display sponsorship options

    Creator->>Frontend: Accept sponsorship deal
    Frontend->>Backend: Confirm selection
    Backend->>AI Engine: Optimize pricing & contract terms
    AI Engine->>Backend: Return contract details
    Backend->>Brand: Send proposal for approval
    Brand->>Backend: Approve/reject deal
    Backend->>Frontend: Send final decision
    Frontend->>Creator: Display result
```

---
