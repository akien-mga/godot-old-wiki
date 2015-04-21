# BBCode for RichTextLabel

### Introduction

[RichTextLabel](class_richtextlabel) allows to display complex text markup in a control. It has a built-in API for generating the markup, but can also parse a BBCode.

### Setting Up

For RichTextLabel to work properly, it must be set-up. This means loading the intended fonts in the releavant properties:

<p align="center"><img src="images/rtl_setup.png"></p>

### Reference

Command | Tag | Description
--------|-----|-------------
*bold* | `[b]{text}[/b]` | Makes {text} bold.
*italics* | `[i]{text}[/i]` | Makes {text} italics.
*underline* | `[u]{text}[/u]` | Makes {text} underline.
*code* | `[code]{text}[/code]` | Makes {text} monospace.
*center* | `[center]{text}[/center]` | Makes {text} centered.
*right* | `[right]{text}[/right]` | Makes {text} right-aligned.
*right* | `[right]{text}[/right]` | Makes {text} right-aligned.
*fill* | `[fill]{text}[/fill]` | Makes {text} fill width.
*indent* | `[indent]{text}[/indent]` | Incrase Indent Level.
*url* | `[url]{url}[/url]` | Show <url> as such.
*url (ref)* | `[url=<url>]{text}[/url]` | Makes {text} reference <url>.
*image* | `[img=<path>][/img]` | Insert image at resource <path>.
*font* | `[img=<path>]{text}[/img]` | Use custom font at <path> for {text}.
*color* | `[color=<code/name>]{text}[/color]` | Change {text} color, use # format such as #ff00ff or name.

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


