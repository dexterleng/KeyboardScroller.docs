<div align="center">
  <img width="200" alt="AppIcon" src="https://user-images.githubusercontent.com/34204380/187113812-3a5f42c9-b008-4851-ab94-140a8a728942.png">
  <h1>Keyboard Scroller</h1>
  <p>
    <b>Scroll with the keyboard in macOS</b>
  </p>
  <br>
</div>

## Demo

<video src="https://user-images.githubusercontent.com/34204380/187025861-dec3a21d-dc22-452c-8a4c-5c1705f79c83.mp4" controls autoplay loop muted playsinline style="max-height:640px;"></video>

Keyboard Scroller helps you scroll through apps, websites, and documents without lifting your fingers off the keyboard. à la Vimium's scroll feature.

## Why not just use `PgUp` and `PgDn` to scroll?

`PgDn` scrolls really quickly by a whole page per keypress, which I find disorientating. Keyboard Scroller allows `PgUp` and `PgDn` (or custom shortcuts) to scroll continuously and smoothly.

## Features

- 😎 Trackpad-smooth scrolling with `PgUp` and `PgDn`
- ⌨️ Bind custom shortcuts to scroll
- 🦘 Two types of scrolling - Normal and Jump (scrolls by a fixed distance)
- ⚙️ Customize scroll speed and jump distance
- 🎯 Automatically moves your cursor to the active window when scrolling

## Download

Download the latest release [here](https://github.com/dexterleng/KeyboardScroller.docs/releases/tag/v1.0.1). View all versions and changelog [here](https://github.com/dexterleng/KeyboardScroller.docs/releases).

Requires macOS 12.3 or later.

## How to use it

Simply set the `Remap PgUp & PgDn` option to either `Scroll` or `Jump`!

Alternatively, you can set custom keyboard shortcuts for easier access to scrolling.

Personally, to avoid lifting my fingers off the home row, I use [Hyperkey](https://hyperkey.app) to remap `Caps Lock` to `⌃⌥⇧⌘`.

Then I use the following bindings in Keyboard Scroller's Preferences:

- `Scroll up` to `⌃⌥⇧⌘K`
- `Scroll down` to `⌃⌥⇧⌘J`
- `Jump up` to `⌃⌥⇧⌘U`
- `Jump down` to `⌃⌥⇧⌘D`

For slowly scrolling through a document I use Scroll, and for dashing through I use Jump.

## Known issues

- Scrolls super fast in VSCode
- "Mouse scroll fixer" apps (e.g. Mos and Mac Mouse Fix) cause scrolling to jump long distances

## Why I made this

I work on [Homerow](https://homerow.app), which has a modal workflow for scrolling. You hit a shortcut to enter "Scroll-mode", then hit `HJKL` to scroll, and hit `Tab` to switch the active scroll area.

I wanted to experiment with an ephemeral workflow using keyboard shortcuts to scroll directly and see how it compares with the modal workflow in Homerow.

However, that was not the plan from the start. I originally wanted to rewrite Homerow's Scroll-mode to explore SwiftUI, play with additional features like [Jumpers and Freestyle](https://twitter.com/dexterleng/status/1554070218783477765), and [snapshot testing the Accessibility API integration to prevent regressions](https://twitter.com/dexterleng/status/1556613890414637056). The poor code quality in Homerow may have played some part in wanting to do a rewrite. I found myself having to find workarounds to implement everything with SwiftUI that would have been fairly simple with AppKit, and overall it was just not fun. Since I plan on continuing using AppKit, there wasn't a point in making Scroll-mode a separate app, and a refactor in Homerow makes more sense. Keyboard Scroller is simply a by-product of the prior mentioned explorations.

## FAQ

### Do you track any data?

Nope.

### Why do you need Accessibility API permission?

To emit scroll events using the `CGEvent` API.

### Do you plan on making it open source?

I might.

### How can I support this project?

Share it with a friend and [buy me a coffee](https://www.buymeacoffee.com/dexterleng)!
