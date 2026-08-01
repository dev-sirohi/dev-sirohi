# Dev Sirohi — Machine Learning Engineer | Software Engineer

Software engineer with 2.5 years of production experience building backend systems and machine learning applications. Interested in ranking, retrieval, recommender systems, and production ML, with a focus on designing systems that are accurate, scalable, and easy to operate.

**Python • C#/.NET • FastAPI • PostgreSQL • SQL Server • Machine Learning**

---

# [Microblog — Full Stack Social Platform](https://github.com/dev-sirohi/microblog) · _[Live Demo](https://microblog-devsirohi-ddfmf3crgvh2akau.centralindia-01.azurewebsites.net/swagger/index.html)_
***.NET • ASP.NET Core • SQL Server • Redis • React • TypeScript • Docker • Azure***

Backend-heavy microblogging platform exploring the trade-off between Redis (performance) and SQL Server (durability).

- JWT authentication with HTTP-only cookie sessions and EF Core-persisted refresh tokens
- Custom Redis sliding-window rate limiter with per-endpoint policies, backed by a `[RateLimit]` attribute/filter
- Eventual-consistency write path: likes/follows queue to Redis and drain to SQL Server in batches via a hosted `BackgroundService`
- Pluggable messaging (Azure Service Bus) and storage (Azure Blob Storage) behind swappable interfaces
- Deployed to Azure App Service with secrets in Key Vault, via a GitHub Actions CI/CD pipeline
- xUnit integration tests (Testcontainers) covering auth, rate limiting, and the batched write path
- Prometheus metrics and Grafana dashboards for request latency and cache-hit monitoring

*Hosted on free-tier Azure resources, so the app is generally kept stopped to conserve them — [email me](mailto:devsirohi000@gmail.com) and I'll spin it back up in a couple of minutes if you'd like to see the live demo.*

---

# [StockSense — Warehouse Intelligence Platform](https://github.com/dev-sirohi/stocksense) · _[Live Demo](https://stocksense-production-80d2.up.railway.app/)_
***Python • FastAPI • PostgreSQL • pgvector • Redis • OpenAI • Docker***

AI-powered warehouse intelligence platform for inventory search, monitoring, and analytics, built around the workflows of an FMCG distributor managing 500+ SKUs.

- Retrieval-augmented natural language inventory search using OpenAI and pgvector.
- Semantic SKU search using text embeddings and pgvector cosine similarity
- Real-time stock health alerts — expiring, expired, low stock
- API performance monitoring with P95 metrics and cache hit rate tracking
- Redis caching layer reducing API latency for repeated inventory queries.

---

# [Credis — In-Memory Database](https://github.com/dev-sirohi/Recreational/tree/main/credis-a-c-sharp-in-memory-db)
***C# • TCP • Async • Networking***

A tiny Redis-style in-memory database written from scratch in C# (.NET 10). It speaks a small binary line protocol over raw TCP, stores everything in memory, supports per-key time-to-live (TTL), and serves many connections concurrently.

This is a learning project: the goal was to hand-roll the networking, the buffer management, and the request parser without leaning on a framework, and to keep the code small enough to read in one sitting.
- Raw TCP server built on TcpListener, one task per connection.
- Hand-written parser that reads a length-prefixed binary frame out of a fixed-size buffer — no StreamReader, no allocations per line beyond the value itself.
- Eight commands: set, get, delete, exists, increment, decrement, expire, ttl.
- Per-key TTL with lazy expiration (a key is reclaimed the moment it is read after expiring).
- Thread-safe store backed by ConcurrentDictionary.
- A single-file benchmark (Test.cs) that proves correctness and measures throughput.

---

# [FastAPI Project Generator](https://github.com/dev-sirohi/fastapi-project-generator)
***Python • CLI • FastAPI • Docker***

CLI script to scaffold a production-ready FastAPI project structure with optional Dockerfile, virtual environment setup, and automatic rollback on failure.
- Interactive prompts — project name, Dockerfile, venv, extra requirements
- Generates `src/`-based layout with `models`, `services`, `dtos`, `routers` as packages
- Automatic rollback on any failure
- Cross-platform: Windows, macOS, Linux
