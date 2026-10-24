# whisper-base-en

- Source: https://huggingface.co/onnx-community/whisper-base.en at revision `51eefc0af78b103839eda9e7e4f4186acc6517fe` (files from `onnx/` and the repository root).
- ONNX export of openai/whisper-base.en (English only) by onnx-community (int8), unchanged.
- Licence: MIT (`LICENSE-MIT-openai-whisper.txt`). The Whisper weights are by OpenAI (github.com/openai/whisper).
- Files over 95 MB are split into `.partN` pieces (GitHub refuses files over 100 MB). The apps download the
  pieces in order, check each piece's SHA-256, join them and check the whole file's SHA-256 (all in `manifest.json`).
- Used by: Slop Transcribe and Slop AI Tools (Speech to text), through `aitools/speech-models.js` in the apps repo.
