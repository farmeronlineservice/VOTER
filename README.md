# Voter Management — Multi Gram Panchayat

## Files
- `admin.html` — Admin panel (add/delete panchayat, generate links, migrate data)
- `index.html` — Voter app for **one** panchayat: open as `index.html?gp=deori`

## Deploy (GitHub Pages / Netlify)
Upload `index.html` + `admin.html` together. Open `admin.html` first.

## Setup flow
1. Open **admin.html**
2. Add Gram Panchayat (name + slug e.g. Deori / deori)
3. Copy generated link → share with workers (mobile)
4. If old data is in root `/voters`, use **Migrate** to move into that GP
5. In GP app: Import Excel if needed → Save (full) once

## Firebase paths
- `panchayats/{slug}` — list meta
- `gp/{slug}/voters/{id}` — voter records
- `gp/{slug}/meta` — updatedAt / count

Legacy root `/voters` still readable as fallback once for migration.
