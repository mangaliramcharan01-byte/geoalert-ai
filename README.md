# GeoAlert AI

Responsive hackathon-ready frontend prototype for SIH26001. It runs with no build step or dependencies.

## Run locally

Open `index.html` in a modern browser, or serve this directory with any static-file server.

## Demo credentials

The prototype opens in Administrator demo mode. Production role handling should use JWT-protected API endpoints.

## Integration points

Replace the browser-side `calculate()` method in `app.js` with `POST /api/predict-risk`, returning `{ riskScore, riskLevel, confidence, recommendations }`. Suggested production stack: React/Vite + FastAPI + PostgreSQL/PostGIS + a versioned Scikit-learn/XGBoost model.

## Proposed API

`GET /api/locations`, `GET /api/risk-map`, `GET /api/sensors`, `GET /api/weather`, `GET /api/alerts`, `GET /api/incidents`, `GET /api/analytics`, `POST /api/predict-risk`, `POST /api/reports`, `PUT /api/alerts/:id`.

## Suggested data model

`users`, `sensors`, `sensor_readings`, `locations`, `risk_predictions`, `alerts`, `incidents`, `citizen_reports`, `historical_landslides`, `weather_data`, `infrastructure`, and `notifications`.

All displayed values are clearly marked as demo data; do not use this UI as an official warning source.
