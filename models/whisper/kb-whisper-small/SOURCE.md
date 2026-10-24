# kb-whisper-small

- Source: https://huggingface.co/KBLab/kb-whisper-small at revision `3564d61a42fc210ceaa55a22a96dd64478959c78` (files from `onnx/` and the repository root).
- KB-Whisper small by KBLab (the National Library of Sweden), fine-tuned on Swedish. Encoder: onnx/encoder_model_quantized.onnx, unchanged. Decoder: onnx/decoder_model_merged.onnx (fp32) quantised to int8 here.
- Quantisation (done for Slopographic, because the published int8 merged decoders of this model are about three times
  the size they need to be): onnxruntime 1.31 `quantize_dynamic` (int8 weights, per tensor, MatMulInteger, both If branches),
  then the tied output projection was pointed at the int8 token table and the unused fp32 copy dropped. Run and checked
  on recorded speech in onnxruntime-web 1.30 (WebAssembly) before upload.
- Licence: Apache-2.0 (`LICENSE-Apache-2.0.txt`). Fine-tuned from OpenAI Whisper (MIT).
- Files over 95 MB are split into `.partN` pieces (GitHub refuses files over 100 MB). The apps download the
  pieces in order, check each piece's SHA-256, join them and check the whole file's SHA-256 (all in `manifest.json`).
- Used by: Slop Transcribe and Slop AI Tools (Speech to text), through `aitools/speech-models.js` in the apps repo.
