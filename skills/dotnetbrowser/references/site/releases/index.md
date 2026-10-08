# Release Policy

**Lead**
This section contains a complete release history for DotNetBrowser in reverse chronological order.
We aim to release a new version with new features, enhancements, and bug fixes at least once a month.
Below we describe our versioning policy and principles we use when choosing the version for a new build.


## Version number format

DotNetBrowser version format is MAJOR.MINOR.PATCH.

### MAJOR

The MAJOR version is incremented when a significant backward-incompatible API change is made. 
For example, this can happen when new language features are used or the architecture of the library has been significantly changed.

We prefer releasing a new major version not often than once a year.

### MINOR

The MINOR version is incremented when the API has been extended with new functionality. 
The changes in the API might be backward-incompatible, but most of the time they are backward-compatible.

### PATCH

The PATCH version is incremented when some enhancements or fixes are made. The API is untouched in this case.
