# ClassicalWeb - Dev Docs - Proposal

They have an extended version of the internal Chrome APIs but some for extra Vivaldi features

- They have their own sync service
- They have [their own theme APIs](https://themes.vivaldi.net/themes/ZQDJnPValLB). I don't know how it works yet. I need to reverse engineer it.
- They have their own user preferences in [prefs_definitions.json](http://wiki.viv.int/doku.php?id=prefs_system) and a flag system in features.json
- Since this uses chromium, I will have to emulate the policies feature. vivaldi://policy. This would mean that I would have to write GSuite proxy. I could also extend the GSuite proxy to allow "cracked" GSuite accounts. This would work on the normal chromium browsers too. Just another project for another day
- The entire Vivaldi UI is comprised of native web technologies (HTML/JS/HTML, NPM Modules, React, Webpack) and the Vivaldi APIs. This makes it extremely easy to port, other than the fact that it is closed-source. You can literally view Vivaldi's source code in `vivaldi://inspect/#apps`. The entire UI for Vivaldi is in a chrome extension! `chrome-extension://mpognobbkildjkofajifpdfhcoklimli/window.html`. It seems like they have a script that injects all the code when ran.
- They encourage modding the UI
