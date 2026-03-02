# Board Art Display

A single-page HTML app that displays a Google Slides presentation fullscreen — designed for digital display boards, kiosks, or any screen that needs to cycle through slides on its own.

## How It Works

The page embeds a published Google Slides presentation in a borderless, fullscreen iframe. Slides auto-advance and loop continuously with no user interaction required.

## Usage

1. Open `index.html` in a browser (or point your display board's browser to it).
2. The slides will start playing automatically.

That's it — no server, no build step, no dependencies.

## Customization

Open `index.html` and find the `<iframe>` tag. You can change:

- **Slides URL** — Replace the `src` value with your own Google Slides embed link.
  To get one: open your presentation in Google Slides, go to **File > Share > Publish to web > Embed**, and copy the URL.
- **Slide delay** — Change `delayms=600000` to your preferred delay in milliseconds.
  For example: `60000` = 1 minute, `300000` = 5 minutes, `600000` = 10 minutes.
- **Auto-advance** — Set `start=false` if you don't want slides to advance automatically.
- **Looping** — Set `loop=false` to stop after the last slide.

## Crop Tool

Most art doesn't match the board's 16:9 aspect ratio. `crop.html` is a browser-based tool that makes it easy to crop any image to the right size before adding it to Google Slides.

### How to use it

1. Open `crop.html` in your browser (just double-click the file).
2. Load an image — three ways:
   - **Drag and drop** a file onto the page
   - **Paste a URL** into the input field
   - **⌘V** to paste an image from your clipboard
3. Adjust the crop by dragging and zooming. The crop box is locked to 16:9.
4. Check the resolution indicator at the bottom — green means sharp on the board, amber means it may look blurry.
5. Click **Download PNG** to save a 1920×1080 image ready for Google Slides.
