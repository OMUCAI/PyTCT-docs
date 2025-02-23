# PyTCT-docs

PyTCT Documents

## Install

### GitHub Codespace (recommend)

1. **Create cpdespace**

    Select Create codespace from the `+` button  
    ![codespace](./img/codespace.png)

### Local PC

1. **Install uv**

    [uv](https://docs.astral.sh/uv/getting-started/installation/) is pakage manager

    ```bash
    curl -LsSf https://astral.sh/uv/install.sh | sh
    ```

2. **Install dependency**

    ```bash
    uv sync
    ```

### Adding New Document Files

When you add a new Markdown file to the documentation, follow these steps to ensure it is properly integrated and displayed:

1. **Add the Markdown file**:
    - Place your new Markdown file in the `docs/` directory.

2. **Update `mkdocs.yml`**:
    - Open the `mkdocs.yml` configuration file.
    - Add an entry for your new Markdown file under the `nav` section to include it in the navigation.

    Example:
    ```yaml
    nav:
      - Home: index.md
      - New Page: new_page.md
    ```

3. **Serve the Documentation Locally**:
    - Run the following command to start the live-reloading docs server and see your changes:

    ```bash
    uv run mkdocs serve
    ```

5. **Commit and Push Changes**:
    - Commit your changes to the repository and push them to the remote repository.

<!-- ## Run Local Docs Server

You can see how the document appears via your local server.
You can run it either the VSCode Tasks way or the shell way

### VSCode Tasks
1. **Open the Command Palette**:
    - Press `Ctrl+Shift+P` to open the Command Palette.

2. **Run the Task**:
    - Type `Run Task` and select it.
    - In the list of tasks, select `check site`.

### Shell

1. **Run command**:  
    Please run the following command in a shell

    ```bash
    uv run mkdocs serve
    ``` -->


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
