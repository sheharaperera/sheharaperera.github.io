# sheharaperera.github.io

Source of Shehara Perera's website, https://sheharaperera.github.io, built with [Hugo](https://gohugo.io/) and the [PaperMod](https://github.com/adityatelange/hugo-PaperMod) theme. It deploys to GitHub Pages from `main` via `.github/workflows/hugo.yml`.

## Run locally

```
hugo server -M
```

`-M` renders in memory so nothing is written to `public/`.

## Folder guide

```
config.yml              Site settings: name, bio line, buttons, social icons, menu
content/                What the pages say
  _index.md               About paragraph on the home page
  papers/                 One file per publication (a card, not a page)
  teaching/ software/ fun/  Section pages
data/
  news.yml                News list on the home page
  themes.yml              Research areas (section headings on the Publications page)
static/                 Files copied to the site as-is
  images/                 Publication thumbnails (png/jpg)
  picture.jpeg            Profile photo; favicons
assets/
  css/variables.css       Colours, text sizes, widths: change the look here
  css/layout/             Page structure (header, main, home profile)
  css/components/         Home sections and publication cards
  figure-sources/         Original figure PDFs the thumbnails were made from (not published)
layouts/                Page templates
  _default/               Base page, generic section page, link rendering
  papers/list.html        Publications page (grouped by research area)
  partials/               Reusable pieces: head, header, home profile, home sections,
                          publication card and list item, social icons, math
themes/PaperMod/        The theme (unmodified; overridden by layouts/ and assets/)
frontmatter.json        Settings for the Front Matter VS Code extension
```

## Changing things

| To change | Edit |
| --- | --- |
| Bio line under the name, buttons, social links, menu | `config.yml` |
| About paragraph | `content/_index.md` |
| News | `data/news.yml` |
| Research area names or order | `data/themes.yml` |
| Colours, text sizes, page width | `assets/css/variables.css` |
| Contact section on the home page | `layouts/partials/home_sections.html` |

## Adding a publication

Copy an existing file in `content/papers/` and edit its front matter:

- `date`: publication date (cards are sorted newest first within each area)
- `venue`: label shown on the card, e.g. `"IEEE Access 2023"`
- `theme`: an `id` from `data/themes.yml`
- `selected: true`: also list it under Recent Publications on the home page
- `author`: full names; "Shehara Perera" is shown in bold, others by last name
- `link`: target of the PDF button
- `abstract`, `bibtex`: shown when hovering the Abstract and BibTeX buttons
- `cover` (optional): thumbnail, with `image: "/images/<file>"` (a file in `static/images/`) and `alt`

Publication files have no body: each paper is a card, not a page.

## License

Except where otherwise noted, the website's content was created by Shehara Perera and is licensed under the [Creative Commons Attribution 4.0 International License](http://creativecommons.org/licenses/by/4.0/).
