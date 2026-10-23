# Nemoviz HiFi Rack — source code of third-party components

Nemoviz HiFi Rack (NHR) is a free, accessible music player for Windows by Gordan Radić.
It ships some components under the GNU GPL and the GNU LGPL. This repository is the
**written offer of source code** those licences require: it holds the exact source of
every GPL and LGPL component in the NHR package, and it will stay available for at
least three years after the last NHR release that contains them.

The archives are attached to the [releases](../../releases) of this repository, one
release per NHR package. `SHA256SUMS.txt` lists their checksums. Nothing in them is
modified by the author of NHR; they are the upstream sources at the versions shipped.

NHR's own licence terms do not restrict any right you have under the GPL or the LGPL
for these components. You may copy, change and redistribute them under their own
licences. The LGPL libraries are separate DLL files in the program folder, so you
can replace them with your own builds.

## Release `nhr-alpha-2026-10-24`

| shipped in NHR | version | licence | source archive(s) |
|---|---|---|---|
| Queen Mary Vamp plugins (`analiza\qm`) | 1.8.0 | GPL-2.0-or-later | `qm-vamp-plugins-1.8.0.tar.gz`, with its pinned `qm-dsp-4d2a4a4.tar.gz` and `vamp-plugin-sdk-44c2487.tar.gz` |
| Sonic Annotator (`analiza\sonic-annotator`) | 1.7 | GPL-2.0-or-later | `sonic-annotator-1.7.tar.gz` and its pinned dependencies `svcore-06dbb26.tar.gz`, `vamp-plugin-sdk-44c2487.tar.gz`, `vamp-plugin-load-checker-5ba2746.tar.gz`, `piper-vamp-cpp-6f16a09.tar.gz`, `sv-dependency-builds-01bb145.tar.gz` (libmad, libid3tag, FFTW, libsamplerate, libsndfile, Ogg, Vorbis, Opus, Serd, Sord and others) |
| — Qt 6 Core, Network, Xml, Test (DLLs beside Sonic Annotator) | 6.7.2 | LGPL-3.0 | `qtbase-everywhere-src-6.7.2.tar.xz` |
| — libsndfile (DLL beside Sonic Annotator) | 1.0.27 per its version resource; 1.0.31 in the pinned dependency builds | LGPL-2.1-or-later | `libsndfile-1.0.27.tar.gz`, and `sv-dependency-builds-01bb145.tar.gz` |
| fpcalc (`analiza\fpcalc.exe`, Chromaprint) | 1.6.1 | LGPL-2.1-or-later | `chromaprint-1.6.1.tar.gz` |
| — FFmpeg, built into fpcalc (audio-only LGPL build, no GPL or nonfree parts) | 8.0 | LGPL-2.1-or-later | `ffmpeg-8.0.tar.xz` and the build scripts `ffmpeg-build-v8.0-1.tar.gz` (acoustid/ffmpeg-build) |
| TagLib# (`TagLibSharp.dll`) | 2.3.0 | LGPL-2.1 | `taglib-sharp-2.3.0.0.tar.gz` |
| BASSenc_MP3 (`bassenc_mp3.dll`), which contains libmp3lame | 2.4 | libmp3lame: LGPL-2.0; BASSenc_MP3: free with BASS | `bassenc_mp3-source.zip` (Un4seen's published source, with its libmp3lame), `lame-3.100.tar.gz` |
| Croatian hunspell dictionary (`rjecnik`) and the word tables NHR derives from it | hr_HR | GPL-2.0 / LGPL-2.1 / MPL-1.1 (triple) | `hunspell-hr_HR-as-shipped.zip` (the shipped files are their own source) |

### Upstream

- Queen Mary Vamp plugins, qm-dsp: https://github.com/c4dm
- Sonic Annotator, svcore, dependency builds: https://github.com/sonic-visualiser
- Vamp plugin SDK: https://github.com/vamp-plugins/vamp-plugin-sdk
- Qt: https://download.qt.io/archive/qt/6.7/6.7.2/
- libsndfile: https://github.com/libsndfile/libsndfile
- Chromaprint: https://github.com/acoustid/chromaprint ; its FFmpeg build: https://github.com/acoustid/ffmpeg-build
- FFmpeg: https://ffmpeg.org/releases/
- TagLib#: https://github.com/mono/taglib-sharp
- BASSenc_MP3 source: https://www.un4seen.com/files/bassenc_mp3-source.zip ; LAME: https://lame.sourceforge.net/
- Croatian dictionary: https://github.com/krunose/hunspell-hr

Components under permissive or proprietary licences (BASS and its add-ons, ONNX
Runtime, the Beat This! model, OpenSSL inside BASS_SSL, .NET helper libraries) need no
source offer; their notices ship in the `Licenses` folder of NHR.

Questions: open an issue in this repository.
