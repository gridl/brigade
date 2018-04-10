[![Build Status](https://travis-ci.org/brigade-automation/brigade.svg?branch=master)](https://travis-ci.org/brigade-automation/brigade) [![Code style: black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/ambv/black) [![Coverage Status](https://coveralls.io/repos/github/brigade-automation/brigade/badge.svg?branch=master)](https://coveralls.io/github/brigade-automation/brigade?branch=master)


Brigade
=======
Brigade is a pure Python automation framework intented to be used directly from Python. While most automation frameworks use their own DSL which you use to describe what you want to have done, Brigade lets you control everything from Python.

One of the benefits we want to highlight with this approach is the ease of troubleshooting, if something goes wrong you can just use your existing debug tools directly from Python (just add a line of `import pdb` & `pdb.set_trace()` and you're good to go). Doing the same using a DSL can be quite time consuming.

What Brigade brings to the table is that it takes care of dealing with your inventory and manages the job of dispatching the tasks you want to run against your nodes and devices. The framework provides a very simple way to write plugins if you aren't happy with the ones we ship. Of course if you have written a plugin you think can be useful to others, please send us your code and test cases as a [pull request](https://github.com/brigade-automation/brigade/pulls).


Install
=======

While Brigade still supports Python 2.7 the recommended version is 3.6. Install it with pip.

```
pip install brigade
```

Versioning
==========

It is recommended to understand what the versioning of brigade tells you. The format is as follows; `x.y.z`, where:

- `x` is the API version. This will rarely change and if it does it means it's a major release that breaks completely backwards compatibility.
- `y` will indicate a change in the existing codebase. This means there has been additions to the core of brigade or changes to existing plugins. As they add new functionality to existing code it is recommended to test your code before upgrading.
- `z` will indicate bugfixes or new plugins. Upgrading should be completely safe as existing code/API will not be modified other than to fix bugs.

We will release a `y` version every quarter and indicate so with the format `YYQ` where `YY` is the year and `Q` the quarter. We will release `z` versions as often as needed.

We recommend pinning the requirements to a `y` version. For instance `brigade>1.181.0<1.183.0` if you want to stick with `1.182.???`

Documentation
=============

Read the [Brigade documentation](https://brigade.readthedocs.io/en/latest/) online or review it's [code here](https://github.com/brigade-automation/brigade/tree/develop/docs)


Bugs & New features
===================

If you think you have bug or would like to request a new feature, please register a GitHub account and [open an issue](https://github.com/brigade-automation/brigade/issues).


Contact & Support
=================

While we are happy to help, the [GitHub issues](<https://github.com/brigade-automation/brigade/issues>) are intended for bugs and discussions about new features. If are struggling to get something to work but don't believe its due to a bug in Brigade, the place to ask questions is in the #brigade channel in the [networktoCode Slack team](https://networktocode.herokuapp.com/).


Contributing to Brigade
=======================

If you want to help the project, the [Contribution Guidelines](CONTRIBUTING.rst) is the best place to start.
