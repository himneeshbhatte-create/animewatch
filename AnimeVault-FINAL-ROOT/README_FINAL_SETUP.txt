ANIMEVAULT FINAL ANDROID APP
============================

This package is deliberately a SINGLE Flutter project root.
There is no nested project folder and there is only ONE codemagic.yaml.

GitHub layout must be:

Animewatchlist-FINAL/
  pubspec.yaml
  codemagic.yaml
  lib/
  assets/
  ...

Do NOT upload this whole folder as a folder inside another folder.
Upload the CONTENTS of AnimeVault-FINAL directly into the ROOT of a NEW empty GitHub repository.

Recommended repository name:
AnimeVault-App-Final

Codemagic:
1. Add the new repository as a Flutter app.
2. The project path is the repository ROOT (leave it as root / .).
3. Select the workflow: android-debug / AnimeVault Android APK.
4. Select branch: main.
5. Build.

The workflow generates the Android platform if needed, builds the debug APK,
and then copies the APK to artifacts/AnimeVault-debug.apk.
Codemagic publishes that exact file, avoiding nested artifact-path problems.

Do not copy this project into the old Animewatchlist repository with the previous nested folders.
Creating a new empty repository avoids the duplicate codemagic.yaml problem entirely.
