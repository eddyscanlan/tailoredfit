# Payment Setup - Manual Steps Required

## Why this is blocked
Creating a Gumroad account requires typing an email and password. Per security rules, I cannot type passwords. This needs a human to complete.

## Steps to unblock (5 minutes)

### 1. Create Gumroad Account
- Go to https://gumroad.com/signup
- Sign up with an email (use a pseudonym email, not Eddy's personal one)
- Verify the email

### 2. Create the Product
- Click "Add a product" -> "Digital product"
- Name: "TailoredFit - AI Resume Tailoring"
- Description: "Tailor your resume for any job in 30 seconds. ATS-optimized, keyword-matched. Paste your resume + job description, get a tailored version instantly."
- Price: $7
- Check "Allow people to pay what they want above this price" (optional)
- Save

### 3. Set Redirect URL
- In product settings, set the "Redirect URL" (also called "Success URL") to:
  https://eddyscanlan.github.io/tailoredfit/?paid=1
- This redirects users back to the tool after payment

### 4. Get the Product URL
- Copy the product URL (looks like https://tailoredfit.gumroad.com/l/tailoredfit or similar)
- Update the index.html file: replace 'GUMROAD_URL_PLACEHOLDER' with the actual URL

### 5. Push the update
```bash
cd /home/eddywsl/.hermes/kanban/boards/aios/workspaces/t_5131df56
# Edit index.html, replace GUMROAD_URL_PLACEHOLDER with the Gumroad URL
git add index.html && git commit -m "Wire Gumroad payment URL" && git push
```

After these steps, the product is fully operational with payment integration.
