# Inventory Manager PWA

This folder is ready to publish as a Progressive Web App.

## Files
- `index.html` — inventory application
- `manifest.webmanifest` — installation metadata
- `service-worker.js` — offline caching
- `icons/` — Home Screen icons

## Recommended publishing method: GitHub Pages
1. Create or sign in to a GitHub account.
2. Create a new repository named `inventory-manager`.
3. Upload the contents of this folder to the top level of the repository. Do not upload only the ZIP file.
4. In the repository, open **Settings > Pages**.
5. Under **Build and deployment**, choose **Deploy from a branch**.
6. Select the `main` branch and `/ (root)`, then save.
7. After GitHub publishes the site, open the provided HTTPS address in Safari on the iPhone.
8. Tap **Share > Add to Home Screen**, leave **Open as Web App** enabled, and tap **Add**.

## Important data note
Inventory data is currently stored in browser local storage on each device. Installing the app does not automatically synchronize data between devices. Use **Backup JSON** regularly and keep the backup in Files or iCloud Drive. Import that backup if the app is moved to a new device or browser.

## Updating the app
Replace the published files with the newer versions. The service worker will refresh its offline cache after the site is reopened. If a change does not appear immediately, close the Home Screen app completely and reopen it.
