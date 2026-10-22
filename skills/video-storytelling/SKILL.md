---
name: video-storytelling
description: Turn personal footage into a narrated video through source discovery, visual and audio analysis, an editing proposal, approved narration, voice previews, and reviewed cuts. Use for travel, everyday stories, events, and other footage-based edits, including material in iCloud Photos or iCloud Drive.
---

# Video Storytelling

Build a story from the user's actual material. Keep language, voice, platform, and visual style project-specific. This skill is a workflow for an agent with media tools, not a bundled editor or cloud-storage connector.

## Start or resume

Read the project's private `project.md` when present. Reuse approved choices and completed assets. Establish only missing decisions that affect the next step: source scope, intended story/audience, approximate duration, format, narration and subtitle languages, and voice preference. Do useful authorized discovery while awaiting optional preferences.

Keep source speech language, narration language, subtitle languages, and conversation language separate. Detect source languages as evidence permits; ask for output language when unclear. Never infer nationality, learner identity, or desired bilingual captions from language alone.

Use an output directory outside this installed skill and outside any public repository. Record approvals against exact versions; approval of a plan is not approval of newly written narration. Existing explicit approvals remain valid unless the relevant content changes.

Before promising an edit, check the current environment for source access, media probing/rendering (for example `ffprobe` and `ffmpeg`), frame inspection, audio inspection, and writable private project storage. Check a transcription engine only when speech requires it, and a synthesis engine only when narration is wanted. Resolve executables from the environment; do not assume a package-manager path, GPU, operating system, model cache, credentials, or another installed skill. Resolve this skill's reference links relative to this `SKILL.md`, not the current working directory.

If a required capability is missing, explain the specific gap and propose a compatible setup or fallback within the user's permissions. Continue independent analysis when possible; do not claim inaccessible media was inspected. With no narration, skip both script approval and voice generation, and build timing around selected footage and original audio. An instruction-only installation does not install media tools or model weights.

## 1. Discover and inspect footage

Search the user-authorized folder, album, date range, or event. When “iCloud” is ambiguous, use available context and a narrow inspection to distinguish Photos from Drive; ask only if that remains unresolved. Read [source-discovery.md](references/source-discovery.md) for iCloud or Photos.

Create a private inventory with stable clip IDs, source locations, durations, dimensions, rotation, frame rates, audio tracks, and color metadata. Check that cloud assets are actually readable before analyzing them. Preserve originals.

Inspect sampled frames and listen to relevant audio. For speech, obtain timestamped transcription with word timing when supported; verify uncertain words by listening. For scenic material, inspect representative frames and motion, not just speech. Compare near-duplicates for complete delivery, focus, motion blur, and useful unique moments. Do not invent visual observations from filenames or transcripts.

Cache analysis by source identity/content and relevant model settings. Record useful source time ranges, uncertainty, and missing coverage. Do not rescan unrelated libraries or retranscribe unchanged material without a reason.

## 2. Propose the edit — checkpoint

Show a concise, evidence-backed proposal before assembling the edit:

- Story arc and intended feeling, with approximate duration and aspect ratio.
- Key scenes mapped to clip IDs and source time ranges, including gaps.
- What original speech/ambience stays, what narration adds, and what gets cut.
- Proposed language, captions, voice approach, music, and title/cover treatment.

Wait for approval of this concrete proposal unless already explicitly approved. Read-only analysis, script drafts, and small technical probes can continue. Do not interpret silence as approval. A narrower user request, such as “only analyze,” stays within that scope.

## 3. Write narration — checkpoint

Deliver the complete proposed script as readable text, grouped by story beat and linked to intended footage. Estimate duration as provisional until audio exists. Distinguish visible facts, user-supplied experiences, and external background facts; verify external claims when necessary. Never invent personal experiences or identify a place solely because it resembles one.

Ask the user to approve the exact narration text and resolve meaningful uncertainties. Do not generate full narration or build a narration-led cut before that approval. If no narration is wanted, mark this stage not applicable. A user's supplied final script may already constitute approval when they explicitly request its narration.

Keep approved words intact during speech generation. Material rewrites, translations, or a new language require approval of their new text. Pronunciation fixes that preserve meaning do not require reapproving the entire story.

## 4. Select and preview the voice — checkpoint

Use the user's chosen engine when available. Otherwise offer a practical local or hosted preset appropriate to the selected language; inspect current availability, terms, costs, and processing location before committing. Do not require a paid service, hardcoded vendor, or specific model.

For cloning, use only the user's authorized voice or a voice they have permission to use. Keep reference recordings, embeddings, model artifacts, and credentials private. Do not download an arbitrary person's recording as a clone source. “Find a voice online” means a licensed voice catalog or permitted voice asset, not unrestricted voice scraping.

Tell the user before sending private footage, scripts, or voice samples to an external service, and obtain authorization if not already covered. Never ask them to paste secrets into a public issue or committed file.

Generate a short sample from approved text covering representative pronunciation and delivery. Get approval of the voice and pacing before full synthesis unless an existing approved voice configuration explicitly applies. Save the approved text/version, voice settings, segment order, and generated audio. Check for omissions, repetitions, clipped endings, and unnatural joins; assemble all approved words without truncation.

## 5. Build and review the rough cut — checkpoint

Use actual narration durations to arrange footage; revise shot choices within the approved story rather than silently rewriting the script. Keep an edit decision list with source in/out points and output positions. Preserve meaningful reactions and ambience, and cut speech at audible word/phrase boundaries with suitable handles.

Deliver a playable rough cut, readable subtitle draft if requested, and a short list of consequential edits or unresolved items. Prefer unburned captions at this stage. Ask uncertain-transcript questions together using current-cut timestamps and candidate wording. Do not present ASR guesses as verified speech.

Wait for feedback on the cut and caption meaning before final rendering. A short style preview may be combined with this review; avoid making the user approve the same unchanged decision twice. If music is included, choose an appropriate licensed track, preserve license evidence privately, and duck under speech. If attribution conflicts with the requested presentation, choose another track. Never promise a license prevents platform muting.

## 6. Finish and verify

Read [production.md](references/production.md) before rendering. Apply the approved title, caption languages/style, color treatment, music mix, and cover choice. Burn captions only if requested or agreed; otherwise provide sidecars. Do not add production or licensing text to the picture unless requested.

Export a clearly versioned final video and any agreed cover/captions. Preserve independent narration, dialogue/ambience, and music assets where practical. Summarize verification and any remaining limitations honestly.

Update private `project.md` with latest deliverables, decisions, approvals, source-to-output mapping, engine settings, and next actions. Never place personal project records in this skill's public source tree. Publishing to social platforms, archiving, or deleting originals is a separate action requiring user authorization.
