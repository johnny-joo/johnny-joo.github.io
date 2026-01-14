# Personal Portfolio Website

A Jekyll-based portfolio website showcasing projects, awards, and blog posts. Built with GitHub Pages for easy deployment and maintenance.

## 🌟 Features

- **Modern Design**: Clean, responsive layout that works on all devices
- **Project Showcase**: Dedicated section for highlighting your work
- **Awards & Achievements**: Display your competition wins and recognitions
- **Blog**: Share your thoughts, tutorials, and insights
- **Easy Customization**: Simple configuration for personalization
- **GitHub Pages Ready**: Automatic deployment on push

## 🚀 Quick Start

### Prerequisites

- Ruby (version 2.5.0 or higher)
- RubyGems
- GCC and Make

### Local Development

1. **Clone the repository**
   ```bash
   git clone https://github.com/johnny-joo/johnny-joo.github.io.git
   cd johnny-joo.github.io
   ```

2. **Install dependencies**
   ```bash
   bundle install
   ```

3. **Run the site locally**
   ```bash
   bundle exec jekyll serve
   ```

4. **View the site**
   Open your browser and navigate to `http://localhost:4000`

### Building for Production

```bash
bundle exec jekyll build
```

The built site will be in the `_site` directory.

## 📝 Customization

### Site Configuration

Edit `_config.yml` to update:

```yaml
title: "Your Name - Portfolio"
description: "Your site description"
email: "your.email@example.com"

social:
  linkedin: "https://www.linkedin.com/in/yourprofile"
  github: "https://github.com/yourusername"
  email: "your.email@example.com"
```

### Personal Information

Update the following files with your information:
- `about.md` - Your biography and background
- `index.md` - Homepage content

## 📂 Content Management

### Adding a New Project

1. Create a new file in `_projects/` directory
2. Name it descriptively: `project-name.md`
3. Add front matter and content:

```markdown
---
title: "Your Project Title"
date: 2024-01-15
category: "Web Development"
tags:
  - React
  - Node.js
  - MongoDB
links:
  github: "https://github.com/yourusername/project"
  demo: "https://demo.project.com"
---

## Overview
Your project description here...
```

### Adding an Award/Competition

1. Create a new file in `_awards/` directory
2. Name it descriptively: `competition-name.md`
3. Add front matter and content:

```markdown
---
title: "Competition Name"
position: "1st Place"
date: 2024-03-15
organizer: "Organization Name"
team:
  - "Your Name"
  - "Team Member 2"
links:
  certificate: "https://example.com/certificate"
  project: "https://github.com/yourusername/project"
---

## Competition Overview
Your competition description here...
```

### Writing a Blog Post

1. Create a new file in `_posts/` directory
2. Name it following the pattern: `YYYY-MM-DD-post-title.md`
3. Add front matter and content:

```markdown
---
layout: post
title: "Your Post Title"
date: 2024-01-10 10:00:00 +0000
author: "Your Name"
tags:
  - Jekyll
  - Tutorial
---

Your post content here...
```

## 🎨 Styling

The site uses custom CSS located in `assets/css/main.css`. Key features:

- **CSS Variables**: Easy color customization
- **Responsive Grid**: Adapts to all screen sizes
- **Modern Layout**: Flexbox and Grid for layouts
- **Custom Components**: Cards, navigation, footer

To customize colors, edit the CSS variables in `assets/css/main.css`:

```css
:root {
  --primary-color: #2c3e50;
  --secondary-color: #3498db;
  --text-color: #333;
  /* ... */
}
```

## 📋 Front Matter Guide

### Common Fields

All content files support these front matter fields:

- `title`: Page/post title
- `date`: Publication date (YYYY-MM-DD format)
- `layout`: Layout template to use
- `permalink`: Custom URL (optional)

### Project-Specific Fields

- `category`: Project category
- `tags`: Array of technology tags
- `links`: Object with github, demo, website URLs

### Award-Specific Fields

- `position`: Your placement/award
- `organizer`: Competition organizer
- `team`: Array of team member names
- `links`: Object with certificate, project, news URLs

### Post-Specific Fields

- `author`: Post author name
- `tags`: Array of topic tags

## 🌐 Deployment

### GitHub Pages (Automatic)

1. Push your changes to the `main` branch (or configured branch)
2. GitHub Pages will automatically build and deploy
3. Your site will be live at `https://yourusername.github.io`

### GitHub Pages Settings

1. Go to repository Settings
2. Navigate to Pages section
3. Set source to your main branch
4. Save changes

### Custom Domain (Optional)

1. Add a `CNAME` file with your domain name
2. Configure DNS settings with your domain provider
3. Update `url` in `_config.yml`

## 🔧 Advanced Configuration

### Navigation Menu

Edit `_data/navigation.yml` to customize menu items:

```yaml
main:
  - title: "Home"
    url: /
  - title: "About"
    url: /about/
  - title: "Projects"
    url: /projects/
```

### Adding Plugins

Add to `Gemfile`:

```ruby
group :jekyll_plugins do
  gem "jekyll-feed"
  gem "jekyll-seo-tag"
  # Add more plugins
end
```

Update `_config.yml`:

```yaml
plugins:
  - jekyll-feed
  - jekyll-seo-tag
```

Run `bundle install` to install new plugins.

### Custom Layouts

Create new layouts in `_layouts/` directory. Extend existing layouts:

```liquid
---
layout: default
---

<div class="custom-layout">
  {{ content }}
</div>
```

## 📊 SEO Optimization

The site includes:
- SEO meta tags via `jekyll-seo-tag`
- Sitemap generation via `jekyll-sitemap`
- RSS feed via `jekyll-feed`

Update SEO settings in `_config.yml` and page front matter.

## 🐛 Troubleshooting

### Bundle Install Errors

```bash
# Update bundler
gem update bundler

# Clean and reinstall
rm Gemfile.lock
bundle install
```

### Jekyll Build Errors

```bash
# Clean Jekyll cache
bundle exec jekyll clean

# Rebuild with verbose output
bundle exec jekyll build --verbose
```

### Port Already in Use

```bash
# Specify a different port
bundle exec jekyll serve --port 4001
```

## 📚 Resources

- [Jekyll Documentation](https://jekyllrb.com/docs/)
- [GitHub Pages Documentation](https://docs.github.com/en/pages)
- [Liquid Template Language](https://shopify.github.io/liquid/)
- [Markdown Guide](https://www.markdownguide.org/)

## 🤝 Contributing

Feel free to fork this repository and customize it for your own use. If you find bugs or have suggestions, please open an issue.

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

## 📧 Contact

- **Email**: your.email@example.com
- **LinkedIn**: [linkedin.com/in/yourprofile](https://linkedin.com/in/yourprofile)
- **GitHub**: [github.com/johnny-joo](https://github.com/johnny-joo)

---

Built with ❤️ using Jekyll and GitHub Pages