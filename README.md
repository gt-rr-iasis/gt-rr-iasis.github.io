# GT-RR-IASIS website

Website of the working group on reproducible research in signal and image processing (GdR IASIS, CNRS), published at <https://gt-rr-iasis.github.io>.

Built with [Jekyll](https://jekyllrb.com/) from [academic-website-template](https://github.com/sbryngelson/academic-website-template) (MIT, see `LICENSE`).

## Editing content

| What | Where |
| --- | --- |
| Home page text | `_pages/home.md` |
| News (3 latest in the sidebar, all on `/allnews.html`) | `_data/news.yml` |
| Site name, links, contact email, accent color | `_config.yml` |
| Images | `images/` |

To add a page, create `_pages/<name>.md` with `layout: gridlay` and `permalink: /<name>/` in its front matter, then add `- name: <name>` under `nav_pages` in `_config.yml` to show it in the navbar.

## Local preview

```bash
bundle install
bundle exec jekyll serve
```

Then open <http://localhost:4000>.

## Deployment

Pushing to the `source` branch triggers `.github/workflows/deploy.yml`, which builds the site and publishes it with GitHub Pages.
