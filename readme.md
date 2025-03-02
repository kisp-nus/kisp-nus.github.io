## One-page version of the KISP Lab website

Two folders are involved:

- `./_data/onepage`: YAML files for data, including news, members, projects, and publications.

- `./onepage`: HTML-related stuff, including the HTML files and the assets, e.g., images.

### How to update personal profiles

1. Add your profile like the following to the correct `kind` section in `./_data/onepage/members.yml`. Supported `kind` are `faculty`, `graduate_students`, `postdocs`, and `alumni`.

``` YAML
    - name: Ruishi Li
      image: ./assets/people/member_ruishi.jpg
      website: https://zero0one1.github.io/
      github: https://github.com/Zero0one1
      linkedin: https://www.linkedin.com/in/ruishili/
      twitter: https://twitter.com/xx
```

2. Upload your profile image to `./onepage/assets/people/` with `member_<your name>.jpg` as the filename.

### How to update publications

Add your publication like the following to `./_data/onepage/publications.yml`. The most recent publication should be added to the beginning of the list.

``` YAML
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

### How to update projects

Add your project like the following to `./_data/onepage/projects.yml`.

``` YAML
- name: Capstone
  description: A Capability-based Foundation for Trustless Secure Memory Access
  url: https://capstone.kisp-lab.org/
```

### How to update news

Add your news like the following to `./_data/onepage/news.yml`. The most recent news should be added to the beginning of the list.

``` YAML
- date: "Nov 01"
  content: "Our paper on a [user study about translating C to Rust](https://arxiv.org/abs/2411.14174) is accepted at NDSS'25."
```