# AttendWise — Static Attendance Calculator

## Files
- `index.html`: complete responsive attendance calculator (HTML/CSS/JavaScript, no backend).
- `README.md`: setup, deployment, AdSense and security checklist.

## Run locally
Open `index.html` in a browser. For a local web server, run:
`python -m http.server 8000`
then visit `http://localhost:8000`.

## Free hosting options
1. **GitHub Pages**: create a public GitHub repository, upload `index.html`, then Settings → Pages → deploy from `main` / root. HTTPS is provided.
2. **Cloudflare Pages**: create a project, connect the Git repository, use no build command and root directory `/`. HTTPS is provided.
3. **Netlify**: import the repository or drag-and-drop the folder. HTTPS is provided.

This is a static website; no server, database, login, or paid hosting is required.

## Google AdSense
AdSense approval is not guaranteed and is separate from hosting.
1. Deploy the site first and use your own domain if possible.
2. Publish useful original content, About, Contact, and Privacy Policy pages; ensure navigation and mobile experience work.
3. Apply at Google AdSense and verify site ownership as instructed in the AdSense dashboard.
4. After approval, copy the exact publisher ID and ad-unit code from AdSense. Replace the ad placeholder in `index.html` with the official code. Do not guess IDs.
5. Add the official AdSense script only once in `<head>`, and place the exact ad unit code in the ad slot.
6. Publish `ads.txt` if AdSense asks; use the exact line provided by AdSense.
7. Never click your own ads, ask people to click, or use bots/paid traffic that violates AdSense policies.

## Security / privacy
- No backend or database; user inputs are calculated locally in the browser and are not sent to a server by this page.
- No passwords, personal data, analytics, or external API keys are used.
- HTTPS is recommended and automatically provided by the hosting platforms above.
- Keep third-party scripts minimal. The current Google Fonts link is optional; remove it for a fully self-contained page.
- Before publishing, test invalid input, mobile layout, links, and calculator results.
- Add a real Privacy Policy and Contact page before applying for AdSense. Do not copy a generic policy blindly; accurately describe any services you actually use.
- AdSense policies and approval requirements can change; follow the latest instructions shown in your account.

## Calculator assumptions
- Attendance percentage = attended / conducted × 100.
- If below target, the calculator shows how many consecutive classes must be attended without bunking to reach the target.
- If at/above target, it shows how many upcoming classes can be bunked while remaining at/above the target.
- Both estimates assume all future classes are counted equally.
- College-specific subject/lab rules may differ; this is an estimate, not an official record.
