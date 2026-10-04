# ☕ Cozy - Personal Sales Tracker

A modern, elegant, self-contained personal sales and inventory tracking web application with live cloud synchronization powered by **Firebase Realtime Database**.

Designed with a warm cozy aesthetic (Espresso Dark & Latte Light themes), built as a single responsive web page ready to deploy directly to **GitHub Pages**.

---

## ✨ Features

- 📊 **Executive Metrics**: Live Revenue, Capital Invested, Net Profit, Profit Margin (%), and Total Orders.
- ⚡ **Firebase Real-Time Cloud Sync**: Instant live synchronization across mobile, desktop, and tablets using Firebase Realtime Database.
- 💾 **Offline-First Resilience**: Automatic fallback to LocalStorage if offline or network drops, seamlessly syncing back once reconnected.
- 📈 **Interactive Charts**:
  - Revenue & Net Profit Trend Line Chart (7 days, 30 days, or all-time).
  - Product Distribution Donut Breakdown.
- 🛍️ **Product Catalog**:
  - Save items with default selling price and purchase/cost price.
  - 1-click **"+ Log Sale"** button directly from product cards.
  - Stock / inventory tracking.
- 📝 **Sales Log**:
  - Search by customer name, order ID, product name, or note.
  - Filter by date range (Today, This Week, This Month, All) and payment status.
  - Instant CSV export for Excel / Google Sheets.
  - Edit and delete sales records.
- 🎨 **Aesthetics & Themes**:
  - Espresso Dark 🌙 and Vanilla Latte Light ☀️ modes.
  - 5 customizable accent color swatches (Warm Amber, Terracotta, Caramel, Matcha, Rose).
- 🔒 **Data Backup & Restore**: Export full JSON backup or import anytime.

---

## 🚀 How to Add & Deploy to GitHub Pages

### Option 1: New Dedicated GitHub Repository
1. In your GitHub account, create a new repository named `cozy` (or `sales-tracker`).
2. Inside your local `Downloads/cozy` folder, initialize Git:
   ```bash
   git init
   git add .
   git commit -m "Initial commit of Cozy Sales Tracker"
   git branch -M main
   git remote add origin https://github.com/YOUR_USERNAME/cozy.git
   git push -u origin main
   ```
3. In GitHub, go to **Settings** > **Pages** > Select branch `main` and root `/` > Click **Save**.
4. Your site will be live at `https://YOUR_USERNAME.github.io/cozy/`!

### Option 2: Subfolder in an Existing Repository
1. Copy the `cozy` folder into your existing repository.
2. Push to GitHub:
   ```bash
   git add cozy
   git commit -m "Add Cozy sales tracker"
   git push
   ```
3. Access it at `https://YOUR_USERNAME.github.io/REPO_NAME/cozy/`.

---

## ☁️ Firebase Configuration

The web application is pre-configured with your Firebase Realtime Database project (`maisonetoile-5eee1`).

### Firebase Security Rules
To ensure data can be saved and read seamlessly, verify that your Firebase Realtime Database rules allow read/write under the `/cozy` node in the [Firebase Console](https://console.firebase.google.com/):

```json
{
  "rules": {
    "cozy": {
      ".read": true,
      ".write": true
    }
  }
}
```

---

## 📁 File Structure

```
cozy/
├── index.html       # Standalone single-page web application
└── README.md        # Documentation and deployment instructions
```
