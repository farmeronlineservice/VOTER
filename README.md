# Voter Management App

Mobile-friendly voter list + family + booth analysis. Data on Firebase Realtime Database.

## Live use (GitHub Pages)

1. Create a new GitHub repository
2. Upload `index.html` (this is the full single-file app)
3. Repo **Settings → Pages → Source: Deploy from branch → main / root**
4. Open the Pages URL on any mobile browser

Or use any static host: Netlify, Vercel, Cloudflare Pages — just upload `index.html`.

## Firebase

Database URL used in app:

`https://voter-c464f-default-rtdb.firebaseio.com`

Rules (open — change later for production):

```json
{
  "rules": {
    ".read": true,
    ".write": true
  }
}
```

## Features

- Auto load data on page open
- Auto save when you mark preference / contacted / slip / etc.
- Name tap → full family with Sr No
- Booth summary with address names
- Print: Ward+Sr / Ward+A-Z / Name A-Z / Sr only
- Pagination 100 per page
- Works offline UI; needs internet for Firebase load/save
