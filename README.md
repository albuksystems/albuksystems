<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Albuksystems | Credit Risk Calculator</title>
    <style>
        body { font-family: sans-serif; background: #f4f4f4; padding: 20px; }
        .card { background: white; padding: 20px; border-radius: 10px; max-width: 400px; margin: auto; box-shadow: 0 4px 6px rgba(0,0,0,0.1); }
        h2 { color: #333; font-size: 1.2rem; }
        label { display: block; margin-top: 10px; font-size: 0.9rem; }
        input { width: 100%; padding: 8px; margin-top: 5px; border: 1px solid #ccc; border-radius: 5px; box-sizing: border-box; }
        button { width: 100%; background: #007bff; color: white; border: none; padding: 10px; margin-top: 20px; border-radius: 5px; cursor: pointer; }
        #result { margin-top: 20px; font-weight: bold; text-align: center; padding: 10px; border-radius: 5px; display: none; }
    </style>
</head>
<body>

<div class="card">
    <h2>Albuksystems Credit Risk Tool</h2>
    <label>Customer Total Debt (Ksh)</label>
    <input type="number" id="debt" placeholder="e.g. 5000">
    
    <label>Last Payment (Days Ago)</label>
    <input type="number" id="days" placeholder="e.g. 15">
    
    <button onclick="calculateRisk()">Check Risk Level</button>
    
    <div id="result"></div>
</div>

<script>
    function calculateRisk() {
        let debt = document.getElementById('debt').value;
        let days = document.getElementById('days').value;
        let res = document.getElementById('result');
        res.style.display = "block";

        if (days > 60 || debt > 50000) {
            res.innerHTML = "🔴 HIGH RISK: Stop Credit Sales";
            res.style.background = "#ffdce0";
            res.style.color = "#af233a";
        } else if (days > 30) {
            res.innerHTML = "🟡 MEDIUM RISK: Follow up for Payment";
            res.style.background = "#fff3cd";
            res.style.color = "#856404";
        } else {
            res.innerHTML = "🟢 LOW RISK: Account Healthy";
            res.style.background = "#d4edda";
            res.style.color = "#155724";
        }
    }
</script>

</body>
</html>




# Credit Control & Debt Tracking System 📊

### 🏗️ Project Overview
This module is a core component of the **Albuksystems Retail Suite**. It is designed to solve the "silent killer" of small businesses: unmanaged credit. This system automates the tracking of customer debts, payment deadlines, and credit limits to ensure healthy cash flow.

### 🚀 Key Features (AI-Driven Logic)
- **Customer Debt Ledger:** Real-time tracking of individual balances.
- **Automated Aging Reports:** Categorizes debt by 30, 60, and 90+ days.
- **Credit Limit Enforcement:** System-level blocks on sales to high-risk accounts.
- **WhatsApp Integration Ready:** Designed to push automated payment reminders to clients.

### 🛠️ Technical Stack
- **Architecture:** Modular JavaScript/HTML for lightweight retail environments.
- **Data Structure:** JSON-based local storage for offline-first reliability in areas with unstable internet.
- **Development Method:** AI-assisted prototyping using Claude/GPT-4o for rapid iteration.

### 📂 How it Works
1. **Entry:** Sales data is captured and checked against the customer's credit profile.
2. **Analysis:** The system calculates the risk score based on payment history.
3. **Action:** Triggers a notification for overdue accounts to prevent stock leakage.

---
*Developed by **Albuksystems** | Bridging the gap between traditional retail and digital precision.*
