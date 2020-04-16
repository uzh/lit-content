# *Lives in Transit* content wrangler

> This repository links to all topics developed for [Lives in Transit](https://livesintransit.org). The repository organises each topic as a [submodule](https://git-scm.com/book/en/v2/Git-Tools-Submodules), so that the latest content for each topic can be harvested with a single `git clone` command.

Because topics are *submodules*, cloning this repository with `git clone https://github.com/uzh/lit-content` will not actually clone the content from the topic submodules. If you want to clone this repo and all the topics at the same time, use:

```bash
git clone --recursive https://github.com/uzh/lit-content
```

## [`metadata.json`](https://github.com/uzh/lit-content/blob/master/metadata.json)

The [`metadata.json`](https://github.com/uzh/lit-content/blob/master/metadata.json) file contains information about each topic. Some fields within this JSON will be used during the deployment process for *Lives in Transit* and its test instance.

## Adding a topic

If you want to add a topic, and you know how to use git, we suggest:

1. Forking this repository
2. [Validating and pretty-printing your JSON content](https://github.com/uzh/marugoto-validator)
3. Adding a submodule that points to your content (the name should start with `lit-`)
4. Adding an entry in `metadata.json`, which maps the repo name to metadata about your topic
5. Submit a pull request

If you don't know git, just [create an issue](https://github.com/uzh/lit-content/issues/new) and provide your content as a link or a download. We might ask for some metadata (i.e. your name, collaborators etc.). Once we have everything we need, we will set your content up as a repository, and link it to this repo as a submodule.

## Gotchas

This repo will ignore any hidden folders in the root directory, due to the way the marugoto deployment works. Bear this in mind!

Anything else? Let us know!
