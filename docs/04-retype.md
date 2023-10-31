# Using Retype

## Website

[Retype](https://retype.com/)

## Installation

```sh
npm install retypeapp --global
```

- Create a directory and `cd` tp it, then execute:

```sh
retype start
```

Only a file will be created:

```yaml title="retype.yml"
input: .
output: .retype
url: https://gbrachetta.com
branding:
  title: Guillermo
  label: Docs
links:
- text: Blog
  link: /blog

footer:
  copyright: "&copy; Copyright {{ year }} GB. All rights reserved."
```

!!!info

    Serves on port 5000
