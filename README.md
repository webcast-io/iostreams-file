# iostreams-file

File stream provider for [iostreams](https://github.com/webcast-io/iostreams)

[![Build Status](https://travis-ci.org/webcast-io/iostreams-file.png)](https://travis-ci.org/webcast-io/iostreams-file?branch=master)
[![Coverage Status](https://coveralls.io/repos/webcast-io/iostreams-file/badge.png?branch=master)](https://coveralls.io/r/webcast-io/iostreams-file?branch=master)
[![Dependency Status](https://david-dm.org/webcast-io/iostreams-file.png?theme=shields.io)](https://david-dm.org/webcast-io/iostreams-file)

## Install

    $ npm install iostreams iostreams-file

## Usage

    var iostreams = require('iostreams');

    iostreams.use(require('iostreams-file'));

    // Getting an input stream
    iostreams.getInputStream('file://home/ben/lolcat.png', function(err, inputStream) {

    });

    // Getting an output stream
    iostreams.getOutputStream('file://home/ben/lolcat.png', function(err, outputStream) {

    });

    // Getting an input and output stream
    iostrams.getInputAndOutputStream(
      'file://inputpath',
      'file://outputpath',
      function(err, inputStream, outputStream) {
        intputStream.pipe(outputStream);
      }
    );

## Licence

MIT