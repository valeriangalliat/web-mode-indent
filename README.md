# web-mode-indent

> Indent files using Emacs [web-mode].

[web-mode]: https://web-mode.org/

## Overview

Sometimes, [web-mode] turns out to be the only tool that properly indent
a particular syntax, whereas [Prettier](https://prettier.io/) or
[`html-beautify`](https://github.com/beautify-web/js-beautify) fail to
understand a templated language.

This is for example the case with the [HEEx templating language](https://hexdocs.pm/phoenix_live_view/Phoenix.LiveView.html).

In that case, web-mode-indent is an Emacs Lisp script that will indent
in place the files you give it using web-mode indentation.

## Installation

```sh
git clone https://github.com/valeriangalliat/web-mode-indent.git ~/opt/web-mode-indent
export PATH=~/opt/web-mode-indent:$PATH
```

## Usage

```sh
web-mode-indent lib/**/*.html
```

For convenience, also included a `heex-indent` command that also adds a hack for
web-mode to handle the `<.tag></.tag>` form of HEEx templates.

```sh
web-mode-indent lib/**/*.heex
```
