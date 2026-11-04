# Reader

Local PDF and Markdown reader. One document per window. The format comes from the file bytes, not the extension.

## Downloads (after the first successful Actions run)

This repository is set up so GitHub Actions on `windows-latest` and `macos-latest` publishes an unsigned alpha:

- https://github.com/samdharma/reader/releases/download/v0.1.0/Reader-windows-x64.exe
- https://github.com/samdharma/reader/releases/download/v0.1.0/Reader-macos-arm64.zip
- https://github.com/samdharma/reader/releases/download/v0.1.0/SHA256SUMS

Release page: https://github.com/samdharma/reader/releases/tag/v0.1.0

Those files appear only after `.github/workflows/release.yml` runs on a commit that contains the full source. A partial tree cannot build.

### Windows 11

1. Download `Reader-windows-x64.exe`.
2. If SmartScreen appears, choose More info, then Run anyway.
3. Windows 11 already includes WebView2.
4. Double-click the exe, or run `Reader-windows-x64.exe C:\path\to\file.pdf`.
5. Open or drop a PDF or Markdown file. There is no format prompt.

### Mac (Apple Silicon)

1. Download `Reader-macos-arm64.zip` and unzip it.
2. Right-click `Reader.app` and choose Open, then Open again.
3. If macOS only offers the Trash, use System Settings, Privacy and Security, Open Anyway.
4. Open a file from the button, or run `Reader.app/Contents/MacOS/reader /path/to/notes.md`.
5. Drop a file on the window.

The build is unsigned. Notarization and Authenticode come later.
