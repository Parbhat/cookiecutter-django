Cookiecutter Django Foundation
==============================

.. image:: https://travis-ci.org/Parbhat/cookiecutter-django-foundation.svg?branch=master
     :target: https://travis-ci.org/Parbhat/cookiecutter-django-foundation?branch=master
     :alt: Build Status

.. image:: https://pyup.io/repos/github/pydanny/cookiecutter-django/shield.svg
     :target: https://pyup.io/repos/github/pydanny/cookiecutter-django/
     :alt: Updates

.. image:: https://img.shields.io/badge/code%20style-black-000000.svg
    :target: https://github.com/ambv/black
    :alt: Code style: black

Cookiecutter Django Foundation is fork of awesome `Cookiecutter Django`_. Powered by Cookiecutter_, Cookiecutter Django
is a framework for jumpstarting production-ready Django projects quickly. Cookiecutter Django Foundation uses the `Zurb
Foundation`_ 6 as the front end framework. This project combines the Cookiecutter Django with the Foundation framework.
The project contains a ``_settings.scss`` file to easily customize the default styling of the Foundation framework.
For example, the default colors can be changed by changing the foundation-palette.

.. code:: sass

    $foundation-palette: (
      primary: #1779ba,
      secondary: #767676,
      success: #3adb76,
      warning: #ffae00,
      alert: #cc4b37,
    );

.. image:: http://i.imgur.com/Z9Q4W37.png
     :alt: Foundation Django

For more information about `Cookiecutter Django`_

* Documentation: https://cookiecutter-django.readthedocs.io/en/latest/
* See Troubleshooting_ for common errors and obstacles
* If you have problems with Cookiecutter Django, please open issues_ don't send
  emails to the maintainers.

.. _Troubleshooting: https://cookiecutter-django.readthedocs.io/en/latest/troubleshooting.html

.. _528: https://github.com/pydanny/cookiecutter-django/issues/528#issuecomment-212650373
.. _issues: https://github.com/pydanny/cookiecutter-django/issues/new

.. _Cookiecutter Django: https://github.com/pydanny/cookiecutter-django

Features
---------

* For Django 2.2
* Works with Python 3.7
* Renders Django projects with 100% starting test coverage
* `Zurb Foundation`_ 6 with an option to customize using SASS variables (100% SASS).
* 12-Factor_ based settings via django-environ_
* Compile Sass files using libsass via django-libsass_.
* `Django Foundation Formtags`_ to work with Zurb Foundation forms
* Secure by default. We believe in SSL.
* Optimized development and production settings
* Registration via django-allauth_
* Comes with custom user model ready to go
* Optional custom static build using Gulp and livereload
* Send emails via Anymail_ (using Mailgun_ by default, but switchable)
* Media storage using Amazon S3 or Google Cloud Storage
* Docker support using docker-compose_ for development and production (using Traefik_ with LetsEncrypt_ support)
* Procfile_ for deploying to Heroku
* Instructions for deploying to PythonAnywhere_
* Run tests with unittest or pytest
* Customizable PostgreSQL version
* Default integration with pre-commit_ for identifying simple issues before submission to code review


Optional Integrations
---------------------

*These features can be enabled during initial project setup.*

* Serve static files from Amazon S3, Google Cloud Storage or Whitenoise_
* Configuration for Celery_ and Flower_ (the latter in Docker setup only)
* Integration with MailHog_ for local email testing
* Integration with Sentry_ for error logging

.. _django-libsass: https://github.com/torchbox/django-libsass
.. _Django Foundation Formtags: https://github.com/chrisdev/django-foundation-formtags
.. _Zurb Foundation: http://foundation.zurb.com/
.. _django-environ: https://github.com/joke2k/django-environ
.. _12-Factor: http://12factor.net/
.. _django-allauth: https://github.com/pennersr/django-allauth
.. _django-avatar: https://github.com/grantmcconnaughey/django-avatar
.. _Procfile: https://devcenter.heroku.com/articles/procfile
.. _Mailgun: http://www.mailgun.com/
.. _Whitenoise: https://whitenoise.readthedocs.io/
.. _Celery: http://www.celeryproject.org/
.. _Flower: https://github.com/mher/flower
.. _Anymail: https://github.com/anymail/django-anymail
.. _MailHog: https://github.com/mailhog/MailHog
.. _Sentry: https://sentry.io/welcome/
.. _docker-compose: https://github.com/docker/compose
.. _PythonAnywhere: https://www.pythonanywhere.com/
.. _Traefik: https://traefik.io/
.. _LetsEncrypt: https://letsencrypt.org/
.. _pre-commit: https://github.com/pre-commit/pre-commit 

Constraints
-----------

* Only maintained 3rd party libraries are used.
* Uses PostgreSQL everywhere (9.4 - 11.3)
* Environment variables for configuration (This won't work with Apache/mod_wsgi).

Support this Project!
----------------------

This project is run by volunteers. Please support them in their efforts to maintain and improve Cookiecutter Django:

* Daniel Roy Greenfeld, Project Lead (`GitHub <https://github.com/pydanny>`_, `Patreon <https://www.patreon.com/danielroygreenfeld>`_): expertise in Django and AWS ELB.

* Nikita Shupeyko, Core Developer (`GitHub <https://github.com/webyneter>`_): expertise in Python/Django, hands-on DevOps and frontend experience.

Projects that provide financial support to the maintainers:

Two Scoops of Django 1.11
~~~~~~~~~~~~~~~~~~~~~~~~~

.. image:: https://cdn.shopify.com/s/files/1/0304/6901/products/2017-06-29-tsd11-sticker-02.png
   :name: Two Scoops of Django 1.11 Cover
   :align: center
   :alt: Two Scoops of Django
   :target: http://twoscoopspress.com/products/two-scoops-of-django-1-11

Two Scoops of Django is the best dessert-themed Django reference in the universe

pyup
~~~~~~~~~~~~~~~~~~

.. image:: https://pyup.io/static/images/logo.png
   :name: pyup
   :align: center
   :alt: pyup
   :target: https://pyup.io/

Pyup brings you automated security and dependency updates used by Google and other organizations. Free for open source projects!

Usage
------

Let's pretend you want to create a Django project called "redditclone". Rather than using ``startproject``
and then editing the results to include your name, email, and various configuration issues that always get forgotten until the worst possible moment, get cookiecutter_ to do all the work.

First, get Cookiecutter. Trust me, it's awesome::

    $ pip install "cookiecutter>=1.4.0"

Now run it against this repo::

    $ cookiecutter https://github.com/Parbhat/cookiecutter-django-foundation

You'll be prompted for some values. Provide them, then a Django project will be created for you.

**Warning**: After this point, change 'Daniel Greenfeld', 'pydanny', etc to your own information.

Answer the prompts with your own desired options_. For example::

    Cloning into 'cookiecutter-django-foundation'...
    remote: Counting objects: 8869, done.
    remote: Compressing objects: 100% (37/37), done.
    remote: Total 8869 (delta 15), reused 0 (delta 0), pack-reused 8832
    Receiving objects: 100% (8869/8869), 3.53 MiB | 468.00 KiB/s, done.
    Resolving deltas: 100% (5591/5591), done.
    Checking connectivity... done.
    project_name [Project Name]: Reddit Clone
    project_slug [reddit_clone]: reddit
    author_name [Daniel Roy Greenfeld]: Daniel Greenfeld
    email [you@example.com]: pydanny@gmail.com
    description [Behold My Awesome Project!]: A reddit clone.
    domain_name [example.com]: myreddit.com
    version [0.1.0]: 0.0.1
    timezone [UTC]: America/Los_Angeles
    use_whitenoise [n]: n
    use_celery [n]: y
    use_mailhog [n]: n
    use_sentry [n]: y
    use_pycharm [n]: y
    windows [n]: n
    use_docker [n]: n
    use_heroku [n]: y
    Select postgresql_version:
    1 - 11.3
    2 - 10.8
    3 - 9.6
    4 - 9.5
    5 - 9.4
    Choose from 1, 2, 3, 4, 5 [1]: 1
    Select js_task_runner:
    1 - None
    2 - Gulp
    Choose from 1, 2 [1]: 1
    Select cloud_provider:
    1 - AWS
    2 - GCP
    3 - None
    Choose from 1, 2, 3 [1]: 1
    Select open_source_license:
    1 - MIT
    2 - BSD
    3 - GPLv3
    4 - Apache Software License 2.0
    5 - Not open source
    Choose from 1, 2, 3, 4, 5 [1]: 1
    keep_local_envs_in_vcs [y]: y
    debug[n]: n

Enter the project and take a look around::

    $ cd reddit/
    $ ls

Create a git repo and push it there::

    $ git init
    $ git add .
    $ git commit -m "first awesome commit"
    $ git remote add origin git@github.com:pydanny/redditclone.git
    $ git push -u origin master

Now take a look at your repo. Don't forget to carefully look at the generated README. Awesome, right?

For local development, see the following:

* `Developing locally`_
* `Developing locally using docker`_

.. _options: http://cookiecutter-django.readthedocs.io/en/latest/project-generation-options.html
.. _`Developing locally`: http://cookiecutter-django.readthedocs.io/en/latest/developing-locally.html
.. _`Developing locally using docker`: http://cookiecutter-django.readthedocs.io/en/latest/developing-locally-docker.html

Modify the default styles of Foundation
---------------------------------------

The projects generated with this cookiecutter include a settings file, named ``_settings.scss``. You can find the settings
file under ``<project_slug>/static/sass``.

Every component includes a set of variables that modify core structural or visual styles. If there's something you can't
customize with a variable, you can just write your own CSS to add it.


Here's an example set of settings variables. These change the default styling of buttons:

.. code:: sass

    // Default padding for button.
    $button-padding: 0.85em 1em !default;

    // Default margin for button.
    $button-margin: 0 $global-padding $global-padding 0 !default;

    // Default fill for button. Is either solid or hollow.
    $button-fill: solid !default;

    // Default background color for button.
    $button-background: $primary-color !default;

    // Default hover background color for button.
    $button-background-hover: scale-color($button-background, $lightness: -15%) !default;

    // Default font color for button.
    $button-font-color: #fff !default;

    // Default alternative font color for button.
    $button-font-color-alt: #000 !default;

    // Default radius for button.
    $button-radius: 0 !default;

    // Default sizes for button.
    $button-sizes: (
      tiny: 0.7,
      small: 0.8,
      medium: 1,
      large: 1.3,
    ) !default;

    // Default font size for button.
    $button-font-size: 0.9rem !default;

    // Default opacity for a disabled button.
    $button-opacity-disabled: 0.25 !default;

Contributing
------------

Contributions are always welcome to improve this project. If you think you've found a bug or are interested in contributing
fork this project and send the pull request. After review, your pull request will be merged. We are always happy to receive
pull requests. If you identify any issue, please raise it in the issues section.
