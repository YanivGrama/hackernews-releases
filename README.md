# HackerNews — Releases

Public APK distribution for the [HackerNews Android app](https://github.com/YanivGrama/HackerNews). The source code lives in a private repository; this repo only hosts the compiled APK builds and release notes so that the in-app updater can fetch them anonymously.

## Install

1. Open the latest **stable** release on the [Releases page](https://github.com/YanivGrama/hackernews-releases/releases/latest).
2. Download `HackerNews-<version>.apk`.
3. On your Android device, open the file. If prompted, allow installation from this source.
4. From this point on, updates are detected automatically inside the app — no need to come back here manually.

## In-app updates

The app polls this repo on cold start and whenever you tap **Settings → Check for updates**. When a newer version is available it shows a Snackbar with an **Update** action that downloads the APK and launches the system installer.

### Pre-release builds

Pull-request builds are published here as **pre-releases** (`vX.Y.Z+prN.M`). They are hidden by default. To opt in, open the app and toggle **Settings → Include pre-release builds**.

## Release cadence

| Channel | Tag format | Trigger | GitHub flag |
|---------|------------|---------|-------------|
| Stable | `vMAJOR.MINOR.PATCH` (e.g. `v1.0.3`) | Merge to `main` in the source repo | `prerelease=false` |
| Pre-release | `vMAJOR.MINOR.PATCH+pr<N>.<idx>` (e.g. `v1.0.3+pr42.2`) | Every PR build in the source repo; `<idx>` resets per PR | `prerelease=true` |

Releases are published here automatically by the [Release workflow](https://github.com/YanivGrama/HackerNews/actions/workflows/release.yml) in the source repo using a scoped fine-grained PAT.

## Reporting issues

The source code, issue tracker, and discussions live in the private source repo. If you don't have access there, please reach out to [@YanivGrama](https://github.com/YanivGrama) directly.

## Privacy

This repo only contains release artefacts (APK + auto-generated release notes). It does not collect any data from users.
