%title: Language Server Protocol
%author: Brendon A. Kay
%date: 2022-02-11

-> # Learning about the Language Server Protocol <-

-> with NeoVim and the gopls Language Server <-


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

Neovim is a project that seeks to aggressively refactor Vim in order to:

- Simplify maintenance and encourage contributions
- Split the work between multiple developers
- Enable advanced UIs without modifications to the core
- Maximize extensibility

---

## What is the LSP?

[The Language Server Protocol (LSP)](https://en.wikipedia.org/wiki/Language_Server_Protocol) is an open,
JSON-RPC-based protocol for use between source code editors
or integrated development environments (IDEs) and servers
that provide programming language-specific features.

*"The goal of the protocol is to allow programming language*
*support to be implemented and distributed independently of*
*any given editor or IDE"*

---

## LSP Overview

[Microsoft's documentation](https://microsoft.github.io//language-server-protocol/overviews/lsp/overview/)
[LSP Official site](https://langserver.org/)

---

## LSP Features

- Go-to-definition
- Find-references
- Hover
- Completion
- Rename
- Format
- Refactor

---

## NeoVim supports the LSP

[Added in version 0.6.1](https://github.com/neovim/neovim/releases/tag/v0.6.1)

[NeoVim's documentation](https://neovim.io/doc/user/lsp.html)

---

## LSP with `gopls`

-> DEMO TIME <-

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
