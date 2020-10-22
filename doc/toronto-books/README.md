# toronto-books

The Toronto BookCorpus, a large collection of books

## Usage notice

The following notice is provided to users who have been granted access
by Toronto researchers:

```
**************** instructions for BookCorpus ****************
The book corpus data can be downloaded in the following format:

The full set of books in text format, one file per book:
http://www.cs.toronto.edu/~mbweb/data/books_txt_full.tar All sentences
from the full set of books (the format used in training our
skipthoughts model):
http://www.cs.toronto.edu/~mbweb/data/books_in_sentences.tar
```

## Corpus details

The corpus was downloaded November 7, 2017.

Detailed information on the corpus is available here:

http://yknzhu.wixsite.com/mbweb

Access to this corpus was previously restricted, but it's no longer
available from the original source. Thus, we treat our internal copy
as read only and generally available within UW.

Citation:

```bibtex
@inproceedings{moviebook,
title = {Aligning Books and Movies: Towards Story-like Visual Explanations by Watching Movies and Reading Books},
author = {Yukun Zhu and Ryan Kiros and Richard Zemel and Ruslan Salakhutdinov and Raquel Urtasun and Antonio Torralba and Sanja Fidler},
booktitle = {arXiv preprint arXiv:1506.06724},
year = {2015}
}
```

## processed

### txt

This is the entire books corpus as one text file with the following
additional preprocessing applied:

- all empty lines removed
- all lines with < 2 alphabetic characters removed
- all lines with no lowercase characters removed
- all lines with "http" anywhere in them removed
