# Site Structure Overview

This document provides an overview of the Jekyll portfolio site structure and how each component works together.

## Directory Structure

```
johnny-joo.github.io/
├── _awards/                    # Award collection files
│   ├── data-science-competition.md
│   └── hackathon-2024-winner.md
├── _data/                      # Site data files
│   └── navigation.yml          # Navigation menu configuration
├── _includes/                  # Reusable components
│   ├── footer.html
│   ├── header.html
│   └── navigation.html
├── _layouts/                   # Page templates
│   ├── award.html              # Template for award pages
│   ├── default.html            # Base template for all pages
│   ├── page.html               # Template for static pages
│   ├── post.html               # Template for blog posts
│   └── project.html            # Template for project pages
├── _posts/                     # Blog posts
│   └── 2024-01-10-getting-started-with-jekyll.md
├── _projects/                  # Project collection files
│   ├── ecommerce-platform.md
│   └── ml-image-classifier.md
├── assets/                     # Static assets
│   ├── css/
│   │   └── main.css           # Main stylesheet
│   └── images/                # Images directory
├── .github/
│   └── workflows/
│       └── jekyll.yml         # GitHub Actions deployment
├── _config.yml                 # Jekyll configuration
├── .gitignore                  # Git ignore rules
├── about.md                    # About page
├── awards.md                   # Awards listing page
├── blog.md                     # Blog listing page
├── Gemfile                     # Ruby dependencies
├── index.md                    # Homepage
├── projects.md                 # Projects listing page
└── README.md                   # Documentation

Generated site (_site/) - NOT committed to git:
├── about/index.html
├── awards/
│   ├── index.html
│   ├── data-science-competition/index.html
│   └── hackathon-2024-winner/index.html
├── blog/index.html
├── projects/
│   ├── index.html
│   ├── ecommerce-platform/index.html
│   └── ml-image-classifier/index.html
├── 2024/01/10/getting-started-with-jekyll.html
├── assets/css/main.css
├── feed.xml
├── sitemap.xml
└── index.html
```

## Page Types

### 1. Home Page (index.md)
- **Purpose**: Landing page with highlights and recent content
- **Layout**: default
- **Features**:
  - Hero section with introduction
  - Highlights grid (Awards, Projects, Blog)
  - Recent projects display
  - Latest blog posts

### 2. About Page (about.md)
- **Purpose**: Detailed personal information
- **Layout**: page
- **Content**:
  - Background and introduction
  - Skills and expertise
  - Experience timeline
  - Education
  - Contact information

### 3. Projects Page (projects.md)
- **Purpose**: Showcase all projects
- **Layout**: page
- **Features**:
  - Grid layout of project cards
  - Category filtering capability
  - Links to individual project pages

### 4. Project Detail Pages (_projects/*.md)
- **Purpose**: Detailed information about each project
- **Layout**: project
- **Front Matter Fields**:
  - `title`: Project name
  - `date`: Project date
  - `category`: Project category
  - `tags`: Technology tags
  - `links`: GitHub, demo, website URLs
- **Features**:
  - Full project description
  - Technology tags display
  - Links to GitHub/demo
  - Navigation to previous/next project

### 5. Awards Page (awards.md)
- **Purpose**: List all awards and competitions
- **Layout**: page
- **Features**:
  - Chronological listing
  - Award metadata (position, organizer)
  - Links to individual award pages

### 6. Award Detail Pages (_awards/*.md)
- **Purpose**: Detailed information about each award
- **Layout**: award
- **Front Matter Fields**:
  - `title`: Competition/award name
  - `position`: Placement or award received
  - `date`: Competition date
  - `organizer`: Organization name
  - `team`: List of team members
  - `links`: Certificate, project, news URLs
- **Features**:
  - Competition overview
  - Project description
  - Team information
  - Related links

### 7. Blog Page (blog.md)
- **Purpose**: List all blog posts
- **Layout**: page
- **Features**:
  - Reverse chronological post listing
  - Post previews with excerpts
  - Tags display
  - RSS feed link

### 8. Blog Post Pages (_posts/*.md)
- **Purpose**: Individual blog posts
- **Layout**: post
- **Naming Convention**: `YYYY-MM-DD-title.md`
- **Front Matter Fields**:
  - `layout`: post
  - `title`: Post title
  - `date`: Publication date and time
  - `author`: Author name
  - `tags`: Topic tags
- **Features**:
  - Full post content
  - Publication metadata
  - Tag display
  - Navigation to previous/next post

## Layouts Hierarchy

```
default.html (base layout)
├── page.html (for static pages)
├── post.html (for blog posts)
├── project.html (for projects)
└── award.html (for awards)
```

All layouts extend the `default.html` layout, which includes:
- Header with navigation
- Main content area
- Footer with links and social media

## Collections

### Projects Collection
- **Directory**: `_projects/`
- **Output**: Yes (generates individual pages)
- **Permalink**: `/projects/:title/`
- **Purpose**: Manage project portfolio items

### Awards Collection
- **Directory**: `_awards/`
- **Output**: Yes (generates individual pages)
- **Permalink**: `/awards/:title/`
- **Purpose**: Manage competition wins and recognitions

## Styling System

### CSS Variables (assets/css/main.css)
Customizable color scheme:
- `--primary-color`: Main brand color
- `--secondary-color`: Accent color
- `--text-color`: Body text color
- `--link-color`: Link color
- `--background`: Page background
- `--background-alt`: Alternate background

### Responsive Design
- Mobile-first approach
- Breakpoint at 768px for tablet/desktop
- Grid layouts that adapt to screen size
- Hamburger menu for mobile navigation

## Key Features

### 1. SEO Optimization
- `jekyll-seo-tag` plugin
- Automatic meta tags
- Open Graph tags
- Twitter Cards support
- Structured data (JSON-LD)

### 2. RSS Feed
- Automatic feed generation
- Located at `/feed.xml`
- Powered by `jekyll-feed` plugin

### 3. Sitemap
- Automatic sitemap generation
- Located at `/sitemap.xml`
- Powered by `jekyll-sitemap` plugin

### 4. GitHub Pages Integration
- Automatic deployment on push
- GitHub Actions workflow
- Compatible with GitHub Pages gem

## Content Management Workflow

### Adding a New Project
1. Create file: `_projects/project-name.md`
2. Add front matter with required fields
3. Write project description in Markdown
4. Commit and push

### Adding a New Award
1. Create file: `_awards/competition-name.md`
2. Add front matter with required fields
3. Write competition details in Markdown
4. Commit and push

### Writing a Blog Post
1. Create file: `_posts/YYYY-MM-DD-title.md`
2. Add front matter with required fields
3. Write post content in Markdown
4. Commit and push

## Deployment

### Local Development
```bash
bundle exec jekyll serve
# Site available at http://localhost:4000
```

### GitHub Pages Deployment
1. Push changes to main branch
2. GitHub Actions builds the site
3. Site deployed to https://johnny-joo.github.io

## Customization Quick Reference

### Change Site Title/Description
Edit `_config.yml`:
```yaml
title: "Your Name - Portfolio"
description: "Your description"
```

### Update Navigation Menu
Edit `_data/navigation.yml`:
```yaml
main:
  - title: "Page Name"
    url: /page-url/
```

### Customize Colors
Edit `assets/css/main.css` CSS variables:
```css
:root {
  --primary-color: #your-color;
  --secondary-color: #your-accent;
}
```

### Update Social Links
Edit `_config.yml`:
```yaml
social:
  linkedin: "https://linkedin.com/in/yourprofile"
  github: "https://github.com/yourusername"
  email: "your.email@example.com"
```

## Performance Features

- Static site generation (fast loading)
- Minimal JavaScript (lightweight)
- Optimized CSS
- GitHub CDN delivery
- Browser caching support

## Maintenance

### Regular Updates
- Keep gems updated: `bundle update`
- Review GitHub Pages versions
- Test locally before pushing
- Monitor build logs in GitHub Actions

### Backup
- All source files in Git repository
- Generated site can be rebuilt anytime
- Configuration preserved in version control
