# ppocr-v5-telugu

- PaddleOCR PP-OCRv5 mobile text recognition for Telugu. Upstream model `te_PP-OCRv5_mobile_rec` by PaddlePaddle
  (https://github.com/PaddlePaddle/PaddleOCR), Apache-2.0.
- Files from the RapidOCR model hub on ModelScope (https://www.modelscope.cn/models/RapidAI/RapidOCR) at tag `v3.10.0`: `onnx/PP-OCRv5/rec/te_PP-OCRv5_rec_mobile.onnx` (the ONNX export
  RapidOCR publishes, unchanged) and its character dictionary `paddle/PP-OCRv5/rec/te_PP-OCRv5_rec_mobile/ppocrv5_te_dict.txt` (unchanged).
- Input: 3 x 48 x width, BGR, (x / 255 - 0.5) / 0.5. Output: CTC over the blank, the dictionary's lines in order and a
  space (1831 bytes of dictionary). Run and checked on rendered text in onnxruntime-web 1.30 (WebAssembly) before upload.
- The text lines are found by the PP-OCRv4 mobile detector (`models/ocr/ppocr-det-v4/`), the same for every script.
- Licence: Apache-2.0 (`LICENSE-Apache-2.0.txt`, PaddleOCR's licence text).
- Used by: Slop OCR, Slop PDF (Recognise text) and Slop AI Tools (OCR), through `aitools/ocr-models.js` in the apps repo.
