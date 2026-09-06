# REBEL website — a step-by-step guide (no coding needed)

Hi! This guide takes you from the files on your computer to a live website,
using only your web browser and mouse. No command line, no "git", no coding.
Take it slowly, one numbered step at a time. You can't break anything.

You have **7 files** (keep them all together in one folder):

- `index.html` — the Home page
- `call-for-papers.html`
- `registration.html`
- `program.html`
- `practical-information.html`
- `contact.html`
- `style.css` — controls how everything looks (you rarely touch this)

There's one rule to remember: **keep all 7 files in the same folder, and
don't rename them.** The pages find each other by name.

---

## PART 1 — Look at it on your own computer first (2 minutes)

Before putting anything online, see it for yourself.

1. Find the folder with the 7 files.
2. Double-click **`index.html`**. It opens in your web browser.
3. Click the menu links (Home, Call for papers, etc.) — they all work,
   right there on your computer, offline.

That's the whole site. Nothing you do here is public yet.

---

## PART 2 — Put it online with GitHub (about 10 minutes)

You already have a GitHub account (the one behind `evalact.github.io`),
so we'll reuse it. We'll make a **new, separate repository** just for REBEL.
Your finished site will live at a web address like:

    https://evalact.github.io/rebel/

(If your username is not "evalact", it'll be *your-username*`.github.io/rebel/`.)

### Step 2a — Create the new repository

1. Go to **github.com** and sign in.
2. Top-right of the page, click the **`+`** icon, then **"New repository"**.
3. **Repository name:** type `rebel` (all lowercase, no spaces).
   → This word becomes part of your web address, so keep it short and simple.
4. Set it to **Public**. (This matters — free websites only work on Public
   repositories. "Public" only means the *files* are visible, which is normal
   for a website anyway.)
5. Leave everything else as-is and click the green **"Create repository"** button.

### Step 2b — Upload your 7 files

1. You're now on your new empty repository page. Look for a link that says
   **"uploading an existing file"** (it's in the text in the middle of the page).
   If you don't see it, click **"Add file"** (a button near the top-right of the
   file area) → **"Upload files"**.
2. Open your folder on your computer, **select all 7 files** at once
   (click the first, hold **Shift**, click the last), and **drag them** onto
   the GitHub upload area. Or use the "choose your files" link and pick all 7.
3. Wait until all 7 file names appear in the list.
4. Scroll down and click the green **"Commit changes"** button.
   ("Commit" just means "save".)

### Step 2c — Turn on the website

1. On your repository page, click the **"Settings"** tab (top of the page).
2. In the left-hand menu, click **"Pages"**
   (it's under the "Code and automation" heading).
3. Under **"Build and deployment"**, find **"Source"** and choose
   **"Deploy from a branch"** from the dropdown.
4. Just below, set the branch dropdown to **`main`**, and leave the folder as
   **`/ (root)`**.
5. Click **"Save"**.
6. **Wait about 1–2 minutes**, then refresh that same page. A box will appear at
   the top saying *"Your site is live at …"* with your web address. 🎉

Click the address to see your live site. Share that link with anyone.

> If the link shows a "404" error at first, don't panic — it can take a few
> minutes the very first time. Refresh after 2–3 minutes.

---

## PART 3 — Your editing checklist (fill in the blanks)

I wrote real content everywhere I could from your call document. A few things
only you know, so I left clearly-marked placeholders. On the site, these show up
as **yellow reminder boxes** and as *"to be announced"* text. Here's the list:

**Contact page** (`contact.html`)
- [ ] Real workshop email address (appears twice — see notes below)
- [ ] Organiser and co-organiser names + affiliations
- [ ] Only publish a co-organiser's email **with their permission**

**Registration page** (`registration.html`)
- [ ] The fees (or "free")
- [ ] The month registration opens
- [ ] The registration form link

**Call for papers** (`call-for-papers.html`)
- [ ] The real EasyAbs submission link (the "Go to the submission portal" button)

**Program page** (`program.html`)
- [ ] Real talk titles, speakers, and times (after acceptances go out)

**Practical information** (`practical-information.html`)
- [ ] Exact venue address
- [ ] A couple of hotel suggestions
- [ ] Confirm the travel times

You don't have to do all of these now. The placeholders read fine as
"coming soon" until you're ready.

---

## PART 4 — How to change text later (the easy way)

You can edit any page **directly on the GitHub website** — no downloading:

1. Go to your repository, click the file you want to change
   (e.g. `contact.html`).
2. Click the **pencil icon** (✏️, top-right of the file) to edit.
3. Change the words. Everything you'll want to change is **plain text between
   the tags**. For example, to change an email you'd find this line:

       <p>Email us at <a href="mailto:rebel-workshop@example.com">rebel-workshop@example.com</a>.</p>

   …and replace `rebel-workshop@example.com` in **both** places with your real
   address. (One is what people see; the other is what their email app uses.)

4. Green lines that start with `<!--` are **notes to you** and never show on the
   website. Many say things like `<!-- EDIT: ... -->` right where a change goes.
5. When done, scroll down, click **"Commit changes"**. Your live site updates
   within a minute or two.

**Safe rule:** only change the words *between* the `>` and `<` symbols, and text
*inside quotation marks* after `href=`. Don't delete the `<...>` tags themselves.
If you mess up, GitHub keeps every past version, so nothing is ever truly lost.

### Removing a yellow reminder box

Once a page is ready, delete its reminder box: in edit mode, find the block that
starts with `<div class="todo">` and delete everything down to its matching
`</div>`. (Or leave them — they're only reminders to you, but they *do* show on
the live site, so you'll want them gone eventually.)

---

## PART 5 — Optional niceties (skip unless you want them)

- **A cleaner web address.** `evalact.github.io/rebel/` works fine. If you'd
  prefer something like `rebel-workshop.info`, you can buy a domain (~€10–15/yr)
  and connect it in **Settings → Pages → "Custom domain"**. GitHub walks you
  through it and gives free HTTPS.
- **Adding a new page later.** Copy an existing `.html` file, rename it, change
  its content — then add a link to it inside the `<nav>` menu on **every** page
  (the menu is repeated at the top of each file, so update all 6).
- **A logo or images.** Upload the image file to the same repository, then ask
  me and I'll show you the one line to add.

---

## If something goes wrong

- **The whole site looks unstyled / plain black text on white.**
  `style.css` probably didn't upload, or got renamed. Re-upload it, spelled
  exactly `style.css`, in the same folder as the pages.
- **A menu link goes to a "404 not found" page.**
  A file name doesn't match the link. File names are case-sensitive on the web:
  `Call-for-papers.html` ≠ `call-for-papers.html`. Keep them all lowercase.
- **"Deploy from a branch" is greyed out.**
  Your repository is Private. Go to **Settings → General**, scroll to the bottom
  ("Danger Zone"), and change visibility to **Public**.
- **Stuck anywhere.** Tell me which step number and what you see on screen, and
  I'll get you unstuck.

That's it — you've got this. 💪
