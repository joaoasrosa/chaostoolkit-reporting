# chaostoolkit-reporting

[![Build Status](https://travis-ci.org/chaostoolkit/chaostoolkit-reporting.svg?branch=master)](https://travis-ci.org/chaostoolkit/chaostoolkit-reporting)

The Chaos Toolkit reporting extension library.

## Purpose

The purpose of this library is to provide reporting support to the
[Chaos Toolkit][chaostoolkit] experiment results.

[chaostoolkit]: http://chaostoolkit.org

## Features

The library takes the journal generated by the `chaos run` command
and transforms into a human friendly report. The report can be a standalone
PDF or HTML document.

## Install

Install this package as any other Python packages:

```
$ pip install -U chaostoolkit-reporting
```

Notice that this draws a few [dependencies][deps]:

[deps]: https://github.com/chaostoolkit/chaostoolkit-reporting/blob/master/requirements.txt

Some of them are LGPL v3 licensed.

You will also need to install the [pandoc][] package on your system.

[pandoc]: https://pandoc.org/

If you intend on creating PDF reports, the following additional packages will
be needed:

```
$ sudo apt-get install texlive-latex-base \
    texlive-fonts-recommended \
    texlive-fonts-extra \
    texlive-latex-extra \
    pdflatex
```

## Usage

Once installed, a new `report` subcommand will be made available to the
`chaos` command, use it as follows:

```
$ chaos report --export-format=html5 chaos-report.json report.html
```

or, for a PDF document:

```
$ chaos report --export-format=pdf chaos-report.json report.pdf
```

## Contribute

Contributors to this project are welcome as this is an open-source effort that
seeks [discussions][join] and continuous improvement.

[join]: https://join.chaostoolkit.org/

From a code perspective, if you wish to contribute, you will need to run a 
Python 3.5+ environment. Then, fork this repository and submit a PR. The
project cares for code readability and checks the code style to match best
practices defined in [PEP8][pep8]. Please also make sure you provide tests
whenever you submit a PR so we keep the code reliable.

[pep8]: https://pycodestyle.readthedocs.io/en/latest/

