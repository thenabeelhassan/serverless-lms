# Backend

This directory contains all backend microservices developed in Node.js and deployed using AWS Lambda via API Gateway.

## Microservices

- `user-service/` – Manages user authentication and roles
- `course-service/` – Handles course creation and management
- `progress-service/` – Tracks user learning progress

## Structure (per service)

- `index.js` or `handler.js` – Main Lambda handler
- `routes/`, `controllers/`, `models/` – Standard MVC pattern
- `serverless.yml` – Deployment descriptor

## Development

```bash
cd user-service
npm install
npm run dev
```

## Deployment (with Serverless Framework)

```bash
serverless deploy
```