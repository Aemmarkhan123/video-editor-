# Reel — Video Remix Studio

A lightweight, browser-based video remix studio with a matte-black and off-white interface. Import local video files, arrange clips on a timeline, make basic edits, and export the result.

## Features

- **Local video import** — Upload or drag and drop supported video files.
- **Media library** — Browse imported videos, search by filename, switch between grid and list views, rename media, or remove it.
- **Timeline editing** — Add clips to the timeline, move them, and adjust their in/out points.
- **Split clips** — Split a clip at the playhead.
- **Duplicate and delete** — Duplicate clips or remove a selected clip from the timeline.
- **Playback controls** — Preview the edit, seek through the timeline, and use fullscreen preview.
- **Per-clip controls** — Adjust playback speed, volume, and mute settings for individual clips.
- **Undo and redo** — Revert or restore recent timeline changes.
- **Export** — Record the timeline preview and download the result in a format supported by your browser.
- **Local persistence** — Store imported media and project timeline data in the browser using IndexedDB.
- **Responsive layout** — Includes a compact layout for smaller screens.

## Tech Stack

- HTML
- CSS
- JavaScript
- Browser APIs: IndexedDB, MediaRecorder, `HTMLMediaElement`, and `captureStream()`

## Project Structure

This project is currently implemented as a single HTML file:

```text
Reel/
└── Reel — Video Remix Studio.html
```

## Getting Started

### Option 1: Open the HTML file

1. Download or clone this project.
2. Open `Reel — Video Remix Studio.html` in a modern browser.
3. Upload a local video and start editing.

### Option 2: Serve it locally

You can also serve the file through a local HTTP server from the directory containing it:

```bash
python3 -m http.server 8000
```

Then open:

`http://localhost:8000/Reel%20%E2%80%94%20Video%20Remix%20Studio.html`

## How to Use

1. **Import videos:** Select **Upload video** or drag video files onto the Home panel.
2. **Open the Media Library:** Search and manage imported media.
3. **Add clips:** Choose **Remix** on a media item, or add it from the Media panel in the studio.
4. **Edit the timeline:** Drag clips to reposition them. Drag the clip edges to change the in/out points.
5. **Adjust clip settings:** Select a clip to change its name, timeline position, trim points, speed, volume, or mute state.
6. **Split or duplicate:** Move the playhead to the desired point and use **Split**; use **Duplicate** to add another copy of a selected clip.
7. **Export:** Choose **Export**, select a quality setting, and start the recording. Keep the browser tab open and in the foreground until export finishes.

## Keyboard Shortcuts

| Shortcut | Action |
|---|---|
| `Space` | Play or pause |
| `S` | Split at the playhead |
| `Delete` / `Backspace` | Delete the selected clip |
| `Ctrl` / `Cmd` + `Z` | Undo |
| `Ctrl` / `Cmd` + `Shift` + `Z` | Redo |
| `Left Arrow` / `Right Arrow` | Move the playhead |
| `Shift` + `Left Arrow` / `Right Arrow` | Move the playhead by larger steps |
| `Esc` | Close the export dialog |

## Export Notes and Limitations

- Export records the preview in **real time**, so longer timelines take longer to export.
- Keep the tab open and in the foreground during export.
- Export formats depend on browser support for `MediaRecorder` and `captureStream()`. Recent versions of Chrome, Edge, or Firefox are recommended.
- The selected quality setting controls the recording bitrate; the final format and quality depend on browser support and source media.
- This project provides basic clip editing, not a full nonlinear editor. It does not currently include a dedicated multi-track audio editor, transitions, titles, or advanced effects.
- Imported media and project data are stored in the current browser's IndexedDB. They are not automatically synced across browsers or devices. Clearing browser site data may remove saved media and project data.

## Privacy

Video files are processed locally in your browser by this application. The current implementation does not upload video files to a remote backend.

## Contributing

Contributions, bug reports, and suggestions are welcome.

1. Fork the repository.
2. Create a branch for your changes.
3. Commit your changes with a descriptive message.
4. Open a pull request.

## License

No license has been specified. Add a `LICENSE` file before distributing the project under specific open-source terms.

---

Built with HTML, CSS, and JavaScript.
