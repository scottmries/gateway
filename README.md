# Lighting design for gallery installation
## GATEWAY - Paintings for black light by Lena Hawkins
### May 17 - June 17, 2019, Newtown Radio, Brooklyn, NY

[Documentation](https://vimeo.com/370438075)

The included Puredata patches and QLC+ configuration implement a 5-channel DMX array designed to interact both with the blacklight-reactive material used in the paintings it lit and with the unpredictable month of music broadcast from the space in which it was installed.

This was accomplished as follows:

Five colors are chosen, corresponding to a pentahedron embedded in the HSV cone -- a combination of high-saturation and high-value, and low-saturation and high-value colors, pure and pastel colors, work particularly well with the paitings. This pentahedron then rotates about the HSV cone's axis over the course of an hour.

A small subset of all 3125 possible correspondences between these five points and five "abstract" fixtures is chosen in sequence; this master map will be iterated over relatively slowly.

Another sequence of maps is generated between each actual DMX signal and these five abstract fixtures. In each case, the sequence advances after its corresponding number of beats, as received from two independent clocks. The sequence is iterated over relatively quickly.

The two clocks in question correspond to opposing sides of a musical axis: beat-heavy/fast, and beat-light/slow, or dancy and ambient. A beat listener calculates the current music's placement along that axis and gradually adjusts a parameter. This parameter determines how frequently random, distantly spaced impulses are let through, vs. an occasionally changing sequence of sets of beats taken directly from the beat listener. An override was also implemented to control this parameter directly during live shows.

The overall effect of this implementation is a set of lighting arrangements that abruptly change, but often return to previous arrangements, in a manner that is not random but is very difficult to predict. Further, the frequency with which these arrangements change adjusts according to the quality of the music, displaying a kind of "mood" in its relation to the sound: engaged and in-time when it's four-on-the-floor, aloof and sponaneous when the music is more ambient.
