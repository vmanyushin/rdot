# RDot — GraphViz diagrams for Ruby classes

## Usage
    rdot [options] <libs>

### Service options
        -h, --help                       Show short help and exit.
        -?, --usage                      Show usage info and exit.
        -B, --about                      Show about string and exit.
        -A, --author                     Show author and contact info and exit.
        -L, --license                    Show info about license and exit.
        -V, --version                    Show version number and exit.
        -I, --info=[info]                Show some information and exit.
                                         Argument may be comma-separated set of:
                                           about, author, license, usage, version;
                                         or one of presets:
                                           help = about + usage,
                                           info (or no argument) =
                                                        about + author + license,
                                           all = about + author + license + usage.

        -o, --output=[file]              File for output instead STDOUT.
                                           'rdot.dot' if empty.
            --stdout                     Reset output to STDOUT.

### Data options
        -p, --preload=libs               Comma-separated list of preloading
                                           libraries which must be hidden.
        -i, --load, --input=libs         Comma-separated list of libraries
                                           which must be loaded and visualized.
        -l, --libs, --search-path=paths  Comma-separated list of paths where search
                                           for libs by load and preload.

        -e, --[no-]exclude-classes=list  Comma-separated list of classes which
                                           should be ignored with their descendants.
        -xlist,                          Comma-separated list of modules which
            --[no-]exclude-namespaces      should be ignored with their namespace.
                                         RDot, Gem, Errno & OptionParser by default,
                                           use '--no-exclude-namespaces' to reset.
            --[no-]exclude-files=list    Comma-separated list of files & wildcards
                                           their methods should by ingnored.
                                         Currect RDot location excluding by default,
                                           use '--no-exclude-files' to reset.
        -c, --[no-]filter-classes=list   Comma separated list of classes which only
                                           should be visualized (with descendants).
        -nlist,                          Comma-separated list of modules which only
            --[no-]filter-namespaces       should be visualized (with nested).
            --[no-]filter-global         Filter classes and modules only in global
                                           namespace.
            --[no-]filter-files=list     Comma-separated list of files & wildcards
                                           their methods only should by processed.

### Diagram options
    -C, --[no-]hide-constants        Ignore constants in classes & modules.
    -M, --[no-]hide-methods          Ignore methods & attributes.
    -G, --[no-]hide-arguments        Don't show methods' arguments.
    -X, --[no-]hide-included         Don't show 'include' links.
    -E, --[no-]hide-extended         Don't show 'extend' links.
    -N, --[no-]hide-nested           Don't show nesting links

    -S, --[no-]show-private          Show private & protected methods.
    -s, --[no-]show-protected        Show protected methods.
    -P, --[no-]show-preloaded        Show preloaded classes & modules.

        --[no-]select-attributes     Show attributes with access rights
                                       instead getters & setters as methods.
                                     True by default.

### Graphic options
    -T, --title=title                Graph title.
                                       'RDot Graph' by default.

        --title-font=name            Font name for the graph title.
                                       'sans-serif' by default.
        --title-size=size            Font size for the graph title (pt).
                                       24 by default.
        --font=name                  Font name for main text.
                                       'monospace' by default.
        --font-size=size             Font size for main text (pt).
                                       9 by default.

        --color-class=color          Background color of class title.
                                       #BBFFBB by default.
                                     RGB value or name from X11 scheme (see
                                       http://graphviz.org/content/color-names).
        --color-class-preloaded=color
                                     Background color of preloaded class title.
                                       #CCEECC by default.
        --color-class-core=core      Background color of core class title.
                                       #DDFF99 by default.
