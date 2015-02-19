Django Template i18n lint
=========================

[![Build Status](https://travis-ci.org/ArabellaTech/django-template-i18n-lint.svg?branch=master)](https://travis-ci.org/ArabellaTech/django-template-i18n-lint.svg)
[![Coverage Status](https://coveralls.io/repos/ArabellaTech/django-template-i18n-lint/badge.svg)](https://coveralls.io/r/ArabellaTech/django-template-i18n-lint)
[![PyPI version](https://pypip.in/v/django-template-i18n-lint/badge.png)](https://pypi.python.org/pypi/django-template-i18n-lint)
[![PyPI Downloads](https://pypip.in/d/django-template-i18n-lint/badge.png)](https://pypi.python.org/pypi/django-template-i18n-lint)

Fork of original project by Rory McCann, [https://github.com/rory/django-template-i18n-lint](https://github.com/rory/django-template-i18n-lint), description by original author: [Lint tool to find non-i18n strings in a django template](http://www.technomancy.org/python/django-template-i18n-lint/)

A simple script to find non-i18n text in a Django template, including:

* native Django translation `{% trans 'x' %}` and `{% blocktrans %}`

* angular translations using `{[{ 'xx'|translate }]}` and `<p translate>paragraph</p>`

* supports a lot of custom angular directives, especially used by ArabellaTech (name starts with aa-)

Usage:

    $ python django_template_i18n_lint.py templates > not_translated.txt

saves all untranslated strings into given file. The original option to wrap in translation blocks was removed, due to 
support of many translation options (i.e. angular).

Program docs are available:

    $ python django_template_i18n_lint --h

Code is copyright Rory McCann 2013 and ArabellaTech 2015, and dual licenced under the GNU GPL version3 (or at your option a later version), and the BSD licence. See the files LICENCE.GPLv3 and LICENCE.BSD for more information

