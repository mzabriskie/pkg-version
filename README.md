# pkg-version

One of the problems with using semver ranges is that you can inadvertently end up with a newer version of one of your dependencies, which can in turn break things. This is where you get into the argument between co-workers "Well, it works on my machine!".

This module is meant to help identify what's different between the version `package.json` is asking for, and what is actually installed. By highlighting the version difference between what you have installed, and what you thought you had installed, you can narrow down what package, and what version introduced the breaking change.

## Installation

```bash
$ npm install -g pkg-version
```

## Synopsis

```bash
$ pkg-version <folder>
```

- \<folder>: A folder containing a package.json file

Uses '.' if no argument supplied

## Usage

Show dependencies for a package and highlight version differences.

```bash
$ pkg-version
Package                     Wanted   Actual
babel                       ^5.5.8    5.8.3
babel-core                  ^5.5.6    5.8.3
babel-eslint               ^3.1.23   3.1.24
babel-loader                ^5.1.4    5.3.2
eslint                     ^0.24.1   0.24.1
karma                     ^0.12.36  0.12.37
karma-chrome-launcher      ^0.1.12   0.1.12
karma-cli                    0.0.4    0.0.4
karma-firefox-launcher      ^0.1.6    0.1.6
karma-mocha                ^0.1.10   0.1.10
karma-sourcemap-loader      ^0.3.5    0.3.5
karma-webpack               ^1.5.1    1.6.0
mocha                       ^2.2.5    2.2.5
webpack                    ^1.9.10   1.10.1
webpack-dev-server          ^1.9.0   1.10.1
```

## License

MIT
