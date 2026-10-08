
# Versioning policy

**Lead**
We release a new version with new features, enhancements, and bug fixes at least once a month. In this guide we describe our versioning policy and principles we use when choosing the version for a new build.


## Version format

DotNetBrowser version format is `MAJOR.MINOR.PATCH`, where:

* The **MAJOR** version is incremented when the significant backward-incompatible API changes are made. 
For example, this can happen when new language features are used or the architecture of the library has been significantly changed;

* The **MINOR** version is incremented when the API has been extended with new functionality. 
The changes in the API might be backward-incompatible, but most of the time they are backward-compatible;

* The **PATCH** version is incremented when some enhancements or fixes are made. The API is untouched in this case.
