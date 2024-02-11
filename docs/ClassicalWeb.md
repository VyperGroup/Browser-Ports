# ClassicalWeb - Proposal

This will be a port of Vivaldi to the web. Just like FoxyWeb you will need to import a zip file, but instead with ClassicalWeb you will need to import the crx files for the UI. This is because the entire UI runs inside of two chrome extensions. This port will work by running Vivaldi's UI inside of my chrome extension emulator, but with custom namespace APIs for Vivaldi. Unfortunately Vivaldi's UI is closed source and obfuscated, so it's a hard to understand what's going on. Gimmicks like their mail client will not be reimplemented.

[Developer notes](./For%20devs/ClassicalWeb.md)

## FAQ

- When will this release?

This will release before FoxyWeb

- Will there be a mobile version

There will not be a port for the mobile version of Vivaldi because it is modified from the the Chromium Mobile UI, which is hard to work with.
