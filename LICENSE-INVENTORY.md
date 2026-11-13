# License inventory

## Shipped files

- `SmallAI.exe`: original Go controller with embedded original HTML/CSS; no external Go modules. Go runtime, BSD 3-clause (`licenses/Go-BSD.txt`). Original app code is distributed under the MIT license (see `LICENSE` in the source repository).
- `engine/llama-server.exe`: llama.cpp CPU server, pinned commit `47c786924ad1ab7e91da2cdc72fcdb563780c2bd` (b9999), MIT (`llama-MIT.txt`). Built with GNU MinGW, statically linked compiler runtimes, no separate toolchain or Microsoft redistributable DLLs. Import inventory: ADVAPI32, KERNEL32, msvcrt, SHELL32, WS2_32, all existing Windows DLLs. These DLLs are not shipped.
- Header components in the engine: cpp-httplib MIT (`cpp-httplib-MIT.txt`); nlohmann JSON MIT (`nlohmann-json-MIT.txt`); subprocess.h Unlicense (`subprocess-Unlicense.txt`); stb_image public-domain/MIT dual notice (`stb-image-notice.txt`); miniaudio public-domain/MIT-0 dual notice (`miniaudio-notice.txt`). llama.cpp/ggml retains its upstream copyright notices in `llama-MIT.txt`. YaRN rotary-position code in ggml CPU ops is MIT, copyright 2023 Jeffrey Quesnelle and Bowen Peng (`yarn-MIT.txt`). LLAMAFILE CPU matrix kernels are included under MIT, copyright 2024 Mozilla Foundation (`llamafile-MIT.txt`); KleidiAI is disabled and not included.
- GNU libgcc/libstdc++ runtime portions: GPLv3 with GCC Runtime Library Exception 3.1 (`GNU-COPYING3`, `GNU-COPYING.RUNTIME`). The exception permits covered independent code under its own terms after eligible compilation. This engine was compiled with GCC, without proprietary compilation plugins.
- MinGW-w64 runtime portions: project and component notices, including Zope-style redistribution terms, BSD and permissive notices (`MinGW-runtime.txt`). The consolidated runtime notice is retained because generic project COPYING alone is insufficient for binary redistribution. Its upstream text flags an unclear historical Cephes math permission and LGPL Wine headers; exact linked-object attribution has not been verified. Do not treat this as a zero-risk legal clearance.
- README and this inventory: instructions and audit notes. No images, web fonts, CDN assets, stock server web UI, extra tools, model files, Microsoft redistributables, installer or telemetry are bundled.

## Models downloaded separately

- Qwen/Qwen3-1.7B-GGUF, pinned repository revision `90862c4`: Apache 2.0 (`Qwen3-Apache.txt`).
- IBM Granite 4.0 1B GGUF, pinned revision `b27c2fe3f211b7f44e80fa620177aea371099aaa`: Apache 2.0 (`Granite-Apache.txt`), upstream converted-model card (`Granite-model-card.md`). Source model card: https://huggingface.co/ibm-granite/granite-4.0-1b . Quantized-model card: https://huggingface.co/ibm-granite/granite-4.0-1b-GGUF .

These model notices describe the only offered downloads; weights are not in the ZIP. No commercial model subscription or runtime installer is needed. Notices are not unnecessary extra software. This inventory is an engineering review, not a guarantee of zero legal risk. The owner approved public distribution and selected the MIT license for the original app code.

## Sources

https://github.com/ggml-org/llama.cpp/tree/47c786924ad1ab7e91da2cdc72fcdb563780c2bd
https://go.dev/LICENSE
https://gcc.gnu.org/onlinedocs/libstdc++/manual/license.html
https://raw.githubusercontent.com/mingw-w64/mingw-w64/master/COPYING.MinGW-w64-runtime/COPYING.MinGW-w64-runtime.txt

https://raw.githubusercontent.com/jquesnelle/yarn/master/LICENSE
