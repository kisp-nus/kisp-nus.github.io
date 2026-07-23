# KISP Lab website

The one-page website for the [NUS KISP Lab](https://kisp.comp.nus.edu.sg/), built with
[Jekyll](https://jekyllrb.com/) and deployed to GitHub Pages. It is **data-driven**: page
content lives in YAML files under `_data/onepage/`, and the layouts render it.

Two homepage designs live side by side and share the same content:

- **v1** — the classic design (current default at `/`)
- **v2** — a modern redesign (light/dark theme, responsive)

## Local development

Requires Ruby and Bundler. From the repo root:

```bash
bundle install            # first time only
bundle exec jekyll serve  # build + serve with live reload
```

Then open:

- <http://localhost:4000/> — the default homepage
- <http://localhost:4000/v1/> — always the classic design
- <http://localhost:4000/v2/> — always the modern design

## Repository structure

```
_data/onepage/*.yml          Content shared by BOTH versions (edit once):
                               members.yml, news.yml, projects.yml, publications.yml

index.md                     The default homepage served at "/". Picks the layout.
index_v1.md / index_v2.md    Always-on previews at /v1/ and /v2/.

_layouts/
  v1/{home,default}.html     Classic page composition + HTML skeleton
  v2/{home,default}.html     Modern page composition + HTML skeleton
  archive/…                  Legacy multi-page layouts (not used by the live site)

_includes/
  v1/*.html                  Classic sections: head, header, slogan, intro, news,
                               projects, people, publications, footer
  v2/*.html                  Modern sections (same set)
  archive/…                  Legacy partials

assets/
  v1.css                     Classic styles (prebuilt export)
  v2.css                     Modern styles (hand-written: design tokens + light/dark)
  people/  projects/  …      Images

.github/workflows/jekyll.yml Builds and deploys to GitHub Pages on every push to `main`
CNAME                        Custom domain (kisp.comp.nus.edu.sg); TLS auto-provisioned
                               by GitHub via Let's Encrypt
archived/                    Old multi-page site + blog (excluded from the build)
```

The flow for the default page: `index.md` → `_layouts/v1/home.html` (pulls in the section
partials from `_includes/v1/`) → `_layouts/v1/default.html` (the surrounding HTML). v2 works
the same way through its `v2/` folders.

## Choosing which version is the default homepage

The homepage at `/` is decided by the `layout:` field in `index.md`:

```yaml
# index.md
layout: v1/home   # classic (current default)
# layout: v2/home # modern
```

Change that one line and commit to switch which design is live at `/`. `/v1/` and `/v2/`
stay available either way. (This lives in `index.md` rather than `_config.yml` on purpose:
`jekyll serve` does not reload `_config.yml`, so keeping the switch here avoids breaking a
running dev server.)

---

## Updating content

All content is in `_data/onepage/`. Because both versions read the same files, you edit once
and both `/v1/` and `/v2/` update.

### Personal profiles — `_data/onepage/members.yml`

Add your entry under the matching `kind` section (e.g. `faculty`, `research_fellows`,
`graduate_students`, `alumni`):

```yaml
    - name: Ruishi Li
      image: ./assets/people/member_ruishi.jpg
      website: https://zero0one1.github.io/
      github: https://github.com/Zero0one1
      linkedin: https://www.linkedin.com/in/ruishili/
      twitter: https://twitter.com/xx
```

Then upload your photo to `assets/people/` (e.g. `assets/people/member_<name>.jpg`).

### Publications — `_data/onepage/publications.yml`

Add newest first (at the top of the list):

```yaml
- title: "Translating C To Rust: Lessons from a User Study"
  authors: ["Ruishi Li*", "Bo Wang*", "Tianyu Li", "Prateek Saxena", "Ashish Kundu"]
  venue: "NDSS Symposium 2025"
  shortVenue: "NDSS 2025"
  location: "San Diego, CA"
  date: "February 2025"
  links:
    - {type: "PDF", url: "https://arxiv.org/abs/2411.14174"}
    - {type: "Artefact", url: "https://doi.org/10.5281/xx"}
    - {type: "Video Demo", url: "https://youtube.com/watch?v=xx"}
  recent: true
```

### Projects — `_data/onepage/projects.yml`

```yaml
- name: Capstone
  fullname: Capability-based Architectural Foundation for Expressive Security
  description: How can the computer architecture provide principled and provable support for diverse software security needs? Capstone provides an answer!
  url: https://capstone.kisp-lab.org/
  image: ./assets/projects/capstone.png
```

Upload the project icon to `assets/projects/`.

### News — `_data/onepage/news.yml`

Add newest first. Markdown links are supported in `content`:

```yaml
- date: "Nov 01"
  content: "Our paper on a [user study about translating C to Rust](https://arxiv.org/abs/2411.14174) is accepted at NDSS'25."
```

## Deployment

Pushing to `main` triggers `.github/workflows/jekyll.yml`, which builds the site with Jekyll
and publishes it to GitHub Pages. The custom domain comes from the `CNAME` file, and GitHub
automatically provisions and renews the HTTPS certificate (Let's Encrypt) for it.
