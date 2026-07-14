# Payment Setup - Manual Steps Required

## Why this is blocked
Creating a Stripe account requires typing an email and password. Per security rules, agents cannot create accounts. This needs Eddy to complete manually.

## Steps to unblock (5 minutes)

### 1. Create Stripe Account
- Go to https://dashboard.stripe.com/register
- Sign up with an email
- Verify the email
- Complete the account activation (bank account for payouts)

### 2. Create a Payment Link
- In Stripe Dashboard, go to Payment Links -> Create
- Product name: "TailoredFit - AI Resume Tailoring"
- Description: "Tailor your resume for any job in 30 seconds. ATS-optimized, keyword-matched."
- Price: $7.00 (one-time)
- After payment -> Success URL: https://eddyscanlan.github.io/tailoredfit/?paid=1
- Save and copy the Payment Link URL (looks like https://buy.stripe.com/abc123)

### 3. Update the Website
Replace STRIPE_PAYMENT_LINK_URL in index.html with the actual Payment Link URL.
Then commit and push.

After these steps, the product is fully operational with Stripe payment integration.
