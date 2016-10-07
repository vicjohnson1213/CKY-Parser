# CKY Chart Parser

> A syntactic parser using the CKY chart parsing algorithm.

## Usage

The parser takes two files as input, the first containing grammar rules for the language, and the second containing all sentences that should be tested.

```bash
python parser.py grammar.txt sentences.txt
```

### The Grammar File

The grammar file should consist of newline separated rules in Chomsky Normal Form.

*Example Grammar File:*

```text
S -> ART NP
S -> ART X
X -> ADJ X
X -> ADJ NP
NP -> ADJ NOUN
ART -> the
ADJ -> beautiful
ADJ -> tropical
NOUN -> fish
```

### The Sentences File

The sentences file is simply a newline separated list of sentences to test against the grammar.

*Example Grammar File:*

```text
the fish
the tropical fish
the beautiful tropical fish
```

### The Ouput

TODO: Make the output of the program show the successful parses of each sentence rather than the contents of the table.

## License

MIT

Copyright (c) 2016 Victor Johnson victor@victorjohnson.io

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.