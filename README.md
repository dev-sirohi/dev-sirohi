# Dev Sirohi — Software Engineer

2.5 years building enterprise ERP and Warehouse Management Systems. Focused on backend systems, API design, and understanding how things work at the foundation.

**.NET (C#) • Python • FastAPI • PostgreSQL • SQL Server • React**

---

# [StockSense — Warehouse Intelligence Platform](https://github.com/dev-sirohi/stocksense) · _[Live Demo](https://stocksense-production-80d2.up.railway.app/)_
***Python • FastAPI • PostgreSQL • pgvector • Redis • OpenAI • Docker***

AI-powered warehouse intelligence platform built for a Delhi-based FMCG distributor managing 500+ SKUs.

- Natural language inventory queries via RAG + OpenAI
- Semantic SKU search using text embeddings and pgvector cosine similarity
- Real-time stock health alerts — expiring, expired, low stock
- API performance monitoring with P95 metrics and cache hit rate tracking
- Redis caching layer with measurable response time improvements

---

# [PayBridge — Payment Gateway Integration](https://github.com/dev-sirohi/Paybridge)
***Python • FastAPI • PostgreSQL • Razorpay • Docker***

Payment gateway integration service handling the full order lifecycle from creation to confirmation.

- Razorpay order creation with async SDK integration
- Webhook processing with HMAC-SHA256 signature verification
- Wallet top-up and withdrawal with balance enforcement
- Transactional integrity — wallet credits only on confirmed webhook events
- Order history with filtering by status and date range

---

# [Microblog — Full Stack Social Platform](https://github.com/dev-sirohi/microblog)
***.NET • ASP.NET Core • SQL Server • Redis • React • TypeScript • Docker***

Backend-heavy microblogging platform exploring caching, eventual consistency, and async messaging.

- JWT auth via HTTP-only cookies with refresh token flow
- Redis cache-aside pattern via generic `ICacheService<T>` wrapper
- Background sync service drains Redis queues to SQL Server asynchronously
- Configurable event streaming — Kafka or Azure Service Bus via config toggle
- AI post recommendations via OpenAI embeddings + cosine similarity, cached in Redis
- Prometheus metrics, health checks, and Redis-backed rate limiting
- React + TypeScript frontend with optimistic UI updates

---

# [Pyblog — Blog Platform](https://github.com/dev-sirohi/pyblog)
***Python • FastAPI • PostgreSQL • Firebase • Docker***

Full-stack blog platform with Markdown-based content authoring and media management.
- JWT auth via HTTP-only cookies
- Markdown content with inline media — images stored in Firebase Storage, referenced by UUID in content
- Users, posts, auth, likes, and follows persisted in PostgreSQL
- Rate limiting via SlowAPI
- Static frontend served directly from FastAPI

---

# [FastAPI Project Generator](https://github.com/dev-sirohi/fastapi-project-generator)
***Python • CLI • FastAPI • Docker***

CLI script to scaffold a production-ready FastAPI project structure with optional Dockerfile, virtual environment setup, and automatic rollback on failure.
- Interactive prompts — project name, Dockerfile, venv, extra requirements
- Generates `src/`-based layout with `models`, `services`, `dtos`, `routers` as packages
- Automatic rollback on any failure
- Cross-platform: Windows, macOS, Linux

---

# [Credis — In-Memory Database](https://github.com/dev-sirohi/Recreational/tree/main/credis-a-c-sharp-in-memory-db)
***C# • TCP • Async • Networking***

Lightweight in-memory database implementing a byte-length-prefixed protocol (RESP-inspired). Built to understand networking, protocol design, and concurrent async request handling across multiple clients.
