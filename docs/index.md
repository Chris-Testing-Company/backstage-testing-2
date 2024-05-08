# TechDocs

## Overview

This set of documentation is intended to show simple working examples of TechDocs.

## Examples

Current examples:

- [iframe](./examples/iframe.md): this shows how you can use an iframe in your TechDocs
- [Lists](./examples/lists.md): this showcases how to setup your lists in TechDocs
- [Mermaid](./examples/mermaid.md): this showcases how to use Mermaid diagrams in your TechDocs
- [PlantUML](./examples/plantuml.md): this showcases how to use PlantUML diagrams in your TechDocs

## Workflow for Publishing TechDocs

1. Create mkdocs.yaml in the Targeted Repository:

    - The mkdocs.yaml should contain at least the following content:

    ``` yaml
        site_name: 'a-unique-site-name'
        site_description: 'description-for-the-doc' #(optional)

        plugins:
        - techdocs-core
        - kroki #(optional) for displaying mermaid diagrams

        nav: #(optional) for sidebar navigation
            - Home Page: index.md
            - Second Page: examples/iframe.md
    ```

2. Create docs Folder in the Targeted Repository:

    - This folder will contain the Markdown files for your documentation.

3. Add index.md within the docs Folder:

    - The index.md file will serve as the main entry point for your documentation.

4. Update catalog-info.yaml in the Targeted Repository:

    - Add the following line to the catalog-info.yaml file under metadata.annotations:

    ``` yaml
    backstage.io/techdocs-ref: dir:.
    ```

    - This tells Backstage where to find the TechDocs files in your repository.

## Existing Element

- [plugins](./plugins/README.md): this is the element prior to the techdocs changes.
