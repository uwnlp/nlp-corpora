# nlp-corpora

UW NLP maintains a repository of corpora for internal UW use on the UW CSE
department fileserver at `/projects/nlp-corpora/`.

The main purpose of this document is to provide a live, browsable index of all
of the corpora. Below that are instructions for accessing the corpora and
proposing new additions.

## Live Status

Below is the live status of the corpora, updated daily
([legend](https://github.com/mbforbes/nlp-corpora-backend#legend)).

dirname | desc | size | dir clean | README exists | README complete
--- | --- | --- | --- | --- | ---
gutenberg-en | English Gutenberg. | 106G | ✔ | ✔ | ✗
nyt-annotated | The New York Times Annotated Corpus | 3.1G | ✔ | ✔ | ✔
fanfiction | This is a corpus of 1.25 billion lines of fan fiction text. | 164G | ✔ | ✔ | ✗
gigaword-en-5 | English Gigaword Fifth Edition | 9.2G | ✔ | ✔ | ✔
byu-coca | https://corpus.byu.edu/coca/ | 6.0G | ✔ | ✔ | ✔
byu-coha | https://corpus.byu.edu/coha/ | 4.4G | ✔ | ✔ | ✔
google-syntax-ngrams | English Google Syntax Ngrams (v20120701) | 319G | ✔ | ✔ | ✔
penn-treebank-revised | English News Text Treebank: Penn Treebank Revised | 16M | ✔ | ✔ | ✔
google-surface-ngrams | Google surface ngrams (web 1T 5-gram v1) | 25G | ✔ | ✔ | ✔
byu-now | https://corpus.byu.edu/now/ | 85G | ✔ | ✔ | ✔
roc-stories | ROCStories Corpus. | 27M | ✔ | ✔ | ✔
deepbank | This is version 1.1 of the DeepBank corpus contains HPSG and MRS | 665M | ✔ | ✔ | ✔
toronto-books | The Toronto Books corpus. | 8.8G | ✔ | ✔ | ✔

## Using the corpora

Accessing the nlp-corpora requires UW CSE department server access (e.g., to
the machines `{recycle,bicycle,tricycle}@cs.washington.edu`) so that they can
view the department filesystem. The nlp-corpora directory is located on the
department filesystem at `/projects/nlp-corpora/`. Anyone with a UW CSE account
can log onto the department servers and view the files there. (For those
without a UW CSE account, see the section below.)

The corpora are meant to be read-only so that they stay in a known, clean
state. To work with files from the corpora, please copy them to a local
directory, e.g., with `scp`.

## Corpus structure

One of the goals of this project is to have a consistent directory structure
across all of the corpora we track to give a smooth experience browsing through
them. Here is a [detailed description of this
structure](https://github.com/mbforbes/nlp-corpora-backend#documentation).

## Adding a new corpus

Fill out this
[form](https://docs.google.com/forms/d/1SBPXlJ8zsE1kbVr6csE3d9XIaW9pCfvOkmH9kD6vEv8/viewform)
and we will work with you to add a new corpus to the repository.

## Restricted access

Some corpora require signing a form and sending it to the authoring institution
to be cleared for access. To honor these requests, we restrict access to
corpora for which this is required by narrowing the unix group that has read
privileges.

Instructions for streamlining this process are coming soon. In the mean time,
please open a github issue to request access to a restricted corpus.

## Access outside UW CSE

Accessing the corpora requires a UW CSE unix account. UW members can receive a
free UW CSE guest account by having a UW CSE faculty or staff [sponsor
them](https://sponsor.cs.washington.edu/). Despite the name "sponsor," this is
absolutely _free_ for both parties. Guest accounts last up to two years and can
pbe renewed indefinitely.

Access outside UW is not possible.

## Bugs / questions / contributions

For any bugs or questions, please open a GitHub issue on this repository (top
of the webpage).

To help contribute to this project, please check out the [backend
repository](https://github.com/mbforbes/nlp-corpora-backend) and open issues or
pull requests there.

## Maintainers

- [Max Forbes](https://github.com/mbforbes)

