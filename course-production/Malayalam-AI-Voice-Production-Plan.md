# Accent Claude Skills Course — Malayalam AI Production Kit

## Goal
Produce eight final course lessons with Malayalam AI narration, on-screen learning visuals, synchronized captions, and the same Accent Sales Program outro. Keep Accent — Choice Is Yours as the primary brand. Use the leaf motif above the t in the approved Accent artwork. Use Claude branding only where the lesson teaches Claude; do not imply Anthropic endorsement.

## Current state
- The existing eight visual files in the production-v2 folder have no audio streams. They are not final.
- Malayalam narration drafts for lessons 1–8 are saved in `Malayalam_Narration_Scripts.md` locally in the working package; use as script source then have the voice output reviewed by a native speaker.
- No paid generation was started.
- GitHub draft branch `claude-course-draft` created in this repository. It contains the TTS research and integration proposal. The live `main` branch is unchanged.

## Recommended free-first voice workflow
1. **Best open-source candidate to test first: AI4Bharat Indic-Speak** — the IndicF5 model page now points users toward Indic-Speak as a newer model supporting 22 Indian languages. Confirm current Malayalam support, actual demo availability, license/model conditions, and export path before basing production on it. https://huggingface.co/ai4bharat/IndicF5
2. **Open-source reference-guided fallback: AI4Bharat IndicF5** — Malayalam is explicitly listed among 11 languages; generation uses text, reference audio, and an exact reference transcript. Public model page says a user must agree to conditions to access model files. https://github.com/AI4Bharat/IndicF5 and https://huggingface.co/ai4bharat/IndicF5
3. **One-command local server option: vexyl-tts** — wraps AI4Bharat Indic Parler-TTS, explicitly lists `ml-IN` Malayalam, supports REST and WebSocket, Python 3.10+ on macOS/Linux, about 6 GB disk; GPU optional. https://github.com/vexyl-ai/vexyl-tts
4. **Browser-based quick audition: Subformer Malayalam** — free, no sign-up; model downloads ~60 MB, inference runs locally in-browser and can save WAV. Its page says the open-source voice sounds synthetic, so use only after listening and acceptance. https://subformer.com/en-US/text-to-speech/malayalam
5. **Sonex Labs / Pāṇini TTS** — free browser preview without an account up to 220 characters; free sign-up states 10,000 characters and downloadable audio. Provider says free voice-over may be used on monetised video/social channels; verify current terms, supported download, and whole-course limits before production. https://docs.sonexlabs.com/text-to-speech/malayalam/voice-over
6. **Avoid TTS.ai free tier for the commercial course** — its current terms say free-tier output is personal/non-commercial only, including business products/apps. https://tts.ai/terms/
7. **TTS Maker / Fliki** can be trial candidates but verify current terms, Malayalam voice quality, export limits, and business/commercial use for each voice/plan before relying on outputs. https://ttsmaker.in/ and https://fliki.ai/voices/malayalam

## Quality gates
- Generate a 30–45 sec Malayalam sample from Lesson 01 first; listen on phone and verify Claude/Projects/Artifacts pronunciation.
- One consistent native-sounding Malayalam voice throughout; natural pauses, not word-by-word stilted delivery.
- Captions must match the final spoken Malayalam and align to actual timings. Do not use English timings for Malayalam audio.
- Keep code/Claude interface examples readable and do not fabricate Claude interface details.
- Add the exact ASP closing card; inspect the last frames of each complete file after muxing.
- Verify with ffprobe that every final MP4 has video AND audio streams; check duration, loudness, first/middle/last frames, caption timing and iOS playback.
- Do not send an interim or silent video ZIP. Share only the final validated course package.

## Integration
- A draft tile/integration proposal is at `course-production/claude-course-integration-proposal.md` on branch `claude-course-draft`.
- Integrate a Claude Skills Course tile alongside Accent Sales Program in the existing single-page `index.html`, with a dedicated lesson list/player and downloadable assets. Do not replace the existing page or payment logic.
- Store this branch for review; do not deploy/push to main until the narrated video package is fully validated.
