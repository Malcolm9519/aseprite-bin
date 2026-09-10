# Aseprite Windows build helper

This fork builds a 64-bit Windows copy of [Aseprite][] from the official Aseprite source using GitHub Actions.

The default build is pinned to **Aseprite v1.3.18.5** so a future upstream tag cannot silently change what gets compiled. You can still enter another Aseprite tag manually when starting the workflow.

## Build Aseprite

1. Open the **Actions** tab in this repository.
2. Select the **aseprite** workflow.
3. Click **Run workflow**.
4. Leave the version as `v1.3.18.5` for the pinned build, or enter another official Aseprite tag intentionally.
5. After the workflow succeeds, open the run and download the `aseprite-<version>` artifact.
6. Extract the downloaded ZIP and run `aseprite.exe` from the extracted Aseprite folder.

The workflow compiles Aseprite from source; this repository does not contain or redistribute a prebuilt Aseprite binary.

## Updating later

When intentionally moving to a newer stable Aseprite release, update the default version in both:

- `.github/workflows/aseprite.yml`
- `build.cmd`

Then run the workflow again.

## Licensing

Aseprite's source code and compiled binaries are subject to Aseprite's license/EULA. Review the official [Aseprite EULA][eula] and [FAQ][faq], particularly before sharing or redistributing compiled builds.

[Aseprite]: https://github.com/aseprite/aseprite
[eula]: https://github.com/aseprite/aseprite/blob/main/EULA.txt
[faq]: https://www.aseprite.org/faq/
