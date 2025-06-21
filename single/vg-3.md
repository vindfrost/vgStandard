# vg-3 - Pull/Merge-request template

* [Purpose](#purpose)
* [Format specification](#format-specification)
* [Notes](#notes)
* [Example](#example)

## Purpose

This document defines the required format for pull-requests, merge-requests and
similar.

## Format specification

All pull-requests, merge-requests and similar shall follow this format:

Title: `<Title>`

Content of requests:

```markdown
# <TITLE>

## Added

* <Changes>

## Changed

* <Changes>

## Fixed

* <Changes>

## Removed

* <Changes>

-----

<description>

-----

#### Additions: +<xx>
#### Deletions: -<xx>

*--*
<*signature*>
```

## Notes

* The signature must always be in the [vg-2](vg-2.md) format.
* All fields are mandatory unless explicitly stated otherwise or there is
  nothing to be filled in.
* Ensure accurate `+xx` and `-xx` counts based on the diff.
* Avoid nonstandard headings or stylistic deviations.
* Use standard Markdown headings (`# Heading`), without trailing hashes
  (i.e., `# Heading #` is not allowed)
* The `<Title>` section shall be replaced by the title of the request.
* The `<TITLE>` section shall be replaced by the title of the request in all
  uppercase.
* The `<Changes>` sections shall be replaced by the changes in bullet-point
  format.
* The `<signature>` section shall be replaced by the already mentioned vg-2
  signature.

## Example

Title: `Update to new version: 0.2.5`

```markdown
# UPDATE TO NEW VERSION: 0.2.5

## Added

* Added communication via chat

## Changed

* Changed input delay from 1ms to 3ms

## Fixed

* UTF-16 letters are now being correctly displayed

## Removed

* Removed flying feature

-----

This version adds chatting and changes the input delay. It would enhance the
overall UX and change core features. Updating the version number from
0.2.4 -> 0.2.5

-----

#### Additions: +28
#### Deletions: -1238

*--*
*shndrit*
```
