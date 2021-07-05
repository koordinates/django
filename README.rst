kx fork of django
=================

to release:

* clean up: :code:`git clean -fdx`
* make sure you're using a modern venv: :code:`virtualenv -p python3 v ; . v/bin/activate`
* package: :code:`make -f extras/Makefile`
* upload: :code:`devpi upload dist/Django-{VERSION}*`
