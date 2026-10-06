# RAKSHA — AI Disaster Intelligence & Response Platform

A single Node.js + Express application that serves the RAKSHA frontend and API from the same origin.

## Run locally

```powershell
npm install
npm start
```

Open:

- http://localhost:5000
- http://localhost:5000/api/health

## Features

- Interactive Leaflet/OpenStreetMap map
- Browser geolocation
- Live weather from Open-Meteo (no API key)
- Best-effort NCS earthquake ingestion with local cache
- Risk scoring engine combining weather, earthquakes and citizen reports
- Dynamic risk zones around the selected location
- Shelters, hospitals and emergency services
- Citizen incident reports saved to JSON file
- AI response assistant grounded in current dashboard data
- Safest-route request using OSRM with a fallback route
- Dashboard, alerts, resources and analytics
- Same-origin `/api` calls so GitHub Pages/localhost CORS confusion is avoided

## Deploy

This project is designed for a Node web service such as Render, Railway or another Node-compatible host. GitHub stores the code; the host runs the Node server.

## Important data note

The risk score is a decision-support index, not an official government warning. Government data sources and third-party public services can be unavailable or delayed, so source status is exposed in the API and UI.
