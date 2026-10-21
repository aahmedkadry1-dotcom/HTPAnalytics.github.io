# HTP Analytics 3D (Tableau)

Tableau can't run 3D (three.js) inside its own objects. Instead, the 3D world is a web page that Tableau shows inside a **Web Page object**.

## Files
- `index.html` + `assets/` is the 3D world. Host this folder on any HTTPS web server.
- `HTP Analytics 3D.twb` is a 1366 × 768 dashboard with one full-size Web Page object.

## Steps
1. **Add links:** open `index.html` and paste the published dashboard URLs into the `EDIT HERE` block at the top (34 entries).
2. **Host:** upload `index.html` and `assets/` to an internal HTTPS host, such as an IIS/Apache server, Azure Static Web Apps or S3/CloudFront.
3. **Allow it:** in Tableau Cloud/Server, go to Settings → Web Page Objects. Turn web page objects on and add your host to the safe list.
4. **Workbook:** open the `.twb` and edit the Web Page object URL (it's set to `https://YOUR-HOST/htp-analytics-3d/index.html`), or add your own Web Page object to any dashboard. Then publish.

## Notes
- The page loads three.js and the Archivo font from public servers (jsdelivr, Google Fonts). If your network blocks them, host those files yourself.
- Dashboard links open in a new tab. You can change this with `linkTarget` in the same block.
- Every object, label, index item, breadcrumb and Previous/Next button moves you around inside the world. The ↗ links open the published Tableau dashboards.
