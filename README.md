Django Angular Template i18n lint
=========================

[![Bitdeli Badge](https://d2weczhvl823v0.cloudfront.net/ArabellaTech/django-angular-template-i18n-lint/trend.png)](https://bitdeli.com/free "Bitdeli Badge")
[![Build Status](https://travis-ci.org/ArabellaTech/django-angular-template-i18n-lint.svg?branch=master)](https://travis-ci.org/ArabellaTech/django-template-i18n-lint.svg)
[![Coverage Status](https://coveralls.io/repos/ArabellaTech/django-angular-template-i18n-lint/badge.svg)](https://coveralls.io/r/ArabellaTech/django-template-i18n-lint)

Fork of original project by Rory McCann, [https://github.com/rory/django-template-i18n-lint](https://github.com/rory/django-template-i18n-lint), description by original author: [Lint tool to find non-i18n strings in a django template](http://www.technomancy.org/python/django-template-i18n-lint/)

A simple script to find non-i18n text in a Django and angular templates, including:

* native Django translation `{% trans 'x' %}` and `{% blocktrans %}`

* angular translations using `{[{ 'xx'|translate }]}` and `<p translate>paragraph</p>`

Usage:
======

    $ python django_angular_template_i18n_lint.py templates > not_translated.txt

saves all untranslated strings into given file. The original option to wrap in translation blocks was removed, due to
support of many translation options (i.e. angular).

Program docs are available:

    $ python django_angular_template_i18n_lint --h


Usefull hints:
==============

Putting `{# notrans #}` or `<!-- notrans -->` at the begining of line will prevent that line from showin in the results.

Known issues
============

* `<div translate><span></span><i class='x'></i>SomeText</div>` will fail due to html tags inside. Required is to use
 `<span translate>value</span>` or `{[{ 'x'|translate}]}`

* in some situations it will be preferable to use `{[{ 'x'|translate}]}` instead of `<tag translate>`, in example when tag has `data-` or `aa-` or `ng-` attribute

