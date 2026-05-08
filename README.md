# KLayout Snap Mode Plugin

`Snap Mode Plugin` adds a menu and shortcut layer for switching path routing and object movement constraints in KLayout.

It provides a workflow similar to `Snap Mode` from Cadence Layout XL by letting the user switch quickly between orthogonal, diagonal, and any-direction movement/path constraints.

## Features

- Adds `Edit -> Snap Mode`
- Adds `Choose Snap Mode...` popup menu
- Shortcuts:
  - `N` for diagonal
  - `Ctrl+N` for orthogonal
  - `Ctrl+Shift+N` for any direction
- Applies the mode to both:
  - path drawing (`edit-connect-angle-mode`)
  - movement/orientation constraints (`edit-move-angle-mode`)
- Rebinds:
  - `Ctrl+Shift+F` to Zoom Fit Selection
  - `Ctrl+Alt+N` to New Hierarchical Layout

## Installation

### From Salt.Mine

Install `Snap Mode Plugin` from Salt once the package is published.

### Manual install

Copy this repository into your KLayout Salt directory so that `grain.xml` sits at the package root:

```text
~/.klayout/salt/SnapModePlugin/
```

KLayout will discover the package automatically on next start.

## Files

- `grain.xml`: Salt package metadata
- `pymacros/snap_mode_menu.lym`: autorun macro implementation

## Notes

- The plugin was written by OpenAI Codex, GPT-5.4 default, in a live coding session for Michał Wołodźko.
- Functional behavior was verified in vivo by Michał Wołodźko in his KLayout environment.
- The implementation stays self-contained and can be removed by deleting this one package directory.

## License

MIT
