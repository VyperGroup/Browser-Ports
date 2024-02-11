# FoxyWeb Dev Info - Dev Docs - Proposal

FoxyWeb will comprise of a series of patches for the files inside of Omni.ja. That's all it is. By patches I mean .patch files
It will replace GeckoView with my [proxified iframe](https://hedge.soundar.eu.org/s/hLUaC8rns#HTML-element1)

## Directories

### apis/ -> The main code

- Sys -> Firefox's Internal Config; works through a c++-like preprocessor system
- Global -> Objects that are included in the Global scope automatically
- Res -> Resources, usually imported scripts

### test/ -> Unit testing

## Internal page url routing

The maps will be imported in [JSON](https://searchfox.org/mozilla-release/source/tools/esmify/map.json). These maps will be routed on the request middleware for FoxyWeb. Additionally the cC api will be These may vary depending on the fork.

## APIs

These apis are currently undocumented. They [used to be documented](https://udn.realityripple.com/docs/Mozilla/Tech) in the pre-quantum days; however, now they are only known and [discussed](https://discourse.mozilla.org/) _[old](https://groups.google.com/g/mozilla.mdn)_ by Firefox devs

### C++ -> JS bindings

The bindings will usually be integrated with WASM bindings. The exceptions include: Browser engine specifics and OS-related / Windowing code. These [bindings use WebIDL](https://webidl.spec.whatwg.org) and are imported inside of Services.jsm. Services is simply defined by Cu.createServicesCache().

### cC API

I don't know much about this but I know that Services calls it. I currently believe this is the only object that is predefined, so I must investigate this as soon as I can.
