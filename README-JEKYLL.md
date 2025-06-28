# Lendurai Careers - Jekyll Setup

This document explains the new Jekyll-based templating system for job postings.

## Overview

Job postings are now managed using Jekyll with markdown files and a consistent template. This provides:

- **Consistent structure** across all job pages
- **Easy content management** using markdown
- **Conditional LinkedIn application** display
- **Automatic SEO optimization**
- **Structured data** for search engines

## File Structure

```
lendurai.com/
├── _config.yml                    # Jekyll configuration
├── _layouts/
│   └── job-posting.html          # Template for job pages
├── _jobs/                        # Job posting markdown files
│   ├── software-engineer-simulation.md
│   ├── head-of-business-development.md
│   ├── head-of-strategic-affairs.md
│   ├── country-manager-ukraine.md
│   └── example-email-only.md
├── careers/                      # Generated HTML files (legacy)
└── styles/                       # CSS files
```

## Creating a New Job Posting

1. Create a new markdown file in the `_jobs/` directory
2. Use the following frontmatter structure:

```markdown
---
layout: job-posting
title: "Job Title"
location: "City, Country (Work Type)"
employment_type: "Full-time"
linkedin_url: "https://www.linkedin.com/jobs/view/..."  # Optional
date_posted: 2024-01-01
valid_through: 2024-12-31
---

## About the company and the role

Your job description content here...

## What you will be doing

- Responsibility 1
- Responsibility 2

## We are looking for

**Required skills:**
- Skill 1
- Skill 2

## What we offer

- Benefit 1
- Benefit 2
```

## Conditional LinkedIn Application

The template automatically handles LinkedIn application display:

- **With LinkedIn URL**: Both LinkedIn and email application options are shown
- **Without LinkedIn URL**: Only email application option is shown

To create an email-only job posting, simply omit the `linkedin_url` field from the frontmatter.

## Building the Site

To build the site with Jekyll:

```bash
# Install Jekyll (if not already installed)
gem install jekyll

# Build the site
jekyll build

# Serve locally for development
jekyll serve
```

## Frontmatter Fields

| Field | Required | Description |
|-------|----------|-------------|
| `layout` | Yes | Must be "job-posting" |
| `title` | Yes | Job title |
| `location` | Yes | Job location and work type |
| `employment_type` | Yes | Full-time, Part-time, Contract, etc. |
| `linkedin_url` | No | LinkedIn job posting URL |
| `date_posted` | Yes | When the job was posted (YYYY-MM-DD) |
| `valid_through` | Yes | When the job posting expires (YYYY-MM-DD) |

## SEO Features

Each job page automatically includes:

- Meta title and description
- Open Graph tags for social media
- Twitter Card tags
- Canonical URL
- JSON-LD structured data for search engines
- Proper heading hierarchy

## Migration from HTML

The existing HTML job pages in the `careers/` directory can be removed once the Jekyll system is fully implemented and tested.

## Benefits

1. **Consistency**: All job pages follow the same structure
2. **Maintainability**: Content is separated from presentation
3. **SEO**: Automatic optimization for search engines
4. **Flexibility**: Easy to add new fields or modify the template
5. **Conditional Display**: LinkedIn application only shows when URL is provided 