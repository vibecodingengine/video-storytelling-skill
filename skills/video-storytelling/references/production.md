# Production checks

## Timeline and sound

Keep source and output time bases explicit. For a normal-speed segment, `output_time = source_time - source_in + output_start`; speed changes and transitions need their own mapping. Rebuild captions from the final mapping after editorial changes. Word timestamps are suggestions to verify against the audio, especially near edits.

Use short fades or crossfades where needed to avoid clicks, without shaving consonants or doubling speech. Preserve intentional pauses. Check dialogue/narration intelligibility against music and avoid clipping; keep a music-free export when requested for platform alternatives.

Choose a render path appropriate to the media. Stream-copy concatenation requires compatible streams and time bases, and arbitrary stream-copy cut points may not be frame-accurate. Normalize/encode when necessary; avoid repeated lossy generations. Do not impose a specific renderer or hardware codec.

## Picture and captions

Inspect rotation, variable frame rate, and HDR/color metadata. HDR-to-SDR conversion requires a real supported color conversion/tone-mapping path, not merely relabeling metadata. Use the same color pipeline for preview and final. Do not claim to preserve dynamic HDR metadata without checking.

Composite captions above layers that would obscure them. Check font coverage, shaping, accents, right-to-left layout when relevant, line breaks, contrast, and placement against faces and interface safe areas. Never hardcode a language pair or a language-specific title.

Choose covers from inspected full-resolution frames, avoiding motion blur, blinking, and awkward expressions. First-frame cover embedding is optional. If requested, verify the actual first and following frames; do not insert a freeze duration or shift audio/captions without agreement. A platform can still require separate thumbnail selection.

## Validate rendered output

- Fully decode the export and inspect reported errors.
- Compare actual duration, audio streams, and dimensions with the approved timeline. Listen to the ending; successful encoding does not rule out truncated audio.
- Inspect rendered frames at cut/transition boundaries, titles, scene changes, and representative caption events throughout the full video. Listen across joins and check synchronization.
- Review narration against the approved script for missing/repeated phrases. State what was checked and flag unresolved issues.
- Keep distinct version names so the user can compare revisions. Mark the latest final deliverables clearly; do not link an intermediate silent video as the final.

After repeated failed fixes, stop the failing approach and report the concrete issue and a practical alternative instead of looping indefinitely.
