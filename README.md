# Yardstick image test suite metadata

This is a list of image metadata for the test suite.

The files follow naming pattern `XX/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX.json` where `X`s are lowercase hex digits of SHA-1 of the image file being described. The first two digits are used for subdirectory name.

## Schema

The JSON contains fields:

* `sha1` — SHA-1 hash of the file being described (lowercase hex, required).
* `created` — Unix timestamp when the image was added to the test suite.
* `updated` — Unix timestamp when the metadata was last updated.
* `lic` — License (required). See `licenses.json`. One of:
    * `pd` — Public Domain
    * `cc0` — Creative Commons Zero
    * `cc-by-2.5`, `cc-by-3.0` — Creative Commons Attribution
    * `cc-by-sa-2.5`, `cc-by-sa-3.0` — Creative Commons Attribution + Share Alike
* `url` — URL where the image has been downloaded from.
* `urls` — Array of alternative locations where this image may be downloaded from.
* `from` — Identifier/name of source where this image was obtained from (see `sources.json`)
* `tags` — Array of arbitrary tags that describe content of this image. Tags with `:` are reserved for special purposes.
* `desc` — Object with keys for image description (including attribution) in one or more formats:
    * `text` — Plain text (with newlines)
    * `html` — HTML-formatted
    * `url` — URL to the description
* `name` — Short name/title of the image. Generally derived from filename.

## Downloading image files

[Yardstick.pictures website](https://yardstick.pictures/) provides bulk downloads. Please use the bulk downloads instead of hitting individual image URLs.
