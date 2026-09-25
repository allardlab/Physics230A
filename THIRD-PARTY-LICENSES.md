# Third-party licenses

Every page on this site is built with `embed-resources`, so it is one self-contained file: the stylesheets, the scripts and the typefaces are not fetched from anywhere, they are inlined into the page itself. That is deliberate --- a page opens with no network, and a student reading offline still sees its equations and its figures --- and it means each page *redistributes* the software and fonts below rather than merely linking to them. The published PDFs embed their typefaces for the same reason. Several of these licences require their notice to travel with the copy. This file is that notice.

The one exception is a slide deck that plays a movie. It is built *linked* rather than self-contained, so its copies of reveal.js, Quarto's scripts and the fonts below sit as ordinary files in a `<deck>_files/` folder beside it, and its movies in `media/`. Nothing is fetched from anywhere in that case either, and the copies are the same software under the same licences, so everything below applies to those folders exactly as it does to an inlined page.

It is generated material's companion, not a claim of ownership: nothing listed here belongs to the course. The course's own licence is in [LICENSE.md](LICENSE.md).

Everything below was read out of the built files rather than recalled --- the html by decoding each page's inlined `data:` URIs, the PDFs with `pdffonts`. Re-check it whenever the toolchain moves or the font set changes; `scripts/build_fonts.py` in the source repository says so at the point where that would happen.

## Fonts embedded in the html pages

**Source Sans 3** --- the body typeface, on three pages only: the landing page, the class outline and the html syllabus. Fifteen faces, weights 300, 400, 600 and 700 plus italic 400, in the latin, latin-ext and greek subsets. The nine problem sets and the lecture notebook are deliberately left on Quarto's default theme and carry none of it.

> Copyright 2010-2020 Adobe (http://www.adobe.com/), with Reserved Font Name 'Source'.
> All Rights Reserved. Source is a trademark of Adobe in the United States and/or other countries.
>
> This Font Software is licensed under the SIL Open Font License, Version 1.1.

**Nunito** --- the slide decks, in both the presentation and the linear reading page built from the same source. Ten faces, weights 400, 500, 600 and 700 plus italic 400, in the latin and latin-ext subsets. Nothing outside `slides/` uses it.

> Copyright 2014 The Nunito Project Authors (https://github.com/googlefonts/nunito)
>
> This Font Software is licensed under the SIL Open Font License, Version 1.1.

**Source Sans Pro** --- four faces, carried into each presentation by reveal.js's own default theme rather than chosen by this course. The decks are set in Nunito and do not use it, but it is inlined with the rest of the theme and so is redistributed all the same.

> Copyright 2010, 2012 Adobe Systems Incorporated (http://www.adobe.com/), with Reserved Font Name 'Source'.
> All Rights Reserved. Source is a trademark of Adobe Systems Incorporated in the United States and/or other countries.
>
> This Font Software is licensed under the SIL Open Font License, Version 1.1.

**Bootstrap Icons 1.13.1** --- one woff face, on *every* page. It draws the copy-to-clipboard button on each code block and the icons in the "Other Formats" sidebar, so it arrives with Quarto's html rather than with the theme.

> Copyright 2019-2024 The Bootstrap Authors. MIT License. https://icons.getbootstrap.com/

**anchorjs-icons** --- one TrueType face, on every page, carried by AnchorJS below. It draws the link glyph that appears beside a heading on hover, and is part of that package rather than a font chosen here.

> Copyright (c) 2023 Bryan Braun. MIT License. https://www.bryanbraun.com/anchorjs/

The full SIL Open Font License text is at <https://openfontlicense.org/open-font-license-official-text/>. Note the one restriction that matters in practice: a font under it may not be sold on its own, and may not be redistributed under a name containing a Reserved Font Name. Shipping one inside a web page, as here, is expressly permitted.

## Software bundled into the html pages

All of the following are MIT, which permits redistribution provided the copyright notice and permission notice are included --- which is what this file does. The full text of the MIT License is at <https://opensource.org/license/mit>.

- **reveal.js 5.1.0** --- the slide decks. Copyright (c) 2011-2024 Hakim El Hattab, https://hakim.se, and reveal.js contributors. <https://github.com/hakimel/reveal.js>
- **Bootstrap 5.3.1** --- Copyright 2011-2023 The Bootstrap Authors. <https://getbootstrap.com/>
- **@popperjs/core 2.11.7** --- <https://popper.js.org/>
- **Tippy.js** --- Copyright (c) 2017-present atomiks, as bundled by Quarto 1.9.38. <https://atomiks.github.io/tippyjs/>
- **AnchorJS 5.0.0** --- Copyright (c) 2023 Bryan Braun. <https://www.bryanbraun.com/anchorjs/>
- **clipboard.js 2.0.11** --- Copyright Zeno Rocha. <https://clipboardjs.com/>
- **Quarto 1.9.38** --- the site is rendered by Quarto, which inlines the components above into each page along with components of its own; reveal.js reaches the decks the same way. Quarto itself is MIT-licensed. <https://github.com/quarto-dev/quarto-cli>

**One absence is worth stating rather than leaving out.**

**MathJax is not redistributed here, and is not fetched either.** Every problem set, notebook, page and slide deck sets `html-math-method: mathml`, so its mathematics is rendered to MathML when the page is built.

The decks are where that needed care rather than a flat statement. Left to Quarto's default, a deck hands its mathematics to reveal.js's math *plugin*, which fetches MathJax from a CDN when the deck is opened. The decks now set MathML like everything else, so that plugin is not loaded: no deck's html contains the string "MathJax", and no deck contains a remote `src` of any kind. The plugin's own source files do still sit, unloaded, inside a linked deck's `<deck>_files/` folder, because Quarto copies reveal.js's plugin directory whole; they are part of reveal.js, above, and are not MathJax. Checked rather than assumed, in the build of 24 September 2026.

## Fonts embedded in the published PDFs

The PDFs are a separate question from the pages, and they answer it differently: nothing here is a web font, and none of the html set above appears in any of them.

**Latin Modern**, in the nine problem sets, the lecture notebook and the slide decks' printed beamer version --- LMRoman 6/8/9/10/12 in regular and italic, LMSans 10, LMMono 10, and **Latin Modern Math**. These are TeX's default typefaces, produced by GUST from the Computer Modern originals.

> Copyright the GUST e-foundation. Licensed under the GUST Font License, a free licence based on the LaTeX Project Public License. <https://www.gust.org.pl/projects/e-foundation/lm>

**TeX Gyre Heros**, in `syllabus.pdf` only --- regular, italic and bold, the sans face that document's own typography selects.

> Copyright the GUST e-foundation. GUST Font License. <https://www.gust.org.pl/projects/e-foundation/tex-gyre>

**Font Awesome 5 Free (Solid)**, in `syllabus.pdf` only, for the icons in its contact block.

> Copyright Fonticons, Inc. The fonts are under the SIL Open Font License 1.1 and the icons under CC BY 4.0. <https://fontawesome.com/license/free>

**DejaVu Sans**, in `python-test-drive.pdf` and in each deck's printed pdf --- matplotlib's default typeface, embedded in the figures those documents generate.

> Fonts are (c) Bitstream (see below). DejaVu changes are in public domain.
> Licensed under the DejaVu Fonts License, a permissive Bitstream Vera derivative. <https://dejavu-fonts.github.io/License.html>

**Arial**, in six of the seven figure PDFs and therefore in six of the nine problem set PDFs --- `PS1`, `PS2`, `PS3`, `PS4`, `PS5` and `PS7`.

Arial is a Monotype typeface and is not free software. It reaches these files because the figures were drawn in an application that used it for their labels, and it is embedded there as a **subset** --- the glyphs those labels actually use, not the font --- which is the ordinary and permitted way a document carries a typeface it was set in. It is named here because this file's job is to say what these files contain, and a notice that quietly listed only the open fonts would be the wrong kind of accurate.

Re-drawing those figures in an open face would remove it. That is recorded as an open item in the source repository's `DEVELOPMENT.md` rather than done here, because the figure PDFs are the single source of truth for the figures and re-authoring them is a piece of work in its own right.

## Material quoted inside the course

The problem sets cite published work, and some quote or reproduce material from it. That material belongs to its owners and appears as quotation for teaching. It is not covered by the course's licence and is not offered for reuse.

The slide decks do the same at larger scale: they reproduce figures and movies from published papers, each cited on the slide that shows it, along with photographs, an xkcd strip under its CC BY-NC 2.5 licence, and a historical film. The same terms apply to all of it. The NETosis deck's own experiments and movies are the Allard lab's, by Matt Bovyn.
