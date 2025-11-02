# Quick Start - Publishing Your Website

Follow these steps to publish your ESAP Smartwatch website to GitHub Pages.

## Step 1: Review Your Changes

The website has been converted and is ready to deploy. Here's what was updated:

✅ Homepage with project information  
✅ About page with team and project details  
✅ Documentation page with guides and links  
✅ Support page for contributions  
✅ Navigation bar configured  
✅ GitHub Actions workflow for automatic deployment  
✅ All configurations updated for GitHub Pages  

## Step 2: Commit and Push Changes

Open your terminal in the project directory and run:

```bash
# Check what files were changed
git status

# Add all changes
git add .

# Commit with a descriptive message
git commit -m "Convert template to ESAP Smartwatch project website"

# Push to GitHub
git push origin main
```

## Step 3: Enable GitHub Pages

1. Go to your GitHub repository: https://github.com/ESAP-Smartwatch/esap-smartwatch.github.io

2. Click **Settings** (top navigation)

3. Click **Pages** (left sidebar)

4. Under **Build and deployment**:
   - **Source**: Select **GitHub Actions**
   - The site will automatically deploy when you push to main

5. Click **Save** (if needed)

## Step 4: Monitor Deployment

1. Go to the **Actions** tab in your repository

2. You should see a workflow running: "Deploy Jekyll site to Pages"

3. Wait for it to complete (usually 1-2 minutes)
   - Green checkmark ✅ = Success
   - Red X ❌ = Failed (check logs)

## Step 5: Visit Your Website

Once deployment is complete:

🌐 **Your website will be live at**: https://esap-smartwatch.github.io

## Step 6: Test Your Website

Check the following:

- [ ] Homepage loads correctly
- [ ] All navigation links work
- [ ] Documentation page displays properly
- [ ] About page shows correct information
- [ ] Screenshots page works (add images to `/docs/screenshots/` folder)
- [ ] External GitHub link opens in new tab
- [ ] Mobile responsive design works

## Optional Enhancements

### Add Project Screenshots

1. Add screenshot images to `/docs/screenshots/` folder
2. Supported formats: JPG, PNG, GIF
3. They'll automatically appear in the Screenshots gallery
4. Commit and push:
   ```bash
   git add docs/screenshots/*
   git commit -m "Add project screenshots"
   git push origin main
   ```

### Update Favicon

1. Replace files in `/docs/media/`:
   - `favicon.ico`
   - `android-chrome-192x192.png`
   - `apple-touch-icon.png`
2. Commit and push changes

### Add Google Analytics (Optional)

1. Get your Google Analytics ID
2. Edit `/docs/_config.yml`
3. Uncomment and add your ID:
   ```yaml
   googleAnalyticsID: "G-XXXXXXXXXX"
   ```
4. Commit and push

### Custom Domain (Optional)

If you want to use a custom domain like `smartwatch.example.com`:

1. Create `/docs/CNAME` file with your domain:
   ```
   smartwatch.example.com
   ```

2. Configure DNS at your domain provider (see DEPLOYMENT.md for details)

3. Update `_config.yml`:
   ```yaml
   url: "https://smartwatch.example.com"
   ```

4. Commit and push

## Troubleshooting

### Site Not Deploying

**Check Actions Tab**: Look for error messages in the workflow logs

**Verify Settings**: Ensure Pages source is set to "GitHub Actions"

**Check _config.yml**: Verify no syntax errors

### 404 Errors on Pages

**Check file names**: Ensure `about.md`, `map.md`, etc. exist in `/docs/`

**Verify baseurl**: Should be empty (`""`) for username.github.io repos

### Styling Issues

**Clear browser cache**: Hard refresh with `Cmd+Shift+R` (Mac) or `Ctrl+Shift+R` (Windows)

**Check assets**: Verify all CSS/JS files exist in `/docs/assets/`

## Need Help?

- 📖 Read [DEPLOYMENT.md](DEPLOYMENT.md) for detailed deployment info
- 📖 Check [CHANGES.md](CHANGES.md) for summary of all changes
- 🐛 [Jekyll documentation](https://jekyllrb.com/docs/)
- 🐛 [GitHub Pages documentation](https://docs.github.com/pages)

## Next Steps After Publishing

1. **Share your website**: Add the URL to your GitHub repository description
2. **Update README**: Add website badge to the app repository
3. **Promote**: Share on social media and with your team
4. **Maintain**: Keep content updated as the project evolves

---

**Ready to go live?** Run the commands in Step 2 and watch your website deploy! 🚀
