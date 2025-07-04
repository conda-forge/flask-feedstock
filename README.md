About flask-feedstock
=====================

Feedstock license: [BSD-3-Clause](https://github.com/conda-forge/flask-feedstock/blob/main/LICENSE.txt)

Home: https://palletsprojects.com/p/flask

Package license: BSD-3-Clause

Summary: A simple framework for building complex web applications.

Development: https://github.com/pallets/flask/

Documentation: https://flask.palletsprojects.com/

Flask is a lightweight [WSGI](https://wsgi.readthedocs.io/) web application framework. It is designed
to make getting started quick and easy, with the ability to scale up to
complex applications. It began as a simple wrapper around [Werkzeug](https://werkzeug.palletsprojects.com/)
and [Jinja](https://jinja.palletsprojects.com/) and has become one of the most popular Python web
application frameworks.
Flask offers suggestions, but doesn't enforce any dependencies or
project layout. It is up to the developer to choose the tools and
libraries they want to use. There are many extensions provided by the
community that make adding new functionality easy.


Current build status
====================


<table><tr><td>All platforms:</td>
    <td>
      <a href="https://dev.azure.com/conda-forge/feedstock-builds/_build/latest?definitionId=2934&branchName=main">
        <img src="https://dev.azure.com/conda-forge/feedstock-builds/_apis/build/status/flask-feedstock?branchName=main">
      </a>
    </td>
  </tr>
</table>

Current release info
====================

| Name | Downloads | Version | Platforms |
| --- | --- | --- | --- |
| [![Conda Recipe](https://img.shields.io/badge/recipe-flask-green.svg)](https://anaconda.org/conda-forge/flask) | [![Conda Downloads](https://img.shields.io/conda/dn/conda-forge/flask.svg)](https://anaconda.org/conda-forge/flask) | [![Conda Version](https://img.shields.io/conda/vn/conda-forge/flask.svg)](https://anaconda.org/conda-forge/flask) | [![Conda Platforms](https://img.shields.io/conda/pn/conda-forge/flask.svg)](https://anaconda.org/conda-forge/flask) |
| [![Conda Recipe](https://img.shields.io/badge/recipe-flask--with--async-green.svg)](https://anaconda.org/conda-forge/flask-with-async) | [![Conda Downloads](https://img.shields.io/conda/dn/conda-forge/flask-with-async.svg)](https://anaconda.org/conda-forge/flask-with-async) | [![Conda Version](https://img.shields.io/conda/vn/conda-forge/flask-with-async.svg)](https://anaconda.org/conda-forge/flask-with-async) | [![Conda Platforms](https://img.shields.io/conda/pn/conda-forge/flask-with-async.svg)](https://anaconda.org/conda-forge/flask-with-async) |
| [![Conda Recipe](https://img.shields.io/badge/recipe-flask--with--dotenv-green.svg)](https://anaconda.org/conda-forge/flask-with-dotenv) | [![Conda Downloads](https://img.shields.io/conda/dn/conda-forge/flask-with-dotenv.svg)](https://anaconda.org/conda-forge/flask-with-dotenv) | [![Conda Version](https://img.shields.io/conda/vn/conda-forge/flask-with-dotenv.svg)](https://anaconda.org/conda-forge/flask-with-dotenv) | [![Conda Platforms](https://img.shields.io/conda/pn/conda-forge/flask-with-dotenv.svg)](https://anaconda.org/conda-forge/flask-with-dotenv) |

Installing flask
================

Installing `flask` from the `conda-forge` channel can be achieved by adding `conda-forge` to your channels with:

```
conda config --add channels conda-forge
conda config --set channel_priority strict
```

Once the `conda-forge` channel has been enabled, `flask, flask-with-async, flask-with-dotenv` can be installed with `conda`:

```
conda install flask flask-with-async flask-with-dotenv
```

or with `mamba`:

```
mamba install flask flask-with-async flask-with-dotenv
```

It is possible to list all of the versions of `flask` available on your platform with `conda`:

```
conda search flask --channel conda-forge
```

or with `mamba`:

```
mamba search flask --channel conda-forge
```

Alternatively, `mamba repoquery` may provide more information:

```
# Search all versions available on your platform:
mamba repoquery search flask --channel conda-forge

# List packages depending on `flask`:
mamba repoquery whoneeds flask --channel conda-forge

# List dependencies of `flask`:
mamba repoquery depends flask --channel conda-forge
```


About conda-forge
=================

[![Powered by
NumFOCUS](https://img.shields.io/badge/powered%20by-NumFOCUS-orange.svg?style=flat&colorA=E1523D&colorB=007D8A)](https://numfocus.org)

conda-forge is a community-led conda channel of installable packages.
In order to provide high-quality builds, the process has been automated into the
conda-forge GitHub organization. The conda-forge organization contains one repository
for each of the installable packages. Such a repository is known as a *feedstock*.

A feedstock is made up of a conda recipe (the instructions on what and how to build
the package) and the necessary configurations for automatic building using freely
available continuous integration services. Thanks to the awesome service provided by
[Azure](https://azure.microsoft.com/en-us/services/devops/), [GitHub](https://github.com/),
[CircleCI](https://circleci.com/), [AppVeyor](https://www.appveyor.com/),
[Drone](https://cloud.drone.io/welcome), and [TravisCI](https://travis-ci.com/)
it is possible to build and upload installable packages to the
[conda-forge](https://anaconda.org/conda-forge) [anaconda.org](https://anaconda.org/)
channel for Linux, Windows and OSX respectively.

To manage the continuous integration and simplify feedstock maintenance
[conda-smithy](https://github.com/conda-forge/conda-smithy) has been developed.
Using the ``conda-forge.yml`` within this repository, it is possible to re-render all of
this feedstock's supporting files (e.g. the CI configuration files) with ``conda smithy rerender``.

For more information please check the [conda-forge documentation](https://conda-forge.org/docs/).

Terminology
===========

**feedstock** - the conda recipe (raw material), supporting scripts and CI configuration.

**conda-smithy** - the tool which helps orchestrate the feedstock.
                   Its primary use is in the construction of the CI ``.yml`` files
                   and simplify the management of *many* feedstocks.

**conda-forge** - the place where the feedstock and smithy live and work to
                  produce the finished article (built conda distributions)


Updating flask-feedstock
========================

If you would like to improve the flask recipe or build a new
package version, please fork this repository and submit a PR. Upon submission,
your changes will be run on the appropriate platforms to give the reviewer an
opportunity to confirm that the changes result in a successful build. Once
merged, the recipe will be re-built and uploaded automatically to the
`conda-forge` channel, whereupon the built conda packages will be available for
everybody to install and use from the `conda-forge` channel.
Note that all branches in the conda-forge/flask-feedstock are
immediately built and any created packages are uploaded, so PRs should be based
on branches in forks and branches in the main repository should only be used to
build distinct package versions.

In order to produce a uniquely identifiable distribution:
 * If the version of a package **is not** being increased, please add or increase
   the [``build/number``](https://docs.conda.io/projects/conda-build/en/latest/resources/define-metadata.html#build-number-and-string).
 * If the version of a package **is** being increased, please remember to return
   the [``build/number``](https://docs.conda.io/projects/conda-build/en/latest/resources/define-metadata.html#build-number-and-string)
   back to 0.

Feedstock Maintainers
=====================

* [@goanpeca](https://github.com/goanpeca/)
* [@marcelotrevisani](https://github.com/marcelotrevisani/)
* [@nehaljwani](https://github.com/nehaljwani/)
* [@ukaratay](https://github.com/ukaratay/)
* [@xylar](https://github.com/xylar/)

