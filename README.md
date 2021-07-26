# search-bookmarks-and-history

Chrome extension to search bookmarks and history.

It also supports searching for bookmark folder names and tags.

## Installation

### Developer Installation

The extension can only be installed locally right now, as it has not been published to the store.

* Check out this extension via git or .zip download
* Go to chrome://extensions/ 
  * Enable "Developer mode"
  * Load unpacked and open the root folder of this repository

> This extension is WIP and only for private use first.
> It is rather configurable, but you need to change the options in `popup/popup.js`

## Demo

![Demo GIF](/images/bookmark-and-history-search.gif "Demo GIF")

## Tipps & Tricks
* This extension can (and should!) be triggered via keyboard shortcut.
  * The default is `CTRL` + `.`
* If you start your query with `+`: only history will be searched
* If you start your query with `-`: only bookmarks will be searched
* Fuse.js Extended Search operators can be used:
  * https://fusejs.io/examples.html#extended-search
* You can tag your bookmarks by just adding `#one tag` or `#first #second` tags to it after the title.
* If you want to search for bookmark tags:
  * Start your query with `#` for fuzzy search
  * Start your query with `'#` for more precise search
* If you want to search for bookmark folders:
  * Start your query with `>` for fuzzy search
  * Start your query with `'>` for more precise search

## Credits

This extension makes use of the following helpful open-source projects (thanks!):
* https://bulma.io/
* https://fusejs.io/

## Ideas and To Dos
* Make extension configurable via UI (requires new `storage` permission)
* Allow to search and navigate open Tabs (requires new `tab` permission)
* Add a Dark Theme
* Allow to quick add & edit bookmarks (title + tags)
  * tags would ideally have autocomplete, based on existing tags (something like select2)
  * quick add current open site via + button
* Try other search algorithms / libraries that are less fuzzy
  * https://github.com/nextapps-de/flexsearch 
* Create one index per type (bookmarks, history) to improve performance
