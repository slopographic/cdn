# whisper-base

- Source: https://huggingface.co/onnx-community/whisper-base at revision `1846881b6b3a3024392c1eea3ad983695bc23925` (files from `onnx/` and the repository root).
- ONNX export of openai/whisper-base by onnx-community (int8), unchanged.
- Licence: MIT (`LICENSE-MIT-openai-whisper.txt`). The Whisper weights are by OpenAI (github.com/openai/whisper).
- Files over 95 MB are split into `.partN` pieces (GitHub refuses files over 100 MB). The apps download the
  pieces in order, check each piece's SHA-256, join them and check the whole file's SHA-256 (all in `manifest.json`).
- Used by: Slop Transcribe and Slop AI Tools (Speech to text), through `aitools/speech-models.js` in the apps repo.
