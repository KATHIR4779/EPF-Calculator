# EPF Withdrawal & Maturity Register

A free, browser-based calculator that helps Indian salaried employees estimate:

1. **Net amount received on PF withdrawal**, after applying TDS rules (5-year service exemption, ₹50,000 threshold, PAN-linked vs non-PAN rates, Form 15G/15H eligibility).
2. **Projected PF maturity balance**, based on current corpus, monthly basic + DA, years remaining, and an assumed EPFO interest rate.

Live demo: `https://KATHIR4779.github.io/EPF-Calculator/`

## Why this exists

Most free EPF calculators online only estimate maturity value and ignore TDS rules on early withdrawal entirely — despite TDS being the part that actually confuses people when they resign before completing 5 years of service. This tool covers both cases in one place.

## Features

- Two-tab interface: Withdrawal + TDS, and Maturity Projection
- All calculations run entirely in the browser — no data is sent to any server
- No sign-up, no accounts, no tracking of entered financial figures
- Passbook/ledger visual style, with a stamped result for each calculation
- Mobile responsive
- Includes a `privacy.html` page for AdSense compliance

## Tech stack

- Single static HTML file (`index.html`) — no build step, no dependencies, no frameworks
- Vanilla JavaScript for all calculation logic
- Deployable directly via GitHub Pages

## Files

| File | Purpose |
|---|---|
| `index.html` | The calculator itself (HTML, CSS, JS all in one file) |
| `privacy.html` | Privacy policy page, required for AdSense approval |
| `README.md` | This file |

## Deployment (GitHub Pages)

1. Push `index.html` and `privacy.html` to the root of this repository.
2. Go to **Settings → Pages** in this repo.
3. Under "Build and deployment," set Source to **Deploy from a branch**, branch = `main`, folder = `/ (root)`.
4. Save. Your site will be live at `https://<your-username>.github.io/<your-repo>/` within a few minutes.

## Assumptions used in calculations

- **TDS on withdrawal**: 10% if PAN is linked and service is under 5 years; 20% if PAN is not linked; 0% if service is 5+ years, amount is under ₹50,000, or a valid Form 15G/15H is submitted.
- **Maturity projection**: assumes monthly compounding, a constant salary and interest rate throughout the projection period, employee contribution of 12% of basic+DA, and employer EPF-bound contribution approximated at 3.67% of basic+DA (i.e. employer's 12% minus the 8.33% routed to EPS, which is a simplification most accurate for salaries above the EPS wage ceiling).

⚠️ **These are estimates for general planning purposes only.** EPFO rules, interest rates, and TDS thresholds change periodically — verify current figures on the [official EPFO site](https://www.epfindia.gov.in/) before making financial decisions. This tool is not affiliated with EPFO or the Government of India, and does not constitute financial or tax advice.

## License

Free to use and modify for personal or commercial projects.
