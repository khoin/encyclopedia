---
permalink: software-licensing
title: Software Licensing
date: 2019-08-22
tag: [legal, software]
category: concepts
---

When I implemented the [Dattorro-Griesinger Reverb in Javascript](https://github.com/khoin/DattorroReverbNode), my professor advised me to choose other open-source licenses over my very bare statement releasing the implementation into the Public Domain.

The suggested licenses were GPL3 or Apache 2 or MIT. I, however, still wanted a very simplistic license that holds me no liability while still releasing it to the Public domain. 

I looked at [The Unlicensed](https://unlicense.org/), but it seemed longer than I would prefer. At the same time, [SQLite](https://www.sqlite.org/copyright.html) seems to make no statement on liability. 

I came up with my own license (which is probably a bad idea), which is essentially a striped down version of The Unlicensed and a simplified liability disclaimer clause, which spun off MIT/X11. I also looked at [how USGS handles liability](https://www.usgs.gov/information-policies-and-instructions/liability) and added an addition phrase to carry over the liability disclaimer in the case of distribution.

Here is the full-text:

```
In jurisdictions that recognize copyright laws, this software is to
be released into the public domain.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND.
THE AUTHOR(S) SHALL NOT BE LIABLE FOR ANYTHING, ARISING FROM, OR IN
CONNECTION WITH THE SOFTWARE OR THE DISTRIBUTION OF THE SOFTWARE.
```

Rationale for modifications from The Unlicensed:

* **"free and unencumbered software"**: simplified to "software". I believe PD implies `free` and `unencumbered`.
* **"In jurisdictions that recognize copyright laws,"** (third paragraph of Unlicensed): I moved the first clause to the first paragraph, removing the rest of it. To me, it is just added fluff.
* Second paragraph is removed altogether. I believe PD implies the second paragraph.
* **"WITHOUT WARRANTY OF ANY KIND"**: is kept with the removal of the succeeding clauses. I believe "ANY KIND" implies the rest of it.
* **"IN NO EVENT"**: is removed, again because I believe "NOT BE LIABLE FOR _ANYTHING_" implies temporally as well.
* **"THE DISTRIBUTION OF THE SOFTWARE"**: was added following USGS liability disclaimer. I find this appealing to add because "using the software", "modifying the software and use it" would fall under "ARISING FROM, OR IN CONNECTION WITH THE SOFTWARE", but if someone where to be harmed by _the distribution_ of the software, the latter clause takes care of the second-order relation. This appears to be a problem of blameworthy. If I were to make video games, and parents sue me for their child being addicted to the video games, the first clause takes care of it. However, let's play with the case where a wife is distressed over their spouse _distributing_ my video games: Can the wife sue me if I didn't have the "distribution" extension?

In any case, I'm not a lawyer, and at the end of the day I can only hope I'll never run into a Kafkaesque situation.