# ⚡ Hermes SuperCode Skills — Codex Edition

**13 production-grade skill modules for OpenAI Codex · AGENTS.md native · MIT License**

[English](#english) · [中文](#中文) · [Türkçe](#türkçe)

> **Claude Code version:** [hermes-supercode-skills](https://github.com/mturac/hermes-supercode-skills)

---

## English

### What is this?

Hermes Codex Edition adapts 13 specialized skill modules for OpenAI Codex via `AGENTS.md`. Each module activates automatically when a task matches its domain — no manual invocation needed.

Skills cover: database optimization, authentication systems, observability, infrastructure, security, deployments, debugging, API design, data pipelines, prompt engineering, web scraping, prediction markets, and multi-agent orchestration.

### Skills

| # | Skill | Domain | Trigger examples |
|---|-------|--------|-----------------|
| 1 | **infra-automation** | DNS, SSL, Cloudflare, CDN | "Add an A record for api.example.com" |
| 2 | **prediction-alpha** | Prediction market analysis | "Analyze this Polymarket market" |
| 3 | **ghost-scraper** | Ethical web scraping | "Scrape product data from this URL" |
| 4 | **mcp-conductor** | Multi-agent orchestration | "Coordinate 5 agents on this task" |
| 5 | **pipeline-architect** | ETL/ELT, streaming, data warehouse | "Build a Kafka-to-ClickHouse pipeline" |
| 6 | **security-sentinel** | Security audits, vuln scanning | "Audit example.com security posture" |
| 7 | **deploy-ninja** | Zero-downtime deployments | "Deploy v2.3.4 with canary strategy" |
| 8 | **quantum-debugger** | Race conditions, memory leaks | "Production service intermittently segfaults" |
| 9 | **api-sculptor** | REST/GraphQL/gRPC design | "Design an Order API for e-commerce" |
| 10 | **prompt-forge** | Prompt engineering | "Write a system prompt for a support agent" |
| 11 | **db-whisperer** | Query optimization, migrations | "This Postgres query is timing out" |
| 12 | **auth-architect** | OAuth2, JWT, RBAC, SSO, MFA | "Implement OAuth2 with refresh token rotation" |
| 13 | **obs-guardian** | OpenTelemetry, Prometheus, SLOs | "Add distributed tracing to my microservices" |

### Installation

#### Option A: Use as AGENTS.md in your project

```bash
# Copy AGENTS.md to your project root
curl -sO https://raw.githubusercontent.com/mturac/hermes-supercode-skills-codex/main/AGENTS.md

# Codex will automatically pick up the skill definitions
```

#### Option B: Full clone with skill reference files

```bash
git clone https://github.com/mturac/hermes-supercode-skills-codex.git

# Place AGENTS.md in your project root
cp hermes-supercode-skills-codex/AGENTS.md ./AGENTS.md
```

### How it works

Codex reads `AGENTS.md` at the start of every session. The 13 skill definitions are loaded as context — when your task matches a skill's domain, Codex activates that skill's **Recon → Plan → Execute → Verify** workflow automatically.

### Design Principles

1. **Recon → Plan → Execute → Verify** — no skill jumps straight to action
2. **Structured JSON output** — every skill produces machine-parseable results
3. **Tiered safety rails** — 🔴 Red (never) / 🟡 Yellow (confirm first) / 🟢 Green (safe)
4. **Self-contained** — copy `AGENTS.md` into any project, no dependencies

---

## 中文

### 这是什么？

Hermes Codex 版本通过 `AGENTS.md` 为 OpenAI Codex 适配了 **13 个专业技能模块**。每个模块在任务匹配其领域时自动激活，无需手动调用。

技能覆盖：数据库优化、身份认证、可观测性、基础设施、安全、部署、调试、API 设计、数据管道、提示词工程、网页抓取、预测市场、多智能体编排。

### 技能列表

| # | 技能 | 领域 | 触发示例 |
|---|------|------|---------|
| 1 | **infra-automation** | DNS、SSL、Cloudflare、CDN | "为 api.example.com 添加 A 记录" |
| 2 | **prediction-alpha** | 预测市场分析 | "分析这个 Polymarket 市场" |
| 3 | **ghost-scraper** | 合规网页抓取 | "从这个 URL 抓取产品数据" |
| 4 | **mcp-conductor** | 多智能体编排 | "协调 5 个代理完成此任务" |
| 5 | **pipeline-architect** | ETL/ELT、流处理、数仓 | "构建 Kafka 到 ClickHouse 的管道" |
| 6 | **security-sentinel** | 安全审计、漏洞扫描 | "审计 example.com 安全状况" |
| 7 | **deploy-ninja** | 零停机部署 | "使用金丝雀策略部署 v2.3.4" |
| 8 | **quantum-debugger** | 竞态条件、内存泄漏 | "生产服务间歇性崩溃" |
| 9 | **api-sculptor** | REST/GraphQL/gRPC 设计 | "为电商设计订单 API" |
| 10 | **prompt-forge** | 提示词工程 | "为支持代理编写系统提示词" |
| 11 | **db-whisperer** | 查询优化、迁移 | "这个 Postgres 查询超时了" |
| 12 | **auth-architect** | OAuth2、JWT、RBAC、SSO、MFA | "实现带刷新令牌轮换的 OAuth2" |
| 13 | **obs-guardian** | OpenTelemetry、Prometheus、SLO | "为微服务添加分布式追踪" |

### 安装

```bash
# 将 AGENTS.md 复制到您的项目根目录
curl -sO https://raw.githubusercontent.com/mturac/hermes-supercode-skills-codex/main/AGENTS.md
```

Codex 在每次会话开始时自动读取 `AGENTS.md`，13 个技能定义作为上下文加载。

---

## Türkçe

### Bu nedir?

Hermes Codex Edition, OpenAI Codex için `AGENTS.md` üzerinden **13 uzmanlaşmış skill modülünü** aktive eder. Her modül, görev kendi alanıyla eşleştiğinde otomatik olarak devreye girer — manuel çağrı gerekmez.

Skill'ler şunları kapsar: veritabanı optimizasyonu, kimlik doğrulama, gözlemlenebilirlik, altyapı, güvenlik, deployment, hata ayıklama, API tasarımı, veri pipeline'ları, prompt mühendisliği, web scraping, tahmin piyasaları, çok ajanlı orkestrasyon.

### Skill Listesi

| # | Skill | Alan | Tetikleyici örnekler |
|---|-------|------|---------------------|
| 1 | **infra-automation** | DNS, SSL, Cloudflare, CDN | "api.example.com için A kaydı ekle" |
| 2 | **prediction-alpha** | Tahmin piyasası analizi | "Bu Polymarket piyasasını analiz et" |
| 3 | **ghost-scraper** | Etik web scraping | "Bu URL'den ürün verisi çek" |
| 4 | **mcp-conductor** | Çok ajanlı orkestrasyon | "5 ajanı bu görevde koordine et" |
| 5 | **pipeline-architect** | ETL/ELT, streaming, veri ambarı | "Kafka'dan ClickHouse'a pipeline kur" |
| 6 | **security-sentinel** | Güvenlik denetimi, zafiyet tarama | "example.com güvenlik durumunu denetle" |
| 7 | **deploy-ninja** | Sıfır-kesinti deployment | "v2.3.4'ü canary stratejisiyle deploy et" |
| 8 | **quantum-debugger** | Race condition, bellek sızıntısı | "Production servis aralıklı çöküyor" |
| 9 | **api-sculptor** | REST/GraphQL/gRPC tasarımı | "E-ticaret için Sipariş API'si tasarla" |
| 10 | **prompt-forge** | Prompt mühendisliği | "Destek ajanı için sistem promptu yaz" |
| 11 | **db-whisperer** | Sorgu optimizasyonu, migrasyonlar | "Bu Postgres sorgusu zaman aşımına uğruyor" |
| 12 | **auth-architect** | OAuth2, JWT, RBAC, SSO, MFA | "Refresh token rotasyonlu OAuth2 uygula" |
| 13 | **obs-guardian** | OpenTelemetry, Prometheus, SLO'lar | "Mikroservislerime dağıtık izleme ekle" |

### Kurulum

```bash
# AGENTS.md'yi proje köküne kopyala
curl -sO https://raw.githubusercontent.com/mturac/hermes-supercode-skills-codex/main/AGENTS.md
```

Codex her oturumun başında `AGENTS.md` dosyasını okur. 13 skill tanımı bağlam olarak yüklenir ve göreviniz bir skill'in alanıyla eşleştiğinde otomatik olarak **Keşif → Planlama → Uygulama → Doğrulama** iş akışı devreye girer.

---

## Repo Structure

```
hermes-supercode-skills-codex/
├── AGENTS.md          ← Drop this in your project root
├── README.md
├── LICENSE
├── skills/
│   ├── db-whisperer/SKILL.md
│   ├── auth-architect/SKILL.md
│   ├── obs-guardian/SKILL.md
│   ├── infra-automation/SKILL.md
│   ├── security-sentinel/SKILL.md
│   ├── deploy-ninja/SKILL.md
│   ├── quantum-debugger/SKILL.md
│   ├── api-sculptor/SKILL.md
│   ├── pipeline-architect/SKILL.md
│   ├── mcp-conductor/SKILL.md
│   ├── ghost-scraper/SKILL.md
│   ├── prediction-alpha/SKILL.md
│   └── prompt-forge/SKILL.md
└── docs/DESIGN_DECISIONS.md
```

## Related

- **Claude Code version:** [hermes-supercode-skills](https://github.com/mturac/hermes-supercode-skills) — uses Claude Code's `Skill` tool mechanism
- **Codex automations:** [awesome-codex-automations](https://github.com/mturac/awesome-codex-automations)

## License

MIT — use it, fork it, extend it.
