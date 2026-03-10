# FieldWork — Task Management

Professional field engineering task management application. Kanban board, checklists, photo uploads, role-based access control, and a fully editable reference database.

## 🚀 Deploy to GitHub Pages (step-by-step)

### Step 1 — Create a GitHub account
Go to [github.com](https://github.com) and sign up (free). Skip if you already have one.

### Step 2 — Create a new repository
1. Click the **+** button (top right) → **New repository**
2. Name it anything, e.g. `fieldwork` or `my-tasks`
3. Set it to **Public** (required for free GitHub Pages)
4. Do **not** check "Add a README" (we'll upload our own files)
5. Click **Create repository**

### Step 3 — Upload the files
1. On your new empty repository page, click **uploading an existing file**
2. Drag and drop these two files:
   - `index.html`
   - `.nojekyll`
3. Scroll down, click **Commit changes**

> ⚠️ The `.nojekyll` file may be invisible on Windows/Mac. If you can't see it, you can skip it — the app will still work. It just prevents a minor GitHub Pages processing delay.

### Step 4 — Enable GitHub Pages
1. Click **Settings** (tab at the top of your repository)
2. Click **Pages** in the left sidebar
3. Under **Source**, select **Deploy from a branch**
4. Under **Branch**, select `main` → `/ (root)` → click **Save**
5. Wait ~60 seconds

### Step 5 — Open your live site
Your site is now live at:
```
https://YOUR-USERNAME.github.io/YOUR-REPO-NAME/
```
GitHub shows this URL at the top of the Pages settings page.

---

## 🔐 Default Login Credentials

| Name | Email | Password | Role |
|------|-------|----------|------|
| Georg Hansen | g.hansen@fieldwork.com | admin123 | Admin |
| Maarten van Asten | m.vanasten@fieldwork.com | eng123 | Engineer |
| Jan Kowalski | j.kowalski@fieldwork.com | eng456 | Engineer |
| Reza Moradi | r.moradi@fieldwork.com | eng789 | Engineer |
| Tina Larsson | t.larsson@fieldwork.com | view123 | Viewer |

> **First thing to do:** Sign in as Admin and change passwords in the Users page.

---

## 💾 Data Persistence

All data (tasks, users, database entries, photos) is saved automatically to your browser's **localStorage**. This means:

- ✅ Data survives page refresh
- ✅ Data survives closing and reopening the browser
- ⚠️ Data is stored **per browser** — different devices or browsers won't share data
- ⚠️ Clearing browser data/cache will erase stored data

> **Tip:** Use the Export CSV buttons regularly to back up your task data.

### Reset to demo data
As an Admin, click the **↺** button (top right of the toolbar) to wipe all data and return to the demo state.

---

## 📋 Role Permissions

| Action | Admin | Engineer | Viewer |
|--------|:-----:|:--------:|:------:|
| View all tasks | ✅ | ✅ | ✅ |
| Create tasks | ✅ | ✅ | ❌ |
| Edit own tasks | ✅ | ✅ | ❌ |
| Edit all tasks | ✅ | ❌ | ❌ |
| Drag & drop cards | ✅ | ❌ | ❌ |
| Delete tasks | ✅ | ❌ | ❌ |
| Upload photos | ✅ | ✅ | ❌ |
| Add comments | ✅ | ✅ | ❌ |
| Manage Database | ✅ | ❌ | ❌ |
| Manage Users | ✅ | ❌ | ❌ |

---

## 🗃️ Database / Reference Data

The database stores all dropdown options used in task attributes:
- Locations, Room Numbers, Plans
- Categories, Tags
- Suppliers, Contractors, Req. Codes
- Statuses, People

**To update via Excel/CSV:**
1. Go to **Database** page (Admin only)
2. Click **Export [Section]**
3. Edit in Excel or Google Sheets
4. Save as `.csv`
5. Click **Import CSV** to upload changes

---

## 🔄 Updating the App

When a new version of `index.html` is available:
1. Go to your GitHub repository
2. Click on `index.html`
3. Click the **pencil icon** (Edit) or click **...** → **Upload file**
4. Upload the new `index.html`
5. Commit — GitHub Pages updates automatically within ~60 seconds

---

## 📱 Mobile / Tablet

The app is fully responsive:
- **Mobile (< 768px):** Single-column board with column selector pills, bottom view toggle, "Move to" button on cards
- **Desktop:** Full multi-column Kanban, drag-and-drop, sidebar navigation

---

*Built with React 18 + Babel Standalone. No build tools required.*
