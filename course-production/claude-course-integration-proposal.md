# Claude Course Integration Proposal (Draft; not deployed)

## Destination
Integrate a Claude Skills Course tile alongside the existing Accent Sales Program on the Accent AI home dashboard. Do not create a separate app or replace current products.

## Tile copy
Claude Skills Course
Practical AI skills in Malayalam
Lessons • Guided demonstrations • Practice activities

## Course structure
01. Claude-ൽ തുടങ്ങാം (Getting started with Claude)
02. നല്ല Prompt എങ്ങനെ എഴുതാം (The brief prompt method)
03. എഴുതുക, ചിന്തിക്കുക, മെച്ചപ്പെടുത്തുക (Write, think and improve)
04. Documents, PDFs, spreadsheets എന്നിവയുമായി പ്രവർത്തിക്കുക
05. Research and fact-checking
06. Projects & context
07. Artifacts ഉപയോഗിച്ച് സൃഷ്ടിക്കുക
08. Repeatable workflows നിർമ്മിക്കുക
09. Sales & marketing workflow with Claude
10. Responsible AI, privacy, verification and advanced workflow

## Lesson experience
- Malayalam narration with selectable Malayalam captions (SRT / embedded captions).
- Keep official Claude logo/mark only in relevant learning areas. Accent remains the course brand.
- Downloadable prompt templates, practical exercise, quick check and answer feedback.
- Use exact existing ASP end card at the end of each lesson video.
- Course tile is UI-only until final MP4s and learning resources are validated and hosted.

## Technical implementation checklist
1. Store final MP4/SRT/resource URLs in a data array for lesson cards.
2. Add a dedicated claude-course screen and back navigation consistent with existing switchTab routing.
3. Add lesson player with native HTML video controls and captions track.
4. Ensure responsive/mobile layout and accessible labels.
5. Never put API keys in client-side HTML; any server API must use a backend.
6. QA links, caption availability, playback on iOS Safari, and session persistence.
7. Do not change payment/access rules for ASP.

## Status
Proposal only. No live page was changed. This file is on the claude-course-draft branch for review.
