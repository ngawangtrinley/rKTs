# rKTs

These files are the database of the [resources for Kangyur and Tengyur studies project](https://www.istb.univie.ac.at/kanjur/rktsneu/sub/index.php) based in Vienna.

### Tags

#### Editions

The tags used in the xml files of the `Kanjur/`, `Tanjur/` and `Tantra/` folder are:

- `<rkts>` (resp. `rktst`, `rktsg`), indicating that the text is a manifestation / expression of a text in the Kernel. For instance `<rkts>1</rkts>` in `Kanjur/derge.xml` indicates that the text in the Derge edition is a manifestation of the text with ID `1` in the Kernel file
- `<ref>` indicates the reference number of the text in the edition. It is unique and prefixed by one or several letter corresponding to the sigla of the edition (see [list of siglas](https://www.istb.univie.ac.at/kanjur/rktsneu/sigla/)). When catalogs of the edition are available, they are used as the source of these reference numbers.
- `<loc>` indicates the location of the text in the edition. Its format varies a bit from file to file (TBD)
- `<tib>` is the Tibetan title indicated in the incipit of the text in the edition, transliterated in EWTS
- `<skttrans>` idem with the Sanskrit title
- `<zhtrans>` idem with the Chinese title
- `<coloph>` is the entire colophon of the text in the edition, transliterated in EWTS
- `<coltitle>` is the title of the text as indicated in the colophon
- `<author>` is the name of the author as appearing in the colophon of the edition (can appear multiple times)
- `<translator>` idem with the translator
- `<translator2>` idem with the translator of the second translation
- `<revisor>` idem with the person involved in the first revision
- `<revisor2>` idem with the person involved in the second revision
- `<revisor3>` idem with the person involved in the third revision
- `<translationplace>` the place where the translation occured according to the colophon of the edition
- `<revisionplace>` the place where the translation occured according to the colophon of the edition
- `<note>` a note, in English

#### Kernel

TODO

### File format

Some indications on the xml format:
- UTF8 with no BOM
- LF for new lines
- format with `cat rkts.xml | xmllint --format - | sed -e 's/^[ ]*//;s/<item>/\n<item>/' | sponge rkts.xml`

### License

The data is under the [CC0 License](https://creativecommons.org/publicdomain/zero/1.0/). If you use these files we ask you to provide a reference to this github repository and to the rKTs project.
