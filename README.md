# Browser Ports Manifesto

> FIXME: Many of the docs right now are mismanged. For example, it isn't well regulated what is in the developer docs and the user docs. Additionally, some links need to be updated.

These are ports of Web Browser technology to the browser, primarily for use in proxy sites, where having no sandboxing restrictions can allow for many new use cases. I haven't yet devised an umbrella name for these two projects. Over time, I will deprecating a lot of my JS implementations of these APIs for WASM whenever I can.

- [Chrome](./docs/Ferrochrome.md) (Won't be 1:1 for a while)
- [Firefox](./docs/Foxyweb.md)
- [Firefox Mobile](./docs/FenixWeb.md)
- [Vivaldi](./docs/ClassicalWeb.md) (Without the Gimmicks)

> In order of releasing first

## Uses

- Evading censorship that uses enterprise policy control
- Being an enteprise and deploying these evil policies
  > Double teaming moment
- Running newer browsers on older OSs without having to backport user space
- Alternative browsers on a Chromebook without needing Crostini or OS write modifications
- Powerusers using the browser to get cross-browser extensions and syncing supporting browsers from different browsers. These ports can be used in a PWA. THINK ABOUT IT. You can go to any computer and just magically have your browser setup, as it is at home, with no downloading.
- Fun WebOS projects

## Features that aren't found in other browsers

- Proxy middleware will be used to integrate the ports with WebOS projects in an easy to use message-based API
- Eventually, extensions from **all browsers** will be supported, meanwhile Firefox extensions are fully compatible right now. This is powered by my Extension Emulator.
- When you are running browsers that don't support the lastest features that the version of the browser you use are using, through my proxy middleware Forward Compat, you will be able to regain these features.

## Tracking progress and ensuring compatibility

Unit tests will come from the browser's Monorepos themselves. They exclude any browser engine tests. I will have a progress tracker site that will list the realtime progress of the ports, and GH actions will check each PR to see if the tests pass.

## Prolouge / History

### The final frontieer

I believe that ported browsers to the web and WebOS projects are the perfect embodiment of a web proxy. As censorship becomes more prevalent, entire browsers and OSs are being geographically retricted. The best part about proxies is they are not vulnerable to attacks like DPI and they can be configured to only work with those that have the restricted devices. They are simple and unlike a VPN it is specialized to the web, so the core software isn't bloated and it can be modified and understood by many easily.

### How I got here

All the web proxy projects I have worked on have lead up to this point. If you notice this project makes use of all the proxy projects I have ever released. That is for a reason, this was all planned. Some have complained about my web proxy not releasing, however I have always explained that it was for experimentation purposes, and I have already found everything I need. I wanted to perfect my projects with consistant innovation not rush them. I have greater ambitions than just providing services to school students, however I will provide to anyone who is in need of these services. It also means that I have already written most of the backend code requiered to do this. If you think about it FoxyWeb is just Firefox's frontend with my proxy backend.
After this project releases, my final work will be Electron and Tauri ports to the web browser for custom WebOS solutions. I will wrap FoxyWeb for and make its APIs compatible with Tauri.

## FAQ

> Wouldn't this be slow?

1. No, unlike a remote browser, this will have nearly the same exact performance of normal browsing, because there will be near zero overhead. Remember the browser engine is completely removed. The only overhead is aero and the lightweight middleware itself, which is unnoticable. It will still support your favorite browser features and more.
