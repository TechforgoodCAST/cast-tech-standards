# CAST tech guide

Using [mkdocs](http://www.mkdocs.org/).

Edit the markdown files in the docs directory. Site configuration found in the
`mkdocs.yml` file.

The contents can either be automatically generated from the structure of the
files (with folders creating submenus), or can be added to a `pages` variable
in the `mkdocs.yml` file to create a custom structure (nb this means new pages
won't be added automatically to the contents).

Most recent deployment: <https://techforgoodcast.github.io/cast-tech-standards/>

## Run local server

    mkdocs serve

## Deploy to github pages

    mkdocs gh-deploy

## Build an html version of the site (stored in `site/`)

    mkdocs build
