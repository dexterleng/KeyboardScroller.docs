<div align="center">
  <img width="200" alt="AppIcon" src="https://user-images.githubusercontent.com/34204380/187025943-93bec8ae-65c0-4e9f-83fd-7906900ce011.png">
  <h1>Keyboard Scroller</h1>
  <p>
    <b>Trackpad-smooth scrolling with keyboard shortcuts</b>
  </p>
  <br>
</div>

## Demo

https://user-images.githubusercontent.com/34204380/187025861-dec3a21d-dc22-452c-8a4c-5c1705f79c83.mp4

The app let's you scroll through apps, documents, and messages without lifting your fingers off the keyboard. à la Vimium's scroll feature.

## Download

Download the latest release [here](https://github.com/dexterleng/KeyboardScroller.docs/releases/tag/v1.0.1). View all versions and changelog [here](https://github.com/dexterleng/KeyboardScroller.docs/releases).

Requires macOS 12.3 or later.

## How to use it

I use [Hyperkey](https://hyperkey.app) to remap `Caps Lock` to `⌃⌥⇧⌘`.

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

I work on [Homerow](https://homerow.app), which has a modal workflow for scrolling. You hit a shortcut to enter "Scroll-mode", you hit `HJKL` to scroll, `Tab` to switch the active scroll area.

I wanted to experiment with an ephemeral workflow using keyboard shortcuts to scroll directly, and see how it compares with the modal workflow in Homerow.

However that was not the plan from the start. I originally I wanted to rewrite Homerow's Scroll-mode to explore SwiftUI, play with additional features like [Jumpers and Freestyle](https://twitter.com/dexterleng/status/1554070218783477765), and [snapshot testing the Accessibility API integration to prevent regressions](https://twitter.com/dexterleng/status/1556613890414637056). The poor code quality in Homerow may have played some part in wanting to do a rewrite. I found myself having find workarounds to implement everything with SwiftUI that would have been fairly simple with AppKit, and overally it was just not fun. Since I plan on continuing using AppKit, there wasn't a point in making Scroll-mode a separate app, and a refactor in Homerow makes more sense.
