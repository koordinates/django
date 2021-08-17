# kx fork of django

to release:

* clean up: `git clean -fdx`
* make sure you're using a modern venv: `python3.10 -m venv v ; . v/bin/activate ; pip install wheel`
* Run `git show -s --pretty=format:"%cd" --date=format:%Y%m%d%H%M%S | cat`
* Update the VERSION in `django/__init__.py` to match (but don't check it in!): 

```diff
-VERSION = (3, 2, 7, 'alpha', 0)
+VERSION = (3, 2, 7, 'dev', 20210817160531)
```

* package: `make -f extras/Makefile`
* upload: `devpi upload dist/Django-{VERSION}*`
