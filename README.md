# usage:
    - countlines -h
    - countlines [options] file
    - countlines -r[options] <extensions> directory

# options:
    - t: only print total
    - T: don't print total
    - n: sort by name
    - r: recursive search
    - f: print just file names
    - p: print full paths

# example usage:

## default options:

`countlines Desktop/java_files`

    /file_4.py:       2 lines
    /File1.java:      5 lines
    /File2.java:      49 lines
    /a_ruby_file.rb:  89 lines
    total:            145 lines
    
## restrict to java files

`countlines Desktop/java_files java`

    /File1.java:  5 lines
    /File2.java:  49 lines
    total:        54 lines

## recursive:

`countlines -r Desktop/java_files java`

    /File1.java:         5 lines
    /File2.java:         49 lines
    /file_3/File3.java:  99 lines
    total:               153 lines

## include python files:

`countlines -r Desktop/java_files java py`

    /file_4.py:          2 lines
    /File1.java:         5 lines
    /file_5/file_5.py:   33 lines
    /File2.java:         49 lines
    /file_3/File3.java:  99 lines
    total:               188 lines
