# README

This is a simple repo for a presentation I intend to share.

## Setup / pre-conditions

[Asciidoctor + deck.js integration](http://asciidoctor.org/docs/install-and-use-deckjs-backend/)
```shell
mkdir boxen-slides; cd boxen-slides
# set ruby version for this project
rbenv local 2.0.0-p247
# install required tools
gem install asciidoctor tilt haml
# get libraries (may want outside of current project)
git clone git://github.com/asciidoctor/asciidoctor-backends.git
git clone git://github.com/imakewebthings/deck.js.git
```

## Testing presentation

Basically, I edited `test.adoc` with code snippets from the integration link above.
Then, I ran:
```shell
asciidoctor -T asciidoctor-backends/haml test.adoc
open test.html
```

## "Building" the presentation

* edit `boxen-slides.adoc`
* `asciidoctor -T asciidoctor-backends/haml boxen-slides.adoc`
* open boxen-slides.html
