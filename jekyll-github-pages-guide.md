# Creating a Jekyll Site with GitHub Pages: A Step-by-Step Guide

Jekyll is a powerful static site generator that works great with GitHub Pages. This guide will walk you through creating your own Jekyll-powered website hosted for free on GitHub Pages.

## Prerequisites

- A GitHub account
- Git installed on your local machine
- Basic knowledge of command line operations
- Ruby installed on your local machine (Jekyll is written in Ruby)

## Step 1: Install Jekyll

First, let's install Jekyll and Bundler (a gem that manages other Ruby gems):

```bash
gem install jekyll bundler
```

## Step 2: Create a New Jekyll Site

Navigate to where you want to create your site and run:

```bash
jekyll new my-awesome-site
cd my-awesome-site
```

This creates a new Jekyll site in the `my-awesome-site` directory.

## Step 3: Test Your Site Locally

Before pushing to GitHub, let's make sure everything works locally:

```bash
bundle exec jekyll serve
```

Visit `http://localhost:4000` in your browser. You should see your new site!

## Step 4: Create a GitHub Repository

1. Go to GitHub and create a new repository.
2. Name it `username.github.io`, where `username` is your GitHub username.

## Step 5: Push Your Site to GitHub

In your local `my-awesome-site` directory:

```bash
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/username/username.github.io.git
git push -u origin main
```

Replace `username` with your GitHub username.

## Step 6: Configure GitHub Pages

1. Go to your repository on GitHub
2. Click on "Settings"
3. Scroll down to the "GitHub Pages" section
4. In the "Source" dropdown, select "main"
5. Click "Save"

## Step 7: Customize Your Site

Now, let's customize your site:

1. Edit `_config.yml`:
   This file contains site-wide configurations. Update the title, description, and other fields.

2. Create Posts:
   In the `_posts` directory, create new files with the format `YYYY-MM-DD-title.md`.

3. Add Pages:
   Create new `.md` files in the root directory for additional pages.

4. Customize Layout:
   Edit files in the `_layouts` and `_includes` directories to change your site's structure.

## Step 8: Using Themes

Jekyll supports themes. You can find many free and paid themes online. To use a theme:

1. Add the theme to your `_config.yml`:
   ```yaml
   theme: minima
   ```
2. Run `bundle install` to install the theme gem.

## Step 9: Adding Custom Domain (Optional)

If you have a custom domain:

1. Create a file named `CNAME` in your repository root.
2. Add your domain to this file, e.g., `www.yourdomain.com`.
3. Update your domain's DNS settings to point to GitHub Pages.

## Step 10: Continuous Deployment

Every time you push changes to your GitHub repository, GitHub Pages will automatically rebuild your site.

```bash
git add .
git commit -m "Update site content"
git push
```

Your changes will be live in a few minutes!

## Helpful Tips

- Use the `jekyll-seo-tag` plugin for better SEO.
- Leverage Jekyll's built-in support for Sass to write cleaner CSS.
- Explore Jekyll collections for organizing related content.
- Use Jekyll's data files feature to separate content from code.

Remember, Jekyll is highly customizable. As you get more comfortable, explore its documentation to unlock its full potential. Happy blogging with Jekyll and GitHub Pages!
