# 🔗 LinkShrink: Scalable URL Shortening Service

A blazing-fast, distributed, and open-source URL shortening service built with **FastAPI**, **ScyllaDB**, **Redis**, and **Zookeeper**. Designed to scale to trillions of URLs and serve millions of requests per second.

---

## 🚀 Features

- ✅ Shorten long URLs to unique, compact hashes
- ✅ Resolve shortened URLs to original links instantly
- ✅ Built-in TTL support for expiring URLs
- ✅ Optimized for horizontal scalability
- ✅ Backed by high-performance ScyllaDB and Redis
- ✅ Health check & metrics endpoints
- ✅ Docker & Docker Compose support for local dev
- ✅ RESTful APIs with automatic OpenAPI docs

---

## 📸 Demo

> Coming soon...

---

## 🛠 Tech Stack

- **FastAPI** – blazing-fast web framework
- **ScyllaDB** – ultra-scalable NoSQL store for URL mappings
- **Redis** – fast in-memory caching layer
- **Zookeeper** – service coordination (optional, e.g., for ID range generation)
- **Docker Compose** – for easy local setup

---

## 🧪 Quickstart (Development)

```bash
# Clone the repo
git clone https://github.com/krishnamadhavan/link-shrink.git
cd link-shrink

# Copy environment variables
cp .env.example .env

# Start services
docker-compose up --build
```

Open API Docs: [http://localhost:8000/docs](http://localhost:8000/docs)

---

## 📦 API Overview

### POST `/shorten`
```json
Request:
{
  "url": "https://example.com/some/long/link"
}

Response:
{
  "short_url": "http://short.ly/abc123"
}
```

### GET `/expand/{short_code}`
```json
Response:
{
  "original_url": "https://example.com/some/long/link"
}
```

---

## 📁 Project Structure

```
app/
├── api/            # FastAPI endpoints
├── db/             # ScyllaDB, Redis, Zookeeper clients
├── models/         # Pydantic models
├── services/       # Business logic (shorten/expand)
├── utils/          # Encoding/hash tools
└── main.py         # Entry point
```

---

## 🧪 Running Tests

```bash
make test
```

---

## 📄 License

[GNU General Public License Version 3.0](LICENSE)

---

## 👨‍💻 Maintainers

Built with ❤️ by [Krishna Madhavan](https://github.com/krishnamadhavan).