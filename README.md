# setup_devops_environment

* This is My experience with so many fields.
* Feel free to fork My notes. :)
* Prepare my devops-enviroment on a Unix-like machine(Could be a physical or virtual machine) and use vscode with ssh plugin to connect this.
* mkdocs-material to render *.md files to static web site files

## Prerequisites

* Python >= 3.11
* [pyenv + poetry](https://github.com/hong539/setup_devops_environment/blob/main/docs/computer%20languages/programming_languages/python/python.md#usage-with-pyenvpoetry)
* [mkdocs-material](https://github.com/squidfunk/mkdocs-material)

## Quick start

```shell
git clone git@github.com:hong539/setup_devops_environment.git
cd setup_devops_environment
uv sync
#activate python venv
source .venv/bin/activate
# uv venv

mkdocs new [dir-name]
mkdocs serve
mkdocs build
mkdocs -h

#exit venv
deactivate

#manually execute
docker build . -t docker.io/focal1119/setup_devops_environment:prod
docker build . -t docker.io/focal1119/setup_devops_environment:test -f Dockerfile.ci
docker run -d --name setup_devops_environment -p 8000:80 docker.io/focal1119/setup_devops_environment:prod

#github actions
#CI
docker login
docker build . -t docker.io/focal1119/setup_devops_environment:latest -f Dockerfile.ci
docker push
#CD
docker run -d --name setup_devops_environment -p 8000:80 docker.io/focal1119/setup_devops_environment:latest

#docker compose
docker compose up -d

#git comment
#update docs and test github action ci
#skip ci
[skip ci] update scripts
[skip ci] update docs
[skip ci] update ci.yml
[skip actions] update docs
```

## Important!!!

== We're Using GitHub Under Protest ==

This project is currently hosted on GitHub.  This is not ideal; GitHub is a
proprietary, trade-secret system that is not Free and Open Souce Software
(FOSS).  We are deeply concerned about using a proprietary system like GitHub
to develop our FOSS project.  We have an
[open {bug ticket, mailing list thread, etc.} ](INSERT_LINK) where the
project contributors are actively discussing how we can move away from GitHub
in the long term.  We urge you to read about the
[Give up GitHub](https://GiveUpGitHub.org) campaign from
[the Software Freedom Conservancy](https://sfconservancy.org) to understand
some of the reasons why GitHub is not a good place to host FOSS projects.

If you are a contributor who personally has already quit using GitHub, please
[check this resource](INSERT_LINK) for how to send us contributions without
using GitHub directly.

Any use of this project's code by GitHub Copilot, past or present, is done
without our permission.  We do not consent to GitHub's use of this project's
code in Copilot.

![Logo of the GiveUpGitHub campaign](https://sfconservancy.org/img/GiveUpGitHub.png)