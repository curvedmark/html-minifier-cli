# html-minifier-cli

Command-line interface for [html-minifier](http://kangax.github.io/html-minifier/)

## Install

`npm install html-minifier-cli -g`

## Usage
See `htmlmin -h` for full details.

### Examples
Read from `index.html` and write to `index.min.html`:
`htmlmin -o index.min.html index.html`

Read all files from `client/views` and write them to `public/views`:
`htmlmin -o public/views client/views`

Read from `client/views/index.html` and write it to already existing folder
`public/views`:
`htmlmin -o public/views client/views/index.html`

### Output
You can pass input either as a path to a file or a folder, or directly from
stdin. When passed a folder as input, the program will attempt to recursively
create a folder with the name specified in the `-o` option. Or if there is
already a folder with the same name as the output location, the program will
write each of the input files to that folder. If the input comes from stdin and
the output location is a folder, a file named `htmlmin.html` will be saved in
that folder.
