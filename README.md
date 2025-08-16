# YouTube Video Downloader (Tkinter + youtube_dl)

This is a simple Python GUI application for downloading YouTube videos using **[youtube_dl](https://github.com/ytdl-org/youtube-dl)** and **Tkinter**.

---

## Features
- GUI-based YouTube video downloader
- Allows browsing and selecting the download directory
- Simple, minimal interface
- Downloads videos in their original format

---

## Requirements

- Python 3.x
- Packages:
  - `youtube_dl`  
  - `tkinter` (comes pre-installed with Python on most systems)
  - `os` (built-in)

Install `youtube_dl`:
```bash
pip install youtube_dl
```

---

## Usage

1. Clone or download this script.
2. Run the script:
```bash
python youtube_downloader.py
```
3. In the GUI:
   - Paste the YouTube video link.
   - Select a destination folder.
   - Click **DOWNLOAD video**.

---

## File Structure
```
youtube_downloader.py   # Main application script
```

---

## Code Overview
- **CreateWidgets()**: Creates and places Tkinter widgets.
- **Browse()**: Lets you choose a folder to save the downloaded file.
- **Download()**: Uses `youtube_dl` to download the YouTube video.
- **paste()**: Placeholder function for clipboard paste (not used in current version).

---

## Example
1. Enter a YouTube link in the **YOUTUBE LINK** field.
2. Click **BROWSE** to choose where the file should be saved.
3. Click **DOWNLOAD video** to start downloading.
4. Once complete, a **SUCCESS** message will pop up.

---

## Notes
- This version downloads the video in its default available format.  
- To customize download options (e.g., MP3, resolution, etc.), modify the `audDWLDopt` dictionary in the code.

Example for downloading audio as MP3:
```python
audDWLDopt = {
    'format': 'bestaudio/best',
    'postprocessors': [{
        'key': 'FFmpegExtractAudio',
        'preferredcodec': 'mp3',
        'preferredquality': '192',
    }]
}
```
