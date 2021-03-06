# DEPRECATION NOTICE

This module is deprecated. Use [lua-ext](https://github.com/RisingWorld/lua-ext) instead.

---

# String-Ext SubModule

This module adds some utility functions to the `string` namespace


## Installation

This script is not standalone and must be used with your own script, as it doesn't have a `definition.xml` file.


### Direct installation (not recommended)

You only need to copy the file `string-ext.lua` to your script's directory. Whenever the file needs updating, this manual step must be done. This is a non-desirable method as, if commited, it will create duplicate versions of this file across different repositories.


### Using as a Git Sub-Module (recommended)

At the script base folder, execute the two commands

```
$ git submodule add https://github.com/RisingWorld/string-ext
$ git commit -am 'Added string-ext sub-module'
```

This will create a directory called `string-ext`, and clone this repository in it. However, the content of the directory will not be commited with the rest of your project, only the directory entry and a file called `.gitmodules` 

Whenever the project needs updating, perform this command, also at the script's base folder :

```
$ git submodule update --remote string-ext
```

Refer to the [official Git documentation](http://www.git-scm.com/book/en/v2/Git-Tools-Submodules) for more information.


## Usage

Just include the script `string-ext.lua`. The file should *not* be included twice. Once included, the extended features will be available globally.


## API Reference

* `string.trim(str)`
  Trim the given string from spaces.

* `string.ltrim(str)`
  Left trim the given string from spaces.

* `string.rtrim(str)`
  Right trim the given string from spaces.

* `string.wrap(str, limit[, indent])`  
  Wrap the given `str` at about `limit` characters per line with an optional `indent`ation of spaces in front of each subsequent lines. The returned value is an array of lines (with no trailing spaces).

  ```
  str = "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Curabitur non urna lectus. Nunc ornare pharetra egestas. In gravida neque mi.";
  string.wrap(str, 50);   
  --> {
        "Lorem ipsum dolor sit amet, consectetur adipiscing",
        "elit. Curabitur non urna lectus. Nunc ornare",
        "pharetra egestas. In gravida neque mi."
      }
  ```


## License

Copyright (c) 2015 Yanick Rochon

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
