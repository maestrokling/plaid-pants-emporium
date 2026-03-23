# Plaid Pants Emporium — Launch Checklist
_Domain transfer expected complete: ~March 26, 2026_

---

## Step 1: Confirm Transfer Complete
- [ ] Log into INWX — verify `plaidpantsemporium.com` shows in your account
- [ ] If not there by March 27, check GoDaddy for pending approval email

---

## Step 2: Set DNS at INWX for GitHub Pages

Add these records in INWX DNS manager for `plaidpantsemporium.com`:

**A records (GitHub Pages):**
```
@    A    185.199.108.153
@    A    185.199.109.153
@    A    185.199.110.153
@    A    185.199.111.153
```

**CNAME (www):**
```
www  CNAME  maestrokling.github.io.
```

**MX records (Proton Mail):**
```
@    MX   10   mail.protonmail.ch.
@    MX   20   mailsec.protonmail.ch.
```

**SPF record:**
```
@    TXT  "v=spf1 include:_spf.protonmail.ch ~all"
```

---

## Step 3: Add Custom Domain to GitHub Pages

Tell Hux "add the custom domain to the Plaid Pants repo" — one command, done in 30 seconds.

Or manually:
1. Go to https://github.com/maestrokling/plaid-pants-emporium/settings/pages
2. Under "Custom domain" → enter `plaidpantsemporium.com` → Save
3. Check "Enforce HTTPS" once it appears (may take a few minutes)

---

## Step 4: Set Up Proton Mail Email Address

1. Go to proton.me → Settings → All Settings → **Addresses**
2. Click **Add address** → **Custom domain**
3. Enter `plaidpantsemporium.com`
4. Proton will give you a **verification TXT record** — add it in INWX DNS
5. Click Verify in Proton
6. Add `hello@plaidpantsemporium.com` as the address
7. Mail lands in your regular Proton inbox as an alias

_(Hux can generate the exact TXT record once Proton shows it to you)_

---

## Step 5: Verify Everything Works

- [ ] https://plaidpantsemporium.com loads the site
- [ ] https://www.plaidpantsemporium.com loads the site
- [ ] HTTPS is active (padlock in browser)
- [ ] Send a test email to hello@plaidpantsemporium.com — arrives in Proton inbox
- [ ] The mailto link in the footer works

---

## What's Already Done
- ✅ Site built: `projects/plaid-pants-emporium/index.html`
- ✅ GitHub repo created: https://github.com/maestrokling/plaid-pants-emporium
- ✅ GitHub Pages enabled: https://maestrokling.github.io/plaid-pants-emporium/
- ✅ Domain transfer initiated from GoDaddy (March 22)
