# RmlUi for Visual Studio Code

An unofficial Visual Studio Code extension for [RmlUi](https://github.com/mikke89/RmlUi) documents (`.rml`) and style sheets (`.rcss`).

## Features

RML is close to XHTML and RCSS is close to CSS, so this extension doesn't add new languages. It opens `.rml` files as HTML and `.rcss` files as CSS, then teaches VS Code's built-in HTML and CSS support about what RmlUi adds. You keep the editor's usual highlighting, Emmet, formatting and folding, plus:

* No false warnings on RCSS-only properties such as `decorator`, `nav-down`, `tab-index`, `font-effect` and `image-color`, or on the `@spritesheet` and `@decorator` at-rules
* Autocomplete and hover docs for those properties and their keywords, with links to the RmlUi documentation
* RML elements and attributes: `<rml>`, `<handle>`, `<tabset>`, `<tab>`, `<panel>`, `<template>`, `<body template>`, `<progress direction>`, and the data binding attributes (`data-model`, `data-if`, `data-for`, `data-value` and others)

## Known Issues

* RmlUi's additions apply to all HTML and CSS files, so they also show up in autocomplete in ordinary web files
* Standard CSS that RmlUi doesn't support, such as `grid`, still autocompletes, and values aren't checked against what RmlUi accepts
* Attribute families such as `data-class-*`, `data-attr-*` and `data-event-*` can't be listed generically. Only `data-event-click` autocompletes; the others work but have no hover docs
* Other extensions that act on HTML files will act on `.rml` files too

## Updating the Data

Everything lives in two [custom data](https://github.com/microsoft/vscode-custom-data) files:

* `data/rcss.css-data.json`: RCSS properties and at-rules
* `data/rml.html-data.json`: RML elements and attributes

They cover RmlUi 6.3.

## Release Notes

### 0.1.1

Updated README

### 0.1.0

Initial release
