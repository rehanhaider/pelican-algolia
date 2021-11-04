Algolia Search: A Plugin for Pelican
====================================================

[![Build Status](https://img.shields.io/github/workflow/status/rehanhaider/pelican-algolia/build)](https://github.com/rehanhaider/pelican-algolia/actions)
[![PyPI Version](https://img.shields.io/pypi/v/pelican-algolia)](https://pypi.org/project/pelican-algolia/)
![License](https://img.shields.io/pypi/l/pelican-algolia?color=blue)


Installation
------------

This plugin can be installed via:

    python -m pip install pelican-algolia

Prerequisites
-------------
1. Create an [Algolia](https://www.algolia.com/) account
2. On Algolia website, create a new application
3. Create a new Index (or Indices) in you Algolia app. This will be `ALGOLIA_INDEX_NAME`
4. Import you records, if asked select **Use the API** option
5. Go to Settings -> API Keys -> Your API Keys and copy your 
    * Application ID, this will be `ALGOLIA_APP_ID`
    * Admin API Key (**DO NOT HARD CODE THIS IN YOUR PROGRAM**). This will be `ALGOLIA_ADMIN_API_KEY`
    * Algolia Search-Only API Key. This will be `ALGOLIA_SEARCH_API_KEY`

Usage
-----
**Step 1**: Set the following configuration in `pelicanconf.py`
```python
# Algolia Publish Data
ALGOLIA_APP_ID = "<Your Algolia App ID>"
ALGOLIA_SEARCH_API_KEY = "<Your Search-only Api Key>"
ALGOLIA_INDEX_NAME = "<You Algolia App Index name>"
```
**Step 2**: Set the `ALGOLIA_ADMIN_API_KEY` as an environmatal variable on path

**Step 3**: Import `ALGOLIA_ADMIN_API_KEY` in your `publishconf.py` (or `pelicanconf.py` if you're not using `publishconf.py` for publish settings)
```python
import os
ALGOLIA_ADMIN_API_KEY = os.environ.get("ALGOLIA_ADMIN_API_KEY")
```

Contributing
------------

Contributions are welcome and much appreciated. Every little bit helps. You can contribute by improving the documentation, adding missing features, and fixing bugs. You can also help out by reviewing and commenting on [existing issues][].

To start contributing to this plugin, review the [Contributing to Pelican][] documentation, beginning with the **Contributing Code** section.

[existing issues]: https://github.com/rehanhaider/pelican-algolia/issues
[Contributing to Pelican]: https://docs.getpelican.com/en/latest/contribute.html

License
-------

This project is licensed under the AGPL-3.0 license.
