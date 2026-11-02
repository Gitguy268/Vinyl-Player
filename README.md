Vinyl Record Player
===================

A single-file, browser-based vinyl turntable that plays your own local audio
files with a spinning-record animation, a draggable tonearm, scratch effects,
and a built-in EQ. Everything runs client-side in one HTML file. No server,
no accounts, no external audio services.


Getting Started
---------------

1. Open index.html in any modern web browser (Chrome, Edge, Safari,
   Firefox).
2. Click "Add audio files" or drag & drop audio files onto the page.
3. Press Play, or drag the tonearm onto the record to drop the needle.

That's it. Your tracks and settings are saved locally in the browser, so
they'll still be there next time you open the file on the same device.


Adding Music
------------

- "Add audio files" button: pick one or more files.
- Drag & drop: drop audio files (or a cover image) anywhere on the page.
- Supported formats: MP3, WAV, OGG, FLAC, M4A, AAC, OPUS, WMA (whatever your
  browser can decode).
- ID3 tags are read automatically, so title, artist, album, year, genre, and
  embedded cover art are filled in when available.


Playback Controls
------------------

- Play / Pause, Previous, Next.
- Shuffle and Repeat (Off / One / All).
- RPM selector: 33 1/3, 45, or 78 — changes both pitch and spin speed.
- Volume slider.
- Tonearm: drag it onto the record to play; lift it to pause. Where you drop
  the needle seeks to that position in the track.
- Spin the record with the mouse to scrub through the track.


Sound Effects & EQ
------------------

- 3-band EQ: Bass, Mid, Treble.
- Graphic EQ panel: Winamp's ten bands and preamp after the 3-band EQ, its 17
  presets, and loading of Winamp .eqf preset files. Off by default; a trim
  ahead of it takes back any boost so it does not clip.
- Vinyl noise: adds analog crackle while playing.
- Scratch mode: turn the record by hand for a DJ-style scratch sound.
- Effects toggle: enables/disables the mechanical click and clunk sounds.
- A bass-reactive glow ring pulses around the label while music plays.
- Visualizer: Lines (a ridgeline), Scope, Spectrogram or Radial covers the
  label while a record plays. Off by default and under reduced motion.


Appearance
-----------

- Themes: Minimal, Wood, and Clear (a frosted "liquid glass" look).
- Light / dark mode toggle.
- Custom colors: set Accent, Background, Panel, and Text colors via the color
  pickers or by typing hex codes. (Custom colors override the light/dark
  toggle — reset them to use the toggle again.)
- Focus mode: hides everything except the record and a floating control bar
  for distraction-free listening.
- Record Info panel: view and edit track and album details, including your
  own liner notes.
- Desktop: the library as a desktop, with artists and albums as folders in
  movable windows. Double-click a track, or drag it onto the Turntable icon,
  to play it. Escape closes the front window, then the desktop.


Keyboard Shortcuts
------------------

- Space        Play / Pause
- Left Arrow    Seek back 5s (or previous track near the start)
- Right Arrow   Seek forward 5s
- Up Arrow      Volume up
- Down Arrow    Volume down
- S             Toggle shuffle
- R             Cycle repeat mode
- F             Toggle focus mode
- Escape        Exit focus mode


Data & Privacy
--------------

- Everything happens locally in your browser. No files are uploaded anywhere.
- Tracks are stored in the browser's IndexedDB; preferences and album info are
  stored in localStorage. The graphic EQ is kept under its own keys
  (vinyl-eq, vinyl-eq-presets). The other vinyl players read them
  too when opened as local files in the same browser.
- Clearing your browser's site data for this file will remove saved tracks and
  settings.


Requirements
------------

- A modern browser with Web Audio API and IndexedDB support.
- An internet connection on first load (the styling library is loaded from a
  CDN). The rest works offline.


Files
-----

- index.html   The entire application (HTML, CSS, and JavaScript).


License and attributions
------------------------

MIT. See LICENSE.

- The graphic EQ uses the band layout and the 17 built-in preset values of
  Webamp (https://github.com/captbaritone/webamp, MIT, copyright 2015 Jordan
  Eldredge); its .eqf reader is written from Webamp's format notes. No Winamp
  skin or artwork is used. Winamp is a trademark of its owner; this project
  is not affiliated with Winamp, Nullsoft or Webamp.
- The library desktop follows the idea of Winampify
  (https://github.com/remigallego/winampify, MIT). No code was taken.
- The Lines, Scope, Spectrogram and Radial visualizers are ideas found through
  awesome-audio-visualization
  (https://github.com/willianjusten/awesome-audio-visualization, CC0), among
  them its "Lines" experiment and the "Awesome Audio Player" and
  "CircleLineNERDDISCO" pens. They are drawn from scratch.
