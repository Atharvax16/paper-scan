# 📄 Paper Scan · दस्तऐवज स्कॅनर

A simple, mobile-first document scanner that runs entirely in the browser.
Take photos of paper documents with your phone and save them as a single PDF —
no app to install, no account, no data ever leaves your phone.

ब्राउझरमध्येच चालणारा सोपा दस्तऐवज स्कॅनर. कागदाचे फोटो काढा आणि एका PDF मध्ये जतन करा —
कोणतेही ॲप नको, खाते नको, तुमचा डेटा फोनमध्येच राहतो.

**🔗 Live link / थेट लिंक:** https://atharvax16.github.io/paper-scan/

---

## ✨ Features

- 📷 **Take photo** with the camera, or **Choose photos** from the gallery (multiple at once)
- 📄 **Choose PDF** — turn an existing/normal PDF into a scanned-looking one (each page is rasterized and filtered, no re-printing needed)
- 🖼️ Four scan looks: **Document**, **Grayscale**, **Black & white**, **Original**
- 🔄 Rotate or 🗑️ delete any page (with confirmation)
- 📑 Export all pages as one **A4 PDF** with margins
- 🕘 **History** — saved PDFs are kept on the device so you can re-download them later, with a one-tap **Clear history**
- 🌐 **Bilingual** — मराठी / English, switch any time
- 🧭 Step-by-step guidance for non-technical users
- 🔒 Offline & private — everything happens on the device, nothing is ever uploaded

## 📱 How to use

1. Press **Take photo** and snap a picture of the paper.
2. Take as many photos as you like — each one becomes a page.
3. Rotate or delete a page if needed.
4. Type a file name and press **Save PDF**. Done!

> Tip: On a phone, open the link and use **"Add to Home Screen"** to use it like an app.

## 🛠️ Tech

- A single self-contained `index.html` — no backend, no build step.
- [jsPDF](https://github.com/parallax/jsPDF) (loaded from cdnjs) for PDF export.
- [pdf.js](https://mozilla.github.io/pdf.js/) (loaded from cdnjs) to rasterize existing PDFs so they can be re-scanned.
- Image handling via `createImageBitmap`, downscaling, and `<canvas>` filters.

## 🚀 Deploy (GitHub Pages)

This repo is published with GitHub Pages:
**Settings → Pages → Source: Deploy from a branch → `main` / root.**

## 📦 Run locally

Because browsers only allow the camera over HTTPS or `localhost`, serve it locally:

```bash
# Python
python -m http.server 8000
# then open http://localhost:8000
```

## 🔐 Privacy

- **Nothing is ever uploaded.** All image processing and PDF creation happen
  locally in your browser — no server, no account, no network requests with your documents.
- **History is stored on your own device only**, using the browser's IndexedDB,
  so you can re-download a PDF you saved earlier. It never leaves the phone.
- Because scans can be sensitive (IDs, bank papers), there is a **Clear history**
  button (and per-file delete) to wipe stored PDFs whenever you want.
- Want zero storage? Just clear the history after each use, or use a private/incognito tab.
