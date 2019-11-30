# Welcome to Joël's page!

![Ma bannière](https://i.imgur.com/I8IGDGc.png)

## Who am I?

My name is **Joël J. Présent** and I am currently a student at EPITA, graduate school of computer science.
You can take a look at my [LinkedIn profile][linkedin] if you want more info about my I.T. experience.

I am passionate of software development, especially in Rust, but also with C++, Java and TypeScript.
I have a few projects hosted here on GitHub and I am currently helping translating [the Rust book][rust-book-fr] from English to French.

## Some of my projects

I don't have much time to work on personal projects at the moment and I'm not allowed to publish my school projects on GitHub.
Nevertheless, you can take a look at some of the projects I carried out or will continue to work on in the future.

### Ongoing projects

#### Vojaq

[Vojaq][vojaq] is a language for data representation that supports two levels of nesting for each of its lines.
Each line can be divided into fields (every other field is placed between curly braces) and each field can be divided into variants (separated by the `|` character).

``` text
ありがとう {arigatou} thank you
馬鹿 {baka} idiot | stupid
洗い熊 | アライグマ {araiguma} raccoon {animal}
サントノーレ {santonôre} Saint-Honoré {pastry | cake} French
```

I have written the [vojaq_parser][vojaq] Rust crate to parse this language so that the values may be extracted and used.

``` rust
let my_vojaq = parse_vojaq("Je | 私 | I {t'aime | <3}").unwrap();
// 1st field's variants: "Je", "私", "I"
// 2nd field's variants: "t'aime", "<3"
```

This crate kinda works at the moment, but still needs more work in the future.

#### ZeDico

[ZeDico][zedico] is a Rust crate that aims to recreate a French sentence with correct inflection and conjugation when provided with French base words with some information attached.
For instance, with the words `moi`, `manger` (*present indicative*), `un(e)/des`, `banane` (*plural*), ZeDico could build the correct sentence *Je mange des bananes*.

ZeDico is still very early in development, but I will work on it in the future.
I know that it can work because I have already developed a similar program in the past.

### Small projects

#### Pseudolocalize

[Pseudolocalize][pseudolocalize] is a Rust crate that transforms strings for pseudolocalization.

```rust
let pl = Pseudolocalizer::new();
let s = pl.transform("The quick brown fox jumps over the lazy dog");
assert_eq!(s, "[!!! Ŧℏë ʠûíçķ ƃŕøẅñ ƒøẍ ĵûɱƥŝ øṽëŕ țℏë łάẓƴ ďøǧ !!!]");
```

#### Linoc

[Linoc][linoc] is a small Java program which changes the colors of an image.
You can display the resulting image and save it.

#### NombresFR

[NombresFR][nombresfr] is a small TypeScript program for writing numbers in French.

```javascript
>> NombresFR.toString(345697)
<< "trois-cent-quarante-cinq-mille-six-cent-quatre-vingt-dix-sept"
```

[linkedin]: https://www.linkedin.com/in/joeljpresent
[linoc]: https://github.com/joeljpresent/linoc
[nombresfr]: https://github.com/joeljpresent/NombresFR
[pseudolocalize]: https://github.com/joeljpresent/pseudolocalize
[rust-book-fr]: https://github.com/Jimskapt/rust-book-fr
[vojaq]: https://github.com/joeljpresent/vojaq_parser
[zedico]: https://github.com/joeljpresent/zedico
