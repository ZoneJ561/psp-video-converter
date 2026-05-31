# PSP Video Converter

PSP Video Converter creates Sony PSP-compatible videos from common video files, permitted online downloads, and unencrypted DVD or Blu-ray folders.

The Windows and macOS downloads are standalone. FFmpeg, FFprobe, and yt-dlp are already packaged with the app. End users do not need to install Python or extra conversion tools.

## Download

Download the latest release:

```text
https://github.com/ZoneJ561/psp-video-converter/releases/latest
```

### Windows

Run `PSPVideoConverterSetup.exe`, then open **PSP Video Converter** from the Start Menu or desktop shortcut.

### macOS

Open `PSPVideoConverter-macOS.dmg`, drag **PSP Video Converter** into Applications, then open the app. The macOS build is ad hoc signed rather than Apple-notarized, so the first launch may require right-clicking the app and choosing **Open**.

## What It Creates

- `avc480` preset: MP4 with H.264 Baseline video, AAC audio, 480x272, and 29.97 fps. This is the recommended preset for most PSP systems.
- `legacy320` preset: MP4 with MPEG-4 video, AAC audio, 320x240, and 29.97 fps. Try this if the PSP will not show the AVC file.
- Matching `.THM` thumbnails: 160x120 PSP thumbnail files with the same base name as the video, such as `movie.mp4` and `movie.THM`.
- `conversion_report.txt`: a report showing what converted, what failed, and whether each output passed PSP checks.

The converter letterboxes or pillarboxes video instead of stretching it, so widescreen and 4:3 sources keep the correct shape.

## Main Features

- Premium PSP-inspired GUI with Sony/PSP-style branding and God1yNigga release credit.
- Quality profiles: Small File, Balanced, Best Quality, and Old PSP Compatibility.
- Optional GPU encoding: Auto GPU, NVIDIA NVENC, Intel Quick Sync, and AMD AMF.
- GPU benchmark tool that runs short real encoder tests and offers to switch to the fastest working encoder.
- DVD and anamorphic aspect-ratio handling that uses display aspect-ratio metadata before fitting video to the PSP screen.
- Unencrypted DVD `VIDEO_TS` folder support with a title picker for the main movie and extras.
- Unencrypted Blu-ray `BDMV` folder support for large `.m2ts` streams.
- In-app online video URL downloader followed by automatic PSP conversion.
- Downloader options for `cookies.txt`, browser cookies, browser-like headers, and direct DRM-free MP4 or M3U8 fallback.
- Optional adult-site URL downloads with an 18+ confirmation gate before enabling.
- Join queue mode for merging multiple videos into one PSP-compatible MP4 in queue order.
- Custom AAC audio bitrate and volume controls, including volume adjustment up to 600%.
- PSP Black, Dark Mode, Light Mode, Mystic Cyan, and editable Custom Colors themes.
- Real conversion progress, estimated time remaining, cancel, and Stop After Current controls.
- Timeline thumbnail scanner, live frame preview, step controls, and contact-sheet picker.
- Sequential queue THM picker for choosing a different thumbnail frame for each selected or queued video.
- Queue project save and load files that preserve batch order, settings, disc-title selections, and per-video THM choices.
- Per-video audio-language and embedded text-subtitle track picker with saved queue-project and joined-video support.
- Per-video item settings for preset, quality, audio bitrate, volume, thumbnail time, filename template, and fit-to-size overrides.
- Fit-to-size targets for 100 MB, 250 MB, 512 MB, 1 GB, or available output-drive space.
- Preflight check for bundled tools, output-folder access, estimated size, disk space, encoder availability, and PSP compatibility notes.
- Preset Manager for named conversion profiles.
- Conversion History with prior outputs, failures, and quick folder opening.
- PSP Library Organizer with scan progress, metadata cache, search, filtering, sorting, THM previews, and batch artwork tools.
- Memory Stick Planner for estimating how many queued videos fit on cards from 512 MB through 128 GB.
- Subtitle burn-in for matching `.srt`, `.ass`, `.ssa`, or `.vtt` files.
- PSP output verification and one-click copying to a PSP `VIDEO` folder.
- Drag-and-drop file and folder support.
- Automatic app update checks and yt-dlp updates.
- Export Diagnostics ZIP tool for troubleshooting.

## Basic Use

1. Add video files, folders, unencrypted disc folders, or permitted online URLs.
2. Choose an output folder.
3. Pick a PSP preset, quality profile, audio settings, and thumbnail frame if desired.
4. Click **Start Conversion**.
5. Use **Copy To PSP** to copy finished videos and thumbnails to your memory stick.

For newer PSP firmware, copy converted `.mp4` and `.THM` files into a `VIDEO` folder at the root of the memory stick. If a video does not appear on the PSP, try the `legacy320` preset or enable PSP legacy file names.

## Disc And Online Sources

The app supports unencrypted DVD and Blu-ray folders. It does not decrypt copy-protected discs.

Only download online videos you own or have permission to download. Direct MP4 and M3U8 streams must be used only where downloading is permitted. DRM-protected sources are not supported.

## Updates

Use **Check Updates** inside the app to download future installers. The public repository intentionally contains release information and downloads only.
