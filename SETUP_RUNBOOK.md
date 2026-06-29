# Bose FABLE Lab — Website Setup Runbook

This repository is a fully customized al-folio site, ready to publish at **boselab.io**.
Everything that could be automated has been done. The remaining steps require YOUR
account login and YOUR payment card, which is why they are yours to do, not mine.

---

## STEP 1 — Buy the domain  (your card, ~10 min)

Pick one registrar. Recommended for clean pricing + easy DNS:
- **Cloudflare** (registers at wholesale cost, free DNS, best pairing with GitHub Pages), or
- **Porkbun** / **Namecheap** (simplest one-click buy).
Avoid GoDaddy's upsell flow.

1. Go to the registrar and search **boselab.io**.
2. Add it to cart. Decline add-ons except WHOIS privacy (usually free; keep it ON).
3. Pay. (.com is typically ~$10–12/year.)
4. You now have access to that domain's DNS settings — you will use them in Step 4.

> I cannot complete a purchase or enter card details for you. This step is yours.

---

## STEP 2 — Put this site on GitHub  (your account, ~10 min)

1. Create a free GitHub account if you do not have one (github.com).
2. Create a new repository named exactly: **YOURUSERNAME.github.io**
   (replace YOURUSERNAME with your GitHub username; this naming makes it a user site).
   - Visibility: Public. Do NOT initialize with a README.
3. Upload this folder's contents to the repo. Two options:
   - **Web upload (no tools):** on the empty repo page, click "uploading an existing file",
     drag in everything from this folder, and commit to the `main` branch.
   - **Command line:**
     ```
     cd al-folio
     git init -b main
     git add .
     git commit -m "Initial Bose FABLE Lab site"
     git remote add origin https://github.com/YOURUSERNAME/YOURUSERNAME.github.io.git
     git push -u origin main
     ```

---

## STEP 3 — Turn on GitHub Pages  (your account, ~5 min)

1. In the repo: **Settings > Actions > General > Workflow permissions** →
   select **Read and write permissions** → Save.
2. **Settings > Pages > Build and deployment** → Source: **GitHub Actions**.
   (al-folio ships an Action that builds and deploys automatically on every push.)
3. Wait a few minutes. Your site will appear at `https://YOURUSERNAME.github.io`.
   Confirm it loads before doing Step 4.

---

## STEP 4 — Connect boselab.io  (your registrar + your repo, ~15 min + DNS wait)

**4a. Tell GitHub the custom domain first.**
- Repo **Settings > Pages > Custom domain** → type `boselab.io` → Save.
- Check **Enforce HTTPS** once it becomes available (may take an hour).

**4b. Add DNS records at your registrar** (the values below are current GitHub Pages targets):

Apex domain `boselab.io` — four **A records** (host `@`):
```
185.199.108.153
185.199.109.153
185.199.110.153
185.199.111.153
```
(Optional IPv6 — four **AAAA records**, host `@`):
```
2606:50c0:8000::153
2606:50c0:8001::153
2606:50c0:8002::153
2606:50c0:8003::153
```
`www` subdomain — one **CNAME record**:
```
host: www    value: YOURUSERNAME.github.io
```

If your registrar is Cloudflare: set the records the same way, and set the DNS records
to "DNS only" (grey cloud) rather than proxied while first issuing the certificate.

**4c. Wait for propagation** (minutes to ~24 hours). Then visit https://boselab.io.

---

## STEP 5 — Make it yours  (edit anytime; changes auto-deploy on push)

- **Headshot:** add a square photo as `assets/img/prof_pic.jpg` (delete the placeholder note there).
- **Publications:** open `_bibliography/papers.bib`. Export BibTeX from your Google
  Scholar or ORCID profile and paste it in. The first entry is a placeholder — VERIFY it.
- **Contact details:** fill the `TODO` lines in `_pages/contact.md`
  (TCH Fetal Center referral info, your professional email).
- **CDH guides:** five articles in `_pages/cdh-*.md` are stubbed with outlines.
  `_pages/cdh-what-is.md` is fully written as the model. Draft the rest (your
  voice-memo-to-draft workflow fits well — they are plain markdown).
- **Before launch:** run the parent-facing and referral content past Baylor/TCH
  communications and compliance, per the guardrails we discussed.

Every push to `main` rebuilds and redeploys the live site within a few minutes.
