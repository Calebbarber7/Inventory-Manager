# Inventory Manager PWA v2

## Replace the existing GitHub Pages files

1. Back up the current app using **Share Backup** or **Export > Export full backup**.
2. In the GitHub repository, replace the old `index.html`, `service-worker.js`, and `manifest.webmanifest`.
3. Add the new `app.js` and `styles.css` files.
4. Keep or replace the `icons` folder with the included folder.
5. Commit the changes to the same branch used by GitHub Pages.
6. On iPhone, fully close the Home Screen app and reopen it. If the old version remains, open the GitHub Pages URL in Safari, refresh it, then reopen the Home Screen app.

## New features

- iPhone-first card interface and desktop table
- Dashboard totals and profit margin
- Item photos using Camera or Photos
- Categories, source, purchase date, location, and notes
- Search, status/category filters, and sorting
- Dark mode
- Bulk-cost calculator inside the item editor
- CSV, Excel, and JSON import/export
- Automatic local snapshots with restore and download
- One-tap iOS Share Sheet backup
- IndexedDB storage for larger inventories and photos

## Import column names

CSV and Excel imports recognize these headers:

`Item Name`, `Size`, `Category`, `Weight (oz)`, `Cost`, `Sold`, `Purchase Date`, `Purchased From`, `Storage Location`, `Notes`

The app also accepts the original headers `Item Name`, `Size`, `Weight`, `Cost`, and `Sold`.

## Backup behavior

Automatic snapshots are stored locally on the device and the app keeps the latest 10. They are recovery points, not cloud copies. Use **Share Backup** to save a JSON backup to iCloud Drive, Files, AirDrop, email, or another destination.

## Excel support

Excel import/export uses the browser build of SheetJS. The script is loaded from the official SheetJS CDN and is cached by the service worker after the first successful online load. CSV and JSON tools do not depend on that library.
