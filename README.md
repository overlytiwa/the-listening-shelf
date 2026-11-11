# The Listening Shelf

The albums that inspire me, collected on an interactive 3D shelf of worn VHS sleeves, paper textures, and nostalgia

![The Listening Shelf](docs/shelf-preview.png)

A personal music archive by Tiwa. The collection holds 37 releases in a hand-picked order, opening on *Donda*. Each album becomes a physical sleeve with worn printing, paper fibres, folded cardboard edges and its own colour palette.

## Explore

- Drag, swipe, scroll or use the arrow keys to browse the continuous shelf
- Jump between release decades
- Open a sleeve to see the original high-resolution artwork and a link to listen
- Use Enter to open and Escape to return

The cases turn in 3D and react to the pointer. Detail pages unfold from the selected sleeve, with the artwork appearing through an ink reveal. Touch controls, visible keyboard focus and reduced-motion preferences are supported. The animation loop sleeps when the shelf settles.

## Run locally

This is a static website built with HTML, CSS and vanilla JavaScript. There are no dependencies to install and no build step.

Serve this directory with a static web server. For example, with Python installed:

```sh
python -m http.server 5177
```

Then open [localhost:5177](http://localhost:5177).

Deploy the same directory to any static host.

## Customize the collection

Edit `albums.js` to change the collection. Each release contains its title, artist, year, artwork paths, sleeve colours and listening link. Optional personal notes can be supplied through `note` and `description`. Set `window.TIWA_FIRST_ALBUM` to the zero-based index of the opening release.

The shelf follows the array order. Album and artist capitalization is retained exactly as written.

## Files

- `index.html` — layout, styling, motion and interactions
- `albums.js` — the ordered collection and release metadata
- `assets/artwork/` — locally hosted shelf and detail artwork
- `assets/materials/` — generated paper-fibre and worn-print materials
- `fonts/` — locally hosted Newsreader and Inter Tight fonts
- `ARTWORK-SOURCES.md` — official release sources and original artwork dimensions

## Credits

Album artwork belongs to the respective artists, labels and rights holders. See [the artwork catalogue](ARTWORK-SOURCES.md) for the official sources. The paper materials were created with image generation. Fonts use the SIL Open Font License, with license texts in `fonts/licenses/`. Interface SVG icons use Lucide; its license is included in `assets/lucide-license.txt`.
