# nlp-corpora

UW NLP maintains a repository of corpora for internal UW use on the UW CSE
department fileserver at `/projects/nlp-corpora/`.

The main purpose of this document is to provide a live, browsable index of all
of the corpora. Below that are instructions for accessing the corpora and
proposing new additions.

## Live Status

Below is the live status of the corpora, updated daily.

dirname | desc | size | dir clean | README exists | README complete
--- | --- | --- | --- | --- | ---
prj-w-crap | None | 0B | ✗ | ✔ | ✔
empty-prj | None | 0B | ✔ | ✗ | ✗
prj-wo-readme | None | 0B | ✔ | ✗ | ✗
good-bare-prj | None | 0B | ✔ | ✔ | ✔
crapfile.crap | None | 0B | ✗ | ✗ | ✗
good-detailed-prj | This is a sample description. | 4.0K | ✔ | ✔ | ✔

### Legend

key | meaning
--- | ---
dirname | The name of the top-level corpus directory within `nlp-corpora`
desc | The description found in the README.md file for the corpus
size | The total size of the corpus directory
dir clean | Whether only the allowed directories and files were found
README exists | Whether the `README.md` file was found
README complete | Whether the `README.md` file contained descriptions for all subdirectories in `processed/`

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

Accessing the corpora requires a CSE unix account. UW members can receive UW
CSE guest accounts by having a UW CSE faculty or staff sponsor them at
https://sponsor.cs.washington.edu/. Despite the name "sponsor," this is
absolutely _free_. Guest accounts last up to two years and can be renewed
indefinitely.

Access outside UW is not possible.

## Bugs / questions / contributions

Please open a GitHub issue or pull request on this repository.

## Maintainers

- [Max Forbes](https://github.com/mbforbes)

