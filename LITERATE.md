# Literate code

Literate programming is a concept by Donald Knuth where code and documentation are one. Where contributors are recognized not just as writers of code, but readers of it as well. For a great, welcoming intro to the idea, [here's a post](https://web.archive.org/web/20130531033055/http://ashkenas.com/literate-coffeescript/) on it by Jeremy Ashkenas.

## Press

Press is a simpler style of writing literate code inspired by [Literate CoffeeScript](http://coffeescript.org/#literate).

Traditionally, literate programming tools intertwine (or *tangle and weave*) different output source files in a single or multiple literate input source file, and output separate viewable annotated web pages from the source. Press (and other tools like lit & Literate CoffeeScript) keep things a lot simpler, simply stripping prose from annotated source.

## Literate programming & documentation

Literate programming is definitely documentation of a form, but is ultimately more like annotated source code. A project with a public API would still want to offer standard documentation, whereas literate source is more for easing development for contributors to a project, and for those needing to understand a project's inner workings.

## Excellent other literate projects

There's a few other amazing literate projects out there that work differently from Press in one way or another, so if Press isn't quite right for you, check them out:

- [Docco](https://github.com/jashkenas/docco): generates separate docs from literate code
- [lit](https://github.com/vijithassar/lit): strips prose from literate code (like Press!)
- [Blaze](https://github.com/0atman/blaze): hashbang execution for literate code
- [literate-programming](https://github.com/jostylr/literate-programming): powerful literate programming
- [Literate](https://github.com/zyedidia/Literate): really powerful literate programming
- [love-notes](https://github.com/ada-lovecraft/love-notes): literate programming the way Donald Knuth himself would do it
