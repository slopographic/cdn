# ppocr-det-v4

- PaddleOCR PP-OCRv4 mobile text detection (DB), by PaddlePaddle (https://github.com/PaddlePaddle/PaddleOCR), Apache-2.0.
- File: `PP-OCRv4/ch_PP-OCRv4_det_infer.onnx` from https://huggingface.co/SWHL/RapidOCR at revision
  `1cfba2e90fc938db55889873735088de210cc173` (RapidOCR's ONNX export), unchanged. The same file Slop OCR has used since
  its first version; it finds text lines in any script.
- Licence: Apache-2.0 (`LICENSE-Apache-2.0.txt`, PaddleOCR's licence text).
- Used by: every OCR recognition model under `models/ocr/` (Slop OCR, Slop PDF, Slop AI Tools), through `aitools/ocr-models.js`.
