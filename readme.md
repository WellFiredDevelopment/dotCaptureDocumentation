# .Capture documentation

This repository contains the source files of [.Capture](http://dotcapture-documentation.readthedocs.io/en/stable/)'s documentation,  in reStructuredText markup language (reST).

They are meant to be parsed with the [Sphinx](http://sphinx-doc.org/) documentation builder to build the HTML documentation on [.Capture](http://dotcapture-documentation.readthedocs.io/en/stable/)'s documentation page.

## Contributing changes

Though it may seem like contributing changes is less convenient than an ordinary wiki, this repository allows us to source pull requests from our community, whilst also providing us a way to version control documentation. The documentation is hosted on [ReadTheDocs](https://readthedocs.org/), and their theme allows us to automatically tag versions with the appropriate version number.

### Editing existing pages

To edit an existing page, just locate its .rst source file in `sphinx/source/`, open it in your favourite text editor. You can then commit the changes, push them to your fork and make a pull request. **Note that the pages in `sphinx/source/api/` should not be edited as these are generated programatically from the .Capture source code, if you spot an issue here, you can feel free to submit an issue on .Capture's [Bug Tracker](https://wellfired.myjetbrains.com/youtrack/issues/DC).**

### Adding new pages

Adding a new page should be relatively straight forward, simple create an rst file in the appropriate location, trying to adhear to the rules set in place by existing files. You can populate the file by simply writing text in your favourite text editor, feel free to use one of the existing files as reference, you can also see the [reStructuredText](http://docutils.sourceforge.net/rst.html) documentation as a reference point.

You should then add your page to the relevant `.. toctree::` in an index.rst page. For example, if you add a file to `learn/step_by_step/`, you would want to append a new line referencing your new file in index.rst. Please feel free to use the existing pages as a point of reference.

## Building with Sphinx

To build the HTML website (or any other format supported by Sphinx, like PDF, EPUB or LaTeX), you need to install [Sphinx](http://sphinx-doc.org/) >= 1.3 as well as (for the HTML) the [readthedocs.org theme](https://github.com/snide/sphinx_rtd_theme).

Those tools are best installed using [pip](https://pip.pypa.io), Python's module installer. The Python 3 version might be provided (on Linux distros) as `pip3` or `python3-pip`. You can then run:

```sh
pip3 install sphinx
pip3 install sphinx_rtd_theme
```

You can then build the HTML documentation from the root folder of this repository with:

```sh
cd sphinx
make html
```