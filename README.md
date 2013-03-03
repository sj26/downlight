# Downlight Editor

This is a syntax-aware text editor for [markdown](http://daringfireball.net/projects/markdown).

## Aim

Create a performant text editor which syntax highlights as you type.

Textareas are great, but people foreign to markdown can find the syntax a little daunting at first. Syntax highlighting provides just enough context to make learning and using markdown much easier, especially for non–technical users.

We also want to emit efficient edit operations compatible with collaborative editing frameworks like sharejs. This is easily achievable

## Structure

Downlight replaces a textarea with a contenteditable div. All editing functionality of the div is intercepted to ensure only plain text can be entered. Text is entered as single character spans. The final value is the textContent of the div.

Markdown syntax is lexed from the textContent into an AST which will be partially transformed as edits are made. The AST is used to attribute the text content using CSS classes on the spans.

## License

Copyright (c) 2013 Samuel Cochran (sj26@sj26.com). Released under the MIT License, see LICENSE for details.
