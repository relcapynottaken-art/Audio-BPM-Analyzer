# Tempo — BPM Analyzer

Drop an mp3 or wav file and it calculates the BPM using a multi-band beat detection algorithm that filters out hi-hats and vocals to focus on kick and bass frequencies, so the result is actually accurate. Everything runs locally in your browser, nothing gets uploaded anywhere.

Once it loads you get a zoomable, pannable waveform that you can scroll through and inspect at whatever resolution you want. Zoom all the way in to check individual transients or zoom out to see the full track. You can click anywhere on the waveform to seek, drag to pan, and use the scroll wheel to zoom in and out. Results get cached so if you drop the same file again it skips the analysis and loads instantly.

There's also a Dead As Disco mode for people making custom song maps in that game. Toggle it on and it calculates two things: the Audio Lag (the offset in milliseconds from the start of the file to the first beat) and both the original and doubled BPM, which is what most mappers prefer for finer placement. The waveform gets a pink beatline overlay so you can visually verify the grid is lining up with the actual peaks before copying the values into the Advanced Editor.

## Usage

Open `index.html` in any modern browser. No build step, no server, no dependencies.

## Features

- BPM detection via two-pass offline audio filtering (kick band + sub band)
- Zoomable and pannable waveform with scroll-wheel zoom and drag-to-pan
- Click anywhere on the waveform to seek
- Results cached in localStorage so repeat loads are instant
- Dead As Disco mode with Audio Lag offset, original and doubled BPM, and pink beatline overlay
- Fully client-side, no data leaves your device
