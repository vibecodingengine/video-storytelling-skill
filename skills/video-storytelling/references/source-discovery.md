# Source discovery

## iCloud Photos versus iCloud Drive

iCloud Photos is a photo-library service; iCloud Drive is file storage. A synced Drive folder is not an inventory of the Photos library. Use available native Photos access or supported exports for Photos, and filesystem access for synced Drive files. This skill supplies neither account access nor an iCloud downloader.

- Use the existing signed-in session and granted permissions. Do not collect passwords, extract session tokens, bypass a locked device, or parse undocumented library internals to evade access controls.
- Narrow discovery using the user's album, event, dates, and visible thumbnails. Modification times after download may differ from capture times; preserve timezone context and check visual evidence before choosing a trip/day.
- With optimized storage, a thumbnail or placeholder is not the original. Export/download selected originals through the available supported interface, wait for completion, then verify decodability, duration, and size. Report unavailable clips rather than silently substituting previews.
- For Photos, prefer unmodified originals; retain paired components when relevant. Export into the private project directory without changing the library. If the user needs an existing Photos edit, distinguish that rendition from the original.
- If access is unavailable, state the specific limitation and request a narrow export or folder location. Do not claim to have searched the entire cloud library from a partial local view.

## Private working records

Keep source paths, asset IDs, timestamps, thumbnails, transcripts, location metadata, and the mapping from short clip IDs to originals inside the private project. Public examples use fictional paths and text. Inspect export metadata before public sharing if the user requests privacy scrubbing; retain originals unchanged.
