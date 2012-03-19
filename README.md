# ext-sozi
SVG-Edit extension to use Sozi in your SVGs

## About
This is an extension to [SVG-Edit](http://code.google.com/p/svg-edit) with the purpose of creating [Sozi](https://github.com/senshu/Sozi) presentations. Created to be used as part of [24MAS](http://www.24mas.com) project.

## Demo
http://asyazwan.github.com/ext-sozi/

## Technology
* [SVG-Edit](http://code.google.com/p/svg-edit) a very cool DOM-based in-browser SVG editor. Everything is client-side. Currently using 2.6-alpha.
* [Sozi](https://github.com/senshu/Sozi) (Main [site](http://sozi.baierouge.fr/wiki/en:welcome)) create presentation SVG by parsing sozi attributes attached to SVG elements. Currently using v11.10
* [saveAs()](https://github.com/eligrey/FileSaver.js) for Chrome (and potentially others), which saves your SVG automatically (you might get a prompt to Keep/Cancel the file).
* [Downloadify](https://github.com/dcneiner/Downloadify) for FF, a small flash-based file saving app. No server contacts are made (which is precisely why I chose to use Flash instead of contacting server to get proper header and save dialog).

## Support
It is important to understand that I created this extension to use in *my* project, which I do not need to care about Internet Explorer, Safari, and Opera (I have cool bosses). Thus I have chosen to support only newer FireFox and Chrome. It may or may not work on other browsers. If you're up for testing on other browsers, patches are welcomed!

Some stuff I use that you may need to check browser support for:
* File-saving mechanism. If your browser do not support FileSaver (or saveAs() above) API and you do not want Flash-based solution provided, then you're on your own
* createObjectURL which is used for previewing your project

## Sozi InkScape extension
* This extension _IS NOT_ compatible with the InkScape extension. This is by design as I have chosen to enforce frames layer. All Sozi frames must be in one layer. I also added a few more custom attributes to help in rebuilding saved SVG in SVG-Edit.

## Code
I am aware that the code is not ideal and can be improved. I started this with proper unit testing but as dateline approaches everything moved too fast, so yeah. It was also tightly integrated with other part of my project which I had to split just to open source the sozi part. So there may be some stuff I overlooked in the process.

My main goal is to make this pass JSLint. If you can help with it, please do!

Also the convention and styling (8 columns tab) is inherited from SVG-Edit. So please stick to it if you want to provide patches/pull request.

## Issues, Suggestions, Wishlist
Use the issue tracker to provide feedback, report bugs, or post suggestions.

