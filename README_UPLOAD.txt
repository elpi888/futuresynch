FutureSynch and My Team AI site files, 10 November 2026

Repo: github.com/elpi888/futuresynch (built on commit 16fa9e3). Put every file in the repo root, replacing the file of the same name. Nothing has been pushed.

UPLOAD IN THIS ORDER

Commit 1 (together, because the routes need the pages):
  vercel.json
  readiness-check.html   (new)
  agent-kit.html         (new)
  playbook-intake.html   (new)
  FutureSynch_Playbook_Intake_Questions.md   (new; the download on the intake page, must sit in the repo root)

Commit 2:
  property-playbook.html
  futuresynch-index.html
  myteamai.html
  myteamai-estate-agencies.html
  myteamai_workspace_v6.html
  terms.html
  privacy.html

THE THREE SERVICE PAGES (one page each)
  futuresynch.com/property-playbook   Playbook, 400. Playbook only now; points to the Agent Kit.
  futuresynch.com/agent-kit           Playbook + Agent Kit + CRM Build Pack, 950. New. Built from the kit's own files.
  futuresynch.com/readiness-check     Readiness Check, 1,500. Ladder now links to the Agent Kit page.

WHAT CHANGED SINCE THE 9 NOVEMBER DRAFTS
  playbook-intake.html (new): futuresynch.com/playbook-intake. Two ways to answer the 12 intake questions. Option 1: fill in the form on the page. Option 2: download FutureSynch_Playbook_Intake_Questions.md, give it to your own AI (for example Claude), then upload the .md answers file on the page. The browser reads the file and sends its text with the buyer's details, so no file upload service is needed. Question 12 (marketing updates) is always answered by the person on the page.
    HUBSPOT (built and published 10 Nov 2026, EU portal 148226118). The two form IDs are already in playbook-intake.html:
      Option 1  "Playbook intake - Option 1 typed answers"   1d51895a-0b87-4084-8292-908370d546c6   (answers typed on the page)
      Option 2  "Playbook intake - Option 2 answers file"    2dc222f1-a899-4103-bff1-46320a176e52   (answers file made by the buyer's AI)
      Both forms have the same 17 fields, one per question of the questions file:
        Q1 and Q2: First name*, Last name*, Job title, Email*, Phone number, Company name*, Website URL
        Q3 to Q11: "3. Areas covered" to "11. The one thing to fix first" (contact properties fs_q3_areas_covered to fs_q11_fix_first)
        Full copy: "Intake answers" (fs_intake_answers)        * = required
      Each form creates a contact from a new email address, records consent to store and process data, has an optional Marketing Information subscription tick-box, and emails synch@futuresynch.com on each submission. Lifecycle stage on submission is HubSpot's default (Lead). reCAPTCHA is off on purpose, because the page submits in the background.
      The page sends the processing consent. The marketing tick-box on the page (Q12) is recorded in the Intake answers text, not as a HubSpot subscription.
      If the page cannot reach HubSpot, it shows a "could not send" box and lets the buyer copy their answers by email, so nothing is lost.
      If you edit a form in HubSpot, keep the field set and names as they are, or the page's answers stop being saved.
    After go-live, make one real test submission and check the contact in the CRM. HubSpot answers 200 even when it discards a submission from an unregistered domain, so a 200 proves nothing.
    Stripe: change the after-payment redirects to https://futuresynch.com/playbook-intake?product=playbook&session_id={CHECKOUT_SESSION_ID} for the Playbook link and ...?product=agent-kit&session_id={CHECKOUT_SESSION_ID} for the Agent Kit link. Without ?product= the page asks which one they bought.
    The Strategic Growth Review application page (futuresynch-apply.html) is unchanged and still has only the form.
  agent-kit.html (new): what the agent does daily, the six kit files, what you need, what the agent does and never does, the dry run, the ladder, Stripe link for 950.
  property-playbook.html: the 950 option moved to its own page; this page now sells the Playbook only.
  futuresynch-index.html, readiness-check.html: ladder step 2 links to /agent-kit (it pointed to the Playbook page).
  myteamai-estate-agencies.html (new in this round): this is the page the emails link to. It still showed the old 3,500 and 12,000 builds, payment plan, equity swap, subscriptions 290 to 3,490 and the Notion AI Playbook block. Now: the three first steps with links, Deployment 12,000 over three months (50% at signing, 50% at go-live), Starter 290, Growth 490, Retainer 990, Scale 1,490. The case study no longer names Curtis or Holland Park. Footer names My Team AI Limited, company number and address.
  myteamai.html: pricing section now opens with the same three first steps as the estate-agencies page (Playbook, Agent Kit, Readiness Check, each linking to its own page), with a short pointer section after the case study. The nav logo goes to my-team-ai.co.uk and a second link goes to Future Synch; same on myteamai-estate-agencies.html.
  terms.html: "the Bundle" renamed "the Agent Kit".
  vercel.json: /readiness-check and /agent-kit added.
  Everything else is as in the 9 November drafts: home ladder, My Team AI pricing, Retainer naming on the Curtis page, terms rewrite.

BEFORE YOU UPLOAD
  1. terms.html: company number 14342723 and the registered office were filled from the Companies House record for OLESYA KOVALSKAYA LTD (checked 10 Nov 2026). Confirm the registered office is still current. Note: 14345724 is a different, dissolved company; 14342723 is the right number.
  2. Read terms.html once. It is a draft, not legal advice.
  3. The intake page is now in this set (see playbook-intake.html above). Its two HubSpot forms are built and published.
  4. The Stripe links are the ones from the handover: Playbook buy.stripe.com/5kQ6oH7zAfuh5Fj0x16EU0d, Agent Kit buy.stripe.com/00weVdcTUfuh0kZ6Vp6EU0g, Readiness Check buy.stripe.com/7sY00jdXY1Dr9VzfrV6EU0h.

AFTER THE UPLOAD, CHECK THESE 6 URLS LOAD
  futuresynch.com/property-playbook
  futuresynch.com/agent-kit
  futuresynch.com/readiness-check
  futuresynch.com/my-team-ai/real-estate   (the demo, unchanged)
  my-team-ai.co.uk/estate-agencies
  futuresynch.com/terms
  futuresynch.com/playbook-intake   (and download the questions file from it)
Only then send the email drafts.

DECISIONS STILL OPEN
  1. Curtis Sloane's written consent to be named. The Curtis page (myteamai_workspace_v6.html) still names him and shows applicant and KYC data. The estate-agencies page no longer names him; restore it only with his consent.
  2. The case-study numbers on the estate-agencies page (35 clients, 24 hours, 100% KYC) are the old claims, left as they were. Confirm they are accurate before the page is promoted.
  3. The #invest section (SEIS) on myteamai.html and myteamai-estate-agencies.html: a public investment offer needs a financial-promotion check.
  4. Home page "How to engage" still lists the Strategic Growth Review at 2,500 plus a diagnostic and a 490 tier that duplicate the ladder.
  5. Domain: the ladder links to my-team-ai.uk; the emails and My Team AI pages use my-team-ai.co.uk. Pick one.
  6. Add-on prices (Agent Kit 450, Build Pack 250, adoption session 500) are unconfirmed, so none appear on any page.

NOT TOUCHED
  real-estate-demo.html (the demo; it shows a fictional agency), privacy.html (cut off at the end like the old terms), kitsoft-pipeline.html, the blog pages.
  The My Team AI hosts have no Terms or Privacy route; the catch-all sends them to myteamai.html.
  The company numbers conflict: the My Team AI app repo says Future Synch Ltd 14342723; these pages use My Team AI Limited 17345724. Check which is right.

WHERE EVERY FORM STORES ITS DATA
All website forms send to HubSpot (portal 148226118) through the Forms API. Nothing is stored on the website or in GitHub.
  - Strategic Growth Review application (futuresynch-apply.html): HubSpot form 722af13d-... Already live. Submissions confirmed in the CRM.
  - Investor memo request (investor-memo.html): HubSpot form 1aef3242-... Already live. Submissions confirmed in the CRM.
  - Newsletter (blog.html): HubSpot form 71bcc6af-... HubSpot shows 2 submissions on the "Newsletter Signup" form.
  - Playbook intake (playbook-intake.html): NEW. Option 1 (typed answers) sends to HubSpot form "Playbook intake - Option 1 typed answers" and Option 2 (uploaded .md file) sends to "Playbook intake - Option 2 answers file". Each question lands in its own contact field (Q3 to Q11), with the full text also kept in "Intake answers". Option 2 splits the uploaded file by its "## N." headings, so keep the headings exactly as the questions file gives them.
  - Payments: Stripe holds card and payment records. The Stripe link is not a form.
  - The "could not send" box on the intake page copies answers to email. It is a fallback for a failed submission only.
  - privacy.html: the old text named Formspree, which no form uses. It now names HubSpot and the intake answers. Add a retention period for intake answers if you want one stated.
After upload, submit one test through each option on the live page and check the contact in HubSpot: the question fields and "Intake answers" should be filled. Delete the test contacts afterwards. HubSpot answers success even for submissions it later discards, so the CRM check is the real test.
