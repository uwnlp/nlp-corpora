# deepbank

Syntactic + semantic annotations on WSJ.

This is version 1.1 of the DeepBank corpus, which contains HPSG and
MRS syntactic and semantic annotations of sections 00 to 21 of the
Wall Street Journal corpus. These annotations are contained in binary
files constructed by the annotation software.

Original data:
http://svn.delph-in.net/erg/tags/1214/

Corpus website:
http://moin.delph-in.net/DeepBank

## dmrs

The `dmrs` corpus is a Dependency Minimal Recursion Semantics (DMRS)
annotation of the original DeepBank corpus (sections 00 to 21 of the
Wall Street Journal corpus).  The `dmrs` version is a processed
version of DeepBank 1.1, which corresponds to the 1214 version of the
English Resource Grammar (ERG).

This version has undergone multiple processing steps:

First the MRS semantic representation is extracted, using software
available in the LOGON software tree
(http://moin.delph-in.net/LogonTop).

Then MRS is then converted to DMRS using pyDelphin
(https://github.com/delph-in/pydelphin).

This version is a JSON formatted version of the DMRS data, and
additionally also include the tokenization and pre-processing output
folllowed by Buys and Blunsom 2017
(http://www.aclweb.org/anthology/P/P17/P17-1112.pdf), which enables
the data to be used to train a data-driven parser independent of the
ERG.

Preprocessing details, including scripts used, can be found at
https://github.com/janmbuys/DeepDeepParser.

Files:

`*.txt` - Untokenized input sentences, one sentence per line.

`*.tok.json` - Pre-processed version of the input. Each line is a
 JSON-formatted representation of a sentence, with the following
 structure:

```
id (int)
tokens [list of tuples]
  id (int)
  start (int)
  end (int)
  predicate_end (optional int)
  constant_end (optional int)
  properties [tuple]
    word (str)
    lemma (str)
    constant (optional str)
    POS (str)
    NE (optional str)
    erg_predicate (optional boolean)
```

`*.dmrs.json` - Original DMRS graphs: Node representations include
character spans, full predicates and constant strings. Each line is a
JSON-formatted representation of a graph, with the following
structure:

```
id (int)
nodes [list of tuples]
  id (int)
  start (int)
  end (int)
  properties [tuple]
    predicate (string)
    constant (optional string)
    type (string)
    top (optional boolean)
    features (optional string)
	edges [list of tuples]
    label (string)
    target (int)
```

`*.dmrs.tok.json` - Processed DMRS graphs for parsing: Node
representations include token spans (corresponding to the tokenized
input), predicates lemmas and constant strings are excluded. Features
and type information are not required for evaluation. Each line is a
JSON-formatted representation of a graph, with the following
structure:

```
id (int)
nodes [list of tuples]
  id (int)
  start (int)
  end (int)
  properties [tuple]
    predicate (string)
    type (string)
    top (optional boolean)
    abstract (optional boolean)
    features (optional string)
	edges [list of tuples]
    label (string)
    target (int)
```
