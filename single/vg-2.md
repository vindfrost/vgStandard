# vg-2 - Developer signature

## Table of Contents

* [Purpose](#purpose)
* [Format specification](#format-specification)
  * [Format 1](#format-1-vg-2f1)
  * [Format 2](#format-2-vg-2f2)
  * [Format 3](#format-3-vg-2f3)
  * [Format 4](#format-4-vg-2f4)
* [Notes](#notes)
* [Example](#example)

## Purpose

This document defines the format used for digital development signatures.

## Format specification

Every digital developer signature shall be in this format:

### Format 1 (vg-2.f1)

```markdown
*--*
*<username>*
```

> For people only having one username.

### Format 2 (vg-2.f2)

```markdown
*--*
*<username>/<real_name>*
```

> For people wanting to use their username and their real name.

### Format 3 (vg-2.f3)

```text
--
<username>
```

> Used when no markdown-like syntax is supported.

### Format 4 (vg-2.f4)

```text
--
<username>/<real_name>
```

> Used when no markdown-like syntax is supported and the person wants to use
  both their username and real name.

## Notes

* The `<username>` field shall be replaced with the username.
* The `<real_name>` field shall be replaced with the real name of the person.
* Choose between markdown (formats 1 and 2) and plain text (formats 3 and 4)
  based on the medium's support.

## Example

```markdown
*--*
*jumpingmonkey/Smithman*
```
