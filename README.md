# PyTCT-docs

PyTCT Documents

## Install

### Install uv

https://docs.astral.sh/uv/getting-started/installation/

```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
```

### Install dependency
```bash
uv sync
```

## Run Local Docs Server
```bash
uv run mkdocs serve
```

## MkDocs
For full documentation visit [mkdocs.org](https://www.mkdocs.org).

Material for MkDocs documentation is [here](https://squidfunk.github.io/mkdocs-material/reference/)

### Commands

* `mkdocs new [dir-name]` - Create a new project.
* `mkdocs serve` - Start the live-reloading docs server.
* `mkdocs build` - Build the documentation site.
* `mkdocs -h` - Print help message and exit.

### Project layout

    mkdocs.yml    # The configuration file.
    docs/
        index.md  # The documentation homepage.
        ...       # Other markdown pages, images and other files.
