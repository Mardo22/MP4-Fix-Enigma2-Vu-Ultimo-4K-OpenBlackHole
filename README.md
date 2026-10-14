# MP4 Fix for Enigma2 – Vu+ Ultimo 4K / OpenBlackHole

**Watch 4K MP4/MKV movies and switch subtitles without freezing your receiver.**
See full movie info and turn any MP4 into an MKV with Slovak subtitles – all with your remote.

**Designed by Mardo22** · YouTube: **SetTvBox4U** · Contact: settvbox4u@gmail.com

MP4 Fix is a plugin for OE-Alliance Enigma2 images. It fixes a problem in the standard
movie player on **OpenBlackHole 6.0**: when you switch subtitles on or change them during
playback (in MP4 or MKV), the standard player (servicemp3, GStreamer 1.28) freezes the whole
receiver. You then have to restart the GUI.

## Features
- **Safe playback**: MP4/MKV movies from the movie list play with **ExtePlayer3** (ServiceApp).
  You can switch subtitles and audio as often as you like. Live TV, IPTV and streams are never changed.
- **Make MKV**: copies video and audio bit-for-bit into a verified MKV, with all audio tracks
  and all text subtitles (tx3g → SRT). **Slovak, then Czech, then English** is the default subtitle track.
  4K HEVC, HDR10 and Dolby Vision are kept. The original MP4 is kept.
- **Quick MKV / TEST**: Yellow key → full movie, or a test of the first **1, 2 or 3 minutes**.
- **Movie info** (new in 3.2): **INFO** key, Blue = Menu → *Movie info*, or MENU in the movie list.
  Shows quality (4K / Full HD, HDR10, HLG, Dolby Vision profile), video (codec, resolution, fps,
  bit depth, bitrate), every audio track (language, codec, Dolby Atmos, 5.1, bitrate) and every subtitle track.

## Supported receivers and images
| Receiver | Image | Status |
|---|---|---|
| Vu+ Ultimo 4K | OpenBlackHole 6.0 (Python 3.14) | ✅ tested |
| other ARMv7 receivers | OE-Alliance images with **Python 3.14** | not tested yet |

The package contains compiled code for **ARMv7 (armv7ahf-neon)** and **Python 3.14**.
It will not install on images with another Python version or on MIPS / ARM64 receivers.

## Installation (OpenBlackHole)
1. Download `enigma2-plugin-extensions-mp4fix_3.2_armv7ahf-neon.ipk` from the latest **[Release](../../releases/latest)**.
2. Copy it to `/tmp` on the receiver (FileZilla / WinSCP, user `root`, port 21).
3. Green key → yellow **Addons** → **Manual Install Ipk packages** → choose the file → **Yes**.
4. Restart the GUI when asked. The plugin is in the Green Panel as **MP4 Fix 3.2**.
5. For safe playback install ServiceApp: MP4 Fix → Blue (Menu) → *Settings* → *Install / update ServiceApp*.

Command line alternative:
```
opkg install /tmp/enigma2-plugin-extensions-mp4fix_3.2_armv7ahf-neon.ipk
```

Check the download: `sha256sum` must match `SHA256SUMS.txt`.

## Requirements
`ffmpeg` (part of OpenBlackHole), optional `enigma2-plugin-systemplugins-serviceapp` + `exteplayer3`.

## License
Free to use. **All rights reserved**. The plugin is distributed as compiled code only.
See [LICENSE](LICENSE). Unofficial plugin. It does not change system multimedia libraries.
