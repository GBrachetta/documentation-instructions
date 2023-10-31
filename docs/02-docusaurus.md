# Using Docusaurus

## General

[Official Site](https://docusaurus.io/docs)

## Commands

### Install

```sh title="" linenums="0"
npx create-docusaurus@latest my-website classic
```

### Project structure

```text linenums="0" title="Tree"
my-website
├── blog
│   ├── 2019-05-28-hola.md
│   ├── 2019-05-29-hello-world.md
│   └── 2020-05-30-welcome.md
├── docs
│   ├── doc1.md
│   ├── doc2.md
│   ├── doc3.md
│   └── mdx.md
├── src
│   ├── css
│   │   └── custom.css
│   └── pages
│       ├── styles.module.css
│       └── index.js
├── static
│   └── img
├── docusaurus.config.js
├── package.json
├── README.md
├── sidebars.js
└── yarn.lock
```

### Start the site

```sh linenums="0" title=""
cd my-website
npx docusaurus start
```
