# Changelog

## Unreleased
### Added
### Changed
### Deprecated
### Removed
### Fixed
### Security


## 1.2.0

### Added
* Run-time text resize using ctrl-+, ctrl+- and ctrl+0
* Font size adjusts dynamically to outputs' DPI
* Reflow text when resizing window
* **pad** option to `footrc`
* **login-shell** option to `footrc` and `--login-shell` command line
  option
* Client side decorations (CSDs). This finally makes foot usable on
  GNOME.
* Sixel graphics support
* OSC 12 and 112 escape sequences (set/reset text cursor color)
* REP CSI escape sequence
* `oc` to terminfo
* foot-server.desktop file
* Window and cell size reporting escape sequences
* `--hold` command line option
* `--print-pid=FILE|FD` command line option

### Changed
* Subpixel antialiasing is only enabled when background is opaque
* Meta/alt ESC prefix can now be disabled with `\E[?1036l`. In this
  mode, the 8:th bit is set and the result is UTF-8 encoded. This can
  also be disabled with `\E[1024l` (in which case the Alt key is
  effectively being ignored).
* terminfo now uses ST instead of BEL as OSC terminator
* Logging to print to stderr, not stdout
* Backspace now emits DEL (^?), and ctrl+backspace emits BS (^H)

### Removed
* '28' from DA response