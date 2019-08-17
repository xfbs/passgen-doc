# Passgen

Generate passwords using a regex-like language describing their shape.

Passgen is a C library and command-line tool to generate random data using a format specified with a syntax loosely based on regular expressions.

## Installation

If you are on macOS, you can install passgen from Homebrew, the macOS package manager.

    brew install xfbs/local/passgen

If you are on another platform, you can install it manually. You need `utf8proc`, `jansson` and `libsodium` as dependency. On a recent version of ubuntu, you can install it as follows:

    wget https://github.com/xfbs/passgen/archive/latest.zip -O passgen.zip
    unzip passgen.zip
    cd passgen
    make
    make install

## Basic Usage

There are some presets available to use. These are mostly sane defaults and can be selected with the `-p` switch on the command line.

    $ passgen -p apple1
    NlY-AUA-7kd-FNR

Alternatively, the format can be specified manually.

    $ passgen "[a-z]{8}[0-9]{2}"
    znjatqzb29

