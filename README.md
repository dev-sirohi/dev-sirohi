# Dev Sirohi — Software Engineer

2.5 years building enterprise ERP and Warehouse Management Systems. Focused on backend systems, API design, and understanding how things work at the foundation.

**.NET (C#) • Python • FastAPI • PostgreSQL • SQL Server • React**

---

# [StockSense — Warehouse Intelligence Platform](https://github.com/dev-sirohi/stocksense)
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

# Credis — In-Memory Database
***C# • TCP • Async • Networking***

Lightweight in-memory database implementing a byte-length-prefixed protocol (RESP-inspired). Built to understand networking, protocol design, and concurrent async request handling across multiple clients.
