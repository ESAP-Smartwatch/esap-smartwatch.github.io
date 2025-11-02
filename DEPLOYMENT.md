# GitHub Pages Deployment Guide

This document explains how to configure and deploy the ESAP Smartwatch website using GitHub Pages.

## Current Configuration

The website is configured to deploy from the `/docs` folder on the `main` branch using GitHub Actions.

## GitHub Repository Settings

To ensure GitHub Pages works correctly, verify these settings in your repository:

### 1. Enable GitHub Pages

1. Go to your repository on GitHub
2. Click **Settings** → **Pages** (in the left sidebar)
3. Under **Source**, select:
   - **Source**: GitHub Actions
4. Save the settings

### 2. Verify Actions Permissions

1. Go to **Settings** → **Actions** → **General**
2. Under **Workflow permissions**, ensure:
   - "Read and write permissions" is selected
   - "Allow GitHub Actions to create and approve pull requests" is checked

## Deployment Process

The site deploys automatically via GitHub Actions:

1. **Trigger**: Push to `main` branch
2. **Build**: Jekyll builds the site from `/docs` folder
3. **Deploy**: Built site is deployed to GitHub Pages
4. **Access**: Site is live at `https://esap-smartwatch.github.io`

## Local Development

### Prerequisites

- Ruby (version 2.7 or higher)
- Bundler gem
- Git

### Setup Steps

1. **Install Jekyll and Bundler**:
   ```bash
   gem install jekyll bundler
   ```

2. **Clone the repository**:
   ```bash
   git clone https://github.com/ESAP-Smartwatch/esap-smartwatch.github.io.git
   cd esap-smartwatch.github.io/docs
   ```

3. **Install dependencies**:
   ```bash
   bundle install
   ```

4. **Run local server**:
   ```bash
   bundle exec jekyll serve
   ```

5. **View the site**:
   - Open [http://localhost:4000](http://localhost:4000) in your browser
   - Changes will auto-reload

### Common Commands

```bash
# Serve with live reload (default)
bundle exec jekyll serve

# Serve with drafts
bundle exec jekyll serve --drafts

# Build without serving
bundle exec jekyll build

# Clean generated files
bundle exec jekyll clean
```

## Configuration Files

### _config.yml

Key settings in `/docs/_config.yml`:

```yaml
url: "https://esap-smartwatch.github.io"
baseurl: ""  # Empty for root domain
serverName: ESAP Smartwatch
serverDescription: Open-source smartwatch project with health tracking capabilities
```

**Important**: 
- `url` should be your GitHub Pages URL
- `baseurl` should be empty (`""`) for `username.github.io` repositories
- Update `serverName` and `serverDescription` as needed

### Gemfile

The `/docs/Gemfile` specifies Jekyll dependencies:

```ruby
gem "github-pages", group: :jekyll_plugins
```

This ensures compatibility with GitHub Pages versions.

## Troubleshooting

### Site Not Deploying

1. **Check Actions tab**: View build logs for errors
2. **Verify permissions**: Ensure Actions have write permissions
3. **Check branch**: Confirm pushing to `main` branch
4. **Review _config.yml**: Verify `url` and `baseurl` are correct

### Build Failures

Common issues:

1. **Ruby version**: GitHub Pages uses Ruby 3.x
2. **Gem dependencies**: Run `bundle update` if gems are outdated
3. **Syntax errors**: Check Jekyll/Liquid syntax in templates
4. **Missing files**: Ensure all referenced files exist

### Local vs Production Differences

If site works locally but not on GitHub Pages:

1. Check `baseurl` usage in links
2. Verify all assets use `{{ site.baseurl }}` prefix
3. Ensure no absolute paths to local files
4. Check for plugins not supported by GitHub Pages

## Custom Domain (Optional)

To use a custom domain:

1. Create `/docs/CNAME` file with your domain:
   ```
   yourdomain.com
   ```

2. Update DNS records at your domain registrar:
   ```
   Type: A
   Name: @
   Value: 185.199.108.153
   Value: 185.199.109.153
   Value: 185.199.110.153
   Value: 185.199.111.153
   ```

3. Update `_config.yml`:
   ```yaml
   url: "https://yourdomain.com"
   baseurl: ""
   ```

## Security

- **HTTPS**: Automatically enabled for `.github.io` domains
- **Environment secrets**: Store sensitive data in GitHub Secrets
- **Permissions**: Actions use minimal required permissions

## Monitoring

- **Build status**: Check the Actions tab after each push
- **Deployment status**: View in Settings → Pages
- **Analytics**: Enable Google Analytics in `_config.yml` (optional)

## Support

For issues:
- Check [Jekyll documentation](https://jekyllrb.com/docs/)
- Review [GitHub Pages documentation](https://docs.github.com/pages)
- Open an issue in the repository

---

**Last Updated**: November 2, 2025
