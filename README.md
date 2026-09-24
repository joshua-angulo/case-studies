# Case studies

Write-ups of the two systems I've built. The code is private: one is my own product and the other contains a strategy I keep to myself. These notes cover what I can share, which is how each system is built, why I made the decisions I did, and what went wrong along the way.

| Case | Stack | Covers |
|---|---|---|
| [Quantitative research and execution platform](plataforma-cuantitativa.md) | Python, Polars, DuckDB, Parquet, XGBoost, CatBoost, LightGBM, AWS (EC2, S3), Rust (Tokio) | Validation without leakage (walk-forward, purged, preregistered), Python and Rust scoring as a tested contract, shadow and canary rollout, controls tested by making them fail |
| [LuckAgents, a multi-tenant SaaS for AI agents](luckai-saas-multitenant.md) | TypeScript, Node/Express, React, Next.js, PostgreSQL/Supabase, pgvector, MongoDB, Redis, Docker | Tenant isolation in the database, idempotent payments, agents with tools and RAG, and an audit that said NO-GO for production with every test passing |

I left out business figures, financial results, credentials and customer data. When a decision depended on something I can't publish, I describe the shape of the problem and leave the specifics out.

## Runnable code

The tenant-isolation pattern from LuckAgents is published as working code in [multi-tenant-rls](https://github.com/joshua-angulo/multi-tenant-rls): about 200 lines of SQL and TypeScript, 16 tests (most of them negative) and a mutation check showing the tests catch a broken policy. It takes about two minutes to run.

If you'd like to go through the rest of the code or the architecture, I'm glad to do it in an interview.

Joshua Angulo González · Culiacán, Mexico (UTC-7) · [LinkedIn](https://www.linkedin.com/in/joshuaangulogonzalez/) · joshuaangulo10@gmail.com

---

**En español.** Notas sobre los dos sistemas que he construido. El código es privado (uno es producto propio y el otro contiene una estrategia que no publico), así que aquí comparto cómo está hecho cada uno, por qué tomé las decisiones que tomé y qué salió mal en el camino. No incluyo cifras de negocio, resultados financieros, credenciales ni datos de clientes.
