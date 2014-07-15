bitpay/default-build
====================

The goal of the project is to create generic build scripts that can be dropped
into almost any project and with a few small changes can be customized to the
project.

# Installation

This assumes that you do not already have a build process in place. If you are
already using Phing, composer, etc. it is assumed that you are able to look at
the source code of this project and update the files that you need to.

* Copy everything into the root of your project.
  * **NOTE** If you are already using composer, just update the `require-dev`
    section with the contents of this projects.
* Edit `build/phpunit.xml.dist` to point to your PHPUnit tests.
* Edit `build/build.properties` and configure what needs to be configured
  within that file.
* Once everything is done, run composer to install all the dependencies.

# Configuration

The majority of the configuration options for running a build are inside of
the `build.properties` file. Please update this file and read the descriptions
of each property in that file.

You may also need to update `phpunit.xml.dist`.

# Usage

By default it runs the `build` target. This will give you a full build. If you
are using this for multiple different build environments, you should copy the
build.properties file and name it something different. For example, to
configure the build for Travis CI, create a new file called travis.properties
and update the properties in that file. When you run phing, tell it to use
the travis.properties file.

# Support

If you have questions or find any issues, please open up a GitHub issue.

# Contribute

To contribute to this project, please fork and submit a pull request.

# License

The MIT License (MIT)

Copyright (c) 2011-2014 BitPay LLC

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.
