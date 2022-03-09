%title: Language Server Protocol
%author: Brendon A. Kay
%date: 2022-02-11

-> # Learning about the Language Server Protocol <-

-> ## with NeoVim and the "gopls" Language Server <-


-> presented using `mdp` <-

---

## Motivation

I wanted to learn more about NeoVim's Language Server
Protocol (LSP) support.

Sharpen the tools of my trade.

Adam kept making fun of my lack of IDE features when pair
programming. /s

---

## What this is

A fun learning session about the Language Server Protocol
and IDEs.

How to use NeoVim's built-in support of LSP, using `gopls` as
an example.

Learn more about our IDEs.

---

## What this isn't

A statement that any IDE is better than the other.

A suggestion that this is the right or wrong way of doing
things.

---

## What is NeoVim?

TODO

I like using Vim/NeoVim and wanted to get the most out of my
editor.

Vim/NeoVim makes me feel "close to the metal".

It can be a very powerful tool once learned.

---

## What is the LSP?

From Wiki: "The Language Server Protocol (LSP) is an open,
JSON-RPC-based protocol for use between source code editors
or integrated development environments (IDEs) and servers
that provide programming language-specific features.

*"The goal of the protocol is to allow programming language*
*support to be implemented and distributed independently of*
*any given editor or IDE"*

---

## LSP Overview

[https://microsoft.github.io//language-server-protocol/overviews/lsp/overview/](https://microsoft.github.io//language-server-protocol/overviews/lsp/overview/#:~:text=and%20tooling%20vendors!-,How%20it%20works,-A%20language%20server)

---

## LSP Features

TODO

---

## NeoVim supports the LSP

[Added in version 0.6.1](https://github.com/neovim/neovim/releases/tag/v0.6.1)

[NeoVim's documentation](https://neovim.io/doc/user/lsp.html)

---

## LSP with `gopls`

https://github.com/golang/tools/tree/master/gopls

TODO

---

## Like all things Vim... RTFM

When I first began this journey I thought I could brute force a nice NeoVim
config by reading blog articles and copying examples, but I eventually found
myself at the doorstep of the nvim reference manual.

`:help lsp-quickstart`

---

## Starting fresh with the default config

I tried this because I already had `gopls` installed.

`:help lsp-config`

---

## I got too scared starting fresh with a default config

Well, that did not go well. Honestly there's no rush like
trashing a vim config and trying to figure out how to get it
working again. I understand that's from my lack of knowledge
about my config, but I digress. So, instead I'm going to
chip away at my config, starting with this.

https://github.com/neovim/nvim-lspconfig

Which ultimately was referenced in the main docs anyways.

---

### Turns out I was nearly there all along Because I had
previously copied some LSP related configs from other blogs
I had read on switching to a Lua config it turns out I
didn't have to do too much refactoring.

Mostly going to just remove `vim-go` and make sure I can use
the LSP features:
- go-to-definition
- find-references
- hover
- completion
- rename
- format
- refactor

With my current mapping I have these features mapped out.

---

### Process

- Install LSP
- Install nvim-lspconfig plugin
- Setup LSP in config, for example

```
local lsp = require 'lspconfig' lsp.gopls.setup{}
```

---

## Final plugin list related to LSP

- shougo/deoplete-lsp
- nvim-treesitter/nvim-treesitter
- ojroques/nvim-lspfuzzy
- sbdchd/neoformat

---

### Find a nice markdown plugin

Writing this in vim was nice but a makrdown plugin for
formatting, word wrapping, spell checking, etc. would be
nice. Maybe even render it.

Or I can just write everything in LaTeX.

---

### Snippets

Another nice feature that comes packaged with most IDEs now
are snippets. As a Go programmer these can be especially
helpful.

---

### Automate Another benefit of NVim is that it's minimal

configuration allows you to automate setting up a new editor
environment.

---

## Goals Write this whole presentation in nvim. Learn about
LSP. Update my current nvim config the only use LSP. i.e.,
No more `vim-go`. At the time of writing my `init.lua` in my
dotfiles repo is `104620c28da0b0d982f7a2b4dae9ef3a962524a6`
Improve my writing skills.

---

### Why not just use VSCode with Vim bindings?

I like to have a minimal editing environment with full
control over my configuration. I've even found Vim to be a
little easier to configure than VSCode.

---

### Well, I don't care about Vim, but I like this LSP stuff

https://medium.com/the-andela-way/gopls-language-server-setup-for-go-projects-3ee79dcac123

---

## Final Thoughts and Notes
Honestly Microsoft was really successful with VS/VSCode. It
seems appropriate to adopt LSP. 

"LSP is a win for both language providers and tooling
vendors!"

---

## References
https://en.wikipedia.org/wiki/Language_Server_Protocol
https://github.com/microsoft/language-server-protocol
https://microsoft.github.io/language-server-protocol/
https://microsoft.github.io/language-server-protocol/overviews/lsp/overview/
https://langserver.org/
