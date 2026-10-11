# App Library Stash

App Library is a lightweight catalog system for distributing Android application packages (APKs). It separates app metadata management from large binary file hosting to avoid bandwidth costs, file size caps, and link expiration.

---

## Architecture Overview

The system uses a two-tier structure:

* Metadata & Catalog: Managed via Supabase for app titles, category tagging, version strings, studio attributions, icons, and description text.
* Binary Distribution: Hosted directly through GitHub Releases. Large games, custom builds, and utility engines (up to 2GB per asset) are stored permanently on GitHub's release infrastructure without bandwidth caps or expiring links.

---

## Release & Upload Workflow

To add or update an application asset:

1. Open the Releases section of this repository.
2. Select "Draft a new release".
3. Assign a release tag following a consistent naming scheme (for example, `v1.0.4` or `noir-engine-v1.0.4`).
4. Upload your compiled `.apk` binary under the release assets section.
5. Publish the release, copy the direct asset URL, and paste it into the App Library admin form.

---

## Character & File Encoding

All database fields, search query handlers, and UI renders are configured for standard UTF-8 encoding. Text entries support accented characters, symbols, and international text without breaking UI alignment or query filtering.

---

## License

Distributed under the MIT License. See `LICENSE` for details.
