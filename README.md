# cubedeck-web

**CubeDeck** — fifteen switchable tools for the YouTube web interface, in one
browser extension — behind a password gate.

**https://hero-999-dev.github.io/cubedeck-web/**

## What is here

Behind the gate: the current `CubeDeck-<version>.zip` and `index.html`, a
single-page documentation of the whole project — architecture, a mind map,
every widget, the layout maths, network calls, performance work and tests. Open
that file in any browser; no internet needed after the download.

The extension source lives in a private repository, so **this is the public
entrance**. Nothing here has to be cloned.

## The gate

`index.html` asks for a password and derives
`p-<sha256("cubedeck:<password>")[:20]>/` in the browser. Neither the password
nor the directory name is in the page source; a wrong password requests a
directory that does not exist and gets a 404.

It locks the **link**, not the content: this repository is public, so anyone
browsing it sees the directory. The gate keeps a URL from travelling further
than it was handed. Nothing that would be a problem to read goes behind it.

## Installing what you download

1. Unzip. You get a `CubeDeck` folder (with `manifest.json`) and `index.html`.
2. Open your browser's extension page — `chrome://extensions`,
   `edge://extensions`, `brave://extensions`, `opera://extensions`,
   `vivaldi://extensions`. The addresses are the same on macOS.
3. Turn on **Developer mode**.
4. **Load unpacked**, and pick the `CubeDeck` folder.
5. Open YouTube and reload the tab.

Works on Windows, macOS and Linux — a browser extension is not
platform-specific.
