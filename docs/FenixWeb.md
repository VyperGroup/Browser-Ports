# FenixWeb - Proposal

A planned port of Firefox Mobile to the web. This might be possible because Firefox uses Jetpack Compose and it [supports compilation to WASM](https://seb.deleuze.fr/introducing-kotlin-wasm/#compose-multiplatform). I would have to replace the GeckoView components with my own WASM binded [proxied iframe](https://hedge.soundar.eu.org/s/hLUaC8rns#HTML-element1).
