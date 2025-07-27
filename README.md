# Venkata Chikkam - Portfolio Website

A professional GitHub Pages portfolio showcasing various computer science projects with password-protected code access.

## 🚀 Features

- **Modern, Responsive Design**: Beautiful gradient background with card-based layout
- **Project Showcase**: Displays all your projects with detailed descriptions and technology tags
- **Password Protection**: Secure access control for viewing project code
- **Mobile-Friendly**: Fully responsive design that works on all devices
- **Professional UI**: Clean, modern interface with smooth animations

## 📋 Projects Included

1. **Machine Learning - Stock Analysis & Prediction**
   - Real-time stock data via Alpaca API
   - Multiple ML models (Decision Trees, Random Forest, Linear Regression)
   - Technical indicators and news sentiment analysis
   - Access Code: `ml2024`

2. **Search Algorithms Implementation**
   - A*, BFS, DFS, UCS algorithms
   - Pac-Man game environment
   - Multiple maze layouts and ghost agents
   - Access Code: `search2024`

3. **Multi-Agent Systems**
   - Intelligent ghost agents
   - Advanced evaluation functions
   - Contest-level performance optimization
   - Access Code: `agent2024`

4. **Operating Systems Projects**
   - Process management implementation
   - File system operations
   - Dining philosophers problem solution
   - Access Code: `os2024`

5. **Tracking & Bayesian Networks**
   - Bayesian network implementation
   - Particle filtering algorithms
   - Exact inference methods
   - Access Code: `track2024`

6. **Senior Project - EDRish**
   - Comprehensive data analysis
   - Research methodology
   - Technical documentation
   - Access Code: `senior2024`

## 🛠️ Setup Instructions

### Option 1: GitHub Pages (Recommended)

1. **Create a new GitHub repository**:
   - Go to GitHub and create a new repository
   - Name it anything you want (e.g., `portfolio-website` or `my-projects`)

2. **Upload the files**:
   - Upload `index.html` to the root of your repository
   - Upload this `README.md` file

3. **Enable GitHub Pages**:
   - Go to your repository settings
   - Scroll down to "Pages" section in the left sidebar
   - Under "Source", select "Deploy from a branch"
   - Choose "main" branch and "/ (root)" folder
   - Click "Save"

4. **Access your site**:
   - GitHub will provide you with a unique URL for your site
   - It will look something like: `https://yourusername.github.io/repository-name`
   - The exact URL will be shown in the Pages settings after deployment

### Option 2: Using GitHub Actions (Advanced)

If you want to use a custom workflow, create a `.github/workflows/deploy.yml` file:

```yaml
name: Deploy to GitHub Pages

on:
  push:
    branches: [ main ]
  workflow_dispatch:

permissions:
  contents: read
  pages: write
  id-token: write

concurrency:
  group: "pages"
  cancel-in-progress: false

jobs:
  deploy:
    environment:
      name: github-pages
      url: ${{ steps.deployment.outputs.page_url }}
    runs-on: ubuntu-latest
    steps:
    - name: Checkout
      uses: actions/checkout@v4
    - name: Setup Pages
      uses: actions/configure-pages@v4
    - name: Upload artifact
      uses: actions/upload-pages-artifact@v3
      with:
        path: '.'
    - name: Deploy to GitHub Pages
      id: deployment
      uses: actions/deploy-pages@v4
```

### Option 3: Local Development

1. **Clone or download the files** to your local machine

2. **Open `index.html`** in your web browser

3. **For live development**, you can use a local server:
   ```bash
   # Using Python 3
   python -m http.server 8000
   
   # Using Node.js (if you have it installed)
   npx serve .
   ```

## 🔐 Password Protection

The site includes a password protection system for accessing project code. Each project has its own access code:

- **Machine Learning**: `ml2024`
- **Search Algorithms**: `search2024`
- **Multi-Agent Systems**: `agent2024`
- **Operating Systems**: `os2024`
- **Tracking**: `track2024`
- **Senior Project**: `senior2024`

### Customizing Access Codes

To change the access codes, edit the `accessCodes` object in the JavaScript section of `index.html`:

```javascript
const accessCodes = {
    "ml": "your_new_code",
    "search": "your_new_code", 
    "multiagent": "your_new_code",
    "os": "your_new_code",
    "tracking": "your_new_code",
    "senior": "your_new_code"
};
```

## 🎨 Customization

### Changing Colors

The site uses a purple gradient theme. To change colors, modify the CSS variables in `index.html`:

```css
body {
    background: linear-gradient(135deg, #your_color1 0%, #your_color2 100%);
}
```

### Adding New Projects

To add a new project, add an entry to the `projects` array in the JavaScript section:

```javascript
{
    title: "Your Project Title",
    description: "Your project description",
    tech: ["Technology1", "Technology2", "Technology3"],
    type: "yourproject",
    hasCode: true  // or false if no code available
}
```

And add the corresponding access code:

```javascript
const accessCodes = {
    // ... existing codes ...
    "yourproject": "your_access_code"
};
```

### Modifying Project Information

Edit the project descriptions, technologies, and features in the `projects` array and the `viewProject()` function in the JavaScript section.

## 📱 Responsive Design

The site is fully responsive and includes:
- Mobile-optimized layout
- Touch-friendly buttons
- Readable text on all screen sizes
- Optimized spacing for different devices

## 🔧 Technical Details

- **HTML5**: Semantic markup
- **CSS3**: Modern styling with flexbox and grid
- **JavaScript**: Vanilla JS for interactivity
- **No Dependencies**: Pure HTML/CSS/JS - no frameworks required
- **Fast Loading**: Optimized for quick page loads

## 🚀 Deployment Tips

1. **Custom Domain**: You can add a custom domain in GitHub Pages settings
2. **HTTPS**: GitHub Pages automatically provides SSL certificates
3. **Analytics**: Consider adding Google Analytics for visitor tracking
4. **SEO**: The site includes proper meta tags for search engine optimization

## 📞 Support

If you need help with:
- Setting up GitHub Pages
- Customizing the design
- Adding new projects
- Troubleshooting issues

Feel free to modify the code or reach out for assistance.

## 📄 License

This project is open source and available under the MIT License.

---

**Note**: This portfolio site is designed to showcase your projects professionally while maintaining control over who can access your code. The password protection system provides a simple way to share access codes with specific individuals while keeping your code private from the general public. 