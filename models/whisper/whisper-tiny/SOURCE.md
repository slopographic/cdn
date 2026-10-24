# whisper-tiny

- Source: https://huggingface.co/Xenova/whisper-tiny at revision `5332fcc35e32a33b86612b9a57a89be7906102b1` (files from `onnx/` and the repository root).
- ONNX export of openai/whisper-tiny by Xenova (int8 encoder and merged decoder), unchanged. config.json and generation_config.json from onnx-community/whisper-tiny at ff4177021cc41f7db950912b73ea4fdf7d01d8e7 (the same model).
- Licence: MIT (`LICENSE-MIT-openai-whisper.txt`). The Whisper weights are by OpenAI (github.com/openai/whisper).
- Files over 95 MB are split into `.partN` pieces (GitHub refuses files over 100 MB). The apps download the
  pieces in order, check each piece's SHA-256, join them and check the whole file's SHA-256 (all in `manifest.json`).
- Used by: Slop Transcribe and Slop AI Tools (Speech to text), through `aitools/speech-models.js` in the apps repo.
