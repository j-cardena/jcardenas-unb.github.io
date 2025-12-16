# Academic Website (Hugo)

A fast, SEO-friendly academic website built with Hugo. All content is managed through simple YAML text files—edit, commit, and the site rebuilds automatically.

## Quick Start

### Step 1: Create GitHub Repository

1. Go to [github.com](https://github.com) → **New repository**
2. Name it `j-cardena.github.io` (use your username)
3. Make it **Public**
4. Click **Create repository**

### Step 2: Upload Files

Upload this entire folder to your repository:
- Drag and drop all files, or
- Use GitHub Desktop, or
- Use git command line

### Step 3: Enable GitHub Pages

1. Go to repository **Settings** → **Pages**
2. Under **Source**, select **GitHub Actions**
3. The site will build automatically

Your site will be live at `https://j-cardena.github.io` within a few minutes.

---

## File Structure

```
├── hugo.toml              # Site configuration (your info, links)
├── data/
│   ├── research.yaml      # Research focus areas
│   ├── projects.yaml      # Research projects  
│   ├── publications.yaml  # Selected publications
│   ├── team.yaml          # Team members
│   └── jobs.yaml          # Job postings
├── static/
│   ├── photo.jpg          # Your headshot (add this)
│   └── cv.pdf             # Your CV (add this)
├── content/
│   └── jobs/_index.md     # Jobs page
├── layouts/               # HTML templates
└── .github/workflows/     # Auto-build configuration
```

---

## Managing Content

Edit the YAML files in `data/`, commit your changes, and the site rebuilds automatically.

### Research Focus (`data/research.yaml`)

```yaml
- title: Renewable Integration
  description: Dynamic thermal rating and forecasting methods...
  active: true    # Set to false to hide
```

### Projects (`data/projects.yaml`)

```yaml
- title: Atlantic Digital Grid
  description: An $8.4M consortium...
  status: active  # active, completed, or hidden
  tag: hiring     # hiring (blue), active (green), new (green), or empty
  dates: "2020–2027"
  partners: Multi-institution Consortium
  funding: ACOA AIF Funded
```

### Publications (`data/publications.yaml`)

```yaml
- title: One-Node Method to Implement Smart Grid Functions
  authors: S.A. Saleh, E.C. McSporran, J.L. Cardenas Barrera...
  venue: IEEE Transactions on Industry Applications
  year: 2025
  doi: "10.1109/TIA.2025.1234567"  # Optional, makes title clickable
  show: true      # Set to false to hide
```

Your name is automatically bolded in author lists.

### Team (`data/team.yaml`)

```yaml
postdocs:
  - name: Tohid Rahimi
    topic: VPP Hierarchical Optimization

phd:
  - name: Faezeh Bashiri
    topic: Forecasting of Aggregated Embedded Energy Resources

msc_alumni:
  - name: Afnan Rudabe Rahman
    topic: Net-Load Variance Minimization
    position: SCADA Engineer, Nova Scotia Power  # For alumni
```

Categories: `postdocs`, `phd`, `msc`, `postdoc_alumni`, `phd_alumni`, `msc_alumni`

### Job Postings (`data/jobs.yaml`)

```yaml
- title: Postdoctoral Research Professional
  type: Postdoctoral Fellow
  project: Real-Time DTR Platform
  description: Lead the development...
  requirements: PhD in Power Systems...
  start_date: January 2026
  deadline: Open until filled
  funding: ResearchNB
  open: true      # Set to false to close posting
```

---

## Common Tasks

| Task | Action |
|------|--------|
| Add new publication | Add entry to `data/publications.yaml` |
| Close a job posting | Set `open: false` in `data/jobs.yaml` |
| Graduate a student | Move from `phd:` to `phd_alumni:`, add `position:` |
| Hide a research area | Set `active: false` in `data/research.yaml` |
| Update your info | Edit `hugo.toml` |

---

## Initial Setup Checklist

Before going live, update these in `hugo.toml`:

- [ ] `google_scholar` - Your Google Scholar ID
- [ ] `linkedin` - Your LinkedIn username
- [ ] `orcid` - Your ORCID iD

And add these files to `static/`:

- [ ] `photo.jpg` - Professional headshot (square, ~400×400px)
- [ ] `cv.pdf` - Your CV

---

## How It Works

1. You edit a YAML file and push to GitHub
2. GitHub Actions detects the change
3. Hugo rebuilds the entire site (takes ~30 seconds)
4. The new site is deployed to GitHub Pages

No JavaScript runs in visitors' browsers. The site is pure HTML/CSS, which means:
- Fast loading
- Works without JavaScript
- SEO-friendly (search engines see all content)
- Accessible

---

## Local Development (Optional)

If you want to preview changes before pushing:

1. [Install Hugo](https://gohugo.io/installation/)
2. Run `hugo server` in this folder
3. Open `http://localhost:1313`

Changes appear instantly as you edit files.

---

## Troubleshooting

**Site not updating?**
- Check the Actions tab in your repository for build errors
- Make sure the workflow file is in `.github/workflows/hugo.yaml`

**Build failing?**
- Check YAML syntax (indentation matters)
- Ensure quotes around titles with colons (e.g., `title: "Q-RPL: A Protocol"`)

**Photo not showing?**
- File must be named exactly `photo.jpg` in `static/` folder
- Case sensitive on some systems

---

## Need Help?

- Hugo documentation: https://gohugo.io/documentation/
- GitHub Pages: https://docs.github.com/en/pages
