---
title: Home
layout: base
head_extra: |
  <link rel="stylesheet" href="/assets/css/home.css">
nav_order: 1
---

### Hi, I'm Arslaan!

# I'm a 13-year-old developer exploring programming, Linux, FOSS, iOS jailbreaking, embedded systems, robotics, and game development.

<details class="about-me">
  <summary>Read more about me</summary>
  <div markdown="1">

I like computer science, writing stories (sometimes), Linux, FOSS (Free Open-Source Software), hacking, reverse-engineering and iOS jailbreaking. My favorite genre of music is Hyperpop, particularly Hyperpop-Digicore & Hyperpop-Glitchcore. I work on various projects in low-level development, system programming, and hardware hacking. I'm also active in [Hack Club](https://hackclub.com){: target="_blank" }, a community of over 100,000+ teens around the world who code together. Come join the Slack and say hi!

I mainly use Gentoo Linux on my ThinkPad E16 Gen 3 (Intel Core Ultra 7 255H) with the bspwm tiling window manager along with picom, polybar, rofi, i3lock-color, sxhkd, and more. Currently, my dotfiles are not available on Git, but hopefully that will change in the near future. My favorite games are osu!, Minecraft and Stick Fight: The Game. I’ve been programming and tinkering with devices since somewhere around the age of six. What originally got me into programming was looking at my old iPad 2 (which I still have as of 2025, seven years later - it's now jailbroken with [EtasonJB](https://etasonjb.tihmstar.net/){: target="_blank" } because I felt like it) and saying – “how are these apps made?”


Feel free to explore my projects, stories, and achievements, and thanks for stopping by!

  </div>
</details>

<br/>

<div class="full-bar bg1">
<div class="content" markdown="1">

# [Saffron](https://git.arslaancodes.com/saffron.git/about/){: .white target="_blank" }

A lightweight, extensible, and dead-simple retained-mode UI framework written in C and SDL3.

- Built with: C, SDL3
- Status: In development (alpha)

---

## Features

- Retained-mode widget system
- GL support
- Extensible and modular
- Consistent styling across platforms

---

## Why I built it 

I looked at the current state of UI frameworks.
- GTK: Not very good on platforms other than Linux, and kind of bloated.
- Qt: Licensing headache, and styling is not consistent across platforms.
- Dear ImGui: Not retained-mode.
- Flutter: The toolchain is horrible, Dart sucks, and it's bloated.

And so, as I do, I decided to make my own lightweight and extensible UI framework on top of SDL3.

---

## Notes

There are currently a few things TODO in Saffron, as it is currently in alpha. For this reason, I would not recommend using it in production at the moment.

1. Write documentation
2. Test for other platforms (just because it theoretically should work, doesn't mean it will)
3. Add more built-in widgets
4. Possibly split it into 2 modular parts, SFCore and SFWidgetsBase (?)

</div>
</div>

<br/>

<div class="full-bar bg2">
<div class="content" markdown="1">

# [SaffronWebKit (SFWK)](https://git.arslaancodes.com/saffronwebkit.git/about/){: .white target="_blank" }

WPEWebKit bindings for Saffron, allowing you to embed webview widgets into any Saffron app with just a few lines of C.

- Built with: C, SDL3, WPEWebKit, GStreamer, EGL
- Status: Completed - in active development

---

## Features

- Full WebKit browser engine embedded into Saffron
- Supports Wayland, X11, and even runs in a TTY via SDL3's kmsdrm driver
- Full audio playback via GStreamer
- WebGL, HTML5 multimedia, and many other web APIs via WebKit

---

## Why I built it 

When I was building Saffron, I thought it'd be really cool to rewrite cinnamon-browser with it once it was stable. The issue was, it's a custom UI framework, how does one put a browser in it? The answer: just write your own bindings! It can't be that hard... right? Right???? Right...

This took up way too much time and effort than I thought it would.

---

## Notes

While Saffron itself is cross-platform, I cannot guarantee that SFWK will work across platforms because WPEWebKit, the library it is based on, is very much Linux-only.  
I am also yet to write documentation, but I am currently delaying that until Saffron itself has a stable API, because SFWK is subject to change based on what happens in Saffron's codebase.

</div>
</div>

<br/>

<div class="full-bar bg4">
<div class="content" markdown="1">

# [cinnamon-browser](https://git.arslaancodes.com/cinnamon-browser.git/about/){: .white target="_blank" }

A lightweight suckless-inspired vimlike browser written in C, powered by WebKit2GTK-4.1 and GTK3.

- Built with: C, GTK3, WebKit2GTK
- Status: Completed

---

## Features

- Vim-like keybindings
- Command mode with `:`
- Quickmarks (similar to ones in qutebrowser)
- Tabs
- Hint mode
- Suckless-style C configuration file (config.h)

---

## Why I built it 

For a while, I was a long-time user of qutebrowser, a popular vim-like browser written in Python and PyQtWebEngine. It was a great browser, and worked very well for my use cases, but eventually, I ran into an issue: the browser was too heavy on my system. Even though back then I used a MacBook Pro M2, which is a powerful machine, I only had 8GB RAM, which, in this digital world, is absolutely nothing. Open too many Chrome tabs? Good luck, mr. OOM killer has come to your doorstep. Because qutebrowser is powered by PyQtWebEngine, which in turn is powered by Chromium, it tends to be quite heavy on my system and eat a lot of RAM.

So, to fix this problem, there was only one proper way. MAKE YOUR OWN BROWSER IN C AND WEBKITGTK!!!!!!!!!!!!!!!!!!!!!!!!!

---

## Notes

This project will eventually be deprecated as I plan to rewrite it in Saffron, my UI framework. Why, you might ask? Because who doesn't want to have a custom browser written in their own custom UI framework AND their own custom browser engine bindings for that UI framework?! How, you might ask? With SFWK, of course! Did you not read the project listings above?

</div>
</div>

<br/>

<div class="full-bar bg5">
<div class="content" markdown="1">

# [Onyx Client](https://github.com/RealArslaanYT/onyx-client-core){: .white target="_blank" }

A modern, feature-packed client for Minecraft 1.21.5, designed to enhance the user experience with a variety of Quality of Life improvements and intuitive features. Mainly created as a side-project.

- Built with: Fabric, Java
- Status: Completed

---

## Features
- 1.8-style Combat
- Coordinates HUD
- Keystrokes HUD
- Freelook
- Mod state saving

--- 

## Why I built it 

No specific reason, I just wanted to get into Minecraft modding at the time and thought it'd be a fun project.

</div>
</div>

<br/>

<br/>
