## Log format description files for lnav

[lnav](https://lnav.org) is a powerful log file reader, designed to take
multiple log files and order them by date.  It understands log file formats
using regular expresions and can highlight sections of line, find errors
and warnings, and more.

This repository is for the log file format descriptions I've written so far.

You can install these using `lnav -i formatfile.json` or by putting them
in your `~/.lnav/formats/installed` directory.

# Easy creation of formats

I now provide a new tool, `make_format.pl`, which takes a series of lines from
stdin and turns them into sample lines in a new format.  This can, for
instance, be used by marking several significant lines in lnav and issuing the
command:

`:pipe-to perl path/to/make_format.pl -name example -output example_log.json`

Using the `-name` or `-n` option sets the name in the format.  This is lazy,
so you'll need to edit it to suit yourself.  If this option is not specified
the format name is 'NEW' throughout.

Using the `-output` or `-o` option sets the destination for the new format.
If this is not specified the result will be written to standard output.
