%title: Debug Adapter Protocol
%author: Brendon A. Kay
%date: 2022-02-27

-> # Debug Adapter Protocol <-

-> presented using `mdp` <-

---

## Motivation

I wanted a universal debugger service, rather than relying on a bunch of
different plugins.

---

## Debugger Adapter Protocol

Generic debugger interface between a debugger and an API consumer.
From the `nvim-dap` help page...

```
A debug adapter is a facilitator between nvim-dap (the client), and a
language-specific debugger:


    DAP-Client ----- Debug Adapter ------- Debugger ------ Debugee
    (nvim-dap)  |   (per language)  |   (per language)    (your app)
                |                   |
                |        Implementation specific communication
                |        Debug adapter and debugger could be the same process
                |
         Communication via the Debug Adapter Protocol


To debug applications, you need to configure two things per language:

- A debug adapter (|dap-adapter|).
- How to launch your application to debug or how to attach to a running
  application (|dap-configuration|).
```

---

## Methodology

To demonstrate the use of a DAP I will be using the Vim plugin
[nvim-dap](https://github.com/mfussenegger/nvim-dap)

For the debugger server I will be using the Go debugger
[Delve](https://github.com/go-delve/delve), which has a DAP option.

```
$ dlv -h | grep DAP
dap         [EXPERIMENTAL] Starts a TCP server communicating via Debug Adaptor Protocol (DAP).
```

---

## Disclaimer

This is not a claim to be the "best" way to debug Go services.

Goland, VSCode, and many other editors have rich proprietary tooling that can be
easier to configure or setup.

Even print logging is a valid method of debugging.

However, as we will see, using a DAP client provides its own set of benefits.

---

-> ## Demo Time 🎉 <-

---

## Other benefits

Using the DAP over TCP means you could connect to a debugger on another server.
I have a proof-of-concept for our Docker development services in [backend PR #2907](https://github.com/syndio/backend/pull/2907)

---

## References

https://microsoft.github.io/debug-adapter-protocol/
