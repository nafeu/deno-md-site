---
title: Deno Markdown Site
styles: >
  @import url('https://fonts.googleapis.com/css2?family=Fira+Sans:wght@100;400;700&display=swap');

  body {
    font-family: 'Fira Sans', sans-serif;
    color: #000;
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 10vmin;
  }

  a {
    color: inherit;
    text-decoration: inherit;
    padding: 0.25em;
  }

  a:hover, .selected {
    border-bottom: 2px solid #000;
  }

  #title {
    font-size: 2em;
    font-weight: 100;
    margin-bottom: 1em;
  }

  #footer {
    font-size: 0.75em;
  }
---
/home:Home

# Home

Using **deno-md-site** you can generate a static site using just a single **.md** file.

+++
/about:About

# About

This site was built to show how easy it is to use JavaScript/TypeScript with **[deno](https://deno.land/)** to make something useful.

+++
/contact:Contact

# Contact

Get in touch at [nafeu.nasir@gmail.com](mailto:nafeu.nasir@gmail.com)

+++
layout:footer

[[source]](https://github.com/nafeu/deno-md-site) Made with ♥ by [Nafeu Nasir](https://nafeu.com).
