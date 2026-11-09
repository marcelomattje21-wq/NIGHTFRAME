# NIGHTFRAME V43 — Loop Studio

V43 adds local video-loop and clip-transition tools to the NIGHTFRAME desktop editor.

## What's included
- Analyse the first/last video frames and display an approximate visual similarity score.
- Create a silent MP4 loop by blending the end of a clip into its beginning.
- Join two clips with an adjustable crossfade, normalising dimensions and frame rate.
- Local processing with FFmpeg/FFprobe. The original file remains untouched.

## Important limitations
The similarity score is a basic comparison of downscaled endpoint frames, not a motion-continuity guarantee. Crossfades may show ghosting in moving scenes; unrelated clips can be dissolved together, but the program does not reconstruct physically continuous motion. Loop Studio exports silent video so a continuous music track can be added separately.

## Build
The GitHub Actions workflow reconstructs the source ZIP, verifies its SHA-256, runs automated tests, builds the Windows NSIS installer and publishes a GitHub Release. The in-app updater is only ready after the release includes the installer and electron-builder update metadata (latest.yml).
