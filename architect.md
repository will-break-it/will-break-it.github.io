---
layout: default
title: William Wolff - Technical Architect
permalink: /architect/
---

<nav class="resume-nav">
  <a href="/">Full CV</a>
  <a href="/product-engineer">Product Engineer</a>
  <a href="/engineering">Engineer</a>
  <span class="active">Architect</span>
  <a href="/master-cv">Master CV</a>
</nav>

# WILLIAM WOLFF
**Technical Architect & Solutions Architect**

Berlin, DE | [linkedin.com/in/wwolff](https://linkedin.com/in/wwolff) • [github.com/will-break-it](https://github.com/will-break-it)

![Experience](https://img.shields.io/badge/Experience-10%2B%20Years-2196F3?style=flat) ![Location](https://img.shields.io/badge/Location-Berlin%2C%20DE-4CAF50?style=flat) ![Focus](https://img.shields.io/badge/Focus-Architecture%20%26%20Strategy-9C27B0?style=flat)

---

## PROFILE

Technical architect with 10+ years designing and implementing large-scale distributed systems, blockchain infrastructure, and high-performance applications. Expert at translating complex technical challenges into elegant architectural solutions that deliver measurable business value - 45% latency reduction, 60%+ cost savings, €6M annual savings.

Proven ability to make strategic technical decisions that balance innovation with pragmatism. Experience spans protocol design, system architecture, team coordination, and technical leadership. Strong track record of authoring technical specifications (CIPs), designing greenfield systems, and re-architecting legacy platforms for scale.

**Core strengths:** System design • Technical strategy • Architecture documentation • Cross-team coordination • Performance optimization • Technology evaluation • Risk assessment • Team mentorship

---

## ARCHITECTURAL EXPERTISE

**System Design:**
- Distributed systems architecture
- Event-driven architectures
- Microservices design
- Real-time data pipelines
- Blockchain infrastructure
- High-availability systems
- Performance optimization
- Scalability planning

**Technical Leadership:**
- Architecture decision records (ADRs)
- Technical specifications and CIPs
- Technology evaluation and selection
- Cross-functional team coordination
- Technical risk assessment
- Documentation and knowledge sharing
- Mentoring engineers

**Technologies:** TypeScript • Rust • Java • PostgreSQL • Redis • Docker • Terraform • gRPC • WebSocket • Blockchain protocols

---

## EXPERIENCE

### **Technical Architect – [Lace Wallet](https://www.lace.io/)**
**Input Output Global (IOG)** • *Remote* • <span class="date">Nov 2022 - Nov 2024</span>

Architected backend infrastructure and led technical strategy for Cardano's flagship wallet product, delivering measurable improvements in performance and cost efficiency.

**Backend Architecture Redesign:**
- **Strategic Decision:** Identified poll-based architecture as bottleneck for user experience and cost
- **Solution Design:** Re-architected to event-driven system using PostgreSQL LISTEN/NOTIFY
- **Business Impact:** 45% latency reduction, >60% infrastructure cost savings
- **Implementation:** Led migration with zero downtime, coordinated across 3 teams
- **Documentation:** Created architecture decision records (ADRs) documenting rationale and trade-offs

**Chain Indexer Architecture:**
- **Problem:** Generic blockchain indexers insufficient for wallet-specific query patterns
- **Design:** Purpose-built indexer optimized for wallet use cases
  - Bloom filters for fast credential membership testing
  - Credential-based indexing reducing query complexity
  - Parallel ingestion pipeline achieving >2,000 tx/s throughput
- **Standardization:** Authored [CIP proposal](https://github.com/will-break-it/wallet-architecture/tree/main/docs/CIP/CIP-XXXX) for wallet indexing standards
- **Result:** Sub-second wallet sync times, ecosystem-wide adoption of patterns

**Feature Development Leadership:**
- **MetaDex Integration:** Led architectural design for DEX aggregation feature
  - NestJS microservice with gRPC for real-time price feeds
  - WebSocket connections for live swap quotes
  - Transaction construction pipeline for multi-step swaps
  - Coordinated with external partners on API integration
- **Team:** Led 7-person cross-functional team (3 FE, 2 BE, 1 QA, 1 PM)
- **Outcome:** First revenue stream for Lace wallet product

**Technical Decision-Making:**
- Evaluated trade-offs between SQL and NoSQL for chain data (chose PostgreSQL for ACID guarantees)
- Selected NestJS over alternatives for team familiarity and ecosystem
- Designed caching strategy balancing freshness with performance
- Established monitoring and alerting standards for production systems

**Technologies:** TypeScript • NestJS • PostgreSQL • Event-driven architecture • Bloom filters • gRPC • System design

---

### **R&D Innovation Lead & Technical Architect – [Ouroboros Leios](https://www.youtube.com/watch?v=YEcYVygdhzU)**
**Input Output Global (IOG)** • *Remote* • <span class="date">Nov 2024 - Present</span>

Leading architecture and technical strategy for high-throughput overlay protocol, coordinating research and engineering teams toward mainnet implementation.

**Protocol Architecture:**
- **Authored [CIP-0164](https://github.com/cardano-scaling/CIPs/blob/leios/CIP-0164/README.md):** Comprehensive protocol specification
  - Defined protocol layers and interfaces
  - Documented consensus mechanisms and data structures
  - Specified node behavior and network protocol
  - Created diagrams and visual architecture representations
- **Decision Framework:** Established decision log tracking architectural choices and rationale
  - Trade-offs between throughput and latency
  - Security considerations and attack vectors
  - Backward compatibility with existing Cardano protocol
  - Migration strategy for mainnet deployment

**Team Coordination:**
- **Cross-Functional Leadership:** Direct 8-person team across formal methods, research, and engineering
- **Process Design:** Established workflows bridging research and implementation
  - Weekly syncs aligning on priorities and blockers
  - Monthly public demos maintaining stakeholder visibility
  - Quarterly planning sessions for milestone definition
- **Workshop Facilitation:** Organized week-long on-site workshop
  - Reduced open research questions through collaborative problem-solving
  - Aligned team on implementation strategy
  - Created shared technical vision

**Strategic Planning:**
- **Simulation-Driven Development:** Designed approach validating protocol before mainnet
- **Risk Assessment:** Identified critical path items and technical risks
- **Stakeholder Communication:** Translated research complexity for product and business teams

**Technologies:** Protocol design • Distributed systems • Formal methods • Technical specification

---

### **Solutions Architect**
**Input Output Global (IOG)** • *Remote* • <span class="date">Nov 2021 - Nov 2022</span>

Designed blockchain architecture solutions for enterprise clients and educated engineers on Cardano's technical model.

**Smart Contract Architecture:**
- **CDP Platform Design:** Architected complete Plutus smart-contract stack for collateralized debt positions
  - On-chain contract design for collateral management
  - Off-chain infrastructure for price feeds and liquidations
  - Transaction construction for multi-party scenarios
  - Risk modeling for over-collateralization ratios
- **eUTxO Patterns:** Developed reusable architecture patterns for eUTxO model
  - State machine implementations in Plutus
  - UTXO threading for sequential state updates
  - Datum/redeemer design patterns

**Technical Education:**
- **Workshop Design:** Created curriculum for Cardano architecture education
- **Amazon Partnership:** Conducted workshops for 100+ Amazon engineers
  - eUTxO model vs. account-based blockchains
  - Smart contract architecture on Cardano
  - dApp design patterns and best practices
- **Knowledge Transfer:** Built training materials and hands-on exercises

**Technologies:** Haskell • Plutus • Smart contracts • Architecture patterns • Technical education

---

### **Migration Lead & Architect – Deloitte**
**Senior Software Engineer** • <span class="date">Sep 2016 - Nov 2019</span>

Architected large-scale migration toolchain transforming 16M LoC legacy system, delivering €6M annual cost savings.

**Migration Architecture:**
- **Problem:** Major insurance company locked into proprietary platform with high licensing costs
- **Solution Design:** 3-stage automated migration pipeline
  1. **Parser:** Custom DSL parser generating abstract syntax tree (AST)
  2. **Transformer:** AST manipulation preserving business logic semantics
  3. **Generator:** Code generation producing equivalent Java 8 code
- **Runtime Layer:** Built compatibility layer ensuring behavioral equivalence
- **Result:** €6M annual license cost savings while maintaining functionality

**Testing Strategy:**
- **Differential Testing Architecture:** Designed framework comparing old vs. new system outputs
  - Processed millions of test cases
  - Automated regression detection
  - Achieved >99.9% compatibility rate
- **End-to-End Testing:** Architected comprehensive testing approach across system integration

**Technical Leadership:**
- **Team Growth:** Grew team from 3 → 20 engineers
- **Promotion:** Advanced to lead architect within 24 months
- **Knowledge Sharing:** Established documentation standards and code review practices
- **Offshore Coordination:** Coordinated with India delivery team on implementation

**Technologies:** Java 8 • Compiler design • AST manipulation • Migration architecture • Testing frameworks

---

## ARCHITECTURAL CONSULTING & SIDE PROJECTS

### **Dump it! – Cross-Platform Application Architecture** • <span class="date">2023 - Present</span>

Designed unified architecture across iOS (Swift), Android (Kotlin), and Web (React) platforms with sophisticated AI processing pipeline.

**Event-Sourced Processing Architecture:**
- **Design Pattern:** Event sourcing with immutable event stream for complete audit trail
- **Task-Based Pipeline:** Async processing with specialized tasks (transcribe → ingest → extract → match → resolve → execute)
- **Real-Time Streaming:** Server-Sent Events (SSE) for non-blocking client experience
- **Transactional Guarantees:** All entity operations in single DB transaction for atomicity
- **Architectural Benefits:** Enables undo, conflict replay, debugging via event stream

**Two-Phase LLM Pipeline Design:**
- **Phase 1 - Intent Classification:**
  - Claude Haiku for semantic separation and intent detection
  - Prompt engineering: Cached static sections (role, rules, examples), dynamic context (recent entities, timezone)
  - Structured JSON output with validation
  - Cost optimization: Haiku for speed/cost, prompt caching reduces token usage
- **Phase 2 - Conflict Resolution:**
  - LLM analyzes ambiguous cases with statistical context (match scores, gap analysis, reasoning)
  - Decides: execute directly vs. request user clarification
  - Handles semantic intent (is "add milk" creating new todo or updating existing grocery list?)

**Adaptive Vector Search Architecture:**
- **Embedding Strategy:** Sentence transformers (768-dim) for semantic similarity
- **Match Quality Analysis:** Statistical decision-making
  - Dynamic quality floor: `max(0.1, min(0.4, mean - stddev * 0.8))`
  - Clear winner threshold: `stddev * multiplier` (1.2 base, 1.8 for DELETE safety)
  - Gap analysis between top matches for ambiguity detection
- **Intelligent Filtering:** Excludes completed todos, past reminders (>48h grace period)
- **Recency Bias:** +0.1 boost for entities updated <24h (balances semantic similarity with temporal relevance)

**Routing & Decision Framework:**
- **CREATE intents** with matches → LLM decides CREATE vs UPDATE
- **UPDATE/DELETE** with single clear match → Direct execution
- **Ambiguous matches** (gap ≤ threshold) → User clarification
- **DELETE** requires higher confidence (1.5x threshold) for safety

**Offline-First Design:**
- Local-first data model with eventual consistency
- SQLite (mobile) and IndexedDB (web) for local storage
- Persistent queue for reliable sync
- Conflict resolution for concurrent edits

**End-to-End Encryption:**
- Zero-knowledge architecture - backend cannot decrypt user data
- Diffie-Hellman key exchange for secure key establishment
- AES-256-GCM encryption for data at rest

**Cross-Platform Consistency:**
- Unified data model and API contracts across iOS, Android, Web
- Shared business logic via backend API
- Platform-specific UX with consistent functionality

**Technologies:** Swift • Kotlin • React • TypeScript • NestJS • PostgreSQL • pgvector • Claude Haiku • Sentence Transformers • Event-sourcing • Cryptography

---

### **Drip Dropz – NFT Marketplace Architecture** • <span class="date">2022 - 2024</span>

**System Design:**
- **Frontend Architecture:** React SPA with background web worker for chain sync
  - Separation of UI thread from blockchain processing
  - Event-driven state updates
  - Optimistic UI updates with rollback on failure
- **Transaction Construction:** UTXO management and coin selection algorithms
- **Smart Contract Integration:** Plutus contract interaction patterns
- **DevOps:** CI/CD pipeline with automated testing and deployment

---

### **Berlin Pool – Infrastructure Architecture** • <span class="date">2021 - 2024</span>

**High-Availability Design:**
- Redundant node topology for 99.9% uptime
- Automated failover mechanisms
- Backup and disaster recovery procedures

**Security Architecture:**
- Air-gapped cold key storage for operational security
- Secure key rotation procedures
- Network segmentation and firewall rules

**Infrastructure as Code:**
- Terraform for reproducible deployments
- Ansible for configuration management
- Monitoring stack (Prometheus, Grafana) for observability

---

## EDUCATION

**Bachelor of Science in Computer Science**
*DHBW Stuttgart* • Germany • <span class="date">2011 - 2014</span>

**International Business**
*Hult International Business School* • San Francisco, CA • <span class="date">2014 - 2015</span>

---

## ARCHITECTURAL PHILOSOPHY

**Strategic Decision-Making:**
- Document architectural decisions with ADRs capturing context and trade-offs
- Balance innovation with pragmatic delivery timelines
- Consider operational costs alongside development complexity
- Design for measurable outcomes (latency, cost, scalability)

**Team Enablement:**
- Create clear technical documentation for team alignment
- Establish patterns and standards for consistent implementation
- Mentor engineers on system thinking and design principles
- Foster collaboration across research, engineering, and product

**Continuous Improvement:**
- Measure architecture effectiveness through metrics
- Iterate based on production learnings
- Stay current with industry patterns and emerging technologies
- Share knowledge through specifications, workshops, and documentation

I'm looking for roles where architectural decisions have significant impact on company success, technical challenges require deep system thinking, and there's opportunity to work with exceptional engineering teams on meaningful missions.

---

![Visitors](https://visitor-badge.laobi.icu/badge?page_id=will-break-it.github.io&color=2196F3&style=flat-square)
