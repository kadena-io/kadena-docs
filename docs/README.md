# Kadena Docs

This project contains all of the documentation used to support the Kadena Docs resource site.

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

### Installing

clone the repository

## Contributing

To make updates to this site you need to complete the following steps.
```
git add .
git commit -m 'short description of changes goes here'
git push -u origin master
```

To preview changes, run the following command:
```
mkdocs serve
```
And navigate to <http://127.0.0.1:8000> on your browser.

## Publishing
Deploy these changes to the live site (AVOID until going live)

```
mkdocs gh-deploy --clean
```

## Built With

* [MkDocs](https://www.mkdocs.org/)
* [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/getting-started/)
* [GitHub Pages](https://pages.github.com/)
