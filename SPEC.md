# AI Resume Tailor - Product Specification

## Product: AI Resume Tailor
**Tagline:** "Tailor your resume for any job in 30 seconds"

## Value Proposition
Job seekers paste their current resume + paste a job description. The AI rewrites their resume bullets to match the job description's keywords and requirements, optimized for ATS (Applicant Tracking Systems). Output: a tailored resume they can download.

## Pricing
$7 per use (pay-per-use, no subscription)
Matches roast buyer's stated willingness-to-pay ("I'd pay $7 today")

## Tech Stack
- Frontend: Single-page HTML/CSS/JS (no framework, minimal deps)
- Hosting: Vercel free tier (static site)
- LLM: Groq free API (Llama 3.3 70B)
- Payment: Gumroad (10% fee, no merchant account)
- No backend server needed (all client-side + Gumroad redirect)

## User Flow
1. Landing page: headline + CTA "Tailor My Resume - $7"
2. User clicks CTA -> Gumroad payment page
3. After payment, Gumroad redirects back with receipt params
4. User sees the tool page (gated by Gumroad receipt verification)
5. User pastes: (a) current resume text, (b) job description
6. User clicks "Generate Tailored Resume"
7. AI returns: rewritten resume with matched keywords, ATS-optimized
8. User can copy or download as .txt

## Architecture
```
[Gumroad CTA Button] -> [Gumroad Payment] -> [Redirect back with receipt_id]
       -> [Tool Page] -> [Groq API call] -> [Tailored Resume Output]
```

## Differentiation from Competitors
- **Speed**: 30 seconds vs 5-10 min signup flows on Rezi/Kickresume
- **Price**: $7 one-time vs $9-30/mo subscriptions
- **Simplicity**: No signup, no account, paste-and-go
- **Focus**: Tailoring for a specific job (not building from scratch)

## Budget
- Domain: Skip (use Vercel subdomain for free)
- Hosting: $0 (Vercel free tier)
- LLM: $0 (Groq free tier)
- Payment processing: $0 (Gumroad takes 10% of sales)
- Total upfront cost: $0

## Revenue Target
$10 (just need 2 sales at $7 = $14 gross, $12.60 net after Gumroad fees)

## Distribution Plan (Free Channels)
1. Product Hunt launch
2. Hacker News "Show HN" post
3. Reddit r/jobs, r/resumes (providing value first, not spamming)
4. Quora answers about resume tailoring
5. SEO: long-tail keywords "tailor resume for job description"

## Pseudonym Identity
- Brand name: "TailoredFit" (check availability)
- Author name: Use a pseudonym, not Eddy's real name

## Kill Switch Criteria
- 30 days without $10 revenue = KILL (generate learnings)
- $50 budget exceeded = KILL
- 7 days no activity = KILL
