layout: true

---
class: middle, center

### What the tmux?
### [Dotfiles Indy Meetup][dotfiles-indy] | 08.2020 | Clayton Parker

???
NOTES HERE

---
class: middle, center

# Who Am I?

![:scale 40%](images/claytron.png)

[@claytron][twitter-claytron] on the internets and IRL

My [dotfiles][dotfiles-claytron]

???
- known as claytron on the internet and in real life
- Links to my dotfiles and more. I'll share the slides after.

---
class: middle, center

# What is tmux?

Terminal MUltipleXer

A better `screen`

The hotness you need

???
- Many terminals within a terminal
- A way to save your work for later or organize things locally
- A new take on the idea
- You NEED this in your life for sure

---
class: middle, left

# `tmux` vs `screen`

## Pros

- Client / server model
- Better keybinding support
- Multiple paste buffers
- More modern overall
- BSD licensed

## Cons

- No serial / telnet terminal
- No support for older platforms and odd terminals

???
- windows are independent entities which may be attached simultaneously to multiple sessions and viewed from multiple clients (terminals), as well as moved freely between sessions within the same tmux server
- Vi / Emacs keybindings available out of the box, and support for mouse and scrolling also.
- A cleaner, modern, easily extended, BSD-licensed codebase.
- If you are stuck on some old mainframe, you could still use `screen`

---
class: middle, center

# How it works?

???
Let's take a tour of the basic functionality of tmux

---
class: middle, center

# Starting a session

```
$ tmux
```

???
- The foundation of `tmux` is the session
- Every time you invoke `tmux` you are starting a new session

---
class: middle, center

# Key Bindings

Defaults are vague and hard to remember

Vi and Emacs modes

---
class: middle, center

# Detach / Attach

TODO: keybindings / screenshots here?

???
- The fundamental reason you'd want to use `tmux`

---
class: middle, center

# Windows and Panes

TODO: screenshots of all these things to demonstrate?

---
class: middle, center

# Pane Movement

TODO

---
class: middle, center

# Status line

TODO: screenshots / explanations?

---
class: middle, center

# Modality

TODO: maybe earlier in the talk?

???
- Normal mode sends keys to the terminal
- Using the prefix allows for commands to be run

---
class: middle, center

# Command Mode

TODO: screenshots / explanations?

---
class: middle, center

# Copy Mode

TODO

---
class: top, left

# Links

- [My Dotfiles][dotfiles-claytron]
- TODO

[/ Links ---------------------------------------------------------------- /]: #
[dotfiles-indy]: https://meetingplace.io/Dotfiles-Indy
[twitter-claytron]: https://twitter.com/claytron
[dotfiles-claytron]: https://github.com/claytron/dotfiles
[/ ---------------------------------------------------------------------- /]: #
