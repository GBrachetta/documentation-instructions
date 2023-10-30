# Using MkDocs

## General

For full documentation visit [mkdocs.org](https://www.mkdocs.org).

### Commands

* `mkdocs new [dir-name]` - Create a new project.
* `mkdocs serve` - Start the live-reloading docs server.
* `mkdocs build` - Build the documentation site.
* `mkdocs -h` - Print help message and exit.

### Project layout

```text title="Tree"
mkdocs.yml    # The configuration file.
docs/
    index.md  # The documentation homepage.
    ...       # Other markdown pages, images and other files.
```

### Config Example

```yaml
site_name: Guillermo Brachetta
theme:
  features:
    - navigation.instant
    - content.code.copy
    - content.code.select
    - search.suggest
    - search.share
    - header.autohide
    - navigation.footer

  name: material
  palette:
    - scheme: default
      primary: deep purple
      accent: teal
      toggle:
        icon: material/brightness-7
        name: Switch to dark mode
    - scheme: slate
      primary: deep orange
      accent: teal
      toggle:
        icon: material/brightness-4
        name: Switch to light mode
plugins:
  - blog
  - search
  - tags:
      enabled: true

markdown_extensions:
  - footnotes
  - attr_list
  - pymdownx.emoji:
      emoji_index: !!python/name:material.extensions.emoji.twemoji
      emoji_generator: !!python/name:material.extensions.emoji.to_svg
  - md_in_html
  - def_list
  - pymdownx.tasklist:
      custom_checkbox: true
  - admonition
  - pymdownx.details
  - pymdownx.highlight:
      auto_title: true
      linenums: true
      linenums_style: pymdownx-inline
      anchor_linenums: true
      line_spans: __span
      pygments_lang_class: true
      use_pygments: true
  - pymdownx.inlinehilite
  - pymdownx.snippets
  - pymdownx.superfences

extra:
  social:
    - icon: fontawesome/brands/mastodon
      link: https://fosstodon.org/@squidfunk
      name: squidfunk on Fosstodonå
    - icon: fontawesome/brands/github
      link: https://fosstodon.org/@squidfunk
      name: squidfunk on Fosstodon
    - icon: fontawesome/brands/slack
      link: https://fosstodon.org/@squidfunk
      name: squidfunk on Fosstodon
  generator: false

copyright: Copyright &copy; 2023 Guille
# repo_url: https://github.com/squidfunk/mkdocs-material
```

## Features

### Code Snippets

```javascript title="test.js" linenums="0"
window.dataLayer = window.dataLayer || [];

function gtag() {
  dataLayer.push(arguments);
  console.log(window)
}

gtag('js', new Date());

gtag('config', 'UA-XXXXX');
```

```python title="bubble_sort.py" hl_lines="2 3 5"
def bubble_sort(items):
  for i in range(len(items)):
    for j in range(len(items) - 1 - i):
      if items[j] > items[j + 1]:
        items[j], items[j + 1] = items[j + 1], items[j]
```

```javascript title="return.js" hl_lines="2" linenums="0"
if (!test) {
  return null;
}
```

### Admonitions

!!! abstract "Interesante"

    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod
    nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor
    massa, nec semper lorem quam in massa.

!!! note

    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod
    nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor
    massa, nec semper lorem quam in massa.

??? note

    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod
    nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor
    massa, nec semper lorem quam in massa.

!!! tip

    Lorem ipsum dolor sit amet, consectetur adipisici elit, sed eiusmod tempor 
    incidunt ut labore et dolore magna aliqua. Me non paenitet nullum 
    festiviorem excogitasse ad hoc. Ambitioni dedisse scripsisse iudicaretur. 
    Unam incolunt Belgae, aliam Aquitani, tertiam. Morbi fringilla convallis 
    sapien, id pulvinar odio volutpat. A communi observantia non est recedendum.

!!! warning

    :Cras mattis iudicium purus sit amet fermentum.

!!! danger

    :Cras mattis iudicium purus sit amet fermentum.

!!! example

    :Cras mattis iudicium purus sit amet fermentum.

!!! pied-piper "Pied Piper"

    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et
    euismod nulla. Curabitur feugiat, tortor non consequat finibus, justo
    purus auctor massa, nec semper lorem quam in massa.

### Images

![Image](https://images.unsplash.com/photo-1682686581484-a220483e6291?auto=format&fit=crop&q=80&w=3540&ixlib=rb-4.0.3&ixid=M3wxMjA3fDF8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D)

### Footnotes

Lorem ipsum[^1] dolor sit amet, consectetur adipiscing elit.[^2]

[^1]: Lorem ipsum dolor sit amet, consectetur adipiscing elit.

[^2]: Lorem ipsum dolor sit amet, consectetur adipiscing elit.

### Annotations

Lorem ipsum dolor sit amet, (1) consectetur adipiscing elit.
{ .annotate }

1. :man_raising_hand: I'm an annotation! I can contain `code`, __formatted
    text__, images, ... basically anything that can be expressed in Markdown.

Lorem ipsum dolor sit amet, (1) consectetur adipiscing elit.
{ .annotate }

1. :man_raising_hand: I'm an annotation! (1)
    { .annotate }

    1. :woman_raising_hand: I'm an annotation as well!
