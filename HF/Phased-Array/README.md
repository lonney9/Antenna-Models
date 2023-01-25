# Phased Arrays

Two element phased array examples using coax delay lines Christman / Simple Feed, Current Forcing, Opposite Voltage Fed feed systems.

The important factors with phased arrays are phase shift and current magnitudes. Different array types and their element spacing need different amounts of phase shift, this phase shift must be delivered with near equal current magnitudes in each element. If both of these are not true the array will not perform due to poor front to back ratio.

Some believe otherwise, and transfer the 84/71 Christman system to other array types, or use 90 degree lines assuming it just works (it doesn't when you model it).

https://lonneys-notebook.blogspot.com/search/label/Phased_Arrays contains a number of posts (goal is to convert to markdown for viewing on GitHub) on the three main types of phased array feed systems, with how to calculate them and example models.

My hope is that this information is easy to follow and removes the mystery around two element phased arrays. I figured most of this out on my own after finding there is no source of information that lays it out in a clear and simple way with practical examples.

ON4UN's Low Band DXing book (which is an excellent resource) has a chapter on phased arrays, it is a math heavy deep dive into the subject that I could not easily follow.

## Christman / Simple Feed

The amount of phase shift is only equal to the line length in degrees when the lines are terminated into their characteristic impedance. This is almost never the case due to the mutual coupling between the elements.

The most commonly known line lengths are a pair of 84 degree lines and a 71 degree line, this was calculated for use with a pair of ground mounted 1/4 wave verticals and their specific driving impedances.

Coax delay lines are correctly calculated starting with a two source model, driving impedances inputted into [Arrayfeed1](https://eznec.com/misc/Arrayfeed/) which calculates the coax lengths, model updated using transmission lines with the calculated lengths, virtual connections are used to join them, and the source moved where the lines meet at the virtual connection.

Then we can see how the array behaves over the desired bandwidth, and check the current magnitudes. Sometimes the result is not as good as hoped.

Example: https://lonneys-notebook.blogspot.com/2020/10/phased-arrays-lewallens-simple-feed.html

## Current Forcing

This uses an L network with fixed 1/4 wave coax lines. 

Same as Christman / Simple Feed, the L network values are calculated by starting with a two source model, driving impedances inputted into [Arrayfeed1](https://eznec.com/misc/Arrayfeed/) which calculates the L network values, model updated using the L network function + two 1/4 wave transmission lines connected using virtual connections.

Example: https://lonneys-notebook.blogspot.com/2020/12/phased-arrays-40m-twin-half-square.html

## Opposite Voltage Fed

OVF was developed by Pekka Ketonen [OH1TV](https://oh1tv.fi/).

This system uses one or two 1/2 wave lines meeting at one element or a common point.

A loading inductor is inserted in series with one line lowering the resonant frequency of one element.

The Element lengths (resonant above the design frequency) in conjunction with the spacing the the loading inductor value work together to arrive at the right phase shift and equal current magnitudes.

Sounds complex, but it can be modeled with out a calculating tool and some trial and error to find the right combination of element length and loading indicator value. This is found by peaking the F/B then moving an equal frequency above and below the center, when the patterns either side of center match you've found the sweet spot, then looking at the current magnitudes in EZNEC they should be very close to equal.

As with Christman and Current Forcing, a switching network can make this array reversible swapping the direction by simply changing which line has the loading inductor inserted.

An L Network is then used to match 50 ohms to the main feed line.

This system is my favorite for several reasons:
- Its simple
- No complex calculation or calculator tool is needed
- Symmetrical pattern stability over a (sometimes much) wider bandwidth compared to Christman or Current Forcing
- Flexible on element spacing from 1/8 to 1/3 wavelength (closer spacing reduces operational bandwidth)
- Works with any element type from verticals, horizontal dipoles, loops, and half square arrays

Example: [https://lonneys-notebook.blogspot.com/2020/11/phased-arrays-opposite-voltage-fed-ovf.html](https://lonneys-notebook.blogspot.com/2020/11/phased-arrays-opposite-voltage-fed-ovf.html).
