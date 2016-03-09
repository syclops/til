# Error: Missing fonts CMSY10, CMMI10, etc.

When loading documents with certain LaTeX fonts in Adobe programs (Illustrator
in my case), the application may complain about missing fonts with names like
CMSY10 or CMMI10. To fix this, make the fonts available to Adobe applications as
follows (on a Mac):


```
BASE = /usr/local/texlibe/2015/texmf-dist/fonts/type1/public/amsfonts/cm
TARGET = ~/Library/Application\ Support/Adobe/Fonts
for f in $(ls -d $BASE/*); do
  ln -s $f $TARGET
done
```
