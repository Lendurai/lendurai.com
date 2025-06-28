# Lendurai.com

Public landing page for Lendurai - satellite navigation and radio independent missions for drones.

## Overview

This repository contains the public website for Lendurai, featuring:
- Company information and team details
- Careers section with job postings
- Contact information

## Technology Stack

- **Static Site**: HTML, CSS, JavaScript
- **Job Postings**: Jekyll with markdown templates
- **Hosting**: GitHub Pages with custom domain (lendurai.com)

## Job Postings Management

Job postings are managed using Jekyll with markdown files in the `_jobs/` directory. See [README-JEKYLL.md](README-JEKYLL.md) for detailed documentation on:
- Creating new job postings
- Template structure
- Conditional LinkedIn application display
- SEO optimization

## Development

### Local Development
```bash
# Install Jekyll (if not already installed)
gem install jekyll

# Serve locally
jekyll serve

# Visit http://localhost:4000
```

### Adding New Job Postings
1. Create a new markdown file in `_jobs/`
2. Use the job-posting template
3. Commit and push to GitHub
4. GitHub Pages will automatically build and deploy

## Deployment

The site is automatically deployed via GitHub Pages when changes are pushed to the main branch.

## Contact

For questions about the website or job postings, contact: careers@lendurai.com
