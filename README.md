# Marp-vim
- just set vim keyMap on textarea using CodeMirror
- Please see below for more details.
------------------

Marp
===

**Markdown presentation writer, powered by [Electron](http://electron.atom.io/).**

![Marp](screenshot.png)

## Usage

### Install

:arrow_forward: **[Download latest archives from release page.](https://github.com/yhatt/marp/releases)**

- **Windows**: Unzip `*.*.*-Marp-win32-[arch].zip` and run `Marp.exe`.
- **Mac OS X**: Mount `*.*.*-Marp-darwin-x64.dmg`, D&D `Marp` to `Applications` and run it from Applications folder / Launchpad. Or use [Homebrew](http://brew.sh) [Cask](https://caskroom.github.io): `brew cask install marp`
- **Linux**: Unpack `*.*.*-Marp-linux-[arch].tar.gz` and run `Marp`.

### How to write slides?

Split slides by horizontal ruler `---`. It's very simple. Please refer to [example.md](https://raw.githubusercontent.com/yhatt/marp/master/example.md).

```md
# Slide 1

foobar

---

# Slide 2

foobar
```

## For developers

### Getting started

```
npm install
npm start
```

### Customizing Slide CSS

It's easy, include a `<link>` tag at the top of your presentation, or alternatively a `<style>` tag that contains all of your styles. All CSS should be targeting either `.slide` or elements inside of `.slide`. For reference, check out the gaia theme in the sass folder.

### Create release builds

```
gulp release
```

Please set application version in `package.json`.

#### OS specific

##### Windows

If you want to build for Windows in other platforms, please install [Wine](https://www.winehq.org/) to rewrite Electron's resources.

##### OSX

To build for Darwin is only supported in OSX. Please install [appdmg](https://github.com/LinusU/node-appdmg) to create archive (`.dmg`) for Darwin release.

```
npm install appdmg
```

###### Notices

- **Don't add development dependency of `appdmg` to `package.json`.** The release task would fail in other platforms.
- *`gulp-appdmg` is no longer in use since v0.0.4.*

## Licenses

Copyright &copy; 2016 [Yuki Hattori](https://github.com/yhatt).
This software released under the [MIT License](https://github.com/yhatt/marp/blob/master/LICENSE).
