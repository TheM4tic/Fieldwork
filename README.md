# FieldWork — Cloud Edition (Firebase Firestore)

Real-time task management for engineering teams. Single HTML file, GitHub Pages hosted, Firebase Firestore backend.

## Deploy in 3 steps

**Step 1 — GitHub Pages**
1. New repository on github.com (Public)
2. Upload index.html + .nojekyll
3. Settings → Pages → Branch main / root → Save
4. Live at: https://YOUR-USERNAME.github.io/REPO-NAME/

**Step 2 — Firebase (free)**
1. console.firebase.google.com → Add project
2. Build → Firestore Database → Create → Start in test mode
3. Project Settings → Web app → copy firebaseConfig JSON

**Step 3 — Connect**
1. Open your GitHub Pages URL
2. Paste your Firebase config into the setup screen
3. Click Connect & Launch — done!

## Hardcode config for teams (recommended)
Find in index.html:
  const [fbConfig,setFbConfig]=useState(()=>lsGet(LS_FB_CONFIG,null));

Replace with:
  const [fbConfig,setFbConfig]=useState({ apiKey:"...", projectId:"...", ... });

## Firestore Rules
In Firebase console → Firestore → Rules:
  rules_version = '2';
  service cloud.firestore {
    match /databases/{database}/documents {
      match /{document=**} {
        allow read, write: if true;
      }
    }
  }

## Default Logins
Georg Hansen    — g.hansen@fieldwork.com  / admin123  (Admin)
Maarten v Asten — m.vanasten@fieldwork.com / eng123   (Engineer)
Jan Kowalski    — j.kowalski@fieldwork.com / eng456   (Engineer)
Reza Moradi     — r.moradi@fieldwork.com  / eng789   (Engineer)
Tina Larsson    — t.larsson@fieldwork.com / view123  (Viewer)

## Free Firebase Tier
50,000 reads/day · 20,000 writes/day · 1GB storage
