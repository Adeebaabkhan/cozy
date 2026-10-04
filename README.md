# ☕ Cozy - Multi-Agent Sales Tracker

A modern sales and inventory tracking system featuring **Owner vs Agent multi-user roles**, PIN authentication, and live cloud synchronization powered by **Firebase Realtime Database**.

---

## 📁 2-File Architecture

The `cozy` project consists of **2 files**:

```
cozy/
├── index.html       # Profile picker & PIN login screen ("Who's using Cozy?")
└── dashboard.html   # Main dashboard (Owner view + Agent-specific views)
```

---

## 👥 How the Roles Work

### 👑 Owner View
- **Overview Dashboard**: Gross revenue, total profit, capital invested, and live charts across **all agents**.
- **Sales Log**: View all sales logged by all agents, or filter by specific agents.
- **Account Tracker**: Streaming slots & account availability (Netflix, Spotify, Canva, CapCut, etc.).
- **Product Catalog**: Manage products, base prices, costs, and categories.
- **Salary Rules & Payroll**: Set commission brackets/rates, review payouts for every agent, mark as paid.
- **Users Management**: Add new agents, edit agent PINs, customize commission modes (Brackets or Flat %).
- **Store Settings**: Change shop name, currency, backup/restore data.

### 👤 Agent (Admin) View — Each Agent Gets Their Own!
- **My Dashboard**: Shows only their personal sales count, revenue, and commission earned.
- **My Sales**: Only logs and views **their own sales**. Cannot see other agents' sales.
- **My Accounts**: Their own tracked accounts and slots.
- **My Salary**: Personal earnings and salary calculation breakdown.
- **Users tab is hidden**: Agents cannot access or edit other user profiles.

---

## 🔑 Default Login
- **Owner**: Select **Owner** avatar ➔ Enter PIN **`1234`**
- Click **+ Add Profile** on `index.html` to create new agents (e.g. `@sarah`, `@agent1`).

---

## ☁️ Firebase Configuration
Configured with your Firebase Realtime Database project (`maisonetoile-5eee1`) under database path:
```
/cozy
```
