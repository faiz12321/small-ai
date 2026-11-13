# Small AI

A small Windows app that runs small AI models on your own PC with one click: chat, summaries and rewrites. No Python, no terminal, no accounts. The app opens in your browser on a private local address.

Download the latest release from the Releases page, extract the whole ZIP into a writable folder, and run `SmallAI.exe`.

## Using it

Extract the whole release ZIP into a writable folder. Keep `engine` and `licenses` beside `SmallAI.exe`. Launch `SmallAI.exe`; it opens your default browser on a private loopback address. Windows 10/11 x64 and a current browser are required. This is an unsigned early release; Windows may warn about an unfamiliar app. No .NET or Visual C++ redistributable installer is bundled or required by the tested binaries. Existing Windows system libraries are still used.

Choose a model and click Install. Only the selected model is downloaded from Hugging Face. Qwen3 1.7B is the starter: about 1.83 GB. Granite 4.0 1B is about 1.74 GB. Working memory and total disk use are larger than the model file. Downloads are hash checked and can resume. Click Use after installation. The model is checked again before loading. Models are stored in `%APPDATA%\SmallAI-Prototype`.

Chat, summarize or rewrite short English text. Granite supports Chat and Rewrite only; use Qwen3 for summaries. The text limit is 6,000 characters and 1,400 input tokens. Output is limited to 256 tokens. Numeric and AM/PM warnings are partial checks, not proof of accuracy. Models can change names, pronouns, dates, conditions and meaning. Review every important fact. In regression testing, Qwen changed who checked an invoice; Granite sometimes reformatted dates. Short rewrites may repeat the source unchanged.

Stop cancels current work and unloads the engine. Remove asks before deleting the selected model. Clear text clears the browser fields. Quit stops the controller and engine. Closing the browser tab alone does not stop them. A fresh launch opens a fresh session.

Model use is local after installation. The app does not upload prompts, save chats, execute actions on your PC, or download extra tools. Installation needs Internet access; subsequent model use does not. The browser itself may have its own background network activity, outside this app.

## Honest limits

Small models are not ChatGPT-quality assistants. The app handles short English text; other languages are untested. This is an early release tested on Windows CI machines, not on your PC.

## Verification

Free Windows CI tests cover download/resume/hash failure, host/origin/session guards, size/token limits, two real models, rewrite/summary regression, Use/Stop cycles, cancellation during loading, and local model use with external controller network requests blocked. Actual Edge desktop/narrow and answer screenshots were inspected. CI Windows is not your physical PC; CPU speed, security software and browser setup may differ. This project is not a guarantee of factual correctness or a legal opinion.

## License

The original app code is under the MIT license (see `LICENSE`). The bundle contains only the controller, engine, instructions and necessary third-party notices. Models are downloaded separately under their own licenses (Apache 2.0). See `LICENSE-INVENTORY.md` for every bundled and downloaded component.
