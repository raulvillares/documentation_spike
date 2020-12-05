# Alea development team documentation generator

This documentation is powered by [MkDocs](https://www.mkdocs.org).

:earth_africa: [Access to the documentation site](https://raulvillares.github.io/documentation_spike/)

## :nut_and_bolt: Configure and install

### Create virtualenv

```
mkvirtualenv documentation -p $(which python3)
```

### Install requirements

```
pip intall -r requirements.txt
```

## :computer: Commands

* `./serve.sh` - Start the live-reloading docs server.
* `./serve_all_ips.sh` - Start the live-reloading docs server [listening on all ips](https://github.com/mkdocs/mkdocs/issues/1239). Usefull for remote development.
* `./build.sh` - Build the documentation site.
* `./deploy.sh` - Deploy the documentation site to GitHub Pages.
* `mkdocs -h` - Print mkdocs help message and exit.

## :card_index: Project layout
    bifer-docs/   # Bifer documentation project
    mkdocs.yml    # MkDoc configuration file.
    docs/
        index.md  # The documentation homepage.
        ...       # Other markdown pages, images and other files.

## :rocket: Deploy

This project uses [GitHub Pages](https://pages.github.com/) to deploy the generated documentation. Run the following command:

```
./deploy.sh
```

That's it! Behind the scenes, MkDocs will build your docs and use the ghp-import tool to commit them to the gh-pages branch and push the gh-pages branch to GitHub repository.

Use mkdocs gh-deploy --help to get a full list of options available for the gh-deploy command.


## :vertical_traffic_light: Athentication

GitHub Pages sites are publicly available on the internet, even if the repository for the site is private or internal.
To avoid this, this project uses [mkdocs-encryptcontent-plugin](https://pypi.org/project/mkdocs-encryptcontent-plugin/).
This plugin allows you to have password protected articles and pages in MkDocs.
However, this could lead to security problems.

:rotating_light: **SO DON'T DOCUMENT ANY SENSITIVE DATA** :rotating_light:
