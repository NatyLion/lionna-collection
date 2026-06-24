# LIONNA™ — Collection & Supplier Management System · SS27

> **She Moves. The World Adjusts.**  
> Phase 1 · Spring/Summer 2027 · Luxury Active Living · Brazil

---

## 🌐 Live Tool (GitHub Pages)

**URL:** `https://[your-username].github.io/lionna-collection`

Anyone with this link can open the tool in their browser — no login, no install.

---

## 📂 Files in This Repository

| File | Purpose |
|------|---------|
| `index.html` | Main web tool — Supplier CRM, Scoring, RFQ Tracker, Collection, FOB Calculator |
| `LIONNA_Collection_Management_System.xlsx` | Excel version — quotes, scoring model, FOB→D2D, fabrics |
| `LIONNA_RFQ_SS27_001.html` | Printable RFQ document — send to OEM suppliers as PDF |
| `README.md` | This file |

---

## 🚀 How to Set Up GitHub Pages (5 steps)

### Step 1 — Create your GitHub account
Go to [github.com](https://github.com) → Sign up (free)

### Step 2 — Create the repository
1. Click **"New repository"** (green button, top right)
2. Name: `lionna-collection`
3. Set to **Public** (required for free GitHub Pages)
4. Click **"Create repository"**

### Step 3 — Upload files
1. In your new repository, click **"uploading an existing file"**
2. Drag and drop ALL files from this folder:
   - `index.html` (rename `LIONNA_Collection_Management_System.html` to `index.html`)
   - `LIONNA_Collection_Management_System.xlsx`
   - `LIONNA_RFQ_SS27_001.html`
   - `README.md`
3. Click **"Commit changes"**

### Step 4 — Enable GitHub Pages
1. Click **Settings** (top tabs of your repository)
2. Scroll to **Pages** (left sidebar)
3. Under "Source": select **Deploy from a branch**
4. Branch: **main** · Folder: **/ (root)**
5. Click **Save**
6. Wait ~2 minutes. Your URL appears: `https://[username].github.io/lionna-collection`

### Step 5 — Share the link
Send the URL to your team. Anyone can open it in Chrome, Safari, or any browser.

---

## 👥 How the Team Uses This

### Adding suppliers
1. Open the live URL
2. Click **Suppliers** tab → **+ Supplier**
3. Fill in name, Alibaba URL, contact, MOQ, etc.
4. Data saves in your browser (localStorage)

### Logging quotes (when OEMs respond)
1. Click **RFQ & Quotes** tab → **+ Log Quote**
2. Enter supplier, SKU, FOB price
3. System auto-calculates: Landed USD → Landed R$ → Gross Margin → Net Margin

### Scoring suppliers
1. Click **Scoring Model** tab
2. Adjust sliders 0–10 for each variable per supplier
3. Rankings update in real time

### Exporting data
- **JSON backup:** Click **Export** button (top right) → saves `LIONNA_Data_[date].json`
- **Excel:** Download `LIONNA_Collection_Management_System.xlsx` → edit in Excel or Google Sheets
- **PDF for OEMs:** Open `LIONNA_RFQ_SS27_001.html` → Print → Save as PDF

---

## 🔄 Keeping Data Synchronized Between Team Members

### Option A: Each person exports JSON → shares via WhatsApp/Email
1. Person A makes changes → clicks **Export** → shares JSON file
2. Person B receives JSON → can import (future feature)

### Option B: Supabase (real-time database — free tier)
For real-time collaboration where everyone sees the same data:

1. Go to [supabase.com](https://supabase.com) → Create free account
2. Create new project → name: `lionna-db`
3. In SQL Editor, run:
```sql
CREATE TABLE suppliers (id text primary key, data jsonb, updated_at timestamptz default now());
CREATE TABLE quotes (id text primary key, data jsonb, updated_at timestamptz default now());
CREATE TABLE skus (id text primary key, data jsonb, updated_at timestamptz default now());
```
4. Copy your **Project URL** and **anon key** from Settings → API
5. Share with Claude to integrate into the HTML tool

### Option C: Google Sheets (easiest for non-technical team)
Import the Excel file into Google Drive → Share → anyone with link can edit

---

## 📊 Excel File — How to Use

### Opening
Download `LIONNA_Collection_Management_System.xlsx` → open in Excel or Google Sheets

### Sheets overview
| Tab | Purpose | Editable cells |
|-----|---------|----------------|
| DASHBOARD | Overview KPIs | Read only (auto-calculates) |
| SUPPLIERS | Supplier CRM | All columns |
| SCORING | Math scoring model | Blue cells (scores 0–10) + yellow (weights) |
| RFQ_QUOTES | Quote log | Blue cells (FOB, supplier, SKU, MOQ) |
| FOB_D2D_CALC | Cost calculator | Yellow cells (assumptions) + blue (FOB per SKU) |
| COLLECTION | Full SKU list | Status column + FOB when known |
| FABRICS | Material library + Golden Rules | All fabric rows |

### Color coding (Excel standard)
- 🔵 **Blue text** = your input — change these
- 🟡 **Yellow background** = key assumptions — update when rates change
- ⬛ **Black text** = formula — do not edit

---

## 📧 Sending the RFQ to Suppliers

1. Open `LIONNA_RFQ_SS27_001.html` in Chrome
2. Replace `[Supplier Company Name]` with the supplier's name
3. **File → Print** (or Ctrl+P)
4. Destination: **Save as PDF**
5. Attach to email with subject: `RFQ-LIONNA-SS27-001 · [Supplier Name]`

---

## 📅 Launch Timeline

| Date | Milestone |
|------|-----------|
| Jun 2025 | RFQ sent to 6 suppliers |
| Jul 2025 | Quote responses received |
| Aug 2025 | Supplier selection by score |
| Sep 2025 | Sample orders placed |
| Oct 2025 | Sample review & approval |
| Nov 2025 | Bulk production order |
| Feb 2026 | Production complete |
| Mar 2026 | Shipment FOB China |
| Apr 2026 | Stock received Brazil |
| Jun 2026 | **SS27 LAUNCH 🦁** |

---

## 🦁 LIONNA Brand

**Campaign:** She Moves. The World Adjusts.  
**Positioning:** Luxury Active Living · Brazilian market  
**Contact:** natalialionn@gmail  
**Document:** RFQ-LIONNA-SS27-001

---

*Confidential — For LIONNA team and approved OEM partners only*

