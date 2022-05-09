Put the contents of the .platformio folder here. Then delete this file.

## !! ARM surumu icin Xcode Python3 kullaniliyor

## PlatformIO'yu tasinabilir hale getirmek icin;

1. penv/bin/ icindeki dosyalarin ilk satirindaki path'i duzenle
```
#!/bin/sh
"exec" "`dirname $0`/python" "$0" "$@"
```
See: https://stackoverflow.com/questions/20095351/shebang-use-interpreter-relative-to-the-script-path/33225909#33225909

2. penv/bin/activate dosyalarindaki VIRTUAL_ENV degiskenini ../ yap

```
VIRTUAL_ENV="../"
```

3. penv/bin/bottle.py icindeki 
```
from __future__ import with_statement
```
satirini en basa al