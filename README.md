# arxivprep

Script that prepares tarball of tex document in current directory tree for arXiv submission, stripping any tex comments.

## Usage

Run `arxivprep` in the top-level directory containing the tex document.

The behavior of the script can be modified by setting the value of shell variables the script respects, e.g. 

    $ TEXFILES=paper.tex arxivprep 

`arxivprep` respects the following shell variables:

- `TEXFILES`: tex files to include in tarball
- `BBLFILES`: bbl files to include in tarball
- `PKGFILES`: cls and sty files to include in tarball
- `FIGFILES`: figures to include in tarball (default: pdf, jp(e)g, png)
- `OUTFILE`: name of output tarball
- `TMPDIR`: base path to temporary directory
- `STRIPTEXCOMMENT`: commandline used to invoke striptexcomments script

## Dependencies

Requires Python and [ply.lex][1]:

    $ pip install ply.lex

## Acknowledgments

`striptexcomments` based on [`strip_comments.py` script by Adam Merberger][2]

`strip_comments.py` modifications that preserve comments in `\makeatletter` and `\makeatother` blocks by [dzhuan][3]

## License

    Copyright 2019 Thomas Nyman <thomas.nyman@iki.fi>

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.

[1]: http://www.dabeaz.com/ply/index.html "PLY (Python Lex-Yacc)"
[2]: https://gist.github.com/amerberg/a273ca1e579ab573b499 "Github: amerberg/strip_comments.py"
[3]: https://gist.github.com/dzhuang/dc34cdd7efa43e5ecc1dc981cc906c85 "Github: dzhuan/strip_comments.py"

