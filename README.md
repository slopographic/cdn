# slopographic/cdn

Optional files for Slopographic apps (models, font packs, the video engine). Apps download these only when a person chooses them. Each folder has a versioned manifest.json with SHA-256 checksums, and apps check every file before use.

| File | Used by | Licence | Source |
|---|---|---|---|
| models/upscale/realesrgan-x4plus.onnx | Slop Upscale | BSD-3-Clause | xinntao/Real-ESRGAN |
| models/depth/depth-anything-v2-small.onnx | Slop Image to 3D | Apache-2.0 | depth-anything/Depth-Anything-V2-Small |
| models/whisper/whisper-tiny/* | Slop Transcribe, Slop AI Tools (speech to text): Whisper tiny (multilingual) | MIT (see models/whisper/whisper-tiny/SOURCE.md) | openai/whisper (ONNX export Xenova/whisper-tiny); the revision is in SOURCE.md |
| models/whisper/whisper-base/* | Slop Transcribe, Slop AI Tools (speech to text): Whisper base (multilingual) | MIT (see models/whisper/whisper-base/SOURCE.md) | openai/whisper (ONNX export onnx-community/whisper-base); the revision is in SOURCE.md |
| models/whisper/whisper-small/* | Slop Transcribe, Slop AI Tools (speech to text): Whisper small (multilingual) | MIT (see models/whisper/whisper-small/SOURCE.md) | openai/whisper (ONNX export onnx-community/whisper-small); the revision is in SOURCE.md |
| models/whisper/whisper-base-en/* | Slop Transcribe, Slop AI Tools (speech to text): Whisper base.en (English only) | MIT (see models/whisper/whisper-base-en/SOURCE.md) | openai/whisper (ONNX export onnx-community/whisper-base.en); the revision is in SOURCE.md |
| models/whisper/whisper-small-en/* | Slop Transcribe, Slop AI Tools (speech to text): Whisper small.en (English only) | MIT (see models/whisper/whisper-small-en/SOURCE.md) | openai/whisper (ONNX export onnx-community/whisper-small.en); the revision is in SOURCE.md |
| models/whisper/kb-whisper-base/* | Slop Transcribe, Slop AI Tools (speech to text): KB-Whisper base (Swedish) | Apache-2.0 (see models/whisper/kb-whisper-base/SOURCE.md) | KBLab/kb-whisper-base (decoder quantised to int8 here); the revision is in SOURCE.md |
| models/whisper/kb-whisper-small/* | Slop Transcribe, Slop AI Tools (speech to text): KB-Whisper small (Swedish) | Apache-2.0 (see models/whisper/kb-whisper-small/SOURCE.md) | KBLab/kb-whisper-small (decoder quantised to int8 here); the revision is in SOURCE.md |
| models/whisper/nb-whisper-base/* | Slop Transcribe, Slop AI Tools (speech to text): NB-Whisper base (Norwegian) | Apache-2.0 (see models/whisper/nb-whisper-base/SOURCE.md) | NbAiLab/nb-whisper-base via onnx-community/nb-whisper-base-ONNX (decoder quantised to int8 here); the revision is in SOURCE.md |
| models/whisper/nb-whisper-small/* | Slop Transcribe, Slop AI Tools (speech to text): NB-Whisper small (Norwegian) | Apache-2.0 (see models/whisper/nb-whisper-small/SOURCE.md) | NbAiLab/nb-whisper-small via onnx-community/nb-whisper-small-ONNX (decoder quantised to int8 here); the revision is in SOURCE.md |
| models/ocr/ppocr-det-v4/* | Slop OCR, Slop PDF (Recognise text), Slop AI Tools (OCR): the text-line detector every OCR model uses | Apache-2.0 (see models/ocr/ppocr-det-v4/SOURCE.md) | PaddlePaddle/PaddleOCR PP-OCRv4 mobile detector (ONNX export SWHL/RapidOCR); the revision is in SOURCE.md |
| models/ocr/ppocr-v6-small/* | Slop OCR, Slop PDF, Slop AI Tools: text recognition in Latin script with accents (Swedish, Polish, Czech, Romanian ...), Chinese and Japanese | Apache-2.0 (see models/ocr/ppocr-v6-small/SOURCE.md) | PaddlePaddle/PaddleOCR PP-OCRv6 small (ONNX export RapidAI/RapidOCR on ModelScope); the revision is in SOURCE.md |
| models/ocr/ppocr-v5-latin/* | Slop OCR, Slop PDF, Slop AI Tools: text recognition in Latin script (Swedish, German, French, Spanish and about 30 more) | Apache-2.0 (see models/ocr/ppocr-v5-latin/SOURCE.md) | PaddlePaddle/PaddleOCR PP-OCRv5 mobile (ONNX export RapidAI/RapidOCR on ModelScope); the revision is in SOURCE.md |
| models/ocr/ppocr-v5-cyrillic/* | Slop OCR, Slop PDF, Slop AI Tools: text recognition in Cyrillic script | Apache-2.0 (see models/ocr/ppocr-v5-cyrillic/SOURCE.md) | PaddlePaddle/PaddleOCR PP-OCRv5 mobile (ONNX export RapidAI/RapidOCR on ModelScope); the revision is in SOURCE.md |
| models/ocr/ppocr-v5-arabic/* | Slop OCR, Slop PDF, Slop AI Tools: text recognition in Arabic script (Arabic, Persian, Urdu ...) | Apache-2.0 (see models/ocr/ppocr-v5-arabic/SOURCE.md) | PaddlePaddle/PaddleOCR PP-OCRv5 mobile (ONNX export RapidAI/RapidOCR on ModelScope); the revision is in SOURCE.md |
| models/ocr/ppocr-v5-devanagari/* | Slop OCR, Slop PDF, Slop AI Tools: text recognition in Devanagari (Hindi, Marathi, Nepali ...) | Apache-2.0 (see models/ocr/ppocr-v5-devanagari/SOURCE.md) | PaddlePaddle/PaddleOCR PP-OCRv5 mobile (ONNX export RapidAI/RapidOCR on ModelScope); the revision is in SOURCE.md |
| models/ocr/ppocr-v5-korean/* | Slop OCR, Slop PDF, Slop AI Tools: text recognition in Korean | Apache-2.0 (see models/ocr/ppocr-v5-korean/SOURCE.md) | PaddlePaddle/PaddleOCR PP-OCRv5 mobile (ONNX export RapidAI/RapidOCR on ModelScope); the revision is in SOURCE.md |
| models/ocr/ppocr-v5-cjk/* | Slop OCR, Slop PDF, Slop AI Tools: text recognition in Chinese (simplified and traditional), Japanese and English | Apache-2.0 (see models/ocr/ppocr-v5-cjk/SOURCE.md) | PaddlePaddle/PaddleOCR PP-OCRv5 mobile (ONNX export RapidAI/RapidOCR on ModelScope); the revision is in SOURCE.md |
| models/ocr/ppocr-v5-greek/* | Slop OCR, Slop PDF, Slop AI Tools: text recognition in Greek | Apache-2.0 (see models/ocr/ppocr-v5-greek/SOURCE.md) | PaddlePaddle/PaddleOCR PP-OCRv5 mobile (ONNX export RapidAI/RapidOCR on ModelScope); the revision is in SOURCE.md |
| models/ocr/ppocr-v5-thai/* | Slop OCR, Slop PDF, Slop AI Tools: text recognition in Thai | Apache-2.0 (see models/ocr/ppocr-v5-thai/SOURCE.md) | PaddlePaddle/PaddleOCR PP-OCRv5 mobile (ONNX export RapidAI/RapidOCR on ModelScope); the revision is in SOURCE.md |
| models/ocr/tesseract-4.0.0-best-int/* | Slop OCR, Slop PDF (Recognise text), Slop AI Tools (OCR): Tesseract text recognition data, one file per language (95 languages) | Apache-2.0 (see models/ocr/tesseract-4.0.0-best-int/SOURCE.md) | tesseract-ocr/tessdata_best via the @tesseract.js-data npm packages 1.0.0; see models/ocr/tesseract-4.0.0-best-int/SOURCE.md |
| models/ocr/ppocr-v5-tamil/* | Slop OCR, Slop PDF, Slop AI Tools: text recognition in Tamil | Apache-2.0 (see models/ocr/ppocr-v5-tamil/SOURCE.md) | PaddlePaddle/PaddleOCR PP-OCRv5 mobile (ONNX export RapidAI/RapidOCR on ModelScope); the revision is in SOURCE.md |
| models/ocr/ppocr-v5-telugu/* | Slop OCR, Slop PDF, Slop AI Tools: text recognition in Telugu | Apache-2.0 (see models/ocr/ppocr-v5-telugu/SOURCE.md) | PaddlePaddle/PaddleOCR PP-OCRv5 mobile (ONNX export RapidAI/RapidOCR on ModelScope); the revision is in SOURCE.md |
| packs/google-fonts-1/v1/*.ttf | Slop fonts (Get more: Google Fonts set 1) | OFL-1.1 (each family's OFL.txt) | github.com/google/fonts at the commit in packs/google-fonts-1/v1/SOURCE.md |
| packs/google-fonts-2/v1/*.ttf | Slop fonts (Get more: Google Fonts set 2) | OFL-1.1 (each family's OFL.txt) | github.com/google/fonts at the commit in packs/google-fonts-2/v1/SOURCE.md |
| packs/google-fonts-3/v1/*.ttf | Slop fonts (Get more: Google Fonts set 3) | OFL-1.1 (each family's OFL.txt) | github.com/google/fonts at the commit in packs/google-fonts-3/v1/SOURCE.md |
| packs/google-fonts-4/v1/*.ttf | Slop fonts (Get more: Google Fonts set 4) | OFL-1.1 (each family's OFL.txt) | github.com/google/fonts at the commit in packs/google-fonts-4/v1/SOURCE.md |
| packs/google-fonts-5/v1/*.ttf | Slop fonts (Get more: Google Fonts set 5) | OFL-1.1 (each family's OFL.txt) | github.com/google/fonts at the commit in packs/google-fonts-5/v1/SOURCE.md |
| packs/metric-compatible/v1/*.ttf | Slop fonts (Get more: Calibri, Cambria, Arial, Times New Roman and Courier New compatible) | OFL-1.1 (each family's OFL.txt) | github.com/google/fonts at the commit in packs/metric-compatible/v1/SOURCE.md |
| packs/barlow/v1/*.ttf | Slop fonts (Get more: Barlow and Barlow Condensed) | OFL-1.1 (see packs/barlow/v1/OFL.txt) | google/fonts ofl/barlow; see packs/barlow/v1/SOURCE.md |
| packs/noto-sans/v1/* | Slop fonts (language pack: Latin, Greek and Cyrillic (Noto Sans)) | OFL-1.1 (see packs/noto-sans/v1/OFL.txt) | notofonts; see packs/noto-sans/v1/SOURCE.md |
| packs/noto-arabic/v1/* | Slop fonts (language pack: Arabic (Noto Sans Arabic)) | OFL-1.1 (see packs/noto-arabic/v1/OFL.txt) | notofonts; see packs/noto-arabic/v1/SOURCE.md |
| packs/noto-hebrew/v1/* | Slop fonts (language pack: Hebrew (Noto Sans Hebrew)) | OFL-1.1 (see packs/noto-hebrew/v1/OFL.txt) | notofonts; see packs/noto-hebrew/v1/SOURCE.md |
| packs/noto-devanagari/v1/* | Slop fonts (language pack: Devanagari (Noto Sans Devanagari)) | OFL-1.1 (see packs/noto-devanagari/v1/OFL.txt) | notofonts; see packs/noto-devanagari/v1/SOURCE.md |
| packs/noto-bengali/v1/* | Slop fonts (language pack: Bengali (Noto Sans Bengali)) | OFL-1.1 (see packs/noto-bengali/v1/OFL.txt) | notofonts; see packs/noto-bengali/v1/SOURCE.md |
| packs/noto-tamil/v1/* | Slop fonts (language pack: Tamil (Noto Sans Tamil)) | OFL-1.1 (see packs/noto-tamil/v1/OFL.txt) | notofonts; see packs/noto-tamil/v1/SOURCE.md |
| packs/noto-telugu/v1/* | Slop fonts (language pack: Telugu (Noto Sans Telugu)) | OFL-1.1 (see packs/noto-telugu/v1/OFL.txt) | notofonts; see packs/noto-telugu/v1/SOURCE.md |
| packs/noto-kannada/v1/* | Slop fonts (language pack: Kannada (Noto Sans Kannada)) | OFL-1.1 (see packs/noto-kannada/v1/OFL.txt) | notofonts; see packs/noto-kannada/v1/SOURCE.md |
| packs/noto-malayalam/v1/* | Slop fonts (language pack: Malayalam (Noto Sans Malayalam)) | OFL-1.1 (see packs/noto-malayalam/v1/OFL.txt) | notofonts; see packs/noto-malayalam/v1/SOURCE.md |
| packs/noto-gujarati/v1/* | Slop fonts (language pack: Gujarati (Noto Sans Gujarati)) | OFL-1.1 (see packs/noto-gujarati/v1/OFL.txt) | notofonts; see packs/noto-gujarati/v1/SOURCE.md |
| packs/noto-gurmukhi/v1/* | Slop fonts (language pack: Gurmukhi (Noto Sans Gurmukhi)) | OFL-1.1 (see packs/noto-gurmukhi/v1/OFL.txt) | notofonts; see packs/noto-gurmukhi/v1/SOURCE.md |
| packs/noto-oriya/v1/* | Slop fonts (language pack: Odia (Noto Sans Oriya)) | OFL-1.1 (see packs/noto-oriya/v1/OFL.txt) | notofonts; see packs/noto-oriya/v1/SOURCE.md |
| packs/noto-sinhala/v1/* | Slop fonts (language pack: Sinhala (Noto Sans Sinhala)) | OFL-1.1 (see packs/noto-sinhala/v1/OFL.txt) | notofonts; see packs/noto-sinhala/v1/SOURCE.md |
| packs/noto-thai/v1/* | Slop fonts (language pack: Thai (Noto Sans Thai)) | OFL-1.1 (see packs/noto-thai/v1/OFL.txt) | notofonts; see packs/noto-thai/v1/SOURCE.md |
| packs/noto-lao/v1/* | Slop fonts (language pack: Lao (Noto Sans Lao)) | OFL-1.1 (see packs/noto-lao/v1/OFL.txt) | notofonts; see packs/noto-lao/v1/SOURCE.md |
| packs/noto-khmer/v1/* | Slop fonts (language pack: Khmer (Noto Sans Khmer)) | OFL-1.1 (see packs/noto-khmer/v1/OFL.txt) | notofonts; see packs/noto-khmer/v1/SOURCE.md |
| packs/noto-myanmar/v1/* | Slop fonts (language pack: Myanmar (Noto Sans Myanmar)) | OFL-1.1 (see packs/noto-myanmar/v1/OFL.txt) | notofonts; see packs/noto-myanmar/v1/SOURCE.md |
| packs/noto-georgian/v1/* | Slop fonts (language pack: Georgian (Noto Sans Georgian)) | OFL-1.1 (see packs/noto-georgian/v1/OFL.txt) | notofonts; see packs/noto-georgian/v1/SOURCE.md |
| packs/noto-armenian/v1/* | Slop fonts (language pack: Armenian (Noto Sans Armenian)) | OFL-1.1 (see packs/noto-armenian/v1/OFL.txt) | notofonts; see packs/noto-armenian/v1/SOURCE.md |
| packs/noto-ethiopic/v1/* | Slop fonts (language pack: Ethiopic (Noto Sans Ethiopic)) | OFL-1.1 (see packs/noto-ethiopic/v1/OFL.txt) | notofonts; see packs/noto-ethiopic/v1/SOURCE.md |
| packs/noto-tibetan/v1/* | Slop fonts (language pack: Tibetan (Noto Serif Tibetan)) | OFL-1.1 (see packs/noto-tibetan/v1/OFL.txt) | notofonts; see packs/noto-tibetan/v1/SOURCE.md |
| packs/noto-thaana/v1/* | Slop fonts (language pack: Thaana (Noto Sans Thaana)) | OFL-1.1 (see packs/noto-thaana/v1/OFL.txt) | notofonts; see packs/noto-thaana/v1/SOURCE.md |
| packs/noto-mongolian/v1/* | Slop fonts (language pack: Mongolian (Noto Sans Mongolian)) | OFL-1.1 (see packs/noto-mongolian/v1/OFL.txt) | notofonts; see packs/noto-mongolian/v1/SOURCE.md |
| packs/noto-cherokee/v1/* | Slop fonts (language pack: Cherokee (Noto Sans Cherokee)) | OFL-1.1 (see packs/noto-cherokee/v1/OFL.txt) | notofonts; see packs/noto-cherokee/v1/SOURCE.md |
| packs/noto-sc/v1/* | Slop fonts (language pack: Chinese, simplified (Noto Sans SC)) | OFL-1.1 (see packs/noto-sc/v1/OFL.txt) | notofonts; see packs/noto-sc/v1/SOURCE.md |
| packs/noto-tc/v1/* | Slop fonts (language pack: Chinese, traditional (Noto Sans TC)) | OFL-1.1 (see packs/noto-tc/v1/OFL.txt) | notofonts; see packs/noto-tc/v1/SOURCE.md |
| packs/noto-jp/v1/* | Slop fonts (language pack: Japanese (Noto Sans JP)) | OFL-1.1 (see packs/noto-jp/v1/OFL.txt) | notofonts; see packs/noto-jp/v1/SOURCE.md |
| packs/noto-kr/v1/* | Slop fonts (language pack: Korean (Noto Sans KR)) | OFL-1.1 (see packs/noto-kr/v1/OFL.txt) | notofonts; see packs/noto-kr/v1/SOURCE.md |
| engines/ffmpeg/0.12.10/ffmpeg-core.wasm (and .js) | Slop Convert (video conversions) | GPL-2.0-or-later (see engines/ffmpeg/0.12.10/LICENSE-GPL-2.0.txt) | ffmpeg.wasm 0.12.10 and FFmpeg; see engines/ffmpeg/0.12.10/SOURCE.md |
| engines/libraw/libraw-wasm-1.6.0/libraw.wasm (and .js) | PhotoSlop, Slop Gallery, Slop Resize, File convert (camera RAW files) | LGPL-2.1 or CDDL-1.0 (LibRaw), MIT (Little CMS), ISC (wrapper); see engines/libraw/libraw-wasm-1.6.0/SOURCE.md | libraw-wasm 1.6.0 (LibRaw 0.22.1); see engines/libraw/libraw-wasm-1.6.0/SOURCE.md |
| engines/libheif/libheif-js-1.23.5/libheif.wasm (and .js) | File convert (HEIC and HEIF photos) | LGPL-3.0 (libheif, libde265); see engines/libheif/libheif-js-1.23.5/SOURCE.md | libheif-js 1.23.5 (libheif, libde265 1.0.15); see engines/libheif/libheif-js-1.23.5/SOURCE.md |

Files over 95 MB are stored as `.partN` pieces (GitHub refuses files over 100 MB); the manifest lists each piece and the joined file with their SHA-256, and the apps check both.

SHA-256 values are listed in the apps' model index files and in each folder's manifest.json (for example engines/ffmpeg/0.12.10/manifest.json).
