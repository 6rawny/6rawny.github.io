# 📊 Adeyemo Jamiu Adewale — Portfolio Website

> A professional data analytics, business intelligence, and finance portfolio website built with pure HTML, CSS, and JavaScript. Deployed via GitHub Pages. Zero frameworks. Zero dependencies.

---

## 🔗 Live Site

```
https://YOUR_USERNAME.github.io/YOUR_REPO/
```

> Replace `YOUR_USERNAME` and `YOUR_REPO` with your actual GitHub username and repository name after deployment.

---

## 📁 Recommended Folder Structure

Set up your repository exactly like this before you start updating anything:

```
your-repo/
│
├── index.html                          ← The main website file (do not rename)
├── README.md                           ← This file
│
└── assets/
    ├── images/
    │   ├── profile.jpg                 ← Your profile photo
    │   └── projects/
    │       ├── project-01.png          ← Project 1 screenshot
    │       ├── project-02.png          ← Project 2 screenshot
    │       ├── project-03.png          ← Project 3 screenshot
    │       └── ...                     ← Add more as needed
    │
    └── icons/
        ├── powerbi.png                 ← Power BI icon
        ├── excel.png                   ← Excel icon
        ├── mysql.png                   ← MySQL icon
        ├── looker.png                  ← Looker Studio icon
        ├── xero.png                    ← Xero icon
        ├── figma.png                   ← Figma icon
        ├── drawio.png                  ← Draw.io icon
        ├── powerpoint.png              ← PowerPoint icon
        ├── gsheets.png                 ← Google Sheets icon
        ├── access.png                  ← MS Access icon
        └── zebrabi.png                 ← Zebra BI icon
```

> **Tip:** You can download official tool icons from [SVG Repo](https://www.svgrepo.com) or [Simple Icons](https://simpleicons.org). Save them as `.png` files (recommended size: **64×64px** or **128×128px**).

---

## 🚀 Step 1 — Deploy to GitHub Pages (First-Time Setup)

Follow these steps once to get your site live on the internet.

### 1.1 — Create a GitHub Repository

1. Go to [github.com](https://github.com) and sign in
2. Click the **"+"** button (top right) → **"New repository"**
3. Name it anything, e.g. `portfolio` or `jamiu-portfolio`
4. Set visibility to **Public**
5. Click **"Create repository"**

### 1.2 — Upload Your Files

1. Open your new repository on GitHub
2. Click **"Add file"** → **"Upload files"**
3. Drag and drop `index.html` and `README.md`
4. Scroll down, write a commit message like `Initial upload`
5. Click **"Commit changes"**

### 1.3 — Create the Assets Folder Structure

GitHub doesn't allow uploading empty folders, so you need to upload at least one file into each folder:

1. Click **"Add file"** → **"Create new file"**
2. In the filename box, type: `assets/images/projects/.gitkeep`
3. Click **"Commit new file"**
4. Repeat the above for: `assets/icons/.gitkeep`

This creates the folder structure ready for your images.

### 1.4 — Enable GitHub Pages

1. In your repository, click **"Settings"** (top menu)
2. Scroll down to **"Pages"** in the left sidebar
3. Under **"Source"**, select **"Deploy from a branch"**
4. Under **"Branch"**, select `main` and folder `/ (root)`
5. Click **"Save"**
6. Wait 1–2 minutes, then your site is live at:
   ```
   https://YOUR_USERNAME.github.io/YOUR_REPO/
   ```

---

## ✏️ Step 2 — Set Your GitHub Base URL (Do This Once)

Open `index.html` in any text editor (Notepad, VS Code, etc.).

Find this line near the top of the `<script>` section:

```javascript
const GITHUB = "https://raw.githubusercontent.com/YOUR_USERNAME/YOUR_REPO/main/assets";
```

Replace `YOUR_USERNAME` with your GitHub username and `YOUR_REPO` with your repository name.

**Example:**
```javascript
const GITHUB = "https://raw.githubusercontent.com/jamiuadeyemo/portfolio/main/assets";
```

> ⚠️ Do this **once**. Every image, icon, and photo on the site uses this path automatically. You never need to change it again.

After editing, save the file and re-upload it to GitHub (see [Step 6 — Saving & Uploading Changes](#-step-6--saving--uploading-changes)).

---

## 👤 Step 3 — Update Your Profile

### 3.1 — Add Your Profile Photo

1. Take or choose a professional photo of yourself
2. Rename the file to `profile.jpg`
3. Go to your GitHub repository
4. Navigate to `assets/images/`
5. Click **"Add file"** → **"Upload files"**
6. Upload your `profile.jpg`
7. Commit the changes

Your photo will now appear automatically on the website. If the photo fails to load for any reason, the site gracefully falls back to showing the **"AJA"** initials badge.

> **Photo tips:**
> - Recommended size: **400×400px** minimum, square crop
> - File formats supported: `.jpg`, `.jpeg`, `.png`, `.webp`
> - Keep file size under **500KB** for fast loading

### 3.2 — Edit Your Personal Details

Open `index.html` and find the `PROFILE` section:

```javascript
const PROFILE = {
  name:     "Adeyemo Jamiu Adewale",     // ✏️ Your full name
  role:     "Accountant & Data Analyst", // ✏️ Your job title
  location: "Lagos, Nigeria",            // ✏️ Your city and country
  initials: "AJA",                       // ✏️ Your initials (shown if photo fails)

  profilePhoto: `${GITHUB}/images/profile.jpg`, // ✏️ Change filename if different

  email:    "adeyemojamiu30@gmail.com",  // ✏️ Your email address
  phone:    "+234 706 082 1273",         // ✏️ Your phone number
  linkedin: "https://www.linkedin.com/in/adeyemo-jamiu-210605251", // ✏️ Your LinkedIn URL

  pills: ["Accountant", "BI Analyst", "Data Strategist", "ACA (In View)"], // ✏️ Your skill badges
```

Edit any value between the quotation marks `" "` and save.

### 3.3 — Edit Your Bio Text

In the same `PROFILE` section, find the `bio` array:

```javascript
bio: [
  `First paragraph text here...`,   // ✏️ Edit paragraph 1
  `Second paragraph text here...`,  // ✏️ Edit paragraph 2
  `Third paragraph text here...`,   // ✏️ Edit paragraph 3
],
```

- Each item between the backticks `` ` ` `` is one paragraph
- You can use `<strong>text</strong>` to **bold** words inside a paragraph
- Add a fourth paragraph by adding a comma after the last one and writing: `` `Your new paragraph here`, ``
- Delete a paragraph by removing the entire line including its backticks and comma

---

## 🎓 Step 4 — Update Certifications

Find the `CERTS` array:

```javascript
const CERTS = [
  { icon: "🎓", name: "ICAN Professional",           body: "In View" },
  { icon: "📊", name: "Power BI Advanced",            body: "Certified" },
  // ... more certs
];
```

- **`icon`** — An emoji to display next to the cert name
- **`name`** — The name of the certification
- **`body`** — A short status like `"Certified"`, `"In View"`, `"2024"`, etc.

**To add a new certification:**
```javascript
{ icon: "📋", name: "Your New Certification", body: "Year or Status" },
```

**To remove a certification:** Delete the entire line including the `{...},`

---

## 💼 Step 5 — Update Work Experience

Find the `EXPERIENCE` array. Each job looks like this:

```javascript
{
  role:    "Finance Officer",                       // ✏️ Job title
  company: "GTI Capital Limited — Abuja, Nigeria", // ✏️ Company name and location
  period:  "June 2025 – Present",                  // ✏️ Employment dates
  current: true,                                   // ✏️ true = shows blue "Current" badge
  desc:    "Brief description of the role...",     // ✏️ One or two sentences about the role
  bullets: [
    "Bullet point one",                            // ✏️ Key responsibility or achievement
    "Bullet point two",
    // add more lines as needed
  ],
},
```

**To add a new job:** Copy the entire block from `{` to `},` and paste it above the others (most recent job should be first).

**To mark a job as current:** Set `current: true`. Set all other jobs to `current: false`.

**To remove a job:** Delete the entire block from `{` to `},`.

---

## 📊 Step 6 — Update Skills

Find the `SKILLS` object. It has two groups — `left` (Finance) and `right` (Data & BI):

```javascript
{ name: "Financial Reporting & Analysis", pct: 95 },
```

- **`name`** — The skill name displayed on the page
- **`pct`** — A number from 0 to 100 representing proficiency percentage

**To add a skill:** Add a new line: `{ name: "Your Skill", pct: 88 },`

**To remove a skill:** Delete the entire line.

**To move a skill to the other column:** Cut the line from one group's `items` array and paste it into the other.

---

## 🛠️ Step 7 — Update Technology Stack Icons

Find the `TOOLS` array. Each tool looks like this:

```javascript
{ name: "Power BI", icon: `${GITHUB}/icons/powerbi.png`, emoji: "📊" },
```

- **`name`** — The tool name displayed on the chip
- **`icon`** — Path to an image file in your `assets/icons/` folder. **Leave `""` to use emoji instead.**
- **`emoji`** — Fallback shown if the icon image is missing or fails to load

### Adding a Real Icon Image

1. Download the tool's logo as a `.png` file (64×64px recommended)
2. Upload it to `assets/icons/` in your GitHub repository
3. Update the `icon` field to match the filename:

```javascript
{ name: "Tableau", icon: `${GITHUB}/icons/tableau.png`, emoji: "📉" },
```

### Using Emoji Only (No Image)

```javascript
{ name: "Notion", icon: "", emoji: "📝" },
```

### Adding a New Tool

Add a new line inside the `TOOLS` array:
```javascript
{ name: "Your Tool Name", icon: `${GITHUB}/icons/yourtool.png`, emoji: "🔧" },
```

### Removing a Tool

Delete the entire line for that tool.

---

## 🗂️ Step 8 — Update Projects

Find the `PROJECTS` array. Each project looks like this:

```javascript
{
  featured: true,   // ✏️ true = wide card (spans 2 columns). false = normal size
  cat:      "Power BI · Financial Analytics",         // ✏️ Category label shown above title
  title:    "Actual vs Budget Executive Dashboard",   // ✏️ Project title
  desc:     "Description of what this project does.", // ✏️ 2–3 sentences
  tags:     ["Power BI", "DAX", "Variance Analysis"], // ✏️ Technology tags shown at the bottom
  image:    `${GITHUB}/images/projects/project-01-budget-dashboard.png`, // ✏️ Screenshot path
  emoji:    "📊",   // ✏️ Fallback shown if image is missing
  link:     "",     // ✏️ URL to the live project (Power BI link, GitHub, etc.)
  gradBg:   "linear-gradient(135deg,#EBF4FF 0%,#DBEAFE 100%)", // ✏️ Background colour behind image
},
```

### 8.1 — Add a Project Screenshot

1. Take a screenshot of your dashboard or report
2. Rename it clearly, e.g. `project-10-new-dashboard.png`
3. Upload it to `assets/images/projects/` in your GitHub repository
4. Update the `image` field to match:

```javascript
image: `${GITHUB}/images/projects/project-10-new-dashboard.png`,
```

If you leave `image: ""`, the site shows the emoji as a placeholder instead — perfectly fine while you prepare the screenshot.

### 8.2 — Add a Project Link

Paste the URL to your published Power BI report, GitHub repository, or any live link into the `link` field:

```javascript
link: "https://app.powerbi.com/view?r=YOUR_REPORT_ID_HERE",
```

When `link` is set, hovering over the project card shows a **"View Project ↗"** button, and a small link badge appears below the tags.

Leave `link: ""` to hide the button entirely.

### 8.3 — Add a Brand New Project

Scroll to the bottom of the `PROJECTS` array and find the commented template:

```javascript
/* ── NEW PROJECT TEMPLATE — copy & paste to add more ────────
{
  featured: false,
  cat:      "Your Category",
  title:    "Your Project Title",
  desc:     "Short description of what this project does and what insight it delivers.",
  tags:     ["Tag 1", "Tag 2"],
  image:    `${GITHUB}/images/projects/project-10-new.png`,
  emoji:    "📌",
  link:     "https://your-project-link.com",
  gradBg:   "linear-gradient(135deg,#F5F3FF 0%,#EDE9FE 100%)",
},
──────────────────────────────────────────────────────────── */
```

1. Copy everything between `{` and `},` (not the comment lines)
2. Paste it **above** the `/* ── NEW PROJECT TEMPLATE` comment line
3. Fill in all the fields
4. Make sure the pasted block ends with `},`

### 8.4 — Remove a Project

Delete the entire block for that project, from `{` to `},`.

### 8.5 — Change Card Size

- `featured: true` → wide card spanning 2 columns (best for your most impressive projects)
- `featured: false` → normal single-column card
- Only 1–2 featured cards per section looks best visually

### 8.6 — Change Card Background Colour

The `gradBg` field controls the gradient colour behind the project image. Use any of these presets or write your own:

| Colour | Value |
|--------|-------|
| Blue   | `"linear-gradient(135deg,#EBF4FF 0%,#DBEAFE 100%)"` |
| Green  | `"linear-gradient(135deg,#ECFDF5 0%,#D1FAE5 100%)"` |
| Purple | `"linear-gradient(135deg,#F5F3FF 0%,#EDE9FE 100%)"` |
| Amber  | `"linear-gradient(135deg,#FFFBEB 0%,#FEF3C7 100%)"` |
| Rose   | `"linear-gradient(135deg,#FFF1F2 0%,#FFE4E6 100%)"` |
| Teal   | `"linear-gradient(135deg,#F0FDFA 0%,#CCFBF1 100%)"` |

---

## 📈 Step 9 — Update Highlights Band

The dark band between Experience and Skills shows four headline numbers. Find the `HIGHLIGHTS` array:

```javascript
const HIGHLIGHTS = [
  { num: "₦118", suffix: "M",    label: "Expenditure tracked at GTI Capital" },
  { num: "₦41",  suffix: ".67T", label: "FAAC fund disbursement analysed" },
  { num: "₦662", suffix: "M",    label: "Baker Homes sales visualised" },
  { num: "8",    suffix: "+",    label: "Months of backlog records cleared" },
];
```

- **`num`** — The main large number (styled white)
- **`suffix`** — The unit or modifier (styled blue), e.g. `"M"`, `"+"`, `"%"`, `"K"`
- **`label`** — The small description below the number

Edit any of the four entries or replace them with your own milestone numbers.

---

## 💾 Step 10 — Saving & Uploading Changes

Every time you edit `index.html`, follow these steps to publish your changes:

### If editing directly on GitHub (easiest):

1. Open your repository on GitHub
2. Click on `index.html` to open it
3. Click the **pencil icon** (✏️) in the top-right corner to edit
4. Make your changes
5. Scroll down to **"Commit changes"**
6. Write a short message like `Update bio text` or `Add project 10`
7. Click **"Commit changes"**
8. Your live site updates within **1–2 minutes**

### If editing on your computer:

1. Edit `index.html` in VS Code, Notepad, or any text editor
2. Save the file
3. Go to your GitHub repository
4. Click **"Add file"** → **"Upload files"**
5. Drag and drop the updated `index.html`
6. Scroll down and click **"Commit changes"**
7. Your live site updates within **1–2 minutes**

> **Tip:** Use [VS Code](https://code.visualstudio.com/) for editing — it colour-codes JavaScript and helps you spot mistakes before uploading.

---

## 🖼️ Step 11 — Uploading Images and Icons

### Upload a profile photo:

1. In your repository, navigate to `assets/images/`
2. Click **"Add file"** → **"Upload files"**
3. Upload your `profile.jpg`
4. Commit the changes

### Upload a project screenshot:

1. Navigate to `assets/images/projects/`
2. Click **"Add file"** → **"Upload files"**
3. Upload your screenshot (e.g. `project-01.png`)
4. Commit the changes
5. Make sure the `image` field in `index.html` matches the exact filename

### Upload a tool icon:

1. Navigate to `assets/icons/`
2. Click **"Add file"** → **"Upload files"**
3. Upload your icon file (e.g. `powerbi.png`)
4. Commit the changes
5. Make sure the `icon` field in `index.html` matches the exact filename

> ⚠️ **Filenames are case-sensitive on GitHub.** If your file is `PowerBI.png` but your code says `powerbi.png`, the image will not load. Always use lowercase filenames.

---

## 🔧 Quick Reference — What to Edit for Common Tasks

| Task | Where to edit |
|------|--------------|
| Change your name or job title | `PROFILE.name`, `PROFILE.role` |
| Change your location | `PROFILE.location` |
| Add or change your photo | Upload to `assets/images/` → update `PROFILE.profilePhoto` |
| Update your bio | `PROFILE.bio` array |
| Add a certification | `CERTS` array |
| Add a new job | `EXPERIENCE` array |
| Change a skill percentage | `SKILLS.left.items` or `SKILLS.right.items` |
| Add a tool icon | Upload to `assets/icons/` → update `TOOLS` array |
| Add a project screenshot | Upload to `assets/images/projects/` → update `PROJECTS` array |
| Add a project link | `PROJECTS[n].link` field |
| Add a new project | Copy template at bottom of `PROJECTS` array |
| Update headline numbers | `HIGHLIGHTS` array |
| Change email / phone | `PROFILE.email`, `PROFILE.phone` |
| Update LinkedIn URL | `PROFILE.linkedin` |

---

## ❓ Troubleshooting

**My photo isn't showing.**
- Check that the filename in your code exactly matches the uploaded file (case-sensitive)
- Make sure the file is in `assets/images/` not somewhere else
- Confirm your `GITHUB` base URL is set correctly with your actual username and repo name
- The "AJA" initials badge will show as a fallback until the image loads correctly

**My project image isn't showing.**
- Confirm the file is uploaded to `assets/images/projects/`
- Check the filename in the `image` field matches exactly
- The emoji fallback will show until the image is available

**My tool icons aren't showing.**
- Confirm files are in `assets/icons/` with matching filenames
- If an icon isn't available yet, set `icon: ""` to use the emoji instead

**My changes aren't appearing on the live site.**
- GitHub Pages can take 1–3 minutes to update after a commit
- Try a hard refresh: `Ctrl + Shift + R` (Windows) or `Cmd + Shift + R` (Mac)
- Check that you committed to the `main` branch

**The site looks broken after my edit.**
- You likely have a missing comma `,` or an unclosed quote `"` somewhere
- Open your browser's developer tools (`F12`) → Console tab to see the error message
- Compare your edit carefully with the original format — every `{` needs a `}`, every `"` needs a closing `"`

---

## 📝 Notes

- All content is controlled from the `CONFIG` section at the top of `index.html` — you never need to touch the HTML structure below it
- The website supports **automatic dark mode** based on your visitor's OS settings
- The site is **fully responsive** — it works on desktop, tablet, and mobile
- No backend, no database, no hosting costs — GitHub Pages is completely free

---

*Built with HTML, CSS & JavaScript · Deployed on GitHub Pages*
