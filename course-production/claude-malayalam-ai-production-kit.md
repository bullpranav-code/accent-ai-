# Accent Claude Skills Course — AI Production Kit
## Purpose
Prepare a launch-ready Malayalam-narrated course aligned to Accent — Choice Is Yours and the existing Accent Sales Program (ASP).

## Production requirements
- Narration language: Malayalam (മലയാളം), native script, clear instructional Kerala/Malayalam delivery.
- Brand: Accent green palette; wordmark should read “Accent”; leaf above the “t” should follow the supplied official logo/art. Do not fake a logo by changing type glyphs if the exact asset exists.
- Claude branding: use official Claude mark only in relevant lesson places; Accent remains the course provider. Avoid implying Anthropic endorsement.
- Closing: reuse the end card extracted from the Sales Basics reference, not a newly approximated logo.
- Every lesson: one Malayalam narration track, subtitle captions matched to narration, appropriate screen visuals/steps, a lesson label, and standard Accent/ASP closing card.
- Quality: listen to the full audio; check Malayalam pronunciation (especially mixed-language terms); captions must match narration; ensure audio track exists, levels are consistent, video has no black/frozen sections, and final card is present.
- Cost: free/open-source tools first; no paid generations without explicit approval.

## Recommended zero-paid workflow
1. Script: write accurate, conversational Malayalam scripts, preserving product names such as Claude, Projects, Artifacts, prompts, PDFs, Excel.
2. Voice audition: compare Subformer browser Malayalam TTS (offline/local after model download; WAV export, but synthetic quality) and TTS.ai free demo (MP3/WAV export; terms say free tier is personal use, so do not use it commercially until terms are confirmed). For production/commercial course, prefer a self-hosted open-source model.
3. Open-source route: AI4Bharat IndicF5 supports Malayalam, takes text plus a reference audio and its transcript, and can generate WAV; setup has Python/model/runtime requirements and is heavier. Alternative: vexyl-tts wraps Indic Parler-TTS and lists ml-IN Malayalam; requires Python/macOS/Linux and ~6 GB disk, optional NVIDIA GPU.
4. Captions: make caption text from final approved Malayalam script and time-align it to final audio; do not guess timings from English.
5. Render with FFmpeg: combine slides/visual walkthrough footage, Malayalam narration, captions, and the exact extracted ASP end card.
6. Inspect: use ffprobe to confirm video+audio streams and test beginning/middle/end frames; listen through all lesson audio. Package only final-ready MP4s, SRTs, and scripts.

## Research links
- AI4Bharat IndicF5: https://github.com/AI4Bharat/IndicF5
- AI4Bharat Indic-TTS: https://github.com/AI4Bharat/Indic-TTS
- vexyl-tts (Indic Parler-TTS wrapper; 22 Indic languages incl. Malayalam): https://github.com/vexyl-ai/vexyl-tts
- IndicF5 overview: https://github.com/ST-SARAVANAPRIYAN/IndicF5-Neo
- Subformer Malayalam TTS: https://subformer.com/en-US/text-to-speech/malayalam
- TTS.ai Malayalam TTS (check free-tier license before commercial use): https://tts.ai/text-to-speech/malayalam/
- Fliki Malayalam voices: https://fliki.ai/voices/malayalam
- TTS Maker: https://ttsmaker.in/

## Important limitation
This production kit is a workflow and quality gate, not a claim that narrated final videos have been produced. Do not label the existing silent exports as final.
