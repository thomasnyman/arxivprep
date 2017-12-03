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

`striptexcomments` based on [`strip_comments.py` script by dzhuan][2]

[1]: http://www.dabeaz.com/ply/index.html "PLY (Python Lex-Yacc)"
[2]: https://gist.github.com/dzhuang/dc34cdd7efa43e5ecc1dc981cc906c85 "Github: dzhuan/strip_comments.py"

