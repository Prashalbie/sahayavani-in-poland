# सह Sahayavani — Indians in Poland

**sahayavani.github.io** · Community-maintained guides for Indians living in Poland · Updated weekly

---

## What is this?

Sahayavani (सहायवाणी — "voice of help") is a free, ad-free, login-free website that gives Indians living in Poland accurate, community-verified answers to the questions every new arrival asks — visa, healthcare, transport, SIM cards, banking, festivals, and more.

No personal data is collected. No cookies. No ads. Ever.

---

## Topics covered

| Category | Topics |
|---|---|
| Essential | Legal & Visa, Healthcare, Banking, Trusted Profile, Driving Licence |
| Daily Life | SIM & Internet, Transport Tickets, Groceries |
| Community | Indian Festivals, Badminton, Summer Camps |

---

## File structure

```
sahayavani-in-poland/
├── index.html                  ← Homepage (search + all topics)
├── style.css                   ← All design — mobile responsive
├── pages/
│   ├── legal-visa.html         ← Full guide page (sample)
│   ├── healthcare.html         ← (add content)
│   ├── banking.html            ← (add content)
│   ├── trusted-profile.html    ← (add content)
│   ├── driving-licence.html    ← (add content)
│   ├── sim-internet.html       ← (add content)
│   ├── transport.html          ← (add content)
│   ├── groceries.html          ← (add content)
│   ├── indian-festivals.html   ← (add content)
│   ├── badminton.html          ← (add content)
│   └── summer-camps.html       ← (add content)
├── content/
│   └── (markdown source files for each topic — Claude edits these weekly)
├── prompts/
│   └── weekly-update-prompt.txt ← Paste this into Claude every Sunday
└── README.md
```

---

## How to publish to GitHub Pages (first time setup)

### Step 1 — Push the files to GitHub

```bash
# Clone the repo
git clone https://github.com/Prashalbie/sahayavani-in-poland.git
cd sahayavani-in-poland

# Copy all the files Claude generated into this folder, then:
git add .
git commit -m "Initial site launch"
git push origin main
```

### Step 2 — Enable GitHub Pages

1. Go to your repo on GitHub: `https://github.com/Prashalbie/sahayavani-in-poland`
2. Click **Settings** (top navigation)
3. Click **Pages** (left sidebar)
4. Under **Source**, select **Deploy from a branch**
5. Choose **main** branch, **/ (root)** folder
6. Click **Save**
7. Wait 1–2 minutes, then visit: `https://Prashalbie.github.io/sahayavani-in-poland`

> **Note:** If you want the URL to be `sahayavani.github.io` instead, rename the repository to `sahayavani.github.io` in Settings → General → Repository name.

---

## How to do the weekly content update

Every Sunday (set a phone reminder):

1. Export WhatsApp group archive as `.txt` file (see `prompts/weekly-update-prompt.txt` for instructions)
2. Open your **Sahayavani Claude Project** at claude.ai
3. Start a new conversation
4. Paste the prompt from `prompts/weekly-update-prompt.txt`
5. Attach the WhatsApp `.txt` file
6. Claude will give you a report + updated HTML sections
7. Copy each updated section and paste into the correct file
8. Save and push to GitHub:

```bash
git add .
git commit -m "Weekly update — $(date +%Y-%m-%d)"
git push origin main
```

Site rebuilds automatically in under 1 minute.

---

## How to add the Google Form suggestion button

1. Create your form at forms.google.com
2. Click **Send → Link icon** — copy the form URL
3. Open `index.html`, find this line:
   ```html
   <a href="#suggest" class="fab" id="fab-suggest"
   ```
4. Replace `#suggest` with your Google Form URL
5. Do the same in `pages/legal-visa.html` and every other page file
6. Push to GitHub

---

## How to add a custom domain (optional)

If you buy `sahayavani.pl` or `sahayavani.com`:

1. In your domain registrar, add a CNAME record:
   - Name: `www`
   - Value: `Prashalbie.github.io`
2. In GitHub repo Settings → Pages → Custom domain, enter `www.sahayavani.pl`
3. Tick **Enforce HTTPS**
4. Done — usually takes 10–30 minutes to go live

---

## Contributing

This is an open community project. To contribute:
- Submit a pull request with updated content
- Use the "Suggest update" button on the site
- Join the WhatsApp group (link in About section)

---

## Disclaimer

This site is maintained by the community. It is not affiliated with any Polish or Indian government body. Always verify critical information with official Polish government sources (gov.pl). Zero personal data is collected.

---

*सहायवाणी — Voice of help · Built with ❤️ by Indians in Poland*
