# Malayalam TTS Tool Research (27 Oct 2026)

## Requirement
Accent Claude Skills Course needs AI-generated Malayalam narration, with Accent/ASP branded visuals, synchronized captions, and the exact ASP outro. Prefer free and commercial-use-safe outputs. Do not spend paid credits without approval.

## Candidate tools

### 1. AI4Bharat IndicF5 — preferred open-source production route
- GitHub: https://github.com/AI4Bharat/IndicF5
- Model card: https://huggingface.co/ai4bharat/IndicF5
- Malayalam is explicitly supported among 11 Indian languages. The model accepts text, reference prompt audio, and a transcript of that reference. This can help voice consistency, but may be more technical and needs local compute/runtime. Model access may require agreeing to its Hugging Face conditions. Check the model license and source dataset/voice permissions before using for a commercial course.

### 2. vexyl-tts — open-source server alternative
- GitHub: https://github.com/vexyl-ai/vexyl-tts
- Wraps AI4Bharat Indic Parler-TTS; explicitly lists `ml-IN` Malayalam.
- Requires Python 3.10+, macOS or Linux, about 6 GB disk space; NVIDIA GPU is optional. Good if Accent wants a reusable TTS service, but is a setup project rather than a one-click web tool.

### 3. Subformer Malayalam TTS — fastest local-browser test
- https://subformer.com/en-US/text-to-speech/malayalam
- Free/no sign-up, about 60 MB model download, on-device WebAssembly inference, can save WAV, offline after model/cache download. It says the free open-source voice sounds noticeably synthetic and is best for drafts/previews. Test quality against native Malayalam listening before considering launch audio.

### 4. TTS.ai Malayalam — easy prototype only, not for the commercial course on free tier
- https://tts.ai/text-to-speech/malayalam/
- Browser offers free Malayalam generation and MP3/WAV export; free 500 characters per generation and limited free character allowance. Current terms effective 14 Sep 2026 say free-tier generated audio is personal/non-commercial use only, including products/apps offered for sale and business use. Therefore do not use free-tier output in the Accent course unless terms change or a commercial license is obtained.
- Terms: https://tts.ai/terms/

### 5. Fliki — convenient but check current plan/export limits
- https://fliki.ai/voices/malayalam
- Six listed Malayalam voices and a text-to-video workflow. The page shows a free tier but says royalty-free on paid plans; do not assume the free tier grants commercial rights for launch content without confirming terms.

### 6. TTS Maker — quick preview
- https://ttsmaker.in/
- Page states free voices, MP3 export and Malayalam language. Anonymous limit shown as 500 characters/request and 2,000/day; free login raises limits. Before using for a paid course, verify voice-by-voice commercial rights and attribution.

## Recommended workflow
1. Translate/adapt the English source into natural Malayalam script, retaining essential terms such as Claude, Projects and Artifacts in a pronunciation-friendly form; avoid Manglish for core Malayalam narration.
2. Prototype one 30–45 second sample in Subformer and compare to a Malayalam speaker/listener. For production prefer AI4Bharat IndicF5 or a self-hosted Indic-Parler wrapper after compute and commercial model conditions are verified.
3. Use the chosen narration voice consistently. Split long scripts into scene-sized clips and preserve pauses around terms and transitions.
4. Generate captions from the final Malayalam script and time-align to the finalized audio; validate proper spelling and timing, not just automatic word alignment.
5. Render/encode using FFmpeg: original lesson visuals + Malayalam audio + captions + exact ASP end card. Check audio/video streams with ffprobe, loudness, first/middle/last frames, mobile playback and all captions.
6. Package final MP4 + SRT + script/resource downloads. No silent draft may be labeled final.

## Current implementation state
- No paid voice generation was submitted.
- The live branch was not changed.
- A draft branch `claude-course-draft` exists with this research and the course integration proposal.
- Existing eight visual exports still need Malayalam narration and timing/quality validation. The closing card has been extracted from the ASP reference, but the exact visual should be rechecked at the tail of every finished file after final muxing.
