# kx fork of django

to release:

* clean up: `git clean -fdx`
* Run `git show -s --pretty=format:"%cd" --date=format:%Y%m%d%H%M%S | cat`
* Update the VERSION in `django/__init__.py` to match (but don't check it in!): 

```diff
-VERSION = (3, 2, 7, 'alpha', 0)
+VERSION = (3, 2, 7, 'dev', 20210817160531)
```

* package: `uv build`
* upload: `devpi upload dist/django-{VERSION}*`
