---
name: Displaying using Python
description: >-
  Use when the user wants existing image or video-frame pixels (crops, enlargements, frames, Python-made graphics) actually shown in chat, not just a path, link, or description.
  Drive hub owns the canonical CORE; this copy is versioned 2026-10-16
  from CORE — displaying-using-python.
---

Adapter of Drive CORE — displaying-using-python (version 2026-10-15). Read-only mirror.
# Displaying Using Python

**Source:** Drive CORE — displaying-using-python (private Drive hub, CORE dated 2026-10-15). Local copy dated 2026-10-16. Prefer the Drive CORE on conflict; refresh this copy when the hub updates. Provider-specific adapters named in the CORE are optional; resolve real capabilities at runtime and report gaps rather than assuming them.

## Objective

Render **real image pixels visible in the chat**, not merely a path, download link, file citation, metadata, OCR text, internal model preview, or an image-shaped placeholder. This skill presents existing image content, including Python-created graphics, without silently generating substitute imagery.

## Workflow

1. **Identify the source and requested presentation.** For an existing uploaded image/video or Library item, retrieve the exact source. Use conversation attachments directly when available; use Files/connector retrieval or materialization for previously stored assets when required. Never invent a filename or sandbox path.

2. **Inspect and verify file access.** Confirm the real path exists and the source is readable. Preserve identity, frame numbers, crop region, and original context. Never claim upscaling reveals nonexistent details.

3. **Apply only the requested operation.** For images, open with Pillow, then crop, enlarge, or label only as useful and authorized. For video, decode requested indices/timestamps, convert OpenCV BGR to PIL RGB, and use the original FPS for timestamps. For a full video/frame recipe, read `references/video-frames.md`.

4. **Render through an actually user-visible rich-media capability.** Where Python rich output is supported, use the tested method from the provider adapter. Private processing, a sandbox link, image metadata or internal model previews do not by themselves satisfy a request to show pixels inline.

5. **Mix media with genuinely supported host interactivity when useful or requested.** Rendered image output and native interactive UI components can coexist in one response as distinct visible regions where the host supports both (demonstrated on one provider; verify on this host before relying on it). On a Grok Bot, save the Python-produced image to a file and deliver it through the host's user-visible media path (e.g. sending the file to the user inline), then compose any interactive UI separately. Do **not** claim the two tools share a JavaScript/Python runtime, an integrated data binding, or a single interactive surface: direct cross-runtime integration has **not yet been verified**. If the user wants an integrated experiment, attempt a bounded test using supported bindings and inspect the actual outcome rather than declaring it impossible or proven in advance.

6. **Verify the result without bluffing.** Tool success or an internal image preview does not prove the user saw pixels in their client. When the client previously failed to render, explicitly request or use user confirmation. If no genuine user-visible image renderer is available, report the limitation; do not substitute a private renderer while claiming success.

## Pixel and source integrity

- Preserve order, labels, timestamps and source identity for multiple images or selected frames.

- If the user supplied an image, inspect/display that exact source, not a generated replacement; create/edit only when the user explicitly requests changed pixels.

- Download links may accompany deliverables but do not replace an explicit inline-display request.

## Portability and runtime boundaries

- Verify which provider surface can actually emit visible image data, and distinguish private file processing from user-facing presentation.

- Display and interaction capabilities may live in separate runtimes; verified co-presentation does not establish direct programmatic coupling.

- Apply exact file type and frame-conversion rules only in the host-specific adapter.

## Acceptance test

The user sees the original pixels in the conversation at a useful size, in the requested order; any requested, supported interactive presentation appears alongside them in the same response. Source accuracy and transformations are verifiable. Only claim success at the level actually observed, and record user feedback when the client rendering differs from internal tool results.
