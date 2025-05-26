# 🔬 Enhanced KS Prediction Application

Smart computer-vision software built **for the textile industry**: upload a fabric image, and our EfficientNet-B0 model predicts “KS” (knitting streak) defects in real time—wrapped in a secure, production-grade API and a sleek dark/light UI.

> **90 % automation, 100 % control.** From batch pipelines to live dashboards, you get data-driven quality assurance with enterprise-class security, monitoring & CI/CD.

---

## ✨ Key Features

* 🤖 **EfficientNet-B0 ML Core** – high-accuracy model tuned for textile imagery
* 🔐 **Zero-Trust Security** – JWT auth, bcrypt hashing, rate-limit middleware
* ⚡ **Realtime & Batch Modes** – stream single frames or process whole folders
* 🌗 **Modern UI** – responsive SPA with one-click dark / light theme toggle
* 📈 **Insight & Alerts** – Prometheus metrics, Sentry tracing, Slack / email hooks
* 🧪 **99 % Test Coverage** – pytest + coverage gates in CI
* 📚 **Auto-Generated Docs** – OpenAPI 3.1 served at `/docs`
* 🔄 **Alembic Migrations** – versioned DB schema, rollback safe
* 🚀 **Speed Boosters** – Redis caching, async workers, gzip compression

---

## 🖥️ Tech Stack

| Layer         | Tools                                 |
| ------------- | ------------------------------------- |
| ML / CV       | TensorFlow • EfficientNet-B0 • Pillow |
| API           | FastAPI • Uvicorn • Pydantic          |
| Auth / Rate   | PyJWT • Starlette-Throttle            |
| Data          | SQLAlchemy • SQLite / PostgreSQL      |
| Caching       | Redis                                 |
| Ops           | Docker • AWS (optional S3)            |
| Observability | Prometheus • Grafana • Sentry         |
| CI / CD       | GitHub Actions                        |

---

## 🚀 Quick Start

### Prerequisites

Python 3.8+, Redis, SQLite (or Postgres), **optional:** AWS credentials for S3.

```bash
# 1 Clone
git clone https://github.com/<your-org>/ks-prediction-app.git
cd ks-prediction-app

# 2 Virtualenv
python -m venv venv
source venv/bin/activate   # Windows: venv\Scripts\activate

# 3 Install deps
pip install -r requirements.txt

# 4 Config
cp .env.example .env       # then add secrets 🔑

# 5 DB migrate
alembic upgrade head

# 6 Run
redis-server &             # if not already running
python ks_prediction_app_enhanced.py
```

## ⚙️ Configuration (`.env`)

| Variable                | Purpose                          |
| ----------------------- | -------------------------------- |
| `DATABASE_URL`          | SQLAlchemy connection string     |
| `REDIS_URL`             | Redis endpoint                   |
| `JWT_SECRET_KEY`        | Token signing secret             |
| `ENCRYPTION_KEY`        | AES-256 key for sensitive fields |
| `SENTRY_DSN`            | Error-tracking DSN               |
| `AWS_ACCESS_KEY_ID`     | (optional) S3 upload auth        |
| `AWS_SECRET_ACCESS_KEY` | –                                |
| `AWS_REGION`            | –                                |

---

## 🧪 Testing

```bash
pytest                     # run suite
pytest --cov=ks_prediction_app_enhanced tests/   # with coverage
```

---

## 🔒 Security Highlights

* Bcrypt-hashed passwords
* JWT access & refresh tokens
* Strict rate-limiting & IP throttling
* Automatic input validation / sanitisation
* Encrypted PII at rest & in transit

---

## 📊 Monitoring & Ops

* Prometheus metrics at `/metrics`
* Sentry traces & alerts
* Resource dashboards (CPU, mem, GPU) via Grafana
* Structured JSON logs (ELK-friendly)

---

## 🤝 Contributing

1. **Fork** the repo and create a feature branch.
2. Follow Conventional Commits (`feat:`, `fix:`, `chore:`).
3. Ensure tests & linters pass (`pre-commit run --all-files`).
4. Open a Pull Request—CI will do the rest.

---

## 📝 License

Released under the **MIT License**. See [`LICENSE`](LICENSE) for full terms.

---

### 📢 Need a Demo or Consulting?

This is bespoke, real-world software for the textile sector.
📧 **Contact us** via Issues or email for a live walkthrough, or custom features.
