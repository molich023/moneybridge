# MoneyBridge — Complete Launch Guide
## From Zero to Live in 30 Minutes (Free)

---

## 🗂 FILES IN THIS PACKAGE
```
index.html      → Your full frontend website
server.js       → Node.js backend + M-Pesa Daraja integration
package.json    → Node.js dependencies
.env.example    → Environment variable template
LAUNCH_GUIDE.md → This file
```

---

## 🚀 STEP 1: Get Your M-Pesa Daraja Credentials

1. Go to → **https://developer.safaricom.co.ke**
2. Click "Sign Up" or "Log In"
3. Click **"Create New App"**
4. Name it: `MoneyBridge`
5. Check: ✅ Lipa Na M-Pesa (STK Push)
6. Copy your:
   - `Consumer Key`
   - `Consumer Secret`
   - `Passkey` (under Lipa Na M-Pesa Online)

> 🔑 Your M-Pesa number: **0704658022** will receive all payments.

---

## 🚀 STEP 2: Deploy FREE on Render.com

### 2a. Upload to GitHub
1. Go to **github.com** → New Repository
2. Name it: `moneybridge`
3. Upload all 5 files from this package
4. Click "Commit changes"

### 2b. Deploy on Render (FREE)
1. Go to **render.com** → Sign up free
2. Click **"New +"** → **"Web Service"**
3. Connect your GitHub repo: `moneybridge`
4. Settings:
   - **Build Command:** `npm install`
   - **Start Command:** `node server.js`
   - **Plan:** Free
5. Click **"Create Web Service"**
6. Wait ~3 minutes → You'll get a URL like:
   `https://moneybridge-xxxx.onrender.com`

### 2c. Set Environment Variables on Render
In Render dashboard → Your service → **"Environment"** tab:

| Key | Value |
|-----|-------|
| `NODE_ENV` | `production` |
| `MPESA_CONSUMER_KEY` | (your key from Safaricom) |
| `MPESA_CONSUMER_SECRET` | (your secret) |
| `MPESA_SHORTCODE` | `174379` (sandbox) or your real shortcode |
| `MPESA_PASSKEY` | (your passkey) |
| `MPESA_CALLBACK_URL` | `https://YOUR-APP.onrender.com/api/mpesa-callback` |
| `ALLOWED_ORIGIN` | `https://YOUR-APP.onrender.com` |

---

## 🚀 STEP 3: Test Your App

1. Visit your Render URL in any browser
2. Fill in the trial form
3. In **sandbox mode**, you can test STK push using Safaricom's test phone numbers
4. Check Render logs to see registration confirming

---

## 💳 Going Live (After Testing)

1. Go to **developer.safaricom.co.ke** → Production
2. Submit your app for approval (takes 1-3 days)
3. Update Render env vars with Production credentials
4. Change `MPESA_SHORTCODE` to your real till/paybill number

---

## 🔐 SECURITY COMPLIANCE SUMMARY

| Standard | How It's Implemented |
|----------|---------------------|
| **OWASP A01** | Broken Access Control → Route-level auth checks |
| **OWASP A02** | Crypto failures → TLS enforced, no plaintext secrets |
| **OWASP A03** | Injection → All inputs sanitized, parameterized SQL |
| **OWASP A05** | Security Misconfig → Helmet.js with strict CSP/HSTS |
| **OWASP A07** | Auth failures → Rate limiting on all endpoints |
| **OWASP A09** | Logging → Morgan logging, no sensitive data in logs |
| **GDPR** | Consent recorded, right to erasure endpoint exists |
| **HIPAA** | No health data stored, access controls on all data |

---

## 🌍 EXPANDING TO OTHER COUNTRIES

The app auto-detects country from the dropdown and shows:
- Local currency equivalent of KSH 100
- For non-M-Pesa countries: connect **Flutterwave** or **Stripe** later

To add Flutterwave (for rest of Africa, EUR, USD payments):
```
npm install flutterwave-node-v3
```
Then add a `/api/flutterwave-pay` route in server.js.

---

## 📊 YOUR LIVE ENDPOINTS

| Endpoint | Method | Purpose |
|----------|--------|---------|
| `/` | GET | Frontend website |
| `/api/register-trial` | POST | Register new user |
| `/api/pay` | POST | Initiate M-Pesa STK Push |
| `/api/mpesa-callback` | POST | Safaricom payment callback |
| `/api/check-trial/:email` | GET | Check trial status |
| `/api/user/:email` | DELETE | GDPR data deletion |
| `/api/stats` | GET | Public usage stats |

---

## 💡 REFERRAL SYSTEM

- Every registered user gets a referral code (their email)
- Each referral = KSH 20 credit stored in DB
- 5 referrals = next year free
- Display user's referrals in a dashboard (Phase 2)

---

## 📞 SUPPORT

M-Pesa Number: **0704658022**
Built with ❤️ for the world's underserved.
