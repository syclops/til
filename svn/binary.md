# Force a file to be considered binary

Certain file types, such as PDFs, should be considered binary in SVN. Sometimes,
when you add a PDF in SVN, it doesn't get marked as binary. To fix that, run

```
svn propset svn:mime-type application/octet-stream <filename>
```
