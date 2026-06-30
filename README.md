# FNovel Platform

An advanced novel reading and aggregation platform built with Java Spring Boot, React, and Python AI.

## 📌 Project Goals
1. Built as a personal project to read novel fanfictions from various sources.
2. Advance core software engineering skills, focusing on system design, scalability (1M+ users), and AI integration.

## 🛠️ Tech Stack & Architecture Plan
- **Backend:** Java Spring Boot (Enterprise Core)
- **Frontend:** ReactJS (Web) + React Native (Mobile)
- **AI & Crawling:** Python (Scrapy/Playwright, PaddleOCR, RAG Chatbot)
- **Data & Cache:** PostgreSQL, MongoDB, Redis, Apache Kafka
- **Infrastructure:** Docker, Kubernetes

## 🗺️ Roadmap & Features Todo

### Phase 1: Core System & Infrastructure 🚧 (Current)
- [ ] Initialize Monorepo structure and `.gitignore`
- [ ] Setup `docker-compose.yml` for databases (Postgres, Mongo, Redis, Kafka)
- [ ] Design Core Database Schemas (User, Novel Metadata, Chapters)

### Phase 2: Core Features (Backend & Frontend) 📅
- [ ] Implement Auth (JWT + HttpOnly Cookies) & Spring Security
- [ ] Build basic Web Reader UI (ReactJS)
- [ ] Build basic Mobile Reader UI (React Native)

### Phase 3: Advanced Features & AI 📅
- [ ] Develop Python Crawler pipeline with Kafka event-driven architecture
- [ ] Implement Bring-Your-Own-Key (BYOK) AI Translation layer
- [ ] Build RAG-driven AI Recommendation Chatbot

### Phase 4: Scaling & Security 📅
- [ ] Add Redis Rate Limiter & Cache-Aside pattern
- [ ] Setup Nginx/Cloudflare for DDoS protection
- [ ] Containerize applications using Kubernetes (K8s)
