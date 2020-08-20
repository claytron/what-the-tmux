layout: true

---
class: middle, center

### What the tmux?
### [Dotfiles Indy Meetup][dotfiles-indy] | 08.2020 | Clayton Parker

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

# What is it?

tmux == Terminal MUltipleXer

A better `screen`

???
- Many terminals within a terminal
- A way to save your work for later or organize things locally
- A new take on the idea
- You NEED this in your life for sure

---
class: middle, left

# `tmux` vs `screen`

<table>
<tr valign="top">
<td width="50%">

<h2>Pros</h2>

<ul>
<li>Client / server model</li>
<li>Better keybinding support</li>
<li>Multiple paste buffers</li>
<li>More modern overall</li>
<li>BSD licensed</li>
</ul>

</td>

<td width="50%">

<h2>Cons</h2>

<ul>
<li>No serial / telnet terminal</li>
<li>No support for older platforms and odd terminals</li>
</ul>

</td>
</tr>
</table>

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

# Starting a new session

![:scale 80%](images/session_start.png)

???
- The foundation of `tmux` is the session
- Every time you invoke `tmux` you are starting a new session

---
class: middle, center

# Sessions

![:scale 80%](images/session_started.png)

???
- A session is started with a single window.
- A status line appears giving you info about the session.
- Another difference from default screen, automatic status line.

---
class: middle, center

# Sessions

![:scale 80%](images/session_list_one.png)

`prefix + s`

???
Now we can see we have one session running one window.

---
class: middle, center

# Detaching

![:scale 80%](images/session_ended.png)

`prefix + d`

???
Now we are back to our original terminal, no longer in tmux.

---
class: middle, center

# Starting another session

![:scale 80%](images/session_start.png)

???
Running tmux again starts a completely new session.

---
class: middle, center

# Sessions

![:scale 80%](images/session_started_two.png)

???
We can see the session number is incremented in the status line.

---
class: middle, center

# Sessions

![:scale 80%](images/session_list_two.png)

`prefix + s`

???
- Now we can see we have two sessions running.
- This view also allows keyboard navigation, so you can see more detailed info.

---
class: middle, center

# Attaching

![:scale 80%](images/session_ended.png)

???
- Now let's go back to our non tmux terminal.
- How do we get back to the original session?

---
class: middle, center

# Attaching

![:scale 80%](images/attach.png)

???
- Running `tmux` each time creates a new session.
- You can see a list of sessions with the `list-sessions` command (or `ls` for short)
- You can attach to a specific session using the `attach` command.
- The `-t` is the `target`

---
class: middle, center

# Attaching

![:scale 80%](images/session_started.png)

???
Now we are back to the original session.

---
class: middle, center

# Windows and Panes

???
- The next most fundamental thing about tmux.
- Windows are a collection of panes.
- Each pane is a horizontal or vertical split of the window.

---
class: middle, center

# Windows and Panes

![:scale 80%](images/session_started_two.png)

???
Starting out with one window in a new session.

---
class: middle, center

# Split Vertically

![:scale 80%](images/pane_split_vertical.png)

`prefix + %`

???
TODO

---
class: middle, center

# Split Horizontally

![:scale 80%](images/pane_split_horizontal.png)

`prefix + "`

???
TODO

---
class: middle, center

# Panes

![:scale 80%](images/pane_list.png)

`prefix + s`

???
TODO

---
class: middle, center

# New Window

![:scale 80%](images/window_new.png)

`prefix + c`

???
TODO

---
class: middle, center

# New Window

![:scale 80%](images/window_new_split.png)

`prefix + "`

???
TODO

---
class: middle, center

# Session List

![:scale 80%](images/navigate01.png)

`prefix + s`

???
Go back to our session list and see everything we've created so far

---
class: middle, center

# Session List

![:scale 80%](images/navigate02.png)

???
- Using the keyboard to navigate.
- Hitting left and right to open / close the tree.

---
class: middle, center

# Session List

![:scale 80%](images/navigate03.png)

---
class: middle, center

# Session List

![:scale 80%](images/navigate04.png)

---
class: middle, center

# Session List

![:scale 80%](images/navigate05.png)

---
class: middle, center

# Session List

![:scale 80%](images/navigate06.png)

---
class: middle, center

# Session List

![:scale 80%](images/navigate07.png)

---
class: middle, center

# Session List

![:scale 80%](images/navigate08.png)

???
- Now you can use the index on the side to go to a specific pane.
- Let's select `8`

---
class: middle, center

# Session List

![:scale 80%](images/navigate09.png)

???
- Now back to session 1 window 1 pane 1
- All zero based of course

---
class: middle, center

# Pane Movement

TODO

---
class: middle, center

# Key Bindings

Defaults are vague and hard to remember

Vi and Emacs modes

???
Some notes...

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

???
- Manipulate everything from here
- Not often used, but handy for certain one off tasks

---
class: middle, center

# Copy Mode

TODO

???
- Probably my favorite feature
- I still use tmux in a tiling window manager because of this
- Modify the defaults to make it less aggravating

---
class: middle, center

# Mouse Mode

TODO

???
- The mouse is NOT evil!
- Modify it to make it MUCH more useful

---
class: middle, center

# Managing Environments

[Teamocil][teamocil]

[Tmuxinator][tmuxinator]

[And many more...][tmux-config-management]

???
- Lots of options
- Used Teamocil for years (because Arrested Development)
- Very helpful for repeated set ups locally or remote

---
class: middle, center

# Clients

Language libraries like python, ruby, etc.

---
class: middle, center

# Pair Programming

Wemux? TODO?

???
- Maybe not quite as easy as the VSCode pairing
- Could be good for two command line junkies though

---
class: top, left

# Links

- [My Dotfiles][dotfiles-claytron]
- [Awesome tmux](https://github.com/rothgar/awesome-tmux)
- Brian Hogan book TODO
- Tao of tmux book TODO
- TODO

[/ Links ---------------------------------------------------------------- /]: #
[dotfiles-indy]: https://meetingplace.io/Dotfiles-Indy
[twitter-claytron]: https://twitter.com/claytron
[dotfiles-claytron]: https://github.com/claytron/dotfiles
[teamocil]: https://github.com/remi/teamocil
[tmuxinator]: https://github.com/tmuxinator/tmuxinator
[tmux-config-management]: https://github.com/rothgar/awesome-tmux#tools-and-session-management
[/ ---------------------------------------------------------------------- /]: #
