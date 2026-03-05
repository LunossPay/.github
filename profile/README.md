<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0d0d0d,100:0d0d0d&height=180&section=header&text=LunosPay&fontSize=70&fontColor=A2E428&fontAlignY=45&desc=Fast%20Solana%20Payments%20Infrastructure&descAlignY=65&descSize=18&descColor=A2E428" width="100%" />

<br>

[Website](https://lunoss.com) •
[Developers](https://lunoss.dev) •
[LinkedIn](https://www.linkedin.com/company/lunoss-pay)

</div>

---

# LunosPay

**LunosPay** is a developer-focused payment infrastructure built on **Solana**.

Accept crypto payments globally with **instant settlement**, **low fees**, and **simple APIs**.

Built for **SaaS platforms, marketplaces, gaming, and global digital products**.

---

# Key Features

⚡ **Fast confirmations** (~500ms)  
💸 **Low fees** starting at **1%**  
🌍 **Global payments** without banks  
🔐 **Secure on-chain settlement**  
🧑‍💻 **Developer-first APIs and SDKs**

---

# Quick Start

Install the SDK:

```bash
npm install @lunospay/sdk
```

Example integration:

```javascript
import { LunosPay } from "@lunospay/sdk"

const lunos = new LunosPay({
  apiKey: process.env.LUNOSPAY_API_KEY
})

const payment = await lunos.createPayment({
  amount: 50,
  currency: "USDC",
  merchantWallet: "your-solana-wallet",
  description: "Product purchase"
})

console.log(payment.paymentUrl)
```

Payment confirmation webhook:

```javascript
lunos.onPaymentConfirmed((data) => {
  console.log("Payment confirmed:", data.txId)
})
```

---

# How It Works

1. Create a payment using the API  
2. Receive a **payment link or QR code**  
3. Customer pays using a **Solana wallet**  
4. Transaction confirms on-chain  
5. Funds go directly to your wallet

---

# Pricing

| Plan | Monthly | Fee |
|-----|-----|-----|
| Free | $0 | 1% |
| Starter | $49 | 0.8% |
| Growth | $299 | 0.5% |
| Enterprise | Custom | Negotiable |

---

# Use Cases

**E-commerce**  
Accept crypto payments globally.

**SaaS Platforms**  
Subscription payments without traditional processors.

**Gaming**  
Microtransactions and in-game purchases.

**Marketplaces**  
Fast payouts for creators and sellers.

---

# Tech Stack

**Blockchain**

Solana • Web3.js

**Backend**

Node.js • TypeScript • PostgreSQL

**Frontend**

Next.js • React • TailwindCSS

**Infrastructure**

Docker • AWS • GitHub Actions

---

# Repositories

| Repository | Description |
|---|---|
| lunospay-core | Smart contracts |
| lunospay-api | Backend services |
| lunospay-sdk | JavaScript SDK |
| lunospay-dashboard | Merchant dashboard |

---

# Security

• On-chain settlement  
• Signed webhooks  
• Secure API authentication  
• Smart contract audits

---

# Links

Website  
https://lunoss.com

Developer Docs  
https://lunoss.dev

LinkedIn  
https://www.linkedin.com/company/lunoss-pay

---

# Contact

Support  
support@lunoss.com

---

<div align="center">

MIT © LunosPay

</div>
