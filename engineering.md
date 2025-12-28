---
layout: default
title: William Wolff - Senior/Staff Engineer
---

<div class="resume-nav">
📋 <strong>View as:</strong> <a href="/">Full CV</a> • <a href="/product-engineer">Product Engineer</a> • <strong>Engineer</strong> • <a href="/architect">Architect</a> • <a href="/master-cv">Master (Detailed)</a>
</div>

# WILLIAM WOLFF
**Senior/Staff Software Engineer**

Berlin, DE | [linkedin.com/in/wwolff](https://linkedin.com/in/wwolff) • [github.com/will-break-it](https://github.com/will-break-it)

![Experience](https://img.shields.io/badge/Experience-10%2B%20Years-2196F3?style=flat) ![Location](https://img.shields.io/badge/Location-Berlin%2C%20DE-4CAF50?style=flat) ![Focus](https://img.shields.io/badge/Focus-Systems%20%26%20Infrastructure-9C27B0?style=flat)

---

## PROFILE

Hands-on systems engineer with 10+ years building high-performance, distributed systems from the ground up. Deep expertise in TypeScript, Rust, and Swift across backend infrastructure, blockchain protocols, and native mobile development. Passionate about solving hard technical problems - from protocol design to performance optimization to cryptographic security.

Experienced building production systems that scale: blockchain indexers processing 2,000+ tx/s, event-driven architectures reducing latency by 45%, migration toolchains handling 16M LoC. Equally comfortable diving into low-level Rust, architecting TypeScript backends, or building native iOS/Android apps.

**Core focus:** Distributed systems • Performance optimization • Blockchain infrastructure • Cryptography • Native mobile • Systems programming

---

## TECHNICAL EXPERTISE

**Primary Languages:**
- **TypeScript** (Expert) - 6+ years building production backends, React apps, Node.js services
- **Rust** (Proficient) - Embedded systems, blockchain tooling, performance-critical components
- **Swift** (Proficient) - Native iOS development, Secure Enclave integration, SwiftUI

**Additional Languages:** Java/Kotlin • Python • Bash • Haskell/Plutus (functional programming)

**Systems & Infrastructure:**
- Event-driven architectures • Microservices • gRPC • WebSocket • Real-time data pipelines
- PostgreSQL internals • Redis • Custom indexing (bloom filters, UTXO indexing)
- Docker • Terraform • Ansible • Infrastructure as Code • CI/CD pipelines

**Blockchain & Cryptography:**
- Cardano consensus • eUTxO model • Ouroboros protocols • Plutus smart contracts
- End-to-end encryption • Diffie-Hellman • AES • Secure Enclave/TEE
- Transaction construction • Wallet standards • Chain indexing

**Testing & Quality:** Jest • Vitest • Playwright • TDD • Integration testing • Differential testing

---

## EXPERIENCE

### **Blockchain Infrastructure Engineer – [Lace Wallet](https://www.lace.io/)**
**Input Output Global (IOG)** • *Remote* • <span class="date">Nov 2022 - Nov 2024</span>

Built high-performance blockchain indexing infrastructure and backend services for Cardano wallet.

**Custom Chain Indexer Development:**
- Designed and implemented chain indexer with **>2,000 tx/s ingest capacity** for mainnet/testnet
- Built **bloom filter** implementation for fast membership testing of stake credentials
- Implemented credential-based indexing optimized specifically for wallet queries
- Achieved sub-second wallet sync times through query optimization and caching
- Authored [CIP proposal](https://github.com/will-break-it/wallet-architecture/tree/main/docs/CIP/CIP-XXXX) documenting indexer architecture and standards

**Backend Re-Architecture:**
- Migrated from poll-based to **event-driven architecture** using PostgreSQL LISTEN/NOTIFY
- Reduced sync latency by **45%** through real-time event propagation
- Cut infrastructure costs by **>60%** via optimized query patterns and caching
- Built NestJS backend with gRPC services for MetaDex swap feature
- Implemented WebSocket connections for real-time wallet updates

**Technical Implementation Details:**
- PostgreSQL trigger-based event system for change detection
- Custom UTXO indexing with efficient lookup structures
- Background job processing for transaction submission and monitoring
- Transaction construction libraries for complex Cardano transaction types
- Monitoring and alerting using Prometheus/Grafana for indexer health

**Technologies:** TypeScript • NestJS • PostgreSQL • Event-driven architecture • Bloom filters • gRPC • WebSocket • Chain indexing

---

### **Protocol Engineering & Research – [Ouroboros Leios](https://www.youtube.com/watch?v=YEcYVygdhzU)**
**Input Output Global (IOG)** • *Remote* • <span class="date">Nov 2024 - Present</span>

Contributing to research and development of high-throughput overlay protocol for Cardano blockchain.

**Protocol Development:**
- Work closely with formal methods team on protocol specification
- Develop simulation frameworks for protocol validation
- Contribute to [CIP-0164](https://github.com/cardano-scaling/CIPs/blob/leios/CIP-0164/README.md) technical specification
- Bridge theoretical research with practical implementation constraints
- Prototype protocol components for performance testing

**Technical Areas:**
- Distributed consensus mechanisms
- Network protocol design
- Performance modeling and simulation
- Formal methods integration

**Technologies:** Haskell • Distributed systems • Consensus protocols • Formal verification

---

### **Full-Stack Blockchain Development – Drip Dropz**
**Consulting** • <span class="date">2022 - 2024</span>

Built production [NFT marketplace](https://dripdropz.io/) on Cardano from scratch.

**Frontend Development:**
- Built React/TypeScript SPA with comprehensive test coverage
- Implemented **CIP-30 wallet standard** for browser wallet integration
- Created background **web worker** for chain sync without blocking UI
- Built transaction construction for multi-asset UTXO scenarios
- Optimized React rendering for large NFT lists using virtualization

**Transaction Construction & UTXO Management:**
- Developed libraries for Cardano transaction construction
- Implemented UTXO selection algorithms for optimal fee management
- Built coin selection strategies balancing fees vs. UTXO fragmentation
- Created error handling for transaction failures and retries
- Integrated Plutus smart contracts for marketplace operations (bidding, swapping, order books)

**Testing & DevOps:**
- Established TDD practices with Jest for unit and integration tests
- Built CI/CD pipeline with automated deployments
- Implemented end-to-end testing with Playwright
- Created comprehensive test fixtures for blockchain scenarios

**Technologies:** React • TypeScript • Cardano • CIP-30 • Web Workers • Plutus • Jest • Playwright • CI/CD

---

### **Native Mobile Development – Dump it!**
**Side Project** • <span class="date">2023 - Present</span>

Built cross-platform note-taking app with sophisticated AI pipeline and end-to-end encryption. [iOS](https://apps.apple.com/de/app/dump-it/id6448620477) • [Android](https://play.google.com/store/apps/details?id=app.dump.it) • [Web](https://dumpit.app)

**Two-Phase LLM Processing Pipeline:**
- **Phase 1 (Intent Classification)**: Claude Haiku analyzes user input, separates semantic units, classifies intents (create/update/delete)
- **Phase 2 (Conflict Resolution)**: LLM resolves ambiguous cases when vector search finds multiple matches
- **Prompt engineering**: Cached static sections, timezone-aware date conversion, structured JSON output with validation
- **Context-aware prompts**: Includes 7 most recent entities for better intent understanding
- Automatic time extraction: "Call mom tonight at 8pm" → todo with `remindAt` field populated, time stripped from text

**Vector Search & Semantic Matching:**
- **Sentence transformers** for 768-dimensional embeddings of notes/todos
- **Adaptive match quality analysis**: Dynamic thresholds based on statistical distribution (mean, stddev, gap analysis)
- **Recency bias**: +0.1 similarity boost for entities updated within 24h (encourages updating recent items)
- **Smart filtering**: Excludes completed todos and reminders overdue >48h from search results
- PostgreSQL pgvector with cosine similarity search (topK=8)

**Event-Sourced Architecture:**
- Task-based async pipeline with Server-Sent Events (SSE) for real-time progress streaming
- Immutable event stream enables features: undo, audit history, conflict resolution replay
- Non-blocking: client receives `dumpId` immediately, processing happens in background
- Transactional execution: all entity operations in single DB transaction for atomicity

**iOS Development (Swift):**
- Native iOS app using **SwiftUI** for modern declarative UI
- **Secure Enclave** integration for cryptographic key storage
- Local SQLite database with FTS5 full-text search
- Background sync using iOS background tasks
- Published to App Store with 4.8★ rating

**Android Development (Kotlin):**
- Native Android app using **Jetpack Compose**
- Room database for local persistence
- WorkManager for background sync
- Keystore for secure key storage
- Published to Google Play

**End-to-End Encryption:**
- **Diffie-Hellman key exchange** for secure key establishment
- **AES-256-GCM** encryption for note content
- Secure key derivation using PBKDF2
- Zero-knowledge architecture - backend cannot decrypt user data

**Web Frontend (React/TypeScript):**
- React SPA with TypeScript
- IndexedDB for local storage
- Web Crypto API for encryption
- Published to [dumpit.app](https://dumpit.app)

**Backend (NestJS + Supabase):**
- PostgreSQL with pgvector extension for embeddings
- Real-time subscriptions (SSE) for multi-device sync
- Task queue for background processing
- Self-hosted Whisper v3 for speech-to-text transcription

**Technologies:** Swift • Kotlin • React • TypeScript • NestJS • PostgreSQL • pgvector • Claude Haiku • Sentence Transformers • Cryptography • Secure Enclave • Event-sourcing

---

### **IoT & Embedded Systems – Mobility Data Lab**
**Senior Software Engineer** • <span class="date">Feb 2020 - Nov 2021</span>

Built OTA update pipeline and WiFi tracking system for connected vehicle platform.

**Embedded Systems (Rust):**
- Developed firmware for embedded devices in vehicles
- Built secure OTA update mechanism with rollback capabilities
- Implemented WiFi probing for audience detection
- Optimized for resource-constrained hardware

**Backend Infrastructure (Vert.x/Java):**
- Built high-throughput event processing using **Vert.x** (reactive JVM framework)
- Designed data ingestion pipeline handling thousands of events/second
- Implemented **ELK stack** (Elasticsearch, Logstash, Kibana) for real-time analytics
- Created real-time ad pricing system based on audience measurements

**Technologies:** Rust • Vert.x (Java) • ELK Stack • IoT • Embedded systems • Real-time processing

---

### **Compiler Development & Migration Tooling – Deloitte**
**Senior Software Engineer** • <span class="date">Sep 2016 - Nov 2019</span>

Built automated migration toolchain for large-scale legacy system transformation.

**Parser & Compiler Development:**
- Built **3-stage migration toolchain**: parser → AST transformer → Java code generator
- Migrated **16M lines of code** from proprietary DSL to Java 8
- Designed abstract syntax tree (AST) representation for domain-specific language
- Implemented code generation preserving business logic semantics
- Built custom runtime environment for compatibility layer

**Testing Infrastructure:**
- Architected differential testing framework comparing old vs. new system outputs
- Processed millions of test cases for equivalence validation
- Achieved **>99.9% compatibility rate** for migrated logic
- Built regression test suite for ongoing correctness

**Technical Impact:**
- Saved client **€6M annually** in licensing costs
- Maintained behavioral equivalence while modernizing codebase
- Enabled future development on standard JVM instead of proprietary platform

**Technologies:** Java 8 • Compiler design • Parser generators • AST manipulation • Differential testing

---

## SIDE INFRASTRUCTURE PROJECTS

### **Berlin Pool – Cardano Stakepool Operations** • <span class="date">2021 - 2024</span>

**Node Operations:**
- Operated Cardano consensus nodes producing **2,000+ mainnet blocks**
- Maintained **99.9% uptime** through redundancy and monitoring
- Managed **15M+ ADA delegation** (~$7M+ value at peak)

**Infrastructure Automation:**
- Automated deployment using **Docker**, **Ansible**, and **Terraform**
- Built infrastructure-as-code for reproducible node deployments
- Implemented disaster recovery and backup procedures

**Security & Cryptography:**
- Managed cryptographic keys for block-signing operations
- Implemented air-gapped cold key storage
- Built secure key rotation procedures

**Monitoring:**
- Built monitoring using **Prometheus** and **Grafana**
- Created alerting for node health, network connectivity, block production
- Tracked performance metrics and optimized for slot leadership

**Technologies:** Cardano node • Docker • Terraform • Ansible • Prometheus • Grafana • Cryptography

---

## EDUCATION

**Bachelor of Science in Computer Science**
*DHBW Stuttgart* • Germany • <span class="date">2011 - 2014</span>

**International Business**
*Hult International Business School* • San Francisco, CA • <span class="date">2014 - 2015</span>

---

## WHAT I'M LOOKING FOR

I'm passionate about working on technically challenging problems that matter:

**Technical interests:**
- Distributed systems and consensus protocols
- Performance-critical infrastructure
- Cryptography and security
- Systems programming (Rust, low-level optimization)
- Blockchain and decentralized systems

**Company culture:**
- Mission-driven work contributing to meaningful goals
- Engineering excellence and technical depth
- Opportunities to work across the stack
- Learning from exceptional engineers

**Target companies:** xAI, SpaceX, Tesla (Autopilot/Infrastructure), Revolut, mission-driven startups building technically ambitious products

I value roles with strong upside potential through equity and the opportunity to make significant technical impact.

---

![Visitors](https://visitor-badge.laobi.icu/badge?page_id=will-break-it.github.io&color=2196F3&style=flat-square)
