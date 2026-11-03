# SmartCity Connect — Smart City Complaint Management System

A responsive frontend-only civic complaint management demo built with React + Vite, JavaScript, React Router, Tailwind CSS, Lucide React, Recharts, React Hook Form and Zod. It uses mock data and browser `localStorage`; no backend, database, REST API, or paid map key is required.

## Run locally

```bash
npm install
npm run dev
```

Open the local URL printed by Vite. To create a production build:

```bash
npm run build
npm run preview
```

## Demo accounts

| Role | Email | Password |
|---|---|---|
| Citizen | `citizen@smartcity.demo` | `citizen123` |
| Government Official | `official@smartcity.demo` | `official123` |
| Administrator | `admin@smartcity.demo` | `admin123` |

The login page includes a quick demo-role selector. Registration adds a citizen account to local storage.

## Features

- Public landing page, demo login and registration with validation.
- Role-aware dashboard navigation for citizens, officials and administrators.
- Seeded complaint records, submission form with image preview, generated complaint IDs, detail timeline and feedback.
- Complaint search, filtering, status updates, department/official assignment fields and CSV export.
- React Leaflet + OpenStreetMap complaint map with sample Jaipur coordinates and local filters (tile imagery needs internet access).
- Recharts dashboard analytics calculated from the current complaint dataset.
- Notification center, user role management, department editor and profile preferences.
- Responsive desktop, tablet and mobile layouts.

## Data and security limitations

- Seeded data is only used when a browser has no saved data for the corresponding key; changes persist in `localStorage`.
- Map coordinates are illustrative. The map uses public OpenStreetMap tiles, which require internet access; complaint records are still local and public markers do not show citizen contact details.
- Role restrictions are frontend-only demonstration controls. They are **not secure authorization** and must not be used as a security boundary in a production system.
- Demo passwords are stored in local browser state, and complaint image previews may be stored as data URLs. Do not enter sensitive or real citizen information.
- All reports, assignments, status updates, notifications and analytics are simulated. Nothing is submitted to a government authority.

## Structure

```text
src/
  components/  Reusable layout and UI elements
  context/     Shared application state + localStorage persistence
  data/        Seed users, departments, notifications and complaints
  pages/       Landing, auth, citizen, official and admin pages
  main.jsx     Router and route guards
  index.css    Responsive design system and page styling
```
