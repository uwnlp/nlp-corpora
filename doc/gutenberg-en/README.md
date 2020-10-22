# Gutenberg English

All English books from Project Gutenberg

Downloaded November 17, 2016.

Only ASCII-encoded versions of files were kept. The full process of
acquiring the data is described here:
https://gist.github.com/mbforbes/cee3fd5bb3a797b059524fe8c8ccdc2b

## processed

### tkn

This contains the results of nltk tokenization run on the entire
corpus. 

https://www.nltk.org/api/nltk.tokenize.html

Editor's note: since this was done, spacy has been released and has a
better tokenizer. A more complete tokenization pipeline would:

- run [Unidecode](https://pypi.org/project/Unidecode/)

- standardize quotes (`\`` -> `'`) and collapse psueudo-double quotes
  (`''` -> `"`).

- run spacy tokenization

If you are reading this and feel like undertaking it, that would be an
improvement over the current tokenized version.
