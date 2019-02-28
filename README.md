# utf8.carp

A simple UTF-8 package for Carp. This nascent string replacement type allows
you to use many of the functions you know from Carp strings while respecting
unicode runes instead of just having bytes.

The full documentation lives [here](https://veitheller.de/utf8/).

## Installation

You can obtain this library like so:

```clojure
(load "git@github.com:carpentry-org/utf8.carp@0.0.1")
```

## Usage

First, let’s define a UTF-8 string to work with!

```clojure
(let [s (UTF8.from-string "hεllö")]
```

That’s a cute, short string! Hm, I wonder how long it is!

```clojure
(length s) ; => 5
```

That’s surprising! So the length is the actual number of runes, and not the
number of bytes, you say? Most curious!

You know what, I want to see this second character there up close! It somehow
looks all Greek to me!

```clojure
(nth s 1) ; => ε
```

Hm, so this is what that looks like, huh? Interesting. And what’s its type?

```clojure
(type UTF8.nth) ; => UTF8.nth : (λ [(Ref UTF8), Int] Rune)
```

So, it’s called a `Rune`, huh? Hm, they don’t seem to be super interesting, but
I seem to be able to compare them and stringify them, and even take their length
in bytes! Quite delicious!

I wonder what else I can do with these functions?

<hr/>

Have fun!
