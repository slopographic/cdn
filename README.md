# slopographic/cdn

Optional model files for Slopographic apps. Apps download these only when a person chooses them.

| File | Used by | Licence | Source |
|---|---|---|---|
| models/upscale/realesrgan-x4plus.onnx | Slop Upscale | BSD-3-Clause | xinntao/Real-ESRGAN |
| models/depth/depth-anything-v2-small.onnx | Slop Image to 3D | Apache-2.0 | depth-anything/Depth-Anything-V2-Small |
| engines/ffmpeg/0.12.10/ffmpeg-core.wasm (and .js) | Slop Convert (video conversions) | GPL-2.0-or-later (see engines/ffmpeg/0.12.10/LICENSE-GPL-2.0.txt) | ffmpeg.wasm 0.12.10 and FFmpeg; see engines/ffmpeg/0.12.10/SOURCE.md |

SHA-256 values are listed in the apps' model index files and in each folder's manifest.json (for example engines/ffmpeg/0.12.10/manifest.json).
