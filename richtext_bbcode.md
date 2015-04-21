# BBCode for RichTextLabel

### Introduction

[RichTextLabel](class_richtextlabel) allows to display complex text markup in a control. It has a built-in API for generating the markup, but can also parse a BBCode.

### Setting Up

For RichTextLabel to work properly, it must be set-up. This means loading the intended fonts in the releavant properties:

<p align="center"><img src="images/rtl_setup.png"></p>

### Reference

Command | Tag | Description
--------|-----|-------------
_bold_ | `[b]{text}[/b]` | Makes {text} bold.
_italics_ | `[i]{text}[/i]` | Makes {text} italics.
_underline_ | `[u]{text}[/u]` | Makes {text} underline.
_code_ | `[code]{text}[/code]` | Makes {text} monospace.
_center_ | `[center]{text}[/center]` | Makes {text} centered.
_right_ | `[right]{text}[/right]` | Makes {text} right-aligned.
_right_ | `[right]{text}[/right]` | Makes {text} right-aligned.
_fill_ | `[fill]{text}[/fill]` | Makes {text} fill width.
_indent_ | `[indent]{text}[/indent]` | Incrase Indent Level.
_url_ | `[url]{url}[/url]` | Show <url> as such.
_url (ref)_ | `[url=<url>]{text}[/url]` | Makes {text} reference <url>.
_image_ | `[img=<path>][/img]` | Insert image at resource <path>.
_font_ | `[img=<path>]{text}[/img]` | Use custom font at <path> for {text}.
_color_ | `[color=<code/name>]{text}[/color]` | Change {text} color, use # format such as #ff00ff or name.

### Built-In Color Names

List of valid color names for the [color=<name>] tag:

* aqua
* black
* blue
* fuchsia
* gray
* green
* lime
* maroon
* navy
* purple
* red
* silver
* teal
* white
* yellow


