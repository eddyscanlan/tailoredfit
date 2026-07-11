# TailoredFit - Free ATS Resume Score Checker

> Check your resume's ATS compatibility score for free. Get keyword gap analysis and an AI-optimized resume. $7 one-time, no subscription.

**Live site:** https://eddyscanlan.github.io/tailoredfit/

## What It Does

TailoredFit is a free ATS (Applicant Tracking System) resume scanner. You paste your resume and a job description, and it shows you:

- **ATS Match Score** — what percentage of keywords from the job description are in your resume
- **Keyword Gap Analysis** — exactly which keywords are found and which are missing
- **AI-Optimized Resume** ($7 one-time) — your resume rewritten with all missing keywords naturally integrated, downloadable as PDF

## Why It Exists

75%+ of resumes are rejected by ATS software before a human ever sees them. Most ATS checkers charge $15-$30/month subscriptions. TailoredFit gives you the score check for free, and the AI optimization for a one-time $7.

## Tech Stack

| Component | Technology | Cost |
|-----------|-----------|------|
| Hosting | GitHub Pages | $0 |
| AI Backend | Pollinations.ai | $0 |
| PDF Generation | html2pdf.js (MIT) | $0 |
| Payments | Gumroad | $0/mo, 10% per transaction |
| Frontend | Vanilla HTML/CSS/JS | $0 |

No backend, no database, no build step. Resume data stays in the browser.

## How It Works

1. User pastes resume + job description
2. Client-side JS extracts keywords from the job description (frequency-based, stop-word filtered)
3. Calculates ATS match score (matched keywords / total keywords)
4. Shows keyword gap analysis (found vs missing)
5. If user wants AI optimization: redirects to Gumroad for $7 payment
6. After payment, localStorage restores the resume text and Pollinations.ai rewrites it
7. User gets optimized resume + PDF download

## Features

- **Free ATS Score Check** — no signup, no account, paste and check
- **Keyword Gap Analysis** — visual display of found/missing keywords
- **AI Resume Optimization** — $7 one-time, rewrites resume with missing keywords
- **PDF Download** — client-side PDF generation via html2pdf.js
- **Privacy-First** — resume data never touches our server, goes directly to AI API from browser
- **No Subscription** — pay once, use forever

## Running Locally

```bash
git clone https://github.com/eddyscanlan/tailoredfit.git
cd tailoredfit
# Open index.html in a browser, or serve with any static server
python3 -m http.server 8000
```

## License

MIT

## Links

- **Live site:** https://eddyscanlan.github.io/tailoredfit/
- **Blog:** https://eddyscanlan.github.io/tailoredfit/how-to-beat-ats.html
- **Buy AI optimization ($7):** https://eddyscanlan.gumroad.com/l/tailoredfit
