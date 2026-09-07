# Synthetic Route (ROS) Sketcher & Exporter

A free, web-based alternative to ChemBioDraw designed for sketching Route of Synthesis (ROS) multi-step schemes and generating publication-ready vector PDFs directly in the browser.

## Features
- **Full Chemical Scheme Canvas**: Powered by EPAM Ketcher with reaction arrows, conditions, yields, and retrosynthesis arrows.
- **ACS 1996 Preset**: Automatically scales bond lengths (14.4 pt), line weights, and Arial typography to American Chemical Society standards.
- **Vector PDF Output**: Uses `svg2pdf.js` and `jsPDF` to generate crisp, infinitely scalable PDFs without pixelation.
- **Zero Server Costs**: Runs entirely on GitHub Pages without server-side dependencies.

## Deployment Instructions

1. Create a new GitHub repository and upload these files:
   - `index.html`
   - `README.md`
   - `.gitignore`
   - `.github/workflows/deploy.yml`
2. Navigate to **Settings** > **Pages** in your repository.
3. Under **Build and deployment** > **Source**, select **GitHub Actions**.
4. Push to `main` (or run the workflow manually under the **Actions** tab). GitHub will fetch Ketcher, configure the site, and publish your link.

## Local Testing
To run the app locally on your machine:
```bash
# 1. Download and extract Ketcher standalone into a /ketcher folder
curl -L -o ketcher.zip [https://github.com/epam/ketcher/releases/download/v2.26.0/ketcher-standalone-v2.26.0.zip](https://github.com/epam/ketcher/releases/download/v2.26.0/ketcher-standalone-v2.26.0.zip)
unzip ketcher.zip -d ketcher

# 2. Start a local HTTP server
python3 -m http.server 8000
