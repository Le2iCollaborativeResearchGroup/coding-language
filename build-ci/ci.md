# Continuous integration

There is several tools available to automatically run your unit tests when
pushing a new pull request or to automatically build the documentation of your
library.

We will give the name of the most trendy tools that you can use.

### Travis CI

Travis-CI is a continuous integration service which offer a remote machine to
run unit tests. It is perfect to manage linux and osx install.

### AppVeyor

This is the counterpart of Travis but for Windows

### Circle CI

This is another continuous integration system offering nice features. In
scikit-learn, this CI is used to build and push automatically the documentation.

### Codecov

Previously, coverall was used to manage code coverage. Codecov offers better
features and should be used instead.
