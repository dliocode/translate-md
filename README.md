# translate-md
Translate the Readme to another language

### Example Action Workflows

```yml
name: dliocode-translate-md

on:
  push:
    branches:
      - main
      - master
    paths:
      - 'README.md'    	  
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
      - name: Adding README - Português
        uses: dliocode/translate-md@main
        with:
          LANG_TO: pt
      - name: Adding README - English
        uses: dliocode/translate-md@main
        with:
          LANG_TO: en
      - name: Adding README - Français
        uses: dliocode/translate-md@main
        with:          
          LANG_TO: fr
      - name: Adding README - Italiano
        uses: dliocode/translate-md@main
        with:
          LANG_TO: it
      - name: Adding README - Deutsch
        uses: dliocode/translate-md@main
        with:
          LANG_TO: de
```