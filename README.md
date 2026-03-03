# Asha Media House

Official website and digital infrastructure of **Asha Media House**, a hyperlocal digital newsroom committed to responsible, verified journalism.

🌐 Live: [https://ashamedia.in](https://ashamedia.in)
🔎 Employee Verification: [https://ashamedia.in/verify](https://ashamedia.in/verify)

---

## About

Asha Media House is a digital-first media organization focused on:

* Civic and public-interest reporting
* Education and community journalism
* Hyperlocal news coverage
* Verified journalist credential system

This repository contains the public website, blog system, and employee verification portal.

---

## Tech Stack

* **Astro** — Static site framework
* **Tailwind CSS** — Styling
* **AstroPaper** — Base theme
* **Cloudflare Pages** — Deployment
* **Static JSON-based credential system** — Verification system

---

## Features

* SEO-optimized blog system
* Dark & light mode
* Hyperlocal newsroom architecture
* Static employee verification system
* QR-code based credential validation
* Fast edge deployment via Cloudflare

---

## Project Structure

```
src/
 ├─ pages/
 │   ├─ blog/
 │   └─ verify/
 │       ├─ index.astro        # Verification portal
 │       └─ [id].astro         # Individual employee pages
 ├─ data/
 │   └─ employees.json         # Credential data
 └─ layouts/
     └─ VerificationLayout.astro
```

---

## Local Development

Clone the repository:

```bash
git clone https://github.com/<your-username>/asha-media-house.git
cd asha-media-house
```

Install dependencies:

```bash
npm install
```

Run development server:

```bash
npm run dev
```

Site will run at:

```
http://localhost:4321
```

---

## Deployment

This project is deployed using **Cloudflare Pages**.

### Build Command

```
npm run build
```

### Output Directory

```
dist
```

Cloudflare automatically handles:

* Edge caching
* Global CDN
* HTTPS
* Performance optimization

---

## Employee Verification System

The verification system is fully static and generated at build time.

To add a new journalist:

1. Open:

```
src/data/employees.json
```

2. Add a new entry:

```json
{
  "id": "AMH-HQ-MG-003",
  "name": "Full Name",
  "designation": "Reporter",
  "unit": "Unit Name",
  "status": "Active",
  "validTill": "31 March 2027"
}
```

3. Commit and deploy.

The following pages are automatically generated:

```
/verify/AMH-HQ-MG-003
```

If a journalist leaves, change:

```
"status": "Inactive"
```

Do not delete verification entries to preserve QR history.

---

## Security Notes

* Do not commit environment variables
* Do not commit private API keys
* Verification system is intentionally static for integrity and reliability

---

## Editorial Disclaimer

Only individuals listed on the verification portal are authorized representatives of Asha Media House.

Asha Media House is committed to ethical, responsible, and community-centered journalism.

---

## License

All content © Asha Media House.
Code may be reused only with attribution unless otherwise stated.
