# bash-hello-world-with-locales

This project is example for create a set of scripts project with installer and auto configuration.

The project contain the script hello-word.sh which simple write "Hello World!" in different locales and script set-default-helloworld-locales.sh for setting the message locales. All file are placed in the directory @bindir@ at GNU.

Also the project contains templates of locales in the directory @datadir@\@PACKAGE@ and working locale at the directory @runstatedir@/@PACKAGE@

## Installation

Simple ./configure && make && sudo make installer

## Requirements

This project require Linux packages bash, sed, coreutils and autotools. Additional compilers and tools no need.


