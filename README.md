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
- **SEO**: Optimized meta tags, Open Graph, Twitter Cards, and structured data
- **Hosting**: GitHub Pages with custom domain (lendurai.com)

## Job Postings Management

Job postings are managed using Jekyll with markdown files in the `_jobs/` directory. Each job includes:

- **Compelling summaries** for main page display and SEO
- **Conditional LinkedIn application** display
- **Automatic SEO optimization** with structured data
- **Social media sharing** optimization

See [README-JEKYLL.md](README-JEKYLL.md) for detailed documentation on:
- Creating new job postings
- Template structure and frontmatter fields
- Summary field best practices
- SEO and social media optimization

## Key Features

### Job Summary System
- **Main page previews**: Compelling one-liners instead of truncated content
- **SEO optimization**: Summary used in meta descriptions and structured data
- **Social media ready**: Optimized for LinkedIn, Facebook, and Twitter sharing

### SEO Features
- **Meta tags**: Title, description, and keywords
- **Open Graph**: Facebook and LinkedIn sharing
- **Twitter Cards**: Twitter sharing optimization
- **Structured data**: JSON-LD for search engines
- **Canonical URLs**: Prevent duplicate content issues

### Conditional Features
- **LinkedIn integration**: Application option only shows when URL is provided
- **Email fallback**: Always available for candidates without LinkedIn

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
2. Use the job-posting template with required frontmatter
3. Include a compelling summary for main page and SEO
4. Commit and push to GitHub
5. GitHub Pages will automatically build and deploy

### Required Frontmatter Fields
```markdown
---
layout: job-posting
title: "Job Title"
summary: "Compelling description for main page and SEO"
location: "City, Country (Work Type)"
employment_type: "Full-time"
linkedin_url: "https://www.linkedin.com/jobs/view/..."  # Optional
date_posted: 2024-01-01
valid_through: 2024-12-31
---
```

## Deployment

The site is automatically deployed via GitHub Pages when changes are pushed to the main branch.

## Contact

For questions about the website or job postings, contact: careers@lendurai.com
