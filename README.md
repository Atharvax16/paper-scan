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
- 🖼️ Four scan looks: **Document**, **Grayscale**, **Black & white**, **Original**
- 🔄 Rotate or 🗑️ delete any page (with confirmation)
- 📑 Export all pages as one **A4 PDF** with margins
- 🌐 **Bilingual** — मराठी / English, switch any time
- 🧭 Step-by-step guidance for non-technical users
- 🔒 100% offline & private — everything happens on the device, nothing is uploaded

## 📱 How to use

1. Press **Take photo** and snap a picture of the paper.
2. Take as many photos as you like — each one becomes a page.
3. Rotate or delete a page if needed.
4. Type a file name and press **Save PDF**. Done!

> Tip: On a phone, open the link and use **"Add to Home Screen"** to use it like an app.

## 🛠️ Tech

- A single self-contained `index.html` — no backend, no build step.
- [jsPDF](https://github.com/parallax/jsPDF) (loaded from cdnjs) for PDF export.
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

No localStorage, no cookies, no network requests with your images.
Photos are processed in memory and discarded when you close the page.
