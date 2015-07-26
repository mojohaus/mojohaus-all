# Repositories of all the MojoHaus organization

Use `git clone --recursive thatrepo`

NOTE: using the ssh protocol for each submodule for interacting more conveniently with the GitHub remote.

`travis.yml` is an example for a working [Travis configuration](https://travis-ci.org/), just copy it into your project as `.travis.yml`. What this will do is:
* Do a matrix build using Oracle's JDK7 and 8 (available at Travis out of the box) combined with Maven 3.0.5 and Maven 3.3.3 by the help
  of the the [Takari Maven Wrapper](https://github.com/takari/maven-wrapper).
* Downloading the Maven versions is done on the fly so the git repositories are not "polluted" with wrapper code.
* Running `test-compile dependency:go-offline` during the Travis `install` phase will do most of the downloading stuff before
  running the interesting stuff in the Travis `script` phase, i.e. `clean verify`.

