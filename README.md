# ESAP Smartwatch Website

Official website for the ESAP Smartwatch project - an open-source health tracking smartwatch developed by Embedded Systems @ Purdue.

**Live Site**: [https://esap-smartwatch.github.io](https://esap-smartwatch.github.io)

## About

This repository contains the GitHub Pages website for the ESAP Smartwatch project. The website provides:

- Project overview and features
- Technical documentation
- Getting started guides
- Screenshots and demos
- Links to source code and resources

## Project Links

- **Mobile App Repository**: [github.com/ESAP-Smartwatch/app](https://github.com/ESAP-Smartwatch/app)
- **Website**: [esap-smartwatch.github.io](https://esap-smartwatch.github.io)

## Technology Stack

This website is built with:
- **Jekyll**: Static site generator
- **GitHub Pages**: Hosting
- **Tailwind CSS**: Styling framework
- **Moonrise Template**: Base template (customized)

## Local Development

To run this website locally:

1. **Install Jekyll and dependencies**:
   ```bash
   gem install jekyll bundler
   ```

2. **Clone the repository**:
   ```bash
   git clone https://github.com/ESAP-Smartwatch/esap-smartwatch.github.io.git
   cd esap-smartwatch.github.io
   ```

3. **Install dependencies**:
   ```bash
   cd docs
   bundle install
   ```

4. **Run the local server**:
   ```bash
   bundle exec jekyll serve
   ```

5. **View in browser**:
   Open [http://localhost:4000](http://localhost:4000)

## Project Structure

```
docs/
├── _config.yml           # Site configuration
├── index.md              # Homepage content
├── about.md              # About page
├── screenshots.md        # Screenshots gallery
├── map.md                # Documentation page
├── donate.md             # Support page
├── _layouts/             # Page templates
├── _includes/            # Reusable components
├── assets/               # CSS, JS, and other assets
└── media/                # Images and media files
```

## Deployment

This site is automatically deployed via GitHub Pages when changes are pushed to the `main` branch.

### GitHub Pages Settings

- **Source**: Deploy from `/docs` folder on `main` branch
- **Custom Domain**: Not configured (uses github.io subdomain)
- **HTTPS**: Enabled

## Contributing

Contributions to improve the website are welcome! Please:

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Submit a pull request

## License

This website is part of the ESAP Smartwatch project and is licensed under the Apache 2.0 License.

Copyright © 2025 by William Zhang & Embedded Systems @ Purdue

---

## Credits

- **Original Template**: [Moonrise](https://github.com/coffeebank/moonrise) by coffeebank
- **Development**: Embedded Systems @ Purdue
- **Project Lead**: William Zhang
