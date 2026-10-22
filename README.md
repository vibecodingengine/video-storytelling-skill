# Video Storytelling Skill

[中文说明](README.zh-CN.md)

A language-independent Codex skill for turning personal footage into a reviewed story: discover footage → analyze → propose an edit → approve narration → audition a voice → review a rough cut → finish.

Supports workflows involving local folders, iCloud Drive, and iCloud Photos when the agent has appropriate access. Narration can use a licensed preset voice or an authorized cloned voice. Source speech, narration, captions, and conversation language are independent choices.

## Install

Ask Codex: "Use $skill-installer to install skills/video-storytelling from https://github.com/vibecodingengine/video-storytelling-skill."

For manual installation, copy `skills/video-storytelling` to `~/.agents/skills/video-storytelling` for user-wide use, or to `.agents/skills/video-storytelling` in your project for project-local use. Keep `SKILL.md` and `references/` together; do not copy the entire repository as the skill folder. Preserve any existing installation before replacing it. These are portable user-relative locations, not paths on the author's machine. See [official skill documentation](https://learn.chatgpt.com/docs/build-skills) for discovery locations supported by your version. If the skill does not appear, restart Codex. No other personal skill is required.

This repository contains agent instructions, not an editor, speech engine, or iCloud connector. Actual editing needs media tools such as FFmpeg/ffprobe, a suitable transcription engine when speech matters, and a TTS engine if narration is requested. Photos discovery needs macOS Photos access or an exported folder. The agent should inspect available tools and explain missing capabilities. No paid API is mandatory.

## First-run check

Ask: "Use $video-storytelling to check your available tools and read its bundled references. Do not edit or upload anything yet."

The agent should confirm source access, media inspection/rendering tools, visual/audio inspection capability, and any required transcription or voice engine. Missing tools should produce a concrete setup or fallback proposal, not a claim that editing succeeded. On systems without Photos access, use exported local files. This check verifies readiness; it is not an end-to-end video test.

## Example request

> Use $video-storytelling to find footage in my selected holiday album, analyze it, and propose a two-minute video. Narration should be in Spanish, with optional English subtitles. Show me the full script before generating narration, then let me hear a preset voice sample before editing.

Or use any other languages, a local footage folder, original sound only, or your own authorized voice configuration.

## Review checkpoints

1. Editing proposal: story, footage choices, duration, format.
2. Exact narration text before full voice generation or a narration-led cut.
3. Voice sample before full synthesis, unless that configuration is already approved.
4. Rough cut and caption meaning before final rendering.

Approvals apply to specific versions. Unchanged approved choices are reused. The skill does not publish videos or delete source material on its own.

## Privacy and scope

Keep all footage, private project notes, source paths, thumbnails, location metadata, transcripts, voice samples, embeddings, and credentials outside this repository. Public examples are synthetic. External processing of private material needs user authorization; voice cloning needs permission from the voice owner.

The skill is written independently as a reusable workflow. It does not redistribute personal media, speech models, or third-party editing helper code. There is no bundled renderer or end-to-end execution guarantee across devices; exported videos still need review.

Contributions should use synthetic examples and avoid uploading real personal assets or logs. Instructions are licensed under MIT; external tools, models, voices, and music retain their own terms.
