# NUS KISP Lab

The website for the NUS KISP Lab is built using
[Jekyll](https://jekyllrb.com/docs/) and at the time of writing
hosted on [GitHub pages](https://pages.github.com/).

## Development

My suggestion for working on this site is to set up Jekyll locally on
your machine following the [Jekyll Docs](https://pages.github.com/)
and test everything locally before pushing to GitHub. As of right now
anything pushed to the main branch goes live immediately. In the
future it may be required to push to a staging branch for testing
before merging to main.

## Personal Profiles

Personal profiles are created by adding a markdown file to the
```_people``` folder. The front matter (the section at the top of the
file marked by three dashes ```---```) sets your name and information
to be displayed in the header and in other pages.

``` YAML
---
layout: person
title: Your Name Here
slug: short_name
role: Your Role
email: person@comp.nus.edu.sg
github_username: username
twitter_username: username
linkedin_username: username
---

Describe yourself here.
```

Please make sure that:

* You use the ```person``` layout

* The ```slug``` field matches the filename (without the ```.md```
extension)

* Your role is correct and matches others of the same role

* All other fields are optional

* You are encouraged to add a personal description after the front
matter

### Profile Pictures

Please include a large and a small profile picture of yourself in
your profile. Full size pictures are stored under
```images/people/[slug].jpeg``` while small pictures are stored under
```images/people/[slug]_small.jpeg```. ***Small images are to be
256x256 pixels precisely***. Large pictures can be any size so long
as it renders well on your page.


## Publications

Publications are created by adding a markdown file to the ```_pubs```
folder. Please start the filename with the year of publication
followed by an underscore (`_`) and a short name, using underscores
instead of spaces. The publication is entirely defined by fields in
the front matter, an example of which is shown below.

``` YAML
---
title: "A Very Exciting New Approach"
authors:
 - slug: author1
 - name: Someone External
   url: https://someone.com/external
 - name: Author Without A Site

publication: A Very Important Conference
year: 2023
pub_url: https://comp.nus.edu.sg/my_paper.pdf
---
```

As of right now, the content is unused as publications don't have
their own pages. In the future, we might use that for the abstract to
be displayed in a collapsible field or have pages for publications.

Authors can be listed using either their "slug", in which case a link
to their personal profile at KISP is used, or a name with an optional
URL. Please use the slug for anyone with a profile at KISP, and a
name and URL otherwise.

Eventually, PDFs of papers will be kept on the KISP site, such that
the URL will be local. We have yet to decide on how that will work.
We might eventually add links to GitHub or other artifacts for
papers.


## Project Pages

Projects are created by adding a markdown file to the ```_projects```
folder. The front matter of the project sets the information that
will be displayed in the list of projects page, and the content is
free for the project owners to add any information they desire. Below
is an example of the front matter.

``` YAML
---
layout: project
name: Some Project
slug: someproject
description: Some Project implements the turbo encambulator.
lead: 
  slug: kareem
people:
 - slug: kareem
 - slug: jason
 - name: Wile E Coyote
   url: https://chuckjones.com/characters/wile-e-coyote/
---

Describe your project here.
```

Please make sure that:

* You use a reasonable short name for the project as the slug

* The filename matches the slug (without the `.md` extension)

* As with publication authors, the project lead and team members
please use slug for people with KISP profiles, and a name and URL for
others.

### Project Logos

Please include a large and a small image of your project logo. Full
size pictures are stored under ```images/projects/[slug].jpeg``` while
small pictures are stored under
```images/projects/[slug]_small.jpeg```. ***Small images are to be
256x256 pixels precisely***. Large pictures can be any size so long
as it renders well on your page.

## Blog

Blog posts are stored under `blog/_posts` in markdown format. Please
name files using the following convention:
`YYYY-MM-DD-Your-Title.md`, where `YYYY-MM-DD` is the date of posting
to the blog, and `Your-Title` is the title of the blog post with
spaces replaced with dashes. An example of the front matter of a blog
post is shown below.

``` YAML
---
layout: post
title:  Example Post
date:   2023-05-16 12:04:54 +0800
mathjax: True
---

Your blog post goes here.
```

Please make sure that:

* You use the `post` layout

* Set the title the same as the filename

* Use the correct date and time for posting to the blog

* Set `mathjax: True` if you use any math formatting. Math must be in
double-dollar sign blocks, i.e. `$$ e = m \cdot c^2 $$`

### Notion Export

It's possible to [export pages from
Notion](https://www.notion.so/help/export-your-content) to markdown
and use the content in a blog post or page. While this mostly works,
there are a few quirks.

First, even though Notion requires you to write math with
double-dollar-sign delimiters, it exports with only a single dollar
sign. Fortunately, it's pretty easy to fix this with the following
`sed` script:

``` sed
s/\([^\$]\)\$\([^\$]\)/\1$$\2/g
s/\([^\$]\)\$\([^\$]\)/\1$$\2/g
s/\([^\$]\)\$\\/\1$$\\/g
s/\([^\$]\)\$$/\1$$/
s/^\$\([^\$]\)/$$\1/
```

Second, your images will almost certainly be named something like
`Untitled 1.png`. Please move your images to be under
`blog/images/YYYY-MM-DD/description.png`, where `YYYY-MM-DD` is the
date of the blog post, description is some reasonable description of
the image, and the appropriate extension. You can then use
`images/YYYY-MM-DD/description.png` as the link in your blog post.
