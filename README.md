# Thunderbird User Chrome

Customization of the appearance of Thunderbird.

## Customizations

### Unread Message Tiles

This style updates the visual style of cards marked "unread" within #threadTree to make them stand out more. Their background is blue, the tile itself is a lighter blue, and the tile is given a thicker light cyan outline.

## Installation

1. Locate the Thunderbird data directory. This is typically `.thunderbird` off of the profile root, but the catch is that on some distributions, Thunderbird is installed as a Snap, which gives it its own isolated profile directory. On my system, it's `/home/logiclrd/snap/thunderbird/common/.thunderbird`

2. Locate the profile directory within the Thunderbird data directory. On my system, it got named `zwmhiwaf.default-release`.

NB: There is a shortcut for going directly to the directory in question. Simply go to the Help menu -> Troubleshooting Information, and in the resulting tab, look in the grid under "Application Basics". There should be an item labelled "Profile Directory" with a handy "Open Directory" button.

3. Place the `userChrome.css` file into this directory.

4. Enable Thunderbird's processing of user chrome. To do this, go to Edit -> Settings, in the resulting tab scroll straight to the bottom and click "Config Editor", and then in _that_ resulting tab, search for `toolkit.legacyUserProfileCustomizations.stylesheets`. If it isn't present, add it as a Boolean. Set its value to `true`.

5. Restart Thunderbird.

## Tweaking

Thunderbird's UI is written in HTML+CSS which is presented with the Firefox engine. You can use the Developer Toolbox to inspect the Thunderbird UI's DOM in order to figure out what exactly needs to be done in `userChrome.css` to achieve your desired style. To access the Developer Toolbox, select menu item Tools -> Developer Tools -> Developer Toolbox.

Any time you alter `userChrome.css`, you'll have to restart Thunderbird for it to take effect.
