# Comprehensive Guide to Jekyll's _config.yml

This guide provides a thorough overview of customizing your Jekyll site using `_config.yml`. We'll cover essential configurations and advanced techniques to optimize your site.

## 1. Basic Site Configuration

```yaml
title: My Professional Blog
email: contact@example.com
description: Insights on web development and technology trends
url: "https://yourdomain.com"
baseurl: "/blog"  # Use if your site is in a subdirectory, e.g., yourdomain.com/blog
```

- `title`: Your site's main title (appears in browser tab)
- `email`: Primary contact email
- `description`: Concise site description (used for SEO)
- `url`: Your domain name
- `baseurl`: Subdirectory, if applicable

## 2. Theme Selection and Customization

```yaml
theme: minima
minima:
  skin: classic
  social_links:
    twitter: your_twitter
    github: your_github
    linkedin: your_linkedin
```

- `theme`: Specify your chosen theme
- `skin`: Theme variation (if supported)
- `social_links`: Social media profiles

## 3. Build Settings

```yaml
markdown: kramdown
permalink: /:categories/:year/:month/:day/:title/
timezone: America/New_York
excerpt_separator: <!--more-->
```

- `markdown`: Markdown processor (kramdown recommended)
- `permalink`: URL structure for posts
- `timezone`: Local timezone for consistent dating
- `excerpt_separator`: Defines how post excerpts are created

## 4. Collections

```yaml
collections:
  projects:
    output: true
    permalink: /projects/:path/
  team:
    output: false
```

- Define custom content types
- `output: true` generates individual pages for items
- `output: false` for internal use only

## 5. Default Front Matter

```yaml
defaults:
  - scope:
      path: ""
      type: "posts"
    values:
      layout: "post"
      author: "Site Owner"
      comments: true
  - scope:
      path: ""
      type: "pages"
    values:
      layout: "page"
```

- Set default layouts and metadata for content types

## 6. Plugin Management

```yaml
plugins:
  - jekyll-seo-tag
  - jekyll-feed
  - jekyll-sitemap
  - jekyll-paginate
```

- Add functionality with plugins
- Note: GitHub Pages supports [limited plugins](https://pages.github.com/versions/)

## 7. Exclude/Include Files

```yaml
exclude:
  - Gemfile
  - Gemfile.lock
  - node_modules
  - vendor
include:
  - .htaccess
```

- `exclude`: Files/directories to exclude from the built site
- `include`: Force inclusion of files that Jekyll would otherwise ignore

## 8. Environment-specific Settings

```yaml
# Global settings
environment: production

# Development-specific overrides
development:
  environment: development
  url: "http://localhost:4000"
```

- Customize settings based on the build environment

## 9. SEO Optimization

```yaml
twitter:
  username: your_twitter_handle
  card: summary_large_image
logo: /assets/img/logo.png
social:
  name: Your Name
  links:
    - https://twitter.com/your_twitter
    - https://www.linkedin.com/in/your_linkedin
    - https://github.com/your_github
```

- Enhance social media sharing and SEO

## 10. Sass/SCSS Configuration

```yaml
sass:
  style: compressed
  sass_dir: _sass
```

- Customize CSS preprocessing

## Best Practices

1. Use comments to explain complex configurations
2. Regularly backup your `_config.yml`
3. Test changes locally before deploying
4. Avoid storing sensitive data in `_config.yml`
5. Use environment variables for API keys and secrets

Remember to restart your Jekyll server after modifying `_config.yml` to apply changes.

This guide covers key aspects of Jekyll site customization via `_config.yml`. For more advanced usage, refer to the [official Jekyll documentation](https://jekyllrb.com/docs/configuration/).
