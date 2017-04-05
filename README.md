# ftopindexmaker
A top-level index maker for [fgallery](https://www.thregr.org/~wavexx/software/fgallery/) [(github)](https://github.com/wavexx/fgallery) written in dotnet core

#### TLDR: Put several fgallery-created folders into one folder. Run this program and point it at that folder. You now have a top level gallery-of-albums!

## Usage

`./ftopindexmaker /path/to/folder/containing/albums`

Following this, you should simply find TWO files: index.html and style.css. These two files contain all the information necessary to allow the page to work.

## Additional Options

#### -preserveunderscores
  *By default, the program replaces underscores with spaces in album titles derived from folder names. Use this flag to preserve the underscores.*

#### -preserveindex
  *By default, the program generates relative links to individual albums by folder name only - it does not include index.html in the links. This assumes you're going to be hosting the files on a server where index.html is not required (nginx, apache, etc). Use this flag to force the inclusion of "/index.html" at the end of album links.*

#### -title {TITLE}
  *Use this flag to specify a custom page title for your top-level index.*

## Download

If you don't want to download the code and compile yourself, I have provided a pre-compiled release for the following platforms:

* ubuntu.16.10-x64
* ubuntu.14.04-x64
* win7-x64
* win7-x86
* osx.10.10-x64

## Running from code

1. Install dotnet core by following the [installation guide](https://www.microsoft.com/net/core) for your platform
2. Create a directory for your stuff and clone into it
  `mkdir ftopindexmaker`
  `cd ftopindexmaker`
  `git clone https://github.com/puargs/ftopindexmaker.git`
3. Run the program and supply your top-level folder location
  `dotnet run /path/to/folder/containing/albums`

## Publishing instructions

Publishing instructions for multiple platforms can be found in publish-instructions.txt .