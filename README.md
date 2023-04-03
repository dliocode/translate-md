# translate-md
Translate the Readme to another language

### Example Action Workflows

```yml
name: Translate-md

on:
  push:
    branches:
      - main
      - master
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - name: Setup Node.js
        uses: actions/setup-node@v1
        with:
          node-version: 12.x

      # ISO Langusge Codes: https://cloud.google.com/translate/docs/languages                  
      - name: Adding README - English
        uses: dliocode/translate-md@main
        with:
          LANG: en
      - name: Adding README - Français
        uses: dliocode/translate-md@main
        with:
          LANG: fr
      - name: Adding README - Italiano
        uses: dliocode/translate-md@main
        with:
          LANG: it
      - name: Adding README - Deutsch
        uses: dliocode/translate-md@main
        with:
          LANG: de
```