# davidebazzana.github.io

Personal research page, published with [GitHub Pages](https://pages.github.com/).
GitHub builds the site automatically (with Jekyll) every time you push to `main`,
so there is no build step on your side: edit a file, commit, push.

## Where to edit what

All the content lives in a handful of small text files. You never need to touch
the HTML or CSS.

| To change...                                  | Edit this file           |
| --------------------------------------------- | ------------------------ |
| Name, initials in the badge, role, email, links, office | `_data/profile.yml` |
| Opening sentence and biography ("About")      | `index.md`               |
| Research interests (the cards)                | `_data/research.yml`     |
| Publications                                  | `_data/publications.yml` |
| Courses                                       | `_data/teaching.yml`     |
| News items                                    | `_data/news.yml`         |
| Browser-tab title, site description, footer   | `_config.yml`            |

Every file has comments at the top explaining its fields. The general rules:

- Files in `_data/` are [YAML](https://learnxinyminutes.com/docs/yaml/): keep the
  indentation, and wrap a value in double quotes if it contains a colon (`:`).
- A section (Research, Publications, Teaching, News) disappears from the page and
  from the side menu when its file has no entries. To hide one, delete its entries
  or leave only comments in the file.
- Text fields accept simple HTML, e.g. `<em>italics</em>` or
  `<a href="https://...">a link</a>`.
- The biography in `index.md` is Markdown: blank lines separate paragraphs,
  `*italics*`, `**bold**`, `[text](https://url)` for links.
- Publications are shown in the order you list them, with a year heading each time
  the year changes. Keep entries of the same year together, newest year first.
- The "Last updated" date in the footer is set automatically at build time.

## Look and layout

`assets/css/style.css` holds the styling (colours are the `--...` variables at the
top). `_layouts/default.html` is the page template; only edit it if you want to
add a new kind of section.

## Previewing on your own machine (optional)

Requires Ruby with Bundler. From the repository folder:

```bash
bundle install
bundle exec jekyll serve
```

Then open <http://localhost:4000>. Pushing to GitHub is enough otherwise; the
live site updates about a minute after each push (check the *Actions* tab of
the repository if it does not).
