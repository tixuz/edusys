# Photos folder

Save the 5 selfies from the chat under these exact filenames so the `<img src="photos/...">` tags in `index.html` resolve:

| Filename                      | Source photo                                                         | Where it appears in `index.html`                                     |
|-------------------------------|----------------------------------------------------------------------|----------------------------------------------------------------------|
| `khindol-sagalassos.jpg`      | Red jacket, Roman ruins at Sagalassos (Turkey)                       | Hero — floating portrait next to "Career Snapshot" card              |
| `khindol-warm.jpg`            | Colorful backdrop, warm smile (head-and-shoulders)                   | Chat widget — header avatar, replaces the robot icon                 |
| `greek-inscription.jpg`       | The stone reading `ΟΣΙΩ ΚΑΙ ΔΙΚΑΙΩ` ("piously and justly")            | Publications section — thematic illustration next to the book copy   |
| `apollo-temple.jpg`           | Temple of Apollo, Side, Turkey                                       | Case Studies — intro banner                                          |
| `singapore-marina.jpg`        | Marina Bay Sands skyline, Singapore 2022                             | "Work in the open" — side illustration                                |

## Recommended export

Long edge 1200–1600 px, JPEG quality ~82, stripped EXIF. Anything bigger just slows the page for no visual gain — these are all displayed at ≤ 480 px wide.

```bash
# example (ImageMagick)
magick input.jpg -auto-orient -strip -resize 1400x -quality 82 photos/khindol-sagalassos.jpg
```

## Layout notes

- The hero portrait uses the existing `.hero-badge-float` drift animation — if that looks busy, drop the `hero-photo-float` class and the image becomes static.
- The chat avatar uses a circular mask with the same palette as the widget — no extra work to wire up.
- All `<img>` tags already have `alt` text, `loading="lazy"`, and sensible aspect ratios. If a photo is missing the layout still holds (empty box with alt text), so the site never crashes on a broken path.
