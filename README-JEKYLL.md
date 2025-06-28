# Lendurai Careers - Jekyll Setup

This document explains the Jekyll-based templating system for job postings.

## Overview

Job postings are managed using Jekyll with markdown files and a consistent template. This provides:

- **Consistent structure** across all job pages
- **Easy content management** using markdown
- **Compelling job summaries** for main page and SEO
- **Conditional LinkedIn application** display
- **Automatic SEO optimization** with structured data
- **Social media sharing** optimization

## File Structure

```
lendurai.com/
├── _config.yml                    # Jekyll configuration with SEO settings
├── _layouts/
│   ├── default.html              # Default layout
│   └── job-posting.html          # Template for job pages
├── _jobs/                        # Job posting markdown files
│   ├── ai-drone-software-intern.md
│   ├── software-engineer-computer-vision.md
│   ├── uav-field-operations-engineer.md
│   ├── software-engineer-simulation.md
│   ├── head-of-business-development.md
│   ├── head-of-strategic-affairs.md
│   └── country-manager-ukraine.md
├── styles/                       # CSS files
└── images/                       # Image assets
```

## Creating a New Job Posting

1. Create a new markdown file in the `_jobs/` directory
2. Use the following frontmatter structure:

```markdown
---
layout: job-posting
title: "Job Title"
summary: "Compelling one-liner description of the role for main page and SEO"
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

## Job Summary Field

The `summary` field serves multiple purposes:

- **Main page display**: Shows on the careers section as a compelling preview
- **SEO meta descriptions**: Used in search engine results
- **Social media sharing**: Appears when job posts are shared on LinkedIn, Facebook, Twitter
- **Structured data**: Included in JSON-LD for search engines

**Best practices for summaries:**
- Keep them compelling and action-oriented
- Focus on the most exciting aspect of the role
- Aim for 1-2 sentences that capture the essence
- Use present tense and active voice

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
| `summary` | Yes | Compelling description for main page and SEO |
| `location` | Yes | Job location and work type |
| `employment_type` | Yes | Full-time, Part-time, Contract, etc. |
| `linkedin_url` | No | LinkedIn job posting URL |
| `date_posted` | Yes | When the job was posted (YYYY-MM-DD) |
| `valid_through` | Yes | When the job posting expires (YYYY-MM-DD) |

## SEO Features

Each job page automatically includes:

- **Meta title and description** using the summary field
- **Open Graph tags** for Facebook/LinkedIn sharing
- **Twitter Card tags** for Twitter sharing
- **Canonical URL** for search engines
- **JSON-LD structured data** for job postings
- **Proper heading hierarchy** for accessibility

## Main Page Integration

Job postings automatically appear on the main page careers section:

- **Sorted by date** (newest first)
- **Summary display** instead of truncated content
- **Clickable cards** that link to full job descriptions
- **Location information** with icons

## Benefits

1. **Consistency**: All job pages follow the same structure
2. **Maintainability**: Content is separated from presentation
3. **SEO Optimization**: Automatic meta tags and structured data
4. **Social Media Ready**: Optimized for sharing on all platforms
5. **Flexibility**: Easy to add new fields or modify the template
6. **Conditional Display**: LinkedIn application only shows when URL is provided
7. **Compelling Previews**: Summary field creates engaging main page descriptions

## Migration from HTML

The existing HTML job pages in the `careers/` directory can be removed once the Jekyll system is fully implemented and tested. 