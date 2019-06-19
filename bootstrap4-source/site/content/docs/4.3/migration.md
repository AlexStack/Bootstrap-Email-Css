---
layout: docs
title: Migrating to v5
description: Track and review changes to the Bootstrap source files, documentation, and components to help you migrate from v4 to v5.
group: migration
aliases: "/migration/"
toc: true
---

## Browser support

See the browser and devices page for details on what is currently supported in Bootstrap 5. Since v4, here's what's changed to our browser support:

- Dropped support for Internet Explorer NN
- Dropped support for Firefox NN - MM
- Dropped support for Safari NN
- Dropped support for iOS Safari NN
- Dropped support for Chrome NN
- Dropped support for Android NN

## Sass

Changes to our source Sass files and compiled CSS.

- Removed `hover`, `hover-focus`, `plain-hover-focus`, and `hover-focus-active` mixins. Use regular CSS syntax for these moving forward. [See #28267](https://github.com/twbs/bootstrap/pull/28267).
- **Todo:** Remove previously deprecated mixins
  - `float()`
  - `form-control-mixin()`
  - `retina-img()`
  - `text-hide()` (also dropped the associated utility class, `.text-hide`)
  - `visibility()`
- **Todo:** New variables?
- **Todo:** Rearrange forms source files (under `scss/forms/`)
- **Todo:** Rearrange grid source files (under `scss/grid/`)
- Removed print styles and `$enable-print-styles` variable. Print display classes, however, have remained intact. [See #28339](https://github.com/twbs/bootstrap/pull/28339).

## JavaScript

Changes to our source and compiled JavaScript files.

- Dropped jQuery dependency and rewrote plugins to be in regular JavaScript.

## Grid and layout

Changes to any layout tools and our grid system.

- Dropped `.media` component as it can be built with utility classes. [See #28265](https://github.com/twbs/bootstrap/pull/28265).
- **Todo:** Remove `position: relative` from grid columns
- **Todo:** Integrate CSS grid into our grid system

## Content, Reboot, etc

Changes to Reboot, typography, tables, and more.

- **Todo:** Make RFS enabled by default

## Forms

- **Todo:** Move forms documentation to it's own top-level section
- **Todo:** Rearrange source Sass files (under `scss/forms/`)
- **Todo:** Combine native and custom checkboxes and radios
- **Todo:** Rewrite checks to support sizing (via `em`/`font-size` or explicit modifier classes)
- **Todo:** Combine native and custom selects
- **Todo:** Combine native and custom file and range inputs

## Components

### Alerts

- **Todo:** Remove auto-darkening of `<hr>` elements in `.alert-*` class variants. `<hr>`s use `rgba()` for their color, so these should naturally blend anyway.

### Badges

Badges were overhauled to better differentiate themselves from buttons and to better utilize utility classes.

- **Todo:** Removed and replaced `.badge` modifier classes with background utility classes (e.g., use `.bg-primary` instead of `.badge-primary`)
- **Todo:** Removed `.badge-pill` for the `.rounded-pill` utility class
- **Todo:** Removed badge's hover and focus styles for `a.badge` and `button.badge`.

### Jumbotron

- The jumbotron component is removed in favor of utility classes like `.bg-light` for the background color and `.p-*` classes to control padding.

### Popovers

- Renamed `.arrow` to `.popover-arrow`

### Tooltips

- Renamed `.arrow` to `.tooltip-arrow`

## Accessibility

- `.sr-only-focusable` does not require `.sr-only` anymore. [See #28720](https://github.com/twbs/bootstrap/pull/28720).

## Utilities

- Renamed `.text-monospace` to `.font-monospace`
- Decreased the number of responsive order utilities per breakpoint. The highest order utility with a number now is `.order-5` instead of `.order-12`. [See #28874](https://github.com/twbs/bootstrap/pull/28874).
- **Todo:** Drop `.text-hide` as it's an antiquated method for hiding text that shouldn't be used anymore
- **Todo:** Split utilities into property-value utility classes and helpers

## Build tools
