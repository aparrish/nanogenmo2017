# The Average Novel

[Allison Parrish](http://www.decontextualize.com/)

This repository contains the source code for my [NaNoGenMo
2017](https://github.com/NaNoGenMo/2017/) project. I made a list of all the
books labelled "fiction" in Project Gutenberg and averaged them together using
word vectors.

[Here's the result.](the-average-novel.txt)

[This Jupyter notebook](normalize-length-and-average.ipynb) explains the
process in more detail. (Unfortunately, you won't be able to totally replicate
the process of generating the novel from this code alone, since the
`gutenfetch` module depends on the particular arrangement of files in my own
Project Gutenberg disk. But hopefully it's enough to get the gist across!)

## Vectors and corpora

To make this project, I trained 100d word vectors from a corpus of several
thousand novels (actually: texts labelled as being fiction) in Project
Gutenberg. [You can download those vectors
here](https://s3.amazonaws.com/aparrish/novel-vectors-word2vec.gz) (~200MB
file).

I can also share the corpus of sentences from these novels that I used
to train the vectors, but that file is much larger and more cumbersome---for
now, please get in touch with me directly for access.

The Project Gutenberg files I used for this project were taken from
[Gutenberg-tar](http://gutenberg-tar.com/).

## Acknowledgements and licenses

The text of *The Average Novel* is made available under a <a
href="https://creativecommons.org/licenses/by/4.0/">CC BY 4.0</a> license.

The file `47000_metadata.json`, containing metadata on the texts in Project
Gutenberg, was produced by [Leonard
Richardson](https://twitter.com/leonardr/status/667049187918356480)

The file `gutenberg.py`, used for pre-processing the texts, is taken from [this
repository](https://github.com/okfn/gutenizer/).

Otherwise the code in this repository has the following license:

    MIT License

    Copyright (c) 2017 Allison Parrish

    Permission is hereby granted, free of charge, to any person obtaining a copy
    of this software and associated documentation files (the "Software"), to deal
    in the Software without restriction, including without limitation the rights
    to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
    copies of the Software, and to permit persons to whom the Software is
    furnished to do so, subject to the following conditions:

    The above copyright notice and this permission notice shall be included in all
    copies or substantial portions of the Software.

    THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
    IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
    FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
    AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
    LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
    OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
    SOFTWARE.
