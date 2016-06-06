# TextSuggest

Simple Linux utility to autocomplete words in the GUI.

![TextSuggest in action](http://i.imgur.com/nG5JAuA.gif)

**NOTE:** If you have not installed `dmenu2` (an extended fork of `dmenu`), you will see the suggestion bar at the bottom of the screen. To get the menu in the video, see [note](#note-on-dmenu).

Uses the [English Open Word List](http://dreamsteep.com/projects/the-english-open-word-list.html) for a basic dictionary. You can define custom words, see [the note](#custom-words).

Licensed under the [GNU GPL 3](https://www.gnu.org/licenses/gpl.txt).

# Installation

Make sure you have all the requirements:

 - `xdotool`
 - `xclip`
 - `dmenu` (See [note](#note-on-dmenu))

Assign keyboard shortcuts to

- `python3 /path/to/TextSuggest.py`
- `python3 /path/to/TextSuggest.py --noselect`

The first one gives you suggestions on the currently highlighted word.
The second one simply gives you a list of all word, you can search through them.

The script stores frequently used words in a history file (`~/.textsuggest_history.txt`). Suggestions more often used
are at the top of list.

**TIP:** You can search for words by their sparts by
typing `part1 part2 ... partN` at the `Type to search >` prompt.

# Custom words

Simply add them to the `Custom_Words.txt` file. The `Custom_Words.txt` file already has a
few jargon, abbreviations and words (total 1653 by default) not included in the EOWL.

# Note on dmenu

`dmenu` is contained in the `suckless-tools` package in Debian/Ubuntu.

For a better search menu, with:

- Position at mouse cursor instead of bottom
- Compact size

Install `dmenu2`, an extended fork of `dmenu`, by Michał Lemke at [melek/dmenu2](https://bitbucket.org/melek/dmenu2).

To enable `dmenu2`-specific features in `TextSuggest`, add the `--dmenu2` flag to the `TextSuggest.py` command.