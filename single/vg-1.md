# vg-1 - File header format

## Table of Contents

* [Purpose](#purpose)
* [Format specification](#format-specification)
  * [Format 1](#format-1-vg-1f1)
  * [Format 2](#format-2-vg-1f2)
  * [Format 3](#format-3-vg-1f3)
  * [Format 4](#format-4-vg-1f4)
  * [Format 5](#format-5-vg-1f5)
  * [Format 6](#format-6-vg-1f6)
  * [Format 7](#format-7-vg-1f7)
* [Notes](#notes)
* [Example](#example)

## Purpose

This document defines the required format for file header comments all source
files. The header provides essential information and metadata about source
files.

## Format specification

Every source file must begin with the following block, using the exact
formatting and alignment:

### Format 1 (vg-1.f1)

```c
/*==============================================================================
 * File:        <filename.ext>
 * Path:        <relative/path/>
 * Purpose:     <brief explanation of file's function>
 * 
 * Author:      <full name or alias>
 * Created:     <YYYY-MM-DD>
 * License:     <license type>
 * Copyright:   (c) <year> <author or organization>
 *============================================================================*/
```

> For languages using `/* */` for comments.

### Format 2 (vg-1.f2)

```bash
# ==============================================================================
# File:        <filename.ext>
# Path:        <relative/path/>
# Purpose:     <brief explanation of file's function>
#
# Author:      <full name or alias>
# Created:     <YYYY-MM-DD>
# License:     <license type>
# Copyright:   (c) <year> <author or organization>
# ==============================================================================
```

> For languages using `#` for comments.

### Format 3 (vg-1.f3)

```java
//==============================================================================
// File:        <filename.ext>
// Path:        <relative/path/>
// Purpose:     <brief explanation of file's function>
//
// Author:      <full name or alias>
// Created:     <YYYY-MM-DD>
// License:     <license type>
// Copyright:   (c) <year> <author or organization>
//==============================================================================
```

> For languages using `//` for comments.

### Format 4 (vg-1.f4)

```lua
--==============================================================================
-- File:        <filename.ext>
-- Path:        <relative/path/>
-- Purpose:     <brief explanation of file's function>
-- 
-- Author:      <full name or alias>
-- Created:     <YYYY-MM-DD>
-- License:     <license type>
-- Copyright:   (c) <year> <author or organization>
--==============================================================================
```

> For languages using `--` for comments.

### Format 5 (vg-1.f5)

```vba
' ==============================================================================
' File:        <filename.ext>
' Path:        <relative/path/>
' Purpose:     <brief explanation of file's function>
' 
' Author:      <full name or alias>
' Created:     <YYYY-MM-DD>
' License:     <license type>
' Copyright:   (c) <year> <author or organization>
' ==============================================================================
```

> For languages using `'` for comments.

### Format 6 (vg-1.f6)

```latex
% ==============================================================================
% File:        <filename.ext>
% Path:        <relative/path/>
% Purpose:     <brief explanation of file's function>
%
% Author:      <full name or alias>
% Created:     <YYYY-MM-DD>
% License:     <license type>
% Copyright:   (c) <year> <author or organization>
% ==============================================================================
```

> For languages using `%` for comments.

### Format 7 (vg-1.f7)

```python
"""=============================================================================
   File:        <filename.ext>
   Path:        <relative/path/>
   Purpose:     <brief explanation of file's function>

   Author:      <full name or alias>
   Created:     <YYYY-MM-DD>
   License:     <license type>
   Copyright:   (c) <year> <author or organization>
  ==========================================================================="""
```

> For languages using `"""` for comments.

## Notes

* No extra or missing fields unless version-controlled
* All `<...>` fields must be filled out or marked `N/A` if not applicable.
* This format must appear at the top of all .cpp, .h, .py, .js, etc., files.
* Auto-generated files do *not* require this header format, although including it
  is recommended.
* SPDX license identifiers shall be used in the `License:` section.
* `<relative/path>` should be replaced by the repository or project root.

## Example

```c
/*==============================================================================
 * File:        main.cpp
 * Path:        src/
 * Purpose:     Entry point to the program
 * 
 * Author:      Sven Specimen
 * Created:     2000-01-01
 * License:     Unlicense
 * Copyright:   (c) 2000 Sven Specimen
 *============================================================================*/
```
