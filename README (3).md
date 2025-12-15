# Personal Academic Website

A clean, professional academic website ready for deployment on GitHub Pages. The research team section is dynamically loaded from an Excel file for easy updates.

## Quick Deployment (10 minutes)

### Step 1: Create a GitHub Repository

1. Go to [github.com](https://github.com) and sign in (or create an account)
2. Click the **+** button → **New repository**
3. Name it exactly: `yourusername.github.io` (replace `yourusername` with your GitHub username)
   - Example: `jcardenas-unb.github.io`
4. Make it **Public**
5. Click **Create repository**

### Step 2: Upload the Website Files

1. On your new repository page, click **"uploading an existing file"**
2. Drag and drop ALL these files:
   - `index.html` (main website)
   - `jobs.html` (openings page)
   - `team.xlsx` (research team data)
   - `jobs.xlsx` (job postings data)
3. Click **Commit changes**

### Step 3: Enable GitHub Pages

1. Go to repository **Settings** → **Pages** (in the left sidebar)
2. Under "Source", select **Deploy from a branch**
3. Select **main** branch and **/ (root)** folder
4. Click **Save**

Your site will be live at `https://yourusername.github.io` within a few minutes!

---

## Managing Your Research Team

The team section automatically loads from `team.xlsx`. This makes it easy to keep your website current without editing HTML.

### Adding a New Team Member

1. Open `team.xlsx` in Excel
2. Go to the "Research Team" sheet
3. Add a new row with:
   - **Category**: Use exactly one of these:
     - `Postdoctoral Fellow`
     - `PhD Student`
     - `MSc Student`
   - **Name**: Full name
   - **Research Topic**: Their thesis/project title
   - **Status**: `Current`
   - **Current Position**: Leave blank for current members
4. Save the file
5. Upload the updated `team.xlsx` to your GitHub repository (it will replace the old one)

### When Someone Graduates

1. Open `team.xlsx`
2. Find their row and change:
   - **Category**: Change to `PhD Alumni`, `MSc Alumni`, or `Postdoc Alumni`
   - **Status**: Change to `Alumni`
   - **Current Position**: Add their new job (e.g., "Electrical Engineer, Hatch")
3. Save and upload to GitHub

### Category Options

| For Current Members | For Alumni |
|---------------------|------------|
| Postdoctoral Fellow | Postdoc Alumni |
| PhD Student | PhD Alumni |
| MSc Student | MSc Alumni |

The website automatically groups members by category and shows alumni separately with their current positions.

---

## Managing Job Postings

Job postings work the same way—edit `jobs.xlsx` and upload to GitHub.

### Posting a New Position

1. Open `jobs.xlsx` in Excel
2. Add a new row with:
   - **Status**: `Open`
   - **Position Type**: e.g., `Postdoctoral Fellow`, `PhD Student`, `MSc Student`
   - **Title**: Full position title
   - **Project**: Associated project name
   - **Description**: What they'll do (2-3 sentences)
   - **Requirements**: Key qualifications
   - **Start Date**: When the position begins
   - **Application Deadline**: Due date or "Open until filled"
   - **Funding Source**: e.g., "NSERC", "ResearchNB", "Atlantic Digital Grid"
3. Save and upload to GitHub

### Closing a Position (Filled or Cancelled)

1. Open `jobs.xlsx`
2. Find the position row
3. Change **Status** from `Open` to `Closed`
4. Save and upload to GitHub

The posting immediately disappears from the website, but you keep the record in your spreadsheet for reference.

### Deleting a Position Entirely

Simply delete the row from `jobs.xlsx` and upload.

### What Visitors See

- **Open positions**: Displayed with full details and "Apply Now" button
- **No open positions**: A friendly message explaining there are no current openings, plus information on how to inquire about future opportunities

---

## Before You Deploy: Customize These Items

### Required Changes

Open `index.html` in any text editor and update:

1. **Photo** (line ~280): Replace the placeholder with your actual photo
   ```html
   <!-- Change this: -->
   <div class="photo-placeholder">JC</div>
   
   <!-- To this: -->
   <img src="photo.jpg" alt="Julian Cardenas Barrera">
   ```
   Then upload `photo.jpg` alongside `index.html`

2. **Google Scholar link** (line ~288): Replace `YOUR_ID` with your actual Google Scholar ID
   - Your ID is in your Scholar URL: `scholar.google.com/citations?user=YOUR_ID`

3. **LinkedIn link** (line ~293): Replace `YOUR_LINKEDIN` with your LinkedIn username

4. **ORCID link** (line ~298): Replace `YOUR_ORCID` with your ORCID iD

5. **CV link** (line ~303): Upload your CV as `cv.pdf` and update the link:
   ```html
   <a href="cv.pdf" target="_blank">
   ```

### Optional Customizations

- **Office location**: Update Head Hall room number if different (line ~530)
- **Team members**: Add/remove team members as needed (starting line ~450)
- **Publications**: Add more recent publications or adjust the selection
- **Colors**: Modify the CSS variables at the top to match UNB branding if desired

---

## Adding Your Photo

For best results:
- Use a professional headshot
- Square aspect ratio (e.g., 400×400 pixels)
- Name the file `photo.jpg`
- Upload to the same repository as `index.html`

---

## Custom Domain (Optional)

If you want to use a custom domain like `juliancardenas.ca`:

1. Purchase a domain from any registrar (Namecheap, Google Domains, etc.)
2. In your repository, go to **Settings** → **Pages**
3. Enter your custom domain under "Custom domain"
4. At your domain registrar, add these DNS records:
   - A record: `185.199.108.153`
   - A record: `185.199.109.153`
   - A record: `185.199.110.153`
   - A record: `185.199.111.153`
   - CNAME: `www` → `yourusername.github.io`

---

## Updating Your Site

### To update team members:
Edit `team.xlsx` → Save → Upload to GitHub (replace existing file)

### To manage job postings:
Edit `jobs.xlsx` → Save → Upload to GitHub (replace existing file)

### To update other content:
Edit HTML files locally → Upload to GitHub (or edit directly on GitHub)

Changes go live within minutes.

---

## File Structure

```
your-repository/
├── index.html      # Main website
├── jobs.html       # Current openings page
├── team.xlsx       # Research team data (edit to update team)
├── jobs.xlsx       # Job postings (edit to manage openings)
├── photo.jpg       # Your headshot (upload separately)
├── cv.pdf          # Your CV (upload separately)
└── README.md       # This file (optional)
```

---

## Need Help?

- GitHub Pages documentation: https://docs.github.com/en/pages
- For UNB-specific IT questions, contact ECE IT support
