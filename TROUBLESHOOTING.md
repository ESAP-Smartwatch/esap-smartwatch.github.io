# GitHub Pages Build Troubleshooting

If your GitHub Pages build is failing, follow these steps:

## Quick Fixes

### Option 1: Use Simpler Deployment (Recommended)

Instead of using GitHub Actions, you can use the built-in Jekyll builder:

1. Go to your repository **Settings** → **Pages**
2. Under **Source**, change from "GitHub Actions" to "Deploy from a branch"
3. Select branch: **main**
4. Select folder: **/docs**
5. Click **Save**

This uses GitHub's built-in Jekyll processor which is simpler and more reliable.

### Option 2: Check Your GitHub Actions Workflow

If you want to use GitHub Actions:

1. Go to the **Actions** tab
2. Click on the failed workflow run
3. Expand the failed step to see the error message
4. Common issues:
   - Ruby version mismatch
   - Bundler cache issues
   - Path problems

## Common Build Errors and Fixes

### Error: "No such file or directory"

**Fix**: Ensure all paths in `_config.yml` start with `/` or use `{{ site.baseurl }}`

### Error: "Liquid Exception"

**Fix**: Check for syntax errors in:
- `index.md` front matter (YAML between `---`)
- Layout files in `_layouts/`
- Include files in `_includes/`

### Error: "Could not find gem"

**Fix**: 
1. Ensure `Gemfile` contains:
   ```ruby
   gem "github-pages", group: :jekyll_plugins
   ```
2. Commit and push again

### Error: "Theme not found"

**Fix**: In `_config.yml`, comment out the theme line:
```yaml
# theme: minima
```

Custom layouts don't need a theme.

## Verify Your Setup

Run these checks:

### 1. Check _config.yml

```yaml
url: "https://esap-smartwatch.github.io"
baseurl: ""  # Should be EMPTY for username.github.io repos
```

### 2. Verify File Structure

```
docs/
├── _config.yml (exists)
├── _layouts/ (exists)
│   ├── default.html
│   ├── home.html
│   └── page.html
├── index.md (exists)
├── about.md (exists)
└── Gemfile (exists)
```

### 3. Check Front Matter Syntax

Each `.md` file should start with:
```yaml
---
layout: page
navname: PageName
---
```

## Test Locally Before Pushing

To catch errors before deploying:

```bash
cd docs
bundle install
bundle exec jekyll build
```

If this succeeds locally, it should work on GitHub Pages.

## Still Having Issues?

### Method 1: Simplify the Config

Create a minimal `_config.yml`:

```yaml
url: "https://esap-smartwatch.github.io"
baseurl: ""
title: ESAP Smartwatch
description: Open-source smartwatch project

plugins:
  - jekyll-feed

exclude:
  - Gemfile
  - Gemfile.lock
  - node_modules/
  - vendor/
```

### Method 2: Check GitHub Pages Status

GitHub Pages might be having issues:
- Check [GitHub Status](https://www.githubstatus.com/)
- Wait 10-15 minutes and try again

### Method 3: Force Rebuild

1. Make a small change (add a space to README.md)
2. Commit and push
3. This triggers a fresh build

## Contact for Help

If none of these work:

1. Check the Actions tab for detailed error logs
2. Copy the specific error message
3. Search GitHub's documentation
4. Ask in the repository discussions

## Current Configuration Status

✅ GitHub Actions workflow created  
✅ _config.yml configured  
✅ All pages created  
✅ Layouts updated  
✅ Gemfile ready  

**Recommended**: Use "Deploy from a branch" method (Option 1 above) as it's more stable.
