bitpay/default-build
====================

The goal of the project is to create generic build scripts that can be dropped
into almost any project and with a few small changes can be customized to the
project.

# Installation

* Copy the `build` directory to your project.
* Add the contents of the `.gitattributes` and `.gitignore` files to the ones
  you already have. If you do not already have those files, just copy them
  to your git repository.
* If you are using Travis CI, copy `.travis.yml` into your project.
* Copy the `build.xml` file into your project.
* Copy the `require-dev` section of THIS projects `composer.json` into YOUR
  projects `composer.json`
* If you want a script that checks the server to make sure it has all the
  requirements for your project, copy the `requirements.php` file into
  your project.

# Configuration

* Edit `build/build.properties` to match your project. By default it assumes
  your source code is in the project root directory.
* Edit `build/phpunit.xml.dist` to match your directory structure. The logging
  sections can be left alone unless you want the code coverage documentation
  to be generated elsewhere.
* Other files you may want to update include the `requirements.php` and the
  `build.xml` script itself. Also update the `.travis.yml` file if your project
  is using it.

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

Copyright (c) 2011-2014 BitPay Inc

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
