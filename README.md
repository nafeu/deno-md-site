# Deno Markdown Site

![](https://res.cloudinary.com/dvivnklwq/image/upload/v1611809447/Screen_Shot_2021-01-27_at_11.50.27_PM_qshv0w.png)

An example static site generator built with Deno. Made for a blog post.

## Usage

Make sure you've templated your website as instructed below, then you can use:

```
deno run --allow-read --unstable --allow-write https://raw.githubusercontent.com/nafeu/deno-md-site/main/main.ts example-site.md build
```

Where you can replace `example-site.md` with your site's `.md` file and replace `build` with your specified build path.

#### Local Installation (optional)

```
git clone https://github.com/nafeu/deno-md-site.git
cd deno-md-site
```

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
favicon: 🦕
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

#### Templating Rules
- [YAML Front Matter](https://jekyllrb.com/docs/front-matter/) is used to declare a `[WEBSITE_TITLE]`, optional css styles and an optional emoji favicon
- Triple plus signs (`+++`) are used to separate pages and layout components
- `[PAGE_PATH]` is the url path to a page
- `[PAGE_TITLE]` is the title of the current page
- `[PAGE_CONTENT]` is the content of that page (written in markdown)

Check out the `example-site.md` file and `docs/` folder included in this repo for a clear example. Note that for the `docs` folder has been manually formatted the HTML so it would be easier to read, the actual build renders HTML that works but isn't as human-readable.

#### Generating Your Website

Target your templated `.md` file and specify a build path like so:

```
deno run --allow-read --unstable --allow-write main.ts example-site.md build
```

You can then use `cd build` to see your generated website.

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
