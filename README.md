# ParkMelbourne Smart

A full-stack MVP for a Melbourne smart-parking system. It demonstrates real-time bay availability, map search, reservation/payment simulation, issue reporting, and a council administration dashboard.

## Features

- Interactive Melbourne parking map using Leaflet + OpenStreetMap
- Filter by availability, parking type and hourly price
- Simulated IoT occupancy updates
- Reserve an available bay
- Automatic fee calculation and simulated payment
- Booking history
- User issue reporting
- Admin metrics and report workflow
- SQLite persistence
- REST API
- Responsive layout

## Technology

- Node.js
- Express
- SQLite via `better-sqlite3`
- HTML/CSS/JavaScript
- Leaflet + OpenStreetMap

## Run

1. Install Node.js 18+.
2. Open a terminal in this project folder.
3. Run:

```bash
npm install
npm start
```

4. Open `http://localhost:3000`.

For development:

```bash
npm run dev
```

## Main API endpoints

- `GET /api/parking`
- `GET /api/parking/:id`
- `PATCH /api/parking/:id/status`
- `POST /api/bookings`
- `GET /api/bookings`
- `POST /api/reports`
- `GET /api/reports`
- `PATCH /api/reports/:id`
- `GET /api/admin/stats`
- `POST /api/simulate`

## Important MVP assumptions

The seeded parking bays are demonstration records, not an authoritative City of Melbourne parking dataset. Occupancy is simulated. Payment is simulated and no card details are collected.

For a production deployment, replace the simulator with real IoT sensor events, connect an official parking/kerbside dataset, use authenticated user/admin accounts, integrate a PCI-compliant payment provider, and implement audit logging, privacy controls and operational monitoring.
