# FoxyWeb - Proposal

> This will be the flagship port

This is a WIP port of [Firefox](https://www.mozilla.org/en-US/firefox) and [Dot Browser](https://www.dothq.org/en-US) (a Firefox fork) to a website. There will be a setup wizard when you first use it

[Developer notes](./For%20devs/FoxyWeb.md)

## Onboarding. The setup wizard

1. You will be prompted to and must provide your own Omni.ja file to support forks and for legal reasons. Omni.ja is a zip file that contains all the frontend code for Firefox. It was formerly a jar file, which is why they renamed it to .ja. On this.
2. You will be asked, if you want to migrate your data. You will be able to do this in two ways.

- Authenticate with your Firefox account for Sync or input a custom sync server
- if you don't want to do this or you have custom policies, prefs.js, userChrome.css files that you want to migrate, you will be able to import your backup data.

3. Finally, you will be asked if you want to theme your Firefox to look like your current browser. If you are using the original Firefox, obviously you won't be asked this (unless you are on Windows 11). You will be able to choose to switch to these modes manually in the settings. Here are the themes that will be supported:

- [Firefox Australis](https://github.com/QNetITQ/WaveFox#tabs-option-12)
- [Firefox Proton (87 and below)](https://github.com/zapSNH/zapsCoolPhotonTheme)
- [Chrome](https://github.com/edelvarden/material-fox-updated) and Chrome Mode
- [Windows 11 / Edge](https://github.com/Guerra24/Firefox-UWP-Style)
- [Safari](https://github.com/yarikbright/Firefox-Arc-Style)
- [IE6](https://github.com/WinClassic/MSFX)
- [Arc](https://github.com/betterbrowser/arcfox)
- [Opera](https://github.com/Godiesc/firefox-gx)
- [Epiphany](https://github.com/rafaelmardojai/firefox-gnome-theme)
- [Empheral](https://github.com/Zonnev/elementaryos-firefox-theme)

## Extra features that Vanilla Firefox and the other ports don't have

- Userscript support
- AdGuard support (undetectable)
  > These are just proxy middleware. I might implement them in the other ports.

### Chrome mode

In addition to the Chrome skin, Foxyweb will automatically function like chrome if you opt opt-in.
This will give you features such as:

- Chrome themes that will work by modifying the css from the theme, after reading the extension with my Extension Emulator.
- Ported [Chrome devtools from Ferrochrome](https://hedge.soundar.eu.org/s/PswwTTsw-#Devtools). Yes, Firefox's devtools will be supported later on.
- Forward Compat will be used to bring newer Chrome APIs to Firefox.

### Modifications to Firefox's internal pages

- Inside of about:policies the user will be able to modify built-in policies. You can use the editor or import from an external url to a JSON (Not recommended for security reasons)

### about:foxyweb

This will be an internal page.

> Changes made here will be optionally syncable with the offical Firefox Sync API. For configuring this, the web proxies used, and the bare servers used, there will a subcategory at the top inside of about:preferences called "FoxyWeb".

It will have:

- a built-in manager for userChrome.css styles. You will be able to modify multiple userChrome.css style modifications as you please, with an editor and toggleable buttons. You will also be able to import styles through a URL containing a userChrome.css.
- a built-in userscript manager using my userscript middleware

## Enterprise deployment

There will be additional policy options in about:policies that will allow you to customize any of the additional features that I have added to FoxyWeb.

## FAQ

> What about Mozilla VPN

1. The only thing that it won't support immediately is Mozilla VPN. I might consider otherwise, but adding VPNs is mostly useless since it is under a web proxy anyways. I can understand, if you need it for switching locations.
