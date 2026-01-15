# PDF Editor (100% Client-Side)

This is a simple but powerful web application for performing the most common operations with PDF files.

**Key Feature: 100% Privacy.** All operations (conversion, merging, extraction) happen **exclusively in your browser**. None of your files are ever uploaded to a server. All processing is performed on your device.

## 🚀 Live Demo

You can try it right now at this link:
**[https://artem0708.github.io/pdf-converter/](https://artem0708.github.io/pdf-converter/)**

---

## 🛠️ Features

This tool combines four main functions in one convenient interface:

1.  **Image to PDF**
    * Converts one or more images (JPG, PNG, WebP) into a single PDF document.
    * Automatically corrects photo orientation (e.g., from phones) by reading EXIF data.
    * Selects the correct page orientation (portrait or landscape) for each image.

2.  **Merge PDF**
    * Allows selecting multiple PDF files.
    * "Glues" them into one final PDF document in the order they were selected.

3.  **Split / Assemble PDF**
    * Loads a PDF file and displays thumbnails of all its pages.
    * Allows you to "assemble" a new document by clicking on the desired pages.
    * In the "Your New Document" window, you can **drag and drop** pages to set the perfect order.
    * Clicking on a page in the new document removes it.

4.  **Extract Images (to .zip)**
    * Scans the entire PDF document page by page.
    * Finds all embedded images (raster and JPEG).
    * Converts every found image to **PNG** format.
    * Packs all images into a **single .zip archive** for convenient downloading.

---

## ⚙️ Technologies

This project is a Single Page Application (SPA) that runs entirely on the client side. It requires no backend.

* **HTML5 / CSS3 / Vanilla JavaScript**
* **[jsPDF](https://github.com/parallax/jsPDF)**: For creating PDF documents from images ("Image to PDF" tab).
* **[exifr](https://github.com/mutiny-labs/exifr)**: For reading EXIF data (orientation) from JPG files.
* **[pdf-lib](https://github.com/Hopding/pdf-lib)**: For "editing" PDF: merging and assembling new documents.
* **[pdf.js](https://github.com/mozilla/pdf.js)**: The engine from Mozilla for reading PDF files and rendering page thumbnails ("Split" and "Extract" tabs).
* **[JSZip](https://github.com/Stuk/jszip)**: For creating .zip archives in the browser ("Extract Images" tab).

---

## 💻 How to use locally

This project requires no build process or complex installation.

1.  Clone the repository:
    ```bash
    git clone [https://github.com/Artem0708/pdf-converter.git](https://github.com/Artem0708/pdf-converter.git)
    ```
2.  Go to the project folder:
    ```bash
    cd pdf-converter
    ```
3.  Since `pdf.js` requires an HTTP server to load its "workers" (and will not work if the file is opened via `file:///`), run a simple local server.

    *If you have **Python 3** installed:*
    ```bash
    python -m http.server
    ```
    *If you have **Node.js** (and `live-server`):*
    ```bash
    npm install -g live-server
    live-server
    ```

4.  Open `http://localhost:8000` (for Python) or `http://localhost:8080` (for `live-server`) in your browser.