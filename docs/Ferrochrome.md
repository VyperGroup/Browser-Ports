# Ferrochrome - Proposal

This will be a partial port of Chromium to the web.

[Developer notes](./For%20devs/Ferrochrome.md)

## Browser UI

The Browser UI will not be ported at this time due to its [complexity](./For%20devs/Ferrochrome.md#Chrome-UI). This is why the port won't be 1:1, unlike the others. The good news is that this backend code will be used in alternative frontends that implement this. One is in the works right now by proudparrot.

## WebUI pages

This represents the sites that start with chrome://.

[Developer notes](./For%20devs/Ferrochrome.md#WebUI)

### Devtools

#### Uses

- Once I get devtools working on Ferrochrome, it will be possible to use Chrome's devtools on mobile, restricted or older browsers.

[Developer notes](./For%20devs/Ferrochrome.md#Devtools)

### Omnibox

#### Uses

- This will be used for [Proxy Components](https://github.com/VyperGroup/Proxy-Components)

[Developer notes](./For%20devs/Ferrochrome.md#Omnibox)
