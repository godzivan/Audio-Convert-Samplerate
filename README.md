# Audio::Convert::Samplerate

Convert the samplerate of PCM audio data using libsamplerate (AKA "Secret Rabbit Code".)

[![Build Status](https://travis-ci.org/jonathanstowe/Audio-Convert-Samplerate.svg?branch=master)](https://travis-ci.org/jonathanstowe/Audio-Convert-Samplerate)

## Description

This provides a mechanism for doing sample rate conversion of PCM audio
data using libsamplerate (http://www.mega-nerd.com/libsamplerate/)
the implementation of which is both fairly quick and accurate.

The interface is fairly simple, providing methods to work with native
C arrays where the raw speed is important as well as perl arrays where
further processing is required on the data.

The native library is designed to work only with 32 bit floating point
samples so working with other sample types requires some conversion
and a subsequent small loss of efficiency (although the int and short
to float conversions are done in C code and so are reasonably quick.)
There is no support for 64 bit int (long) or float (double) data.

The full documentation is available as POD or [Markdown](Documentation.md)

## Installation

You will need to have "libsamplerate"  installed on your system in order to
be able to use this. Most Linux distributions offer it as a package, though
it is such a common dependency for multimedia applications that you may well
already have it installed.

If you are on some platform that doesn't provide libsamplerate as a package
then you may be able to install it from source:

http://www.mega-nerd.com/libsamplerate/download.html

I am however unlikely to be able to offer help with installing it this way.

Assuming you have a working perl6 installation you should be able to
install this with *zef* :

    # From the source directory
   
    zef install .

    # Remote installation

    zef install Audio::Convert::Samplerate

Other install mechanisms may be become available in the future.

## Support

Suggestions/patches are welcomed via github at https://github.com/jonathanstowe/Audio-Convert-Samplerate/issues

## Licence

Please see the [LICENCE](LICENCE) file in the distribution

© Jonathan Stowe 2015, 2016, 2017, 2019
