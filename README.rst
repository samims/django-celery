Looking for sponsor for working on django 1.11 to 5.2 support https://github.com/celery/django-celery/issues/568

THIS Project is only for celery v3.x to v4.x only for now!

===============================================
 django-celery - Celery Integration for Django
===============================================

.. image:: https://user-images.githubusercontent.com/26336/59113881-917c5180-890b-11e9-9863-f5a98d0e235e.png

:Version: 3.3.1
:Web: http://celeryproject.org/
:Download: http://pypi.python.org/pypi/django-celery/
:Source: http://github.com/celery/django-celery/
:Keywords: celery, task queue, job queue, asynchronous, rabbitmq, amqp, redis,
  python, django, webhooks, queue, distributed

--

.. warning:: 

    **THIS PROJECT IS ONLY REQUIRED IF YOU WANT TO USE DJANGO RESULT BACKEND
    AND ADMIN INTEGRATION**

    Please follow the new tutorial at:

    https://docs.celeryq.dev/en/stable/django/first-steps-with-django.html

django-celery provides Celery integration for Django; Using the Django ORM
and cache backend for storing results, autodiscovery of task modules
for applications listed in ``INSTALLED_APPS``, and more.

Using django-celery
===================

To enable ``django-celery`` for your project you need to add ``djcelery`` to
``INSTALLED_APPS``::

    INSTALLED_APPS += ("djcelery", )

then add the following lines to your ``settings.py``::

    import djcelery
    djcelery.setup_loader()

Everything works the same as described in the `Celery User Manual`_, except you
need to invoke the programs through ``manage.py``:

=====================================  =====================================
**Program**                            **Replace with**
=====================================  =====================================
``celery``                             ``python manage.py celery``
``celery worker``                      ``python manage.py celery worker``
``celery beat``                        ``python manage.py celery beat``
``celery ...``                         ``python manage.py celery ...``
=====================================  =====================================

The other main difference is that configuration values are stored in
your Django projects' ``settings.py`` module rather than in
``celeryconfig.py``.

If you're trying celery for the first time you should start by reading
`Getting started with django-celery`_

Special note for mod_wsgi users
-------------------------------

If you're using ``mod_wsgi`` to deploy your Django application you need to
include the following in your ``.wsgi`` module::

    import djcelery
    djcelery.setup_loader()

Documentation
=============

The `Celery User Manual`_ contains user guides, tutorials and an API
reference. It also has a dedicated `subsection about the Django integration`_.

.. _`Celery User Manual`: http://docs.celeryproject.org/
.. _`subsection about the Django integration`:
   http://docs.celeryproject.org/en/latest/django/
.. _`Getting started with django-celery`:
   http://docs.celeryproject.org/en/latest/django/first-steps-with-django.html

Installation
=============

You can install ``django-celery`` either via the Python Package Index (PyPI)
or from source.

To install using ``pip``,::

    $ pip install django-celery

To install using ``easy_install``,::

    $ easy_install django-celery

You will then want to create the necessary tables. If you generating
schema migrations, you'll want to run::

    $ python manage.py migrate djcelery



Downloading and installing from source
--------------------------------------

Download the latest version of ``django-celery`` from
http://pypi.python.org/pypi/django-celery/

You can install it by doing the following,::

    $ tar xvfz django-celery-0.0.0.tar.gz
    $ cd django-celery-0.0.0
    # python setup.py install # as root

Using the development version
------------------------------

You can clone the git repository by doing the following::

    $ git clone git://github.com/celery/django-celery.git

Getting Help
============

Mailing list
------------

For discussions about the usage, development, and future of celery,
please join the `celery-users`_ mailing list. 

.. _`celery-users`: http://groups.google.com/group/celery-users/

IRC
---

Come chat with us on IRC. The **#celery** channel is located at the `Freenode`_
network.

.. _`Freenode`: http://freenode.net


Bug tracker
===========

If you have any suggestions, bug reports or annoyances please report them
to our issue tracker at http://github.com/celery/django-celery/issues/

Wiki
====

https://github.com/celery/celery/wiki

Contributing
============

Development of ``django-celery`` happens at Github:
http://github.com/celery/django-celery

You are highly encouraged to participate in the development.
If you don't like Github (for some reason) you're welcome
to send regular patches.

License
=======

This software is licensed under the ``New BSD License``. See the ``LICENSE``
file in the top distribution directory for the full license text.

.. # vim: syntax=rst expandtab tabstop=4 shiftwidth=4 shiftround

django-celery as part of the Tidelift Subscription
=======

The maintainers of django-celery and thousands of other packages are working with Tidelift to deliver commercial support and maintenance for the open source dependencies you use to build your applications. Save time, reduce risk, and improve code health, while paying the maintainers of the exact dependencies you use. [Learn more.](https://tidelift.com/subscription/pkg/pypi-django-celery?utm_source=pypi-django-celery&utm_medium=referral&utm_campaign=readme&utm_term=repo)

