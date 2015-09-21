powerline-evil
==============

[![GPL](http://img.shields.io/badge/license-GNU%20GPLv3-blue.svg)](https://github.com/raugturi/powerline-evil/blob/master/LICENSE)
[![MELPA](https://melpa.org/packages/powerline-evil-badge.svg)](https://melpa.org/#/powerline-evil)

Utilities for better Evil support for [Powerline](https://github.com/milkypostman/powerline).

## Installation

    (require 'powerline-evil)
    

## Faces

There are custom faces for each evil mode in the format `powerline-evil-<state>-face`. The appropriate value is returned by `powerline-evil-face` based on the current state, so once these faces are configured you can use that function in your theme to apply the correct face.

## Functions

The following helper functions for building powerline themes are provided by this package:
* `powerline-evil-face`: Returns the appropriate face for the current evil state as described in the [Faces](#faces) section.
* `powerline-evil-tag`: Returns the tag for the current evil state. See [Options](#options) for details about configuring the tag style.

## Themes

The package provides the following three themes:
* `powerline-evil-center-color-theme`: This is the same as the `powerline-center-evil-theme` that comes with Powerline, except the evil state section is color coded.
* `powerline-evil-vim-theme`: This is the same as the `powerline-vim-theme` that comes with Powerline, except with the evil state added to the beginning of the line.
* `powerline-evil-vim-color-theme`: This is the same as the `powerline-evil-vim-theme` above, except the evil state section is color coded.

## Options

The only configuration option (apart from the face customization) is `powerline-evil-tag-style` which is used to modify the behavior of `powerline-evil-tag`. It has 3 possible values:
* `standard`: It will simply return the current value of `evil-mode-line-tag` as it is provided by the evil package.
* `verbose`: It will return the name of the evil state in upper case. For the visual state if `evil-visual-selection` is block or line it will add those labels to the tag as well.
* `visual-expanded`: For all but the visual state this is the same as `standard`. For visual state if `evil-visual-selection` is block it will replace the angle brackets around the "V" with "+". If it is line it will replace the brackets with "-".
