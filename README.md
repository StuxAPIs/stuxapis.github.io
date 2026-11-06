<p align="center">
  <picture><source media="(prefers-color-scheme: dark)" srcset="https://global.media.stuxapis.net/logo-light.png"><source media="(prefers-color-scheme: light)" srcset="https://global.media.stuxapis.net/logo-dark.png"><img src="https://global.media.stuxapis.net/logo-dark.png" height="100" alt="StuxAPIs Logo"></picture>
</p>

# GitHub Pages Redirect

A simple template for redirecting your GitHub Pages site (username.github.io) to your custom domain.

## Features

- ✨ Lightweight and fast redirect solution
- 🎯 Easy to set up in minutes
- 📱 Works on all devices and browsers
- 🔗 Preserves URL paths during redirect

## Quick Start

1. **Fork or use this template** to create a new repository named `username.github.io`
2. **Update the domain** in the HTML file:
   - Replace `example.com` with your actual domain
3. **Enable GitHub Pages** in your repository settings
4. **Visit** `https://username.github.io` to test the redirect

## How It Works

This template uses a simple HTML meta refresh to redirect visitors from your GitHub Pages URL to your custom domain. The redirect happens automatically when users visit your `username.github.io` page.

## Installation

### Option 1: Using as a Template
1. Click **"Use this template"** on the GitHub repository page
2. Name your repository `username.github.io` (replace `username` with your GitHub username)
3. Customize the domain in `index.html`

### Option 2: Manual Setup
1. Create a new repository named `username.github.io`
2. Copy the contents of this template to your repository
3. Update the redirect URL in `index.html`
4. Push to GitHub

## Configuration

Edit `index.html` and change this line:
```html
<meta http-equiv="refresh" content="0;url=https://example.com" />
<link rel="canonical" href="https://example.com" />
```

Replace `https://example.com` with your actual domain.

## Troubleshooting

- **Redirect not working?** Ensure your repository is named exactly `username.github.io` and GitHub Pages is enabled
- **Need to change the redirect delay?** Modify the `content="0;url=..."` value (0 = immediate)
- **Want to customize the loading page?** Edit the HTML content before the meta redirect tag

## Versioning

This project uses [Date Versioning](https://datevers.ing): each release is numbered by its UTC release date as `YY.MM.DD` (for example `26.10.23`), with `-1`, `-2`… for later releases the same day. See [CHANGELOG.md](CHANGELOG.md) for what changed in each release.

Releases are committed and tagged on the `test` branch and reach `main` through a pull request from `test`, which needs CI to pass and is reviewed and merged by Leo; see [Branches](CONTRIBUTING.md#branches).

## License

Feel free to use this template for your own projects!

## Support

Have questions? Check the [GitHub Pages documentation](https://pages.github.com/) or open an issue in this repository.

---

Made by [StuxAPIs](https://github.com/StuxAPIs)

*StuxAPIs is part of the [Stux.Group](https://github.com/StuxGroup) Brand of Companies.*
