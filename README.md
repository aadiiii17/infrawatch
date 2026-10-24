# InfraWatch

A clickable prototype of a real-time infrastructure inspection platform. It has two sides:

- **Inspector app** (phone-style UI): check in at a site, verify location, capture evidence, fill the inspection form and export a report.
- **Admin Command Center**: live site map, KPIs, inspector activity, issues, analytics and reports.

It is a single static file (`index.html`) with no build step.

https://infrawatch-pro.netlify.app

## Features

- Role selection on login (Inspector or Admin), with email and password checks
- Site QR scanning with the device camera, or by uploading or taking a photo of a QR code
- GPS verification using the device's real location, checked against the site within a 150 m radius
- Camera evidence capture
- Inspection form and PDF report export
- Live monitoring map for admins, with a pin for each site
- Profile: editable name, phone, email and photo, notification and dark mode toggles
- English and Hindi

## Demo accounts

Use the "Use" buttons on the login screen, or type any email and password.

| Role | Email |
|------|-------|
| Inspector | demo.inspector@example.com |
| Admin | demo.admin@example.com |

## Run locally

Open `index.html` in a browser. Camera and location need a secure context, so they work on https pages or localhost.

## Notes

- All data (sites, inspectors, stats) is mock data for demonstration. The AI analysis step is simulated.
- Map tiles come from Esri (with OpenStreetMap as a fallback), so the map needs an internet connection.
- Libraries are loaded from CDNs: Leaflet, jsPDF and jsQR.

## Tech

HTML, CSS and vanilla JavaScript. Leaflet for maps, jsQR for QR decoding, jsPDF for reports.
