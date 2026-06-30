# FNovel Platform

An advanced novel reading and aggregation platform built with Java Spring Boot, React, and Python AI.

## Project Structure

```
fnovel-platform/
├── .gitignore
├── LICENSE
├── README.md
├── docker-compose.yml
├── k8s/
│   ├── backend-deployment.yml
│   ├── python-deployment.yml
│   └── database-services.yml
├── backend-java/          # Spring Boot core API
├── ai-crawler-python/     # Crawler, OCR, RAG chatbot
├── frontend-web/          # React (Vite) web app
└── frontend-mobile/       # React Native (Expo) mobile app
```

## Tech Stack

- **Backend:** Java Spring Boot (Web, Security, JPA, MongoDB, Lombok)
- **Frontend:** ReactJS (Vite) + React Native (Expo)
- **AI & Crawling:** Python (Scrapy, Playwright, PaddleOCR, LangChain)
- **Data & Cache:** PostgreSQL, MongoDB, Redis, Apache Kafka
- **Infrastructure:** Docker, Kubernetes

## Quick Start

### 1. Start local infrastructure

```bash
docker compose up -d
```

Services:

| Service    | Port  |
|------------|-------|
| PostgreSQL | 5432  |
| MongoDB    | 27017 |
| Redis      | 6379  |
| Kafka      | 9092  |

### 2. Backend (Spring Boot)

```bash
cd backend-java
./mvnw spring-boot:run
```

API runs at `http://localhost:8080`.

### 3. Web frontend (Vite + React)

```bash
cd frontend-web
npm install
npm run dev
```

### 4. Mobile app (Expo)

```bash
cd frontend-mobile
npm start
```

To generate native `android/` and `ios/` folders:

```bash
cd frontend-mobile
npx expo prebuild
```

### 5. Python AI pipeline

```bash
cd ai-crawler-python
python -m venv .venv
# Windows: .venv\Scripts\activate
pip install -r requirements.txt
cp .env.example .env
```

## Roadmap

### Phase 1: Core System & Infrastructure (Current)
- [x] Initialize monorepo structure
- [x] Setup `docker-compose.yml` for Postgres, Mongo, Redis, Kafka
- [ ] Design core database schemas (User, Novel, Chapter)

### Phase 2: Core Features
- [ ] Auth (JWT + HttpOnly Cookies) & Spring Security
- [ ] Web reader UI (React)
- [ ] Mobile reader UI (React Native)

### Phase 3: Advanced Features & AI
- [ ] Python crawler pipeline with Kafka events
- [ ] BYOK AI translation layer
- [ ] RAG-driven recommendation chatbot

### Phase 4: Scaling & Security
- [ ] Redis rate limiter & cache-aside pattern
- [ ] Nginx / Cloudflare DDoS protection
- [ ] Kubernetes deployment
