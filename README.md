# Media Submodule Directory

This directory is a git submodule checkout of the external media repository.

## Purpose

- Serve uploaded media from the same site origin at `/media/...`
- Keep binary history out of the main content/code repository
- Allow build-time responsive variant generation from canonical files

## Expected layout

- `uploads/<yyyy>/<mm>/<file>` for canonical media
- `uploads/variants/<yyyy>/<mm>/<file>-{width}w.webp` for generated variants

## Important

- Do not manually reorganize files in this directory unless you are intentionally migrating media layout.
- Keep this path as the configured submodule target: `apps/web/public/media`.
- Uploaded content is committed to the media repo by the Worker, then published when Pages rebuilds.
