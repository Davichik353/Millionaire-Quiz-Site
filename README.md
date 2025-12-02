# Millionaire Quiz Site — Local Run Instructions

To run the game locally like a normal site, follow these steps:

1. Place `Millionaire_Quiz _ite.html` (this file) and any local audio files (e.g., `q1-5-bed-2008.mp3`) in the same folder.
2. Open a terminal (PowerShell) in the folder and run a simple HTTP server. This is recommended because some browsers restrict audio and other features for `file://` pages. For the easiest experience, rename the file to `index.html` so visiting `http://localhost:8000/` opens the game directly.

PowerShell / Python 3 (if python is installed):

```powershell
# run in the directory containing the files
python -m http.server 8000
# open http://localhost:8000/Millionaire_Quiz %20_ite.html in your browser
```
Or, if you renamed to `index.html`:
```powershell
# visit http://localhost:8000/
```

3. If you don't have Python, you can right-click the HTML file and choose "Open with" and select a modern browser — but running a local server is preferred.

4. Audio: The page expects `q1-5-bed-2008.mp3` next to the HTML file. If it's missing, the site attempts to use a remote fallback audio track.

5. If audio doesn't autoplay, click "Воспроизвести музыку" to start the background audio.

6. If you run into any problems, please open the browser DevTools (F12) and check the console for errors.

If you'd like, I can also add a proper local `index.html` and a small folder structure for assets (audio, images) and update in-file audio paths.

Local domain (hosts) testing
---------------------------------
If you'd like to use a custom local domain (for example `mytestsite.local`) for testing, add an entry to your hosts file (Windows):

```powershell
# as Administrator, edit C:\Windows\System32\drivers\etc\hosts
# add the following line (example):
127.0.0.1    mytestsite.local
```

Then visit: http://mytestsite.local:8000/ (or just http://mytestsite.local/ if you use port 80).

Custom domain for deployment
---------------------------------
If you want to use a real domain for the live site, add a `CNAME` file to the repo with your domain (this repo contains a `CNAME` with `example.com` currently). Configure your DNS provider: point the apex or `www` record to the host provider (GitHub Pages: A or CNAME records). If you provide a domain, I can replace `example.com` in the `CNAME` with your actual domain.