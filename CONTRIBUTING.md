# Contributing

Corrections, clearer explanations, and fixes to the code samples are all welcome.

If the change is small, a typo, a broken link, a wrong number, just open a pull request. If it is larger, a reworked explanation, a new section, a change to how a chapter is structured, open an issue first so we can agree on the approach before you spend time writing it. When you report a problem, say which chapter file it is in, which section heading, and what is wrong or unclear.

## Keep English and Persian together

Every chapter holds both languages in the same HTML file, switched by the toggle in the header through `.en` and `.fa` spans.

If you change one language, change the other in the same pull request. A pull request that only touches the English or only the Persian side of a passage will be asked to add the missing side before it can be merged. If you are not comfortable writing the Persian, say so in the pull request and mark the untranslated part clearly so a maintainer or another contributor can finish it.

## Style

The book is plain, self-contained HTML with no build step, no framework, and no new dependencies. Keep it that way. Images stay embedded as `data:` URIs, and the only things a chapter should load from the network are the fonts and the KaTeX stylesheet that are already there.

Keep new or replaced images small. Export plots at a modest size, and save screenshots as JPEG rather than PNG when there is no transparency to keep. Match the tone of the text around your edit: define a term where it first appears, and add it to that chapter's glossary.
