Objective

Analyze a suspicious email sample and identify phishing indicators using header analysis and email content inspection.

🧪 1. Email Sample Used

I used a sample phishing email received in Gmail titled:

“Urgent: Your PayPal Account Will Be Limited in 24 Hours!”

The email was intentionally crafted to look urgent and to trick the user into clicking malicious links.

🔍 2. Tools Used
Tool	Purpose
MXToolbox Email Header Analyzer	Checked SPF, DKIM, routing path, spoofing attempts
Gmail Original Message View	Extracted raw headers
Browser preview	Hovered links to detect mismatched URLs
🧩 3. Steps Followed
Step 1 — Extract Headers

In Gmail:

Open email

Click ⋮ (3 dots)

Click “Show Original”

Copy the raw header

Paste into MXToolbox analyzer

Step 2 — Check Sender Email

The email appears “from”:

Gayathri Iyynara 19 <gayathriyynara19@gmail.com>


A PayPal email should never come from a Gmail address → Phishing indicator ❌

Step 3 — Analyze Headers

MXToolbox revealed:

SPF: FAIL
DKIM: FAIL


❌ Email failed authentication
❌ Sender domain does not match the claim
❌ “From” name is spoofed
❌ Message-ID looks randomly generated

Step 4 — Check Subject & Body

Subject:

Urgent: Your PayPal Account Will Be Limited in 24 Hours!


Indicators:

Uses urgency (classic social-engineering)

Threatens account disablement

Pushes user to click quickly

Step 5 — Check Links

When hovering the link (without clicking):

Displayed link: looks like PayPal
Actual redirect link: suspicious non-PayPal domain

➡️ This is a major phishing sign.

Step 6 — Grammar / Formatting Check

Phishing email contained:

Grammar mistakes

Unprofessional spacing

Capitalization errors

Poor formatting

Legitimate PayPal emails are clean and professional.

🚨 4. Phishing Indicators Found
Indicator	Why It's Suspicious
Gmail sender pretending to be PayPal	PayPal uses @paypal.com only
SPF & DKIM Fail	Email failed authentication (spoofing)
Urgent subject line	Social engineering tactic
Suspicious redirect URL	Leads to phishing page
Grammar mistakes	Common in phishing
Random message-ID	Not used by real companies
Warning-style content	Designed to scare users
