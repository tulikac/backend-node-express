# Express Backend Sample

A small Express application with no external service dependencies.

## Requirements

- Node.js 20 or later
- npm 10 or later

## Run locally

```powershell
npm install
npm start
```

The server listens on `PORT` when it is set and otherwise uses port `8080`.

Open `http://localhost:8080`.

## Verify

```powershell
npm test
.\scripts\verify.ps1 -BaseUrl http://localhost:8080
```

## Builder Apps configuration

The root `builder.yaml` declares one public Node.js web component. It uses the
repository root, starts through the existing `npm start` script, listens on port
`8080`, and reports readiness through `/health`.

## Routes

| Route | Purpose |
|---|---|
| `GET /` | Sample identity and deployment markers |
| `GET /products/widget-1` | Direct deep-link test |
| `GET /health` | Runtime health |
| `GET /api/status` | API reachability |
| `GET /api/version` | App, framework, runtime, and deployment identity |
| `GET /api/request` | Safe request metadata |
