# babyFIRE - Retirement Calculator

> **Solving retirement on Day 1**

## Overview

babyFIRE is a single-page investment calculator that determines the one-time, birth-year deposit needed to fully fund a retirement at age 50. The calculator accounts for inflation and uses the inverse 4% Safe Withdrawal Rate (SWR) to calculate your "FIRE Number" — the exact amount you need to invest today to achieve your retirement goals.

## The Philosophy

This calculator is designed for families and individuals who want to take a proactive approach to financial security. Rather than delaying retirement planning until adulthood, babyFIRE makes it possible to lock in retirement funding from day one. By understanding the power of compound growth over 50 years, you can see how small investments early in life compound into substantial retirement security.

## How It Works

### The Math

babyFIRE executes two primary calculation phases:

**Phase A: The Goal (Future Value)**
```
Target Nest Egg = Desired Annual Income ÷ SWR

Example: $150,000 ÷ 0.04 = $3,750,000
```

This determines how much you need invested to sustain your desired annual income in retirement.

**Phase B: The Deposit (Present Value)**
```
Effective Rate = Investment Return − Inflation Rate

Lump Sum Needed = Target Nest Egg ÷ (1 + Effective Rate)^Years to Retirement

Example: $3,750,000 ÷ (1.07)^50 ≈ $127,303
```

This calculates how much you need to deposit today (in today's dollars) to reach your target nest egg.

### Key Concepts

- **Safe Withdrawal Rate (SWR):** The percentage of your portfolio you can safely withdraw annually without running out of money. The traditional benchmark is 4%.
- **Real Rate of Return:** Investment return minus inflation. This is the "true" growth of your money adjusted for purchasing power.
- **Inflation-Adjusted Results:** All output values are presented in "Today's Dollars" to maintain purchasing power relevance.

## Features

✨ **Interactive Sliders** — Instantly adjust all assumptions and see results update in real-time

📊 **Portfolio Growth Chart** — Visual representation of your projected portfolio growth from today through retirement

💰 **Clear Metrics** — At-a-glance display of target nest egg, real rate of return, and years to retirement

📝 **Natural Language Summary** — Human-readable explanation of your required deposit

🎨 **Modern Dashboard UI** — Clean, professional financial dashboard aesthetic with high-contrast typography

## Default Assumptions

- **Current Age:** 0
- **Retirement Age:** 50
- **Goal Annual Income:** $150,000 (in today's dollars)
- **Safe Withdrawal Rate:** 4%
- **Expected Annual Investment Return:** 10%
- **Expected Annual Inflation Rate:** 3%

These defaults result in a required deposit of approximately **$127,303**.

## Usage

1. Adjust your desired annual retirement income
2. Set your expected investment return and inflation assumptions
3. Customize your target retirement age and current age
4. Instantly see your required deposit and projected portfolio growth

All calculations update dynamically as you adjust the sliders.

## Important Disclaimers

⚠️ **This calculator provides estimates based on historical average market returns and inflation rates.** Your actual results may vary significantly.

- Past performance does not guarantee future results
- A 50-year projection involves substantial uncertainty
- Market returns are unpredictable and can be highly volatile
- Inflation rates fluctuate based on economic conditions
- This tool is for educational purposes only
- **This is not professional financial advice** — Always consult with a qualified financial advisor before making investment decisions

## The 4% Rule

The 4% Safe Withdrawal Rate is based on the Trinity Study, which found that withdrawing 4% annually from a diversified portfolio had a 95% historical success rate of lasting 30+ years. However, this is a historical benchmark and not a guarantee. Your individual circumstances may warrant a different withdrawal rate.

## Deployment

babyFIRE is designed to be deployed on **Cloudflare Pages** for global distribution, fast load times, and zero-config HTTPS.

### Deploy to Cloudflare Pages

1. Push this repository to GitHub
2. Connect the repository to Cloudflare Pages
3. Set the build command to `(none)` (this is a static site)
4. Set the publish directory to `/`
5. Deploy!

The `_redirects` file ensures proper Single Page Application (SPA) routing.

### Local Development

Simply open `index.html` in your browser or serve with any static HTTP server:

```bash
# Using Python
python -m http.server 8000

# Using Node.js (http-server)
npx http-server

# Using Ruby
ruby -run -ehttpd . -p8000
```

## Technology Stack

- **HTML5** — Semantic markup
- **CSS3** — Modern styling with CSS Grid and Flexbox
- **Vanilla JavaScript** — No dependencies for core calculations
- **Chart.js** — Beautiful, responsive charts via CDN

## File Structure

```
.
├── index.html          # Complete SPA with embedded CSS and JavaScript
├── _redirects          # Cloudflare Pages SPA routing configuration
├── wrangler.jsonc      # Cloudflare Pages project configuration
└── README.md           # This file
```

## Contributing

Suggestions for improvements? Found a calculation error? Please open an issue or submit a pull request.

## License

This project is open source. Use it, modify it, and share it freely.

---

**Remember:** Your future self will thank you for starting early. The power of compound growth means that every dollar invested today has 50 years to grow. Time is your greatest investment asset.
