# Formatting and Style Guide for Concept Exercise Files

This document records the current styleguide applicable to Concept exercise Markdown files, which refer to the files contained in `.docs` and `.meta`. Please follow them when implementing a Concept Exercise; maintainers should also reference the Style Guide when reviewing pull requests. When the relevant language also includes a style guide, those preferences will take precedence over the ones here.

## Headers

 - Use level 2 headers, e.g. `##`
 - Do not use top-level headers, e.g. `#`
 - Do not use leading whitespace in the file.


## Empty Documents

If a document is empty, i.e. there is no `after.md` content, then do not check one in.


## Links

Exercism prefers "indirect reference" links. They are defined at the bottom of the Markdown file and mapped to a reference slug, and referenced by that slug in the text.

This makes maintenance easier, since the link must only be updated once.

Example:

```
I have a paragraph of text that links to the same page twice. 

The [first link][indirect-reference] in one sentence. 

Then, another sentence with the [link repeated][indirect-reference].

[indirect-reference]: https://example.com/link-to-page
```

Links should be inline where possible, i.e. as `<a href="">text</a>` tags instead of bare URLs. This is accomplished using the Markdown bracketed notation, as exemplified above.


## Code

Where possible and relevant, format code first as if it was being typed into a terminal, or if not applicable to your language, as if in a code file itself. Please reference the docs for your language, as they may have more information.

For example, Python has the REPL (read-eval-print loop), which allows a programmer to type code directly into a terminal, so we prefer formatting example code as if it was being typed into the REPL, with a leading `>>>`:

```
>>> extract_message("[INFO] Logline message")
```


## Language Code Style

Please consult each language's docs folder for more information on the preferred style conventions for that language.


## Miscellaneous

 - Use dashed-style UUIDs in `config.json` files. e.g. `1234-5678-8901`