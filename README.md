# Antenna Models
Antenna model files I have created or adapted from others, and some which are as-is.

Migrating models and descriptions to GitHub.

Work in progress as I add and reformat the text into markdown format, fixup file names, and convert images from GIF to PNG.

Blog posts referencing some of these at https://lonneys-notebook.blogspot.com/search/label/Antenna_Models

Antenna modeling helps validate ideas, designs, and guides us to a solution. It also develops a much better understanding of how they work.

`The models and information are provided as-is for self learning, and may contain errors or inaccuracies.`

# Antenna Modeling Software

[EZNEC](https://www.eznec.com) (.ez)
- [AutoEZ](https://ac6la.com/autoez.html) is an automation tool and optimizer used in conjunction with EZNEC (.weq).
- [Arrayfeed](https://eznec.com/misc/Arrayfeed/) ([PDF Manual](https://raw.githubusercontent.com/lonney9/Antenna-Models/main/software/Arrayfeed/Arrayfeed1.pdf)) is used with EZNEC to calculate coax line lengths (Christman) or L network values with 1/4 wave lines (current forcing) for two and four element phased arrays. [Feed2EL](https://ac6la.com/feed2el.html) is an Excel version of Arrayfeed with additional features. [This post](https://lonneys-notebook.blogspot.com/2020/10/phased-arrays-christman-feed-system.html) covers a practical example using Feed2EL and EZNEC.
- [Advanced Antenna Modeling Book](http://www.on5au.be/advanced_modeling_book.html) covers using EZNEC and AutoEZ from beginner to advanced users.
- EZNEC (now free, but no longer to supported or developed) is likely the better choice as it includes high accuracy ground model, wire insulation, transmission lines, L-Networks, Transformers and more. This provides the ability to model complete antenna systems as they would be built to see how a design behaves over the given bandwith. 4NEC2 I understand can do most of or all of this but is in my expierence is harder to use.

[MMANA-GAL](http://gal-ana.de/basicmm/en/) (.maa) / [GAL-ANA](http://gal-ana.de/) (.gaa)

[4NEC2](https://www.qsl.net/4nec2/) (.nec)