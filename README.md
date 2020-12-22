# mauricebauer.de - Portfolio website

![GitHub Workflow Status (branch)](https://img.shields.io/github/workflow/status/mauricebauer/portfolio/Hugo%20CI/master?label=Pipeline&logo=GitHub)
![GitHub deployments](https://img.shields.io/github/deployments/mauricebauer/portfolio/github-pages?label=Deployment&logo=Github)

This is my portfolio website to showcase some of my projects and to provide information about me.

This project uses the static page builder [Hugo](https://gohugo.io/) in combination with the [PaperMod](https://github.com/adityatelange/hugo-PaperMod)-Theme and follows the [Git-Flow](https://www.atlassian.com/de/git/tutorials/comparing-workflows/gitflow-workflow).

## Contribution

If you find a mistake on the page, please let me know either via e-mail or create an issue here on this repository. Also feel free to open a pull-request.

## Development server

```bash
# Make sure to update the theme Git-Submodule
git submodule update --init --recursive
git submodule update --remote --merge

# Start live server with "development"-environment
hugo server -D
```

## Build production version

```bash
# Make sure to update the theme Git-Submodule
git submodule update --init --recursive
git submodule update --remote --merge

# Build production-ready minified version of the website
hugo --minify
```
