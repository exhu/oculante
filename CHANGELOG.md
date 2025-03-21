\# 0.9.2

### :beetle: Bug Fixes

* Prevent application from saving current channel to settings file. The current image channel now is reset between restarts as this was confusing to users. (98ebe9e0)
* prevent dng from being loaded as tiff (96417bbf)
* Send frame wen editing alpha tools to prevent crash (f4eb4690)
* Fallback to native image library if TurboJPEG fails on certain images, such as taken by Samsung phones (3a8b34cc)
* Add all supported heif extensions. Fixes #457 (2e316a95)

### :sparkles: Features

* Simplified Chinese support (dfb6b67d)
* Arabic language support (0851570c)
* Support Japanese, Arabic, Chinese (a5b0dc77)
* Enable bypassing image filters (60beaf6c)
* generate palette from image (932e9ae2)
* Copy palette color to clipboard, highlight palette color if contained (Closes #572, #571) (4279a7d7)
* Basic swatch / palette UI (f1052395)
* enable thumbnails in image browser (d39b79d5)
* search files in current directory in file browser (1a1775c1)
* Expose image save options (372aeefb)
* Allow storing bookmarls in the file dialog (bf5b7e1e)
* Criterion benchmarks (c8218834)
* Read Krita files (711b666a)
* Rotate images according to their EXIF rotation data (dbeb9a96)
* Heif format is bundled in release for Apple Silicon macs (extra heif build available for intel macs) (dbd71465)
* Heif support in OSX release builds (0e1a3d78)

### :green_apple: Chore

* Filters are in scrollable list (01264bbf)

# 0.9.1 (2024-09-21)

### :beetle: Bug Fixes

* Prevent scrollbars from occluding info panel (19d3be85)
* Remove duplicated shortcuts entry in Readme and fix build script to auto-generate keymaps (99e9d9ef)
* Noise filter ui would extend panel too much (063df9d6)

### :sparkles: Features

* Generate flathub meta for a release (77e43596)

### :green_apple: Chore

* Improved changelog generation (1665cd3c)
* Exclude screenshots from cates.io build to save space (c80df685)
* Fix wronf icon for Rotate operator (5f564b46)

# 0.9.0 (2024-09-21)

### :beetle: Bug Fixes

* Flip operation would always flip horizontal (7019c757)
* Mac build broke because of icon. Switched image format. (7954c29d)
* When pressing right mouse, panning operation got stuck. Panning is now only possible using left or middle mouse. (dff337f3)

### :sparkles: Features

* Show confirmation dialog when deleting a file (4ca02a5b)
* Stack Blur provides much faster blur performance for the blur filter (65a345f3)
* Visually indicate difference between operator types with a separator (fb26bc06)
* Persistent and volatile settings are now split for easier versioning of configuration files (936c996c)
* enable version control friendly settings (297abe16)
* Use built in file browser (35f9b9ea)

### :green_apple: Chore

* Update deps (ac7e9dc8)
* **deps**: bump quinn-proto from 0.11.3 to 0.11.8 (c64b79a7)
* update turbojpeg and remove image dependency (bb021b41)
* Update `gif`/ `gif-dispose` (8894ef70)
* Update `fast_image_resize`, `libavif-image`, `self_update`, `libheif-rs` (00da1e57)
* update `trash` (22bd5e45)
* Update webbrowser, wgpu, ruzstd (2f27aef8)
* Update jpg2000 and add test image (541e6c93)
* update image and nalgebra (5c50f05e)
* cargo update (0273560e)

# 0.8.23 (2024-07-29)

### :beetle: Bug Fixes

* Display image path for loading errors (fixes #387) (9bc72095)
* Prevent panic for scrubber index being out of range and allow opening images without path prefic correctly (7a9a99c1)
* update index when image in same folder is loaded (fixes #377) (f2297402)
* Switching theme removes accent color (fixes #375) (e35dea4d)
* Preserve scubber index (d9146d08)
* Prevent image removal going out of bounds (fixes #379) (9b69076f)
* Clearing and deleting an image removes it from the virtual scrubber and advances to the next according to the scrubber direction (a0b7dc5a)
* Fix issue where SVG files were detected as XML (fixes #371) (d2ce9f17)
* Compare menu works without image loaded (46a8218f)
* ClearImage can be assigned to a shortcut (b9b00aca)
* extend BSD variants (f716dfc5)

### :sparkles: Features

* Allow configuring mipmaps and linear mag/min filters (58da0b26)
* Allow passing multiple images on the command line (0a2e918a)
* Enhance scrubber experience to provide a virtual file list. (e3c45a8e)
* Detect file types by content instead of extension. Warn if mismatch happens. (59138263)
* More love for compare mode ui, option to remove current image (68a5a483)
* Allow configuring the minimum window size (1787a14f)

### :green_apple: Chore

* **deps**: bump zerovec from 0.10.2 to 0.10.4 (4cf7959e)
* update resvg (be6a67f6)
* Update Notan and Egui (fc1fccef)
* update deps (031e83ce)

# 0.8.22 (2024-05-19)

### :beetle: Bug Fixes

* Ensure spirv is not used when only using shaderc (03f9167e)
* Allow loading huge webp images and handle still frames differently (e4ebc2dc)
* Set window min size to 100x100 to prevent super tiny window (fixes #325) (d63d971c)

### :sparkles: Features

* add icns image support (internal png data only, load largest contained image) (0703d220)

### :green_apple: Chore

* update avif-decode, evalexpr, exr, rfd, self_update, jxl-oxide, imageproc (a6c98436)
* Clean up warnings (ab2b03fe)

# 0.8.21 (2024-05-10)

### :green_apple: Chore

* Disable AUR publishing: This package has been moved to the official [extra] repository. (55245529)

# 0.8.20 (2024-05-10)

### :sparkles: Features

* Support EXR with single layers (non-rgba) (d22e78c4)

### :green_apple: Chore

* update deps and use new HDR support from `image` (bd7cbf89)

# 0.8.19 (2024-04-29)

### :beetle: Bug Fixes

* prevent zoom with keyboard (fixes #304) (2de35ed6)

### :sparkles: Features

* Map float TIFF images to min-max range (52f87f82)

### :green_apple: Chore

* Update logo (1783609d)
* update icon (716f6e9c)
* **deps**: bump rustls from 0.21.10 to 0.21.11 (f0c1743b)

# 0.8.18 (2024-04-06)

### :sparkles: Features

* APNG support (c633764d)

### :green_apple: Chore

* **deps**: bump h2 from 0.3.24 to 0.3.26 (59c559ac)
* update logo (6ae3bc03)

# 0.8.17 (2024-03-29)

### :beetle: Bug Fixes

* Do not display console window on Windows (fixes #300) (f83eb463)

# 0.8.16 (2024-03-13)

### :beetle: Bug Fixes

* Fix Uri causing files not loading (ad886555)

# 0.8.15 (2024-03-10)

### :beetle: Bug Fixes

* Fix issue where "Open with..." does not work any more (b5677977)

# 0.8.14 (2024-03-08)

### :beetle: Bug Fixes

* Enable hotkey copy and paste (a538c1d5)
* Enable clipboard support on wayland (f86af424)
* Prevent image from flickering at the first frame (df4439a8)
* Make sure window size is not larger than window (36c03c8f)

### :sparkles: Features

* use .config location on unix for storing settings (024dc70b)
* Add perspective cropping with UI. You can now de-warp scans or similar into a nice rectangular picture. (ba7c7575)

# 0.8.13 (2024-02-27)

# 0.8.12 (2024-02-26)

### :beetle: Bug Fixes

* Document that `heif` is now optional on Mac and Linux due to non-static linking. (5f1b4669)

### :green_apple: Chore

* update depndencies (9255847a)
* update jxl-oxide (c5b7e1d4)

# 0.8.11 (2024-02-25)

### :beetle: Bug Fixes

* Prevent app from hanging if not image in stdin (695b2fa7)

# 0.8.10 (2024-02-24)

### :beetle: Bug Fixes

* prevent zoom from being stuck at extreme levels (32c6b02f)
* Blurry text/UI is now rendered crisp (cbb1e165)

### :sparkles: Features

* Allow piping image data to oculante on the command line (e8f92dfa)

### :green_apple: Chore

* rename release artifacts (fcd24e37)

# 0.8.9 (2024-02-21)

### :sparkles: Features

* Only redraw when needed on windows (less cpu/gpu usage) (bffccf7f)
* App Id is now available for wayland (db7afa31)

# 0.8.8 (2024-02-19)

### :beetle: Bug Fixes

* Prevent "Do not reset image view" being reset (4e06ca71)

### :sparkles: Features

* Allow opening of webp animations (8cfb3a40)
* Use custom filebrowser instead of rfd (de581a9f)
* Enable borderless mode and allow to toggle via settings menu (01d48256)
* add 3x3 Filter operator (8ce56fad)
* scale to available ui area (89969e13)

### :green_apple: Chore

* Update notan (f163e3c8)
* Update rfd and strum (0b2d246e)

# 0.8.7 (2024-01-27)

### :sparkles: Features

* Basik support for ktx2 (6a41adda)

# 0.8.6 (2023-12-17)

### :beetle: Bug Fixes

* Disable lazy_loop so UI refreshes on windows (workaround) (9324fe2b)

# 0.8.5 (2023-12-14)

### :beetle: Bug Fixes

* Preserve EXIF across formats when saving (ae855690)

### :sparkles: Features

* Support DNG files with tiff extension (b4db9a6d)
* New toast system to improve UI messages and notifications (9f8c6882)

# 0.8.4 (2023-12-08)

# 0.8.3 (2023-12-08)

# 0.8.2 (2023-12-04)

### :beetle: Bug Fixes

* Mac universal binary fixes, enable heif on Apple silicon (5f234fd9)

# 0.8.1 (2023-12-03)

### :beetle: Bug Fixes

* restore accent color on startup (5fa1c778)

### :sparkles: Features

* Zoom multiplier and min size (ecec7bf2)
* Allow configuring magnification filter (a513a083)
* File change detection (03a955f9)
* Support QOI format (bd32ac32)
* Add HEIF/HEIC decoding (79ee4f95)
* support rgb16 avif (6194c639)
* Add Hald CLUT support (51a88fe4)

### :green_apple: Chore

* update avif (f3b35f43)
* update zune-png (ca615efc)
* update deps (cb299669)
* update self_update (319ccd6a)
* update dependencies (1e4038ec)
* update to notan 0.11 (c228b398)

# 0.7.7 (2023-10-08)

# 0.7.6 (2023-09-20)
- Update smithay-client-toolkit
- Update JXL
- Remove LTO from pkgbuild
- Add file deletion option (They are moved to system trash)
# 0.7.5 (2023-09-15)
- Better Windows performance (Lazy_loop enabled)
- Notan and Egui update
# 0.7.4 (2023-09-03)

# 0.7.3 (2023-08-22)

# 0.7.2 (2023-08-21)

### :green_apple: Chore

* update dependencies (601968b4)

# 0.6.69 (2023-07-20)

### :green_apple: Chore

* update deps (872704cb)

# 0.6.67 (2023-07-05)

### :green_apple: Chore

* update dependencies (7e9f87c7)

# 0.6.66 (2023-06-25)

### :green_apple: Chore

* update deps (2236c283)

# 0.6.65 (2023-06-18)

# 0.6.64 (2023-05-27)

### :beetle: Bug Fixes

* EXIF data is horizontally scrollable (fixes #184) (85cd7618)

### :sparkles: Features

* svg update with faster performance and text rendering support (0278fe97)
* Native rust JXL support (16f73800)

# 0.6.63 (2023-04-20)

# 0.6.62 (2023-04-19)

# 0.6.61 (2023-04-19)

### :beetle: Bug Fixes

* Prevent info panel flickering while auto-hiding scrollbar (696d8818)

### :sparkles: Features

* Simplified file saving - now with file picker (aa410cc6)
* Add optional checker background (f09d012e)

# 0.6.60 (2023-04-02)

# 0.6.59 (2023-04-02)

# 0.6.58 (2023-04-01)

### :green_apple: Chore

* update dependencies (498c862b)

# 0.6.57 (2023-03-27)

### :green_apple: Chore

* Update libwebp-sys and dirs (8fd3f97b)

# 0.6.56 (2023-03-23)

# 0.6.55 (2023-03-23)

### :green_apple: Chore

* Zip only executable for arm (57dfc4d4)

# 0.6.54 (2023-03-18)

### :sparkles: Features

* Support directory-specific edits (.oculante file). If such an edit file is present, the edit operations will be applied to any image.
* Minor UI tweaks
* The release process now builds `armv7-unknown-linux-gnueabihf` (Raspberry pi and others) and includes it in the release. This is Oculante with minimal features for now, with some external libraries disabled (have a look at Cargo.toml for details what is left out)

# 0.6.53 (2023-03-04)

### :beetle: Bug Fixes

* Prevent freezing when window resizes (91424bac)
* update jpegxl (8779d04b)

### :sparkles: Features

* Allow window title to be configured (000a34db)
* Keep track of recently opened images (77857a8f)

### :green_apple: Chore

* update dependencies (2dad8909)
* Update dependencies (8c78fa9f)

# 0.6.52 (2023-02-19)

# 0.6.51 (2023-02-12)

### :sparkles: Features

* Add multiply / divide by aplha operator (8b3eda86)
* Add window and taskbar icon (32900ab5)

### :green_apple: Chore

* update dependencies (92f3eb87)
* Update resvg and usvg (c2f96b47)
* update notan and rfd (6e0c00c2)

# 0.6.50 (2023-01-16)
* AVIF support

There are two features to choose from: `avif_native` (default, less images supported) and `dav1d` (optional, harder to build, better support)
`david` requires meson, ninja and nasm at least.

### :sparkles: Features

* RAW file support (02fa90e2)

# 0.6.39 (2023-01-07)

### :beetle: Bug Fixes

* slider is 1-based (fixes #116) (63226d5e)

### :green_apple: Chore

* update deps (2bc54c8f)

# 0.6.38 (2023-01-05)

### :beetle: Bug Fixes

* Reverse PanUp/Down (fixes #110) (89e43ef8)
* Shortcuts are sorted and grouped (8e6d2430)

### :sparkles: Features

* add home/end to move to first/last image (39412c7f)
* Add slider to step through images (5934b052)

# 0.6.37 (2023-01-02)

# 0.6.36 (2023-01-01)

### :beetle: Bug Fixes

* Make it possible to pass a folder-path as a command-line arg, instead of requiring a file within that (61547f46)
* Use Natural Sorting for filenames (d7783bd8)
* Prevent old settings file from becoming invalid (fixes #103) (10573c1b)

### :sparkles: Features

* Ctrl-O and/or F1 bring up a file browser dialog to select an image to load (8778b92c)
* Go to Next/Prev now cycles through the images in the folder, instead of stopping at either end (6d2cd8cc)
* Ctrl-Scrollwheel can be used to go to the next/prev images too (77154a1f)

### :green_apple: Chore

* update clap (c08f5f1a)
* update rfd and self_update (8ba00d8e)
* Update Changelog with the missing revision ID's (01f7bad3)
* Split out the list of supported image formats to a constant (SUPPORTED_EXTENSIONS) (60762f49)
* Update Changelog with recent changes (c4ab7fe7)

# 0.6.35 (2022-12-30)

### :sparkles: Features

* Enable persistent offset/zoom in settings (20e33e14)

### :green_apple: Chore

* remove edit/info checkboxes (11613c21)

# 0.6.34 (2022-12-19)

### :beetle: Bug Fixes

* Correct offset when entering/exiting full-screen mode (2ffe2d03)

### :green_apple: Chore

* Enhance crop precision (3b02a304)

# 0.6.33 (2022-12-18)

# 0.6.32 (2022-12-13)

### :sparkles: Features

* Mipmap generation (smoother images when zoomed out) and correct gamme when zooming (SRgba8 format) (b83b1c65)

# 0.6.31 (2022-12-13)

# 0.6.30 (2022-12-12)

### :sparkles: Features

* Correct gamma scaling and SIMD speedup (21d7159b)

### :green_apple: Chore

* update dependencies (1c73246b)

# 0.6.29 (2022-12-12)

### :beetle: Bug Fixes

* Support lossless ops on jpeg and jpg (757b29fc)

# 0.6.28 (2022-12-11)

### :beetle: Bug Fixes

* Allow building without default features (10a0f6a4)

# 0.6.27 (2022-12-10)

# 0.6.26 (2022-12-09)

# 0.6.25 (2022-12-08)

# 0.6.24 (2022-12-08)

### :sparkles: Features

* Lossless JPEG editing (2b4e4d40)

# 0.6.23 (2022-12-03)

### :beetle: Bug Fixes

* Histogram was not computed on image change (2096104a)

# 0.6.22 (2022-11-13)

### :sparkles: Features

* Save/load edit information in metafile. This allows non-destructive eding while leaving your original pictures intact. (c47bddb6)

### :green_apple: Chore

* Update SVG rendering (9fdc2e56)
* Slightly relax & update dependencies (bb9c03a8)

# 0.6.20 (2022-10-30)

### :beetle: Bug Fixes

* Support bad Gif data gracefully (fixes #60) (c0acfa69)
* Build script generates app icon on windows (548b9749)

# 0.6.19 (2022-10-25)

### :beetle: Bug Fixes

* Prevent thread crashing when opening corrupt images (3360dc7f)

# 0.6.18 (2022-10-22)

### :beetle: Bug Fixes

* Remove UI flicker if alpha tools are expanded/closed (1254dffc)
* Network listen mode now refreshes UI and has a dedicated unit test (00c7a91b)

### :sparkles: Features

* Enable EXIF support (37aeda9d)

# 0.6.17 (2022-10-17)

### :sparkles: Features

* Keep image centered on window resize (a8ca6f1e)

# 0.6.14 (2022-10-14)

### :beetle: Bug Fixes

* Fix unreliable gif loading (928610b6)


# 0.6.13 (2022-10-10)

### :green_apple: Chore

* update arboard and notan (4cb66206)


# 0.6.12 (2022-10-03)

### :beetle: Bug Fixes

* Change windows release to use windows server 2019 (bb740e12)

# 0.6.11 (2022-10-01)

### :beetle: Bug Fixes

* Re-enable blur (fixes #52) (e33d27db)

# 0.6.10 (2022-09-30)

### :beetle: Bug Fixes

* Tooltip colors automatically contrast theme color (51eee15e)

### :sparkles: Features

* Add always on top mode (a8fdc891)
* Filter with custom expressrion per pixel (afa438fe)

### :green_apple: Chore

* update dependencies (72ac0dce)

# 0.6.9 (2022-09-11)

### :beetle: Bug Fixes

* Enable correct accent color selection by changing layout (fixes #48) (a63cc859)

### :sparkles: Features

* Better operator layout, fixes quirky color picking in operator menu (627ace1c)

# 0.6.8 (2022-09-07)

### :beetle: Bug Fixes

* Remove offset when initially clicking into OSX window (81544cc4)

### :sparkles: Features

* Persistent settings support. Vsync and color theme are now customizable. (21ed3954)

### :green_apple: Chore

* Update psd, ext, dds-rs (ad2f531b)

# 0.6.7 (2022-09-06)

### :beetle: Bug Fixes

* Disable image center on window resize, as this caused jumping (ee557d47)

### :sparkles: Features

* Add Posterize image effect (3e019728)
* Equalize image operator added (748bf15e)
* Allow editing the export image extension to save as a different image format (23519eee)

# 0.6.6 (2022-09-01)

### :sparkles: Features

* Channel  Copy filter replaces Swapping - this brings more flexibility. Fill operator is now supporting the alpha channel to blend the color. (670ecaac)
* Improved UI slider widgets (9a3d2b20)
