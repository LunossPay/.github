<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0d0d0d,50:1a1a1a,100:0d0d0d&height=220&section=header&text=LunosPay&fontSize=80&fontColor=d4f542&fontAlignY=40&desc=The%20Future%20of%20Payments%20on%20Solana&descAlignY=62&descSize=22&descColor=a8c73a&animation=fadeIn" width="100%"/>

<br/>

[![SDK](https://img.shields.io/npm/v/@lunospay/sdk?color=d4f542&labelColor=0d0d0d&label=SDK&style=for-the-badge)](https://www.npmjs.com/package/@lunospay/sdk)
[![License](https://img.shields.io/badge/License-MIT-d4f542?style=for-the-badge&labelColor=0d0d0d)](LICENSE)
[![Discord](https://img.shields.io/badge/Discord-2000%2B-d4f542?style=for-the-badge&labelColor=0d0d0d&logo=discord&logoColor=d4f542)](https://discord.gg/lunospay)
[![Twitter](https://img.shields.io/badge/Twitter-10K%2B-d4f542?style=for-the-badge&labelColor=0d0d0d&logo=twitter&logoColor=d4f542)](https://twitter.com/lunospaydev)
[![GitHub Stars](https://img.shields.io/github/stars/lunospay?color=d4f542&labelColor=0d0d0d&style=for-the-badge&logo=github&logoColor=d4f542)](https://github.com/lunospay)

<br/>

> ### _Process Solana payments in under **500ms** — **1% flat fee**, instant settlement, zero bureaucracy._

<br/>

[![Get Started](https://img.shields.io/badge/▶_Get_Started_Free-d4f542?style=for-the-badge&labelColor=0d0d0d&color=d4f542)](https://lunospay.dev)
[![Docs](https://img.shields.io/badge/📖_Documentation-0d0d0d?style=for-the-badge&labelColor=d4f542&color=0d0d0d)](https://docs.lunospay.dev)
[![API](https://img.shields.io/badge/🔐_API_Reference-0d0d0d?style=for-the-badge&labelColor=d4f542&color=0d0d0d)](https://api.lunospay.dev/docs)

</div>

<br/>

<img src="https://capsule-render.vercel.app/api?type=rect&color=d4f542&height=3&section=header" width="100%"/>

<br/>

## ◈ By the Numbers

```
╔══════════════════════════════════════════════════════════════════════════════╗
║                            LUNOSPAY  AT A GLANCE                            ║
╠══════════════════╦══════════════════╦══════════════════╦════════════════════╣
║   SPEED          ║   VOLUME         ║   PROJECTS       ║   UPTIME           ║
║   ~500ms         ║   $10M+ USDC/mo  ║   500+ Active    ║   99.99%           ║
║   confirmation   ║   processed      ║   integrations   ║   guaranteed       ║
╚══════════════════╩══════════════════╩══════════════════╩════════════════════╝
```

<br/>

## ◈ Fee Savings vs. Traditional Processors

| Monthly Volume | Stripe `2.9%` | PayPal `3.5%` | **LunosPay `1%`** | ✦ Your Savings |
|----------------|:------------:|:--------------:|:-----------------:|:--------------:|
| $10,000        | $290         | $350           | **$100**          | **$190–$250**  |
| $100,000       | $2,900       | $3,500         | **$1,000**        | **$1,900–$2,500** |
| $500,000       | $14,500      | $17,500        | **$5,000**        | **$9,500–$12,500** |
| $1,000,000     | $29,000      | $35,000        | **$10,000**       | **$19,000–$25,000** |

> **✦ For every $1M processed, you save up to $25,000 compared to legacy processors.**

<br/>

## ◈ Performance Benchmark

```
  Payment Confirmation Speed — lower is better
  ──────────────────────────────────────────────────────────────────────

  LunosPay      ▓▓ ~500ms                                    ← ✦ YOU
  ACH           ▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓ ~2 days
  Stripe        ▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓ ~2-3 days
  PayPal        ▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓ ~3-5 days
  Wire Transfer ▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓ ~5-7 days

  Scale: each ▓ ≈ half a day
```

<br/>

<img src="https://capsule-render.vercel.app/api?type=rect&color=d4f542&height=3&section=header" width="100%"/>

<br/>

## ◈ Quick Start

```bash
# Install the SDK
npm install @lunospay/sdk

# Set your API key
export LUNOSPAY_API_KEY="lp_live_xxxxxxxxxxxxxxxxxxxx"
```

```javascript
import { LunosPay } from '@lunospay/sdk';

const lunos = new LunosPay({ apiKey: process.env.LUNOSPAY_API_KEY });

// ✦ Create a payment in 3 lines
const payment = await lunos.createPayment({
  amount: 50,
  currency: 'USDC',
  merchantWallet: 'your-solana-wallet',
  description: 'Purchase of product X'
});

console.log('QR Code:', payment.qrCode);          // → Ready to display
console.log('Payment Link:', payment.paymentUrl); // → Ready to share

// ✦ Get notified the instant it confirms
lunos.onPaymentConfirmed((data) => {
  console.log(`Payment confirmed! TxID: ${data.txId}`);
  // Money is already in your wallet.
});
```

> **First integration in under 5 minutes.** &nbsp;[Full Documentation →](https://docs.lunospay.dev)

<br/>

## ◈ How It Works

```
  USER               LUNOSPAY              SOLANA BLOCKCHAIN
   │                     │                        │
   │── createPayment ───>│                        │
   │                     │─── Deploy PDA ────────>│
   │<── QR + Link ───────│                        │
   │                     │                        │
   │── Scan & Pay ───────────────────────────────>│
   │                     │                        │
   │                     │<── Tx Confirmed ✦ ─────│
   │                     │         (~500ms)        │
   │<── Webhook ─────────│                        │
   │                     │─── Release Funds ─────>│
   │                     │                        │
   ▼                     ▼                        ▼
              Total elapsed: under 30 seconds
```

**Five steps. Under 30 seconds. Money in your wallet.**

1. **Create** — Call the API, receive a QR code and payment link instantly
2. **Share** — Customer scans the QR or opens the payment link
3. **Confirm** — Solana validates the transaction in ~500ms
4. **Notify** — Your webhook fires the moment it's confirmed
5. **Settle** — Funds are in your wallet. No waiting. No clearing.

<br/>

<img src="https://capsule-render.vercel.app/api?type=rect&color=d4f542&height=3&section=header" width="100%"/>

<br/>

## ◈ Use Cases

<table>
<tr>
<td width="33%">

### ✦ E-Commerce
Accept crypto natively. **Zero chargebacks**, instant settlement, global reach with no additional setup.

</td>
<td width="33%">

### ✦ SaaS & Subscriptions
Recurring billing without traditional processors. Go international with zero friction.

</td>
<td width="33%">

### ✦ Gaming
P2P and in-game purchases at scale. Microtransactions actually make sense at 1%.

</td>
</tr>
<tr>
<td width="33%">

### ✦ NFT Marketplaces
Native SPL token support with **automatic royalty splits** across multiple wallets.

</td>
<td width="33%">

### ✦ Freelancing & Payroll
Instant cross-border payments. No SWIFT fees, no 5-day holds, no middlemen.

</td>
<td width="33%">

### ✦ Fundraising & DAOs
Accept donations and investments on-chain with **total transparency**.

</td>
</tr>
</table>

<br/>

## ◈ Plans & Pricing

| | 🆓 Free | 🚀 Starter | 📈 Growth | 🏢 Enterprise |
|:--|:--:|:--:|:--:|:--:|
| **Price** | $0/mo | $49/mo | $299/mo | Custom |
| **Transactions** | 100/mo | Unlimited | Unlimited | Unlimited |
| **Fee** | 1.0% | 0.8% | 0.5% | Negotiable |
| **Support** | Email | Priority | 24/7 + Manager | Dedicated SLA |
| **Analytics** | Basic | Advanced | Advanced | Custom |
| **Webhooks** | Basic | Custom | Custom | Custom |
| **White-Label** | — | — | — | ✦ |
| **KYC / AML** | — | — | ✦ | ✦ |
| **Custom Integrations** | — | — | ✦ | ✦ |

> **✦ Volume discounts available on all paid plans.** &nbsp;[Talk to Sales →](mailto:sales@lunospay.dev)

<br/>

<img src="https://capsule-render.vercel.app/api?type=rect&color=d4f542&height=3&section=header" width="100%"/>

<br/>

## ◈ Security Architecture

```
╔══════════════════════════════════════════════════════════════════╗
║                    LUNOSPAY  SECURITY STACK                      ║
╠═════════════════════╦══════════════════════╦═════════════════════╣
║  TRUSTLESS ESCROW   ║  SIGNED WEBHOOKS     ║  THIRD-PARTY AUDITS ║
║                     ║                      ║                     ║
║  Funds held in      ║  Every webhook is    ║  Smart contracts    ║
║  on-chain PDAs.     ║  signed HMAC-SHA256. ║  audited by         ║
║  Zero centralized   ║  Verify in one line  ║  specialized firms. ║
║  custody ever.      ║  of code.            ║  Reports are public.║
╚═════════════════════╩══════════════════════╩═════════════════════╝
```

**Webhook Verification:**

```javascript
import { LunosPay } from '@lunospay/sdk';

app.post('/webhook', (req, res) => {
  const sig = req.headers['x-lunospay-signature'];
  const valid = LunosPay.verifyWebhook(req.body, sig, process.env.WEBHOOK_SECRET);

  if (!valid) return res.status(401).send('Invalid signature');

  const { event, payment } = req.body;
  if (event === 'payment.confirmed') {
    fulfillOrder(payment.metadata.orderId); // Funds are already in your wallet
  }

  res.sendStatus(200);
});
```

<br/>

## ◈ Roadmap

```
  ╔══════════════════════════════════════════════════════════════════╗
  ║  Q2 2025   ████████████████████████  ✦ SHIPPED                  ║
  ║            Core payment processing                               ║
  ║            REST API + Merchant Dashboard                         ║
  ║            Devnet launch                                         ║
  ╠══════════════════════════════════════════════════════════════════╣
  ║  Q3 2025   ████████████████████████  ✦ SHIPPED                  ║
  ║            Mobile SDK (iOS + Android)                            ║
  ║            SDKs: JavaScript, Python, Go, Rust                    ║
  ║            Shopify & WooCommerce plugins                         ║
  ║            Mainnet launch                                        ║
  ╠══════════════════════════════════════════════════════════════════╣
  ║  Q4 2025   ████████████░░░░░░░░░░░░  ◈ IN PROGRESS              ║
  ║            Full White-Label solution                             ║
  ║            Advanced analytics suite                              ║
  ║            Compliance suite (KYC/AML)                            ║
  ║            Global partnerships                                   ║
  ╠══════════════════════════════════════════════════════════════════╣
  ║  2026+     ░░░░░░░░░░░░░░░░░░░░░░░░  ○ PLANNED                  ║
  ║            Enterprise features & custom SLAs                     ║
  ║            Multi-chain support                                   ║
  ║            Loyalty & rewards programs                            ║
  ║            Developer marketplace                                 ║
  ╚══════════════════════════════════════════════════════════════════╝
```

<br/>

<img src="https://capsule-render.vercel.app/api?type=rect&color=d4f542&height=3&section=header" width="100%"/>

<br/>

## ◈ Tech Stack

<table>
<tr>
<td width="25%" align="center">

**⛓ Blockchain**

`Solana` `Web3.js`
`PDAs` `Jupiter DEX`

</td>
<td width="25%" align="center">

**◈ Backend**

`Node.js` `TypeScript`
`Express` `PostgreSQL` `Redis`

</td>
<td width="25%" align="center">

**◈ Frontend**

`Next.js 14` `React 18`
`TailwindCSS` `Recharts`

</td>
<td width="25%" align="center">

**☁ Infrastructure**

`Docker` `AWS`
`GitHub Actions` `Sentry` `Datadog`

</td>
</tr>
</table>

<br/>

## ◈ Open Source Repositories

| Repository | Description | License |
|:-----------|:------------|:-------:|
| [`lunospay-core`](https://github.com/lunospay/lunospay-core) | Smart contracts & blockchain layer | `MIT` |
| [`lunospay-api`](https://github.com/lunospay/lunospay-api) | REST API & backend services | `MIT` |
| [`lunospay-sdk`](https://github.com/lunospay/lunospay-sdk) | Official JavaScript / TypeScript SDK | `MIT` |
| [`lunospay-dashboard`](https://github.com/lunospay/lunospay-dashboard) | Merchant analytics dashboard | `MIT` |

> **✦ Contributions welcome!** See [`CONTRIBUTING.md`](CONTRIBUTING.md) to get started.

<br/>

## ◈ FAQ

<details>
<summary><b>✦ How fast is a payment confirmation?</b></summary>
<br>
Typically 400–500ms end-to-end. Solana's block time is ~400ms, and LunosPay's infrastructure adds minimal overhead. You receive a webhook the moment the transaction is finalized on-chain.
</details>

<details>
<summary><b>✦ What happens if a transaction fails?</b></summary>
<br>
LunosPay automatically retries failed transactions. Funds held in PDAs are never lost — if the transaction doesn't complete, the smart contract returns funds to the sender automatically.
</details>

<details>
<summary><b>✦ Can I white-label LunosPay?</b></summary>
<br>
Yes. The Enterprise plan includes a full white-label solution — your brand, your domain, your customer experience. Contact <a href="mailto:sales@lunospay.dev">sales@lunospay.dev</a> for details.
</details>

<details>
<summary><b>✦ Do you support other blockchains?</b></summary>
<br>
Currently Solana only. Ethereum, Base, and other EVM chains are planned for 2026. Solana was chosen for its ~500ms confirmation time and sub-cent fees — essential for a payments product.
</details>

<details>
<summary><b>✦ Are there hidden fees?</b></summary>
<br>
None. The fee is a flat percentage per transaction. No setup fees, no monthly minimums on the Free plan, no surprises. Solana network fees (~$0.00025/tx) are negligible and absorbed within your plan.
</details>

<details>
<summary><b>✦ Is my data secure?</b></summary>
<br>
All webhooks are cryptographically signed (HMAC-SHA256). Smart contracts are audited by third-party firms with public reports. The core is open source — audit it yourself.
</details>

<details>
<summary><b>✦ Can I cancel anytime?</b></summary>
<br>
Yes. No long-term contracts. Cancel from your dashboard at any time with no penalties.
</details>

<br/>

<img src="https://capsule-render.vercel.app/api?type=rect&color=d4f542&height=3&section=header" width="100%"/>

<br/>

## ◈ Community

<div align="center">

[![Discord](https://img.shields.io/badge/Discord-Join_2000%2B_devs-d4f542?style=for-the-badge&labelColor=0d0d0d&logo=discord&logoColor=d4f542)](https://discord.gg/lunospay)
[![Twitter](https://img.shields.io/badge/Twitter-Follow_us-d4f542?style=for-the-badge&labelColor=0d0d0d&logo=twitter&logoColor=d4f542)](https://twitter.com/lunospaydev)
[![GitHub](https://img.shields.io/badge/GitHub-Star_us-d4f542?style=for-the-badge&labelColor=0d0d0d&logo=github&logoColor=d4f542)](https://github.com/lunospay)

**Join thousands of developers building the future of payments on Solana.**

</div>

<br/>

## ◈ Contact

| | Email |
|:--|:--|
| General Support | [support@lunospay.dev](mailto:support@lunospay.dev) |
| Sales & Partnerships | [sales@lunospay.dev](mailto:sales@lunospay.dev) |
| Security Disclosures | [security@lunospay.dev](mailto:security@lunospay.dev) |

**Links:** &nbsp;[lunospay.dev](https://lunospay.dev) &nbsp;·&nbsp; [app.lunospay.dev](https://app.lunospay.dev) &nbsp;·&nbsp; [docs.lunospay.dev](https://docs.lunospay.dev) &nbsp;·&nbsp; [status.lunospay.dev](https://status.lunospay.dev)

<br/>

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0d0d0d,50:1a1a1a,100:0d0d0d&height=140&section=footer&text=MIT%20%C2%A9%202025%20LunosPay%2C%20Inc.&fontSize=16&fontColor=d4f542&fontAlignY=65" width="100%"/>

</div>
