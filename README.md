# ☕ Cozy - Multi-Agent Sales Tracker

A modern sales and inventory tracking system featuring **Owner vs Agent multi-user roles**, custom profile pictures & display names, PIN authentication, and live cloud synchronization powered by **Firebase Realtime Database**.

---

## 📁 2-File Architecture

```
cozy/
├── index.html       # Profile login & PIN screen ("Who's using Cozy?")
└── dashboard.html   # Full Dashboard (Owner view + Each Agent's own view)
```

---

## 🖼️ Profile Pictures & Custom Names

### For Owner:
1. Go to the **Settings** tab in `dashboard.html`.
2. Under **Profile Settings**:
   - Change your **Display Name**.
   - Set a **Profile Picture** by either **pasting an Image URL** or clicking **📁 Upload Photo File** directly from your phone/computer.
3. Click **Save Profile**. Your picture and name update immediately across the sidebar, dashboard, and login screen cards on `index.html`.

### For Admins & Agents:
1. **When adding an Agent** (on `index.html` via `+ Add Profile` or in `dashboard.html` via `+ Add Profile` in the Users tab):
   - Set the agent's name, PIN, role, and attach a **Profile Picture** (via image URL or 📁 file upload).
2. **When editing an Agent** (in `dashboard.html` > **Users** tab):
   - The Owner can click **Edit** on any agent card to change their display name, PIN, commission mode, or update their **Profile Picture** anytime.

---

## 👥 How the Roles Work

### 👑 Owner View
- **Overview Dashboard**: Gross revenue, total profit, capital invested, and live charts across **all agents combined**.
- **Sales Log**: View and search all sales logged by every agent, or filter by specific agents.
- **Account Tracker**: Streaming slots & account inventory (Netflix, Spotify, Canva, CapCut, etc.).
- **Product Catalog**: Manage products, base prices, costs, and categories.
- **Salary Rules & Payroll**: Set commission rules, review payouts for every agent, mark payouts as paid.
- **Users Management**: Add new agents, change agent PINs, update photos, and adjust individual commission rates.
- **Store Settings**: Change shop name, currency, backup/restore data.

### 👤 Agent View (Each Agent Gets Their Own!)
- **My Dashboard**: Shows **only their personal sales count, revenue, and commission earned**.
- **My Sales**: Only logs and displays **their own sales**. Cannot see other agents' sales.
- **My Accounts**: Their own tracked accounts and slots.
- **My Salary**: Personal earnings and salary calculation breakdown.

---

## 🔑 Default Login
- **Owner**: Select **Owner** avatar ➔ Enter PIN **`1234`**
- Click **+ Add Profile** on `index.html` to create new agents with photos.
