# tesseract-4.0.0-best-int

- Tesseract text recognition data (LSTM), one file per language, for the Tesseract engine (tesseract.js 7.0.0) of the
  apps. Upstream: the tessdata_best models of the Tesseract OCR project (https://github.com/tesseract-ocr/tessdata_best),
  Apache-2.0.
- Files copied unchanged from the npm packages `@tesseract.js-data/<code>@1.0.0` (https://www.npmjs.com/org/tesseract.js-data),
  folder `4.0.0_best_int` (tessdata_best converted to integer models, the data tesseract.js loads by default for its
  LSTM engine). `tgl.traineddata.gz` (Tagalog) has no `4.0.0_best_int` there and comes from the package's `4.0.0` folder.
- Each file is gzip-compressed `<code>.traineddata`; tesseract.js unpacks it. The codes are Tesseract's (ISO 639-2/3
  with a script suffix where needed: `chi_sim`, `chi_tra`, `srp_latn`).
- Licence: Apache-2.0 (`LICENSE-Apache-2.0.txt`).
- Checksums are in `manifest.json`. The apps check the SHA-256 before a file is kept.
- Used by: Slop OCR, Slop PDF (Recognise text) and Slop AI Tools (OCR), through `aitools/ocr-tesseract.js` in the apps repo.
