# Ferrochrome - Dev Docs - Proposal

## Chrome UI

If you want to see how the UI works through tinkering, despite it not being made with native web technology, [you can debug it through inspect](https://chromium.googlesource.com/chromium/src/+/main/docs/ui/learn/ui_debugging.md).

### Small rundown on how the Chrome UI system works

1. An [Aura](https://www.chromium.org/developers/design-documents/aura/graphics-architecture) (Formerly [Ash](https://github.com/blueboxd/chromium-legacy/blob/master.lion/docs/ui/learn/glossary.md#ash)) window is created. This wouldn't be important for running on the Web.
2. These two wouldn't be relevant for Ferrochrome, rather you should run the components in HTML.
3. The GUI is managed by a library called Skai. [Skai kinda works on WASM](https://source.chromium.org/chromium/chromium/src/+/main:third_party/skia/experimental/wasm-hello-world/BUILD.bazel)
4. Chrome's UI is finally rendered in [Views](https://chromium.googlesource.com/chromium/src/+/master/docs/ui/views/overview.md) a Skai library. Views has custom XML elements with CSS. What makes it difficult to work with, is that the custom functionality is programmed in C++.

### Unit Testing

- <https://skia.org/docs/dev/testing/skiagold>

## Chrome Extensions

### Extensions

### Themes

## WebUI

For the most part WebUI pages use Polymer and some of the new ones use Lit-HTML. For C++ to JS bindings Mojo is used. Mojo interface calls will be intercepted and either ran in preferrably WASM or emulated with proxy middleware.

### Devtools

`devtools://devtools/bundled/inspector.html`

Many assets are fetched from <https://chrome-devtools-frontend.appspot.com>

#### Test cases

> This is more of a link collection right now

- <https://github.com/chromium/chromium/blob/92ea470ab69c1e86526fd5137e6cf8d9647b4199/chrome/test/data/devtools/extensions/can_inspect_url/manifest.json>
- <https://github.com/chromium/chromium/blob/92ea470ab69c1e86526fd5137e6cf8d9647b4199/headless/test/data/protocol/inspector-protocol-test.html>

### Omnibox

`chrome://omnibox`

This will require me having to compile the Mojo-bindings to WASM and intercept the calls.

### Info (REMOVE THIS)

Chrome's test cases work like [this](https://github.com/chromium/chromium/blob/92ea470ab69c1e86526fd5137e6cf8d9647b4199/chrome/test/data/devtools/extensions/can_inspect_url/manifest.json) TODO:...
