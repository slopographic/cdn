# ppocr-v6-small

- PaddleOCR PP-OCRv6 small text recognition (`PP-OCRv6_small_rec`, 5.2M parameters) by PaddlePaddle
  (https://github.com/PaddlePaddle/PaddleOCR, https://huggingface.co/PaddlePaddle/PP-OCRv6_small_rec), Apache-2.0. One model
  for Latin-script languages with their accents (Swedish å ä ö, Polish, Czech, Romanian, Latvian ...), Chinese (simplified
  and traditional) and Japanese.
- Files from the RapidOCR model hub on ModelScope (https://www.modelscope.cn/models/RapidAI/RapidOCR) at tag `v3.10.0`: `onnx/PP-OCRv6/rec/PP-OCRv6_rec_small.onnx` (the ONNX export
  RapidOCR publishes, unchanged) and its character dictionary `paddle/PP-OCRv6/rec/PP-OCRv6_rec_small/ppocrv6_dict.txt` (unchanged).
- Input: 3 x 48 x width, BGR, (x / 255 - 0.5) / 0.5. Output: CTC over the blank, the dictionary's lines in order and a
  space. Run and checked on rendered text in onnxruntime-web 1.30 (WebAssembly) before upload.
- The text lines are found by the PP-OCRv4 mobile detector (`models/ocr/ppocr-det-v4/`), the same for every script.
- Licence: Apache-2.0 (`LICENSE-Apache-2.0.txt`, PaddleOCR's licence text).
- Used by: Slop OCR, Slop PDF (Recognise text) and Slop AI Tools (OCR), through `aitools/ocr-models.js` in the apps repo.
