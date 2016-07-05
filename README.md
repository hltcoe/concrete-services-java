Copyright 2012-2016 Johns Hopkins University HLTCOE. All rights
reserved.  See LICENSE in the project root directory.

Concrete services
========

Provides Java classes for the
[Concrete](https://github.com/hltcoe/concrete) services schema.

Maven dependency
---
```xml
<dependency>
  <groupId>edu.jhu.hlt</groupId>
  <artifactId>concrete-services-core</artifactId>
  <version>x.y.z</version>
</dependency>
```

Requirements
------------

For building, this project requires the following:
* Java, 1.8 or greater.
* [Apache Maven](http://maven.apache.org/), 3.0.4 or greater
* [Apache Thrift](http://thrift.apache.org/), 0.9.3
* `bash` shell
* A checked out copy of [Concrete][concrete]
* A checked out copy of [Concrete Services][concrete-services]

Installation (*nix only)
------------

Concrete requires `bash` and `thrift` installed and available on your `PATH`.

Additionally, you will need a copy of `concrete-thrift` checked
out. This repository can be closed in *nix via:


```bash
git clone git@github.com:hltcoe/concrete.git
```

Next, set the environment variable `PATH_TO_CONCRETE_FILES`
to the path where the concrete `.thrift` files exist on disk. For example,
if you just cloned the project per above, this would be `$(pwd)/concrete/thrift`.

Next, set the environment variable `PATH_TO_CONCRETE_SERVICES_FILES`
to the path where the concrete services`.thrift` files exist on disk. For example,
if you just cloned that project, it would be `$(pwd)/concrete-services-core/thrift`.

Afterwards, running:

```sh
mvn install
```

will install the code to your local maven repository.

Using the code in your project
------------------------------

Compiled java classes end up in several packages:

``` java
edu.jhu.hlt.concrete.access
edu.jhu.hlt.concrete.annotate
edu.jhu.hlt.concrete.search
```

The Thrift structures generate many classes; additional technical
documentation can be found in the comments of the thrift definitions
themselves, or in the Javadocs.

[concrete]: https://gitlab.hltcoe.jhu.edu/concrete/concrete
[concrete-services]: https://gitlab.hltcoe.jhu.edu/concrete/concrete-services
