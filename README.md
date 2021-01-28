# Deno Markdown Site

![](https://res.cloudinary.com/dvivnklwq/image/upload/v1611809447/Screen_Shot_2021-01-27_at_11.50.27_PM_qshv0w.png)

An example static site generator built with Deno. Made for a blog post.

## Usage

#### Templating Your Website

Create a markdown file:

```
touch example-site.md
```

And format it like so:

```markdown
---
title: [WEBSITE_TITLE]
styles: >
  /* Add Optional CSS Here */
---
/home:Home

# Home

[Home page content]

+++
/[PAGE_PATH]:[PAGE_TITLE]

# [PAGE_TITLE]

[PAGE_CONTENT]

+++
layout:footer

[FOOTER_CONTENT]
```

Where the templating works as follows:
- YAML frontmatter is used to declare a `[WEBSITE_TITLE]` of your choice as well as css styles respectively
- Triple plus signs (`+++`) are used to separate pages and layout components
- `[PAGE_PATH]` is the url path to a page
- `[PAGE_TITLE]` is the title of the current page
- `[PAGE_CONTENT]` is the content of that page (written in markdown)

Check out the `example-site.md` file included in this repo for a clear example.

#### Generating Your Website

Target your templated `.md` file and specify a build path like so:

```
deno run --allow-read --unstable --allow-write main.ts example-site.md build
```

## Development

I recommend using [`denon`](https://github.com/denosaurs/denon):

```bash
deno install --allow-read --allow-run --allow-write -f --unstable https://deno.land/x/denon/denon.ts
```

Then you can use

```bash
denon run --allow-read --unstable --allow-write main.ts example-site.md
```

## License

MIT