# ChordScope

Browser-only song key and chord finder. No server, no build step.

## Put it on GitHub Pages
1. Create a new GitHub repository and upload `index.html` (and this README).
2. Go to **Settings → Pages**, choose **Deploy from a branch → main → / (root)**, and save.
3. After a minute your app is live at `https://<your-username>.github.io/<repo-name>/` and works on phone and PC.

## Notes
- Chords and key are detected on-device from the audio (chroma analysis, key profiles, Viterbi smoothing). Accuracy is best on clear, band-style recordings; major and minor triads only.
- Links must point to a file that allows cross-origin access. YouTube, Spotify and similar sites cannot be read from a browser-only app. Doing that needs a small backend (for example one using `yt-dlp`).
- Automatic lyrics use Whisper (tiny) through transformers.js, downloaded from a CDN on first use.
- PDF export uses jsPDF from cdnjs.
