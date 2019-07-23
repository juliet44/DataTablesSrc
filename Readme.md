# DataTables plug-in for jQuery - source repository

This git repository contains the un-built source files for DataTables - the table enhancing plug-in for jQuery. If you are looking to use DataTables, rather than to modify it, please use the built files in the build repo: [//github.com/DataTables/DataTables](//github.com/DataTables/DataTables). There are instructions there on how to use DataTables, and on the [DataTables site](//datatables.net) which contains the full documentation for DataTables.


## Installing DataTables

To use DataTables, the primary way to obtain the software is to use the [DataTables downloader](//datatables.net/download). You can also include the individual files from the [DataTables CDN](//cdn.datatables.net). See the [documentation](//datatables.net/manual/installation) for full details.

### NPM and Bower

If you prefer to use a package manager such as NPM or Bower, distribution repositories are available with software built from this repository under the name `datatables.net`. Styling packages for Bootstrap, Foundation and other styling libraries are also available by adding a suffix to the package name.

Please see the DataTables [NPM](//datatables.net/download/npm) and [Bower](//datatables.net/download/bower) installation pages for further information. The [DataTables installation manual](//datatables.net/manual/installation) also has details on how to use package managers with DataTables.


## Why two repos

The source repo for DataTables is kept distinct from the built repo in order to provide separation between generated files and source files. The majority of the files in the DataTables built repo are generated by compiling source files from this repo, including:

* Main Javascript file - compiled from multiple individual Javascript files
* CSS files -compiled from SASS files
* Examples - compiled from a common data source data and HTML template files

This separation allows developers who simply want to use DataTables as is, to do so, while keeping the source repo clean of generated files.


## Building

DataTables can be built using the [`make.sh`](build/make.sh) script in the [`/build`](build) directory of this repo. Simply check out the repo, cd into the `build` folder and run `bash make.sh --help` to get a full list of the options available for the build process. `bash make.sh build` will be the most common (with `bash make.sh build debug` available for quick testing - it skips the minification steps for speed).

A number of programs are required out your computer to be able to build DataTables:

* Bash
* PHP 5.4+
* [Sass](http://sass-lang.com/install) - CSS compiler
* [Closure compiler](https://github.com/google/closure-compiler) - Javascript compressor
* [JSHint 2.1+](http://jshint.com/install/) - Linter (optional)

The build script assumes that a Mac or Linux environment is being used - Windows builds are not currently directly supported (although would be possible using [Cygwin](https://www.cygwin.com/)). Additionally, you may need to alter the paths for the above programs to reflect where they are installed on your own computer - this can be done in the [`build/include.sh`](build/include.sh) script.

The output files are placed into `built/DataTables/` which is a temporary directory. No changes should be made in that directory as they will be **overwritten** when you next build the software.


## Documentation

Full documentation of the DataTables options, API and plug-in interface are available on the [DataTables web-site](//datatables.net). The site also contains information on the wide variety of plug-ins that are available for DataTables, which can be used to enhance and customise your table even further.


## Support

Support for DataTables is available through the [DataTables forums](//datatables.net/forums) and [commercial support options](//datatables.net/support) are available.


## License

DataTables is release under the [MIT license](//datatables.net/license). You are free to use, modify and distribute this software, but all copyright information must remain.